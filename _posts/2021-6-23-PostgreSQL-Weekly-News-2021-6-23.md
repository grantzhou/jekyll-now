---
layout: post
title: PostgreSQL 每周新闻 2021-6-23
---
### PostgreSQL每周新闻#411 - 2021年6月23日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)
备注：[英文原文地址](https://postgresweekly.com/issues/411)
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/lkidgg7yr6w7lujy2qb3.jpg)

## [postgres14中更好的范围类型：将100行SQL变成3行](https://postgresweekly.com/link/110139/web)
我总是少用几行代码，而不是多用几行代码，所以单凭标题我就赢了。即将发布的postgres14增加了对多范围类型的支持，这为一些纯SQL解决方案提供了额外的能力。。我在这里提供了一个例子。

`Jonathan S. Katz `

## [如何（以及为什么）成为一名Postgres贡献者](https://postgresweekly.com/link/110140/web)
一个“建议的集合”，帮助那些渴望从没有过贡献到贡献一点点的人。关键是要了解开发过程，在本地机器上为Postgres设置一个开发环境，并完成一些非常重要的比较小的工作。


`Aleksander Alekseev `
## [在Postgres之上（更快地）构建内部应用程序](https://postgresweekly.com/link/110141/web)
构建内部应用程序，而不需要那些无聊的东西（与UI库纠缠或将数据源和API拼凑在一起）。

`Retool `

## [一种新的数据库：Postgres与Citus表的结合](https://postgresweekly.com/link/110146/web)
Citus通常用于使Postgres更具分布性和可伸缩性，但您仍然可以享受Postgres的所有常见功能，甚至可以将它们混合在一起。本文深入研究了citus10对本地Postgres表和Citus引用表之间的外键的支持。

`Onur Tirtir (Citus Data) `

## [从MD5到SCRAM-SHA-256](https://postgresweekly.com/link/110147/web)
postgres10及更高版本支持scram-sha-256密码散列和身份验证机制，尽管您可能仍然使用MD5。这篇文章讲到了切换的好处和方法。

`Laurenz Albe `

## [浅谈CMU的Postgres优化器](https://postgresweekly.com/link/110148/web)
上周我们特别报道了Robert Haas最近关于Postgres的查询优化器的演讲，但是如果你没时间看的话，他会在演讲的特定部分写一些笔记。

`Robert Haas `

## [▶️ 创建示例Postgres数据：您有什么选择？](https://postgresweekly.com/link/110150/web)
观看这个简短的操作视频系列，了解为基准测试、演示和其他方面生成真实示例数据的4种方法 🚀


`Timescale `
## [Postgres中使用视图的零停机“模式迁移”](https://postgresweekly.com/link/110151/web)
这不完全是一种典型的迁移，但是。。我想这是一个有趣的思路。


`Fabian Lindfors `
## [Postgres中日志的技巧，以你的慢查询为为例](https://postgresweekly.com/link/110152/web)
查看一个有用的与日志相关的设置（log_min_duration_statement），以帮助识别性能问题。很多帖子都是关于Crunchy和LogDNA的，所以你可能更喜欢日志配置文件。


`Kat Batuigas `
## [pg_notify_exporter：Prometheus的监听/通知Exporter](https://postgresweekly.com/link/110154/web)
使用LISTEN/NOTIFY将表操作（INSERT、UPDATE和DELETE）中触发的事件导出到Prometheus。


`hmolinab `
# 💡本周提示


**🗓即将举办的Postgres活动**
