---
layout: post
title: PostgreSQL 每周新闻 2021-4-14
---
### PostgreSQL每周新闻#401 - 2021年4月14日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)
备注：[英文原文地址](https://postgresweekly.com/issues/401)
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/kojhnf0zdptcuyxnhkl2.jpg)
## [清理Postgres中的大量BLOB](https://postgresweekly.com/link/106213/web)
不，不是来自外太空的致命blob，而是“二进制大对象”。许多工程师根本不赞成在数据库中存储大型二进制数据，但当你需要时，有一些方法可以让Postgres的处理更高效。


`Hans-Jürgen Schönig `
## [是Amazon RDS for PostgreSQL 还是Amazon Aurora PostgreSQL？哪个是更好的选择？](https://postgresweekly.com/link/106214/web)
我认为很多人都对Aurora或直接RDS在什么时候适应哪些情况有很多困惑。本文中，亚马逊试图澄清一些事情。

`Vivek Singh and Sagar Patel (AWS) `

## [⚡ 改进PostgreSQL插入的13个技巧](https://postgresweekly.com/link/106215/web)
从如何测试和优化磁盘性能到使用并行写入、批量插入等等，获取我们最喜欢的加速PG摄取率的方法，以此获取更快的数据库，更快的查询🚀

`Timescale `

## [Apache AGE 0.4: 一个Postgres的图形扩展](https://postgresweekly.com/link/106216/web)
为Postgres提供图形数据库功能的扩展，其灵感来自AgensGraph。最新版本（0.4.0）添加了各种小语法级别的特性。详见GitHub库。


`Apache Foundation `
## [如何运行分层查询](https://postgresweekly.com/link/106219/web)
从Oracle的方式，然后到Postgres中CTE的使用，演示如何查询标准表中表示的层次结构。


`Ahsan Hadi `
## [确定共享内存的大小](https://postgresweekly.com/link/106221/web)
Postgres 13添加了pg_shmem_allocations，这是一种详细了解Postgres对分配的共享内存的使用情况和大小的方法。

`Bruce Momjian `

## [管理事务ID耗尽和循环](https://postgresweekly.com/link/106222/web)
在过去，事务ID的循环给许多Postgres管理员带来了问题。这篇文章关注的是一种监视和缓解这一问题的方法。


`Keith Fiske `
## [2021年内部工具状况报告](https://postgresweekly.com/link/106223/web)
我们调查了650名开发者，了解他们如何以及为什么构建内部应用程序。找出最流行的工具和数据库。


`Retool `
## [QGIS、Postgres和PostGIS入门](https://postgresweekly.com/link/106224/web)
快速介绍如何设置PostGIS和QGIS，这是一个用于查看、编辑和分析地理空间数据的桌面应用程序，用于查看OpenStreetMap数据。


`Hans-Jürgen Schönig `
## [采访EDB的Devrim Gündüz](https://postgresweekly.com/link/106225/web)
Andreas的“PostgreSQL每周人物”系列，很高兴能更多地了解我们社区的人。Devrim为Postgres工作了22年。


`Andreas Scherbaum `
## [如何使用AWS CodeBuild和Amazon EventBridge在Amazon RDS for PostgreSQL中调度作业](https://postgresweekly.com/link/106226/web)


`Suresh Moolya (AWS) `
# 💡本周提示


**🗓即将举办的Postgres活动**
