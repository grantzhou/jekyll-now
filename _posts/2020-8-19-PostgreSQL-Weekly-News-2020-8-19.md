---
layout: post
title: PostgreSQL 每周新闻 2020-8-19
---
### PostgreSQL每周新闻#369 - 2020年8月19日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)
备注：[英文原文地址](https://postgresweekly.com/issues/369)
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/frkwxajs9vvoj2iol3af.jpg)
## [Postgraphile：快速获取适用于Postgres数据库的GraphQL API](https://postgresweekly.com/link/93611/web)
正在开发此流行的Node.js工具的v5，但与此同时，我们获得了4.8版本，该版本支持“枚举表”和所有Postgres的内置几何类型。如果您想通过基于GraphQL的API提供Postgres数据库，则值得一试。


`Graphile `
## [已发布Postgres 12.4、11.9、10.14、9.6.19、9.5.23和13 Beta 3](https://postgresweekly.com/link/93612/web)
一系列Postgres版本修复了多个错误，但更重要的是，修复了两个安全漏洞（仅在9.5-12版中）。我们还提醒您，Postgres 9.5将在2021年2月之后停止接收修复程序。


`PostgreSQL Global Development Group `
## [实时Postgres性能监控](https://postgresweekly.com/link/93613/web)
收集现成的和自定义的PostgreSQL指标，并将它们与来自分布式基础架构，应用程序和日志的数据相关联。使用Datadog获得实时性能见解并设置智能警报。开始免费试用。


`Datadog `
## [使用Python和Pandas在Postgres内部构建推荐引擎](https://postgresweekly.com/link/93614/web)
了解如何直接在Postgres内部利用Python和Pandas构建自己的推荐引擎。


`Craig Kerstiens `
## [递归查询简介](https://postgresweekly.com/link/93615/web)
递归查询（使用WITH构建）使您可以使用SQL进行有趣的事情，并且不太难理解，尤其是此处提供的简单实用示例。


`Laurenz Albe `
## [SQLite 3.33.0发布（具有受Postgres启发的功能）](https://postgresweekly.com/link/93669/web)
我们在本新闻通讯中并不经常介绍SQLite，但是当世界上使用最频繁的数据库引擎获得UPDATE FROM的支持并旨在与Postgres的实现兼容时，为什么不这样做呢？ ？ 😄


`SQLite Team `
## [Timescale Cloud跨3个云扩展到76个区域](https://postgresweekly.com/link/93616/web)
TimescaleDB本质上扩展了Postgres，具有重要的时序数据功能，而Timescale Cloud是创建者的商业化“ TimescaleDB in cloud”服务。


`Timescale `
## [Envoy 1.15引入了具有监控支持的新Postgres扩展](https://postgresweekly.com/link/93617/web)
Envoy是云应用程序的流行服务代理，它现在可以“说出Postgres”有线协议！这篇文章深入探讨了此插件的开发原因，当前实现的功能以及未来版本的发展路线。


`CNCF `
## [使用systemd运行多个PgBouncer实例](https://postgresweekly.com/link/93619/web)
PgBouncer是一个连接池，可以作为单个进程运行，但是只需做一些工作，您就可以为不同的虚拟主机运行多个实例。


`Peter Eisentraut `
## [看一下键集分页](https://postgresweekly.com/link/93621/web)
上周，Bruce介绍了分页方法，现在主要关注一种技术，即在WHERE中使用LIMIT和OFFSET。他还研究了在插入或删除项目时它在实际中的工作方式。


`Bruce Momjian `
## [CockroachDB：可扩展的分布式PostgreSQL](https://postgresweekly.com/link/93624/web)
不再分片Postgres实例。认识CockroachDB，这是一种分布式SQL数据库，具有自然弹性，并具有开箱即用的可扩展性。


`Cockroach Labs `
## [具有横向联接的Postgres中的迭代器](https://postgresweekly.com/link/93625/web)
“将关键字LATERAL添加到联接中后，输出现在将把联接的右手部分应用于联接左部分中的每个记录。”


`Steve Pousty `
## [我们如何使用Postgres扩展统计信息实现3000倍的速度提升](https://postgresweekly.com/link/93626/web)
像这样的大数字总是让我戴上愤世嫉俗的眼镜，但在这种情况下，这是鼓励Postgres做正确的事情的精湛技术故事


`Jared Rulison `
## [已发布PostGIS 3.0.2、2.5.5和2.4.9](https://postgresweekly.com/link/93627/web)
较小的错误修复和性能增强版本，用于流行的地理空间扩展。


`PostGIS Developers `
# 💡本周提示


**🗓即将举办的Postgres活动**
