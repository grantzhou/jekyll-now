---
layout: post
title: PostgreSQL 每周新闻 2019-04-24
---

### PostgreSQL每周新闻#302 - 2019年4月24日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)

备注：[英文原文地址](https://postgresweekly.com/issues/302)

![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/kkezxirgkdbs56ajblmu.jpg)

## [使用SQL和Postgres生成图形](https://malisper.me/generating-fractals-with-postgres-escape-time-fractals/)

在“!! Con West 2019”会议上，Michael[谈到了使用SQL生成图形](https://www.youtube.com/watch?v=xKoYIvMFnoQ)，这是已经完成的版本。这不仅仅是一个（非常详细的）有趣的东西，你可以从中学到很多SQL和Postgres相关的知识——强烈推荐！

`MICHAEL MALIS`

## [电子书：Postgres日志中有关监控的最重要事件](https://pganalyze.com/ebooks/monitoring-postgres-logs?utm_source=PostgresWeeklyPrimary)
![img](https://copm.s3.amazonaws.com/0da05f27.png)  
在这本pganalyze的电子书中，我们可以了解有关监控查询性能和防止停机的最重要的6个Postgres日志事件。

`PGANALYZE` **赞助商**

## [关于Postgres 12 REINDEX CONCURRENTLY的更多信息](https://paquier.xyz/postgresql-2/postgres-12-reindex-concurrently/)
几个星期前，我们链接了一篇关于[REINDEX CONCURRENTLY](https://www.depesz.com/2019/03/29/waiting-for-postgresql-12-reindex-concurrently/)的简短帖子，这是Postgres 12的一个新功能，它允许在重建索引期间进行读写查询。Michael Paquier现在对其运作和历史有了更多见解。

`Michael Paquier`

## [如何在Go（lang）中使用Postgres](https://jbrandhorst.com/post/postgres/)
经验丰富的“gopher”可以提供有关驱动程序，迁移，查询和测试的最佳知识包。 如果你碰巧是Go开发人员，你知道我们有[Go的简报](https://golangweekly.com/?utm_source=pg&utm_medium=email&utm_campaign=cross_promo&utm_content=302)吗？

`JOHAN BRANDHORST`

## [▶如何修复损坏的TOAST表](https://www.youtube.com/watch?v=4jcC-lYGM0k)

`RAGHAVENDRA TADIPATHRI`

## [PostgreSQL 12新功能：对一个事务的所有的SQL进行取样记录](https://www.depesz.com/2019/04/18/waiting-for-postgresql-12-log-all-statements-from-a-sample-of-transactions/)
快速浏览一下Postgres 12的一个新功能，它可以让你的日志文件中的sql语句受控，在你想要的时候对SQL语句进行取样记录。

`HUBERT DEPESZ LUBACZEWSKI`

# 🛠工具和代码

## [pg_sampletolog：一个取样记录sql语句和事务的插件](https://github.com/anayrat/pg_sampletolog)

Sql语句取样记录功能即将在pg12发布（前文提到）。这个扩展可以让你在pg9.4-pg11上使用sql语句和事务取样记录功能。

`ADRIEN NAYRAT`

## [plpgsql_check：PL / pgSQL代码检查器](https://github.com/okbob/plpgsql_check)
如果你想找到潜伏在你的PL / pgSQL函数中的任何错误，它可能是一个救星。该项目创建时间比较长了，但一直保持更新，并能运行在现代Postgres版本上。

`PAVEL STEHULE`

## [管理Postgres访问的最佳方式](https://www.strongdm.com/product/?utm_source=&utm_medium=email&utm_campaign=2019-04-24%20-%20%5BUSA%5D%20-%20%5BSchD%5D%20-%20%5BSDM%5D%20-%20%5BENT%5D%20-%20PGW)
strongDM对你所接触的很多东西都有效。认真的讲，任何数据库，任何服务器，每个环境。[看看它是怎么工作的](https://www.strongdm.com/product/?utm_source=&utm_medium=email&utm_campaign=2019-04-24%20-%20%5BUSA%5D%20-%20%5BSchD%5D%20-%20%5BSDM%5D%20-%20%5BENT%5D%20-%20PGW)

`STRONGDM` **赞助商**

## [tail_n_mail：专注于Postgres日志的日志文件监视器](https://github.com/bucardo/tail_n_mail)
一个Perl脚本，可自动检测并发送邮件给管理员日志文件中的“有趣”项目。[文档在这里](https://bucardo.org/tail_n_mail/)

`JOSH WILLIAMS`

## [deno-postgres：PostgreSQL驱动Deno](https://github.com/bartlomieju/deno-postgres)
[Deno](https://github.com/denoland/deno)是一个运行在JavaScript的上的postgres驱动，它有趣且具有实验性，由Node.js的原始创建者构建（注意Deno是由Node字母重新排列而来的！）

`BARTEK IWAŃCZUK`

## [node-postgres：Node.js的非阻塞PostgreSQL客户端](https://github.com/brianc/node-postgres)
非常受欢迎，并在过去几周内发布了一些版本。

`BRIAN CARLSON`

## [pq：用于数据库/sql的纯Go Postgres驱动程序](https://github.com/lib/pq)
[pqv1.1](https://github.com/lib/pq/releases/tag/v1.1.0)上周发布了，支持Go 1.8及以下版本。

`BLAKE MIZERANY AND CONTRIBUTORS`

# ![_config.yml]({{ site.baseurl }}/images/Tips-icon.png)   本周提示
由HASURA提供支持

使用FILTER将表的实体/值转换为实体行

在这个主题上可以写一篇完整的文章，但我想展示SQL的最基本用法：2003年添加到Postgres 9.4的FILTER子句。

假设您有一个名为props的表，它来展示具有整数id列，文本属性列和值列的实体，属性和值，以及以下内容：
![img](https://res.cloudinary.com/cpress/image/upload/v1556051543/gyrmqkc10uqzt0liqnmi.jpg)  

[FILTER子句](https://modern-sql.com/feature/filter)实质上添加了一个额外的WHERE子句来聚合函数（例如MIN，MAX和SUM），允许您对它们限定范围。
这对于根据attr列的值从val列中提取值非常方便，因此允许我们将表的实体，属性和值转换为更经典的列集。

```
SELECT id,
       MAX(val) FILTER(WHERE attr='name') AS name,
       MAX(val) FILTER(WHERE attr='age') AS age,
       MAX(val) FILTER(where attr='city') AS city
FROM props GROUP BY id;
```

您可能需要重现此表并使用查询来了解正在发生的事情，但实质上我们按ID分组来选择每一行（即基础实体的ID），然后选择与某些属性名称匹配的ID相关联的值，在这种情况下，允许我们提取名称，年龄和城市值。MAX在这里作为聚合函数正常工作，因为每个实体只有一个attr/val对。

FILTER子句有更多的用途，但我觉得这是一个非常清楚，但也许意外的使用案例。

您可以在[这篇文章](https://medium.com/little-programming-joys/the-filter-clause-in-postgres-9-4-3dd327d3c852)和[Postgres官方文档](https://www.postgresql.org/docs/9.5/sql-expressions.html#SYNTAX-AGGREGATES)中了解更多信息。

>本周提示由[Hasura](https://github.com/hasura/graphql-engine)提供支持，Hasura是新的和现有的Postgres数据库上的高性能GraphQL引擎的创建者。[在GitHub上查看它们](https://github.com/hasura/graphql-engine)。

🗓  即将举办的Postgres活动  

 [pgconf.de 2019 (5月10日,莱比锡)](https://2019.pgconf.de/) ——最成功的德语PostgreSQL会议。  
 [PGDay.IT 2019 (5月16-17日,博洛尼亚)](https://2019.pgday.it/en/)  
 [PGCon 2019(5月28-31日,渥太华)](https://www.pgcon.org/2019/) ——一个年度会议，供用户和开发人员见面和讨论Postgres。  
 [Postgres Vision 2019(6月24日,波士顿)](https://postgresvision.com/)  
 

