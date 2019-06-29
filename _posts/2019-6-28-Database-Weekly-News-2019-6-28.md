---
layout: post
title: 数据库每周新闻 2019-6-28
---

## 数据库每周新闻 #260 - 2019年6月28日
![config.yml]({{ site.baseurl }}/images/DBWeekly.png)
备注：[英文原文地址](https://dbweekly.com/issues/260)
![img](<https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/oznmvemhqzly31jmrymk.jpg>)

## [使用AWK和R解析25TB的数据](https://livefreeordichotomize.com/2019/06/04/using_awk_and_r_to_parse_25tb/)
这是一个有趣的视角，可以看到几个处理大数据集的方法。你可以在这里获取别人的经验教训来完善你的最终方案。

`NICK STRAYER`

## [在MongoDB World上预览的MongoDB 4.2版本](https://www.mongodb.com/blog/post/mongodb-42-previewed-at-mongodb-world)
MongoDB 4.2版本将包含新功能-下面将介绍其中的四个功能，包括分布式事务和客户端字段级加密。

`DJ WALKER-MORGAN (MONGODB)`

## [studio 3t使SQL迁移到mongodb变得非常简单](https://studio3t.com/knowledge-base/articles/import-sql-database-to-mongodb/?utm_source=cooper&utm_medium=newsletter&utm_campaign=june13)
现在，您可以使用Studio3T及其新的SQL迁移功能将整个SQL数据库导入MongoDB。

`STUDIO 3T`



## [Postgres 12的主要功能](https://momjian.us/main/writings/pgsql/features.pdf)

著名的Postgres专家Bruce Momijan发布了一个文档，重点介绍了Postgres12的新功能和显著的改善。，包括jit编译和并发reindex，仅需要1分钟就可以读完。

`BRUCE MOMIJAN`

## [云现在是数据库的默认平台，整个数据库市场正在增长](https://www.datanami.com/2019/06/26/cloud-now-default-platform-for-databases-gartner-says/)
Gartner说，云部署占增长的68%，主要是在AWS和Azure上。然而，尽管云部署正迅速成为“默认”，但云仅占市场收入的23%，因此还有很长的路要走。

`DATANAMI`

## [新的Redis基准达到2亿次/秒](https://redislabs.com/blog/redis-enterprise-extends-linear-scalability-200m-ops-sec/)

Redis实验室推出了企业版的数据结构存储Redis，每秒高达2亿次操作，40个EC2实例的延迟时间低于1毫秒，比去年的类似测试提高了4倍。

`REDIS LABS`



## [用Kaggle Kernels分析BigQuery数据](https://cloud.google.com/blog/products/data-analytics/analyze-bigquery-data-with-kaggle-kernels-notebooks)

Kaggle是一种面向数据科学家的社交网络/共享平台，谷歌在2017年收购了它，现在它已经集成到BigQuery中，使BigQuery用户能够使用Kaggle的简洁分析工具。

`GOOGLE CLOUD`



**简介**

- Redis6正在开发中，[将于今年12月发布](https://twitter.com/RedisLabs/status/1144242384189788160)。
- MongoDB推出了[Atlas Data Lake](https://www.mongodb.com/blog/post/mongodb-atlas-data-lake-debuts-at-mongodb-world)，这是一项使用MongoDB的查询语言查询存储在AmazonS3存储桶中的数据的服务。
- EnterpriseDB已被一家私人股本公司[收购](https://www.prnewswire.com/news-releases/enterprisedb-acquired-by-great-hill-partners-300875303.html)。
- MongoDB的首席执行官在CNBC向Jim Cramer解释[MongoDB为何比Oracle更具优势](https://www.cnbc.com/video/2019/06/20/mongodb-ceo-explains-why-the-company-has-an-edge-over-oracle-in-database.html)。
- Oracle已经[推出了自主数据库专用服务](https://venturebeat.com/2019/06/26/oracle-launches-autonomous-database-dedicated-for-enterprise-customers/)，这是一项以企业为中心的服务，提供自主数据库基础设施管理。



### 💻招聘
[高级软件工程师（Santa Barbara or Remote）](https://www.invoca.com/company/job-listings/?gh_jid=4293087002&gh_src=2cce24422)-加入一个团队，每个人都在努力不断地提高他们对软件开发工具、实践和过程的知识。
`CARBON FIVE`

[在Vettery上寻找数据库有关的工作](https://www.vettery.com/tech?utm_source=newsletter&utm_medium=cooper-dbweekly&utm_term=tech&utm_content=grouped&utm_campaign=ad-88878) – Vettery专门为科技领域的求职者提供相关工作并完全免费。
`VETTERY`

### 📒 教程和故事

[使用Amazon DynaModb进行高级NoSQL数据建模](https://www.youtube.com/watch?v=nhUtZ7suZWI)-这是一系列YouTube视频中最新的一个，这些视频深入使用了Amazon的可扩展NoSQL数据库DynaModb。DynaModb在工作方式上非常独特，因此如果您打算使用它，类似这样的内容是很有价值的。

`AMAZON WEB SERVICES`

[使用NIFI&influxdb为物联网构建数据流](https://www.influxdata.com/blog/building-a-data-stream-for-iot-with-nifi-and-influxdb/?utm_campaign=iot&utm_medium=newsletter&utm_source=cooperpress)-结合NIFI&influxdb可实现安全、可访问和可用的物联网数据流。此解决方案支持跨所有设施的单一数据视图，提供主动维护、故障检测等。

`INFLUXDATA `



[PostgreSQL中假设索引的介绍](https://www.percona.com/blog/2019/06/21/hypothetical-indexes-in-postgresql/)-想一下为什么要为Postgres创建虚拟索引呢？这是一种有意义的方法，它可以在你真的创建一个索引之前，判断你将要创建的索引是否有用。

`AVINASH VALLARAPU`



[使用AWS lambda分析大规模数据处理的性能和成本](https://aws.amazon.com/cn/blogs/apn/analyzing-performance-and-cost-of-large-scale-data-processing-with-aws-lambda/) -- 无服务器方法不适用于每个数据分析用例，但是AWS lambda的低TCO和灵活性有很大的用处。

`AMAZON WEB SERVICES`



[sqlsmith：蟑螂数据库中的随机SQL测试](https://www.cockroachlabs.com/blog/sqlsmith-randomized-sql-testing/)--随机测试允许您自动发现有趣的测试用例，这些测试用例很难自己找到，蟑螂数据库采用了超弹性SQL数据库的思想。

`MATT JIBSON (COCKROACH LABS)`



[MongoDB打算使用简单粗暴的方式来阻止攻击]( https://www.wired.com/story/field-level-encryption-databases-mongobd/)--MongoDB一直在研究一种新的加密方案，该方案有助于保持客户数据的安全性。

`LILY HAY NEWMAN (WIRED)`



[怎样设置数据库清理策略]( https://blog.overops.com/spring-cleaning-at-overops-how-and-why-we-changed-our-db-cleaning-strategy/)--我们的数据库经过长时间的运行，数据库的磁盘空间开始耗尽，下面僵尸解决这个问题的方法。

`AVIV DANZIGER`



[RedistimeSerie：一个用于处理时间序列数据的Redis模块](https://redislabs.com/blog/redistimeseries-ga-making-4th-dimension-truly-immersive/)-Redis已经非常适合于时间序列的工作，但这引入了一些很酷的新功能，如流上的定时保留策略、降采样以及与其他工具的集成。

`REDIS LABS`