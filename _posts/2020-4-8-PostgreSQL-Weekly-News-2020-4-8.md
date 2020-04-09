---
layout: post
title: PostgreSQL 每周新闻 2020-4-8
---
### PostgreSQL每周新闻#350 - 2020年4月8日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)
备注：[英文原文地址](https://postgresweekly.com/issues/350)
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/v1586270433/ijuzjdzhc2pclam1imnp.jpg)

## [PostgreSQL的10个缺陷](https://postgresweekly.com/link/86502/web)
几周前，这里发表了一个博客“Postgres是世界上最好的数据库”，但任何事物都有好与坏！Rick提醒我们，没有一个软件是完美的，即使是Postgres也有缺陷.


`Rick Branson `
## [比较MongoDB和PostgreSQL的join](https://postgresweekly.com/link/86505/web)
通过建立一个经典的员工部门数据模型，分析MongoDB和PostgreSQL

`Michael Stonebraker and Álvaro Hernández `

## [通过配置设置优化Postgres性能](https://postgresweekly.com/link/86507/web)
这篇文章包含了5个值得优化你的Postgres服务器的设置，即：共享缓冲区、wal缓冲区、有效缓存大小、工作内存和维护工作内存。


`Tom Swartz `
## [Postgres 13实现了WAL监控功能](https://postgresweekly.com/link/86508/web)
看一下Postgres的新功能。后端将跟踪与WAL生成相关的信息，pg_stat_statements将能够跟踪WAL的使用情况，并在EXPLAIN命令中提供一个新的WAL选项。


`Julien Rouhaud `
## [pspg 3.0：为Postgres表设计的Unix分页器](https://postgresweekly.com/link/86510/web)
`Pavel Stehule `

## [Postgres 13允许pg_stat_statements统计计划](https://postgresweekly.com/link/86513/web)
pg_stat_statements是一个用于跟踪SQL查询执行统计信息的模块。Postgres13正在为跟踪的内容添加更多统计信息，特别是在计划和执行时间方面。

`Hubert depesz Lubaczewski `

## [Michael Paquier：PostgreSQL的“本周人物”](https://postgresweekly.com/link/86515/web)
这是对Michael Paquier简短采访。他最喜欢的扩展是pg_stat_statements，它已经在本期中出现了：-）


`Andreas Scherbaum `
# 💡本周提示


psql是一个很好的工具，可以与Postgres交互工作，但也可以在命令行的一行程序中使用它来输出查询结果等。它可以被引导以HTML格式输出这些结果，因此快速生成服务器上数据库的HTML报告很简单，如下所示：


```
psql -c "\l+" -H -q postgres > out.html
```


![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/v1586273327/mjlv8purhzsux4dauhfr.png)


当然，您不仅限于将其与\l+一起使用，还可以使用任何命令或查询，并以这种方式以HTML格式输出结果。


**🗓即将举办的Postgres活动**

由于新冠肺炎爆发，我们列出的所有面对面活动现已被取消或推迟。 一些事件正在寻找在线运行的方式，因此我们将在本节中专门讨论在线事件，直播等。

如果您有这样的活动，请给我们留言，我们可以在这里推广。 举例来说，即使您正在Twitch或YouTube Live上进行一次预定的演讲，我们也可以列出它。