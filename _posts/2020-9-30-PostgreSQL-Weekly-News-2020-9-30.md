---
layout: post
title: PostgreSQL 每周新闻 2020-9-30
---
### PostgreSQL每周新闻#375 - 2020年9月30日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)
备注：[英文原文地址](https://postgresweekly.com/issues/375)
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/v1601459537/oeuuwvsn6lijzdzybx6d.png)
## [Postgres 13发布](https://postgresweekly.com/link/95879/web)
距离Postgres 12发布不到一年，这里13致力于我们最喜欢的数据库的进化步骤。发行说明提供了所需的新功能和已调整功能的清单，但是我们将在此处介绍相关文章的链接，以涵盖其中的一些大问题：
 * B树索引中的重复数据删除
 * VACUUM的并行性
 * 受信任的扩展
 * 使用SELECT gen_random_uuid（）无需扩展
 * CREATE STATISTICS现在可以帮助进行IN / ANY操作的计划
 * postgres_fdw现在支持证书认证
 * TLS改进
 * ..和其他隐藏的宝石！


`PostgreSQL Global Development Group `
## [🏆排名前5位的PostgreSQL扩展](https://postgresweekly.com/link/95887/web)
我们汇总了我们和TimescaleDB社区成员的一些必备PG扩展，并提供了为什么选择它们，安装说明，示例查询和专业提示来帮助您入门。


`Timescale `
## [快速了解Postgres 13 RC1的查询性能](https://postgresweekly.com/link/95888/web)
这些基准测试是在Postgres 13最终发行版（已经花了三天的时间！）发布之前完成的，但应该继续坚持下去。与12.4相比，新版本的结果大致（但并非一致）是肯定的。


`Kaarel Moppel `
## [大规模运行Postgres：免费（基本）节省空间](https://postgresweekly.com/link/95889/web)
在其Postgres集群上运行着超过100 TB的数据，任何可能的效率提高对于Braintree都是一个巨大的胜利。这是有关他们如何通过对表列进行重新排序而“不费吹灰之力”来节省大约10％磁盘空间的故事。


`James Coleman (Braintree) `
## [何时部署或升级到新的主要Postgres版本](https://postgresweekly.com/link/95890/web)
尽快将某些东西（咳嗽，咳嗽，Postgres 13）升级到最新和最好的版本几乎是不切实际的，但是您如何应对不可避免的未来升级呢？


`Andrew Dunstan `
## [使用普通SQL进行简单的异常检测](https://postgresweekly.com/link/95891/web)
使用一些高中水平的统计信息和对SQL的充分了解，我实现了一个有效的简单异常检测系统。”


`Haki Benita `
## [使用Postgres和pgRouting探索游艇岩石的平滑波](https://postgresweekly.com/link/95892/web)
pgRouting是Postgres和PostGIS的强大地理空间路由扩展，通常用于寻路/映射/方向应用。这篇文章创造性地试图用它来找到最有影响力的游艇摇滚艺术家。


`John Porvaznik `
## [我们将看看Postgres 13的新增功能：更高的性能，更好的监视和更多功能](https://postgresweekly.com/link/95894/web)
带有B树重复数据删除功能的较小索引，扩展的Statis改进，并行VACUUM，改进的WAL使用情况统计信息等等。


`Pganalyze `
## [使用GET STACKED DIAGNOSTICS调试PL / pgSQL](https://postgresweekly.com/link/95895/web)
GET STACKED DIAGNOSTICS使调试PL / pgSQL代码容易得多，但并不广为人知。这篇文章将展示它的作用以及如何使用它。


`Hans-Jürgen Schönig `
## [如何在Pgpool-II中配置SCRAM和MD5身份验证](https://postgresweekly.com/link/95896/web)
Pgpool-II是流行的Postgres连接池。


`Bo Peng `
## [DuckDB：一个可嵌入的SQL OLAP数据库系统](https://postgresweekly.com/link/95898/web)
DuckDB内置C ++，自称（geddit？）为“ SQLite for Analytics”，并具有C / C ++，Python和R的绑定。我们在《数据库每周》中多次提到了这一点。 ，但令我感到惊讶的是，它也可以补充Postgres的用例。


`CWI Database Architectures Group `
# 💡本周提示


**🗓即将举办的Postgres活动**
