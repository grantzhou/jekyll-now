---
layout: post
title: PostgreSQL 每周新闻 2020-9-9
---
### PostgreSQL每周新闻#372 - 2020年9月9日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)
备注：[英文原文地址](https://postgresweekly.com/issues/372)
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/y7yg2yhwsqhaaabsamhg.jpg)
## [看看Postgres中的B树索引重复数据删除13](https://postgresweekly.com/link/94762/web)
B树索引是Postgres中创建的默认索引类型，因此对其操作的任何更改都可能会产生很多连锁反应。在即将发布的Postgres 13中尽可能对这些索引进行重复数据删除将有助于使这些索引保持较小并具有性能影响（很可能会降低I / O使用率，但会略微增加CPU，但在大多数情况下会提高整体性能）。


`Ryan Lambert `
## [如何充分利用Postgres日志](https://postgresweekly.com/link/94763/web)
Postgres的日志记录系统非常可调，并且有很多参数可供选择。这篇文章介绍了一些基本的实践，可以充分利用Postgres服务器的日志以及您可以进行的调整。


`Sadequl Hussain `
## [[白皮书]专业支持的业务案例](https://postgresweekly.com/link/94816/web)
了解专业支持对关键任务PostgreSQL系统的重要性以及它如何使您的公司受益。了解它如何提高数据库性能，帮助扩展，分发数据，降低成本，使您免于已知的陷阱等。


`2ndQuadrant Services `
## [Citus 9.4 Postgres扩展的新增功能](https://postgresweekly.com/link/94765/web)
Citus将Postgres转换为分布式数据库，从而将数据和SQL查询分布在多个节点上。 v9.4改进了EXPLAIN ANALYZE，具有一些性能和安全性改进，现在可以使用t-digest扩展大规模地计算百分位。 


`Marco Slot (Citus Data) `
## [在SQL中生成正态分布](https://postgresweekly.com/link/94766/web)
Postgres的tablefunc扩展提供了多种返回表的函数，包括一组正态分布的随机值。


`Hans-Jürgen Schönig `
## [PostGIS和地理类型](https://postgresweekly.com/link/94768/web)
PostGIS地理类型是一种地理坐标类型，可将坐标理解为球坐标（经度和纬度），这是对它们的基本介绍（也是使用PostGIS的原因之一）。


`Paul Ramsey `
## [如何加快Postgres查询的最佳做法。免费电子书](https://postgresweekly.com/link/94769/web)
Robinhood和Atlassian等公司可以将查询速度提高几个数量级。这本电子书分享了我们优化Postgres性能的最佳实践。


`pganalyze `
## [在ZFS上调整Postgres ](https://postgresweekly.com/link/94770/web)
“使用ZFS而不是ext4 / xfs的主要原因是压缩。通过合理的配置，您可以使用LZ4实现3-5倍的压缩率。这意味着LZ4会将1 TB的数据压缩到约300 GB。”


`Uptrace `
## [使用Deno，Ren​​o和Postgres构建微服务](https://postgresweekly.com/link/94771/web)
Deno是基于V8（有点类似于Node，但不类似）构建的服务器端JavaScript运行时，Reno是Deno应用程序的路由库。


`James Wright `
## [使用SQLancer挖掘到Postgres的Citus扩展中的逻辑错误](https://postgresweekly.com/link/94773/web)
您可能不需要做这些事情之一，但是很高兴知道如何解决这些问题。 SQLancer是我们之前链接过的工具，可帮助您检测数据库系统中与逻辑相关的错误。 


`Nazli Ugur Koyluoglu `
# 💡本周提示


按列表中指定的顺序返回行
如果您有一个数据表（例如，一个以其名称和publication_date存储的书的书表），并且您想要返回列表指定的行，则可以使用IN来执行此操作，如下所示：

```
SELECT * FROM books WHERE name IN ('The Adventures of Huckleberry Finn', 'Pride and Prejudice', 'The Great Gatsby');

                name                |  publication_date   
------------------------------------+---------------------
 Pride and Prejudice                | 1813-01-28 00:00:00
 The Adventures of Huckleberry Finn | 1884-12-10 00:00:00
 The Great Gatsby                   | 1925-04-10 00:00:00
(3 rows)
```

但是，不能保证以在IN子句中出现的顺序返回这些行。

如果要检索行并根据其在IN子句中的顺序对其进行排序，则可以使用VALUES子句并进行联接，如下所示

```
SELECT b.* FROM books b
    JOIN (
      VALUES ('The Adventures of Huckleberry Finn',1),
             ('Pride and Prejudice',2),
             ('The Great Gatsby',3)
    ) AS x (name, sortorder)
    ON b.name = x.name ORDER BY x.sortorder;
```

另外，您也可以将WITH ORDINALITY用于其他方法：

```
SELECT b.* FROM books b 
    JOIN 
    unnest('{"The Adventures of Huckleberry Finn",
             "Pride and Prejudice",
             "The Great Gatsby"}'::text[])
    WITH ORDINALITY t(name, sortorder) USING (name)
    ORDER BY t.sortorder;
```


本周的提示由YugabyteDB赞助。在9月15日至17日举行的（免费）分布式SQL虚拟峰会上，可以获得更多的技巧，数据库迁移的故事以及实际的分布式SQL数据库之旅

**🗓即将举办的Postgres活动**
