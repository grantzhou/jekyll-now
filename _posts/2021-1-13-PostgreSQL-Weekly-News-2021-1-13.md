---
layout: post
title: PostgreSQL 每周新闻 2021-1-13
---
### PostgreSQL每周新闻#388 - 2021年1月13日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)
备注：[英文原文地址](https://postgresweekly.com/issues/388)
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/x4d9guyjlctepjwgtnre.jpg)

## [Postgres中Hash索引](https://postgresweekly.com/link/101230/web)
这是一个不常见的索引类型，也是不推荐使用的索引，但它的性能有时可以击败可靠的B-tree，正如我们在这里看到的。

`Haki Benita `

## [int4与float4与numeric](https://postgresweekly.com/link/101231/web)
Postgres提供了许多不同的数据类型，本文重点介绍了三种重要的数字存储类型及其差异。

`Hans-Jürgen Schönig `

## [Amazon RDS for PostgreSQL支持12.5、11.10、10.15、9.6.20和9.5.24](https://postgresweekly.com/link/101233/web)
还添加了对pg_cron（用于调度维护命令）和pg_partman（用于管理分区）的支持。

`Amazon Web Services `

## [Postgres 14:添加空闲会话超时](https://postgresweekly.com/link/101236/web)
当他们等待的时间太长时，会话是否终止。

`Hubert depesz Lubaczewski `

## [在Postgres中使用R进行Logistic回归建模](https://postgresweekly.com/link/101237/web)
`Steve Pousty `

## [如何将满足某个条件的行数限制为最多N）](https://postgresweekly.com/link/101238/web)
几个问题之前，我们链接到了一个方便的教程，演示了如何将查询返回的行数限制为每秒一定数量的条件。但是，它有一个与并发性相关的问题，所以Hubert在这里有第二个尝试。

`Hubert depesz Lubaczewski `

## [⏰ 关于时间序列数据你需要知道的12件事](https://postgresweekly.com/link/101240/web)
获取我们的最佳建议和时间序列资源，从postgresqlpro提示和示例项目到数据库基准测试等等。

`Timescale `

## [Sysbench：在内存Postgres，Postgres是无聊的](https://postgresweekly.com/link/101241/web)
有时没有消息就是好消息。“我很高兴地说Postgres很无聊，因为从11版到13版没有CPU退化。”

`Mark Callaghan `

## [在AWS EC2 t4g ARM实例上托管Postgres](https://postgresweekly.com/link/101242/web)
AWS有用于运行Postgres的托管RDS服务，但是如果您想在EC2较新的基于ARM的实例上尝试，这里有一些指导。

`Pedro Alonso `

## [oid与relfilenode的映射](https://postgresweekly.com/link/101243/web)
PostgreSQL如何管理表文件的位置。很少有人需要理解这一点，但也许更多的人愿意去学习。

`Movead Li `

## [pg_back 1.10：用于将数据库转储到文件的Bash脚本](https://postgresweekly.com/link/101244/web)
本质上是一个围绕pg_dumpall和pg_dump的包装器，为简单的数据库备份过程添加更多的结构。

`Nicolas Thauvin `

## [PostgresNIO:Swift的非阻塞、事件驱动客户端](https://postgresweekly.com/link/101246/web)

`Vapor `

## [PGMoon 1.12.0：一个用于OpenResty等的纯luapostgres驱动程序](https://postgresweekly.com/link/101247/web)

`leaf `