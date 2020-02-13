---
layout: post
title: PostgreSQL 每周新闻 2020-2-12
---
### PostgreSQL每周新闻#342 - 2020年2月12日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)
备注：[英文原文地址](https://postgresweekly.com/issues/342)
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/vkvxgzqqrby3afyuozve.jpg)

## [psql+gnuplot通过你的数据绘制的命令行图形](https://postgresweekly.com/link/83733/web)
gnuplot是一个命令行绘图程序，您可以将psql输出直接输入其中，以创建整洁的基于命令行的绘图。这里没什么可看的，但这项技术可能对你有用或启发其他想法。

`Pavel Stěhule `

## [Postgres 13中的psql支持显示事务状态](https://postgresweekly.com/link/83735/web)
Postgres 13版本psql中的提示将显示当前连接是否在事务块中。

`Michael Paquier `



## [在Postgres中配置work_mem](https://postgresweekly.com/link/83739/web)
work_mem是在使用临时磁盘文件之前用于内部排序操作和哈希表的内存量，默认设置为4MB。

`David Conlin `

## [Aurora PostgreSQL现在支持机器学习并导出到Amazon S3](https://postgresweekly.com/link/83737/web)
本周AWS发布了一些关于Aurora（与Postgres兼容的RDBMS）和RDS（AWS基础设施上的实际Postgres）的新闻。Aurora PostgreSQL现在可以与AWS的SageMaker机器学习服务集成，您可以直接将数据导出到S3中，并且改进了Postgres 11.6的兼容性。


`Amazon Web Services `
## [Amazon RDS for PostgreSQL支持新版本和实例大小](https://postgresweekly.com/link/83740/web)
更多的AWS新闻，这次是RDS。除了支持Postgres 11.6、10.11、9.6.16和9.5.20之外，如果Postgres实例上确实需要512GB或RAM，现在还可以在更多实例类型（db.m5和db.r5 8xlarge和16xlarge大小）上使用RD:-）


`Amazon Web Services `
## [为什么删除列不会回收磁盘空间？](https://postgresweekly.com/link/83742/web)
简而言之，因为这通常是不必要的。一个列对于SQL操作来说只是“不可见”的，随着时间的推移，空间将被回收。


`Luca Ferrari `
## [如何从基于触发器的分区迁移到本机分区](https://postgresweekly.com/link/83743/web)


`Keith Fiske `
## [Aurora PostgreSQL集群缓存管理简介](https://postgresweekly.com/link/83744/web)
群集缓存管理是AWS的Aurora Postgres变体上的一项功能，它有助于减少故障转移后丢失/冷缓存的负面性能影响。


`Sameer Malik and Andrei Ilyashenko `
## [从SQL Server迁移到Postgres时处理大小写](https://postgresweekly.com/link/83745/web)
SQL Server和Postgres在命名事物时使用大写字母的方法有很大不同。


`Hans-Jürgen Schönig `
## [使用Postgres快捷键节省时间](https://postgresweekly.com/link/83748/web)
Postgres快捷键

`Timescale `

## [如何使用JPA和Hibernate将Postgres数组映射到Java列表](https://postgresweekly.com/link/83747/web)

`Vlad Mihalcea `

## [es2postgres：对Postgres加载程序的弹性搜索](https://postgresweekly.com/link/83750/web)
使用es2csv、xsv、sed和psql定期将数据从Elasticsearch移动到Postgres。


`Tibor Kiss `
## [Hasql：haskell的灵活易用的PostgreSQL驱动](https://postgresweekly.com/link/83751/web)
拥有一个“灵活映射API”，用于将表数据映射到语言中的值。

`Nikita Volkov `

# 💡本周提示


**🗓即将举办的Postgres活动**
- [PgConf India](https://postgresweekly.com/link/83753/web)（2月26日至28日，印度班加罗鲁）
- [Postgres Conference 2020](https://postgresweekly.com/link/83754/web)（3月23日至27日，美国纽约）
- [Nordic PgDay 2020](https://postgresweekly.com/link/83755/web)（3月24日芬兰赫尔辛基）
- [pgDay Paris 2020](https://postgresweekly.com/link/83756/web)（3月26日，法国巴黎）
- [Swiss PGDay 2020](https://postgresweekly.com/link/83758/web)（6月18日至19日，瑞士）
