---
layout: post
title: PostgreSQL 每周新闻 2019-5-8
---

### PostgreSQL每周新闻#304 - 2019年5月8日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)

备注：[英文原文地址](https://postgresweekly.com/issues/304)

![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/attbh6ihgai6ueh9hfsn.jpg)

## [pg_auto_failover：Postgres的自动故障转移和高可用性](https://cloudblogs.microsoft.com/opensource/2019/05/06/introducing-pg_auto_failover-postgresql-open-source-extension-automated-failover-high-availability/)
由被微软收购的Citus Data提供的新的开源扩展程序。 pg_auto_failover旨在提供基于流复制的简单自动故障转移，无需外部依赖。

`LUKAS FITTL (MICROSOFT)`

## [在Azure上为PostgreSQL引入Hyperscale（Citus）](https://www.citusdata.com/blog/2019/05/06/introducing-hyperscale-citus-on-azure-database-for-postgres/)
现在，在Microsoft Azure上Hyperscale（Citus）可以跨多个物理节点扩展数据，并将底层数据进行分割。Hyperscale是微软最近收购Citus Data的关键原因。

`CITUS DATA`

## [如果工程师需要访问数据库，你需要strongDM](https://www.strongdm.com/product/?utm_source=&utm_medium=email&utm_campaign=2019-04-24%20-%20%5BUSA%5D%20-%20%5BSchD%5D%20-%20%5BSDM%5D%20-%20%5BENT%5D%20-%20PGW)
![img](https://copm.s3.amazonaws.com/69ff4959.png)  
strongDM对任何东西都有效。认真的讲，任何数据库，任何服务器，每个环境。[了解更多](https://www.strongdm.com/product/?utm_source=&utm_medium=email&utm_campaign=2019-04-24%20-%20%5BUSA%5D%20-%20%5BSchD%5D%20-%20%5BSDM%5D%20-%20%5BENT%5D%20-%20PGW)

`STRONGDM` **赞助商**

## [PostgreSQL参与Google Docs 2019（以及Summer of Code）](https://www.postgresql.org/about/news/1938/)
 Season of Docs是Google的一个新项目，旨在鼓励文档作者和开源项目共同努力来改进他们的文档。作者可以获得三个月的合作[津贴](https://developers.google.com/season-of-docs/docs/tech-writer-stipends)。Postgres也参加了今年的[Google Summer of Code](https://andreas.scherbaum.la/blog/archives/974-Google-Summer-of-Code-2019-PostgreSQL-participates-with-5-projects.html),如果你或任何你认识的人是学生，欢迎参加。
 
 `POSTGRESQL全球开发小组`
 
 ## [TimescaleDB 1.3发布：基于Postgres的时间序列SQL数据库]()
 如果您还没有使用过[TimescaleDB](https://github.com/timescale/timescaledb)，TimescaleDB是一个Postgres扩展，它会将Postgres变成一个快速的时间序列数据库。TimescaleDB 1.3引入了对连续聚合的支持，它可以在后台计算查询结果并将结果实例化，使其更接近于[PipelineDB](https://www.pipelinedb.com/)，后者专注于此类用例。
 
 `TIMESCALE`
 
 ## [为Postgres做贡献](https://www.citusdata.com/blog/2019/01/15/contributing-to-postgres/?utm_source=PG_Weekly&utm_medium=email&utm_campaign=sponsor_blog)
 如果你想为Postgres做贡献，这里有一些我们编译的有用提示。
 
 `CITUS DATA, A MICROSOFT COMPANY` **赞助商**
 
 ## [在Postgres中实现一对一的关系（用于实际中）](https://www.cybertec-postgresql.com/en/1-to-1-relationship-in-postgresql-for-real/)
 忘了那些关于UNIQUE约束的技巧，下面是如何使用DEFERRABLE外键来完成它。
 
 `PAVLO GOLUB`
 
 ## [谨慎使用CREATE USER](https://www.cybertec-postgresql.com/en/postgresql-using-create-user-with-caution/)
 在Postgres中区分用户和角色对于数据库管理至关重要。
 
 `HANS-JÜRGEN SCHÖNIG`
 
 ## [如何使用pgBackRest备份Postgres（和TimescaleDB）](https://severalnines.com/blog/how-use-pgbackrest-backup-postgresql-and-timescaledb)
 
 `SEBASTIAN INSAUSTI`
 
 ## [如何识别慢速查询](https://dev.to/pythonmeister/how-to-identify-slow-queries-in-postgresql-4igk)
 我们在第301期中就此做了一个提示，但本文进一步说明了如何使用pg_stat_statements扩展来查看查询执行统计信息。

`STEFAN SONNENBERG-CARSTENS`

## [在Raspberry Pi上Postgres的性能](https://blog.rustprooflabs.com/2019/04/postgresql-pgbench-raspberry-pi)
好吧，你可能不会使用Raspberry Pis来托管你的生产数据库，但作为乐于尝试的人，我很高兴看到有人这么做。

`RYAN LAMBERT`

## [与PostgreSQL，MongoDB和JSON共进午餐](https://www.ongres.com/blog/having-lunch-with-postgresql-mongodb-json/)
比较PostgreSQL和MongoDB中的JSON处理，最终Postgres更胜一筹。

`ÁLVARO HERNÁNDEZ`

# 🏖你可以给我们提供一些提示吗？
本周的Postgres本周提示将会休息一下，但是下周将会回归。如果您有任何建议或提示，可以在[这里提交](https://cooperpress.typeform.com/to/bTSq7v)，一经采用我们将支付最高达100美元的稿费:-)

🗓  即将举办的Postgres活动  

 [pgconf.de 2019 (5月10日,莱比锡)](https://2019.pgconf.de/) ——最成功的德语PostgreSQL会议。  
 [PGDay.IT 2019 (5月16-17日,博洛尼亚)](https://2019.pgday.it/en/)  
 [PGCon 2019(5月28-31日,渥太华)](https://www.pgcon.org/2019/) ——一个年度会议，供用户和开发人员见面和讨论Postgres。  
 [PostgreSQL Ibiza(六月19-21日, 伊维萨)](https://www.pgibz.io/index.html) —— 这个在西班牙著名的度假岛上举行的会议将会带来“海滩上的Postgres”，同时仍然在一个漂亮整洁的场地上进行会谈和培训。  
 [Postgres Vision 2019(6月24日,波士顿)](https://postgresvision.com/)  
