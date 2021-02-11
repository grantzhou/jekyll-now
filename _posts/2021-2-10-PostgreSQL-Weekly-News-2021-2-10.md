---
layout: post
title: PostgreSQL 每周新闻 2021-2-10
---
### PostgreSQL每周新闻#392 - 2021年2月10日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)
备注：[英文原文地址](https://postgresweekly.com/issues/392)
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/xdb0tkslgc8tugwjzobd.jpg)
## [深入的Postgres思想：Linux刺客](https://postgresweekly.com/link/102697/web)
一个相当令人联想起的标题，用于描述Linux的OOM（内存不足）管理器，该管理器将终止进程以释放内存。您可以采取什么方法来保护Postgres免受这种“刺客”的侵害，当Kubernetes出现时您可以采取哪些特殊措施？


`Joe Conway `
## [清理您的Postgres数据库](https://postgresweekly.com/link/102698/web)
正如我们在上周的专题文章中了解到的那样，清理未使用的索引有很多好处。这是一篇更快的文章，其中包含有关保持数据库清洁和查找潜在目标的提示。


`Craig Kerstiens `
## [Timescale Analytics项目：PostgreSQL的时间序列分析](https://postgresweekly.com/link/102700/web)
Timescale Analytics旨在将SQL执行时间序列分析所需的所有功能组合到一个PG扩展中-我们需要（并且需要）您的帮助。查看当前的提案，捐款方式以及如何加入我们和制定项目💪


`Timescale `
## [什么是'检查站'？](https://postgresweekly.com/link/102701/web)
关于Postgres如何通过使用预写日志（WAL）来防止数据库损坏或数据丢失以及与之相关的检查点的快速教程。值得快速阅读以了解您的术语。


`Hans-Jürgen Schönig `
## [TOAST数据损坏或“错误：意外的块号” ](https://postgresweekly.com/link/102702/web)
TOAST是一种将“超大”数据单独存储在表旁边而不是直接存储在行内的机制。但是，如果表与外部数据之间的连接断开，则可能会发生损坏。


`Luca Ferrari `
## [为什么有一个名为“postgres”的数据库？](https://postgresweekly.com/link/102703/web)
这不是有关Postgres存在的问题，而是有关postgres许多新安装的命名数据库的问题。


`Hubert depesz Lubaczewski `
## [如何取消分发Postgres表的分发](https://postgresweekly.com/link/102704/web)
如果您使用Citus扩展名分发Postgres数据库，如果由于某种原因需要返回到未分发的系统会怎样？Citus 9.5使其成为可能。


`Halil Ozan Akgül `
## [对由于磁盘和RAM而引起的性能问题进行故障排除](https://postgresweekly.com/link/102706/web)
快速查看评估磁盘空间和内存使用情况的方法，这两个方面的管理不当会迅速导致性能问题。


`Hamid Akhtar `
## [立即使用CYPEX来构建内部PostgreSQL应用程序](https://postgresweekly.com/link/102707/web)
只需很少的编码即可获得较大的结果：CYPEX使您可以轻松地将PostgreSQL表变成完全成熟的应用程序。


`CYBERTEC `
## [“池”在Pgpool-II中是什么意思？](https://postgresweekly.com/link/102708/web)
PgPool-II是流行的Postgres连接池和负载平衡器，尽管它现在肯定不仅仅只是一个池器，而且Tatsuo希望您现在从更广泛的角度来考虑它。


`Tatsuo Ishii `
## [通过Java 16 Unix域套接字通道与Postgres交谈](https://postgresweekly.com/link/102710/web)
l,null,"en


`Gunnar Morling `
## [如何在Ubuntu 18.04上设置Postgres 13 WAL流复制](https://postgresweekly.com/link/102711/web)
l,null,"en


`David Zhang `
## [TimescaleDB 2.0现在普遍可用](https://postgresweekly.com/link/102712/web)
Timescale的人员去年年底透露了TimescaleDB 2.0，但现在是GA。如果您希望将开放源代码，高度可扩展的时间序列数据库放在Postgres之上，则值得一看。


`Erik Nordström (Timescale) `
## [lib_mustache：PL / pgSQL中的基本Mustache模板引擎](https://postgresweekly.com/link/102714/web)
Mustache是一种流行的模板系统，如果需要，您可以依靠Postgres进行渲染。


`Netwo `
## [pg-boss 5.1.0：用于Node.js的Postgres支持的作业队列系统](https://postgresweekly.com/link/102716/web)
用于后台处理和可靠的异步执行的作业队列。它使用Postgres特定的功能来保证安全。


`Tim Jones `
# 💡本周提示


**🗓即将举办的Postgres活动**
