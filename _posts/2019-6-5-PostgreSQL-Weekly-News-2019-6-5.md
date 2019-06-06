---
layout: post
title: PostgreSQL 每周新闻 2019-6-5
---

### PostgreSQL每周新闻#308 - 2019年6月5日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)

备注：[英文原文地址](https://postgresweekly.com/issues/308)

![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/v1559735604/pwkj4s4p7kakrzulztte.png)  

## [Postgres12的表访问方法和blackhole插件](https://paquier.xyz/postgresql-2/postgres-12-table-am-blackhole/)
表访问方法（通常称为“可插入存储”）被认为是Postgres 12中的一个突出的特性，可以更容易地显着扩展Postgres的工作方式。Michael用一个基本的[“blackhole”插件](https://github.com/michaelpq/pg_plugins/tree/master/blackhole_am)展示了它的基础知识（它本质上充当/dev/null存储方法）。

`MICHAEL PAQUIER`

## [使用Datadog进行实时PostgreSQL性能监控](https://www.datadoghq.com/postgres-monitoring/?utm_source=Advertisement&utm_medium=CooperPress&utm_campaign=CooperPress-PostgresWeeklyP)
![img](https://copm.s3.amazonaws.com/009a5d55.png)  
收集并可视化开箱即用的自定义Postgres指标，以更快地解决性能问题。将它们与动态基础架构，分布式跟踪和日志中的数据相关联。使用Datadog开始监控。

`DATADOG` **赞助商**

## [介绍pg_auto_failover（再次）：一个高可用性和自动故障转移的Postgres扩展](https://www.citusdata.com/blog/2019/05/30/introducing-pg-auto-failover/)
如果你感觉有些似曾相识，我们在[一个月前](https://postgresweekly.com/issues/304)微软发布这个项目时首先对它进行了介绍。现在，Citus Data团队对pg_auto_failover进行了更广泛的描述。

`CITUS DATA (MICROSOFT)`

## [对云端托管的Postgres进行基准测试：Microsoft Azure](https://severalnines.com/blog/benchmarking-managed-postgresql-cloud-solutions-part-four-microsoft-azure)
一系列有关托管的Postgres服务基准测试文章中的最后一篇————Microsoft Azure。

`SEVERALNINES`

## [PostgresOpen征集文章](https://2019.postgresopen.org/callforpapers/)
今年9月11日至13日将在美国奥兰多举办的PostgresOpen已经开启了他们的文章征集。关于Postgres有话要说吗？请考虑提交你的文章。还是想在欧洲发言？[PGConf.EU 2019’s CFP](https://2019.pgconf.eu/callforpapers/)也已开放文章征集，将于今年10月举行。

`UNITED STATES POSTGRESQL ASSOCIATION`

## [我如何降低Postgres对我的SaaS的响应时间](https://blog.checklyhq.com/how-i-decimated-postgres-response-times-for-my-saas/)
将Postgres查询响应时间从平均约100ms、峰值约1秒拉低到稳定的1-10ms。

`TIM NOLET`

## [电子书：优化Postgres查询性能的最佳实践](https://pganalyze.com/ebooks/optimizing-postgres-query-performance?utm_source=PostgresWeeklySecondary)
在这个免费的pganalyze电子书中，了解如何在Postgres数据库上获得3倍的性能提升，减少500倍从磁盘加载的数据。

`PGANALYZE` **赞助商**

## [Postgres中的分区的概述及其与MongoDB的关系](https://www.percona.com/blog/2019/05/24/an-overview-of-sharding-in-postgresql-and-how-it-relates-to-mongodbs/)

`FERNANDO LAUDARES CAMARGOS`

## ▶[安装，设置和使用PostGIS](https://www.youtube.com/watch?v=EBfjZgjyZmM)
一个30分钟的截屏视频，通过安装Postgres和PostGIS来处理地理数据。

`KLAS KARLSSON`

## [Sqitch 1.0：数据库变更管理](https://github.com/sqitchers/sqitch)
独立的数据库和框架（支持Postgres 8.4+）系统，用于通过SQL脚本管理数据库和模式更改。以下是[它的工作原理](https://github.com/sqitchers/sqitch/blob/develop/lib/sqitchtutorial.pod)。

`SQITCH`

# ![_config.yml]({{ site.baseurl }}/images/Tips-icon.png)   本周提示
由GitPrime提供支持 ![img](https://res.cloudinary.com/cpress/image/upload/v1554813939/kwagarrsergds4sxgjr9.png)

### 在psql中搜索旧查询

Postgres的官方（并且一直很受欢迎）的psql终端客户端有很多有趣的功能，到现在我才意识到这都是因为它使用了[Readline库](https://en.wikipedia.org/wiki/GNU_Readline)（通常，基于UNIX的实用程序, shell等也使用Readline库）。

Readline为提高psql的可用性带来了许多有用的文本编辑功能，包括补全功能（在键入查询时尝试它，这个功能很好用），按 `Ctrl+W` 可以整个删除键入的最后一个词。

你还可以访问历史记录（通常存储在运行Postgres的用户的主目录中的 `.psql_history` 文件中）可以按↑或↓来浏览最近输入的命令和查询，你知道可以动态搜索历史记录吗？

假设你有这样的会话：

`INSERT INTO people (name, age) VALUES ('Jim', 74);`
`SELECT * FROM people WHERE age > 18;`
`SELECT * FROM people ORDER BY name ASC LIMIT 1;`

如果现在按Ctrl + R并输入SEL，你将看到之前的查询再次出现，因为它已准备好自动完成。如果你继续输入，可以进一步调整搜索范围或按Ctrl + C以跳出搜索功能。

如果你使用搜索找到的查询并不是你想要的查询，那么再次按 `Ctrl + R`，它将循环其他的匹配。因此，如果按 `Ctrl + R` 并输入 `SEL` ，然后按住`Ctrl + R`，它将循环显示存储在历史记录中的其他SELECT查询。

>本周提示由[GitPrime](https://resources.gitprime.com/books/20-patterns/?utm_source=nl(pgw)&utm_medium=email-nl&utm_campaign=nl(pgw))提供支持。获取他们新的指南['20个工程团队需要关注的模式'](https://resources.gitprime.com/books/20-patterns/?utm_source=nl(pgw)&utm_medium=email-nl&utm_campaign=nl(pgw))的副本，其中包含可操作的见解，以帮助您调试开发过程中的数据。

🔬 psql命令周期表  
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/v1559733987/y74anviavcgujchlknif.png)


🗓  即将举办的Postgres活动  
- [PostgreSQL Ibiza(六月19-21日, 伊维萨)](https://www.pgibz.io/index.html) —— 这个在西班牙著名的度假岛上举行的会议将会带来“海滩上的Postgres”，同时仍然在一个漂亮整洁的场地上进行会谈和培训。  
- [Postgres Vision 2019(6月24日,波士顿)](https://postgresvision.com/) —— Web发明者Tim Berners-Lee爵士将发表主题演讲。
- [PostgresLondon 2019 (7月2-3日，伦敦)](https://postgreslondon.org/)
- [PostgresConf Beijing 2019(7月3-6日，中国北京)](https://postgresconf.org/conferences/Beijing)
