---
layout: post
title: PostgreSQL 每周新闻 2019-12-18
---
### PostgreSQL每周新闻#336 - 2019年12月18日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)
备注：[英文原文地址](https://postgresweekly.com/issues/336)
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/v1576621869/fbx7orxszxhxlwdbiif6.png)

####  🏆 2019年最火热的6个Postgres链接



## [1.避免在Postgres内做的事情](https://postgresweekly.com/link/81499/web)

这是Postgres维基上的一个页面，在2019年占据了#1的位置！它试图总结使用Postgres时的各种“常见错误”，如“不使用char（n）”和“不使用serial”。他们中的一些人有点固执己见，但有理由支持。

`Postgres Wiki `

## [2.如何提高COUNT（*）的性能](https://postgresweekly.com/link/81500/web)
使用count（*）可能会导致性能问题。本文探讨了各种选项，使计数行更快使用近似和其他技巧。

`Cybertec `

## [3.面向视觉倾斜的PostgreSQL工具](https://postgresweekly.com/link/81502/web)
Rob Conery专业的回应了一位SQL Server DBA对Postgres工具的批评。

`Rob Conery `

## [4.一些Postgres最佳实践](https://postgresweekly.com/link/81504/web)
对主键使用BIGINT或UUID，保持凭据旋转，使用连接池。

`Kenneth Reitz (DigitalOcean) `

## [5.Postgres的JSON功能概述](https://postgresweekly.com/link/81505/web)
多年来，Postgres的JSON功能不断改进，虽然本文在1月份非常流行，但随着10月份发布的Postgres 12中引入JSONPath支持（PDF），情况在2019年持续改善。

`Severalnines `

## [6. PostgreSQL 12发布](https://postgresweekly.com/link/81507/web)
这被作放在了第6的位置，因为Postgres12的发布不是一件意外的事情，但这无疑是今年Postgres世界上最大的事件。关键的增强包括SQL/JSON支持（本PDF中有更多内容）、生成的列和显著的性能改进（特别是索引和分区表）。Postgres周刊326期有一个非常好的总结。


`PostgreSQL Global Development Group `
# 💡本周提示


索引可以占用比您想象的多得多的空间。有好几次我在表中添加了索引以加快速度，并对磁盘使用量的快速增长感到震惊。虽然索引是围绕列组织的，但并不是每一行都需要包含在索引中，“部分索引”提供了一个解决方案。


假设您在电子商务应用程序的数据库中有一个很大的orders表，它包含应用程序中制定的每种类型的订单，甚至那些从未完成的订单。您的应用程序有一个搜索功能，可以根据orders表中的列进行筛选，但您几乎不需要将所有未完成的订单都包含在该列的索引中。


在创建索引时使用WHERE子句可创建“部分索引”，该索引仅包含与提供的谓词匹配的行。下面是一个基于上述订单场景的简单示例：


```
CREATE INDEX orders_completed_user_id
  ON orders (user_id)
  WHERE completed IS TRUE;
```


不可否认，在这样的场景中保存的数据很小（用户id可能只是一个整数），但是对于文本列或多列索引，最终的节省可能是巨大的。


PostgreSQL文档有一个关于部分索引的很棒的页面，如果您想了解更多信息，请提供更多示例。


**🗓即将举办的Postgres活动**
- [PgDay SF](https://postgresweekly.com/link/81512/web)（1月21日在旧金山）
- [PgDay FOSDEM](https://postgresweekly.com/link/81513/web)（1月31日，比利时布鲁塞尔）
- [PgConf.Russia](https://postgresweekly.com/link/81514/web)（2月3日至5日，俄罗斯莫斯科）
- [PgConf India](https://postgresweekly.com/link/81515/web)（2月26日至28日，印度马哈拉施特拉邦班加罗鲁）
- [Nordic PgDay 2020](https://postgresweekly.com/link/81516/web)（3月24日在芬兰赫尔辛基）
- [pgDay Paris 2020](https://postgresweekly.com/link/81517/web)（3月26日，法国巴黎）
- [Swiss PGDay 2020](https://postgresweekly.com/link/81518/web)（6月18日至19日，瑞士）
