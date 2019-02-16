---
layout: post
title:  PostgreSQL 11中的新功能
---

[原文链接]https://modern-sql.com/blog/2019-02/postgresql-11#footnote-0）

## PostgreSQL 11中的新功能
PostgreSQL 11在四个月前就发布，我的评论本应早就发出。 让我们现在开始！

除了标准SQL外，PostgreSQL 11中的特色是窗口函数（over）。 
近8年来，从2009年到2017年，PostgreSQL是唯一支持SQL窗口功能的免费开源产品。
仅仅一年之后，[到2018年9月，所有开源竞争对手都赶上来了](https://modern-sql.com/blog/2019-01/sqlite-in-2018#window-functions)......
[有些甚至超过了PostgreSQL](https://modern-sql.com/blog/2018-04/mysql-8.0#window-functions)。
PostgreSQL社区已经做好准备，[PostgreSQL 11于2018年刚刚发布](https://www.postgresql.org/about/news/1894/)，它已经恢复甚至扩大了其领导地位。<sup>[0](#myfootnote0)</sup>

本文解释了这方面的竞争，并介绍了PostgreSQL 11中的其他改进。

内容包括:

<sup>[1. 完整的SQL:2011 **Over** 子句](#titleh1)</sup>

<sup>[2. 创建及调用 Procedure](#titleh2)</sup>

<sup>[3. **Fetch First|Next**中的参数](#titleh3)</sup>

<sup>[4. 相对XPath表达式](#titleh4)</sup>

<sup>[5. 其他新闻](#titleh5)</sup>

<sup>[6. 附加内容: `Create Index … Include`](#titleh6)</sup>


## <a name="titleh1">1. 完整的SQL:2011 **Over** 子句</a>
over子句定义哪些行对窗口函数可见。 窗口函数最初使用SQL：2003标准，PostgreSQL自PostgreSQL 8.4（2009）以来一直支持它们。 在某些领域，PostgreSQL实现不如其他实现（**range**构成，**ignore nulls**）完整，但在其他领域，它是第一个支持它们的主要系统（**window**子句）。 一般来说，PostgreSQL与商业竞争对手非常接近，它是迄今为止唯一支持窗口功能的主要免费数据库。

2017年，MariaDB推出了窗口功能。 MySQL和SQLite紧随其后在2018年也推出此功能。那时，over子句的MySQL实现甚至比PostgreSQL更完整，这是PostgreSQL 11关闭的一个空白。 此外，PostgreSQL再次支持over子句的某些方面，即<sup>[帧单元组](#framunitgroups)</sup>(Frame Unit **groups**)和<sup>[帧排除](#framexclusion)</sup>(frame exclusion)。 任何其他主要的SQL数据库都不支持这些 - 无论是开源还是商业。

PostgreSQL 11不支持的唯一over子句是**pattern**和相关子句。 这些子句属于 SQL:2016 标准，并基于正则表达式进行框架化。 
目前没有主流数据库支持这种框架。<a name="myfootnote1">1</a>

### <a name="framunitgroups"> 帧单元组(Frame Unit **groups**) </a>
在研究PostgreSQL 11中的新功能之前，我将向您展示一个典型的窗口函数用例。 然后我们可以进行所谓的框架（*framing*）。

该例子计算列amnt上的运行总计，因此根据指定的**order by**子句计算当前行之前和之前所有行的总和：

<pre>
SELECT SUM(amnt)
       OVER(ORDER BY id
            <b>ROWS BETWEEN UNBOUNDED PRECEDING
                    AND CURRENT ROW</b>
           ) running_total
 FROM …
</pre>

聚合函数**sum**与**over**子句一起使用，而不是与group by子句一起使用 - 这使它成为一个窗口函数。 这个例子中有趣的部分是框架(framing)，以**粗体**显示。

窗口框架将有序窗口缩小到指定的开始行和结束行之间的行。

一般语法是:
> <unit> BETWEEN <window frame bound>
>           AND <window frame bound>
> [<frame exclusion>]

让我们从窗口框架边界开始，即框架开始和结束的定义。

窗口框架边界可以相对于当前行的术语指定，或者它们可以是“无界”的。 Unbounded指的是当前结果或分区的开始或结束。
>  CURRENT ROW
>| <distance> (PRECEDING|FOLLOWING)
>| UNBOUNDED  (PRECEDING|FOLLOWING)

以下帧定义使用相对于当前行的帧边界。
><unit> BETWEEN 1 PRECEDING AND CURRENT ROW
  
要真正理解相对边界的含义，我们还必须了解三个框架单元 - 行，范围和组(rows, range, 和 groups) - 如何改变这些边界的含义。

行单元(rows unit)正如您所期望的那样：它将当前行解释为引用当前行，并将前面和后面的<distance>解释为行数。 对于行单元，前一个示例定义了一个包含最多两行的帧：一行在当前行之前，另一行在当前行本身。 如果当前行之前没有行，例如 因为当前行是第一行，所以框架只覆盖当前行本身。
  
![_config.yml]({{ site.baseurl }}/images/pgn1.png)

下一个帧单位,**range**,根本不计算行数。 相反，它使用排序键的值（按表达式排序）并添加或减去指定的<distance>。 排序键的值落入指定范围的所有行都将被带入帧中。

请注意，当前行(**current row)作为范围(**range**)绑定是指与当前行具有相同值的所有行。 那可以是很多行。 将当前行视为前面的0或后面的0 <sup>[2](#myfootnote2)</sup>。如果是范围，“当前对等”或“当前值”可能是比当前行更好的选择。

下图使用单位范围而不是行。 由于当前行的值为2，因此框架将覆盖值为1到2（包括）的所有行。 帧从第一行开始，因为它的值是1，因此落入值范围。 帧的结尾甚至超出当前行，因为下一行仍然落在值范围内。

![_config.yml]({{ site.baseurl }}/images/pgn2.png)

这是一个适用于MySQL 8.0的示例，但不适用于版本11之前的PostgreSQL。虽然PostgreSQL之前支持范围帧，但您无法使用如上所示的数字距离。 在PostgreSQL 11之前只能使用无界和当前行。顺便说一句，SQL Server和SQLite仍然如此。 PostgreSQL 11支持具有所有边界类型的所有帧单元。

`代表我自己`
`我靠培训，其他SQL相关服务和销售我的书来谋生。 通过 https://winand.at/ 了解更多信息。`

PostgreSQL 11完全支持最后一个帧 - **groups**。组将结果或分区的每一行分配到一个组中，就像group by子句一样。 然后，<distance>指的是当前行之前和之后要覆盖的组的数量，即不同的排序键值的数量。

下图显示了组帧如何在当前值（前一个）和当前值本身（当前行）之前覆盖一个不同的值。 值之间的数字差异无关紧要，行数也不重要。 组仅仅是关于不同值的数量。
![_config.yml]({{ site.baseurl }}/images/pgn3.png)

PostgreSQL 11是第一个支持组帧的主要SQL数据库。

![_config.yml]({{ site.baseurl }}/images/pgn4.png)
![_config.yml]({{ site.baseurl }}/images/pgn5.png)
![_config.yml]({{ site.baseurl }}/images/pgn6.png)
![_config.yml]({{ site.baseurl }}/images/pgn7.png)
![_config.yml]({{ site.baseurl }}/images/pgn8.png)
![_config.yml]({{ site.baseurl }}/images/pgn9.png)


### <a name="framexclusion"> 帧排除(frame exclusion) </a>
  
## <a name="titleh2">2. 创建及调用 Procedure</a>

## <a name="titleh3">3. **Fetch First|Next**中的参数</a>

## <a name="titleh4">4. 相对XPath表达式</a>

## <a name="titleh5">5. 其他新闻</a>

## <a name="titleh6">6. 附加内容: `Create Index … Include`</a>

## 关于作者
---
<img align="left" width="100" height="100" src="https://modern-sql.com/static/markuswinand.5Ot1gTRt.jpg">
Markus Winand教授高效的SQL - 现场或者在线课程。 他使用现代SQL来最小化开发时间，并通过智能索引优化运行效率。
他的名为SQL Performance Explained的书已成为标准阅读。
---

### 在亚马逊上购买他的书
---
<img align="left" width="100" height="100" src="https://modern-sql.com/static/9783950307825_w220.d9ybRqoS.jpg">
The essence of SQL tuning in 200 pages
SQL调优的精髓 200页
[在亚马逊上购买](https://sql-performance-explained.com/r/local-amazon?utm_content=promo-book&utm_source=modern-sql.com&utm_campaign=blog-2019-01-postgresql-11&utm_medium=web)
(只有印刷版)
*[Markus的商店](https://sql-performance-explained.com/?utm_content=promo-book&utm_content=text&utm_source=modern-sql.com&utm_campaign=blog-2019-01-postgresql-11&utm_medium=web)有印刷版和PDF版本*

---

### 雇佣Markus
Markus为在任何规模的公司工作的开发人员提供SQL培训和咨询。
[查看更多](https://winand.at/)

## 脚注
<a name="myfootnote0">0</a>: PostgreSQL现在已经成为over子句的领导者。
在考虑支持的窗口函数时，由于PostgreSQL缺乏支持窗口函数中的*respect|ignore nulls*子句，因此可能与Oracle数据库排名类似。
在考虑运行时行为时，Oracle数据库可能会获胜，因为它可以根据单调推进窗口函数的结果正确应用Top-N优化（与PostgreSQL不同）。.

<a name="myfootnote1">1</a>: Oracle Database 12c支持与from中的match_rocognize子句匹配行模式，但不支持**over**。

<a name="myfootnote2">2</a>: SQL：2016-2：§7.15GR5bi3EII 甚至明确提到了关于**groups**这一点


<a name="myfootnote2">3</a>: 我认为这是一个专有扩展。 SQL：2016-2：§4.33.2“SQL调用例程的特性”第一段将SQL例程（过程和函数）的事务控制语句限制为与保存点相关的语句。
