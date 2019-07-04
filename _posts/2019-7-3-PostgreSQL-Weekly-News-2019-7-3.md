---
layout: post
title: PostgreSQL 每周新闻 2019-7-3
---

### PostgreSQL每周新闻#312 - 2019年7月3日

![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)

备注：[英文原文地址](https://postgresweekly.com/issues/312)



![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/ocstzavnuapr5ctzzwwd.jpg)

## [通过EXPLAIN变成更好的开发者](https://postgresweekly.com/link/66142/web)

一场有趣的长达40分钟的讨论，深入探讨查询解析和规划的世界，以及如何使用EXPLAIN命令创建查询计划，以分析查询和数据库设计的效率。

`LOUISE GRANDJONC`

## [深入了解PostgreSQL预设及其对安全性的影响](https://info.crunchydata.com/blog/postgresql-defaults-and-impact-on-security-part-1)

对Postgres默认安全设置的两步探索（[点此看第2部分](https://info.crunchydata.com/blog/postgresql-defaults-and-impact-on-security-part-2)）以及[crunchy_check_access](https://github.com/CrunchyData/crunchy_check_access)扩展如何帮助您更加深入的挖掘。

`JOE CONWAY`

## [使用Telegraf和InfluxDB监控PostgreSQL数据库](https://www.influxdata.com/blog/monitoring-your-postgresql-database-with-telegraf-and-influxdb/?utm_campaign=postgres&utm_medium=newsletter&utm_source=cooperpress)

本教程将专门介绍设置Telegraf和InfluxDB以监控PostgreSQL的过程。

`INFLUXDATA` **赞助商**                                                                       

## [另一个关于GIN索引的介绍](http://www.louisemeta.com/blog/indexes-gin/)

最近我们已经看了很多关于Postgres索引的精彩文章，Louise Grandjonc在这里有一篇专注于GIN（广义倒排索引）索引以及[如何使用它们](http://www.louisemeta.com/blog/indexes-gin-algorithms/)的文章。

`LOUISE GRANDJONC`

## [Postgres的缓慢攀升和持久化的价值](https://thenewstack.io/the-slow-climb-of-postgres-and-the-value-of-persistence/)

最近PostgresVision会议的与会者从数据库先驱Michael Stonebraker博士那里听到了消息。他讲述了他如何帮助Postgres走向全世界 —— 一段15年升腾跌宕的旅程。

`JOAB JACKSON(THE NEW STACK)`

## [设置max_connections的挑战以及为何要使用连接池](http://richyen.com/postgres/2019/06/25/pools_arent_just_for_cars.html)

是什么让max_connections成为了一个棘手的Postgres设定，以及如何使用一些基准测试来为您自己的设置找到合理的数值。

`RICHARD YEN`

## [Postgres 11的CIS基准测试如何工作](https://info.crunchydata.com/blog/cis-11-benchmark)

CIS PostgreSQL基准测试是由互联网安全中心发布的关于如何测试Postgres的一套指南和最佳实践。下面介绍如何使用它来改进您自己的Postgres设置，并将其作为自动化安全验证过程的一部分。

`DOUGLAS HUNLEY`

## [Postgres Ibiza：另一种不同类型的会议](https://momjian.us/main/blogs/pgblog/2019.html#June_28_2019)

Postgres会议在会议地点上进行了大胆的尝试，上个月在西班牙著名的派对岛举行了Postgres会议。。

`BRUCE MOMJIAN`

## [如果您的管理员用户无法登录，如何重新获得对Postgres的访问权限](https://fluca1978.github.io/2019/06/27/PostgreSQLSingleMode.html)

您可以依靠Postgres的单用户模式重新获得访问权限。

`LUCAFERRARI`

## [PostgreSQL日志记录最佳实践](https://www.strongdm.com/postgresql-logging-best-practices/?utm_source=PG%20Weekly&utm_medium=email&utm_campaign=2019-07-03%20-%20%5BSchD%5D%20-%20%5BSDM%5D)

以下是一些让每个人都能在同一页面上的最佳实践。

`STRONGDM` **赞助商**

## [如何在Azure DB上为PostgreSQL设置PgBouncer作为连接池代理](https://techcommunity.microsoft.com/t5/Azure-Database-for-PostgreSQL/Steps-to-install-and-setup-PgBouncer-connection-pooling-proxy/ba-p/730555)

`PARIKSHIT SAVJANI`.

## [在Windows下使用MSYS2和MinGW构建Postgres和OpenSSL](https://www.cybertec-postgresql.com/en/bulding-postgresql-x86-x64-and-openssl-using-msys2-and-mingw-under-windows/)

可以通过在Windows上使用MSYS2（Cygwin派生的POSIX兼容层）为自己编译Postgres。

`PAVLO GOLUB`

## [PgBouncer 1.10.0发布](https://pgbouncer.github.io/2019/07/pgbouncer-1-10-0) 

PgBouncer是一个轻量级连接池，除去[其他事情](https://pgbouncer.github.io/changelog.html#pgbouncer-110x)，最新版本改进了TLS 1.3的支持。

`PETER EISENTRAUT`

## [db-to-sqlite 1.0：一个用于将表或查询从任何SQL数据库导出到SQLite的CLI工具](https://github.com/simonw/db-to-sqlite)

`SIMON WILLISON`



# 💡 本周提示

由GitPrime支持提供

### 持久性换取性能提升

​	Postgres中的持久性是确保您执行的任何数据相关操作成功提交到磁盘，因此如果Postgres服务器运行时突然重启或断电，稍后它就可以返回到正确的状态。
​	持久性的需求可能因您的使用案例或您想要执行的操作而异。例如，在将大型数据加载到新数据库时，您可能会使用持久性换取性能提升，而如果您实时运行的数据库中，则持久性比性能更重要！

如果您乐意为性能交换耐用性，这里有几个设置可以调整（在SHOW config_file显示的文件中）以实现它：

​	• 关闭[fsync设置](https://www.postgresql.org/docs/9.3/runtime-config-wal.html#GUC-FSYNC)以阻止Postgres确保所有更新都物理写入磁盘。虽然最终都会成功，但这会让Postgres无法确信数据刷盘成功。

​	• 禁用[FULL PAGE WRITE](https://www.postgresql.org/docs/9.3/runtime-config-wal.html#GUC-FULL-PAGE-WRITES)。这在某种程度上与fsync密切相关。

​	• 将[synchronous_commit设置为'off'](https://www.postgresql.org/docs/9.3/runtime-config-wal.html#GUC-SYNCHRONOUS-COMMIT)以使事务在WAL记录写入磁盘之前被认定为成功。

​	• 增加[checkpoint_segments和checkpoint_timeout](https://www.postgresql.org/docs/9.3/runtime-config-wal.html#GUC-CHECKPOINT-SEGMENTS)的选项，以减少WAL条目向磁盘提交的频率

想要以后回看这些技巧？您需要Postgres的[非持久性设置文档](https://www.postgresql.org/docs/9.3/non-durability.html)。

本周的tips由[GitPrime](https://resources.gitprime.com/books/20-patterns/?utm_source=nl(pgw)&utm_medium=email-nl&utm_campaign=nl(pgw))赞助。获取他们的新领域指南[《工程团队中需要注意的20个模式》](https://resources.gitprime.com/books/20-patterns/?utm_source=nl(pgw)&utm_medium=email-nl&utm_campaign=nl(pgw))的副本，其中充满了可操作的见解，以帮助用数据调试您的开发过程。

🗓  **即将举办的Postgres活动**  

​	• [PGConf.Brasil 2019](https://www.pgconf.com.br/2019/en/) (8月1日 - 3日，巴西圣保罗) —— 为期三天的会议，包括会谈、教程、课程和闪电会谈。

​	• [PGDay Austria 2019](https://pgday.at/en/)（9月6日，奥地利维也纳新城）

​	• [PostgreSQL Conference Asia 2019](http://2019.pgconf.asia/)（9月9日 - 12日，印度尼西亚巴厘岛）

​	• [PostgresConf South Africa 2019](https://postgresconf.org/conferences/SouthAfrica2019)（10月8 - 9日，约翰内斯堡）——对于使用Postgres的数据库管理和开发社区的人员之间相互了解来说是一个机会。

