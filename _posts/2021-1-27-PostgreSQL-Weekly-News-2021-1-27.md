---
layout: post
title: PostgreSQL 每周新闻 2021-1-27
---
### PostgreSQL每周新闻#390 - 2021年1月27日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)
备注：[英文原文地址](https://postgresweekly.com/issues/390)
![img](https://res.cloudinary.com/cpress/image/upload/v1611669682/xnlqjbit939y7ykb9rvo.png)

## [Postgres基于ARM的AWS EC2实例：它是否有好处？](https://postgresweekly.com/link/101879/web)
与苹果开发他们自己的基于ARM的芯片一样令人兴奋，AWS也在自己的Graviton2 CPU上取得了巨大的进步——下面是他们在运行Postgres时的表现。总之，这是个好消息。去年一篇关于Postgres如何在M1芯片上运行的帖子也可能引起关注。


`Jobin Augustine and Sergey Kuzmichev `
## [Postgres扩展建议2021](https://postgresweekly.com/link/101881/web)
关于单个Postgres实例可以扩展多远以及为什么它比扩展整个集群更好的想法和见解。您的用例是否需要每秒数万个事务？


`Kaarel Moppel `
## [实时Postgres性能监测](https://postgresweekly.com/link/101882/web)
收集现成的和定制的PostgreSQL度量，并将它们与分布式基础设施、应用程序和日志中的数据相关联。获取实时性能见解，并使用Datadog设置智能警报。开始免费试用。


`Datadog `
## [一个约会应用程序的Postgres12之旅](https://postgresweekly.com/link/101883/web)
一个约会应用程序的Postgres12之旅——Coffee Meets Bagel是一个约会系统（在某种程度上），他们最近将自己的集群从Postgres9.6升级到了12.4。这里介绍了升级和Postgres的一般使用方法（当然，还有一个架构图！😍)。

`Tommy Li `

## [Heroku宣布了更大的Postgres计划（和连接池）](https://postgresweekly.com/link/101884/web)
即使你不使用Heroku，这些年来他们对Postgres空间产生了相当大的影响，并且是最早提供这种规模的服务之一。他们的计划现在增加到768GB的RAM和4TB的存储空间，不，它们一点也不便宜😆 在其他Heroku新闻中，他们已经为Postgres提供了连接池。。


`Greg Nokes (Heroku) `
## [北欧PGDAY 2021取消了](https://postgresweekly.com/link/101885/web)
一年前，当面对面活动开始被取消时，我没想到一年后仍然会发生，但北欧PGDay现在推迟到2022年3月在赫尔辛基举行。


`PostgreSQL Europe `
## [Postgres的金色比例](https://postgresweekly.com/link/101886/web)
如果两个量的比值等于它们的总和与两个量中较大者的比值，那么这两个量就是黄金比例... 了解了？Hans-Jürgen Schönig展示了如何使用Postgres帮助进行此类计算。 


`Hans-Jürgen Schönig `
## [免费电子书：使用Postgres的Rails高效搜索](https://postgresweekly.com/link/101887/web)
将搜索查询的速度从几秒提高到几毫秒，并了解精确匹配、trigrams、ILIKE和全文搜索。。


`pganalyze `
## [Postgres复制如何运作](https://postgresweekly.com/link/101888/web)
Postgres复制、HA配置、集群等方法的高级教程。


`Adriano `
## [Postgres动态哈希的初步探索](https://postgresweekly.com/link/101889/web)
如果你对Postgres如何处理它的哈希表感兴趣，那么可以在Postgres内部进行更多的探索。


`Neil Chen `
## [PG_Activity 2.0：一个类似top的Postgres服务器活动监控工具](https://postgresweekly.com/link/101896/web)
就像您可以在服务器上使用top来监视进程和CPU使用情况一样，pgu活动为检查PostgreSQL提供了类似的方法。2.0.0刚刚发布。 

`Dalibo `

## [pg_hint_plan：让Postgres能够在执行计划中手动强制执行某些决策](https://postgresweekly.com/link/101898/web)

`NTT OSS Center DBMS Development and Support Team `
# 💡本周提示


psycopg2是一个流行的Postgres数据库适配器，面向Python开发人员，它的维护人员最近开始着手进行psycopg3的大型升级（他非常希望得到您的支持）。我对一个已经很流行的库需要一个主要的新版本很感兴趣，所以问了他几个问题：详见原文


**🗓即将举办的Postgres活动**
