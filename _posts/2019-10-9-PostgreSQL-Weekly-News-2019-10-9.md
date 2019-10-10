---
layout: post
title: PostgreSQL 每周新闻 2019-10-9
---
### PostgreSQL每周新闻#326 - 2019年10月9日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)
备注：[英文原文地址](https://postgresweekly.com/issues/326)
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/v1570535120/f7ksfjt0klgx0oyoom09.jpg)
## [PostgreSQL 12发布](https://postgresweekly.com/link/78166/web)
从Postgres11发布到Postrges12只用了一年的时间，我们的Postgres又向前迈出了一大步。主要的增强包括sql/json支持、生成的列和显著的性能改进（特别是索引和分区表）。


`PostgreSQL Global Development Group `
## [postgres 12中生成的列](https://postgresweekly.com/link/78168/web)
“生成列有点像视图，但他是列。” 虽然一些限制，其本质是基于其他列的列。这里有一个简洁的示例。


`RapidLoop `
## [免费网络研讨会：使用simon riggs学习postgresql分区](https://postgresweekly.com/link/78169/web)
概述postgresql分区特性&它们如何提高大数据库的性能。学习最近对分区和并行性的改进，探索特定的用例，并探索即将到来的特性。

`2ndQuadrant PostgreSQL Webinars `



## 🐘 **Postgres 12 概述**

在过去的几个月里，我们链接到了各种各样的帖子，涵盖了新的postgres 12特性。这里有一个概述：

1. [Bruce Momijan的PDF，涵盖了Postgres12主要的新功能](https://postgresweekly.com/link/78170/web)
2. [仅仅升级到postgres 12就可以在不做任何其他事情的情况下提高性能](https://info.crunchydata.com/blog/just-upgrade-how-postgresql-12-can-improve-your-performance)
3. [Postgres12使得分区更快](https://postgresweekly.com/link/78172/web)
4. [vacuum的改进](https://postgresweekly.com/link/78173/web)
5. [分区表的改进](https://postgresweekly.com/link/78174/web)
6. [COPY和批量加载数据的改进](https://postgresweekly.com/link/78175/web)
7. [几个更新Postgres版本的方法](https://www.cybertec-postgresql.com/en/a-primer-on-postgresql-upgrade-methods/)
8. [sql/json（Postgres12中支持）与jsquery的比较](https://thombrown.blogspot.com/2019/07/jsquery-vs-sqljson.html)
9. [sql/json路径](https://paquier.xyz/postgresql-2/postgres-12-jsonpath/)



## [使用调试器跟踪查询处理内部](https://postgresweekly.com/link/78179/web)

这是一个SQL查询调试的过程。不需要大家都精通这个过程，但如果你账务了这个技能，会带来很多的便利性。


`Cary Huang `
## [高可用PostgreSQL使关键应用程序保持运行](https://postgresweekly.com/link/78180/web)
利用可信的开源软件确保PostgreSQL数据始终可用。


`Crunchy Data `
## [PostgreSQL 12中的流复制配置更改](https://postgresweekly.com/link/78181/web)
复制配置设置已经存储在一个特殊的文件recovery.conf中，但在postgres 12中，这些设置已经转换为普通的postgres配置设置，因此现在可以在postgresql.conf或alter system中进行管理。


`Ian Barwick `
## [Postgis 3.0.0发布候选1](https://postgresweekly.com/link/78182/web)
上周我们链接到了beta版，现在流行的postgres地理空间数据扩展已经在rc1上发布，最终版本马上发布。


`PostGIS Developers `
# 💡本周提示

**psql中查询的快捷方式/变量**

如果您在psql中花了一些时间来处理查询、进行一些优化或以其他方式处理数据库，您可能会发现自己一遍又一遍地键入相同的内容，例如在查询之前放置explain analyze，以便查看它们的查询计划。psql允许您定义“变量”，在查询中用作快捷方式，而不是每次都键入。



下面是一个使用explain analyze的例子：

```sql
\set ea 'EXPLAIN ANALYZE'
```

这将设置一个名为ea的变量来解释analyze，它可以简单地如下使用：

```
:ea SELECT * FROM [...rest of query here]
```

用：ea作为查询的前缀当然比select analyze简单得多。如果希望每次使用psql时都定义它们，也可以将它们添加到.psqlrc文件中



**🗓即将举办的Postgres活动**

- [pgDay Santiago](https://postgresweekly.com/link/77478/web)（10月29日，智利圣地亚哥）
- [PG Down Under 2019](https://postgresweekly.com/link/77479/web)（11月15日，澳大利亚悉尼）-本年度澳大利亚邮政会议的第二次出游。
- [PgConf.Russia 2020](https://postgresweekly.com/link/78187/web)(2020年2月3～5日，俄罗斯莫斯科) -在三个同步的环节中进行为期一天的教程和为期两天的讲座
- [PGConf India 2020](https://pgconf.in/conferences/pgconfin2020)(2020年2月26~28日， Bengaluru, Maharashtra, India) 

