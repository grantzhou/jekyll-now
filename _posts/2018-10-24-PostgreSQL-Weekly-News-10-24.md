---
layout: post
title: PostgreSQL 每周新闻 2018-10-24
---

### PostgreSQL每周新闻 #279 - 2018年10月24日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)
![_config.yml](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/selwciixerbd5unntgxb.jpg)

备注：[英文原文地址](https://postgresweekly.com/issues/279)


## [PostgreSQL 11发布](https://www.postgresql.org/about/news/1894/)

期待已久的主要版本包括散列分区，覆盖索引，存储过程中的事务等等，[以及更多](https://pgdash.io/blog/postgres-11-whats-new.html)

`POSTGRESQL全球开发组`

## [Postgres 11中的新功能：监控JIT性能，自动预热和存储过程](https://pganalyze.com/blog/postgres11-jit-compilation-auto-prewarm-sql-stored-procedures)
![性能](https://pganalyze.com/static/jit_performance-777a3f748901304870e81805c2b0cdef-fed13.png)
Postgres 11具有一些重大改进，特别是JIT编译可以带来一些很好的性能改进。 快速了解它对性能的意义。

`LUKA FITTL`

## [Postgres中的SQL函数，来自Citus数据的Devs](https://www.citusdata.com/blog/2018/06/21/fun-with-sql-functions/?utm_source=PG_Weekly&utm_medium=email&utm_campaign=sponsor_blog)
![CitusData](https://copm.s3.amazonaws.com/c9e3d9ee.png)
只要你能想的到，Postgres中就会有一个SQL函数。
请收藏数百个内置SQL函数的示例，包括array_agg，array_to_string，now，allballs，data_trunc和JSONB运算符等。

`CITUS DATA` **赞助商**

## [PostgreSQL 11：新版本的首次使用](https://www.percona.com/blog/2018/10/18/postgresql-11-our-first-take-on-the-new-release/)
对最新版本的一些“杀手级功能”的思考。

`JOBIN AUGUSTINE，IBRAR AHMED，AVINASH VALLARAPU和FERNANDO LAUDARES CAMARGOS`

## [看看Postgres 11中的并行性](https://speakerdeck.com/macdice/parallelism-in-postgresql-11)
Postgres在几个版本之前得到了对并行性的初步支持。 这并不意味着一切都是并行化的（至少目前为止）。
几周前，硅谷PostgresOpen的这篇演讲深入探讨了Postgres的并行性问题。

`THOMAS MUNRO`

## [在Postgres 11中添加具有默认值的新列](https://blog.2ndquadrant.com/add-new-table-column-default-value-postgresql-11/)
在Postgres 11中，向表添加具有默认值的新列时，速度要快得多，因为该默认值不再写入每个现有行。

`ANDREW DUNSTAN`

## [使用Postgres 11对数据进行分片](https://pgdash.io/blog/postgres-11-sharding.html)
Postgres 10添加了声明性表分区，但在Postgres 11中，您现在可以将其与外部数据包装器结合使用，从而提供了一种在多个服务器上本地分片表的机制。

`RAPIDLOOP`

## [如何使用时间点恢复最大限度地减少Postgres数据库的RPO（恢复点目标）](https://severalnines.com/blog/how-minimize-rpo-your-postgresql-databases-using-point-time-recovery)
![PRO](https://severalnines.com/sites/default/files/blog/node_5405/image11.jpg)
“RPO”（恢复点目标）是灾难恢复计划中的一个值，它定义了您可以“承受”丢失的数据量，并帮助确定备份系统的设计。
 
`SEVERALNINES`

## [注释您的Postgres数据库](https://www.citusdata.com/blog/2018/10/17/commenting-your-postgresql-database/)
注释有助于提高您的应用程序代码可读性，但在记录您的查询和模式时，它们也可以是一个强大的工具。

`CRAIG KERSTIENS`

## [Postgres 11的分区改进专题](https://blog.2ndquadrant.com/partitioning-improvements-pg11/)

`ALVARO HERRERA`

## [使用Telegraf和InfluxDB监控PostgreSQL数据库](https://www.influxdata.com/blog/monitoring-your-postgresql-database-with-telegraf-and-influxdb/)
![IMG](https://www.influxdata.com/wp-content/uploads/influxdb-iwi.png)
`INFLUXDATA` **赞助商**

## [使用开源工具构建企业级Postgres设置](https://www.percona.com/blog/2018/10/19/postgresql-building-enterprise-grade-setup-with-open-source/)
您可以在此处观看Percona最近的网络研讨会重播，或[阅读本文以了解出现的关键问题和答案](https://www.percona.com/resources/webinars/enterprise-grade-postgresql-built-open-source-tools)。

`JOBIN AUGUSTINE`

## [Pgpool-II 4.0发布](http://pgsqlpgpool.blogspot.com/2018/10/pgpool-ii-40-released-scram.html)
Pgpool是一种流行的连接池中间件，它现在也支持SCRAM身份验证。

`TATSUO ISHII`

# 活动
## [PostgreSQL并非是您的传统SQL数据库 - 10月30日（网络研讨会](https://register.gotowebinar.com/register/3930869911246887681?source=lp)
）GülçinYıldırımJelínek将介绍PostgreSQL中的设计选择，PostgreSQL中的全文搜索等。

## [PGDay.Seoul 2018](http://pgday.postgresql.kr/)
2018年11月3日（韩国首尔）PostgreSQL韩国用户组准备了第三个活动(半天)。
所有演讲均采用韩语。

## [Pg Down 2018](https://2018.pgdu.org/)
12月7日（澳大利亚墨尔本）PG Down 2018年是第二届年会，为PostgreSQL开发者和用户提供了一个聚会、学习和加强联系的绝佳机会。

## [PGConf.ASIA 2018年12月10日至12日（日本东京）](https://www.pgconf.asia/EN/2018/)
亚洲最大的PostgreSQL活动。
