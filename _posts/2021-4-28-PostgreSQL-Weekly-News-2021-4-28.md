---
layout: post
title: PostgreSQL 每周新闻 2021-4-28
---
### PostgreSQL每周新闻#403 - 2021年4月28日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)
备注：[英文原文地址](https://postgresweekly.com/issues/403)
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/mpmyll9qnwg4j5kyudqe.jpg)
## [了解僵局](https://postgresweekly.com/link/106997/web)
僵局实际上是更直接的演示之一。从本质上讲，这是两个事务互相等待对方放弃锁的时候，出现了22类问题。


`Hans-Jürgen Schönig `
## [pgvector：Postgres的向量相似性搜索扩展](https://postgresweekly.com/link/106999/web)
支持L2距离，内积和余弦距离。


`Andrew Kane `
## [蟑螂大学：学习构建云原生应用程序](https://postgresweekly.com/link/107000/web)
蟑螂大学是一个免费的在线学习平台，您将在其中获得分布式数据库技能和现代应用程序开发经验（对简历有用的技能😉）。


`Cockroach Labs `
## [何时使用NUMERIC/DECIMAL与其他数字类型进行比较](https://postgresweekly.com/link/107001/web)
对于希望尽可能提高性能的Postgres用户而言，管理行的每个字节的布局和使用可能是值得的，数字类型就是一个很好的例子。（上周的“每周技巧”也涉及到这一点。）


`David Youatt `
## [您可以从pl / PgSQL触发器中的动态列中获取值吗？](https://postgresweekly.com/link/107002/web)
Hubert演示了一种解决方法（需要付费）。


`Hubert depesz Lubaczewski `
## [集合操作入门](https://postgresweekly.com/link/107003/web)
例如，UNION用于将结果集放在一起，并且INTERSECT仅返回多个SELECT结果集之间共有的行。


`Paul Odhiambo `
## [从CHAR（1）迁移到Postgres时进行布尔转换](https://postgresweekly.com/link/107004/web)
您知道Oracle数据库没有布尔类型吗？如果您正在考虑从Oracle到Postgres的迁移，那么您可能会这样做，这是从CHAR(1)方法到布尔型的迁移方法。


`Dileep Kumar `
## [散列索引的内部原理](https://postgresweekly.com/link/107005/web)
 B树是Postgres中最流行的索引类型，而散列索引实际上在文档中“被淘汰”。Hamid快速浏览了散列索引的工作原理，并揭示了为什么它们仍有很大的改进空间。


`Hamid Akhtar `
## [[指南]关于开发人员生产率指标的真相](https://postgresweekly.com/link/107007/web)
您需要了解的内容，可以避免为绩效评估提供武器指标，而使用它们来加快发布速度。


`Sleuth `
## [关于数据库软件包](https://postgresweekly.com/link/107008/web)
这里没有优势，但Bruce考虑商业数据库供应商如何提供“完整软件包”，但是对于Postgres，您需要权衡各种提供商的产品。Postgres项目本身是否应该提供更多？


`Bruce Momjian `
# 💡本周提示


**🗓即将举办的Postgres活动**
