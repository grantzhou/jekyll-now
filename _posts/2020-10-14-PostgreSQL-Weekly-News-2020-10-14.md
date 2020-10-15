---
layout: post
title: PostgreSQL 每周新闻 2020-10-14
---
### PostgreSQL每周新闻#377 - 2020年10月14日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)
备注：[英文原文地址](https://postgresweekly.com/issues/377)
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/v1602675284/fihmm34fouqnzxajl8p2.jpg)

## [利用pg_squeeze优化存储](https://postgresweekly.com/link/96656/web)
一个扩展，它可以定期、自动和透明地修复超过“膨胀阈值”的表。”再也不需要VACUUM FULL,pg_squeeze就可以了。”

`Hans-Jürgen Schönig `

## [分析连接可扩展性的限制](https://postgresweekly.com/link/96657/web)
Postgres可以处理数千个连接，但是大量并发客户端并不是它的强项之一。这篇文章着眼于如何长期改善这一状况。

`Andres Freund `

## [postgres12中全文检索的状态](https://postgresweekly.com/link/96659/web)
▶音频不是很好，但这是一个伟大的入门，不同的文本搜索技术在Postgres从绝对的基础（例如，LIKE和regexp_match）开始，并转到Postgres的full fat FTS功能。

`Jimmy Angelakos `

## [论EDB第二季度采购对社区的影响](https://postgresweekly.com/link/96660/web)
上周，我们提到了EDB（以前是EnterpriseDB）收购了2ndQuadrant，这使得它在Postgres领域有点重量级，而Bruce考虑了风险，尤其是Postgres的核心团队（包括Bruce）现在有一半来自这家公司。


`Bruce Momjian `
## [使用Postgres和Python发布200万篇古代Usenet帖子](https://postgresweekly.com/link/96668/web)
Usenet是一个迷人的分布式讨论系统，它的全盛时期是在80年代和90年代，它有各种各样的帖子存档（比如有人在1989年问Postgres是什么！）。

`Jozef Jarosciak `

## [将行级别安全性扩展到组角色](https://postgresweekly.com/link/96674/web)
行级别的安全性允许您为所选用户向所选行授予权限，但是用户组或“角色”又如何呢？


`Elephant Tamer `
## [面向开发人员的Postgres监控：DBA基础知识](https://postgresweekly.com/link/96676/web)
在管理Postgres数据库时，可以查看几个统计信息。pgmonitor是一种可以用来跟踪这些东西的工具。


`Jonathan S. Katz `
## [测量Postgres连接的内存开销](https://postgresweekly.com/link/96679/web)
这与上面介绍的连接可伸缩性post直接相关，但可能会引起单独的兴趣。


`Andres Freund `
## [一些查询缓存和负载平衡工具](https://postgresweekly.com/link/96681/web)
总结了一些可用于Postgres的查询缓存和负载平衡选项，包括pgpool II、Apache insert、Heimdall Data、HAProxy和Bucardo。


`Viorel Tabara `
## [什么是神话般的零停机时间数据库迁移到云端？](https://postgresweekly.com/link/96682/web)
加入我们的CIO领导的小组讨论会，讨论问题和风险以及简化体验的可用技术。


`ScaleArc `
## [Postgres模式下的多重租赁：关键概念解释](https://postgresweekly.com/link/96683/web)
如果你对这个话题感兴趣，他们的《Postgres Schema Multitenancy》一文也可能有用。


`Tomasz Wróbel `
## [pg_auto_failover 1.4的新增功能](https://postgresweekly.com/link/96685/web)
pg_auto_failover是一个开源扩展，它管理Postgres集群的自动故障转移。这个版本发给我的时候附带了一个注释：“在这个新的1.4版本中，Dimitri添加了多个备用支持，这真是一件大事。”


`Dimitri Fontaine `
# 💡本周提示


**🗓即将举办的Postgres活动**
