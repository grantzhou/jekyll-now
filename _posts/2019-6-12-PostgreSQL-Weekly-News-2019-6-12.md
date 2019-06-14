---
layout: post
title: PostgreSQL 每周新闻 2019-6-12
---

### PostgreSQL每周新闻#309 - 2019年6月12日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)

备注：[英文原文地址](https://postgresweekly.com/issues/309)

![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/v1560346213/fg5y56anj1ybanycy7h3.jpg)  

## [ 探索10个Postgres的使用技巧](https://www.youtube.com/watch?v=vFq9Yg8a3CE)
 这个视频的形式类似于网络通话，你可以获得一些PPT。视频的内容是很不错的，Bruce深入研究了各种较小但实用且有趣的Postgres技巧。

`BRUCE MOMIJAN`

## [PG12中如何改善COPY操作和数据批量导入](https://www.cybertec-postgresql.com/en/tech-preview-improving-copy-and-bulkloading-in-postgresql-12/) 
copy命令通常用于快速将数据加载到postgres中，Postgres 12的copy命令将支持where语句。

`HANS-JÜRGEN SCHÖNIG`

## [PostgreSQL记录日志的最佳实践](https://www.strongdm.com/postgresql-logging-best-practices/?utm_source=PG%20Weekly&utm_medium=email&utm_campaign=2019-06-07%20-%20%5BRBLP%5D%20-%20%5BSDM%5D%20-%20postrgres)
在一些情况下你可能想要开启数据库审计，这里介绍几种审计的最佳实践以及他们的优劣势。

`STRONGDM ` **赞助商**

## [Postgres的Bloom索引](https://habr.com/en/company/postgrespro/blog/452968/)
之前的文章深入介绍了Postgres提供的每种类型的索引。这一次是基于bloom过滤的bloom索引，这是一种可以提供迅速字符串匹配查询的数据结构，但是它会有查询不精确的风险。

`EGOR ROGOV`

## [AWS怎样管理PostgresSQL](https://www.youtube.com/watch?v=hdQ-geGBsq4)
一个高水准的50分钟视频，涵盖了AWS RDS的历史以及AWS多年来如何提供托管Postgres服务。介绍加密的工作方式、实例类型和复制。基本上是一个在AWS使用Postgres的初级课程。

`KEVIN JERNIGAN`

## [Postgres12将会支持干预执行计划](https://habr.com/en/company/postgrespro/blog/452900/)
使用prepare可以提高查询的性能，Postgres可以智能的决定在不同的参数下使用不同的查询计划。Postgre12能让你更直观的了解它的原理。

`HANS-JÜRGEN SCHÖNIG`

## [PostgreSQL的BRIN索引](https://pganalyze.com/ebooks/optimizing-postgres-query-performance?utm_source=PostgresWeeklySecondary)
BRIN（块范围索引）索引是一种加速表顺序扫描的强大方法，索引值可以被分组为值的“范围”（例如邮政编码、年龄、订单总数）。

`EGOR ROGOV`

## [Postgres的增量备份和基于时间点的还原](https://pgdash.io/blog/postgres-incremental-backup-recovery.html)
怎样使用归档的wal日志完成基于时间点的还原（PITR）
`RAPIDLOOP`

## ▶[深入研究Amazon Aurora PostgreSQL性能调优](https://www.youtube.com/watch?v=hdQ-geGBsq4)
一个小时的演讲，演讲者承诺你将真正学到一些东西。

`JAMES FINNERTY`

## [为什么RDMB S是分布式数据库的未来](https://www.citusdata.com/blog/2018/11/30/why-rdbms-is-the-future-of-distributed-databases/?utm_source=PG_Weekly&utm_medium=email&utm_campaign=sponsor_blog)
探索为什么分布式Postgres RDRMS能为APP开发者减少开发成本。

`CITUS DATA, NOW PART OF MICROSOFT` **赞助商**

## [获取分区信息的递归CTE](https://fluca1978.github.io/2019/06/12/PartitioningCTE.html)
一个相当强大的SQL查询，它将让您看到关于数据库中所有分区的信息

`LUCA FERRARI`

## [Boxball:加载一个完整的棒球历史数据集到Postgres](https://github.com/droher/boxball)
想找一个数据集来玩Postgre数据库么,尤其是玩cstore_fdw?这里有一个内建的Docker镜像可能成为你的选择。

`DAVID ROHER`

```markdown
🗓  **即将举办的Postgres活动**  

- [PostgreSQL Ibiza(六月19-21日, 伊维萨)](https://www.pgibz.io/index.html) —— 这个在西班牙著名的度假岛上举行的会议将会带来“海滩上的Postgres”，同时仍然在一个漂亮整洁的场地上进行会谈和培训。  
- [Postgres Vision 2019(6月24日,波士顿)](https://postgresvision.com/) —— Web发明者Tim Berners-Lee爵士将发表主题演讲。
- [PostgresLondon 2019 (7月2-3日，伦敦)](https://postgreslondon.org/)
- [PostgresConf Beijing 2019(7月3-6日，中国北京)](https://postgresconf.org/conferences/Beijing)
- [2019年奥地利PGDay (September 6 in Wiener Neustadt, Austria)](https://pgday.at/en/)

```



🔬 **psql命令周期表 （Again!）**
上周，我们包含了PSQL命令表（由Cybertec的Marcelo Diaz提供），但未能链接到更高分辨率版本以供您自己打印或安全保存！

感谢所有通过电子邮件指出这个问题的人。现在已经解决了这个问题，所以这里是图表，它现在链接到一个更高分辨率的副本在[这里](http://no.gd/cheatsheet.png)：—）
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/v1559733987/y74anviavcgujchlknif.png)


