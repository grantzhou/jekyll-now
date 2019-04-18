---
layout: post
title: PostgreSQL 每周新闻 2019-04-17
---

### PostgreSQL每周新闻#301 - 2019年4月17日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)

备注：[英文原文地址](https://postgresweekly.com/issues/301)

## ['Postgres现在有可插拔的表存储'](https://twitter.com/AndresFreundTec/status/1113948321976946689)
好吧，核心确实如此，我们需要等待一段时间才能在生产中使用它，但能够更轻松地切换到表存储系统将会带来有趣的机会。

`ANDRES FREUND ON TWITTER`

## [用C语言编写PostgreSQL扩展很有趣](https://www.percona.com/blog/2019/04/05/writing-postgresql-extensions-is-fun-c-language/)
这取决于你对乐趣的定义，但它并不像我想象的那么困难。这篇文章介绍了入门的基本步骤。如果您希望继续这样做，我认为阅读简单但完整的扩展代码，例如[count_distinct](https://github.com/tvondra/count_distinct/blob/master/src/count_distinct.c)，是非常有用的。

`IBRAR AHMED`

## [学会保护您的数据库](https://resources.2ndquadrant.com/security-and-compliance-with-postgresql)
![img](https://copm.s3.amazonaws.com/9a6f3274.png)  
加入免费的PostgreSQL网络研讨会：PostgreSQL的安全性和合规性，并学习如何识别和保护您的数据库漏洞点。[今天预定您的位置](https://resources.2ndquadrant.com/security-and-compliance-with-postgresql)

`2NDQUADRANT POSTGRESQL WEBINARS`  **赞助商**

## [当Postgres阻塞：处理锁的7个技巧](https://www.citusdata.com/blog/2018/02/22/seven-tips-for-dealing-with-postgres-locks/)
我们正在重新审视一个经典帖子，该帖子强调了开发人员在处理Postgres锁时会遇到的常见错误以及措施。

`MARCO SLOT`

## [Postgres 12正在优化小表的存储](https://www.2ndquadrant.com/en/blog/optimizing-storage-small-tables-postgresql-12/)
如果您的数据库模型要求您拥有大量小表（例如，multi-tenant schema），请阅读这篇文章。在Postgres 12中，事情会变得更有效率。

`JOHN NAYLOR`

## [Swarm64支持Xilinx Alveo加速器](https://swarm64.com/press-release/swarm64-supports-xilinx-alveo/)
冒着听起来像一堆流行语和商标的风险，这是一篇关于[基于FPGA的数据库加速器](https://swarm64.com/productsolution/)支持Postgres的新闻稿。

`SWARM64`

## [使用pg_upgrade以最短的停机时间快速升级Legacy Postgres](https://www.percona.com/blog/2019/04/12/fast-upgrade-of-legacy-postgresql-with-minimum-downtime-using-pg_upgrade/)
来自Percona的一系列Postgres升级帖子中的最新一篇。这次考虑了[pg_upgrade](https://www.postgresql.org/docs/11/pgupgrade.html)（以前的pg_migrator）。

`AVINASH VALLARAPU`

## [用于PostgreSQL的Azure数据库入门](https://docs.microsoft.com/en-us/azure/postgresql/?ocid=orcas_pw_pgs)
完全托管的Postgres数据库引擎，具有内置的高可用性，可伸缩性和安全性等功能。 开始使用您选择的开源工具。

`MICROSOFT AZURE` **赞助商**

## [Postgres 12亮点：pg_checksums](https://paquier.xyz/postgresql-2/postgres-12-pg-checksums/)
重新命名Postgres 11中引入的pg_verify_checksums。

`MICHAEL PAQUIER`

## [pspg：Postgres的psql客户端的替代](https://github.com/okbob/pspg)
替换较少并支持表格数据。

`PAVEL STEHULE`

## [Marten：基于Postgres的.NET系统持久性](http://jasperfx.github.io/marten/)
基于.NET的应用程序的文档数据库和事件存储，它使用Postgres在后端执行繁重的工作。 并且，是的，它适用于.NET Core :-)

`JASPERFX`

## [libpqxx：Postgres官方C ++客户端API](https://github.com/jtv/libpqxx)
libpqxx最近有很多更新。

`JEROEN VERMEULEN`

# ![_config.yml]({{ site.baseurl }}/images/Tips-icon.png)   本周提示
由PERCONA提供支持

自动记录慢查询

托管我们的时事通讯业务的服务器运行缓慢，我们不知道原因。特别是Postgres，所以我们希望看到哪些查询陷入困境。

与大多数数据库一样，Postgres具有内置的慢查询日志功能，如果它们占用了一定的时间，它会自动将查询记录到主Postgres日志文件中，设置起来非常简单。

在你的主postgresql.conf文件（通常是/etc/postgresql/9.6/main/postgresql.conf）中，编辑或添加一行如下：

```
log_min_duration_statement = 1000
```

重新启动Postgres或使用SELECT pg_reload_conf（）重新加载配置后，此指令将记录超过1000毫秒（一秒）的任何查询。

（日志文件的位置不同，但在我的测试设置中的是/var/log/postgresql/postgresql-9.6-main.log。）

故意为测试目的运行长查询：

```
select pg_sleep(10) /* just testing */;
```

请注意查询中是否存在注释，该注释也会出现在日志中，以便其他监控人员了解正在发生的事情。

Postgres不会导致我们的性能问题。我们的VPS是在一个共享的盒子上，它被大量使用，实例的升级修复了它。不过，我会注意到，如果你运行任何VPS风格的服务器，那么熟悉[“窃取时间”以及如何监控它](https://scoutapm.com/blog/understanding-cpu-steal-time-when-should-you-be-worried)是非常值得的！

> 本周提示由[Percona](https://www.percona.com/resources/webinars/upgrading-migrating-your-legacy-postgresql-newer-postgresql-versions)提供支持。加入Percona，我们将您的[老版本PostgreSQL升级/迁移到更新的PostgreSQL版本](https://www.percona.com/resources/webinars/upgrading-migrating-your-legacy-postgresql-newer-postgresql-versions)。

🗓  即将举办的Postgres活动  

 [pgconf.de 2019 (5月10日,莱比锡)](https://2019.pgconf.de/) ——最成功的德语PostgreSQL会议。  
 [PGDay.IT 2019 (5月16-17日,博洛尼亚)](https://2019.pgday.it/en/)  
 [PGCon 2019(5月28-31日,渥太华)](https://www.pgcon.org/2019/) ——一个年度会议，供用户和开发人员见面和讨论Postgres。  
 [Postgres Vision 2019(6月24日,波士顿)](https://postgresvision.com/)  
 
