---
layout: post
title: PostgreSQL 每周新闻 2020-3-4
---
### PostgreSQL每周新闻#345 - 2020年3月4日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)
备注：[英文原文地址](https://postgresweekly.com/issues/345)
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/nlwk6d6nenv6p2lxoget.jpg)

## [Postgres查询优化助手Joe Bot](https://postgresweekly.com/link/84766/web)
“Joe”是一个很有意思的项目，但是目前关注它的人很少，它是一个可以与Database Lab（一个开源的实时数据库克隆器）交互的聊天机器人，可以在几乎实时的情况下快速了解真实的查询性能。


`Postgres.ai `
## [如何编写复杂的递归SQL查询](https://postgresweekly.com/link/84768/web)

`Egor Rogov `
## [免费电子书：如何在Postgres数据库上获得3倍的性能提升](https://postgresweekly.com/link/84769/web)
了解我们为像Atlassian这样的客户优化Postgres查询性能的最佳实践，以及如何将从磁盘加载的数据减少500倍。


`pganalyze `
## [通过增加检查点距离来减少WAL](https://postgresweekly.com/link/84770/web)
调整检查点在优化服务器时非常有用，可以提高数据库性能。此外，它有助于总体上减少预写日志的数量。


`Hans-Jürgen Schönig `
## [PGTune：创建Postgres配置设置的Web工具](https://postgresweekly.com/link/84771/web)
选择Postgres版本（现在也支持v12），说明你的数据库的用途，总内存等，它会产生一套优于默认值的配置文件。


`Alexey Vasiliev `
## [Postgres13中的平行vacuum](https://postgresweekly.com/link/84772/web)
虽然花了很多年才取得成果，但支持并行vacuum的主要工作还是致力于Postgres内核。

`Hamid Akhtar `

## [Citus 9.2加速Postgres上的大规模HTAP工作负载](https://postgresweekly.com/link/84773/web)
如果你一直在想“Citus对Postgres的开源扩展发生了什么事？”？“自从团队进入微软以来，简短的回答是‘很多’。Citus 9.2包括HTAP（混合事务分析处理）重要领域的性能改进，包括cte、聚合函数和重新分区连接。


`Marco Slot (Citus Data) `
## [网络研讨会：如何像专业人士一样监控Postgres](https://postgresweekly.com/link/84774/web)
了解为什么必须监视Postgres以及何时不监视此按需网络研讨会。


`EnterpriseDB `
## [Joe Conway访谈录](https://postgresweekly.com/link/84775/web)
Joe，一个PostgreSQL的提交者，已经和PostgreSQL走过了20年，所以他有很多东西要分享。了解他的背景，他对PostgreSQL的贡献，以及他最喜欢的扩展是什么。Lætitia Avrot上周也接受了采访。


`Andreas Scherbaum `
## [GROUPBY和SELECT DISTINCT的优化](https://postgresweekly.com/link/84777/web)


`That Guy From Delhi `
## [Pgpool II的证书认证方法](https://postgresweekly.com/link/84778/web)
生成自签名SSL证书和使用Pgpool II配置证书身份验证的方法。

`Muhammad Usama `

## [如果您的Postgres流复制发生延迟，需要检查什么](https://postgresweekly.com/link/84779/web)
复制延迟可能是一个常见的问题，但本文讨论了在使用Postgres时遇到复制延迟时应注意的事项。


`Paul Namuag `
# 💡本周提示


在我通常的工作中，数据库要么由我手动生成，要么由我在Ruby on Rails或Django等框架中定义的模式生成。在手工操作的情况下，我通常在SQL中布局一个模式，然后根据需要运行相关的CREATE TABLE查询！


但是，如果您需要的模式已经存在一个数据库（例如，对于测试数据库），您知道可以将它用作新数据库的模板吗？


```
CREATE DATABASE appdb_test TEMPLATE appdb;
```


如果您只想对数据库的副本临时运行一些代码（例如在测试中），这可能特别方便。


另一个有趣的小细节是：当您在不指定模板的情况下运行一个普通的CREATE DATABASE命令时，会在后台使用一个名为template1的默认模板数据库，这意味着如果您总是希望同一服务器上的新数据库包含类似的内容，则可以将它们添加到template1数据库中。


例如，如果您总是使用hstore扩展，那么有一个始终针对template1运行CREATE extension hstore的策略可能是有意义的，以确保它在将来出现在新鲜的数据库中（即使它们是从自动化系统或ORMs创建的）。


这里有更多关于这一切的信息。


**🗓即将举办的Postgres活动**
- [Postgres Conference 2020](https://postgresweekly.com/link/84780/web)（3月23日至27日，美国纽约）
- [Nordic PgDay 2020](https://postgresweekly.com/link/84782/web)（3月24日芬兰赫尔辛基）
- [pgDay Paris 2020](https://postgresweekly.com/link/84783/web)（3月26日法国巴黎）
- [Swiss PGDay 2020](https://postgresweekly.com/link/84784/web)（6月18日至19日，瑞士）
- [Postgres Ibiza 2020](https://postgresweekly.com/link/84785/web)（6月25日至26日，西班牙伊比沙岛）
