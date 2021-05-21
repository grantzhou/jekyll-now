---
layout: post
title: PostgreSQL 每周新闻 2021-4-21
---
### PostgreSQL每周新闻#402 - 2021年4月21日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)
备注：[英文原文地址](https://postgresweekly.com/issues/402)
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/ja18sroyeztdigdyrost.jpg)
## [postgres“磁盘不足”，如何恢复：注意事项](https://postgresweekly.com/link/106587/web)
我最近在RDS上遇到了这种情况（建议：为此事件设置警报;-)）。几个CrunchyData工程师在这里分享了一些有用的提示，告诉你在进入panic模式时要做或不做的事情。


`E Christensen, D Christensen, Katz, and Frost `
## [MostgreSQL的亚马逊RDS现在与AWS Lambda集成](https://postgresweekly.com/link/106588/web)
我仍然需要完全了解这一点，但是能够从Postgres存储过程或用户定义函数中调用无服务器Lambda函数似乎有很大的潜力。


`Amazon Web Services, Inc. `
## [Postgres Vision 2021  - 自由在线大会（6月22日至23日）](https://postgresweekly.com/link/106589/web)
这个自由，虚拟，全球活动将世界领先的PostgreSQL专家，用户和社区成员汇集在一起。演示将探讨现实世界中的用户故事和新技术，所有这些都将随着PostgreSQL的发展而发展。


`EDB `
## [五年来扩展PostgreSQL的经验教训](https://postgresweekly.com/link/106591/web)
“多年来，我们在近40台服务器上存储的数据已扩展到75 TB。”阅读这些人的故事总是非常有趣，尤其是在这样的部署中。


`Joe Wilm `
## [PostgreSQLite：一种使用Postgres“Like-SQLite”的方法](https://postgresweekly.com/link/106592/web)
一个简洁的小主意，由一个简单的30行shell脚本编排而成。不过，Docker承担了大部分的繁重工作。


`Felix Dietze `
## [Postgres中连接管理的三种方法](https://postgresweekly.com/link/106594/web)
连接池和管理是大多数人在数据库中忽略太久的领域之一。Craig简单地介绍了三种方法，以便在扩大规模时加以考虑。


`Craig Kerstiens `
## [基准测试Postgres：从头开始设置RAID阵列](https://postgresweekly.com/link/106595/web)
我已经很久没有坐下来建立自己的RAID阵列了（‘云’有很多问题要回答！）


`Vik Fearing `
## [实时可视化所有PostgreSQL性能指标](https://postgresweekly.com/link/106596/web)
在Datadog中收集OOTB和用于实时性能分析的定制度量。开始一个免费的Datadog试验。


`Datadog `
## [CITUS在CMU交谈：作为扩展的分布式Postgres](https://postgresweekly.com/link/106597/web)
Marco最近做了一个有趣的关于Citus的演讲，作为卡内基梅隆大学数据库技术系列的一部分，Citus是一个横向扩展的Postgres，视频现在已经可以查看了。一个好的，可访问的概述。


`Marco Slot `
## [Synchronous_commit的力量](https://postgresweekly.com/link/106599/web)
“Synchronous_commit是一个并不简单的设置之一，它可能控制了太多事情......”除了重写该特性的文档外，Bruce还概述了它在这里所做的工作的本质。


`Bruce Momjian `
## [PSPG 4.6.0发布](https://postgresweekly.com/link/106600/web)
pspg是一个“寻呼机”工具，用于处理Postgres中的表数据（尽管现在也支持MySQL）。4.6添加了一个新的查询流模式，用于从文本编辑器使用pspg。


`Pavel Stěhule `
# 💡本周提示


要减少数据库的存储占用，请确保列的顺序正确。通常，最好先放置固定大小的列，然后再添加可变长度的列。


将以下结构：


```
CREATE TABLE t_foo (
   c   varchar(100),
   a   int,
   d   varchar(100),
   b   int
);
```


改为：


```
CREATE TABLE t_foo (
   a   int,
   b   int,
   c   varchar(100),
   d   varchar(100)
);
```


它将减少表的大小，从而加快数据库。


要了解有关列的更多信息及其对PostgreSQL性能的影响，请查看我们的博客文章“缩小数据的存储空间”。


**🗓即将举办的Postgres活动**
