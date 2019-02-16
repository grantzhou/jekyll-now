---
layout: post
title:  PostgreSQL 11中的新功能
---

[原文链接】（https://modern-sql.com/blog/2019-02/postgresql-11#footnote-0）

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

PostgreSQL 11不支持的唯一over子句是**pattern**和相关子句。 这些子句属于 SQL:2016 标准，并基于正则表达式进行框架化。 目前没有主流数据库支持这种框架

### <a name="framunitgroups"> 帧单元组(Frame Unit **groups**) </a>
在研究PostgreSQL 11中的新功能之前，我将向您展示一个典型的窗口函数用例。 然后我们可以进行所谓的框架（*framing*）。

该例子计算列amnt上的运行总计，因此根据指定的**order by**子句计算当前行之前和之前所有行的总和：

```
SELECT SUM(amnt)
       OVER(ORDER BY id
            **ROWS BETWEEN UNBOUNDED PRECEDING**
                    **AND CURRENT ROW**
           ) running_total
  FROM …
```

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

![_config.yml]({{ site.baseurl }}/images/pgn2.png)
![_config.yml]({{ site.baseurl }}/images/pgn3.png)
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
在考虑运行时行为时，Oracle数据库可能会获胜，因为它可以根据单调推进窗口函数的结果正确应用Top-N优化（与PostgreSQL不同）。

