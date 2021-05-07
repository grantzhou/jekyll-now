---
layout: post
title: PostgreSQL 每周新闻 2021-5-5
---
### PostgreSQL每周新闻#404 - 2021年5月5日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)
备注：[英文原文地址](https://postgresweekly.com/issues/404)
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/psuhygcnaxoh6wlhdjje.jpg)
## [使用SQL，PL / PGSQL和Python创建测试数据](https://postgresweekly.com/link/107378/web)
Greg认为，即时创建测试数据可以鼓励您更深入地思考数据模型（这是一件好事），并且可以轻松地按您选择的规模工作。本教程一个有趣的方面是，您可以继续使用Docker。


`Greg Schafer `
## [无操作，可扩展和灵活的Postgres替代方案](https://postgresweekly.com/link/107379/web)
Fauna将Postgres的操作完整性和关系建模与界面和体系结构相结合，该界面和体系结构更适合现代云中的应用程序开发。没有操作瓶颈的Postgres的优点-了解有关Fauna的更多信息。


`Fauna `
## [Supabase：通过WebSocket实时监听数据库更改](https://postgresweekly.com/link/107380/web)
我们在一年多以前第一次提到这个项目，并且它正在不断获取更新（这是他们的最新消息）。他们还发布了一个系统，可将Stripe帐户连续同步到Postgres数据库。


`Supabase `
## [Dave Page的访谈](https://postgresweekly.com/link/107383/web)
PostgreSQL本周人物系列的最新一次访谈是与社区中一位杰出人士的一次实质性访谈（他是核心团队和董事会成员，并且从事Postgres已有20多年了） 。


`Andreas Scherbaum `
## [JSONB多列类型转换](https://postgresweekly.com/link/107384/web)
我最近一直在做大量的jsonb列的工作，并且这种简洁的方式逐一键入施法的多个值完全通过。


`Bruce Momjian `
## [TLS：揭秘Postgres中的通信加密](https://postgresweekly.com/link/107385/web)
（传输层安全性）是一种广泛使用的技术，用于加密包括Postgres在内的客户端/服务器连接。以下是涉及的主要概念的高级概述。


`Julian Markwort `
## [使用EXPLAIN查找缓慢的Postgres查询的根本原因](https://postgresweekly.com/link/107386/web)
有关如何使用Postgres EXPLAIN来查找和改进有问题的查询计划以及如何使用auto_explain的深入指南。


`pganalyze `
## [usql 0.9：数据库通用CLI ](https://postgresweekly.com/link/107389/web)
一种用于与Postgres，SQL Server，MySQL，SQLite3，Oracle Database，CockroachDB等一起使用的CLI工具（用Go编写）。如果需要的话，可以使用数据库瑞士军刀。v0.9.0添加了命令自动完成功能，\copy在数据库之间移动数据的命令等。


`Kenneth Shaw `
## [Datanymizer：具有灵活规则的数据库匿名器](https://postgresweekly.com/link/107392/web)
用Rust编写，此工具为Postgres提供了进行中的模板驱动的数据匿名处理（仅目前，MySQL支持正在进行中）。


`Evrone `
## [sqlc 1.8：从SQL生成类型安全的Go（lang）](https://postgresweekly.com/link/107394/web)
—您编写SQL查询，运行sqlc以生成用于这些查询的代码和接口，然后编写用于调用上述代码的Go代码。1.8.0通过升级基础依赖项增加了对Postgres 12和13功能的支持。


`Kyle Conroy `
# 💡本周提示


**🗓即将举办的Postgres活动**
