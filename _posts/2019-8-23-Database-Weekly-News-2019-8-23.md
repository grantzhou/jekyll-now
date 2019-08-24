---
layout: post
title: 数据库每周新闻 2019-8-23
---

## 数据库每周新闻 #268 - 2019年8月23日

![config.yml]({{ site.baseurl }}/images/DBWeekly.png)
备注：[英文原文地址](https://dbweekly.com/issues/266)

![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/v1566560254/m4vbujuwwetgzf6mm7me.png)

## [学习怎样在微秒量级内查询1.3万亿行数据](https://pingcap.com/success-stories/lesson-learned-from-queries-over-1.3-trillion-rows-of-data-within-milliseconds-of-response-time-at-zhihu/)

本周我们将进行一个详细的技术案例研究，知乎是中国最大的问答网站，拥有超过2.2亿用户。这篇文章深入探讨了他们如何利用tidb横向扩展减少相应时间。

`XIAOGUANG SUN`

## [DigitalOcean推出了Managed MySQL和Redis服务](https://blog.digitalocean.com/take-the-worry-out-of-managing-your-mysql-redis-databases/)

今年早些时候，我们写了DigitalOcean提供Managed PostgreSQL服务的步骤，现在是MySQL和Redis。

`ANDRÉ BEARFIELD`

## [将Oracle迁移至云的5个决断点 ](https://info.enterprisedb.com/WhitepaperMovingOracleWorkloadstotheCloud.html)

本技术指南涵盖了您需要做出的五个关键决策，以指导您的选择并使您获得成功。

`ENTERPRISEDB `

## [Startup Rockset将SQL添加至DynamoDB](https://www.datanami.com/2019/08/21/startup-rockset-adds-sql-to-dynamodb/)

这是一个无服务器搜索和分析启动，它已经推出了一个针对AWS典型的NoSQL DynaModb的SQL平台。

`DATANAMI`



## [Percona基于Postgres11的分布式现在发布](https://www.percona.com/blog/2019/08/19/percona-distribution-for-postgresql-11-beta-is-now-available/)

Percona，可能更以其MySQL性能专业知识而闻名，现在也在Postgres世界中。Postgres11的这个Percona风格的发行版包含了各种工具和扩展，使Postgres更加强大和可扩展。

`BORYS BELINSKY (PERCONA)`



## [CouchBase Mobile](https://hackernoon.com/couchbase-mobile-the-power-of-nosql-on-the-edge-dkdhx30jl)

couchbase是一个分布式nosql数据库，它最初汇集了couchdb和memcached的思想。CouchBase Mobile使CouchBase能够直接在最终用户的设备上运行，并在适当的时候与云中的主数据库同步，从而使事情进一步发展。



## 快速浏览

- 在亚马逊2019年的“黄金日”期间，亚马逊dynamodb每秒提供4550万个请求，总通话量达7.11万亿次。

- 一个以人工智能为核心的1.2万亿晶体管芯片已经问世。从一个典型的现代英特尔CPU的大约100亿个跃迁而来。

- 据报道，由于一台关键服务器没有密码保护，数千部未加密的电影通行证客户卡号和其他数据已暴露数月。

### 💻招聘

[首席云安全工程师](https://www.cockroachlabs.com/careers/job/?gh_jid=1746802&gh_src=59299dec1)-作为我们的第一个安全工程师，发挥作用，专注于推动围绕我们的云安全工作的创新和最佳实践。

[Vettery有需求DB开发人员](https://www.vettery.com/tech?utm_source=newsletter&utm_medium=cooper-dbweekly&utm_term=tech&utm_content=grouped&utm_campaign=ad-88878)——准备好大胆的职业发展了吗？制作一份免费的个人资料，标明你期望的待遇，并与当今顶尖雇主的招聘经理联系。



### 📒 其他

[了解apache arrow flight-arrow flight](https://www.dremio.com/understanding-apache-arrow-flight/)--arrow flight是一种用于大容量数据传输的高性能有线协议，用于分析现代数据传输需求（包括安全性、并行性和平台独立性）。它在引擎盖下使用GRPC和HTTP/2。

`LUCIO DAZA`

[怎样在SQL查询中添加IF-ELSE逻辑](https://dev.to/helenanders26/sql-201-how-to-add-if-else-logic-to-sql-queries-41j)——介绍CASE

`HELEN ANDERSON`

[在aws aurora上使用proxysql实现mysql负载平衡](https://severalnines.com/database-blog/database-load-balancing-proxysql-aws-aurora)--介绍如何使用开放源代码mysql代理proxysql来平衡aurora数据库的负载。

`KRZYSZTOF KSIAZEK`

[Badoo的数据工程：每天处理200亿个事件](https://www.infoq.com/news/2019/08/badoo-20-billion-events-per-day/)Badoo是一个在线交友网络，在他们的堆栈中使用Protobuf、Exasol、Spark和Cubedb。还有20分钟的谈话。

`INFOQ`

[supersqlite:python的sqlite库](https://github.com/plasticityai/supersqlite)

提供了独特的功能，如HTTP上的远程流和扩展捆绑，如JSON、R-Trees（地理空间索引）和全文搜索

`PLASTICITY`

[KVROCKS：基于ROCKSDB的ReIDIS兼容的关键值数据库](https://github.com/meitu/kvrocks)

一个新的开源数据存储库，用C++支持命名空间、MySQL ESK复制，但目的是使用SSD磁盘作为后端存储来增加容量（相对于ReISIS面向内存的方法）。

`MEITU`

[pgcmd：一个非交互式的postgresql查询cli工具](https://github.com/soheilpro/pgcmd)——本质上它允许您连接到postgres数据库，发出查询，并以json格式返回结果。

`SOHEIL RASHIDI`



