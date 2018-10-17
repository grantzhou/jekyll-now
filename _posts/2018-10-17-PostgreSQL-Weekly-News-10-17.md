---
layout: post
title: PostgreSQL 每周新闻 2018-10-17
---

### PostgreSQL每周新闻 #278 - 2018年10月17日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)
![_config.yml]({{ site.baseurl }}/images/wn1017.jpg)

备注：[英文原文地址](https://postgresweekly.com/issues/278)


## [管理大型Postgres数据库的备份和复制](https://medium.com/leboncoin-engineering-blog/managing-postgresql-backup-and-replication-for-very-large-databases-61fb36e815a0)

Postgres有不同的模型用于制作具有不同优缺点的备份，当在大规模的情况下，这家公司却依赖于Barman，pg_basebackup和pg_receivewal。

[*Medium 网站国内无法访问，这里提供PDF版本下载* DOWNLOAD]({{ site.baseurl }}/images/Managing%20PostgreSQL%20backup%20and%20replication%20for%20very%20large%20databases.pdf)

`FLAVIO GURGEL`

## [PostgreSQL 11 候选版本1 发布](https://www.postgresql.org/about/news/1893/)
下一个主要Postgres版本的第一个候选版本就在这里。 一切顺利，最终版本可能是明天，但这取决于这个RC的表现如何:-)
这里有一些新的东西。

`POSTGRESQL全球开发组`

## [2Q PGConf 2018 - 现在就安排](http://www.2qpgconf.com/)
![2QPG](https://copm.s3.amazonaws.com/7b89e5d9.png)

加入我们，在芝加哥，了解PostgreSQL最近的成就和令人兴奋的未来发展。 您还可以参加以下专家的实践培训：多主复制，性能调优和PostgreSQL安全。

`2NDQUADRANT POSTGRESQL` *活动赞助商*

## [将Postgres扩展到多TB及以上的想法](https://www.cybertec-postgresql.com/en/ideas-for-scaling-postgresql-to-multi-terabyte-and-beyond/)
Postgres可以适应一些真正大型数据集的一些功能和方法的随意综述。

`KAAREL MOPPEL`

## [如何在Postgres（或任何数据库）中有效地管理连接](https://brandur.org/postgres-connections)
连接管理和这些连接的成本是您在启动时不会注意的事情，但可能会在以后引起问题。 Brandur讲述了从Postgres连接的基础知识，以及如何通过连接池更好地处理它们。

`BRANDUR LEACH`

## [PostgreSQL的Amazon RDS支持新的小版本10.5,9.6.10,9.5.14,9.4.19和9.3.24](https://aws.amazon.com/about-aws/whats-new/2018/10/rds-postgresql-supports-minor-versions/)
`亚马逊网络服务 AWS`

## [PostgreSQL 11：新增功能](https://pgdash.io/blog/postgres-11-whats-new.html?h)
Postgres 11的一个系列综述，最终版本蓄势待发。

`RAPIDLOOP`

## [了解PostgreSQL中的检查约束](https://severalnines.com/blog/understanding-check-constraints-postgresql)
检查约束是一种完整性约束，它指定数据库表中每一行必须满足的要求。

`JOSHUA OTWELL`

## [使用公钥/私钥签名跟踪行更改](https://www.percona.com/blog/2018/10/12/track-postgresql-row-changes-using-public-private-key-signing/)
在某些情况下帮助防止恶意结构或数据更改的方法。

`IBRAR AHMED`

## [Autoprewarm：pg_prewarm中的新功能](https://postgresrocks.enterprisedb.com/t5/Postgres-Gems/Autoprewarm-a-new-functionality-in-pg-prewarm/ba-p/1908?_ga=2.180339172.1388954721.1537932578-1636716584.1528749863)
pg_prewarm可用于将关系数据加载到OS或Postgres缓冲区缓存中。 在PG 11中，您将能够自动预热服务器重启后缓冲区将重新加载的位置。

`POSTGRES ROCKS`

## [PostgreSQL中的索引功能 YOUTUBE](https://www.youtube.com/watch?v=VVG8nYqIiMI)
涵盖Postgres支持的不同类型的索引，如何查找丢失和未使用的索引，GIN和GiST索引的概述等。
*如果无法访问Youtube，请联系我们，我们可以将视频下载地址*
`PAVAN DEOLASEE`

## [PostgreSQL管理和自动化 - 免费白皮书](xx)
探索管理PostgreSQL的挑战以及如何有效地处理管理带来的任务。

`SEVERALNINES` *赞助商*

## [PGTune：创建Postgres配置设置的Web工具](https://pgtune.leopard.in.ua/#/)
选择你的Postgres版本，说明你有什么用途，总RAM等等，它会产生一些比默认值更好的配置设置（尽管你仍然会有调整）。

`ALEXEY VASILIEV`

## [pgFormatter：Postgres SQL语法Beautifier](https://github.com/darold/pgFormatter)
可以通过CGI从终端或Web服务器上运行。 在这里演示。

`GILLES DAROLD`

# 活动
## [PGConf.EU 2018 - 会议日程](https://www.postgresql.eu/events/pgconfeu2018/schedule/)
10月23日至24日（葡萄牙里斯本）激动人心的会议阵容已经出版。

## [PGDay.Seoul 2018](http://pgday.postgresql.kr/)
2018年11月3日（韩国首尔）PostgreSQL韩国用户组准备了第三个活动(半天)。
所有演讲均采用韩语。

## [Pg Down 2018](https://2018.pgdu.org/)
12月7日（澳大利亚墨尔本）PG Down 2018年是第二届年会，为PostgreSQL开发者和用户提供了一个聚会、学习和加强联系的绝佳机会。


