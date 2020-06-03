---
layout: post
title: PostgreSQL 每周新闻 2020-6-3
---
### PostgreSQL每周新闻#358 - 2020年6月3日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)
备注：[英文原文地址](https://postgresweekly.com/issues/358)
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/zpny9hxugkgvphan1tns.jpg)
## [用递归SQL和SVG绘制Sierpiński三角形](https://postgresweekly.com/link/89426/web)
注意，这篇文非常有意思：“在本文中，我将展示一个非常简单的递归CTE1，该CTE1实现了迭代函数系统来生成Sierpiński三角形” ，简单地说 这纯粹是为了乐趣。


`Noah Doersing `
## [死锁，页面锁，咨询锁和谓词锁](https://postgresweekly.com/link/89427/web)
欢迎使用Egor Rogov的一个惊人的Postgres深入探究。 来这里有很多东西要学习


`Егор Рогов `
## [Postgres Vision 2020-免费在线会议（6月23日至24日）](https://postgresweekly.com/link/89428/web)
该会议将讲述客户如何利用Postgres降低成本并提高创新的真实故事。 以及PostgreSQL专家用于部署模型的工具和技术。


`EnterpriseDB `
## [TimescaleDB，一个基于Postgres的大规模时间序列数据库，现已免费](https://postgresweekly.com/link/89429/web)
Timescale在PostgreSQL上免费提供其多节点时间序列数据库（“有源代码”）。 这篇文章深入探讨了它的原理。


`Timescale `
## [加快对分层数据的递归查询](https://postgresweekly.com/link/89430/web)
分层查询是一种SQL查询，用于处理诸如树的分层模型数据。 Postgres的标准ltree模块可用于加快一些常见的用例。


`Hans-Jürgen Schönig `
## [消除由高流量引起的Postgres运行瓶颈](https://postgresweekly.com/link/89431/web)
这篇文涵盖了多种方法来管理连接，包含调整配置参数，autovacuuming的配置，还有服务器硬件的调优。


`Robert Bernier `
## [Postgres中时间和相关数据类型的复杂性](https://postgresweekly.com/link/89432/web)
作为Cockroach实验室的一部分，我们致力于使CockroachDB与Postgres更加兼容（目标是直接替代），我们花了很多时间研究时间相关的数据上。 并在此过程中学到了很多东西。


`Oliver Tan `
## [可视化排序规则](https://postgresweekly.com/link/89433/web)
排序规则定义了如何对值（几乎总是字符串）进行排序，并且在对字符串进行排序时，不同的排序规则可以有相当不同的结果。 这里有两个查询证明了这一概念。


`Bruce Momjian `
## [了解PostgreSQL中的时间数据类型](https://postgresweekly.com/link/89434/web)
我们在优化CockroachDB 的 Postgresql兼容性的同时，我们了解了很多关于PostgreSQL时间的复杂性。


`Cockroach Labs `
## [使用来自Deno的Postgres的示例](https://postgresweekly.com/link/89435/web)
▶仅4分钟即可轻松完成。


`Adrian Twarog `
## [使用Postgres的复合数据类型](https://postgresweekly.com/link/89436/web)
复合类型是由其他现有数据类型（例如C中的结构）形成的数据类型。

`Craig Kerstiens `
## [使用PostGIS定义空间约束](https://postgresweekly.com/link/89437/web)
约束用于确保数据库中的数据能够反映数据模型的假设，并且对于空间数据也可以像使用PostGIS一样可靠。


`Paul Ramsey `
## [不要让我感觉无助：另一种需要监视的事务](https://postgresweekly.com/link/89438/web)
准备好的事务（prepared transaction）使两阶段提交成为可能，但是在持有锁方面有一些危险，在不需要它们的情况下都不建议使用。


`Richard Yen `
## [PostGIS 2.3.11的发布](https://postgresweekly.com/link/89439/web)
最终错误修复的2.3版本发布-强烈建议升级到2.4或更高版本（3.0是最新版本，但至少需要Postgres 9.5）。


`PostGIS Developers `
# 💡本周提示


**🗓即将举办的Postgres活动**
- [Postgres Pulse](https://postgresweekly.com/link/89441/web) - 每周星期一美东时间上午11点。 每周进行一次基于Zoom的会议，与Bruce Momjian，Vibhor Kumar和EnterpriseDB的其他人进行会议。
- [Postgres Vision 2020](https://postgresweekly.com/link/89442/web) - 6月23日至24日的Postgres Vision 2020。 多天多次的进行在线Postgres会议。
