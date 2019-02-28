---
layout: post
title: PostgreSQL 每周新闻 2019-02-27
---

### PostgreSQL每周新闻#294 - 2019年2月27日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)  
备注：[英文原文地址](https://postgresweekly.com/issues/294)

![pg_img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/bmmyebm9gbi5slivgwj8.jpg)

## [使用并行查询](https://www.percona.com/blog/2019/02/21/parallel-queries-in-postgresql/)
“PostgreSQL中的并行查询允许我们利用许多CPU资源来更快地完成报表查询。并行查询功能在9.6中得以实现并有所帮助。从PostgreSQL 9.6开始，报表查询能够使用许多CPU资源，并且完成得更快。 ”

`NICKOLAY IHALAINEN`

## [不要错过Postgres Vision 2019](https://postgresvision.com/)
![img](https://copm.s3.amazonaws.com/620f4361.png)  
6月24日至26日，波士顿，马萨诸塞州，加入我们。现在注册。

`ENTERPRISEDB` **赞助商**

## [Postgres的开源备份管理现状](https://severalnines.com/blog/current-state-open-source-backup-management-postgresql)
深入探讨最流行的Postgres开源备份程序，包括它们的现状以及相互之间的对比。

`ACHILLEAS MANTZIOS`

## [PostgreSQL BRIN索引：最小存储实现大数据查询](https://info.crunchydata.com/blog/postgresql-brin-indexes-big-data-performance-with-minimal-storage)
块范围索引（或“BRIN”）可以帮助您显着减少对大数据进行高性能查询所需的磁盘空间量。这是在Postgres 9.5中引入的。

`JONATHAN S. KATZ`

## [如果Postgres是增长最快的数据库，为什么Postgres社区如此之小？](https://blog.timescale.com/postgresql-database-community/)
Timescale的Andrew Staller指出Postgres继续被称为“增长最快的DBMS”，但它的相关会议和社区团体规模仍然很小。

`ANDREW STALLER (TIMESCALE)`

## [PostgreSQL fsync失败问题修复了（为什么！）](https://www.percona.com/blog/2019/02/22/postgresql-fsync-failure-fixed-minor-versions-released-feb-14-2019/)
Postgres最近修复了使用fsync的长期问题。这篇文章解释了问题所在。

`AVINASH VALLARAPU`

## [使用Laravel和Postgres创建简单的联系人列表](https://blog.digitalocean.com/create-simple-contacts-laravel-postgresql/)
现代的PHP肯定比我以前用的摔过跤的PHP好很多！

`KAMAL NASSER`

## [电子书：优化Postgres查询性能的最佳实践](https://pganalyze.com/ebooks/optimizing-postgres-query-performance?utm_source=PostgresWeeklySecondary)
在这本免费的pganalyze的电子书中，可以了解如何在Postgres数据库上获得3倍的性能提升，并且磁盘加载的数据减少500倍。

`PGANALYZE` **赞助商**

## [我们如何使用延迟复制进行Postgres灾难恢复](https://about.gitlab.com/2019/02/13/delayed-replication-for-disaster-recovery-with-postgresql/)
复制不是备份。或者复制是备份？下面介绍延迟复制以及GitLab如何用它来恢复意外的标签删除。

`ANDREAS BRANDL`

## [在Emacs和Postgres上经营一家面包店](https://bofh.org.uk/2019/02/25/baking-with-emacs/)
这是当程序员将他们的技能转变为经营面包店时会发生的事情。

`PIERS CAWLEY`

## [WAL-G：Postgres的归档和恢复](https://github.com/wal-g/wal-g)
作为WAL-E的继承者，WAL-G是一个完整的重写版本，具有更好的性能，并行化和压缩选项。

`CITUS DATA`

## [PostGIS中的Proj6](http://blog.cleverelephant.ca/2019/02/proj4-postgis.html)
仅限地理空间人群！Proj是Postgres在将空间坐标从一个系统转换为另一个系统时使用的库。Proj6是其最新版本。

`PAUL RAMSEY`

# ![_config.yml]({{ site.baseurl }}/images/Tips-icon.png)   本周提示
由strongDM提供支持

## 看看你的表（和索引！）占用了多少空间
我一直在开发一个小应用程序（[Hacker News标题编辑跟踪器](https://hackernewstitles.netlify.com/)）并使用一个非常小的[ElephantSQL](https://www.elephantsql.com/)实例进行存储。密切关注数据使用对我来说很重要，但是怎么做呢？

依靠提供者的管理系统或数据库管理工具展示总使用情况是一个好主意，但如果您想快速从psql中获取一些数字，有一些方法可以用SQL做同样的事情：

`SELECT`  
`relname AS table_name,`  
`pg_size_pretty(pg_total_relation_size(relid)) AS total,`  
`pg_size_pretty(pg_relation_size(relid)) AS internal,`  
`pg_size_pretty(pg_table_size(relid) - pg_relation_size(relid)) `  
`AS external,`  
`pg_size_pretty(pg_indexes_size(relid)) AS indexes`  
`FROM pg_catalog.pg_statio_user_tables ORDER BY `  
`pg_total_relation_size(relid) DESC;`  

它不是世界上最好看的查询，但会得到这样的结果：
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/evcxzs4e1s9c3zptx0c8.jpg)

在这里，我们可以看到一个表占用的空间总量（如果包括存储在表本身和附加的TOAST表中的数据）以及每个表的索引。

如果要查看每一个有问题的索引，而不是将表的所有索引捆绑成一个，这里有一个[稍微复杂的查询](https://gist.github.com/peterc/05fca349f6f0ad683941e36e82a97b9e)可供使用。

> 本周的技巧由[strongDM](https://www.strongdm.com/)赞助，这是保护您访问服务器/数据库的最佳方式。 [安排10分钟的演示](https://www.strongdm.com/)
