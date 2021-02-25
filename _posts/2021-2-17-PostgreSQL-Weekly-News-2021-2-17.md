---
layout: post
title: PostgreSQL 每周新闻 2021-2-17
---
### PostgreSQL每周新闻#393 - 2021年2月17日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)
备注：[英文原文地址](https://postgresweekly.com/issues/393)
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/v1613561722/cn8nnsbneolsbkeekwyf.jpg)
## [Babelfish：显而易见的问题？](https://postgresweekly.com/link/103130/web)
去年，AWS发布了Babelfish，这是一个为PostgreSQL提供与sqlserver兼容的端点的项目，该项目将于今年开源。开源版本是否可以轻松地与Postgres集成？显然不是这样的，这就是这里要研究的问题。

`Álvaro Hernández `

## [PostgreSQL 13.2,12.6,11.11,10.16,9.6.21和9.5.25发布](https://postgresweekly.com/link/103132/web)
一套Postgres更新，以修复两个安全漏洞。 预计这也是有史以来的最终9.5分支版本，因此，如果您现在使用9.5，那么进行升级变得更加重要。


`PostgreSQL Global Development Group `
## [从PostgreSQL获得更多收益的5种方法](https://postgresweekly.com/link/103133/web)
PostgreSQL是当今企业的顶级开源数据库管理系统（DBMS）选择。 该电子书探讨了5种重要策略，以帮助IT经理和DBA更好地管理PostgreSQL部署并最终从Postgres中获得最大收益。。

`EDB `

## [使用SQL实现通用REDUCE聚合函数](https://postgresweekly.com/link/103134/web)
这是一个有趣的SQL探索，可以任意减少数据收集。如果您今天想学习一些关于SQL的知识，这是为您准备的文章。

`Lukas Eder `

## [在Postgres故障后重新连接您的应用程序](https://postgresweekly.com/link/103135/web)
深入客户端HA，以了解发生Postgres故障时会发生什么。

`Dimitri Fontaine `

## [关于ANALYZE和优化器统计](https://postgresweekly.com/link/103136/web)
快速，实际地了解了Postgres如何处理查询，尝试为查询找到最佳执行计划以及可帮助优化程序找到最佳执行计划的统计信息。

`Hans-Jürgen Schönig `

## [postgres配置文件在哪里？](https://postgresweekly.com/link/103137/web)
您可以只询问Postgres自己来告诉您各种配置文件在哪里，而不是在文件系统中四处浏览。


`Hubert depesz Lubaczewski `
## [Postgres 14的几个SQL命令变化](https://postgresweekly.com/link/103138/web)
即使已有同名触发器，CREATE TRIGGER也会获得OR REPLACE选项来创建触发器。 在许多情况下，您也可以在不使用AS的情况下指定列别名。


`Ahsan Hadi `
## [将搜索查询从秒加快到毫秒](https://postgresweekly.com/link/103139/web)
下载我们的免费电子书，了解何时以及如何最佳使用完全匹配，三角形，ILIKE和全文搜索。

`pganalyze `

## [在Postgres中查询JSON数据](https://postgresweekly.com/link/103140/web)
最近，我一直在Postgres中直接查询JSON，这是。。相当愉快！在这篇文章中没有什么让人兴奋的地方，但是如果你还没有深入到JSONB列的世界中，这篇文章涵盖了一些基本知识。


`Aaron Bos `
## [如何在ubuntu 20.04上设置连续归档并执行与Postgres 12的时间点恢复](https://postgresweekly.com/link/103141/web)
DigitalOcean发布的另一个简单的“如标题所说”教程。。


`Nathan McCulloch `
## [pgCenter：Postgres观察和故障排除的命令行工具](https://postgresweekly.com/link/103142/web)
想象一下，类似top命令，但是专门为Postgres服务。您可以随时关注统计数据并实时运行查询。仅限Linux，二进制文件仅限amd64。


`Lesovsky Alexey `
## [PGFormatter 5.0：Postgres SQL 语法美化器](https://postgresweekly.com/link/103144/web)
我们去年链接了这个，但是版本5已经被各种各样的修复和改进删除了。这里有一个在线演示，它可以与SQL一起使用，而不仅限于Postgres的方言。

`Gilles Darold `

## [pg_probackup：postgres的备份和恢复管理器](https://postgresweekly.com/link/103147/web)
用于从Postgres 9.5到13的Postgres集群的备份和恢复（包括增量备份和还原）的工具。刚刚发布了v2.4.10。


`Postgres Professional `
## [PostgreSQL-OCaml 5.0：Postgres的OCaml绑定](https://postgresweekly.com/link/103149/web)
v5在准备或执行查询时增加了对参数类型的支持。 顺便说一句，如果您从未使用过OCaml，它是一种非常简洁的语言。


`Markus Mottl `
## [Adminer：单个PHP文件中的数据库管理](https://postgresweekly.com/link/103151/web)
一个成熟的项目，可以代替phpMyAdmin通过网络界面管理Postgres，MySQL，SQL Server和其他数据库。 主要卖点是将其作为单个PHP文件分布。 v4.8.0刚刚删除。详见Github repo.


`Jakub Vrána `
## [如何在远程服务器上安装PGBadger](https://postgresweekly.com/link/103154/web)
PGBadger是一个postgres日志分析报告工具（即它需要postgres日志并生成HTML报告 - 生成与服务器行为，查询数量，vacuum等信息相关的图表）


`Pablo en Roshka `
# 💡本周提示


**🗓即将举办的Postgres活动**
