---
layout: post
title: PostgreSQL 每周新闻 2019-7-17
---

### PostgreSQL每周新闻#314 - 2019年7月17日

![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)

备注：[英文原文地址](https://postgresweekly.com/issues/314)

![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/sames4exo9xx1ti9ob9t.jpg)

## [如何将您的Postgres密码提升到SCRAM标准](https://info.crunchydata.com/blog/how-to-upgrade-postgresql-passwords-to-scram)

支持[SCRAM](https://en.wikipedia.org/wiki/Salted_Challenge_Response_Authentication_Mechanism)身份验证是在Postgres 10中引入的，它提供了比MD5更大的好处。下面是如何以及为什么这样做，和如何将现有登录账号升级到使用SCRAM方法。

`JONATHAN S. KATZ`

## [用Postgres索引清理鳄鱼的牙齿](https://www.youtube.com/watch?v=2l-nCkPQVuQ)

Citus Data(现在是微软的一部分)的一名工程师在Postgres Open(2018)上发表了一场40分钟的演讲，从一只鳄鱼出发，讲述了一个关于Postgres中所有索引类型的故事。这比听上去的更具有有教育意义，您将从中学到很多，如果您正好需要了解Postgres索引，这40分钟将是一个很好的机会。

`LOUISE GRANDJONC`

## [了解Postgres真空调优如何提高DB性能](https://resources.2ndquadrant.com/webinar-postgres-vacuuming-through-pictures)

加入免费的PostgreSQL网络研讨会: Postgres通过图片进行真空调优，了解PostgreSQL中的真空和自动真空的关键概念、真空操作、如何调优用于Postgres部署的真空，等等。

![img](https://copm.s3.amazonaws.com/547e0ba0.png)

`2NDQUADRANT POSTGRESQL WEBINARS`**赞助商**

## [使用ICU排序来避免glibc 2.28数据损坏](https://www.cybertec-postgresql.com/en/icu-collations-against-glibc-2-28-data-corruption/)

这是一个技术问题! 最新版本的GNU C库(2.28)[对Unicode排序规则(排序规则是控制字符串比较或排序的规则)进行了很大的更改](https://postgresql.verite.pro/blog/2018/08/27/glibc-upgrade.html)，这可能会导致索引出现问题，包括损坏。Postgres在默认情况下使用os级排序，但也可以使用ICU排序，它本质上是一组独立的、第三方的、跨平台的排序，本文将深入探讨为什么要进行这种转换，以及如何进行这种转换。

`LAURENZ ALBE`

## [PostgreSQL Conference Europe 2019现在开放注册](https://2019.pgconf.eu/)

今年10月在意大利米兰。演讲人要到八月才会选出(CFP现在已经关闭了)，但是现在可以买到票了。

`PGCONF.EU`

## [看看Postgres 12中的分区增强功能](https://www.2ndquadrant.com/en/blog/partitioning-enhancements-in-postgresql-12/)

Postgres 12在分区选择、引用完整性改进和内省方面得到了一些“非常显著”的改进。

`KIRK ROYBAL`

## [在Postgres中实现“自治事务”](https://www.cybertec-postgresql.com/en/implementing-autonomous-transactions-in-postgres/)

在Oracle世界中更常见，自治事务是由其他事务发起的独立事务(也就是说，它们具有不同的上下文，不会干扰“调用”事务)。Postgres对此没有原生支持，但有两种解决方案。

`KAAREL MOPPEL`

## [反向代理到pgAdmin](https://pgsnake.blogspot.com/2019/07/reverse-proxying-to-pgadmin.html)

[pgAdmin](https://www.pgadmin.org/)是一种流行的基于web的Postgres管理和数据库管理工具。

`DAVE PAGE`

## [为全文搜索建立文档索引](https://pgsnake.blogspot.com/2019/06/indexing-documents-for-full-text-search.html)

`DAVE PAGE`

## [CREATE STATISTICS:它是用来做什么的?](https://www.slideshare.net/fuzzycz/create-statistics-what-is-it-for-postgreslondon)

最近的一次演讲中这些代码丰富的幻灯片突出了[CREATE STATISTICS](https://www.postgresql.org/docs/10/sql-createstatistics.html)的用例，这是Postgres 10中引入的一个命令，可以创建扩展的统计对象[来帮助查询规划](https://www.citusdata.com/blog/2018/03/06/postgres-planner-and-its-usage-of-statistics/)。

`TOMAS VONDRA SLIDEDECK`

## [SQL、Python和R.都在一个平台上，并且永远免费](https://mode.com/?utm_campaign=studio&utm_content=studio_20190717&utm_medium=sponsored_email&utm_source=postgresweekly)

此模式结合了一个SQL编辑器、原生Python和R笔记本，还有viz builder在同一个平台上。连接、分析并且分享。

`MODE`**赞助商**

## [如何在GraphQL中使用MongoDB和PostgreSQL](https://www.youtube.com/watch?v=_trOqBZMJHQ)

演示如何使用GraphQL查询语言、Apollo Server和Node.js将各种数据库组合在一起(这里对MongoDB和Postgres的选择相当随意)。

`BEN AWAD`

## [从Postgres谈图形数据库的远景](https://www.youtube.com/watch?v=JQ0ycS8HqjE)

几周前，在Postgres Vision 2019上发表了一篇关于AgensGraph的演讲，AgensGraph是建立在Postgres之上的一个多模型图数据库。音频质量不佳，但是您可以很好地了解什么是AgensGraph以及它是如何提供帮助的。

`AGENSGRAPH`

# 💡本周提示

由percona提供支持![Percona](https://res.cloudinary.com/cpress/image/upload/v1559053486/vmjp4kyjuomp5klwidlw.png)

### 测试您的应用程序如何处理Postgres的失败或高延迟

如果您运行自己的Postgres服务器，它就像石头一样坚固，对吧? 如果您运行在云基础设施上，您永远不知道它是如何工作的，因此以一种能够应对Postgres失败的弹性方式构建系统是值得的。

您可以在各种故障场景下测试您的应用程序，方法包括提供不正确的数据库身份验证细节、关闭数据库服务器，甚至设置防火墙规则，但是间歇性故障怎么办? 你需要一些不那么严重的东西。

[Toxiproxy](https://github.com/Shopify/toxiproxy)是一个开源系统，它可以模拟不同的网络环境，因此您可以看到您的应用程序在后台服务(如Postgres数据库)处于间歇性或遭受高延迟的情况下如何执行。它既是一个Go支持的TCP代理(因此您可以将它用于Postgres之外的其他服务)，也是用于Go、Ruby、Python、. net、PHP和Node的客户机库。因此，您可以将它直接集成到您的测试套件中。

本周的小贴士由[Percona](https://learn.percona.com/postgresql-high-availability-registration-cooperpress)赞助。本[白皮书](https://learn.percona.com/postgresql-high-availability-registration-cooperpress)讨论了高可用性数据库体系结构的重要性，以及[如何为高可用性配置PostgreSQL。](https://learn.percona.com/postgresql-high-availability-registration-cooperpress)

🗓  **即将举办的Postgres活动**  

• [GConf.Brasil 2019](https://www.pgconf.com.br/2019/en/)(8月1日至3日，巴西圣保罗)——为期三天的会议，包括讲座、辅导课、课程和闪电讲座。

• [PGDay Austria 2019](https://pgday.at/en/)(9月6日，奥地利维也纳诺伊施塔特)

• [PostgreSQL Conference Asia 2019](https://2019.pgconf.asia/) (9月9日至12日，印度尼西亚巴厘岛)

• [PostgresConf South Africa 2019](https://postgresconf.org/conferences/SouthAfrica2019)(10月8日至9日在约翰内斯堡)——提供给使用Postgres的数据库管理和开发人员互相了解的机会。

