---
layout: post
title: 数据库每周新闻 2021-4-9
---
### 数据库每周新闻#349 - 2021年4月9日
![_config.yml]({{ site.baseurl }}/images/DBWeekly.png)
备注：[英文原文地址](https://dbweekly.com/issues/349)
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/c4pk5raiq39z113gdgmz.jpg)


## [HStreamDB：一种用于IoT的实时流数据库](https://dbweekly.com/link/106096/web)
一种新开放源代码的数据库，旨在通过标准SQL（加上一些流扩展）来处理大规模实时数据流。这里有一个详尽的介绍。它内置在Haskell中。

`EMQ Technologies Co`


## [TiDB 5.0：分布式HTAP数据库](https://dbweekly.com/link/106098/web)
TiDB是用Go编写的数据库，与MySQL的有线协议兼容，该协议可提供水平可伸缩性，并针对HTAP（混合事务和分析处理）工作负载。5.0添加了实验性的列表分区功能，不可见的索引，并改进了错误消息和日志中个人数据的“脱敏性”。

`PingCAP`


## [无操作，可扩展和灵活的Postgres替代方案](https://dbweekly.com/link/106100/web)
Fauna将Postgres的操作完整性和关系建模与界面和体系结构相结合，该界面和体系结构更适合现代云中的应用程序开发。没有操作瓶颈的Postgres的优点-了解有关Fauna的更多信息。

`Fauna sponsor`


## [与Andy Pavlo一起分析数据库](https://dbweekly.com/link/106102/web)
Andy是“Databaseology”在CMU的副教授，当然知道他的东西！在这次采访中，他解释了他对未来数据库前进的方向，他正在从事的工作以及自动驾驶数据库系统的看法。

`Josh Mintz (IBM)`


## [Redis Labs在G轮融资中筹集了1.1亿美元](https://dbweekly.com/link/106104/web)
Redis背后的主要公司目前在此轮融资中的账面价值超过20亿美元。随着客户和部署的继续发展，他们声称拥有财富500强中31％的份额。他们的RedisConf活动将在两周后举行，并有一次黑客马拉松。

`Datanami`


## [GitHub如何使用复制的Redis驱动的速率限制器扩展其API](https://dbweekly.com/link/106109/web)
GitHub的基于Memcached的旧速率限制器很简单，但遇到了问题。这是Redis加上一些Lua脚本的救援方法。

`Robert Mosolgo (GitHub)`


## [您需要知道的三个DynamoDB限制](https://dbweekly.com/link/106110/web)
这些限制是单个文档的大小，查询和扫描操作的页面大小限制以及分区吞吐量限制。大规模使用DynamoDB时必不可少的知识。

`Alex DeBrie`


## [如何使用Amazon S3对象Lambda匿名化数据](https://dbweekly.com/link/106111/web)
我们最近宣布发布S3 Object Lambda，这是一种通过S3对象检索的方式放置无服务器Lambda函数的方法，一种用例是使数据匿名（或至少使用假名）。在飞行中。

`Jérôme Van Der Linden`


## [Postgres日志中需要监视的最重要事件](https://dbweekly.com/link/106112/web)
在这本电子书中，我们将查看排名前6位的Postgres日志事件，以监视查询性能并防止停机。

`pganlayze sponsor`


## [构建用于市场数据的实时无服务器数据管道](https://dbweekly.com/link/106113/web)
这是面向Google Cloud的，因此显示的技术包括Pub / Sub，BigQuery和Dataflow。

`Rachel Levy & Bhupinder Sindhwani (Google Cloud Blog)`


## [是适用于PostgreSQL的Amazon RDS还是适用于我的Amazon Aurora PostgreSQL？](https://dbweekly.com/link/106114/web)
我认为Aurora或直接RDS何时适合情况存在很多困惑。在这里，亚马逊试图澄清事情。

`Vivek Singh & Sagar Pate (AWS)`


## [工作日-PostgreSQL数据库工程师/管理员](https://dbweekly.com/link/106116/web)
我们正在寻找一名工程师来帮助我们为将来构建，改进持久性体系结构并确保我们的系统24/7完美运行。我们是在欧洲快速发展的全球最大的SaaS公司之一。

`Workday`


## [查找具有雇用条件的数据工程工作](https://dbweekly.com/link/106117/web)
花5分钟时间建立免费的个人资料，并开始为您的下一份工作进行面试。聘请的公司现在正在积极招聘。

`Hired`


## [fselect：查找具有类似SQL的查询的文件](https://dbweekly.com/link/106118/web)
您是否对SQL如此热爱，以至于想使用其代码风格在系统上查找文件？您的愿望已兑现！它超出了您的想象。

`J H S Petersson`


## [谷歌数据库迁移服务](https://dbweekly.com/link/106119/web)
Google Cloud的数据库迁移服务（DMS）是一项服务，用于支持从本地迁移到Google的Cloud SQL服务的MySQL和Postgres迁移。

`Shachar Guz (Google Cloud Blog)`


## [TiKV 5.0：分布式事务性键值数据库](https://dbweekly.com/link/106120/web)
最初是为补充TiDB而创建的（如上所述）TiKV受到Google的一些分布式数据系统（如Spanner）的启发，不仅提供常规的键/值存储功能，而且还提供带有ACID的事务性API。遵守。

`TiKV Project`


## [SQLean：所有“缺失的” SQLite函数](https://dbweekly.com/link/106121/web)
大胆地暗示SQLite是“缺失的”东西，但是这个有趣的项目增加了许多新的细节，包括字符串，数学和统计函数。

`Anton Zhiyanov`


## [Dflat：用于移动设备的结构化数据存储](https://dbweekly.com/link/106122/web)
SQLite + FlatBuffers = 幸福吗？

`Liu Liu`
