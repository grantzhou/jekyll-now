---
layout: post
title: PostgreSQL 每周新闻 2020-1-8
---
### PostgreSQL每周新闻#337 - 2020年1月8日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)
备注：[英文原文地址](https://postgresweekly.com/issues/337)
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/v1578484754/wbkj4yuuybusrpsuvaul.png)

## [2019巴黎pgDay的8个讨论](https://postgresweekly.com/link/81944/web)
巴黎pgDay是去年3月在法国最大城市举行的一天的毕业会后会议

`YouTube `

## [使用Postgres HyperLogLog扩展](https://postgresweekly.com/link/81951/web)
HyperLogLog是一种有效地统计预测方法，CITUS发布了HyperLogLog的PASGREST扩展。


`Wisdom Devs `
## [介绍自动化Postgres解释关于pganalyze的计划见解](https://postgresweekly.com/link/81954/web)
pganalyze现在可以自动收集解释计划，并提供最昂贵计划节点的可视化表示，以及对Postgres数据库的更有用的见解。在这篇博客文章中了解有关所有新解释计划功能的更多信息。

`pganalyze `

## [表锁定更新查询的奇怪情况](https://postgresweekly.com/link/81955/web)
“您的数据库有锁（认为是互斥锁，但其作用域不同），如果这些锁所做的事情与您预期的不同，它们可能会扰乱您的一天。”


`Richard Schneeman `
## [亚马逊RDS用户？轮换证书的时间到了](https://postgresweekly.com/link/81956/web)
每五年，AWS RDS、Aurora和DocumentDB使用的证书都会过期并替换为新的证书，因此，如果您使用SSL/TLS连接或证书验证，您可能需要在2020年3月5日之前完成一些工作。


`Jeff Barr (AWS) `
## [2019年最热门的Postgres链接](https://postgresweekly.com/link/81957/web)
《Postgres周刊》的读者点击了过去12个月的Postgres亮点。

`Za'e Johnson `

## [为什么您可能需要增加每个事务的最大锁数](https://postgresweekly.com/link/81958/web)
如果您曾经看到过“共享内存不足”错误，这是一个您可能需要考虑调整的参数。

`Hans-Jürgen Schönig `

## [一个开发人员的Web服务“转到”Postgres配置](https://postgresweekly.com/link/81959/web)
这基本上是一个开发人员草草记下了他所有的笔记，以便设置Postgres，但是。。我喜欢这样的帖子，因为通常会有一两条建议可供参考


`Peter Bui `
## [如何有效地转储Postgres数据库](https://postgresweekly.com/link/81960/web)
关于pg_dumpall和pg_dump的一些有用的注释和脚本。


`Hubert depesz Lubaczewski `
## [设置Postgres的配置参数](https://postgresweekly.com/link/81961/web)
调整postgresql.conf中的内容是一回事，但还有其他相关的选项，包括更改用户或会话级别的某些设置。

`Hans-Jürgen Schönig `

## [recovery.conf在Postgres 12中消失](https://postgresweekly.com/link/81962/web)
在Postgres 12中，recovery.conf的设置已经被“吸收”到postgresql.conf中了——这里有更多关于更改和如何自己处理的信息。


`Laurenz Albe `
## [自动化Postgres和TimescaleDB架构设计](https://postgresweekly.com/link/81963/web)
PGSchema是由Timescale团队构建的一个易于使用的工具，它可以通过3个简单的步骤生成SQL模式：上传、格式化、复制。

`Timescale `

## [与EC2相比，RDS的价格溢价可能超出您的预期](https://postgresweekly.com/link/81965/web)
RDS是Amazon的关系数据库服务，它可以在AWS上提供完全托管的Postgres（或MySQL、Oracle等）服务。然而，RDS比EC2的价格溢价越来越高，这让开发人员感到惊讶。


`Rick Branson `
## [消息数据库：Postgres的事件存储和消息存储](https://postgresweekly.com/link/81966/web)
针对pub/sub、事件源和事件微服务用例，消息数据库可以帮助您利用事件架构的优点，但不必一直使用Apache Kafka之类的东西。


`Eventide Project `
## [Postgres.js：Node.js的快速、功能齐全的Postgres客户端](https://postgresweekly.com/link/81967/web)
号称是最快的甚至（比流行的pg模块快2-10倍），但我们会让你来判断这一点：-）


`Rasmus Porsager `
# 💡本周提示


如果你是大多数还没有参加过Postgres活动的Postgres用户，那么在新的一年里将会有很多这样的活动：


**🗓即将举办的Postgres活动**
- [PgDay SF](https://postgresweekly.com/link/81968/web)（1月21日在旧金山）
- [PgDay FOSDEM](https://postgresweekly.com/link/81969/web)（1月31日，比利时布鲁塞尔）
- [PgConf.Russia](https://postgresweekly.com/link/81970/web)（2月3日至5日，俄罗斯莫斯科）。
- [PgConf India](https://postgresweekly.com/link/81971/web)（2月26日至28日，印度班加罗鲁）
- [Nordic PgDay 2020](https://postgresweekly.com/link/81972/web)（3月24日芬兰赫尔辛基）
- [pgDay Paris 2020](https://postgresweekly.com/link/81973/web)（3月26日，法国巴黎）。
- [Swiss PGDay 2020](https://postgresweekly.com/link/81974/web)（6月18日至19日，瑞士）
