---
layout: post
title: PostgreSQL 每周新闻 2020-7-1
---
### PostgreSQL每周新闻#362 - 2020年7月1日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)
备注：[英文原文地址](https://postgresweekly.com/issues/362)
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/v1593609071/cchxwnmldtjs9xojgu4u.jpg)

## [Amazon RDS代理现已正式提供](https://postgresweekly.com/link/91150/web)
RDS Proxy是RDS的完全托管数据库代理（包括PostgreSQL变体）。无需更改代码，但需要收费（数据库服务器每vCPU每小时0.015美元）。由于可能会出现大量的开放式数据库连接，因此构建 serverless应用程序的人可能会特别感兴趣。

`Channy Yun (AWS) `

## [使用GitHub Actions测试扩展](https://postgresweekly.com/link/91022/web)
pgxn工具提供了一个Docker映像，其中包含安装和运行任何版本Postgres的脚本，并且可以将其与CI/CD平台（如GitHub Actions）结合起来，在多个Postgres版本上测试Postgres扩展。

`David E. Wheeler `

## [白皮书：BDR-针对PostgreSQL的高级集群和扩展](https://postgresweekly.com/link/91023/web)
了解有关使用BDR的PostgreSQL的高级集群和扩展的更多信息，包括使用案例、体系结构、特性和优点。BDR为PostgreSQL数据库提供具有AlwaysOn可用性的多主机复制、全球集群和云本地部署。


`2ndQuadrant PostgreSQL Products `
## [在SQL中计算行之间的差异](https://postgresweekly.com/link/91024/web)
如果有很多行表示不断变化的值（比如说时间序列数据），那么能够计算值随时间的差异可能会很有用，下面是一些方法。

`Hans-Jürgen Schönig `

## [在K8S运行PostgreSQL](https://postgresweekly.com/link/91025/web)
PDF:Kubernetes中运行Postgres的主要选项以及每个选项中包含的一些特性的幻灯片。


`Lukas Fittl `
## [提高Postgres和TimescaleDB插入性能的13个技巧](https://postgresweekly.com/link/91026/web)
前五个技巧通常与Postgres相关，其余的则特定于TimescaleDB，一个Postgres的时间序列数据扩展。


`Michael Freedman `
## [论Join策略与性能](https://postgresweekly.com/link/91028/web)
有必要了解Postgres在连接关系时使用的三种连接策略形式，以及如何通过索引影响它们。

`Laurenz Albe `

## [PostgreSQL的关键字大小写可控么](https://postgresweekly.com/link/91029/web)
“让我们回顾一下Postgres的一些大小写精度行为，比如字符串、标识符和关键字的处理。”这里是一个关于大小写比较问题的简单入门。

`Bruce Momjian `

## [Timescale云：高性能PostgreSQL](https://postgresweekly.com/link/91030/web)
现在在三个主要云层的75+个地区都可以使用。分析、性能和规模。

`Timescale `

## [Postgres按需匿名化](https://postgresweekly.com/link/91031/web)
如果你的数据库存储了个人身份信息——很可能是这样！–匿名化可以帮助保护数据，同时保持数据库的有用性。本文深入研究了一种在全局范围内应用匿名化的方法，它覆盖了所有应用程序，并且代码重写最少。


`Achilleas Mantzios `
## [从Oracle到Postgres迁移工具ora2pg](https://postgresweekly.com/link/91032/web)
我怀疑如果你可以访问Oracle数据库，你可能不会随便找教程，但如果你是。。如果您需要将数据迁移到Postgres。。ora2pg和本教程可以帮助您。


`Yorvi Arias `
## [使用LDAP验证pgpool II](https://postgresweekly.com/link/91034/web)


`Ahsan Hadi `
## [为JSONB列编制索引的故事](https://postgresweekly.com/link/91035/web)
当涉及到大规模使用JSONB时，故事和技巧的完美结合。

`Vsevolod Solovyov `

# 💡本周提示


对于公共表表达式（CTE），从遍历树到在排名中使用窗口函数，您可以做很多事情。CTE函数由“WITH”子句实现。一个基本用途是查询子集——类似于子查询。


让我们通过设置一些示例数据来演示这一点：


```
CREATE TABLE databases (
  name TEXT, model TEXT, type TEXT, pgcompat boolean, opensource boolean);
 
INSERT INTO databases VALUES
  ('YugabyteDB', 'rdbms' , 'distributed sql', TRUE, TRUE), 
  ('CockroachDB', 'rdbms', 'distributed sql', FALSE, FALSE),
  ('MongoDB', 'document', 'nosql', FALSE, FALSE), 
  ('Neo4j', 'graph', 'nosql', TRUE, FALSE),
  ('Cassandra', 'columnar', 'nosql', FALSE, TRUE);
```


如果要对已获得开源许可的数据库运行查询，请支持SQL并与PostgreSQL兼容：


```
WITH dbs AS (
    SELECT 
        name, 
        model,
        (CASE 
            WHEN type = 'distributed sql' then TRUE
            ELSE FALSE
        END) sql_support,
    pgcompat,
    opensource    
    FROM
        databases
)
SELECT
    name,
    model
FROM 
    dbs
WHERE
    opensource = TRUE,
    pgcompat = TRUE,
    sql_support = TRUE
ORDER BY 
    name;
```


我们将sql语句重新解释为一个布尔类型，并将其重新解释为“支持”。在主select语句中，我们针对这个CTE查询，在where子句中，我们只能指定布尔值。


结果是这样的：


```
name     | model
-------------------
YugabyteDB | rdbms
```


**🗓即将举办的Postgres活动**
