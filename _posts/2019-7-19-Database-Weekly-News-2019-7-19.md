---
layout: post
title: 数据库每周新闻 2019-7-19
---

## 数据库每周新闻 #263 - 2019年7月19日

![config.yml]({{ site.baseurl }}/images/DBWeekly.png)
备注：[英文原文地址](https://dbweekly.com/issues/263)

![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/avyzcxj6dbmynkkcfocy.jpg)

## [基准测试中的MongoDB：“要么做好，要么根本不做”](https://www.mongodb.com/blog/post/benchmarking-do-it-right-or-dont-do-it-at-all)

MongoDB, Inc.对[最近的一个基准测试](https://www.enterprisedb.com/news/new-benchmarks-show-postgres-dominating-mongodb-varied-workloads)做出了回应，该测试显示PostgreSQL在性能方面战胜了MongoDB，但[基准测试进行的很困难](https://www.pingcap.com/blog/why-benchmarking-distributed-databases-is-so-hard/)，并且MongoDB对此并不满意，所以他们用自己的一些基准测试进行了反击。像往常一样，在依赖基准测试之前要考虑所有因素。

`GREG MCKEON (MONGODB, INC.)`

## [Redis Gears：Redis的新脚本语言](https://redislabs.com/blog/introduction-redis-gears/)

对Redis数据结构键/数值存储的一个有趣的补充。Gears是一个新模块，它添加了基于python的、集群感知的脚本语言，用于对数据执行更高级的查询。[GitHub报道。](https://github.com/RedisGears/RedisGears)

`REDIS LABS`

## [DevOps对数据库共存的看法](https://studio3t.com/mongodb-sql-coexistence-whitepaper/?utm_source=cooper&utm_medium=newsletter&utm_campaign=july19)

无论您是在DevOps、开发部门还是数据库管理部门，都可以从Studio 3T免费下载完整的SQL Migration白皮书。

`STUDIO 3T`**赞助商**

![img](https://copm.s3.amazonaws.com/deb4409d.png)

## [YugaByte DB重新定义为100%开源](https://blog.yugabyte.com/why-we-changed-yugabyte-db-licensing-to-100-open-source/)

[YugaByte](https://www.yugabyte.com/)几年前就已经存在了，它是一个高性能的分布式数据库，支持SQL和Cassandra api。而它现在是完全开源的，包括以前的封闭源码和企业特性。

`KARTHIK RANGANATHAN (YUGABYTE)`

## [这就是为什么大数据现在仍然困难重重](https://www.datanami.com/2019/07/15/big-data-is-still-hard-heres-why/)

一篇文章回顾了hadoop驱动的“大数据”时代的十年，并指出随着新技术的扩散和向“云数据”发展的大幅度变化，目标也在不停的变化。

`DATANAMI`

## [在Elasticsearch数据库配置失败中暴露了800万行与酒店相关的代码](https://siliconangle.com/2019/07/16/8m-hotel-records-exposed-latest-elasticsearch-database-configuration-fail/)

如果您没有一个系统来设置和检查所有数据库系统的身份验证和网络访问策略，那么现在是时候开始了。

`SILICONANGLE`

## [问HN：有人在生产中使用CockroachDB吗？](https://news.ycombinator.com/item?id=20472640)

一场骇客新闻探讨，内容涉及[CockroachDB](https://github.com/cockroachdb/cockroach)、分布式SQL数据库、它的用例以及谁在实际使用它。还有一个[关于](https://news.ycombinator.com/item?id=20473985)TiDB、yumb、Citus和MemSQL的有趣解释。

`HACKER NEWS`

## [WePay的流式Cassandra的故事](https://wecode.wepay.com/posts/streaming-cassandra-at-wepay-part-1)

WePay是一个庞大的MySQL用户，但在面临扩展问题时，他们必须决定是分割MySQL还是切换到另一个解决方案。他们和卡桑德拉一起去的。

`JOY GAO (WEPAY)`



### 💻招聘

[在Vettery上找到一份新的开发工作](https://www.vettery.com/tech?utm_source=newsletter&utm_medium=cooper-dbweekly&utm_term=tech&utm_content=grouped&utm_campaign=ad-88878)——Vettery专注于技术角色，对求职者来说是完全免费的。

`VETTERY`

### 📒 教程和故事

[用SQL编写解释器来寻开心](https://www.youtube.com/watch?v=MPSMH8w7nfw)——这取决于你的兴趣，但是很高兴看到这种事情是可能的。我喜欢这句话:“SQL代码是吼叫和关系代数的奇怪组合。”

`MICHAEL MALIS`



[操作分析的SQL查询规划](https://rockset.com/blog/sql-query-planning-for-operational-analytics/)——在基于SQL的事件数据分析系统[Rockset](https://rockset.com/)中，了解如何实现SQL查询规划来支持操作分析需求，比如低延迟和高并发性。

`PURVI DESAI`



[开始在Containers中部署Postgres数据库](https://info.enterprisedb.com/WhitepaperDeployingPostgresDatabasesinContainers-advertising.html?utm_source=Cooperpress&utm_medium=ad)——探索是什么推动了containers的增长，以及containers用例的机会:数据库

`ENTERPRISEDB` **赞助商**



[SQL 301:为什么需要SQL窗口函数](https://dev.to/helenanders26/sql-301-why-you-need-sql-window-functions-part-1-6e1)——窗口函数非常强大，它允许您查看表中的行，其中的新列显示了运行的总数、排名或移动平均线等。

`HELEN ANDERSON`



[从Postgres看图形数据库的远景](https://www.youtube.com/watch?v=JQ0ycS8HqjE)——几周前在Postgres Vision 2019上发表的一个关于AgensGraph的演讲，AgensGraph是一个基于Postgres的多模型图形数据库。音频质量不是很好，但是您可以很好地了解什么是AgensGraph以及它是如何提供帮助的。

`AGENSGRAPH`



[在AWS选项中评估MySQL性能](https://www.percona.com/blog/2019/07/17/assessing-mysql-performance-amongst-aws-options-part-one/)——比较Amazon Aurora、RDS和两个基于Percona服务器的选项。

`ALEXEY STROGANOV (PERCONA)`



[OctoSQL:使用SQL支持的数据源连接、分析和转换来自多个数据源的数据](https://github.com/cube2222/octosql)——支持的源文件有CSV、JSON、MySQL、PostgreSQL和Redis

`JACOB MARTIN`