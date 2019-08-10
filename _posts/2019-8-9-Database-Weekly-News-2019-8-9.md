---
layout: post
title: 数据库每周新闻 2019-8-9
---

## 数据库每周新闻 #266 - 2019年8月9日

![config.yml]({{ site.baseurl }}/images/DBWeekly.png)
备注：[英文原文地址](https://dbweekly.com/issues/266)

![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/ehctjbeuoj5jbfijmgbj.jpg)

## [NVIDIA怎样提升数据科学](https://medium.com/m/global-identity?redirectUrl=https%3A%2F%2Ftowardsdatascience.com%2Flife-after-hadoop-getting-data-science-to-work-for-your-business-c9ab6605733f)

我们之前就提到NVIDIA在数据科学领域的志向，现在有两位NVIDIA的工程师的一篇文章，展示了基于GPU的工具如何将数据科学推向新的阶段，其中包括GPU存储。

`JOSH PATTERSON`

## [使用BigQuery和HyperLogLog建立PB级别的数据分析](https://t.co/6XsmhZvp18)

Permutive为发布者提供了一个数据和分析平台，BigQuery和HyperlogLog在保持事物快速和准确方面发挥着重要作用。

`PAULIUS IMBRASAS`

## [电子书：优化数据库性能的最佳实践](https://pganalyze.com/ebooks/optimizing-postgres-query-performance?utm_source=PostgresWeeklyPrimary)

学习我们如何为Postgres优化性能,如何500倍的降低磁盘IO。

`PGANALYZE`

## [对比Postgres的JSONB和Couchbase](https://blog.couchbase.com/postgres-jsonb-and-nosql/)

Postgres真的能通过JSONB取代‘NOSQL’文档数据库么？从一个文档数据库供应商的角度来看，这是一个有意思的话题。

`DENIS ROSA (COUCHBASE)`



## [使用Amazon Aurora Multi-Master创建高可用MySQL APP](https://henrikwarne.com/2019/07/27/book-review-designing-data-intensive-applications/)

新推出的AmazonAurora多主机为Amazon的MySQL兼容数据库服务Aurora带来了更高的可用性功能。

`AMAZON WEB SERVICES`



## 快速浏览

- PostgresSQL 11.5 ，10.10,9.6.15发布，它修复了两个安全性问题和超过40个bug
- 有史以来第一次分布式SQL峰会将于9月20日在San Jose举行
- 从2019年10月1日起，微软的许可条款将影响用户在“专用托管云服务”（如AWS）上使用prem服务。
- 惠普已经收购了Mapr，这家Hadoop公司最近面临着不确定的未来
- BigQuery现在支持持久的用户定义函数。
- 由于预计PostgreSQL 12将增加对SQL/JSON的支持，Markus Winand一直在测试和比较其他数据库（包括SQLite、Mariadb、MySQL和SQL Server）的SQL/JSON功能。
- BlazingSQL，一个基于Rapids的SQL引擎，现在是开源的。Nvidia数据科学故事的另一个有趣部分。



### 💻招聘

在Vettery上找到一份新的开发工作——Vettery专注于技术角色，对求职者来说是完全免费的。

`VETTERY`



### 📒 其他

[我是如何销毁多个生产数据库的](https://www.redhat.com/sysadmin/destroying-multiple-production-databases)一个90年代的系统管理员“恐怖故事”教会了这位工程师一些未来的教训。

`JAN GERRIT KOOTSTRA`

[Stack Overflow如何使用redis进行应用缓存](https://nickcraver.com/blog/2019/08/06/stack-overflow-how-we-do-app-caching/)一个有趣的技术描述，描述了流行的开发者Q&A站点Stack Overflow如何使用redis来保持事情的顺利运行。

`NICK CRAVER (STACK OVERFLOW)`

[Mariadb vs MySQL，一个技术的衰败](https://kinsta.com/blog/mariadb-vs-mysql/)——不要只是把Mariadb看作是MySQL的衍生产品，它还有更多的功能。

`TONINO JANKOV`

[您不需要一个ER图来理解您的数据库](https://dataedo.com/blog/you-dont-need-an-er-diagram-to-understand-your-database)-“ERD对于可视化数据库很好，但不适合作为文档本身。”
`PIOTR KONONOW`

[MontyDB:python中MongoDB的一个很小的克隆版本](https://github.com/davidlatwe/montydb)——这对python开发人员来说有点有趣。这是一个Tinydb灵感，纯Python MongoDB-A-like！

`DAVID LAI`

[LF：一个完全分散、完全复制的密钥/值存储](https://github.com/zerotier/lf)——它被称为“beta”软件，但这是一个有趣的实验，可以为“小但关键”的信息片段创建一个快速的数据存储（想想ETCD，但适用于开放、分散的系统）。。
`ZEROTIER, INC.`