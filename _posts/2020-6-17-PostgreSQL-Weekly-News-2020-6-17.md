---
layout: post
title: PostgreSQL 每周新闻 2020-6-17
---
### PostgreSQL每周新闻#360 - 2020年6月17日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)
备注：[英文原文地址](https://postgresweekly.com/issues/360)
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/v1592353852/fcvz8isytnc7mmlufysc.png)
## [Jepsen在Postgres 12.3中发现错误](https://postgresweekly.com/link/90206/web)
“Jepsen”这个名字肯定会激起任何数据库服务器创建者的情绪，因为他们对分布式系统（例如数据库！）的分析经常揭示出各种极端情况和缺陷。Postgres也是如此，它发现了可序列化隔离中的一个错误。这是技术性的东西，但是很高兴看到Postgres这样的系统受到如此严格的分析。


`Kyle Kingsbury `
## [Postgres中的一个单词如何实现9倍性能提升](https://postgresweekly.com/link/90207/web)
个人理财工具的创建者遇到了一个用户，该用户的数据导致大量的INSERT泛滥成灾。这是一个简单的RETURNING子句如何在过程中实现巨大优化的故事。


`James Long `
## [网络研讨会|分布式SQL：现代的云原生PostgreSQL](https://postgresweekly.com/link/90208/web)
遇到挑战扩展PostgreSQL，将其部署在云中或与微服务架构一起使用？分布式SQL数据库可能更适合您的工作负载。明天（6月18日）收听，以进行架构审查和现场演示。


`COCKROACH LABS `
## [Citus 9.3发布：Postgres水平缩放扩展](https://postgresweekly.com/link/90209/web)
Citus是Microsoft现在拥有的Postgres扩展程序，它将Postgres变成一个分布式数据库，可以在多个服务器之间更强大地使用它。 9.3改进了对分布式SQL的支持，现在完全支持窗口功能。 


`citusdata `
## [XgeneCloud：任何数据库上的即时REST和GraphQL API](https://postgresweekly.com/link/90210/web)
自然地，“任何”都包括Postgres :-)这有很多方面，它们似乎正在围绕该技术组建一家公司，但它仍然是开源的。


`xgenecloud `
## [了解PgBouncer中的用户管理](https://postgresweekly.com/link/90212/web)
PgBouncer是Postgres的流行连接代理和合并器，但它不仅将事情直接传递给Postgres，它还可以直接处理身份验证。本文阐明了它是如何工作的。


`Peter Eisentraut `
## [通过语句超时控制失控查询](https://postgresweekly.com/link/90214/web)
在良好硬件上经过良好调整的数据库可以轻松地每秒处理数千个查询，但是寿命长的查询会很快导致备份。这是针对希望永生的查询的一种防御措施。


`Craig Kerstiens `
## [Postgres上的免费，多节点，PB级的时间序列数据库](https://postgresweekly.com/link/90215/web)
详细了解Timescale的多节点时间序列数据库以及为何免费提供该数据库。


`Timescale `
## [在连接时控制服务器变量](https://postgresweekly.com/link/90216/web)
一个简短的提示。例如：psql'options = -cwork_mem = 100MB dbname = test'


`Bruce Momjian `
## [Postgres中的复合数据类型性能问题](https://postgresweekly.com/link/90217/web)
l,null,"en


`Hans-Jürgen Schönig `
## [在FreeBSD上运行pgbackrest](https://postgresweekly.com/link/90218/web)
pgbackrest是Postgres的备份和还原系统。


`Luca Ferrari `
## [pq：用于数据库/ sql的Pure Go（lang）Postgres驱动程序](https://postgresweekly.com/link/90220/web)
现在支持GSS身份验证。


`Blake Mizerany and contributors `
# 💡本周提示


**🗓即将举办的Postgres活动**
- [Postgres Vision 2020](https://postgresweekly.com/link/90221/web)在6月23-24日。多天多次尝试在线进行一次在线Postgres会议。

- [Postgres Pulse](https://postgresweekly.com/link/90222/web) - 与Bruce Momjian，Vibhor Kumar和EnterpriseDB的其他人进行基于缩放的会话。现在每隔一周在美国东部时间上午11点运行。下一个是6月29日。
