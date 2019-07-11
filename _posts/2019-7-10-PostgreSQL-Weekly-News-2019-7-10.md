---
layout: post
title: PostgreSQL 每周新闻 2019-7-10
---

### PostgreSQL每周新闻#313 - 2019年7月10日

![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)

备注：[英文原文地址](https://postgresweekly.com/issues/313)

![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/c6vmpzectzfcgjviu0zg.jpg)

## [Amazon Aurora PostgrsSQL Serverless 现已推出](https://aws.amazon.com/cn/blogs/aws/amazon-aurora-postgresql-serverless-now-generally-available/)

[Amazon Aurora](https://aws.amazon.com/cn/rds/aurora/)是一个适应于性能的基于AWS的数据库，它提供MySQL和Postgres兼容性，并按小时收费。然而，serverless版本将自动衡量，让您只需“按需付费”(在一定程度上)。MySQL已经支持这种方法[一年了](https://aws.amazon.com/cn/blogs/aws/aurora-serverless-ga/)，现在轮到Postgres用户来尝试这种方法。

`AMAZON WEB SERVICES`

## [在Postgres 12中生成列](https://www.2ndquadrant.com/en/blog/generated-columns-in-postgresql-12/)

“数据仓库社区会很高兴知道，PostgreSQL现在有了一个可以基于其他列中的数据生成新的列的功能。“ 这里说明他是怎样工作的。

`KIRK ROYBAL`

## [内存计算为PostgreSQL增加了速度和规模](https://www.gridgain.com/resources/papers/adding-speed-and-horizontal-scale-postgresql?adsource=postgresweekly)

将内存计算和PostgreSQL结合起来可以加速应用程序性能，支持更快的事务处理，支持大规模的可伸缩性，并且允许更好的业务分析——而不需要对现有架构进行复制和替换。[白皮书可以在这里找到。](https://www.gridgain.com/resources/papers/adding-speed-and-horizontal-scale-postgresql?adsource=postgresweekly)

`GRIDGAIN SYSTEMS, INC`**赞助商**

## [E-Maj 3.1.0:一种记录和回滚表数据更新的方法](https://www.postgresql.org/about/news/1952/)

是Postgres的扩展，支持细粒度的写日志和数据库子集上的“时间旅行”。这个版本现在支持Postgres 9.5到12。[GitHub 报道](https://github.com/dalibo/emaj)

`PHILIPPE BEAUDOIN`

## [psql中的CSV输出格式](https://postgresql.verite.pro/blog/2019/07/06/psql-csv-output.html)

CSV是一种方便而通用的（多少有点怪怪的）数据交换格式，Postgres多年来一直以各种方式支持这种格式。Postgres 12更进一步，如果您乐意，可以让psql将所有表格结果输出为CSV格式。

`DANIEL VÉRITÉ`

## [用Python将数据加载到Postgres的最快方法](https://hakibenita.com/fast-load-data-python-postgresql)

如果您有大量的“脏”数据需要获取转换，然后输入到Postgres中，这是一个广泛的教程，将为您提供指导。

`HAKI BENITA`

## [Postgres的时间间隔、日期、时间戳和时间数据类型](https://www.2ndquadrant.com/en/blog/know-what-time-it-is/)

这是对Postgres实现的各种类型的简单介绍，允许您表示和处理持续时间(有关技巧，请参阅下面的每周技巧)。

`ELEIN MUSTAIN`

## [免费电子书:如何获得一个3倍的性能改进您的Postgres数据库](https://pganalyze.com/ebooks/optimizing-postgres-query-performance?utm_source=PostgresWeeklySecondary)

学习我们的最佳实践，像Atlassian一样为客户优化Postgres查询性能以及如何将磁盘加载的数据减少500倍。

`PGANALYZE`**赞助商**

## [（几乎）自动生成主键](https://fluca1978.github.io/2019/07/09/GeneratePrimaryKeys.html)

我想不出一个我想做这件事的理由。但是我还是很乐意知道我能够做到它(!)

`LUCA FERRARI`

## [提供来自PostGIS的动态向量块](https://info.crunchydata.com/blog/dynamic-vector-tiles-from-postgis)

PostGIS扩展了Postgres，使之成为一个强大的地理和地理空间数据引擎，还可以生成和处理平铺地图。

`PAUL RAMSEY`

## [Terraform PostgreSQL Provider](https://github.com/terraform-providers/terraform-provider-postgresql) 

[Terraform](https://www.terraform.io/)是一个受欢迎的基于代码的基础设施管理系统。

`TERRAFORM`

# 💡每周提示

由EnterpriseDB提供支持![EnterpriseDB](https://res.cloudinary.com/cpress/image/upload/v1562592058/ejysjrwdn0ew88ofido4.png)

### 使用date_trunc降低时间精度

date_trunc是内置在Postgres中的众多[日期/时间函数](https://www.postgresql.org/docs/9.1/functions-datetime.html)之一，但对我来说，它的性价比肯定很高。

date_trunc将时间戳截断到特定的精度级别，比如特定的小时、秒、天、周、年等等。

例如，让我们创建一个非常简单的订单表，它只存储订单创建的时间:

 

```
 CREATE TABLE orders (created_at timestamp);

INSERT INTO orders VALUES
  ('2019-01-01 04:05:33'),
  ('2019-01-01 09:05:51'),
  ('2019-01-03 02:55:14'),
  ('2019-01-08 14:12:07');  
```

现在，我们可以在created_at上使用date_trunc来按天或周分组和计数订单:

```
SELECT date_trunc('day', created_at) AS day,
       COUNT(created_at) FROM orders
       GROUP BY day
       ORDER BY day;
```

```
 day                | count
 ----------------------------
2019-01-01T00:0 ... | 2
2019-01-08T00:0 ... | 1
2019-01-03T00:0 ... | 1
```

这个基本示例显示，如果我们按照created_at 缩短到天级别进行分组，那么我们可以计算每一天有多少个订单。

本周的技巧是由[EnterpriseDB](https://www.enterprisedb.com/enterprise-postgres/edb-postgres-platform)赞助的，它是最完整的开源数据库平台。[了解更多关于企业Postgres解决方案的信息。](https://www.enterprisedb.com/enterprise-postgres/edb-postgres-platform)

🗓  **即将举办的Postgres活动**  

• [PGConf.Brasil 2019](https://www.pgconf.com.br/2019/en/) (8月1日 - 3日，巴西圣保罗)——为期三天的会议与讲座，教程，课程，闪电会谈。

•  [PGDay Austria 2019](https://pgday.at/en/) (9月6日，奥地利维也纳Neustadt)

• [PostgreSQL Conference Asia 2019](https://2019.pgconf.asia/)(9月9日 - 12日，印度尼西亚巴厘岛)

• [PostgresConf South Africa 2019](https://postgresconf.org/conferences/SouthAfrica2019) (10月8日 - 9日，南非约翰内斯堡)——为使用Postgres数据库的管理人员和开发人员提供了一个彼此了解的机会。
