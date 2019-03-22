---
layout: post
title: PostgreSQL 每周新闻 2019-03-20
---

### PostgreSQL每周新闻#297 - 2019年3月20日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)

备注：[英文原文地址](https://postgresweekly.com/issues/297)

![pg_img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/kodl8cm0uhix6qto8ih0.jpg)

## [Azure Data Studio：开源GUI工具现在支持Postgres](https://azure.microsoft.com/en-us/blog/azure-data-studio-an-open-source-gui-editor-for-postgres/)
Postgres的psql命令行客户端非常棒，但有些人更喜欢图形工具，而Microsoft的Azure Data Studio现在对Postgres有预览级支持。他们还在[VS Code的扩展中](https://github.com/Microsoft/vscode-postgresql)发布了类似的工具。

`RACHEL AGYEMANG (MICROSOFT)`

## [注册Postgres-BDR 60天试用版](https://resources.2ndquadrant.com/postgres-bdr-trial)
![img](https://copm.s3.amazonaws.com/e3a3cff1.png)  
作为多主复制的最强大工具，Postgres-BDR显著降低了主故障的影响，并最大限度地降低了数据丢失的风险。BDR可以提供多达五个9的可用性，即时恢复，滚动升级等。

`2NDQUADRANT POSTGRESQL PRODUCTS` **赞助商**

## [垂直扩展PostgreSQL](https://pgdash.io/blog/scaling-postgres.html)
Postgres非常容易使用额外的资源（CPU，内存，磁盘等），但并非都是自动的，有时可以进行调整。 当然，如果你想为Postgres进行一些水平扩展，请查看[Citus](https://github.com/citusdata/citus)。

`RAPIDLOOP`

## [postgresqltuner.pl：获取调优建议的简单脚本](https://github.com/jfcoz/postgresqltuner)
一个分析Postgres数据库配置并提供调整建议的脚本。

`JULIEN FRANCOZ`

## [外部数据封装器（FDW）性能调优](https://www.cybertec-postgresql.com/en/foreign-data-wrapper-for-postgresql-performance-tuning/)
postgres_fdw有一些隐藏的调优选项，但是大部分用户并不知道。

`HANS-JÜRGEN SCHÖNIG`

## [如何将Postgres数据复制到远程站点](https://severalnines.com/blog/how-replicate-postgresql-data-remote-sites)
文章对比了Slony，Bucardo，逻辑复制和FDW

`VENKATA NAGOTHI`

## [▶如何管理和自动化PostgreSQL](https://severalnines.com/resources/webinars/how-automate-manage-postgresql-clustercontrol?utm_campaign=Choosing_MySQL_HA_Campaign_MAR18&utm_content=pgweekly&utm_medium=Email&utm_source=Link_Click)
请观看我们最近关于PostgreSQL自动化功能的网络研讨会的免费重播。

`SEVERALNINES` **赞助商**

## [SQL的乐趣：文本和系统函数](https://www.citusdata.com/blog/2019/03/13/fun-with-sql-text-functions/)
文章主要介绍了Postgres的position函数以及其他一些有用的相关函数。

`CRAIG KERSTIENS`

## [使用pg_dumpall升级PostgreSQL](https://www.percona.com/blog/2019/03/18/postgresql-upgrade-using-pg_dumpall/)
文章介绍了使用pg_dumpall升级Postgres。pg_dumpall非常适合集群，并且相对简单，但对于特别大的数据库它并不是理想的选择。

`AVINASH VALLARAPU`

# ![_config.yml]({{ site.baseurl }}/images/Tips-icon.png)   本周提示
由Citus Data提供支持

## 在psql中使用\watch 
(这真的是“会就是会，不会就是不会”的提示之一！)

Postgres的psql客户端附带了许多[元命令](https://www.postgresql.org/docs/10/app-psql.html#APP-PSQL-META-COMMANDS)，可以帮助您浏览数据库并执行各种管理功能。一个特别有趣的命令是\watch。

最简单的是，\watch每2秒运行一次最新运行的查询（来自psql的查询缓冲区)。如果你指定一个单位为秒的参数，那么它将每隔 X 秒运行一次查询：比如， \watch 1指每秒运行一次。 使用CTRL + C可以跳出循环。

假如你总是想看到你的应用最后添加的用户，那这个命令应该很有用。例如：

`SELECT * FROM users ORDER BY created_at DESC LIMIT 1; \watch 30`  

另一个有趣的用途是监视Postgres服务器上当前正在运行的所有查询（当然，只有那些以1秒为间隔运行的查询会被跟踪）:

`SELECT datname, usename, query FROM pg_stat_activity; \watch`  

> 本周提示由[Citus Data](https://www.citusdata.com/?utm_source=PG_Weekly&utm_medium=email&utm_campaign=sponsor_blog)提供支持，Citus Data现在是微软家族的一员。访问[Citus Data博客](https://www.citusdata.com/blog/?utm_source=PG_Weekly&utm_medium=email&utm_campaign=sponsor_blog)来详细了解Citus如何扩展Postgres。

🗓  即将举办的Postgres活动  

 [pgconf.de 2019 (5月10日,莱比锡)](https://2019.pgconf.de/) ——最成功的德语PostgreSQL会议。  
 [PGDay.IT 2019 (5月16日,博洛尼亚)](https://2019.pgday.it/en/)  
 [PGCon 2019(5月28日,渥太华)](https://www.pgcon.org/2019/) ——一个年度会议，供用户和开发人员见面和讨论Postgres。  
 [Postgres Vision 2019(6月24日,波士顿)](https://postgresvision.com/)  
 
