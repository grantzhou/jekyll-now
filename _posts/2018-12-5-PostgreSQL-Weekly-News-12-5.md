---
layout: post
title: PostgreSQL 每周新闻 2018-12-05
---


### PostgreSQL每周新闻#284 - 2018年12月05日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)

备注：[英文原文地址](https://postgresweekly.com/issues/284)

##[PostgreSQL11中有什么新功能](https://severalnines.com/blog/whats-new-postgresql-11)
Postgres 11大约在6周前发布，如果你还没有使用过，这篇文章概述了新的特性和功能。

`VIOREL TABARA`

##[PostgreSQL中的事务：READ COMMITTED与REPEATABLE READ](https://www.cybertec-postgresql.com/en/transactions-in-postgresql-read-committed-vs-repeatable-read/)
SQL标准提出了不同的事务隔离级别（例如，READ COMMITTED和REPEATABLE READ）来控制数据库引擎关于读取在并发运行的事务中提交的数据的行为。

`HANS-JÜRGEN SCHÖNIG`

##[宣布EDB Postgres云数据库服务测试版](https://www.enterprisedb.com/edb-postgres-cds)
![EDB COMPANY](https://copm.s3.amazonaws.com/11b09ec3.png)
完整的托管服务，在Amazon Web Services（AWS）云上提供企业级EDB Postgres数据库

`ENTERPRISEDB` *赞助商*

##[在Postgres 11中安装和配置JIT](https://www.percona.com/blog/2018/11/19/installing-and-configuring-jit-in-postgresql-11/)
SQL语句的即时（JIT）编译作为Postgres 11的一个选项发布到Postgres 11，但由于并非所有工作负载都能从中受益，因此默认情况下不会启用它。
以下是如何让它运行以查看它是否对您有帮助。

`JOBIN AUGUSTINE`

##[AgensGraph 2.0：Postgres的多模型图形数据库](https://www.postgresql.org/about/news/1909/)
AgensGraph是Postgres上构建的图形数据库（支持SQL和Cypher查询）。[GitHub repo](https://github.com/bitnine-oss/agensgraph)

`BITNINE`

##[psql在Postgres 12上获得简单的CSV输出功能](https://okbob.blogspot.com/2018/11/postgresql-12-psql-csv-output.html)

`PAVEL STĚHULE`

##[pgBackRest和流复制的结合](https://pgstef.github.io/2018/11/28/combining_pgbackrest_and_streaming_replication.html)
pgBackRest是一个强大的Postgres备份和恢复工具。

`STEFAN FERCOT`

##[Postgres 12功能亮点：DOS预防](https://paquier.xyz/postgresql-2/postgres-12-dos-prevention/)
可以使用某些查询锁定Postgres数据库，并且Postgres 12正在修复。

`MICHAEL PAQUIER`

##[带插槽的PostgreSQL流式物理复制](https://www.percona.com/blog/2018/11/30/postgresql-streaming-physical-replication-with-slots/)
物理Postgres复制基于Write Ahead Log（WAL）和Postgres 9.4中引入的插槽，使主服务器能够跟踪副本的状态并保留它们可能需要的WAL段。

`NICKOLAY IHALAINEN`

##[管理Postgres中的高可用性](https://scalegrid.io/blog/managing-high-availability-in-postgresql-part-1/)
关于如何通过开源工具使用流式复制管理高可用性以实现自动故障转移，监控和复制的三部系列文章的第一部分。

`MADAN KUMAR K`

##[为什么Citus Data向PostgreSQL非营利组织捐赠1％的股权](https://www.citusdata.com/blog/2018/10/24/why-citus-data-is-donating-1-percent-equity/?utm_source=PG_Weekly&utm_medium=email&utm_campaign=sponsor_blog)
Citus Data的联合创始人分享了他们与Postgres社区分享未来的成功的原因。

`CITUS DATA` *赞助商*

##[Postgres和Kubernetes：没有供应商锁定的DBaaS](https://www.youtube.com/watch?v=q26U2rQcqMw&feature=share)
一段关于使用Kubernetes创建自己的Postgres驱动的数据库作为服务的30分钟谈话。

`OLEKSII KLIUKIN`

#活动

##[Pg Down Under 2018](https://2018.pgdu.org/)
12月7日(澳大利亚墨尔本)

PG Down 2018是第二届年会，为PostgreSQL开发者和用户提供了独一无二的机会来见面，学习和了解。

##[PGConf.ASIA 2018](https://www.pgconf.asia/EN/2018/)
12月10日至12月12日(日本东京)

亚洲最大的PostgreSQL活动

##[FOSDEM PGDay 2019](https://2019.fosdempgday.org/)
2019年2月1日(比利时布鲁塞尔)

FOSDEM常规PostgreSQL活动的扩展
