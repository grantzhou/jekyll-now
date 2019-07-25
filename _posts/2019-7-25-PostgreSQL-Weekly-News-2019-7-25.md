---
layout: post
title: PostgreSQL 每周新闻 2019-7-25
---

### PostgreSQL每周新闻#315 - 2019年7月24日

![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)

备注：[英文原文地址](https://postgresweekly.com/issues/315)

![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/v1563921627/twah9uwlfbt4ve2bn8s1.png)

## [待命生产：衡量世界第二大分类网站](https://medium.com/avitotech/standby-in-production-scaling-application-in-second-largest-classified-site-in-the-world-97a79a1929de)

阿维托是俄罗斯最大的分类广告网站，它在100个Postgres节点上存储了20TB的数据。这里带你从幕后详细地了解他们的Postgres高可用性设置。

`KONSTANTIN EVTEEV`

## [使用pg_qualstats和HypoPG的自动索引建议](https://www.percona.com/blog/2019/07/22/automatic-index-recommendations-in-postgresql-using-pg_qualstats-and-hypopg/)

[HypoPG](https://github.com/HypoPG/hypopg)是Postgres的扩展，用于创建“假想索引”，本质上是虚拟索引，您可以使用它来测试某个索引是否能够提前改进查询。本文通过自动查找值得创建的索引，使事务推进到下一步。

`AVINASH VALLARAPU`

## [Chef的首席技术官选择StrongDM](https://www.strongdm.com/postgres-weekly/?utm_source=PGWeekly&utm_medium=email&utm_campaign=2019-07-22%20-%20%5BSELF%5D%20-%20%5BSDM%5D%20-%20%5BMID%5D)

Adam Jacob说:“StrongDM消除了终端用户访问他们需要的系统时发生的摩擦。”零信任访问任何数据库、服务器或k8集群。[点击这里](https://www.strongdm.com/postgres-weekly/?utm_source=PGWeekly&utm_medium=email&utm_campaign=2019-07-22%20-%20%5BSELF%5D%20-%20%5BSDM%5D%20-%20%5BMID%5D%20)免费试用。

![img](https://copm.s3.amazonaws.com/975a5f60.png)

`STRONGDM`**赞助商**

## [不要忘记BRIN索引的好处](https://www.percona.com/blog/2019/07/16/brin-index-for-postgresql-dont-forget-the-benefits/)。

BRIN索引(它提供了一种有效的方法，可以将索引值分组为“范围”)在Postgres 9.5中引入，并具有一些特定的用例。这篇文章测试了一种确实可以提供帮助的情况。

`JOBIN AUGUSTINE`

## [使用SQL对随机结果排序](https://vladmihalcea.com/sql-order-by-random/)

这篇文章介绍了如何使用ORDER以几种特定于数据库的方式对行进行随机排序，包括Postgres。

`VLAD MIHALCEA`

## [在psql脚本中检查Postgres的版本](https://fluca1978.github.io/2019/07/18/CheckPostgreSQLVersionInScripts.html)

假设您想根据正在运行的Postgres版本运行不同的代码。你可以的!

`LUCA FERRARI`

## [献给平均和高级（甚至更多）用户的Postgres技巧](https://www.citusdata.com/blog/2019/07/17/postgres-tips-for-average-and-power-user/)

希望你喜欢我们今年在《Postgres Weekly》中收录的各种“本周要诀”，但在这里，Craig Kerstiens还会发掘出更多:-)

`CRAIG KERSTIENS`

## [使用Datadog主动监控PostgreSQL性能](https://www.datadoghq.com/postgres-monitoring/?utm_source=Advertisement&utm_medium=CooperPress&utm_campaign=CooperPress-PostgresWeeklyS)

通过对延迟峰值、错误、异常等发出可操作的警报来改进PostgreSQL性能。智能监控与Datadog ——免费使用。

`DATADOG`**赞助商**

## [如何复制函数和存储过程？](https://www.cybertec-postgresql.com/en/postgresql-how-are-functions-and-stored-procedures-replicated/)

简要介绍Postgres是如何存储函数和过程的，以及这些函数和过程是如何被复制的。

`HANS-JÜRGEN SCHÖNIG`

## [Postgres Docker Containers的证书认证配方](https://info.crunchydata.com/blog/ssl-certificate-authentication-postgresql-docker-containers)

了解如何使用一个简单的Docker Containers配方设置基于PostgreSQL证书的认证。

`JONATHAN S. KATZ`

## ['Mysterious'backend_flush_after配置设置](https://www.cybertec-postgresql.com/en/the-mysterious-backend_flush_after-configuration-setting/)

这是一个非常特别的设置，适用于那些希望获得一些额外性能的服务器操作人员(并且仅适用于那些使用Linux的操作人员)。

`KAAREL MOPPEL`

## [配置pgBackRest以使用Amazon S3](https://pgstef.github.io/2019/07/19/pgbackrest_s3_configuration.html)

[pgBackRest](https://pgbackrest.org/)是一个功能强大的备份和恢复工具，可以配置以使用AWS S3。

`STEFAN FERCOT`

# 💡本周提示

由Gremlin提供支持

### 使用ROLLUP获取聚合的整体结果行

如果要将结果分组并聚合在一起，则使用GROUP BY作为一个常用方法，但ROLLUP是少数条款中的一个，它可以帮助您通过让多个集合在一个单元中将事物转移到另一个维度查询。

这是现场最佳演示的功能，所以让我们创建一个表并加载一些示例数据。不同年份不同足球队的得分数：

```
  CREATE TABLE goals (
  team TEXT, year INT, goals INT);

INSERT INTO goals VALUES
  ('USA', 2010, 5), ('USA', 2011, 3),
  ('USA', 2012, 12), ('ENG', 2010, 17),
  ('ENG', 2011, 9), ('ENG', 2012, 11);  
```

如果我们想要获得每队每年平均进球数，我们可以这样做：

```
SELECT team, ROUND(AVG(goals))
  FROM goals GROUP BY team;
```

但是，假设我们不仅希望按团队分组，还希望通过整体表格（即没有专栏）来获得总体平均目标数量。 我们可以这样做：

```
SELECT team, ROUND(AVG(goals))
  FROM goals GROUP BY ROLLUP(team);
```

这给我们带来了如下结果：

```
  team | round
--------------
   ENG | 12
   USA | 7
 (null)| 10
```

除此之外还有更多内容，所以请享受[本教程](http://www.postgresqltutorial.com/postgresql-rollup/)来了解更多信息。

本周的提示由[Gremlin](https://www.gremlin.com/?utm_medium=cpm&utm_source=PostgresWeekly&utm_content=20190724&utm_campaign=2019_Cooperpress)提供给您，这个平台可以通过运行合理的Chaos Engineering实验来帮助您构建更具弹性的软件。 更多信息请访问[gremlin.com](https://www.gremlin.com/?utm_medium=cpm&utm_source=PostgresWeekly&utm_content=20190724&utm_campaign=2019_Cooperpress)。

🗓  **即将举办的Postgres活动**  

• [PGConf.Brasil 2019](https://www.pgconf.com.br/2019/en/)(8月1-3日，圣保罗)——为期三天的会议，包括讲座，教程，课程和闪电讲座。

• [PGDay Austria 2019](https://pgday.at/en/)（9月6日， 维纳·纽斯塔特，奥地利）

• [PostgreSQL Conference Asia 2019](https://2019.pgconf.asia/)（9月8-11日，巴厘岛，印度尼西亚）

• [PostgresConf South Africa 2019](https://postgresconf.org/conferences/SouthAfrica2019)（10月8-9日，约翰内斯堡）——提供给使用Postgres的数据库管理和开发人员互相了解的机会。