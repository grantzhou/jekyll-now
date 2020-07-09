---
layout: post
title: PostgreSQL 每周新闻 2020-7-8
---
### PostgreSQL每周新闻#363 - 2020年7月8日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)
备注：[英文原文地址](https://postgresweekly.com/issues/363)
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/v1593533532/n1oxkrkkiu4xysoxgtav.jpg)
## [使用system_stats扩展程序监视Postgres](https://postgresweekly.com/link/91417/web)
system_stats是一个新的扩展程序（在EDB中，以前是EnterpriseDB），它由多个存储过程组成，可用于监视Postgres（或更准确地说，是它运行的服务器）。


`Dave Page `
## [生成实际上不是的随机字符串和整数](https://postgresweekly.com/link/91419/web)
一种在PL / pgSQL函数中创建“看起来很随机”的优惠券代码或类似字符串的方法。


`Josh Williams `
## [我们已经帮助数百名客户加快了Postgres的速度。了解我们的最佳实践](https://postgresweekly.com/link/91420/web)
通过pganalyze，像Robinhood这样的公司能够将查询速度提高几个数量级。在这本电子书中，我们分享了优化Postgres性能的最佳实践。


`pganalyze `
## [Bitnine希望通过AGE扩展Postgres](https://postgresweekly.com/link/91421/web)
AgensGraph是一个基于Postgres的事务图数据库，但是现在已经演变为一个名为AGE的新项目，并且正在由Apache进行孵化。


`Datanami `
## [Amazon RDS现在可在AWS Outposts上工作](https://postgresweekly.com/link/91424/web)
让我们解开这件事。 RDS（关系数据库服务）是AWS的服务，用于在云中运行Postgres（和MySQL）。 AWS Outpost是一种将AWS体验带入您自己的数据中心的方法。因此，现在您可以在自己的物理环境中在AWS的硬件上使用AWS的云数据库服务。好的，我知道了！ 


`AWS `
## [使用CREATE DOMAIN创建新的数据类型](https://postgresweekly.com/link/91427/web)
如果要创建比默认数据类型所能提供的更高级的服务器端数据类型约束，则可以创建自己的数据类型（域）。


`Hans-Jürgen Schönig `
## [Postgres 12中的生成列与触发器](https://postgresweekly.com/link/91428/web)
Postgres 12引入了生成列的概念，即从其他列的值生成的列。这篇文章比较了使用触发器到类似目的的性能。


`Emanuel Calvo and Anthony Sotolongo `
## [更多的Postgres 13功能：B树索引中的重复数据删除](https://postgresweekly.com/link/91431/web)
今年晚些时候发布的Postgres 13具有一项功能，可以通过避免重复来减小B树索引的大小。这篇文章包括一个人为设计的例子，以炫耀差异。


`Hamid Akhtar `
## [企业就绪的PostgreSQL | ](https://postgresweekly.com/link/91433/web)
服务产品组合，可帮助您进行PostgreSQL之旅。数据迁移。混合云。高可用性。


`EDB `
## [
Storj如何从Postgres迁移到CockroachDB：批量加载性能](https://postgresweekly.com/link/91435/web)
l,null,"en


`Jessica Grebenschikov `
## [plpgsql_check：PL / pgSQL代码检查器](https://postgresweekly.com/link/91437/web)
一种专用工具，用于当您希望发现潜伏在PL/pgSQL函数中的任何错误时。刚刚添加了对具有多态类型参数的函数的支持。


`Pavel Stehule `
## [Noisia：Postgres的“有害工作量生成器”](https://postgresweekly.com/link/91443/web)
创建诸如死锁，不执行任何事务的事务以及生成磁盘临时文件的查询之类的东西。为什么？在进行测试，对设置进行压力测试等时，请小心谨慎使用。


`Lesovsky Alexey `
# 💡本周提示


**🗓即将举办的Postgres活动**
