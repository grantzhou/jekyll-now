---
layout: post
title: 数据库每周新闻 2021-1-8
---
### 数据库每周新闻#336 - 2021年1月8日
![_config.yml]({{ site.baseurl }}/images/DBWeekly.png)
备注：[英文原文地址](https://dbweekly.com/issues/336)
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/sgsagbkbipxpqwgvasuo.jpg)


## [使用校验和来验证同步100M数据库记录](https://dbweekly.com/link/100986/web)
Shopify工程师考虑了以下挑战：使用SQL快速检查两个数据存储是否同步。

`Simon Hørup Eskildsen`


## [随着数据爆炸性的增长，Presto有望迎来突破性的一年](https://dbweekly.com/link/100987/web)
Presto是在Facebook上开发的联合SQL查询引擎，是Apache Hive的后续产品，并且其普及度正在不断提高。 Facebook使用它对多个内部数据存储（包括其300PB数据仓库）执行交互式查询。

`Alex Woodie`


## [试用DataStax Astra DBaaS | 5 GB免费试用](https://dbweekly.com/link/100988/web)
使用Astra（适用于现代数据应用程序的开源产品）快速构建云原生应用程序。 使用Astra，您可以使用REST，GraphQL，CQL和JSON / Document API更快地构建架构。 [立即尝试](https://dbweekly.com/link/100989/web)。

`DataStax Astra sponsor`


## [为什么CockroachDB和PostgreSQL可互相兼容](https://dbweekly.com/link/100990/web)
作为其他数据库的构建基础，Postgres及其有的协议的地位不断提高，CockroachDB故意实现了Postgres兼容性，以此作为“可被驱动程序，现有代码和开发人员生态系统访问的方式” 。 我敢肯定，我们会在2021年看到更多此类信息。

`Raphael 'kena' Poss`


## [TimescaleDB 2.0 GA发布：时间序列的PB级关系数据库](https://dbweekly.com/link/100991/web)
我们在10月发布了TimescaleDB 2.0，但现在它正式成为了GA。 2.0能给我们带来什么？ 社区版中添加了分布式超表，用户定义的操作以及一系列企业功能。

`Ajay Kulkarni and Mike Freedman (Timescale)`


## [PostgreSQL是DB-Engines的“2020年度DBMS”](https://dbweekly.com/link/100993/web)
DB-Engines是流行的DBMS知识库，并且根据普及率的增长，每年都有“年度DBMS”。 MySQL在2019年获得了荣誉。

`Paul Andlinger and Matthias Gelbmann`


## [使用Amazon EventBridge摄取MongoDB地图集数据](https://dbweekly.com/link/100995/web)
EventBridge是一种AWS服务，提供事件总线，用于将各种SaaS应用程序和其他AWS服务捆绑在一起。

`James Beswick (AWS)`


## [使用Amazon DocumentDB的读取自动缩放功能](https://dbweekly.com/link/100996/web)
Amazon Document DB（具有MongoDB兼容性）是AWS的MongoDB（主要是兼容）的文档数据库服务，并且由于存储和计算是分离的，因此缩放非常灵活，如此处所示。

`Randy DeFauw (AWS)`


## [AskGit SQL的平均Pull Merge请求时间](https://dbweekly.com/link/100997/web)
AskGit是一个开源命令行工具，用于在git存储库上运行SQL查询。

`Patrick DeVivo`


## [用于增加HDD容量的新硬盘写头分析技术](https://dbweekly.com/link/100999/web)
我们正在进行一些相当令人费解的研究，其中涉及对HDD写头的磁化动力学进行成像，以最终增加硬盘驱动器的容量。

`Tohoku University`


## [数据库Jiu Jitsu：ScyllaDB如何开源兼容DynamoDB的API](https://dbweekly.com/link/101000/web)
▶Corey Quinn（您可能在AWS的上周和他幽默的Twitter snark中认识过）与ScyllaDB的首席执行官一起讨论了供应商锁定，开源经济以及 ScyllaDB正在做什么。

`ScyllaDB`


## [细分数据库：从AWS最近的AWS存储日开始，为什么S3是构建数据湖的最佳选择](https://dbweekly.com/link/101001/web)
▶这基本上是20分钟的时间，将各种想法联系在一起，如果您正在使用或考虑使用S3进行文件存储以外的其他操作，则可能会很有用。
`Matt Sidley (AWS)`

## 🔨 代码和工具

## [另一个Redis Desktop Manager 1.4.0](https://dbweekly.com/link/101002/web)
一个用于Redis的开源桌面客户端，它承诺如果处理大量密钥，它不会崩溃。 支持TLS，暗模式等–作者似乎在这里付出了很多努力。

`qii404`


## [simple-graph：基于SQLite的简单图形数据库](https://dbweekly.com/link/101004/web)
借助其递归CTE支持，无论如何您都可以在SQLite上建立图形数据库，但如果您是Pythonista使用者，您可能会发现这种抽象层很有趣。

`Denis Papathanasiou`


## [CYBERTEC PostgreSQL企业版：完全加密和高性能](https://dbweekly.com/link/101005/web)
使用诸如用户友好的监视和24/7支持等高级功能，检查高度安全的PostgreSQL发行版。

`CYBERTEC sponsor`


## [rqlite 5.8：建立在SQLite上的分布式关系数据库](https://dbweekly.com/link/101006/web)
我有时想知道Postgres和SQLite是否在秘密竞争中建立了许多其他数据库：-) 5.8.0这个受欢迎的分布式数据库增加了对 TLS连接。

`rqlite`


## [Database Lab Engine 2.1：适用于开发环境的大型Postgres数据库的即时克隆](https://dbweekly.com/link/101008/web)
在几秒钟内为独立的非生产环境提供数TB的Postgres数据库，而无需支付额外费用。

`Postgres.ai`

## 💼 招聘

## [X-Team（远程）的DevOps工程师](https://dbweekly.com/link/101009/web)
加入最有活力的开发人员社区，并参与Riot Games，FOX，Sony，Coinbase等项目。

`X-Team`
