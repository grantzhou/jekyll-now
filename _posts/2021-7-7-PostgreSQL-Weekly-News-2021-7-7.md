---
layout: post
title: PostgreSQL 每周新闻 2021-7-7
---
### PostgreSQL每周新闻#413 - 2021年7月7日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)
备注：[英文原文地址](https://postgresweekly.com/issues/413)
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/fsov0xxtno1flu4npziy.jpg)
## [使用 dblink 和复制延迟模拟临时表](https://postgresweekly.com/link/110711/web)
使用延迟流复制和dblink（一种通过另一个 SQL 查询在远程数据库上执行查询的方法）来模拟临时表（即回顾时间）的奇怪观察。这是一个如此奇怪但聪明的方法。


`Kaarel Moppel `
## [看一下行级锁](https://postgresweekly.com/link/110713/web)
关于如何在 Postgres 中管理行级锁以及如何与对象级锁一起使用的实用演示。


`Egor Rogov `
## [🌟时间序列 101：获取 10 多个教程、示例数据集及更多](https://postgresweekly.com/link/110714/web)
探索 10 多个教程- 包含示例数据集和 SQL 查询 - 开始并运行时间序列数据分析。主题范围从分析加密趋势到 DevOps 和物联网监控，构建出色的可视化等。🚀


`Timescale `
## [了理解pg_repack：可以出现什么问题以及如何避免它](https://postgresweekly.com/link/110716/web)
pg_repack是从表和索引中删除膨胀，以及可选恢复聚簇索引的物理顺序的工具，不超过持有的排他锁说表，但它不是没有它的痛点。


`Jobin Augustine `
## [Ora2PG 现在支持oracle_fdw提高数据迁移速度](https://postgresweekly.com/link/110718/web)
Ora2Pg是一个开源的 Oracle 到 Postgres 迁移工具，它现在可以使用oracle_fdw来提高性能，特别是在使用 BLOB 列的表上。这是因为新版本v22.0 和 22.1刚刚发布（除了上面有更多功能）。


`Gilles Darold `
## [Postgres 权限和物化视图](https://postgresweekly.com/link/110725/web)
物化视图让你可以保留查询的结果，但让非所有者适当地刷新它们可能需要对权限进行一些工作。


`Ryan Lambert `
## [带有授权的 Postgres 上的即时实时 API | 30 年代免费开始](https://postgresweekly.com/link/110726/web)
l,null,"en


`Hasura `
## [开始使用用于 PostgreSQL 的 Azure 数据库的新方法](https://postgresweekly.com/link/110727/web)
在 20 分钟内快速介绍在 Azure 上运行 Postgres，特别是在其 Citus 风味的“超大规模”形式中。顺便说一下，Claire 是 Postgres Weekly 链接最多产的供应商之一，所以很高兴看到她在现场谈论 Postgres。


`Scott Hanselman and Claire Giordano `
## [如何本地和分布式的Postgres表工作与Citus之间的联接](https://postgresweekly.com/link/110728/web)
CITUS能够分布在多个节点表中的一个集群，甚至他们之间的连接。这篇文章是对其工作原理的基本介绍。


`Sait Talha Nisanci `
## [Postgres 上的偏执 SQL 执行](https://postgresweekly.com/link/110730/web)
Jeremy想到了一些想法，通过使用超时、完全限定事物的名称、使用热备用等，以“偏执”安全级别执行 SQL。


`Jeremy Schneider `
# 💡本周提示


**🗓即将举办的Postgres活动**
