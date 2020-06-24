---
layout: post
title: PostgreSQL 每周新闻 2020-6-24
---
### PostgreSQL每周新闻#361 - 2020年6月24日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)
备注：[英文原文地址](https://postgresweekly.com/issues/361)
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/v1592996647/hzfrltkirjio5g3b34nj.jpg)
## [Postgres可以改善的“十件事”](https://postgresweekly.com/link/90641/web)
正在进行的四部分系列文章（此处为第2部分），涉及诸如事务ID问题和复制之类的主题。


`Shaun Thomas `
## [现在是时候实现JSON / JSONB的统一了](https://postgresweekly.com/link/90642/web)
📊PDF：如果您真的喜欢JSON并且非常在意Postgres的JSON功能，那么这个密集的技术滑盖非常适合您。 它探讨了即将发布的SQL标准中对JSON的支持，以及Postgres的未来版本可以通过将JSON和JSONB统一成为一种新的数据类型来实现这一点。



`Oleg Bartunov `
## [我们帮助客户将Postgres查询速度提高1000倍。 学习怎样](https://postgresweekly.com/link/90643/web)
借助pganalyze，像Atlassian这样的公司可以将查询速度提高几个数量级。 在这本电子书中，我们分享了优化Postgres性能的最佳实践。


`pganalyze `
## [Postgres 13 Beta 1现在可在Amazon RDS数据库预览环境中使用](https://postgresweekly.com/link/90644/web)
RDS允许您在AWS上运行的Postgres部署，预览环境可以让您使用预发行版本来测试一些工具等等，


`Amazon Web Services `
## [如何强制一个表只有一行](https://postgresweekly.com/link/90646/web)
Bruce透过在恒定值上创建一个UNIQUE索引（没有列名引用）来演示如何强制一个表最多具有一行。


`Bruce Momjian `
## [EnterpriseDB重命名为EDB](https://postgresweekly.com/link/90647/web)
EnterpriseDB是Postgres领域中的热门公司，因此，如果您现在在任何地方看到 “EDB”，那就是它们:-)

`EnterpriseDB / EDB `
## [SQL技巧：假想的聚合](https://postgresweekly.com/link/90648/web)
您可以使用此技术来推算现有数据集中的假想值等级。


`Hans-Jürgen Schönig `
## [tuned，Postgres和You](https://postgresweekly.com/link/90649/web)
tuned是一个动态系统调整程序（来自Red Hat），可以根据使用情况动态调整系统设置。 这篇文章演示了如何为Postgres特别创建经过调整的配置文件。


`Douglas J Hunley `
## [ltree与WITH RECURSIVE](https://postgresweekly.com/link/90651/web)
这是Hans-Jürgen关于分层查询的文章的后续内容。


`Hans-Jürgen Schönig `
## [您的数据就是您的业务](https://postgresweekly.com/link/90653/web)
PGX是一家提供全面服务的数据库咨询公司，专注于在任何平台或托管环境上的PostgreSQL数据系统。


`PostgreSQL Experts, Inc. `
## [用Postgres包装Db2](https://postgresweekly.com/link/90654/web)
Db2是IBM开发的一系列数据库产品，主要用于企业用途。 如果需要将Db2数据迁移到Postgres，db2_fdw提供了一种方法。


`Marcelo Diaz `
## [从Oracle迁移到Postgres的原因](https://postgresweekly.com/link/90656/web)
这确实是本新闻稿中 “preaching to the choir” （俚语：意指想再说服已经相信的人）的一种情况，但是如果您在与其他人聊天时还需要更多原因。。 😄


`Kirk Roybal `
## [pg_auto_failover：自动故障转移和高可用性扩展](https://postgresweekly.com/link/90657/web)
监视和管理Postgres集群的自动故障转移。


`Citus Data `
# 💡本周提示


在方言之间转换SQL

这是那些“工具”提示之一，您现在不太可能需要它，但是将来某个时候您会发现：“啊！我知道我需要解决这个问题！” 😂

假设您用方言编写了一些与Postgres不兼容的SQL，或者可能是相反的，您需要将Postgres查询带入Oracle或SQL Server世界-您能做什么？

您可以查阅文档并确定如何在SQL方言之间进行转换，或者首先查阅jOOQ SQL Translator：

![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/v1592842516/ste9av2ep4irqq6d2rve.jpg)

它远非完美的工具，但如果您忘记了有关Oracle，SQL Server（或该工具支持的几种方言之一）的怪癖，它可以提供有用的意义检查，而我已经多次依靠它来翻译 检查我向他人建议的SQL是否得到广泛支持。

本周的提示由Retool赞助。 在几天（而不是几周）内构建内部工具。 Retool提供了可连接到任何数据库和API的UI构建块，因此您可以快速构建公司所需的工具。


**🗓即将举办的Postgres活动**
- [Postgres Pulse](https://postgresweekly.com/link/90660/web) - 与诸如Bruce Momjian，Vibhor Kumar和EnterpriseDB的其他人的基于缩放的会话。 现在每隔一周在美国东部时间上午11点运行。 下一个是6月29日（下周一）。
- [Postgres中的表分区](https://postgresweekly.com/link/90661/web) - 加入Amit Langote这个免费的会议，他将分区视为解决某些问题的工具。 6月26/27日（取决于时区）。
