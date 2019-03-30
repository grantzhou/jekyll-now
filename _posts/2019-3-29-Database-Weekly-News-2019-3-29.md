---
layout: post
title: 数据库每周新闻 2019-3-29
---

## 数据库每周新闻 #247 - 2019年3月29日
![config.yml]({{ site.baseurl }}/images/DBWeekly.png)
备注：[英文原文地址](https://dbweekly.com/issues/247)
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/ujrnhvi0iljfsxwgwgcm.jpg)

## [深入研究Amazon Aurora的设计](https://blog.acolyer.org/2019/03/25/amazon-aurora-design-considerations-for-high-throughput-cloud-native-relational-databases/)
最近的一篇晨报发表了两篇深入探讨亚马逊[Aurora](https://aws.amazon.com/rds/aurora/)数据库系统如何工作的论文。
Aurora是一个MySQL和PostgreSQL兼容的数据库，它使用了许多优化，并且这些文章深入研究了这些优化。 [第二篇论文](https://blog.acolyer.org/2019/03/27/amazon-aurora:-on-avoiding-distributed-consensus-for-i-os,-commits,-and-membership-changes/)涵盖了分布式共识模型。

`ADRIAN COLYER`

## [MongoDB是不是正确的选择？](https://www.simplethread.com/was-mongodb-ever-the-right-choice/)
如果你正在寻找一个狂热赞扬MongoDB的地方，这里不是。
作为数据库世界的一项创新，MongoDB多年来受到了很多批评，但它解决的问题很重要，作者说。（如果您是MongoDB用户，请访问我们的[MongoDB新闻通讯](https://mongodb.email/?ref=db):-)）

`JUSTIN ETHEREDGE`

## [为什么要在你的物联网应用程序中使用关系数据库](https://blog.timescale.com/use-relational-database-instead-of-nosql-for-iot-application/?utm_campaign=db-weekly-sponsor&utm_source=db-weekly-newsletter-mar&utm_medium=referral&utm_content=blog-post-relational)
![img](https://copm.s3.amazonaws.com/17a6b19d.jpg)
不要错误地创建数据孤岛。 使用像TimescaleDB这样的关系数据库，您可以在一个从云到边缘扩展的单个数据库系统中统一时间序列，元数据和地理空间数据。
这就是为什么[Azure与Timescale合作](https://blog.timescale.com/timescale-microsoft-azure-team-up-to-power-iot-and-time-series-workloads/?utm_campaign=db-weekly-sponsor&utm_source=db-weekly-newsletter-mar&utm_medium=referral&utm_content=blog-post-azure)为物联网和时间序列工作负载提供支持的原因。

`TIMESCALE` **赞助商**

## [如何使用Elasticsearch OSS为Elasticsearch SQL插件构建和运行Open Distro](https://aws.amazon.com/blogs/opensource/build-run-sql-plugin-open-distro-elasticsearch-oss/?sc_channel=sm&sc_campaign=Open_Source&sc_publisher=TWITTER&sc_country=Open+Source&sc_geo=GLOBAL&sc_outcome=adoption&trk=_TWITTER&sc_content=blog&linkId=65327932)
我们最近提到了Amazon有争议的[Elasticsearch新发行版](https://aws.amazon.com/blogs/aws/new-open-distro-for-elasticsearch/)，现在我们可以看到它的一部分正在运行：一个允许您[使用SQL查询Elasticsearch存储的插件](https://github.com/opendistro-for-elasticsearch/sql)。

`JON HANDLER`

## [麦当劳3亿美元的大数据收购](https://www.wired.com/story/mcdonalds-big-data-dynamic-yield-acquisition/)
麦当劳凭借其20年来的最大收购，将大数据带入其巨无霸市场。 该计划是使用数据分析来推荐客户更有可能购买的产品。

`BRIAN BARRETT`

## [Neo4j向小公司推出其“启动计划”提供图形数据库技术 ](https://neo4j.com/startup-program/)
[Neo4j图形数据库](https://github.com/neo4j/neo4j)背后的公司已经启动了一项计划，向某些类型的初创公司和小公司开放其企业级产品。

`Neo4j`

### 📖 教程

## [Redis Streams作为纯数据结构](http://antirez.com/news/128)
Redis的创建者，数据结构服务器，将流视为纯数据结构，以及它们如何像“Steroids上的CSV文件”。

`SALVATORE SANFILIPPO`

## [计算不同索引数据的最佳方法](https://www.peterbe.com/plog/best-way-to-count-distinct-indexed-things-in-postgresql)
计算子查询结果的效率比尝试在单个查询中使用DISTINCT进行计数要高效得多。

`PETER BENGTSSON`

## [电子书：如何在Postgres数据库中获得3倍的性能提升](https://pganalyze.com/ebooks/optimizing-postgres-query-performance?utm_source=DBWeeklySecondary)
了解为Atlassian等客户优化Postgres查询性能的最佳实践，以及如何将磁盘加载的数据减少500倍。

`PGANALYZE` *赞助商*

## [Postgres中的索引：了解B-Tree](https://habr.com/en/company/postgrespro/blog/443284/)
[最新的一系列广泛的帖子](https://habr.com/en/company/postgrespro/blog/441962/)深入探讨了Postgres中索引的工作原理。

`EGOR ROGOV`

## [加速GROUP BY](https://www.cybertec-postgresql.com/en/speeding-up-group-by-in-postgresql/)
SQL的GROUP BY通常用于将结果集中的记录组合在一起以进行汇总/聚合，作者声称有一种方法可以加速这些操作并获得一些“免费”的额外性能。

`HANS-JÜRGEN SCHÖNIG`

### 📖 科技文章与行业见解

## [我们如何将大规模并行Postgres DB移动到Kubernetes上](http://engineering.pivotal.io/post/how_we_moved_a_massively_parallel_postgres_database_onto_kubernetes/)

`OZ BASARIR（PIVOTAL）`

## [如果你已经使用SQL Server一段时间，你会发现一些你会知道的数字](https://sqlservercode.blogspot.com/2019/03/some-numbers-that-you-will-know-by.html)
对于SQL Server用户来说，这是一个轻松愉快的话题。 我认为每个数据库都可以有相同的文章！

`DENIS GOBO`

## [两个查询的故事：支持ANSI-89 SQL JOIN语法！](https://sqlha.com/2019/03/25/a-tale-of-two-queries/)
我必须承认，这也是我仍然使用“Join”的方式。👴🏻

`ALLAN HIRT`

### 🛠 代码 & 工具

## [automl-gs：在CSV文件上快速执行机器学习](https://github.com/minimaxir/automl-gs)
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/gz2bjknkbv23t7hahi7h.jpg)
好吧，标题并没有完全理解它是什么，但它很整洁。 为automl-gs提供一个CSV文件，它将创建一个模型，用于预测您可以从Python中选择的字段的值。

`MAX WOOLF`

## [Bitraft：使用Raft实现与Redis兼容API的Bitcask分布式键/值存储](https://github.com/prologic/bitraft)
[Bitcask](https://github.com/prologic/bitcask)既是高性能Go键/值存储，也是Riak使用的存储格式。 Bitraft增加了Raft的支持以分发数据。

`JAMES MILLS`

## [csvq：在CSV文件上使用类似SQL的查询语言](https://github.com/mithrandie/csvq)
包括交互式REPL。

`MITHRANDIE`


