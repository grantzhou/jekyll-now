---
layout: post
title: PostgreSQL 每周新闻 2020-7-22
---
### PostgreSQL每周新闻#365 - 2020年7月22日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)
备注：[英文原文地址](https://postgresweekly.com/issues/365)
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/v1595411808/vqjkbubxjggoojnbjgyp.png)

## [用PostgreSQL重建YikYak](https://postgresweekly.com/link/92177/web)
YikYak是一个匿名的社交网络，它利用你的位置向你展示你周围5公里处的发布者， 您可以使用Postgres的地理坐标支持重新创建它。


`Adam Fallon `
## [pgwatch2 v1.8.0发布](https://postgresweekly.com/link/92178/web)
pgwatch2是一个流行的Postgres监控工具，现在它支持Pgpool II、postgres13和TimescaleDB metrics存储。

`Kaarel Moppel `

## [实时Postgres性能监控](https://postgresweekly.com/link/92179/web)
收集现成的和定制的Postgres指标，并将它们与分布的基础设施和应用程序中的数据关联起来。用Datadog免费试用14天。

`Datadog `

## [在不加长时锁的情况下对大表进行分区](https://postgresweekly.com/link/92180/web)
你有一个巨大的表，你需要对它进行分区，但是你需要这个表对你的应用程序保持可用。你应该怎么做？Andrey有一个秘密武器。

`Andrew Dunstan `

## [为LIKE和ILIKE语句获得更多性能](https://postgresweekly.com/link/92181/web)
我们的本周小贴士（以下）包括模式匹配和LIKE，但如果这并不足以支撑生产环境，你想加速性能呢？这里有解决办法！

`Hans-Jürgen Schönig `

## [GROUPING SETS和NULL](https://postgresweekly.com/link/92182/web)
我们在第359期中的技巧是关于分组集的，一种在查询中执行分组的方法，它比简单的按列分组要复杂得多。Bruce研究了使用分组集和空值之间的关系。


`Bruce Momjian `
## [用Postgres表示日期、时间和间隔](https://postgresweekly.com/link/92184/web)
Postgres附带了一组与日期和时间相关的内置数据类型。但为什么要在字符串或整数上使用它们呢？这里是一个概述，看看为什么，以及如何有效地这样做。

`RapidLoop `

## [💻在线研讨会：提高Postgres插入性能的5种方法](https://postgresweekly.com/link/92185/web)
8月19日加入我们，学习五个简单但强大的技术，以增强您的PostgreSQL写入性能。

`Timescale `

## [用Python检查Postgres目录](https://postgresweekly.com/link/92186/web)
MarkRyan研究了如何最大限度地利用数据库元数据——通过编写一个程序来自动提取其中包含的信息。

`Towards Data Science `

## [用springbootjpa生成和管理Postgres模式迁移](https://postgresweekly.com/link/92187/web)


`Muhammad Haroon `
## [在Postgres中使用PEM提高性能：Postgres调优向导和性能诊断](https://postgresweekly.com/link/92188/web)
▶为期一小时的网络研讨会，讲解如何使用EDB的Postgres Enterprise Manager（PEM）GUI。


`EDB `
# 💡本周提示


如果您需要在不设置全文搜索的情况下过滤超出常规比较或相等的查询结果，您有什么选择？LIKE可能是最著名的：


```
SELECT * FROM people WHERE name LIKE 'Sam%';
  
// All 'people' whose names start with 'Sam' here
```


我也希望这样的查询不区分大小写：


```
SELECT * FROM people WHERE name ILIKE 'sam%';
  
// 'SAM', 'sAMantha', etc. would be picked up
```


但你知道还有其他选择吗？


like TO是like，但它使用SQL的正则表达式标准定义来进行匹配（这意味着您仍然可以得到%作为一种.*等价物）：


```
SELECT * FROM people WHERE name SIMILAR TO '(Pat|Sam)%';
  
// Rows where name starts with Pat.. or Sam..
```


如果您喜欢POSIX样式的正则表达式（我也喜欢！）您还可以使用诸如~（case sensitive）和~*（不区分大小写）之类的运算符：


```
SELECT * FROM people WHERE name ~* '(Pat|Sam).*';
```


这个技巧只是为了激起您的兴趣，但是模式匹配文档中还有很多内容。您需要注意效率，如果您在大规模操作（否则您可能需要使用真正的全文索引和搜索），那么只在表的子集上运行这样的查询，但是对于许多情况，Postgres的正则表达式和模式匹配支持就可以了。
