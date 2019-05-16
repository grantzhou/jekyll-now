---
layout: post
title: PostgreSQL 每周新闻 2019-5-15
---

### PostgreSQL每周新闻#305 - 2019年5月15日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)

备注：[英文原文地址](https://postgresweekly.com/issues/305)

![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/v1557914353/gqytlwienctadmgcvky1.jpg)

## [如何尝试使用Postgres的前沿版本](https://www.depesz.com/2019/05/15/how-to-play-with-upcoming-unreleased-postgresql/)
我们经常链接关于Postgres即将推出的功能的有趣帖子，其中已经有许多功能被纳入项目的核心源代码。如果你想使用最新的Postgres实验版，应该怎么做呢？

`HUBERT DEPESZ LUBACZEWSKI`

## [Postgres 11.3,10.8,9.6.13,9.5.17和9.4.22发布](https://www.postgresql.org/about/news/1939/)
这些是针对bug修正的补丁级别发布，包括两个安全问题修复，一个缺陷——“运行PostgreSQL 11的用户可以通过对分区表执行特定的INSERT语句来读取服务器内存的任意字节。[更多信息](https://www.percona.com/blog/2019/05/13/postgresql-minor-versions-released-may-9-2019/)

`POSTGRESQL全球开发小组`

## [如果工程师需要访问数据库，你需要strongDM](https://www.strongdm.com/product/?utm_source=&utm_medium=email&utm_campaign=2019-04-24%20-%20%5BUSA%5D%20-%20%5BSchD%5D%20-%20%5BSDM%5D%20-%20%5BENT%5D%20-%20PGW)
![img](https://copm.s3.amazonaws.com/69ff4959.png)    
strongDM对全栈都有效。认真地讲，任何数据库，任何服务器，所有环境。[了解更多](https://www.strongdm.com/product/?utm_source=&utm_medium=email&utm_campaign=2019-04-24%20-%20%5BUSA%5D%20-%20%5BSchD%5D%20-%20%5BSDM%5D%20-%20%5BENT%5D%20-%20PGW)

`STRONGDM` **赞助商**

## [使用LibPostal进行快速匹配和脏地址匹配](https://info.crunchydata.com/blog/quick-and-dirty-address-matching-with-libpostal)
[libpostal](https://github.com/openvenues/libpostal)是一个有趣的库，用于解析和规范地址，您可以在自己的Postgres数据库中更轻松地比较和搜索地址。

`PAUL RAMSEY`

## [Postgres 12发行说明草稿](https://www.postgresql.org/docs/devel/release-12.html)
Bruce Momijan宣布他已经完成了Postgres 12发行说明的初稿，他们将持续更新，直到今年晚些时候的最终版本。它有点像装满未知物品的盒子，但[关于Postgres 12特性的这些PDF幻灯片](http://www.sai.msu.su/~megera/postgres/talks/pg12-stachka-2019.pdf)非常的详细。

`BRUCE MOMIJAN`

## [Postgres 12新功能：函数优化器支持](https://www.kdobson.net/2019/ultimate-postgresql-slug-function/)
我通常使用客户端应用进行函数优化，如这篇文章所示，为数据库实体创建规范化的“slug”可以很容易地引用Postgres函数。

`KESTER DOBSON`

## [使用S3将数据导入Amazon RDS上的Postgres](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/PostgreSQL.Procedural.Importing.html#USER_PostgreSQL.S3Import)
如何将存储在Amazon S3 bucket 中的数据导入Amazon RDS上托管的Postgres表中。

`AMAZON WEB SERVICES, INC.`

## [使用Datadog监控自定义PostgreSQL指标](https://www.datadoghq.com/postgres-monitoring/?utm_source=Advertisement&utm_medium=CooperPress&utm_campaign=CooperPress-PostgresWeeklyS)
同时查看数据库，工具和服务的实时指标。尝试使用Datadog进行监控。

`DATADOG ` **赞助商**

## [使用SQL Notebooks 进行Postgres数据库运行状况检查](https://azure.microsoft.com/en-us/blog/operationalizing-your-database-health-checks-using-sql-notebooks/)
了解Azure Data Studio（是的，我认为只能在Azure中使用）中用于创建交互式SQL 查询“笔记本”来监控Postgres安装的技术。


`PARIKSHIT SAVJANI (MICROSOFT)`

## [使用ClickHouse数据库改进Postgres的OLAP工作负载性能](https://www.percona.com/blog/2019/05/09/improving-olap-workload-performance-for-postgresql-with-clickhouse-database/)
[ClickHouse](https://clickhouse.yandex/)是一个开源的column-oriented DBMS，专注于快速生成分析数据报告。

`IBRAR AHMED`

## [Postgraphile：快速获取Postgres数据库的GraphQL API](https://github.com/graphile/postgraphile)
[最新版本（4.4.0）](https://github.com/graphile/postgraphile/releases/tag/v4.4.0)引入了对订阅和实时查询的支持。

`GRAPHILE`

# ![_config.yml]({{ site.baseurl }}/images/Tips-icon.png)   本周提示
由Microsoft Azure提供支持

Postgres拥有比你想象中更多的数据类型：了解IP地址和网络  
在像Postgres这样的数据库中构建数据模型时，很容易坚持使用像TEXT和INTEGER这样的经典的数据类型。您甚至可能会分别使用[数组](https://www.postgresql.org/docs/9.1/arrays.html)，[hstore](https://www.postgresql.org/docs/9.1/hstore.html)或[JSON](https://www.postgresql.org/docs/10/datatype-json.html)来使数据更具动态性，但还有更多值得发现的东西。

深入研究Postgres的所有数据类型可能会填满一本书，因此我们今天关注的是一个例子：使用INET获取IP地址。

INET用于存储IPv4或IPv6地址，还可以通过指定网络掩码来存储networks 如果您尝试存储的内容不是有效的IP地址或networks，Postgres会报错，因此您基本上可以获得数据验证：

```
CREATE TABLE addrs (address INET);
INSERT INTO addrs VALUES ('127.0.0.1');
INSERT INTO addrs VALUES ('hello world');
# ERROR: invalid input syntax for type inet: "hello world"

```

INET类型比数据验证更进一步，并且您可以在SQL查询中使用各种方法来进一步查询IP和网络地址：

```
INSERT INTO addrs VALUES ('202.121.0.0/16');
SELECT address, host(address), broadcast(address), netmask(address) FROM addrs;
```

查询结果版面有点太宽，无法适应周报格式，因此没有体现。如果您熟悉IP寻址，则会按照您对函数名称的期望返回有关网络的相关详细信息。 对于比较IP地址，提取部分地址和屏蔽地址，还有[很多函数](https://www.postgresql.org/docs/9.3/functions-net.html)。

>本周提示由Microsoft Azure提供支持。想要使用Postgres而不必担心管理，保护和扩展数据库？了解有关[Azure上的PostgreSQL](https://docs.microsoft.com/en-us/azure/postgresql/overview?ocid=orcas_pw_pgs)以及[有关Hyperscale的最新消息](https://mybuild.techcommunity.microsoft.com/sessions/76988?source=sessions&ocid=orcas_pw_pgs)。

🗓  即将举办的Postgres活动  
 [PGCon 2019(5月28-31日,加拿大渥太华)](https://www.pgcon.org/2019/) ——一个年度会议，供用户和开发人员见面和讨论Postgres。  
 [PostgreSQL Ibiza(六月19-21日, 伊维萨)](https://www.pgibz.io/index.html) —— 这个在西班牙著名的度假岛上举行的会议将会带来“海滩上的Postgres”，同时仍然在一个漂亮整洁的场地上进行会谈和培训。  
 [Postgres Vision 2019(6月24日,波士顿)](https://postgresvision.com/) 
 最新：[PostgresConf Beijing 2019(7月3-6日，中国北京)](https://postgresconf.org/conferences/Beijing)
