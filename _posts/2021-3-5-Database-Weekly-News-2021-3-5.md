---
layout: post
title: 数据库每周新闻 2021-3-5
---
### 数据库每周新闻#344 - 2021年3月5日
![_config.yml]({{ site.baseurl }}/images/DBWeekly.png)
备注：[英文原文地址](https://dbweekly.com/issues/344)
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/mq5rff2zgbd2mfalului.jpg)


## [sq：用于数据的通用瑞士军刀](https://dbweekly.com/link/104215/web)
周围有很多“瑞士军刀”式的数据“工具”（例如xsv用于CSV或jq用于JSON）–认为这就像jq，但对于所有 各种格式和系统。 您可以将Excel工作表导入Postgres表，将查询结果从SQL Server移至SQLite，将整个数据库导出为CSV。 支持多种格式，到目前为止，支持的数据库包括Postgres，SQLite，SQL Server和MySQL。

`Neil O'Toole`


## [Clickhouse作为ElasticSearch和MySQL的替代品](https://dbweekly.com/link/104218/web)
Clickhouse是一个面向列的开源OLAP系统，作者讨论了如何以及重要的是他的团队将其用于项目的日志存储和分析的原因。

`Anton Sidashin`


## [[指南]如何计算数据库的真实成本](https://dbweekly.com/link/104220/web)
使用本指南可将您的许可成本，运营开销成本，基础架构成本以及两者之间的所有费用加起来-这样您就可以清楚地了解自己的支出（以及支出地点） 您可以花更少的钱）。

`CockroachDB sponsor`


## [Google Cloud Memorystore：它是托管的memcached](https://dbweekly.com/link/104221/web)
memcached是一个长期存在的内存对象缓存系统，最初是在LiveJournal（！）上创建的，而Google Cloud Platform拥有自己的托管的Memcached系统，称为Memorystore，现已普遍可用。

`Google Cloud`


## [回顾2011年以及Hadoop的兴起](https://dbweekly.com/link/104223/web)
Datanami是我们经常链接到的来源，它是数据科学和分析领域的重要新闻站点，并且他们通过回顾2011年的情况来庆祝自己的10岁生日。 他们说Hadoop在今天几乎是一个“脏话”，但在2011年，它是“大数据酷度”的最前沿。

`Datanami`

## [如何通过BigQuery ML在Google表格中使用机器学习模型](https://dbweekly.com/link/104227/web)
电子表格不会很快消失，因此任何涉及将现代数据科学实践引入电子表格的项目都会立即引起我的兴趣。

`Karl Weinmeister (Google Cloud)`


## [使用Python和Pandas在Postgres内部构建推荐引擎](https://dbweekly.com/link/104228/web)
了解如何直接在Postgres内部利用Python和Pandas（一种流行的数据分析工具）来构建自己的推荐引擎。

`Craig Kerstiens`


## [使用适用于Apache Flink的Amazon Kinesis Data Analytics创建Amazon Timestream插值视图](https://dbweekly.com/link/104230/web)
标题中听起来有些时髦的宾果游戏，是吗？ 这里的想法是建立一个流数据管道，在摄取期间生成聚合，以使仪表板（在本例中为QuickSight）能够更快地进行最终查询。

`Will Taff and John Gray (AWS)`


## [迁移到Aurora：轻松，除了账单外](https://dbweekly.com/link/104231/web)
“将我们的生产数据库从Postgres迁移到Aurora很容易，直到我们注意到我们的日常数据库成本增加了一倍以上。” 幸运的是，尽管他们对这一举动似乎有些矛盾，但他们继续减轻了这种负担。

`Kimberly Nicholls`


## [如何为您的应用程序有效地选择正确的数据库](https://dbweekly.com/link/104232/web)
请注意，这是在PingCAP的博客（TiDB的创建者，一个开放源代码的分布式SQL数据库）上，因此请注意偏见。 尽管如此，这里还是提出了一些合理的问题，并且作者在他们的系统中使用了多个数据库（包括MySQL，Redis和Couchbase）。

`Leitao Guo`


## [与SQL Server的Azure相比，AWS声称“性能更佳”](https://dbweekly.com/link/104234/web)
难道这是AWS独占their头吗？ 是的。 但这只是他们与Microsoft在运行SQL Server工作负载方面持续竞争中的又一小步。 看到Azure重新回到这一点很有趣。

`Fred Wurden (AWS)`


## [在Azure上提供更好的Redis体验](https://dbweekly.com/link/104233/web)
我们不想被偏见，所以也让Azure做些啦啦队-这篇文章涵盖了针对Redis的Azure缓存的新企业级产品（Azure的托管Redis服务）。

`Kyle Teegarden (Microsoft)`


## [使用Google BigQuery和Cloud Run构建库存管理系统](https://dbweekly.com/link/104235/web)

`Aja Hammerly (Google Cloud)`

## 🛠项目和工具

## [OrbitDB：分散式Web的对等数据库](https://dbweekly.com/link/104236/web)
一种无服务器的，分布式的，对等数据库，使用IPFS进行存储并在对等节点之间自动同步。 目前仅限于Node和浏览器用例，这里是入门指南。

`OrbitDB Community`


## [使用Studio 3T Enterprise通过5个步骤将SQL数据库导入到MongoDB中](https://dbweekly.com/link/104238/web)
将整个SQL数据库导入MongoDB的最简单方法是使用Studio 3T及其创新的SQL迁移功能。

`Studio 3T sponsor`


## [TerminusDB 4.2：开源图形数据库和文档存储](https://dbweekly.com/link/104239/web)
TerminusDB的目标是“知识基础”类型的用例，在这些用例中，诸如不变性，数据沿袭和协作之类的事情非常重要。 它不是典型的图形数据库，尤其是因为它是在Prolog中内置的！

`Luke Feeney`


## [ScalarDB 3.0：使非ACID分布式数据库符合ACID的Java库](https://dbweekly.com/link/104242/web)
Scalar本身并不是一个数据库，而是一个Java客户端，它扩展了您可能正在使用的其他数据存储（例如Cassandra）的功能。

`Scalar`

## 💻招聘

## [X-Team（远程）的DevOps工程师](https://dbweekly.com/link/104243/web)
加入最有活力的开发人员社区，并参与Riot Games，FOX，Sony，Coinbase等项目。

`X-Team`
