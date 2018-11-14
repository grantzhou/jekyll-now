---
layout: post
title: PostgreSQL 每周新闻 2018-11-14
---

### PostgreSQL每周新闻 #282 - 2018年11月14日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)
![_config.yml](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/gbjg8tv40u9lhl2mikl1.jpg)

[阅读原文](https://postgresweekly.com/issues/282)

## [PipelineDB 1.0：PG 11的高性能时间序列聚合](https://www.pipelinedb.com/blog/high-performance-time-series-aggregation-for-postgresql-11)
如果这与上周发布的TimegaleDB 1.0（Postgres的另一个时间序列系统）相似，那么PipelineDB更侧重于聚合，并且不会长期存储粒度数据。 
正如他们自己所说，“PipelineDB应该用于仅需要摘要数据的分析用例，例如实时报告仪表板。”

`德里克·尼尔森 DEREK NELSON`

## [Postgres 11.1,10.6,9.6.11,9.5.15,9.4.20和9.3.25 发布了](https://www.postgresql.org/about/news/1905/)
主要用于修复pg_upgrade和pg_dump中的SQL注入安全问题的一系列发布。 
这也标志着9.3的最终版本，现已达到其寿命终结。
`PosrgreSQL全球开发组`

## [JackDB：Postgres的现代数据库客户端](https://www.jackdb.com)

![JackDB](https://copm.s3.amazonaws.com/14f5a240.png]
JackDB是一个基于Web的数据库客户端，具有用于安全性和协作的内置工具。 立即注册免费试用版。

`JACKDB，INC` **赞助商**

## [使用加密来加强Postgres数据库安全性](https://severalnines.com/blog/utilizing-encryption-strengthen-postgresql-database-security)
概述了使用加密作为建立数据库安全性和保护数据的措施之一。

`MARYANN KAMAU`

## [phpPgAdmin的幽魂](https://github.com/phppgadmin/phppgadmin)
phpPgAdmin是一个现在相当古老的基于Web的Postgres管理工具（与MySQL的phpMyAdmin类似）.
但是有一个新版本支持最近的Postgres版本..唯一的问题是它仍然使用PHP 5，而PHP 7版本即将推出。

`ROBERT TREAT`

## [防止Postgres中的SQL注入](https://tapoueh.org/blog/2018/11/preventing-sql-injections/)
![xkcd](https://tapoueh.org/img/exploits_of_a_mom.png)
当应用程序允许用户输入（或任何其他意外数据）来更改SQL查询的结构时，会发生SQL注入。 以下是一些避免这种情况的方法。

`DIMITRI FONTAINE`

## [使用Postgres进行机器学习 - K均值聚类算法](https://www.cybertec-postgresql.com/en/machine-learning-in-postgresql-part-1-kmeans-clustering/)
新系列帖子中的第一篇，探讨如何在不离开Postgres的情况下使用机器学习算法。

`HERNAN RESNISKY`

## [将Oracle自治事务迁移到Postgres](https://aws.amazon.com/blogs/database/migrating-oracle-autonomous-transactions-to-postgresql/)
从Oracle迁移到Postgres时，您可能会遇到Oracle自治事务。 这篇文章解释了它们是什么以及如何在Postgres中复制功能。

`YASER RAJA`

## [处理重要的Postgres数据库膨胀 - 您有什么选择？](https://labs.contactually.com/dealing-with-significant-postgres-database-bloat-what-are-your-options-a6c1814a03a5)
在Postgres中更新或删除数据时，会写入新数据。 然后需要对旧数据进行VACCUUM。 
这种未被VACCUUM的数据被称为*膨胀（bloat）*。 参见本文看看如何处理它。

`JOHN GERHARDT`

## [免费网络研讨会：PostgreSQL的备份管理](https://severalnines.com/resources/webinars/backup-management-mysql-mariadb-postgresql-mongodb-clustercontrol?utm_campaign=Backup_Campaign_NOV_2018&utm_content=webinar&utm_medium=Paid_Search&utm_source=banner)
解备份类型以及如何设计备份策略以确保高可用性。

`SEVERALNINES` **赞助商**

## [在Postgres中使用并行顺序扫描](https://rafiasabih.blogspot.com/2018/10/using-parallel-sequential-scan-in.html)
并行顺序扫描是PostgreSQL中的第一个并行访问方法，并在9.6版中引入。 下面介绍它的工作原理以及如何设置它。

`RAFIA SABIH`

# 活动
## [阿根廷PgDay 2018](https://www.pgday.com.ar/buenosaires2018?lang=en)
2018年11月21日（阿根廷布宜诺斯艾利斯）一个专注于PostgreSQL的小型会议。

## [澳大利亚 Pg Down 2018](https://2018.pgdu.org/)
2018年12月7日（澳大利亚墨尔本）PG Down 2018年是第二届年会，为PostgreSQL开发者和用户提供了一个聚会、学习和加强联系的绝佳机会。

## [欧洲2019年 PostgreSQL会议](https://2019.pgconf.eu)
2019年10月15日至18日（意大利米兰）第11届PostgreSQL欧洲会议，先是一天的由讲师指导的培训日，随后是为期三天的世界级PostgreSQL演讲和超级棒的展示。

