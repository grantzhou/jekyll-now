---
layout: post
title: 数据库每周新闻 2019-8-2
---

## 数据库每周新闻 #264 - 2019年8月2日

![config.yml]({{ site.baseurl }}/images/DBWeekly.png)
备注：[英文原文地址](https://dbweekly.com/issues/264)

![img](<https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/v1564746944/xbsqve5qlclfidkbjbhh.jpg>)

## [Amazon发布了partiql：一种通用的、与SQL兼容的查询语言](https://aws.amazon.com/cn/blogs/opensource/announcing-partiql-one-query-language-for-all-your-data/)

partiql是一种新的查询语言，它将SQL扩展为能够支持非关系、无模式和其他数据格式。它是开源的，已经在各种AWS系统内部使用。几年前，它的一个共同创建者还创建了SQL++（通过CouchBase的N1QL实现了这一点）。

`PAPAKONSTANTINOU, GOO, ET AL.`

## [Dgraph实验室为图形数据库筹集了1150万美元](https://blog.dgraph.io/post/how-dgraph-labs-raised-series-a/)

这篇来自dgraph的文章并没有聚焦于金钱，而是深入探讨了dgraph为什么存在，以及它如何对大多数图形数据库采取不同的方法（通过以图形为核心，而不仅仅是一堆抽象的传统关系)

`MANISH RAI JAIN`

## [利用NIFI和InfluxDB构建物联网数据流](https://www.influxdata.com/blog/building-a-data-stream-for-iot-with-nifi-and-influxdb/?utm_campaign=iot&utm_medium=newsletter&utm_source=cooperpress)

结合NIFI和InfluxDB可产生安全、可访问和可用的物联网数据流。此解决方案支持跨所有设施的单一数据视图，提供主动维护、故障检测等。

`INFLUXDATA`

## [数据库潜力股：CouchDB](https://www.ibm.com/cloud/blog/new-builders/database-deep-dives-couchdb)

10年前，couchdb（一个早期面向文档的nosql数据库）引起了很多关注，但现在它并没有那么多出现在我们的视野中。所以很高兴看到它仍在积极开发中，并且有大量的用例。这篇文章围绕着对两个主要CouchDB团队成员的采访展开。

`JOSH MINTZ (IBM)`

## [数据工程目录](https://github.com/andkret/Cookbook)

一个仍在编写的数据工程目录，试图涵盖数据工程中值得了解的主要思想。这是不完整的，但如果你想了解大局，这足够了。

`ANDREAS KRETZ`



## [了解Azure SQL数据库的SLA](https://azure.microsoft.com/en-us/blog/understanding-and-leveraging-azure-sql-database-sla/)

Azure SQL数据库服务级别协议的两个主要更改：业务关键层中99.995%的可用性SLA，以及地理复制数据库的“业务连续性SLA”。

`ALEXANDER NOSOV (MICROSOFT)`

## [书评：Martin Kleppmann的《设计数据密集型应用程序》](https://henrikwarne.com/2019/07/27/book-review-designing-data-intensive-applications/)

我对这本书非常喜爱，这本书评对这本书的内容进行了相当深入的探讨。一本学习数据建模、查询语言、格式、事务和分布式数据库以及它们如何连接在一起的。

`HENRIK WARNE`



### 💻招聘

在Vettery上找到一份新的开发工作——Vettery专注于技术角色，对求职者来说是完全免费的。

`VETTERY`



### 📒 其他

[对ApacheCassandra的介绍](https://aiven.io/blog/an-introduction-to-apache-cassandra/)—Cassandra不是典型的RDBMS，这个介绍清楚地描述了与Cassandra相关的所有术语的含义。

`JOHN HAMMINK`

[Postgres系数据库AWS Aurora](https://www.percona.com/blog/2019/07/16/brin-index-for-postgresql-dont-forget-the-benefits/)—Amazon Aurora提升了Postgres的兼容性，这具体指什么，它是如何使用的，它的限制是什么。Viorel Tabara带你了解所有的这一切。

`SEVERALNINES`

[引入MongoDB 4.2](https://www.mongodb.com/blog/post/coming-in-mongodb-42-pipeline-powered-updates-and-more-expressive-queries)：管道驱动的更新和更具表现力的查询

`DJ WALKER-MORGAN (MONGODB, INC.)`

[介绍Postgres的并行](https://www.percona.com/blog/2019/07/30/parallelism-in-postgresql/)—介绍了新版本Postgres的并行机制，包括并行顺序扫描、并行聚合和并行B-tree索引扫描和他们加速数据扫描的原理。
`IBRAR AHMED`


[在NEO4J中运行决策树](https://neo4j.com/blog/running-decision-trees-neo4j/)-通过一个非正统的示例，了解NEO4J如何与决策树一起工作，以快速解决现实问题。
`MAX DE MARZI`

[Postgres的组合索引和独立索引](https://www.cybertec-postgresql.com/en/combined-indexes-vs-separate-indexes-in-postgresql/)—在设计数据库关系时，会遇到一个常见的问题，组合索引和单个索引哪一个更有意义。HANS-JÜRGEN研究了Postgres中的一些场景。
`HANS-JÜRGEN SCHÖNIG`

[LiftBridge：轻量级的、容错的消息流](https://github.com/liftbridge-io/liftbridge)—为NATS实现持久的、复制的消息日志的服务器。

`LIFTBRIDGE`