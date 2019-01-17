---
layout: post
title: PostgreSQL 每周新闻 2019-1-16
---

### PostgreSQL每周新闻#288 - 2019年1月16日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)

备注：[英文原文地址](https://postgresweekly.com/issues/288)

![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/mzmbylaeip5dxl8iriov.jpg%0A)

## [回顾：Postgres的历史](https://arxiv.org/abs/1901.01973)
这篇文章介绍了一些关于Postgres的[背景信息](https://databeta.wordpress.com/2019/01/09/a-history-of-postgres/),但它基本上是ACM委托编写的关于图灵奖获奖者的书的免费章节，它深入研究了Postgres的起源。[PDF链接](https://arxiv.org/pdf/1901.01973.pdf)

`JOSEPH M. HELLERSTEIN`

## [如何为Postgres做贡献](https://www.citusdata.com/blog/2019/01/15/contributing-to-postgres/)
PostgreSQL每年都会发布一个新版本。新版本的开发工作能够顺利提前完成，是因为提出改进是以“commitfest”竞赛的形式组织的。我们来看一些能够开始为postgres作出贡献的方法。

`CRAIG KERSTIENS`

## [数据是您的业务根本](https://pgexperts.com/)
![img](https://copm.s3.amazonaws.com/27676a9c.png)

PGX的开源专家提供解决数据库问题，加速现有应用程序，重构基础架构和开发新应用程序所需的数据库和应用程序技能。

`POSTGRESQL EXPERTS, INC.` **赞助商**

## [发掘隐藏的PostgreSQL11宝藏](https://www.cybertec-postgresql.com/en/unearthing-some-hidden-postgresql-11-gems/)
Postgres 11仅仅发布了三个月，所以仍然需要时间来挖掘它的所有新功能。Kaarel Moppel就是这么做的，并且分享了一些他感兴趣的部分。

`KAAREL MOPPEL`

## [ 2019年PostgresConf CFP延长至周五](https://blog.pgconf.us/2019/01/cfp-extended-until-friday.html)
2019年的PostgresConf US将在今年3月在纽约举行，到目前为止已有170多个提案。 但是，大会渴望得到更多提案，如果你想加入这个聚会，截止日是本周五（1月18日）。

`JOSHUA DRAKE`

## [亚马逊的DocumentDB真的是Postgres吗？](https://www.enterprisedb.com/blog/documentdb-really-postgresql)
亚马逊刚刚宣布了兼容MongoDB的文档数据库DocumentDB，但是有一些提示显示它实际上是由Postgres驱动...

`KEN RUGG`

## [使用新的Azure数据库进行PostgreSQL功能的性能故障排除](https://azure.microsoft.com/en-us/blog/performance-troubleshooting-using-new-azure-database-for-postgresql-features/)
如果您在Azure上使用Postgres，这篇文章可能有所帮助。

`HARINI GUPTA (MICROSOFT)`

## [一个包括应用程序，连接池和PostgreSQL的安全系统——为LDAP提供案例](https://severalnines.com/blog/one-security-system-application-connection-pooling-and-postgresql-case-ldap)

`ACHILLEAS MANTZIOS`

## [pgDash对PostgreSQL的诊断和监控](https://pgdash.io/features)
将PostgreSQL性能最大化，并深入了解PostgreSQL部署。查看诊断，监控核心功能，与您的团队共享。

`PGDASH` **赞助商**

## [Dimitri Fontaine对“掌握应用程序开发中的PostgreSQL”一书的回顾](https://medium.com/@shvetsovdm/mastering-postgresql-in-application-development-by-dimitri-fontaine-4378173e01dd)

`DMITRY SHVETSOV`

## [pgqr:Postgres的QR码生成扩展](https://abdulyadi.wordpress.com/2019/01/12/pgqr-a-qr-code-generator/)
我们仍在努力弄清楚为什么这个很有用，但如果你需要它，那你就需要这篇文章.. :-)

`ABDUL YADI`

# 本周提示

:information_source:
 
>找出哪些表需要额外的索引
>pg_stat_user_tables是一个出色的系统视图，可以向我们展示有关数据库中表的宝贵信息，并可用于诊断性能问题。last_autovacuum和n_dead_tup等vacuum统计信>息将显示是否存在未被vacuum的表，如果未执行HOT更新，则显示n_tup_hot_upd。
>但是，首先要考虑的是，是否存在需要新索引的表，因为这会对数据库的整体性能产生重大影响：
>
>```SQL
>SELECT relname,  
>    seq_scan,  
>    seq_tup_read,  
>    idx_scan  
>FROM pg_stat_user_tables  
>WHERE seq_scan > 0  
>ORDER BY 3 DESC LIMIT 10; 
>```
>
>这个简单的查询将有助于突显重顺序扫描的表以及需要添加索引的潜在候选者。
>通过查看seq_scan结果，您可以准确地看到表上发生了多少次顺序扫描。然后查看seq_tup_read，您可以看到在这些扫描期间多少个元组正在被读取。如果某些表上的>数字明显更高，则可能非常需要一些额外的索引。
>这个“本周提示”由Peter Tormey @ SoFi 提供，并由[strongDM](https://www.strongdm.com/?utm_source&utm_medium=email&utm_campaign=2019-01-16%20-%20%5BNL%5D%20-%20%5BSchD%5D%20-%20%5BSDM%5D%20-%20PGW-TIP-JAN)赞助。
>SoFi依靠strongDM来管理和保护对数据库和服务器的访问。[了解有关strongDM的更多信息](https://www.strongdm.com/?utm_source&utm_medium=email&utm_campaign=2019-01-16%20-%20%5BNL%5D%20-%20%5BSchD%5D%20-%20%5BSDM%5D%20-%20PGW-TIP-JAN)

**如果您对“本周提示”有任何想法，[请联系我们](https://cooperpress.typeform.com/to/bTSq7v) —— 一经采用，我们将为您的“提示”支付50美元。**
