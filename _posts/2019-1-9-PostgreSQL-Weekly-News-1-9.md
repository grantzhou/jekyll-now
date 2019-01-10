---
layout: post
title: PostgreSQL 每周新闻 2019-1-9
---

### PostgreSQL每周新闻#287 - 2019年1月9日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)

备注：[英文原文地址](https://postgresweekly.com/issues/287)

我们回来了！我们希望您度过了愉快的假期，并期待今年的Postgres有尽可能多的发展。
在休息期间Postgres社区没有发生巨大的新闻（所以没有新版本升级）但是我们已经推出了新的"每周提示"版块-见周报底部。感谢那些提交了想法的人，我们很快就会与您联系，如果您想提交自己的想法，[请联系我们](https://cooperpress.typeform.com/to/bTSq7v)。

🐘编辑 Peter Cooper 和 Craig Kerstiens

## [PostgreSQL获得DB-Engine2018年度DBMS](https://db-engines.com/en/blog_post/79)
DB-Engines是数据库系统受欢迎程度的热门排名，他们连续第二年将其“年度DBMS”奖项授予Postgres。MongoDB和Redis分获二、三名。

`PAUL ANDLINGER,MATTHIAS GELBMANN`

## [《卫报》:再见Mongo,你好Postgres](https://www.theguardian.com/info/2018/nov/30/bye-bye-mongo-hello-postgres)
四月份，英国著名报纸《卫报》（The Guardian）关闭了他们的MongoDB集群，并完成了迁移到Amazon RDS上PostgreSQL的过程。下面是完整的故事。

`PHILIP MCMAHON`

## ▶[Postgres会永远存在吗？](https://www.youtube.com/watch?v=sc1EIqwoJLY)
![youtube_image](https://copm.s3.amazonaws.com/11530c7a.png)与EDB团队一起讨论创新来保持Postgres的活力。

`ENTERPRISEDB` **赞助商**

## [Postgres的即时编译（JIT）概述](https://severalnines.com/blog/overview-just-time-compilation-jit-postgresql)
即时（JIT）编译是在运行时将解释代码编译为更快的本机代码以提高重复性能的过程。Postgres添加JIT功能到Postgres 11中，但由于并非所有工作负载都能从中受益，因此默认情况下不会启用它。

`VIOREL TABARA`

## [8个Postgres的匿名化策略](http://blog.taadeem.net///english/2019/01/03/8_anonymization_strategies_with_postgres)
GDPR可能看起来引起了2018年的恐慌，但数据系统中对隐私性的改善需求只会不断增加，因此考虑如何对数据进行匿名化是一个好主意。

`DAMIEN CLOCHARD`

## [SQL的乐趣：Self Join](https://www.citusdata.com/blog/2019/01/02/fun-with-sql-self-joins/)
Self Join在SQL中是一个简单但偶尔会提供便利的概念，它允许您在一行中将某个关系定义到该表中的另一行时将表连接到自身。

`CRAIG KERSTIENS`

## [Postgres的14种身份验证方法](https://momjian.us/main/blogs/pgblog/2019.html#January_2_2019)
你知道它支持这么多吗？ 它们有六种类型。

`BRUCE MOMJIAN`

## [处理Stuck TransactionIDs案例](http://richyen.com/replication/postgres/2019/01/08/zombie_transactions.html)
如果您在日志中看到“最早的xmin已经过去”和“很快就会关闭打开的事务以避免出现问题”，该怎么办？

`RICHARD YEN`

## [完整的Cloud SQL免费教程](https://www.qwiklabs.com/quests/52?locale=en)
创建实例和查询数据。Cloud SQL将为您提供开始集成此服务所需的知识。

`GOOGLE CLOUD` **赞助商**

## [为Postgres开发配置Vim](https://wiki.postgresql.org/wiki/Configuring_vim_for_postgres_development)
Postgres官方wiki上的新页面。

`NIKOLAY SHAPLOV`

## [HypoPG 2.0 Beta版](https://github.com/HypoPG/hypopg)
HypoPG是一个Postgres的扩展，支持假设索引和推荐。2.0版本现在在这里，增加了对Postgres 10及更高版本中假设分区的支持。

`POSTGRESQL GLOBAL DEVELOPMENT GROUP`

# 本周提示
欢迎阅读我们2019年的最新版块 — 便利的每周Postgres相关技巧。 我们从一些简单的东西开始 — 一种查看Postgres服务器设置的方法，这比通过postgresql.conf进行查看更好。
首先，进入psql或任何可以进行查询的客户端。 然后运行此查询：

SHOW ALL;

你会得到一个（非常长的）结果，如下所示：
![image](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/gt3zmrgglnbkhjwdqowq.jpg)
您不仅可以查看设置名称及其值，还可以查看设置的描述或用途。

“本周提示”由Citus Data赞助,Citus Data是可靠的Postgres的创建者，旨在不断发展。在Citus Data博客中可以[了解更多](https://www.citusdata.com/blog/?utm_source=PG_Weekly&utm_medium=email&utm_campaign=sponsor_blog)。

如果您对“本周提示”有任何想法，[请联系我们](https://cooperpress.typeform.com/to/bTSq7v) - 一经采用，我们将为您的“提示”支付50美元。

