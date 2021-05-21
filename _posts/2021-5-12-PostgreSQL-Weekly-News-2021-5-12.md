---
layout: post
title: PostgreSQL 每周新闻 2021-5-12
---
### PostgreSQL每周新闻#405 - 2021年5月12日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)
备注：[英文原文地址](https://postgresweekly.com/issues/405)
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/hds0bl8ps9g3u4irrgpr.jpg)
## [跳过扫描：一种使不重复查询加快8000倍的方法](https://postgresweekly.com/link/107769/web)
首先，值得注意的是，这是一个TimescaleDB的特性，但考虑到Timescale是Postgres的扩展，它仍然是一个有趣的开发。“跳过扫描”是一项新功能，它解决了Postgres无法有效地从有序索引中提取唯一值列表的问题。马上到来的postgres15中也有一个类似的功能，但是TimescaleDB用户现在就可以使用它了，下面是它的工作原理。即使您没有使用TimescaleDB的计划，理解其基本概念也是值得的。


`Sven Klemm and Ryan Booz (Timescale) `
## [使用Postgres作为数据仓库](https://postgresweekly.com/link/107770/web)
Postgres通常不是创建数据仓库的第一个选择，但是如果您不想将数据移动到像Snowflake或BigQuery这样的东西中的话，通过一些调整配置，它也可以在一定的规模下很好地工作。


`Cedric Dussud `
## [避免整数溢出和零停机时间](https://postgresweekly.com/link/107771/web)
了解Buildkite是如何跨三个分区（覆盖8.5TB）在我们最大的表之一中迁移超过20亿行的，以及更多具有相同数据类型外键的行。来阅读我们一位工程师的博客。


`Buildkite `
## [创建只读Postgres用户](https://postgresweekly.com/link/107774/web)
了解如何在当前版本以及即将到来的Postgres14中创建典型的只读用户。


`Jonathan S. Katz `
## [快速获取随机行(快很多)](https://postgresweekly.com/link/107775/web)
感觉从表中随机抓取一行的话题这些年来出现了很多，因为有很多方法可以做到，都有各自的优缺点。要介绍的这种方法使用TABLESAMPLE来让它变快。


`Magnus Hagander `
## [关于Postgres表的聚类](https://postgresweekly.com/link/107776/web)
Bruce的开场白说到：“写了600多篇博客，我本以为我已经讨论了CLUSTER命令的复杂性，但似乎我还没有，所以现在就开始吧。”😄


`Bruce Momjian `
## [📺 5月19日Livestream:ALTER DATABASE<db>SURVIVE REGION FAILURE](https://postgresweekly.com/link/107778/web)
一位分布式系统工程师解释了多区域应用程序体系结构&看看它如何不像您想象的那么复杂。


`Cockroach Labs `
## [使用Postgres的ETL模式](https://postgresweekly.com/link/107779/web)
▶    它可以追溯到2018年，但是这个关于用Postgres做ETL和数据仓库工作的演讲得到了强烈的推荐。很实用，很好的幻灯片，很明显这个演讲中提炼了很多经验。


`Dr. Martin Loetzsch `
## [windyquery：一个非阻塞的Python Postgres查询生成器](https://postgresweekly.com/link/107782/web)
一个使用异步io的非阻塞PostgreSQL查询生成器。


`windymile `
## [PGSync 2.0：一个Postgres到Elasticsearch的同步工具](https://postgresweekly.com/link/107783/web)
用于将Postgres同步到Elasticsearch的中间件，以便您可以在Elasticsearch中公开非规范化文档以进行查询。


`Tolu Aina `
# 💡本周提示


**🗓即将举办的Postgres活动**
