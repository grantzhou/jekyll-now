---
layout: post
title: PostgreSQL 每周新闻 2021-6-9
---
### PostgreSQL每周新闻#409 - 2021年6月9日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)
备注：[英文原文地址](https://postgresweekly.com/issues/409)
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/qrwhqffegu5tdncphhie.jpg)

## [PLV8 3.0：V8 JavaScript，但适用于 Postgres](https://postgresweekly.com/link/109254/web)
浏览器中、服务器上的 JavaScript ......但是你的数据库内部呢？ PLV8 通过这个刚刚推出新主要版本的扩展，将 JavaScript 的强大功能带入了 Postgres 程序/触发器/等。 [文档在这里](https://plv8.github.io/)。


`plv8 team `
## [EXPLAIN ANALYZE 和如何解释其结果](https://postgresweekly.com/link/109256/web)
本文简要介绍了 EXPLAIN ANALYZE和解释了要查找的内容，并展示了一些用于可视化输出的有用工具。


`Laurenz Albe `
## [Postgres Vision 2021 - 免费在线会议（6 月 22 日至 23 日）](https://postgresweekly.com/link/109269/web)
随着数据爆炸式增长，挑战和机遇也随之而来。 来自世界各地的领导者将在 Postgres Vision 2021 上分享 Postgres 如何为他们的组织创造价值。 你会在那儿吗？


`EDB `
## [在 Postgres 中使用 BIGINT](https://postgresweekly.com/link/109258/web)
“我开始改变我的默认思维方式，改用 BIGINT 而不是 INT，扭转了我长期以来的习惯。 这篇文章解释了为什么我默认使用 BIGINT 并检查决策对性能的影响”。


`Ryan Lambert `
## [关闭自动提交模式如何损坏您的数据库](https://postgresweekly.com/link/109259/web)
除非您使用BEGIN来明确启动一个事务，否则 Postgres 会自动运行您在其自己的事务中发出的每个语句。


`Laurenz Albe `
## [HypoPG 1.3.0：Postgres 的假设索引](https://postgresweekly.com/link/109260/web)
令人惊讶的是我们在 296 个问题之前首次提到这个项目（！）您可以使用 HypoPG 创建实际上不存在的索引，但可以用来确定是否可能使用某些索引 由查询计划器来提高性能。 本周的新版本增加了对 Postgres 10+ 中假设哈希索引的支持。


`PostgreSQL GLobal Development Group `
## [DigitalOcean 的托管数据库服务现在支持 Postgres 13](https://postgresweekly.com/link/109262/web)
好吧，我们应该说 Postgres 10、11、12 和 13。 加上 MySQL 和 Redis。 如果您使用 DO 或想要比 RDS 更便宜的东西，这是一个很有吸引力的选择。 ElephantSQL 也是预算管理 Postgres 空间中需要考虑的另一个参与者。


`Mark Huber (DigitalOcean) `
## [使用 EXPLAIN 查找 Postgres 查询缓慢的根本原因](https://postgresweekly.com/link/109264/web)
关于如何使用 Postgres EXPLAIN 查找和改进有问题的查询计划以及如何使用 auto_explain 的深入指南。


`pganalyze `
## [使用 Datastream 从 Oracle 迁移到 Postgres](https://postgresweekly.com/link/109265/web)
根据 Google 的说法，该工具包使迁移“更容易并最大限度地减少停机时间”。 Datastream 是一个仍处于预览阶段的 Google Cloud 无服务器数据捕获和复制服务。


`Dylan Hercher (Google Cloud) `
## [Postgres 如何提供对时区缩写的访问](https://postgresweekly.com/link/109267/web)


`Bruce Momjian `

