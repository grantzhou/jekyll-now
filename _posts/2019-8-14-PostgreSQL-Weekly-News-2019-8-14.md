---
layout: post
title: PostgreSQL 每周新闻 2019-8-14
---

### PostgreSQL每周新闻#318 - 2019年8月14日

![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)

备注：[英文原文地址](https://postgresweekly.com/issues/318)

![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/v1565784888/kpdyfke8ozgutzp29xox.jpg)

## [Postgres的服务端程序一览](https://pgdash.io/blog/postgres-server-side-programming.html)

如果你刚刚使用Postgres作为你的数据库服务，你可能还没有意识到它有多强大。使用定义类型、SQL、PL/PSQL函数、存储过程、甚至使用C、Python和Perl扩展Postgres的功能。

`RAPIDLOOP`

## [PostgreSQL 11.5, 10.10, 9.6.15, 9.5.19, 9.4.24, and 12 Beta 3 Released](https://www.postgresql.org/about/news/1960/)

当你能发布6个版本时，为什么要发布一个版本的Postgres？这些发布的动机是修复安全问题和其他bug。

`POSTGRESQL GLOBAL DEVELOPMENT GROUP`

## [2Q PGConf 2019 - CFP 现已开放注册](https://www.2qpgconf.com)

在芝加哥与我们一起学习Postgres最新的研究成果和未来的发展。在这里你可以获得手把手的教学：性能调优、PostgreSQL安全，多主复制。

`2NDQUADRANT POSTGRESQL EVENTS`**赞助商**

## [Postgres的状态：社区调查](https://stateofpostgres.com)

Timescale正在进行Postgres社区调查，并计划公开分享汇总结果和分析结果。

`TIMESCALE`



## [怎么在使用GROUP BY的时候获取第一个和最后一个值](https://www.2ndquadrant.com/en/blog/postgresql-award/)

一个项目获得“终身成就”奖让人感觉很奇怪。好在Mark Wong、Bruce Momjian和Christophe Pettus代表PostgreSQL项目在O'Reilly的Oscon活动上接受了该奖项。

`HAKI BENITA`



## [Postgres的简单时间序列举例](https://www.cybertec-postgresql.com/en/postgresql-trivial-timeseries-examples/)

使用TImescaleDB这样的插件可以增强Postgres的时间序列功能，你也可以使用Postgres吱声完成一些简单是时间序列工作

`HANS-JÜRGEN SCHÖNIG`



## [缩写使网络类型的排序速度加倍](https://www.percona.com/blog/2019/08/02/out-of-memory-killer-or-savior/)

虽然这不会立即被许多读者使用，但这是如此华丽的利基和详细！它深入探讨了在使用Postgres的inet/cidr类型对存储的网络地址进行排序时如何提高Postgres的性能。

`BRANDUR LEACH`



## [提高速度和规模](https://www.gridgain.com/resources/papers/postgresql-speed-and-scale-options-in-memory-computing?adsource=postgresweekly)

学习怎样使用内存计算平台提升Postgres的速度和规模，来支持你的数据密集型应用。

`GRIDGAIN SYSTEMS`



## [自动更新物化视图](http://pgsqlpgpool.blogspot.com/2019/08/automatically-updating-materialized.html)

`GAJUS KUIZINAS`



## [PostGIS 3.0.0alpha4, 2.5.3, 2.4.8, and 2.3.10发布](http://postgis.net/2019/08/11/postgis-patches/)

`POSTGIS DEVELOPERS`



## [Slonik：具有严格类型，详细日志记录和断言的Postgres客户端](https://github.com/gajus/slonik) 

构建在Node.js的pg库之上，Slonik为Postgres CLI体验提供了一些有趣的细节和便利方法。

`GAJUS KUIZINAS`



## [postgres的自适应查询优化](https://github.com/postgrespro/aqo)

要让这个补丁和扩展与postgres一起工作，需要做一些改动，但是一旦这样做了，这是改进查询优化器的一个有趣的实验。仅限高级用户。

`POSTGRES PROFESSIONAL`

# 💡本周提示

###### psqsl的‘expanded’格式模式

由PGX提供



一个（非常）简单的改变！

当我在上周写有关使用pgstattuple查看死行的提示时，我遇到了一些对截图不切实际的输出：

![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/eyqttewffm4vopmvdpvq.jpg)

幸运的是，psql支持一种称为“扩展表格式化模式”的不同类型的输出。通过运行带有-x或--expanded选项的psql启用它，或者在psql已经运行时键入\ x以打开和关闭它。

![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/plddshx3ufnaqxsoqxby.jpg)

这对于截取屏幕截图或复制并粘贴到自述文件或电子邮件中更好

本周提示由[pgexperts](https://postgresweekly.com/link/68300/web)赞助。



🗓  **即将举办的Postgres活动**  

• [PGDay Austria 2019](https://pgday.at/en/)（9月6日， 维纳·纽斯塔特，奥地利）

• [PostgreSQL Conference Asia 2019](https://2019.pgconf.asia/)（9月8-11日，巴厘岛，印度尼西亚）

• [PostgresOpen 2019](https://postgresweekly.com/link/68304/web) (9月11-13日， 佛罗里达)——两天包含有关PostgreSQL和相关技术的教程和演示文稿。

[PostgresConf Silicon Valley 2019](https://postgresweekly.com/link/68305/web)（9月18-20日，圣荷西）——时间表（包括培训）现已公布

[PostgresConf South Africa 2019](https://postgresweekly.com/link/68306/web)（10月8-9日， 约翰内斯堡）——提供给使用Postgres的数据库管理和开发人员互相了解的机会。

[PostgreSQL Conference Europe 2019](https://postgresweekly.com/link/68391/web)（10月15-18日， 米兰）