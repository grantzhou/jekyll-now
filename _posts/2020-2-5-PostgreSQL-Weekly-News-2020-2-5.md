---
layout: post
title: PostgreSQL 每周新闻 2020-2-5
---
### PostgreSQL每周新闻#341 - 2020年2月5日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)
备注：[英文原文地址](https://postgresweekly.com/issues/341)
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/ptxjxrxaxroft1w5ja1h.jpg)

## [Postgres 12中全文搜索的状态](https://postgresweekly.com/link/83369/web)
在FOSDEM的50分钟精彩演讲中，介绍Postgres 12全文搜索功能的来龙去脉。在这次演讲中有很多很棒的东西，这里有非常详细的幻灯片。

`Jimmy Angelakos `

## [Postgres的行变更审计选项](https://postgresweekly.com/link/83371/web)
如果您想为一段时间内对表所做的所有行变更建立一个“审计跟踪”，下面将介绍实现它的方法的优缺点。

`Kaarel Moppel `

## [在CockroachDB上构建Django应用程序](https://postgresweekly.com/link/83372/web)
Django简化了与数据库的交互，这也是它成为最流行的Python web框架的原因之一。使用CockroachDB和Django可以轻松地使用Python编写，同时获得开源分布式SQL数据库的所有好处。


`Cockroach Labs `
## [最被忽视的Postgres功能？](https://postgresweekly.com/link/83373/web)
但这是一个有趣的帖子，关于使用log_line_prefix来构建更智能的日志文件。

`Richard Yen `

## [三种Postgres作业调度工具](https://postgresweekly.com/link/83374/web)
上周我们介绍了pg_timetable，这是一个新的高级的Postgres作业调度程序，但是还有其他的解决方案，包括cron，pgAgent和pg_cron扩展。

`Severalnines `

## [Postgres 12在Heroku上发布](https://postgresweekly.com/link/83376/web)
Postgres 12现在是新Heroku Postgres数据库的默认版本。

`Heroku `

## [Amazon关系数据库服务（RDS）现在可以将快照导出到S3](https://postgresweekly.com/link/83377/web)
现在，您可以将Amazon关系数据库服务（Amazon RDS）或Amazon Aurora快照作为Apache Parquet导出到Amazon S3，Apache Parquet是一种用于分析的高效开放列存储格式。


`Amazon Web Services `
## [SQL查询中的空值](https://postgresweekly.com/link/83378/web)
SQL查询中空值的概念经常给开发人员带来麻烦，本文将巧妙地解释它们的特殊状态以及它如何影响查询。针对Oracle用户，但也适用于Postgres。

`Kaley Crum `

## [用pg_catcheck检查目录是否损坏](https://postgresweekly.com/link/83379/web)


`Luca Ferrari `
## [使用Buildkite为所有软件项目提供更快的CI/CD](https://postgresweekly.com/link/83380/web)
看看Shopify如何将300名工程师扩展到1500名，同时将他们的构建时间控制在5分钟以内。


`Buildkite `
## [获取假日日期的PL/pgSQL包](https://postgresweekly.com/link/83381/web)
例如：按国家（加拿大，2020，2020）从假日中选择*；


`Christopher Thompson `
## [PostGIS 3.1 Alpha 1发布](https://postgresweekly.com/link/83382/web)
一个只为最前卫的PostGIS用户。针对Postgres12.1，但也与开发中的Postgres13分支合作。


`PostGIS Developers `
# 💡本周提示


在过去的几年里，我们在时事通讯中包含了很多psql技巧，但是考虑到psql是多么成熟和功能丰富，我们总是可以分享更多的东西。今天，我们将快速查看\pset，这是一个用于设置输出格式选项的命令。


psql文档中包含了完整的选项列表，因此我们将重点介绍几个示例：


\pset null'ø'使psql将空值显示为ø字符（类似于'empty set'符号），而不是容易丢失的空白。


\pset linestyle和\pset border允许您更改在结果表周围放置（或不放置）边框的方式：


另一个相对较新的特性是，运行不带任何参数的\pset将显示所有不同设置及其当前值的列表。。所以你可以自由发挥。

**🗓即将举办的Postgres活动**

- [PgConf India](https://postgresweekly.com/link/83385/web)（2月26日至28日，印度班加罗鲁）
- [Postgres Conference 2020](https://postgresweekly.com/link/83383/web)（3月23日至27日，美国纽约）
- [Nordic PgDay 2020](https://postgresweekly.com/link/83386/web)（3月24日芬兰赫尔辛基）
- [pgDay Paris 2020](https://postgresweekly.com/link/83387/web)（3月26日，法国巴黎）
- [Swiss PGDay 2020](https://postgresweekly.com/link/83389/web)（6月18日至19日，瑞士）

