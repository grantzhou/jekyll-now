---
layout: post
title: PostgreSQL 每周新闻 2021-3-17
---
### PostgreSQL每周新闻#397 - 2021年3月17日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)
备注：[英文原文地址](https://postgresweekly.com/issues/397)
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/xkr5yf16lq768c9nf1nq.jpg)
## [用PostGIS和pgRouting解决旅行商问题](https://postgresweekly.com/link/104731/web)
旅行商问题是在各个点之间寻找路径的问题，每个点仅访问一次且距离尽可能短。 这篇文章使用pgRouting的扩展程序解决了PostGIS支持的Postgres数据库中的问题。


`Florian Nadler `
## [Amazon为Aurora提供了基于ARM的实例](https://postgresweekly.com/link/104734/web)
AWS Graviton2 处理器是基于ARM的CPU，由AWS自行定制构建，并且似乎以更低的成本提供了更高的性能（如Apple和其新的M1芯片）。 该公告为Amazon Aurora PostgreSQL（和MySQL）用户带来了性能和成本方面的改进。


`Amazon Web Services `
## [免费电子书：用Postgres在Rails中高效搜索](https://postgresweekly.com/link/104735/web)
将搜索查询的速度从几秒提高到几毫秒，并了解精确匹配，trigram，ILIKE和全文本搜索。


`pganalyze `
## [能否降低带时间的 auto_explain的开销？](https://postgresweekly.com/link/104736/web)
auto_explain是一个Postgres模块，用于记录运行缓慢的查询的执行计划-虽然它有一些开销，但是它是否真的是个问题，并且可以减轻吗？


`Michael Christofides `
## [以报告为目的建立一个Postgres支持的“数据湖”](https://postgresweekly.com/link/104738/web)
大多数公司都制定数据驱动的决策并查询数据仓库（或数据结构不那么正式的“湖”），这是十分普遍的。 这个故事涵盖了一家公司如何以有趣的方式使用Postgres和FDW来达成这个目的。


`Paul Bonaud `
## [优化Postgres读写性能的基本实践](https://postgresweekly.com/link/104739/web)
需要考虑的一些基本技术和速度优化“规则”。

`Michael Aboagye `

## [在Docker中运行Postgres-为什么和怎么做？](https://postgresweekly.com/link/104740/web)
Docker简介以及是否应该在Docker容器中运行生产Postgres工作负载。


`Kaarel Moppel `
## [使用Citus开源Shard Rebalancer扩展Postgres](https://postgresweekly.com/link/104741/web)
上周的citus10发布包括其shard rebalancer的开源，这是Citus优化跨不同节点拆分/分片的表的关键部分。


`Jelte Fennema `
## [Postgres与MySQL的性能差异](https://postgresweekly.com/link/104743/web)


`Blessing Krofegha `
## [调整Postgres数据库以应对高写负载](https://postgresweekly.com/link/104744/web)


`Tom Swartz `
## [PgHero 2.8：Postgres的性能Dashboard](https://postgresweekly.com/link/104745/web)
在Ruby中（在Instacart中使用），可以查看基本的性能统计信息，包括实时查询、维护状态和连接。

`Andrew Kane `

## [用Nagios和Checkmk监控Postgres](https://postgresweekly.com/link/104746/web)
以RHEL / CentOS为重点的教程，但是它是一个简洁的设置。 Checkmk是位于Nagios上方的工具，可以提供一个更好的界面。


`Hamid Akhtar `
## [在Postgres之上构建内部应用程序（更快）](https://postgresweekly.com/link/104748/web)
构建内部应用程序，而不需要那些平凡乏味的东西（与UI库搏斗，或者将数据源和api拼凑在一起）。


`Retool `
## [SQLBoiler4.5：生成一个根据您的数据库模式定制的Go ORM](https://postgresweekly.com/link/104749/web)
其思想是首先在数据库级别创建模式，然后根据实际设计查询模式并为Go生成ORM代码。

`Volatile Technologies Inc. `

## [Orafce3.15.0发布：Oracle数据库函数的Postgres实现](https://postgresweekly.com/link/104750/web)


`Pavel Stěhule `
# 💡本周提示


对于使用SQLAlchemy ORM框架的Python开发人员，可以让数据库服务器在创建映射类时自动生成UUID列。


这很有价值，因为它使您不必使用应用程序库。使用server_default参数并调用gen_random_uuid（）函数：


```
class Account(Base):
    """The Account class corresponds to the "accounts" database table.
    """
    __tablename__ = 'accounts'
    id = Column(UUIDtype, server_default=text("gen_random_uuid()", primary_key=True)
    balance = Column(Integer)
```


这个Column.server_default参数可用于调用任何数据库函数来设置列的默认值。


**🗓即将举办的Postgres活动**
