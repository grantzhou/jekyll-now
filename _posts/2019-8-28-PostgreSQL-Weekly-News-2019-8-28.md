---
layout: post
title: PostgreSQL 每周新闻 2019-8-28
---

### PostgreSQL每周新闻#320 - 2019年8月28日

![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)

备注：[英文原文地址](https://postgresweekly.com/issues/320)

![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/v1566985036/yo4lnibdiishpaptekox.png)

## [Postgres的艺术第二版](https://theartofpostgresql.com)

一位Postgres社区的核心成员，收集了一些吸引人的东西，包括新版本的书籍，采访，代码，深入挖掘Postgres的例子（但是，这需要购买。）

`DIMITRI FONTAINE`

## [行安全，Postgres魔力视角](https://www.cybertec-postgresql.com/en/postgresql-row-level-security-views-and-a-lot-of-magic/)

行安全是Postgres的一个重要功能，它可以创建更细粒度的策略划分用户能查询或者更新的数据行。让我们一起来看一下这是如何实践的。

`HANS-JÜRGEN SCHÖNIG`

## [电子书:Postgres日志中管理数据库的的重要信息](https://pganalyze.com/ebooks/monitoring-postgres-logs?utm_source=PostgresWeeklyPrimary)

在这本pganalyze电子书中，我们将查看前6个Postgres日志事件，以监控查询性能并防止停机。

`PGANALYZE`**赞助商**

## [Timescale是如何在Postgres的基础上建立分布式数据库的](https://blog.timescale.com/blog/building-a-distributed-time-series-database-on-postgresql/)

TimescaleDB是一个流行的扩展，它为Postgres带来了时间序列数据库功能。在这里，Timescale共享他们的设计、计划和新的（仍然是封闭测试版）分布式版本TimescaleDB的基准。。

`MIKE FREEDMAN AND ERIK NORDSTRÖM (TIMESCALE)`



## [使用Patroni管理高可用Postgres数据库](https://scalegrid.io/blog/managing-high-availability-in-postgresql-part-3/)

在技术的角度比较Patroni与repmgr和PAF在管理高可用Postgres集群的区别

`MADAN KUMAR`



## [快速收集你的Postgres数据库的图表](https://github.com/nsingla/dbdiagrams)

dbdiagram.io是一个使用简单的DSL语言绘制数据库关系图的在线工具。这个简短的脚本将您基于Postgres的数据库转换为该语言。

`HOLISTICS SOFTWARE`



## [开发者需要知道的Postgres的6个关键点](https://info.enterprisedb.com/Tech-Guide-6-Things-a-Developer-Should-Know-About-Postgres-paper.html?utm_source=Cooperpress&utm_medium=ad)

下载我们的白皮书，了解为什么PostgreSQL在开发人员中的受欢迎程度急剧上升

`ENTERPRISEDB`



## [PgBouncer 1.11.0发布](http://www.pateldenish.com/2019/08/clone-schema-in-postgres.html)

最新版本的流行连接池中的主要新功能是支持SCRAM 身份验证。改进了Postgres 12的支持。

`PETER EISENTRAUT`



## [PL/Prpxy在Postgres11和FreeBSD12中运行](https://fluca1978.github.io/2019/08/26/PLProxy_FreeBSD.html)

但如果你需要这样做，这是不容易的，这个新的项目拉请求将有帮助。卢卡还建议了一种让它与Postgres12一起工作的方法，但建议在生产中不要使用它。

`LUCA FERRARI`



# 💡本周提示

###### SELECT DISTINCT

由DATADOG提供



今天的提示很简单，但我知道很多Postgres用户并不熟悉。在接下来的几周里，我们将从这个简单的提示构建成更有趣和更复杂的不同示例。

在最基本的级别上，distinct是一个关键字，可以用于select查询，以从最终结果中消除重复的行。例如：

```sql
SELECT DISTINCT city FROM employees;
```

这是一个比下面的语句更好的例子

```sql
SELECT city FROM employees GROUP BY city;
```

本周提示由[DataDog](https://www.datadoghq.com/postgres-monitoring/?utm_source=Advertisement&utm_medium=CooperPress&utm_campaign=CooperPress-PostgresWeeklyTip)赞助。





🗓  **即将举办的Postgres活动**  

• [PGDay Austria 2019](https://pgday.at/en/)（9月6日， 维纳·纽斯塔特，奥地利）

• [PostgreSQL Conference Asia 2019](https://2019.pgconf.asia/)（9月8-11日，巴厘岛，印度尼西亚）

• [PostgresOpen 2019](https://postgresweekly.com/link/68304/web) (9月11-13日， 佛罗里达)——两天包含有关PostgreSQL和相关技术的教程和演示文稿。

• [PostgresConf Silicon Valley 2019](https://postgresweekly.com/link/68305/web)（9月18-20日，圣荷西）——时间表（包括培训）现已公布

• [PostgresConf South Africa 2019](https://postgresweekly.com/link/68306/web)（10月8-9日， 约翰内斯堡）——提供给使用Postgres的数据库管理和开发人员互相了解的机会。

• [PostgreSQL Conference Europe 2019](https://postgresweekly.com/link/68391/web)（10月15-18日， 米兰）