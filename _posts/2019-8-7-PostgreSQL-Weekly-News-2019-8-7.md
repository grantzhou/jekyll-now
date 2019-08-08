---
layout: post
title: PostgreSQL 每周新闻 2019-8-7
---

### PostgreSQL每周新闻#317 - 2019年8月7日

![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)

备注：[英文原文地址](https://postgresweekly.com/issues/317)

![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/v1565174369/cf22e4nqrrvzco0djbht.jpg)

## [使用C写Postgres插件的初级教程](https://www.percona.com/blog/2019/07/31/postgresql-simple-c-extension-development-for-a-novice-user/)

Postgres通过插件使自己容易扩展，最常见的插件是用C语言构建的。这个博客演示了如何建立一个基本的Postgres扩展项目并使其工作。

`JOBIN AUGUSTINE`

## [对比Postgres的JSONB和Couchbase](https://blog.couchbase.com/postgres-jsonb-and-nosql/)

Postgres真的能通过JSONB取代‘NOSQL’文档数据库么？从一个文档数据库供应商的角度来看，这是一个有意思的话题。

`DENIS ROSA (COUCHBASE)`

## [免费的电子书](https://pganalyze.com/ebooks/optimizing-postgres-query-performance?utm_source=PostgresWeeklyPrimary)：如何将你的Postgres数据库提升3倍的性能

学习我们如何为Postgres优化性能,如何500倍的降低磁盘IO。

`PGANALYZE`**赞助商**

## [Postgres VS MongoDB的Benchmarking:'要么透明化要么别测试'](https://www.percona.com/blog/2019/07/16/brin-index-for-postgresql-dont-forget-the-benefits/)

最近有一个关于Postgres和MongoDB的基准测试，测试结果显示Postgres吊打MongoDB。MongoDB回应测试者没有将两个数据库放置在公平的测试环境之下。

`ÁLVARO HERNÁNDEZ`



## [Postgres获得终生成就奖](https://www.2ndquadrant.com/en/blog/postgresql-award/)

一个项目获得“终身成就”奖让人感觉很奇怪。好在Mark Wong、Bruce Momjian和Christophe Pettus代表PostgreSQL项目在O'Reilly的Oscon活动上接受了该奖项。

`MARK WONG`



## [Postgres对正则表达式的支持](https://www.2ndquadrant.com/en/blog/postgresql-regular-expressions-and-pattern-matching/)

正则表达式是描述文本搜索模式的字符序列。Postgres支持几种使用regex的方法。

`MUHAMMAD HAROON`



## [如何为Postgres程序进行linux的OOM killer设置](https://www.percona.com/blog/2019/08/02/out-of-memory-killer-or-savior/)

oom“killer”负责终止应用程序，以回收内存并防止内核崩溃。这里有一些建议，以避免它将Postgres进程干掉。

`IBRAR AHMED`



## [使用pl pgsql_check查找编译错误](https://www.percona.com/blog/2019/07/30/using-plpgsql_check-to-find-compilation-errors-and-profile-functions/)

plpgsql_check是一个类似于plprofiler的项目，它还能检查PL/pgSQL代码指出其中的编译错误。

`AVINASH VALLARAPU`



## [监控Postgres数据库的标准](https://www.influxdata.com/blog/metrics-to-monitor-in-your-postgresql-database/?utm_campaign=postgres&utm_medium=newsletter&utm_source=cooperpress)

当涉及到数据库性能时，您需要跟踪几个关键指标，它们并不都是特定于数据库的。

`INFLUXDATA`



## [为什么Postgres不会被卖掉](https://www.2ndquadrant.com/en/blog/postgres-is-the-coolest-database-reason-5-it-can-not-be-bought-out/)

MYSQL之前也是一款开源数据库，oracle通过收购其母公司，接管了MYSQL项目，这种事情不会发生在Postgres。

`UMAIR SHAHID`



## [Barman 2.9：备份恢复管理工具](https://www.postgresql.org/about/news/1959/)

此版本引入了对即将发布的Postgres12的本机支持，其中包括对时间点恢复和复制管理方式的重大更改。

`2NDQUADRANT`



## [怎样将一个VARCHAR类型的数据显示为encode byte流](https://abbas-technical.blogspot.com/2019/07/how-to-display-encoded-byte-stream-of.html)

虽然不知道这会有什么应用场景，但是这是一个有趣的SQL。

`ABBAS`

# 💡本周提示

###### 使用pgstattuple去查看无效的行和空闲空间

由[GitPrime提供

pgstattuple是一个内置的postgres扩展，它提供了各种函数来查看数据库中各种对象的统计信息。一种用途是检查表中有多少死行（通常是从表中删除数据时导致的）或者表中有多少可用空间。

我们来创建一个有1000行数据的表，然后看一下pgstattuple能带给我们什么。

```
CREATE TABLE numbers (id int);
INSERT INTO numbers SELECT * FROM generate_series(1,1000);
```

现在让我们来使用pgstattuple

```
CREATE EXTENSION pgstattuple;
SELECT * FROM public.pgstattuple('numbers');
```

![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/v1565092544/mtu5it0lrih9ho7r2w96.png)

这显示我们的表里有1000行数据，有0个无效tuple

让我们删掉一半的数据

```
DELETE FROM numbers WHERE id < 500;
SELECT * FROM public.pgstattuple('numbers');
```

![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/v1565093436/l5mitxgxty3d4f8mj5ke.png)

现在我们得到了499的死元组计数(我们删除的行数)。但是整个表是一样的。因为那些无效tuple还存在。这可以通过运行以下命令来解决：

```
VACUUM numbers;
```

之后重新运行pgstatuple将不会显示无效行，但可用空间得到提升。表长度保持不变！这样做的原因是vacuum将清除死行并将其转换为自由空间（可以重新用于新行），但如果您真的希望Postgres重写表并释放该空间，则需要更进一步并使用vacuum full（尽管您需要注意执行此操作，在生产表上，因为它可能非常慢，并且会一直锁定表）。

本周提示由[GitPrime](https://resources.gitprime.com/books/20-patterns/?utm_source=nl(pgw)&utm_medium=email-nl&utm_campaign=nl(pgw))赞助。



🗓  **即将举办的Postgres活动**  

• [PGConf.Brasil 2019](https://www.pgconf.com.br/2019/en/)(8月1-3日，圣保罗)——为期三天的会议，包括讲座，教程，课程和闪电讲座。

• [PGDay Austria 2019](https://pgday.at/en/)（9月6日， 维纳·纽斯塔特，奥地利）

• [PostgreSQL Conference Asia 2019](https://2019.pgconf.asia/)（9月8-11日，巴厘岛，印度尼西亚）

• [PostgresConf South Africa 2019](https://postgresconf.org/conferences/SouthAfrica2019)（10月8-9日，约翰内斯堡）——提供给使用Postgres的数据库管理和开发人员互相了解的机会。