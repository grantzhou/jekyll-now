---
layout: post
title: 数据库每周新闻 2021-3-12
---
### 数据库每周新闻#345 - 2021年3月12日
![_config.yml]({{ site.baseurl }}/images/DBWeekly.png)
备注：[英文原文地址](https://dbweekly.com/issues/345)
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/oikjl80ggpvkzqss2rg2.jpg)


## [改善数据库用户和开发人员体验的想法](https://dbweekly.com/link/104613/web)
作者一直在思考数据库提供的开发人员体验以及如何改善这些体验。涵盖了使数据库迁移的意识，改进的内部脚本编写能力以及让数据库提供有关如何使用它们的“反馈”。

`Daniel Haig`


## [Citrus 10如何为Postgres带来柱状压缩](https://dbweekly.com/link/104614/web)
Citus是一个长期存在的扩展，它使Postgres更具分布式/水平可扩展性，而版本10刚刚发布。它将列式存储首次引入Postgres，并且该帖子很好地解释了包括优缺点在内的内容。

`Jeff Davis (Microsoft)`


## [📈TimescaleAnalytics项目：PostgreSQL的时间序列分析](https://dbweekly.com/link/104616/web)
Timescale Analytics的目的是将SQL执行时间序列分析所需的所有功能组合到一个由Rust构建的PG扩展中，我们需要（并且需要）您的帮助。查看当前的提案，捐款方式以及如何加入我们和制定项目💪

`Timescale sponsor`


## [使用Parquet压缩数据](https://dbweekly.com/link/104617/web)
Parquet是一种面向开放列的数据存储格式，主要与Hadoop相关。这篇文章探讨了为什么Parquet可以是一种有效的（在存储使用方面）存储大型数据集的方法，而不是像SQLite这样的方法。

`Istvan Szukacs`


## [使用适用于Amazon DynamoDB和Apache Hudi的Amazon Kinesis数据流构建数据湖](https://dbweekly.com/link/104622/web)
这是很多流行语。基本上，您将诸如客户行为或操作之类的内容存储在Amazon DynamoDB中，通过Kinesis在流中推送更改，然后将其存储在S3上以供Apache Hudi进行批处理。

`Thakur, Qu, and Shrivastava`


## [通过按需模式安全地降低未使用的DynamoDB表的成本](https://dbweekly.com/link/104624/web)
一种通过将按需模式应用于未使用的表（而不是仅删除它们）来降低DynamoDB I / O成本的简介。

`Lee and Rahaman Sayem`


## [SQL的三值逻辑（3VL）](https://dbweekly.com/link/104625/web)
除了对与错之外，SQL中逻辑表达式的结果也可能是未知的。

`Markus Winand`


## [Oracle 21c中的JSON数据类型支持](https://dbweekly.com/link/104626/web)
今年早些时候发布的Oracle Database 21c引入了一种新的二进制JSON数据类型，该数据类型由一种新的OSON格式提供支持（是的，O代表Oracle。）

`Zhen Hua Liu (Oracle)`


## [在SQL中无需额外往返就可以计算分页元数据](https://dbweekly.com/link/104628/web)
有关如何在不进行第二次往返的情况下进行分页的教程，包括首先计算总行数，当前页数等。SQL首先是SQL，但是后面的jOOQ示例也很有趣。

`Lukas Eder`


## [加快pgbench使用速度COPY FREEZE](https://dbweekly.com/link/104629/web)
pgbench是Postgres随附的基准测试工具，由该文章的作者于1999年编写。在这里，他研究了由于即将推出的Postgres 14增强而为加快基准测试过程而进行的优化。

`Tatsuo Ishii`


## [探索适用于DOS的Borland dBase IV](https://dbweekly.com/link/104631/web)
借助dBase IV进行整洁的（远程）存储通道，早期DBMS的发布也许标志着其在早期PC市场上的统治地位已经结束。（注意：当我阅读它时，该站点上的侧边栏包含一些NSFW内容，因此请注意是否有问题。） 

`psychocod3r`


## [如何在macOS上使用SQLite运行MediaWiki](https://dbweekly.com/link/104632/web)
如果要深入了解架构，则可能很有用。

`Simon Willison`


## [在Kubernetes上运行CockroachDB](https://dbweekly.com/link/104633/web)
l,null,"en

`Alex Robinson and Jim Walker`


## [使用NFL游戏数据的R中的线性回归模型](https://dbweekly.com/link/104634/web)
l,null,"en

`Geoffrey Grosenbach`


## [将SQL从一种方言转换为另一种方言](https://dbweekly.com/link/104635/web)
尽管SQL已进行了多次标准化，但其实现方式确实会有所不同，因此该工具继续提供了一种有趣的方式来查看您自己的查询中的差异。

`Lukas Eder`


## [使用Datadog提升数据库性能](https://dbweekly.com/link/104636/web)
通过Datadog中的细粒度分析快速识别运行缓慢的查询，瓶颈和错误。免费试用Datadog。

`Datadog sponsor`


## [fsql：使用SQL式查询在文件系统中进行搜索](https://dbweekly.com/link/104637/web)
用Go语言编写的工具，可让您执行以下操作SELECT name, size FROM . WHERE NOT name RLIKE *.go

`kashav`


## [Hive 2.0：使用Pure Dart编写的快速键值数据库](https://dbweekly.com/link/104638/web)
Dart是十年前起源于Google的一种JavaScript竞争对手，它并不是用于构建数据库系统的显而易见的语言，因此对于看。它是在考虑Flutter用例的情况下创建的。

`Simon Leier`


## [想要：具有❤的好奇开发人员](https://dbweekly.com/link/104640/web)
停滞不前？碳五公司拥有新的项目，技术和挑战，与友善，支持且有才华的人们完美地结合在一起。加入我们。

`Carbon Five`


## [X-Team（远程）的DevOps工程师](https://dbweekly.com/link/104641/web)
加入最有活力的开发人员社区，并参与Riot Games，FOX，Sony，Coinbase等项目。

`X-Team`
