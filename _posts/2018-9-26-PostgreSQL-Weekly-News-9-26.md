---
layout: post
title: PostgreSQL 每周新闻 2018-09-26
---

### PostgreSQL每周新闻 #275 - 2018年9月26日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)
![_config.yml]({{ site.baseurl }}/images/wn0928.jpg)

备注：[英文原文地址](https://postgresweekly.com/issues/275)

## [在EC2上运行Postgres？ 你的时钟可能会让你失望](https://postgresweekly.com/link/53268/web)
一个在EC2上运行Postgres集群的公司发现了一个奇怪的故事，EC2在获得时间方面特别慢，从而导致该公司的Postgres分析工作受到性能影响。 
有趣的是，Heap的一位工程师也解释了为什么他们[使用EC2而不是RDS来运行Postgres](https://postgresweekly.com/link/53269/web)。

`KAMAL MARHUBI（HEAP）`

## [PostgreSQL 11 Beta 4发布了](https://postgresweekly.com/link/53270/web)
你会注意到我们正在链接很多与Postgres 11相关的东西（这个问题也不例外），而且它更接近今天发布的最新测试版。
如果您正在进行基准测试，请注意:默认情况下JIT编译现在是关闭的，如果需要的话现在必须明确打开它。

`POSTGRESQL全球开发组`

## [Postgres-XL：可水平扩展的PostgreSQL](https://postgresweekly.com/link/53271/web)
![XL IMG]({{ site.baseurl }}/images/xl.jpg)

Postgres-XL是一个大规模并行处理数据库 - 与PostgreSQL密切兼容，可以横向扩展。 
它在同一平台上支持Business Intelligence(商业智能)工作负载和大容量事务性写入和读取工作负载。

`2NDQUADRANT POSTGRESQL产品` **赞助商**

## [PostGIS 2.5.0发布 - PostgreSQL的空间和地理对象](https://postgresweekly.com/link/53272/web)
眼尖的读者会注意到所有2.5测试版针对的都是Postgres 11，而PostGIS 2.5最适合Postgres 11，它将适用于Postgres 9.4以及以上版本。

`POSTGIS开发人员`

## [优化Postgres列顺序](https://postgresweekly.com/link/53273/web)
您可以采用技术方式来进行一些底层修改，以便以高效内存的方式排序“列”。

`2NDQUADRANT`

## [Postgres 11：适合每个人的新功能](https://postgresweekly.com/link/53274/web)
这是对Postgres 11中的一些新功能的一个很好的高级解释
我们在过去几个月里大部分都引用了这些功能。 我们自己的Craig Kerstiens也 [尝鲜了一些新功能](https://postgresweekly.com/link/53275/web)。

`PETER GEOGHEGAN`

## [Amazon Aurora现在支持停止和启动数据库集群](https://postgresweekly.com/link/53276/web)
现在可以停止Aurora（它与Postgres兼容的版本）集群（最多7天）并重新启动，使其更有用，更便于开发和测试。

`亚马逊网络服务`

## [宣布：EDB Postgres迁移网站Beta](https://postgresweekly.com/link/53288/web)

`ENTERPRISEDB` **赞助商**

## [如何在SQL中编写乘法聚合函数](https://postgresweekly.com/link/53278/web)

`LUKAS EDER`

## [为企业级环境保护Postgres](https://postgresweekly.com/link/53279/web)
 这篇简短的文章介绍了一些可以提高安全性的Postgres功能。

`AVINASH VALLARAPU`

## [关于行为准则争议的思考]()
对PostgreSQL社区对其[最近发布的“行为准则”](https://postgresweekly.com/link/53281/web)的需求的反思以及应该采取什么样的流程来取得适当的平衡。

`CHRIS TRAVERS`

## [pg_terminator：清理会话和查询的工具](https://postgresweekly.com/link/53282/web)
配置后，它可以根据各种规则取消/终止查询和连接。

[Git 地址](https://postgresweekly.com/link/53283/web)。

`HUBERT DEPESZ LUBACZEWSKI`

# 活动
## [PostgresConf南非2018](https://postgresweekly.com/link/52934/web)
10月9日至10日（南非约翰内斯堡）

数据库管理和开发者社区有机会一起交流并了解当前的功能和未来的趋势。

## [2Q PGConf 2018 ](https://postgresweekly.com/link/53285/web)
12月4日至5日 (芝加哥)

一个致力于分享PostgreSQL知识的会议。


## [PGCONF.ASIA 2018](https://postgresweekly.com/link/52935/web)
12月10-12日（日本东京）

PGConf.ASIA 2018是PostgreSQL的国际会议。 快来参加在亚洲最大的PostgreSQL会议。

## [FOSDEM PGDay 2019](https://postgresweekly.com/link/52936/web)
2019年2月1日（比利时布鲁塞尔）

FOSDEM常规PostgreSQL活动的延伸。



