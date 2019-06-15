---
layout: post
title: 数据库每周新闻 2019-6-14
---

## 数据库每周新闻 #258 - 2019年6月14日
![config.yml]({{ site.baseurl }}/images/DBWeekly.png)
备注：[英文原文地址](https://dbweekly.com/issues/258)
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/ftryu0c63eifvjsgdhd4.jpg)

## [一份2019年的开源数据库报告：MySQL还在领先吗？](https://scalegrid.io/blog/2019-open-source-database-report-top-databases-public-cloud-vs-on-premise-polyglot-persistence/)
根据最近的调查，scalegrid介绍了开源数据库的使用情况（其中mysql、postgresql和mongodb是不出所料的领先者）。

`SCALEGRID`

## [将R和Python在数据科学的较量](https://github.com/matloff/R-vs.-Python-for-Data-Science)
在数据科学工作中使用python的方法越来越流行，但是r也许更适合这个任务。哪个更好？一个学习R的教授在这里做了一些比较。

`NORM MATLOFF`

## [怎样在K8s中运行数据库](https://studio3t.com/knowledge-base/articles/import-sql-database-to-mongodb/?utm_source=cooper&utm_medium=newsletter&utm_campaign=may31)

在K8S中运行数据库是一个有争议的话题，因为有状态集和K8S并不总是很好地发挥作用。数据库需要什么属性才能工作？

`COCKROACH LABS` **赞助商**

## [Postgres的Bloom索引](https://habr.com/en/company/postgrespro/blog/452968/)
之前的文章深入介绍了Postgres提供的每种类型的索引。这一次是基于bloom过滤的bloom索引，这是一种可以提供迅速字符串匹配查询的数据结构，但是它会有查询不精确的风险。

`EGOR ROGOV`

## [Socrates：云上新的SQL Server](https://www.microsoft.com/en-us/research/publication/socrates-the-new-sql-server-in-the-cloud/)
本文提出了一种新的DBAS体系结构，称为SOCRATES，该体系结构已在Microsoft SQL Server中实现，并在Azure中作为SQL数据库超尺度提供。

`MICROSOFT RESEARCH`

## [从Kafka到MongoDB：预览官方连接器](https://www.mongodb.com/blog/post/kafka-is-coming--previewing-the-official-mongodb-connector-for-apache-kafka)

Apache Kafka实时数据管道和流处理系统在企业部署中非常流行，MongoDB正在开发一种新的、本机的、完全支持的连接器，以实现双向集成

`SCOTT L'HOMMEDIEU (MONGODB, INC.)`



### 💻招聘
[招聘有求知欲的负责的开发者](https://www.keyvalues.com/carbon-five)--个人技术水平遇到瓶颈？新项目、技术和挑战与善良、支持和优秀的人完美结合。
`CARBON FIVE`

[在Vettery上寻找数据库有关的工作](https://www.vettery.com/tech?utm_source=newsletter&utm_medium=cooper-dbweekly&utm_term=tech&utm_content=grouped&utm_campaign=ad-88878) – Vettery专门为科技领域的求职者提供相关工作并完全免费。
`VETTERY`

### 📒 教程和故事

[AWS怎样管理PostgresSQL](https://www.youtube.com/watch?v=hdQ-geGBsq4) -- 一个高水准的50分钟视频，涵盖了AWS RDS的历史以及AWS多年来如何提供托管Postgres服务。介绍加密的工作方式、实例类型和复制。基本上是一个在AWS使用Postgres的初级课程。

`NORM MATLOFF`

[从RDBMS切换到DynamoDB的20个步骤](https://twitter.com/jeremy_daly/status/1137002244157710336) -- 这些关于如何从一个单一的RDBMS转变为一个围绕AWS流行的键/值和基于文档的产品的想法很有趣。

`JEREMY DALY ON TWITTER`



[引入MongoDB 4.2：通配符索引](https://www.mongodb.com/blog/post/coming-in-mongodb-42--1-wildcard-indexes)-- MongoDB 4.0发布已经一年多了，但现在我们可以开始期待下一个功能驱动的版本4.2，它将包含一种索引类型，该类型的索引只能索引与特定过滤器匹配的数据。

`DJ WALKER-MORGAN`



[探索10个Postgres的使用技巧](https://www.youtube.com/watch?v=vFq9Yg8a3CE) 

 这个视频的形式类似于网络通话，你可以获得一些PPT。视频的内容是很不错的，Bruce深入研究了各种较小但实用且有趣的Postgres技巧。

`BRUCE MOMIJAN`



[如何使用studio 3t将mongodb迁移到SQL数据库](https://www.youtube.com/watch?v=yt8TdNPDvfY)

`STUDIO 3T`



**简介**

- Jepsen对[tidb 2.1.7进行了分析](https://jepsen.io/analyses/tidb-2.1.7)。TiDB的维护人员PingCap已经写了[一篇关于过程和结果的文章](https://jepsen.io/analyses/tidb-2.1.7)。
- Qubole有一个[无服务器的SQL引擎](https://www.datanami.com/2019/06/13/serverless-sql-engine-targets-cloud-analytics/)，旨在进行基于云计算的“按量付费”分析。
- 人们质疑Hadoop的时间是否已经到了，是[公共云](https://www.nextplatform.com/2019/06/06/have-the-public-clouds-killed-hadoop/)还是[Kubernetes](https://www.bmc.com/blogs/hadoop-cloud-native-kubernetes/)在扼杀它。