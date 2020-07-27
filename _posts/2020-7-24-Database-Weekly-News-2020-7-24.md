---
layout: post
title: 数据库每周新闻 2020-7-24
---
### 数据库每周新闻#314 - 2020年7月24日
![_config.yml]({{ site.baseurl }}/images/DBWeekly.png)
备注：[英文原文地址](https://dbweekly.com/issues/314)
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/v1595590765/f1oc3q8nobgzocas8qju.jpg)


## [在MacBook上使用OmniSciDB分析11亿次出租车出行](https://dbweekly.com/link/92396/web)
这是用不同的数据库系统分析大量数据的一系列实验中的最新一次。这一次轮到OmniSciDB（以前叫MapD）了，它是一个基于SQL的列式数据库引擎，专注于通过并行化实现性能。

`Mark Litwintschik`


## [Spanner的SQL故事](https://dbweekly.com/link/92399/web)
Spanner是Google构建的分布式“NewSQL”数据库，考虑到了全局分布（例如事务和复制）。不过，对于其实际的SQL支持有一些困惑，Jaana在这里澄清了Spanner的SQL故事。

`Jaana Dogan (Google)`


## [免费下载：Kubernetes最佳实践（O'Reilly）](https://dbweekly.com/link/92400/web)
在这本新手册中，四位专业人士（包括Kubernetes的联合创始人Brendan Burns）将指导您在Kubernetes上构建应用程序的最佳实践。

`Cockroach Labs sponsor`


## [介绍Apache Cassandra 4.0测试版](https://dbweekly.com/link/92401/web)
Cassandra是一个宽列NoSQL数据库，它启发了许多其他系统，包括scyllab，它又以“最稳定”的版本而自豪：4.0。它仍处于测试阶段，但显然在压力测试、监控和可观察性方面投入了大量精力。

`Apache Cassandra Team`


## [ravendb5.0发布：ACID NoSQL文档数据库](https://dbweekly.com/link/92407/web)
RavenDB是一个完全事务性的NoSQL数据库，可扩展到每秒100万次读取和150000次写入。目前还没有发布博客文章，但我们听说5.0刚刚正式面世，是在经历了一些最后一刻的压力测试混乱之后才正式发布的，而这些问题现在都得到了解决,5.0版本的很大一部分是时间序列数据支持。

`RavenDB`


## [解开数据库系统的神秘感：隔离级别与一致性级别](https://dbweekly.com/link/92410/web)
有时候，隔离和一致性的概念可能会混淆，特别是当供应商试图将其中一个或另一个的好处推向市场时。

`Daniel J. Abadi`


## [离开Oracle去PostgreSQL？你并不孤单](https://dbweekly.com/link/92411/web)
我们将帮助您的开发人员迁移到PostgreSQL，确保应用程序代码转换为与Oracle兼容的函数。

`EDB sponsor`


## [Shopify如何解决其数据发现难题](https://dbweekly.com/link/92412/web)
作为最大的电子商务服务提供商之一，Shopify有很多有商业价值的数据需要处理，这篇文章向我们介绍了Artifact，一个他们为数据可访问性和治理目的而构建的工具。它是专有的（目前），但可能会给你一些想法。

`Shopify Engineering`


## [为什么ListenBrainz从InfluxDB迁移到TimescaleDB](https://dbweekly.com/link/92413/web)
简言之，他们对博士后更为熟悉，不想在头脑中保留一套单独的心理模型来应对涌入。

`MusicBrainz`


## [超越关系数据库：关注Redis、MongoDB和ClickHouse](https://dbweekly.com/link/92414/web)
一份相当高级别的白皮书，你必须输入你的姓名和电子邮件才能下载，但是。。这个登陆页面也值得检查一下数据库系统的整洁的公共交通风格地图😁

`Percona`


## [FastOnSQL：跨平台Redis、Memcached、SSDB、LevelDB、RocksDB、UnQLite、LMDB等客户端](https://dbweekly.com/link/92415/web)
如果您使用的是众多非SQL数据库中的一个，这个跨平台、本地（使用Qt和C++）构建的客户端可能对您有兴趣。

`FastoGT`
## 快速浏览


- Nebula Graph，一个分布式图形数据库系统和公司，已经达到了1.0，并获得了800万美元的资金。我们希望不久能从这些人身上看到更多。


- 新的内存和计算优化的硬件选项现在在azuresql数据库上正式上市。128个vCore和4TB的数据库内存听起来如何？（我想很贵吧。）


- 一个名为“喵喵”的持续攻击正在清除所有不安全的数据，但没有明显的原因。祈祷他们在帮我们的忙。
