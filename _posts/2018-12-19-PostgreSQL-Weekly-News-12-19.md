---
layout: post
title: PostgreSQL 每周新闻 2018-12-19
---

### PostgreSQL每周新闻 #286 - 2018年12月19日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)
![_config.yml](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/duggn4rj89kddgveevkq.jpg)

备注：[英文原文地址](https://postgresweekly.com/issues/286)

这一年对于Postgres来说是多么美好的一年！PostgreSQL 11的发布是明显的亮点，但也有很多很棒的教程和工具我们必须享受。
本周我们将从通常的每周新闻中休息一下，来涵盖2018年的顶级项目，这些项目主要基于读者的点击次数。 我们将在新的一年早些时候恢复全速，祝你圣诞快乐，新年快乐。

_Peter Cooper和Craig Kerstiens，编者_

附： 我们明年将在周报中推出“本周提示”部分，并正在寻找（付费）提交的内容。 有关详细信息，请参阅此周报的最后部分。

## [2018年Postgres 11大发布的主要特点](http://momjian.us/main/writings/pgsql/features.pdf)

Bruce保留了一个受欢迎的幻灯片，涵盖了最新版Postgres中的功能，他对Postgres 11的综述是我们今年最受欢迎的链接。 Bruce一如既往的出色工作。

`BRUCE MOMJIAN`

## [Postgres的隐藏宝石](http://www.craigkerstiens.com/2018/01/31/postgres-hidden-gems/)
一系列对这个问题的回答：_“你希望更多人知道的你最喜欢的Postgres隐藏的宝石是什么？”_

`CRAIG KERSTIENS`

## [了解Google Cloud SQL对于PostgreSQL的高可用性](https://cloudplatformonline.com/2018-Cloud-SQL-for-PostgreSQL.html?utm_source=cooper&utm_medium=email&utm_campaign=FY18-Q4-americas-other-email-wd-postgresql&utm_content=promo)
下载本指南,了解Cloud SQL如何通过持续运行状况检查，跨区域的同步数据复制,自动故障转移和可伸缩性来优化和增强典型的PostgreSQL HA技术堆栈。

`GOOGLE CLOUD` *赞助商*

## [我最喜欢的Postgres查询及其重要性](https://severalnines.com/blog/my-favorite-postgresql-queries-and-why-they-matter)
作者发现的关于一个有趣的查询组合的有趣\引人入胜的探究，研究和学习。

`JOSHUA OTWELL`

## [PostgreSQL崩溃：对性能的影响是什么？](https://blog.2ndquadrant.com/postgresql-meltdown/)
还记得2018年初Spectre和Meltdown CPU漏洞的戏剧性吗？ Postgres最终没有受到太大影响。 很快就能看到对长期影响的正确回顾。

`2NDQUADRANT`

# 2018年最好的工具

## [PostgreSQL Anonymizer：屏蔽个人信息的工具](http://blog.taadeem.net///english/2018/10/29/Introducing-PostgreSQL-Anonymizer)
我们今年链接的最受欢迎的工具，也许不出所料，这是一个新的Postgres扩展，用于屏蔽或替换个人身份信息（PII），这有助于浏览适用于今年新实施的GDPR法规的内容。

`DAMIEN CLOCHARD`

## [为什么要升级PostgreSQL？这就是为什么](https://why-upgrade.depesz.com/show?from=11&to=11.1)
一个有用的工具，可以揭示从任何给定版本的Postgres升级的真正好处。例如：从9.3.2升级到11.1？ 该网站列出了所有的好处。

`HUBERT DEPESZ LUBACZEWSKI`

## [几分钟内在AWS云上按需部署EDB Postgres数据库](https://www.enterprisedb.com/edb-postgres-cds)

`EDB POSTGRES CLOUD DATABASE SERVICE` *赞助商*

## [Graphile：Postgres数据库的即时GraphQL API](https://www.graphile.org/postgraphile/)
自动发现表，列，关系，过程等，然后运行符合最佳实践的高性能安全GraphQL API服务器。

`BENJIE GILLAM`

## [使用pg_repack减少磁盘膨胀](https://reorg.github.io/pg_repack/)
用于从表和索引中删除“膨胀”而不保留独占锁的扩展。[Github Repo](https://github.com/reorg/pg_repack)

`KNUT INGVALD DIETZEL`

## [pgbedrock：声明性角色和权限管理工具](https://github.com/Squarespace/pgbedrock)
来自Squarespace的工具，用于从YAML编写的规范文件以声明方式管理Postgres集群的角色，角色成员资格，模式所有权和特权。

`SQUARESPACE INC.`

# 2018年最好的教程

## [Postgres中的物化视图和汇总表](https://www.citusdata.com/blog/2018/10/31/materialized-views-vs-rollup-tables/)
今年第二受欢迎的链接来自我们自己的Craig Kerstiens！物化视图通常用于使报告更快，但是另一种方法（汇总表）在提供相同的好处的同时具有一些优势。

`CRAIG KERSTIENS`

## [PostgreSQL Exercises](https://pgexercises.com/)
如果您正在寻找一种在假期练习SQL技能的方法，PG Exercises会提供一些很好的示例数据和练习来磨练您的技能。

`ALISDAIR OWENS`

## [三种数据库建模反模式](https://tapoueh.org/blog/2018/03/database-modelization-anti-patterns/)
查看一些经典的反模式：实体属性值，单个列中的多个值，以及如何使用UUID也可以是反模式。

`DIMITRI FONTAINE`

## [一些你可能没有尝试过的Postgres功能](https://pgdash.io/blog/postgres-features.html?h)
剧透:包括pub / sub，表继承，触发器，数组等。

`RAPIDLOOP`

## [在Postgres中选择除一列之外的所有列](https://blog.jooq.org/2018/05/14/selecting-all-columns-except-one-in-postgresql/)
Google的BigQuery具有EXCEPT和REPLACE关键字，用于在查询中删除或替换列结果。 这是在Postgres上模拟这样的功能。

`LUKAS EDER`

## 即将到来的2019年-本周提示
明年，我们将在周报中推出一个本周提示的新环节。 只是一些可以帮助您日常使用Postgres的东西，包括工具，SQL技术或是您都没有意识到的命令行选项。
有趣的部分是我们正在寻找提交内容，我们将为您提供50美元（通过PayPal），以便好好地编写和使用。
感兴趣吗？[请通过此提交表单联系](https://cooperpress.typeform.com/to/bTSq7v)。 如果你现在还不能完整地写出，可以告诉我们你的想法。如果我们感兴趣，我们会与你联系。

