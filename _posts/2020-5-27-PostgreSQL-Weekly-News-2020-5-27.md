---
layout: post
title: PostgreSQL 每周新闻 2020-5-27
---
### PostgreSQL每周新闻#357 - 2020年5月27日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)
备注：[英文原文地址](https://postgresweekly.com/issues/357)
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/v1590578119/r9cos6ub8ngudxno6wuy.jpg)
# 💡顺便说一句，如果您想关注一些Postgres现场对话，请务必检查PGCon，因为在我们发行这一版时，它正在进行中。


## [EXPLAIN ANALYZE可能是在骗你](https://postgresweekly.com/link/88968/web)
Postgres上的文章通常不是一开始就依赖海森堡的不确定性原理，但Álvaro着眼于分析查询可能会扭曲幕后实际情况。


`Álvaro Hernández `
## [PostgreSQL的13 Beta 1已经发布](https://postgresweekly.com/link/88969/web)
可以使用发行说明草案（我们也在上周链接了这些发行说明），但是最大的改进是分区，B树索引，增量排序，并行VACUUMing，客户端连接安全性和Windows可操作性。


`PostgreSQL Global Development Group `
## [宣布CockroachDB 20.1：构建快速，并持久构建](https://postgresweekly.com/link/88971/web)
满足具有弹性，可扩展的SQL数据库，现在具有改进的PostgreSQL兼容性。为您的所有应用程序带来轻松的可伸缩性和防弹能力。


`Cockroach Labs `
## [PGCon 2020会议正在直播](https://postgresweekly.com/link/88972/web)
与许多活动一样，Postgres的年度PGCon也是虚拟的，并且现在将参加5月26日至29日的三个流媒体室，Zoom和IRC聊天。如果您有时间，请安排完整的时间表-我们将在发送此问题后不久开始主要对话:-)


`PGCon `
## [您是否真的需要分区管理工具？](https://postgresweekly.com/link/88974/web)
表分区是一种将表划分为更易于管理的部分的方法，还可以加快查询速度。 Postgres自版本10以来就提供了该功能，但是围绕它的工具不多。那么我们需要吗？


`Kaarel Moppel `
## [隐藏/隐式表列](https://postgresweekly.com/link/88975/web)
您是否知道每个表的幕后都有几个隐藏列，包括tableoid，cmax和ctid？这篇文章探讨了它们的内容代表什么。


`muhammad usama `
## [用于优化Django和Python性能的Postgres技巧](https://postgresweekly.com/link/88976/web)
基于Louise为PyCon 2020所做的（而更为详细的）演讲的广泛总结。


`Louise Grandjonc `
## [Postgres的13再添FETCH先用TIES](https://postgresweekly.com/link/88978/web)


`Denis Gobo `
## [检查事件触发器中的命令标记和事件](https://postgresweekly.com/link/88979/web)
如果您没有看到它，我们在第352期采访了Luca。


`Luca Ferrari `
## [了解要在数据库日志中监视的前6个事件](https://postgresweekly.com/link/88981/web)
在这本电子书中，我们将引导您完成最重要的Postgres日志事件，以监视查询性能并防止停机。


`pganalyze `
## [开发人员在Azure上使用Postgres和MySQL做什么？](https://postgresweekly.com/link/88982/web)
上周的虚拟Microsoft Build会议进行了30分钟的讨论。很高的水平。


`Andrea Lam and Samay Sharma `
## [Zapatos：用于TypeScript的零抽象Postgres](https://postgresweekly.com/link/88983/web)
为Postgres表构建TypeScript架构，为进出Postgres的事物获取正确的类型，等等。顺便说一句，做这些详尽的文档确实花费不少时间。


`George MacKerron `
## [pgagroal 0.7.0：高性能Postgres连接池](https://postgresweekly.com/link/88984/web)
0.7带来Prometheus支持，远程管理以及在选定的秒数后断开空闲客户端的功能。


`Red Hat Inc. `
# 💡本周提示


**🗓即将举办的Postgres活动**
- [Postgres Pulse](https://postgresweekly.com/link/88985/web) - 每周的东部时间上午11点。每周进行一次基于Zoom的会议，与诸如Bruce Momjian，Vibhor Kumar和EnterpriseDB的其他人进行。
- [Postgres Vision 2020](https://postgresweekly.com/link/88986/web) - 
6月23日至24日。多天多次尝试在线进行一次在线Postgres会议。
