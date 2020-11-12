---
layout: post
title: PostgreSQL 每周新闻 2020-11-11
---
### PostgreSQL每周新闻#381 - 2020年11月11日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)
备注：[英文原文地址](https://postgresweekly.com/issues/381)
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/hzpplmat7ekv9pzew8ha.jpg)

## [Postgres可观测性：观测Postgres的视图和函数图](https://postgresweekly.com/link/98285/web)
一种交互式图表，提供与监视Postgres和跟踪统计信息相关的系统视图和功能的简化视图。这是在之前的工作基础上对Postgres13的更新，Alexey将在文中做更多解释。


`Alexey Lesovsky `
## [用Postgres、MobilityDB和Citus大规模分析GPS轨迹](https://postgresweekly.com/link/98287/web)
MobilityDB将时间和时空对象添加到Postgres和PostGIS中，这篇文章从实际意义上探讨了这意味着什么，以及Postgres如何做到不仅可以处理位置，而且可以处理移动。


`Mahmoud Sakr `
## [免费电子书：如何让你的Postgres数据库性能提高3倍](https://postgresweekly.com/link/98289/web)
了解我们为Atlassian等客户优化Postgres查询性能的最佳实践，以及如何将从磁盘加载的数据减少500倍。


`pganalyze `
## [复制冲突及其处理方法](https://postgresweekly.com/link/98290/web)
如果备用服务器是只读的，如何发生复制冲突？Vacuum，lock，buffer pin，等问题让这个问题更困难！幸运的是，有很多方法可以缓解这些问题，Laurenz分享了一些技巧。


`Laurenz Albe `
## [调查发现，开发者越来越多地将MongoDB与Postgres搭配](https://postgresweekly.com/link/98291/web)
这是一个有趣的发现，来自于一项对18000名开发者的新调查。

`Matt Asay `

## [如何分析Postgres Crash Dump文件](https://postgresweekly.com/link/98292/web)
我们真的希望你永远不必这样做，但是如果你真的在运行Postgres时遇到了core dump，这些提示可能会给你一些方向。


`Cary Huang `
## [是时候让PostgreSQL核心团队现代化了吗？](https://postgresweekly.com/link/98293/web)
Alvaro想知道是否有人和他一样对Postgres 核心团队的流程、结构和管理产生疑虑。


`Álvaro Hernández opinion`
## [托管PostgreSQL数据库的5种方法](https://postgresweekly.com/link/98294/web)
本指南介绍了运行PostgreSQL的各种方法：自行管理、由云提供商管理、由第三方管理。


`Prisma `
## [phpPgAdmin 7.13.0发布](https://postgresweekly.com/link/98295/web)
流行的基于Web的Postgres管理工具。删除了对PHP7.1的支持，增加了对Postgres13（和14，暂时）的支持。


`Robert Treat `
## [NoisePage：“自我驱动”的数据库管理系统](https://postgresweekly.com/link/98296/web)
NoisePage是一个开源的关系型数据库（使用Postgres兼容的wire protocol），完全专注于测试自主部署和机器学习优化技术。


`Carnegie Mellon University Database Group `
# 💡本周提示


Postgres和psql内置了对从不同格式的文件中复制（即批量加载）数据的支持。它被认为是一种在表和数据库之间转换数据的简单方法，这是正确的！


在psql中，这个命令被称为\COPY，它使得从在本地工作站上的文本和二进制文件中加载数据变得很容易。


给出一个名为readings的表，包含以下列：


```
id |          time          | reading
----|------------------------|---------
  1 | 2020-10-01 00:00:00-00 | 12.3
```


和名为reading的CSV文件.csv包括以下数据：


```
1,2020-10-01 01:00:00-00,15.4
1,2020-10-01 01:30:00-00,18.1
2,2020-10-01 01:00:00-00,20.2
...
```


我们可以在psql提示符下使用以下命令加载成千上万条记录：


```
\COPY readings FROM readings.csv CSV;
```


\COPY的一个缺点是它是单线程的，不支持批处理或并行复制。因此，对于一个大文件，这可能需要大量的时间。


Parallel Copy，一个用Go编写的免费开源工具，包装\Copy并提供批处理数据的并行插入。这意味着可以以较低的事务开销以更高的速率插入数据。


使用Parallel copy 复制相同的数据，运行内容如下，其中包括有用的功能可以获取进度更新：


```
timescaledb-parallel-copy --connection {CONNECTION STRING} --db-name {DATABASE NAME} --table readings --file {PATH TO `readings.csv`} --workers 4 --reporting-period 30s
```


默认情况下，这将一次批量复制5000行。


注意，Parallel Copy的开发主要是为了与TimescaleDB（一个建立在Postgres之上的时间序列数据库）一起使用，但是也可以与标准Postgres一起使用。


**🗓即将举办的Postgres活动**
