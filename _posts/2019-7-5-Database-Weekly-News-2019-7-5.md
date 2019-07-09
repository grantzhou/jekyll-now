layout: post

title: 数据库每周新闻 2019-7-5

# 数据库每周新闻#261 - 2019年7月5日

![config.yml]({{ site.baseurl }}/images/DBWeekly.png)

备注：[英文原文地址](https://dbweekly.com/issues/261)

![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/v1562325808/g6ul9s0x1bymmu2rujws.jpg)

## [DuckDB: 一种新的可嵌入式SQL OLAP DBMS](https://github.com/cwida/duckdb)

内置于C++中，DUCKDB将自己“标榜”为“用于分析的SQLite”。经过一段时间的开发，第一个官方0.1版本现已发布，同时已与C/C++、Python和 R绑定。[官方主页](https://www.duckdb.org/)。

`CWI DATABASE ARCHITECTURES GROUP`

## [使用SQL可以完成所有的事情？](https://blog.acolyer.org/2019/07/03/one-sql-to-rule-them-all/)

回顾一篇[学术论文](https://arxiv.org/abs/1905.12133)，概述了SQL可以扩展到更强大地支持现代流媒体需求的一些方法。

`THE MORNING PAPER`

## [教程：使用DocumentDB进行复杂的设计](https://www.gremlin.com/community/tutorials/chaos-engineering-with-documentdb/?utm_medium=cpm&utm_source=DBWeekly&utm_content=20190705&utm_campaign=2019_Cooperpress)

本教程介绍如何针对Amazon的新MongoDB兼容数据库DocumentDB运行简单的网络黑洞攻击。![img](https://copm.s3.amazonaws.com/31d1640d.png)

`GREMLIN` **赞助商**

## [PostgreSQL的缓慢攀升和持久性的价值](https://thenewstack.io/the-slow-climb-of-postgres-and-the-value-of-persistence/)

最近PostgresVision会议的与会者从数据库先驱Michael Stonebraker博士那里听到了消息。他讲述了他如何帮助Postgres走向全世界。

`JOAB JACKSON(THE NEW STACK)`

## [db-to-sqlite 1.0：一个用于将表或查询从任何SQL数据库导出到SQLite的CLI工具](https://github.com/simonw/db-to-sqlite)

来自[Datasette](https://github.com/simonw/datasette)的创建者，这是一种将数据转换为基本Web站点和API的流行工具。

`SIMON WILLISON`

## [通过EXPLAIN变成更好的开发者](https://www.youtube.com/watch?v=IwahVdNboc8)

一个有趣的40分钟的讨论，深入探讨了查询解析和规划的世界，以及如何分析使用PostgreSQL的EXPLAIN命令创建的查询计划。

`LOUISE GRANDJONC`

**简介：**

• SQL Server 2019[引入了对UTF-8](https://techcommunity.microsoft.com/t5/SQL-Server/Introducing-UTF-8-support-for-SQL-Server/ba-p/734928)(广泛使用的字符编码方案)的本机支持。

• RavenDB[推出了RavenDB Cloud](https://www.datanami.com/2019/07/02/ravendb-launches-managed-cloud-service/)，这是一个基于托管云的事务性NoSQL数据库版本。

• 中国的初创企业正在寻找“购买中国”的途径，它们[将目光从Oracle和IBM身上移开](https://www.scmp.com/tech/enterprises/article/3015931/chinas-biggest-start-ups-ditch-oracle-and-ibm-home-made-tech-us)，转而投向像	PingCAP这样的供应商

• 开源的github -a平台[GitLab已经放弃了对MySQL的支持](https://about.gitlab.com/2019/06/27/removing-mysql-support/)，并解释了原因。

• 公平地说，Oracle对AWS赢得一份重要的美国军事合同[并不满意](https://www.theregister.co.uk/2019/07/01/oracle_jedi_case_filing/)。

### 💻**招聘**

[寻求:有️❤️和好奇心的开发者](https://www.keyvalues.com/carbon-five) - 停滞不前?看看C5吧:新项目、新技术、新挑战，以及身处旧金山、洛杉矶、纽约的善良而又聪明的同事们。

`CARBON FIVE`

[在Vettery上找一份新的开发工作](https://www.vettery.com/tech?utm_source=newsletter&utm_medium=cooper-dbweekly&utm_term=tech&utm_content=grouped&utm_campaign=ad-88878) - Vettery专注于技术角色，对求职者来说是完全免费的。

`VETTERY`

### 📒 教程和故事

[Redis 6中的客户端缓存](http://antirez.com/news/130) - Redis的创建者解释了Redis的下一个主要版本将如何支持那些相当高级的客户端缓存，并完成服务器导向的缓存失效。

`SALVATORE SANFILIPPO`

[积极地调优Cosmos DB (漫漫长路)](http://blog.tdwright.co.uk/2019/06/29/aggressively-tuning-cosmos-db-the-long-way-round/) - 有多少种调优Cosmos DB的方法?“为了(最终还是相当绝望)让它更好地扩展，我们尝试了9种方法。”

`TOM WRIGHT`

[社区亮点:Timbergrove如何使用InfluxDB来提供一组智能的办公套件](https://www.influxdata.com/blog/community-highlight-how-timbergrove-uses-influxdb-to-offer-a-smart-workplace-kit/?utm_campaign=whytimeseries&utm_medium=newsletter&utm_source=cooperpress)

`INFLUXDATA`**赞助商**

[基于缓存的数据库架构可能过时的五个迹象](https://www.datanami.com/2019/06/28/five-signs-your-cache-based-database-architecture-may-be-obsolete/)

`DATANAMI`

[36个关于Azure Cosmos DB概念的“宇宙级笔记”](https://azurecosmosdb.github.io/CosmicNotes/) - 如果你有任何关于Azure的多模型数据库服务的工作要做的话，这些笔记可能会派上用场。

`AZURE COSMOS DB`

[用Clang/WASI将Redis移植到WebAssembly中](https://medium.com/fluence-network/porting-redis-to-webassembly-with-clang-wasi-af99b264ca8) - 几乎可以肯定，您自己永远不需要这样做，但我发现这是一个有趣的幕后观察。(如果您对这些内容感兴趣，您可能还喜欢这个[编译为WebAssembly demo的SQLite。](http://kripken.github.io/sql.js/examples/GUI/)）

`MIKHAIL VORONOV`

[CDNs应该像数据库一样工作](https://www.macrometa.co/blog/cdns-should-work-like-databases) - 一个新的边缘计算创业公司为它的方法提出了一个有趣的论点。

`MACROMETA`