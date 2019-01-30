---
layout: post
title: PostgreSQL 每周新闻 2019-1-30
---

### PostgreSQL每周新闻#290 - 2019年1月30日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)

备注：[英文原文地址](https://postgresweekly.com/issues/290)

![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/jdtcqvqtmtfmgninlrcd.jpg)

## [微软收购Postgres横向扩展公司Citus Data](https://blogs.microsoft.com/blog/2019/01/24/microsoft-acquires-citus-data-re-affirming-its-commitment-to-open-source-and-accelerating-azure-postgresql-performance-and-scale/)
Citus以其同名的Postgres扩展而闻名，这使得Postgres更容易横向扩展。 此次收购是微软承诺支持Azure上的开源数据库用户和Postgres的一个有趣的证明。

`微软`

## [将Postgres扩展到每月12亿条记录的经验教训](https://medium.com/@gajus/lessons-learned-scaling-postgresql-database-to-1-2bn-records-month-edc5449b3067)

**译者**: 文章发表在Medium网站，国内访问需要梯子

**译者**: [查看此文章的复制版本](https://grantzhou.github.io/lessons-learned-scaling-postgresql-database-to-1-2bn-records-month/)

`GAJUS KUIZINAS`

## [在PostgreSQL环境中诊断和解决性能问题](https://www.quest.com/products/foglight-for-postgresql/?utm_source=&utm_medium=Direct-External+Online+Advertising&utm_campaign=FY2019_Q4_AMER_DBPerf_CooperPress_FoglightPostgres_Jan_eNewsletter_ADV&utm_term=&utm_content=cooper-press-enewsletter)
![quest](https://copm.s3.amazonaws.com/2100ff85.jpg)

管理基础架构的运行状况。 直观的基于Web的仪表板提醒您注意可能影响性能或可用性的问题，清晰的企业范围视图可帮助您优化整个PostgreSQL环境。 [下载免费试用版。](https://www.quest.com/register/110829/)

`QUEST SOFTWARE` *赞助商*

##[看看Postgres的六大顶级GUI工具](https://severalnines.com/blog/top-gui-tools-postgresql)
使用GUI很少是必须的，但基于GUI的工具在某些情况下可能很有用。 以下是对五个可选工具的简要回顾，包括pgAdmin，Navicat和ClusterControl。

`SEBASTIAN INSAUSTI（SEVERALNINE)`

## [优秀的Postgres吞吐量跟踪](https://blog.2ndquadrant.com/pg-phriday-terrific-throughput-tracking/)
您是否知道可以使用Postgres的一些内置信息功能来监控实例的吞吐量？

`SHAUN THOMAS（2NDQUADRANT 第二象限)`

## [适用于PostgreSQL的Amazon RDS现在支持T3实例类型](https://aws.amazon.com/about-aws/whats-new/2019/01/amazon-rds-postgresql-now-supports-t3-instance-types/)
适用于AWS用户。 T3实例是'burstable'实例的新形式，特别适合间歇使用。

`亚马逊网络服务公司`

## [Postgres监控工具pgwatch2的主要功能更新](https://www.cybertec-postgresql.com/en/major-feature-update-for-the-pgwatch2-postgres-monitoring-tool/)
pgwatch2是一个流行的独立Postgres指标监控和仪表板系统。

`KAAREL MOPPEL`

## [电子书：优化Postgres查询性能的最佳实践](https://pganalyze.com/ebooks/optimizing-postgres-query-performance?utm_source=PostgresWeeklySecondary)
在这个免费的pganalyze eBook中，你可以了解如何在Postgres数据库中获得3倍的性能提升，以及从磁盘加载的数据减少500倍。

`PGANALYZE` *赞助商*

## [Postgres后端的流程图](https://www.postgresql.org/developer/backend/)
Postgres如何在幕后工作的图表。 您可以单击每个项目以获取更多信息。

`POSTGRESQL全球开发组`

## [与Postgres运营商一起安排备份](https://info.crunchydata.com/blog/schedule-pgbackrest-backups-with-the-postgres-operator)
一个可靠的灾难恢复计划（Postgres集群与pgBackRest和Crunchy PostgreSQL运算符相结合）将帮助您使用少量命令管理数千个实例的备份。

`JONATHAN S. KATZ`

# ![_config.yml]({{ site.baseurl }}/images/Tips-icon.png)   本周提示

如何可视化您的查询计划

![v plan](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/n5lbz4p2vrgwjxh1nvin.jpg)

[*EXPLAIN命令*](https://www.postgresql.org/docs/current/sql-explain.html)显示Postgres的计划程序为提供的SQL语句生成的执行计划，该语句允许您查看获取所需结果所需的方法。 是否使用了索引（以及哪些索引），加入了哪些表，使用了哪些连接算法等等。

然而，以原始形式可视化和理解输出可能有点棘手，但幸运的是，有一个免费的在线工具可以提供帮助。

使用ANALYZE，COSTS，VERBOSE，BUFFERS和FORMAT JSON选项运行EXPLAIN查询，然后将结果以及查询粘贴到[Postgres EXPLAIN Visualizer](http://tatiyants.com/pev/#/plans/new)中。

> 本周的技巧由[strongDM](https://postgresweekly.com/link/58601/web)赞助，这是保护您访问服务器/数据库的最佳方式。 [安排10分钟的演示](https://postgresweekly.com/link/58601/web)

