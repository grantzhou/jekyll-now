---
layout: post
title: PostgreSQL 每周新闻 2019-04-10
---

### PostgreSQL每周新闻#300 - 2019年4月10日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)

备注：[英文原文地址](https://postgresweekly.com/issues/300)

![pg_img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/x9ttl8oxzxvbn0mhiw6v.jpg)

## [如何提高COUNT(*)的性能](https://www.cybertec-postgresql.com/en/count-made-fast/)
在Postgres中使用count（*）通常很慢。 本文探讨了使用近似和其他的技巧,让计算行数更快的方法。

`LAURENZ ALBE`

## [当漏洞不是漏洞时](https://blog.hagander.net/when-a-vulnerability-is-not-a-vulnerability-244/)
有时一些功能会被标记为记录“漏洞”，例如[CVE-2019-9193](https://nvd.nist.gov/vuln/detail/CVE-2019-9193)和Postgres的COPY TO/FROM PROGRAM功能。如果您在管理Postgres系统，那么在您的部署中值得了解一些潜在的滥用情况。

`MAGNUS HAGANDER`

## [实时Postgres性能监控](https://www.datadoghq.com/postgres-monitoring/?utm_source=Advertisement&utm_medium=CooperPress&utm_campaign=CooperPress-PostgresWeeklyP)
![img](https://copm.s3.amazonaws.com/d400ddf8.png)  
收集开箱即用的自定义PostgreSQL指标，并将其与分布式基础架构，应用程序和日志中的数据相关联。使用Datadog获得实时性能分析并设置智能警报。开始免费试用。

`DATADOG` **赞助商**

## [PGCon 2019现已开放注册](https://www.pgcon.org/2019/registration.php)
今年的Postgres会议将于5月28日至31日在加拿大渥太华举行，包括为期两天的教程，两天的会谈和一次非正式会议。

`PGCON`

## [pgmetrics 1.6.2：从正在运行的Postgres服务器上收集和显示统计信息](https://github.com/rapidloop/pgmetrics)
[主页](https://pgmetrics.io/)有更多信息，包括[示例输出](https://pgmetrics.io/docs/index.html#example)。

`RAPIDLOOP`

## [用显式JOIN子句控制Postgres的Planner](https://www.postgresql.org/docs/11/explicit-joins.html)
直接来自PG文档，但这是一个方便的建议，特别是像我一样的人，你通常会更喜欢ANSI SQL 89的连接方式。

`POSTGRES DOCUMENTATION`

## [为什么hot_standby_feedback可能会产生误导](https://postgresrocks.enterprisedb.com/t5/Postgres-Gems/Why-hot-standby-feedback-can-be-Misleading/ba-p/3172)
在Postgres中设置复制时，hot_standby_feedback是一种可能比您预期的更复杂的功能。

`RICHARD YEN`

## [使用Slony实现从旧版Postgres到较新版本的连续复制](https://www.percona.com/blog/2019/04/09/continuous-replication-from-legacy-postgresql-version-using-slony/)
PostgreSQL中的本地流复制仅在运行相同主版本的服务器之间工作，但Slony提供了应用程序级替代方案。

`NICKOLAY IHALAINEN`
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/fi5nogk38qlbv1yo9sky.jpg)  

## [dbdot：为Postgres Schemas生成DOT描述](https://github.com/akarki15/dbdot)
基本上是另一种创建数据库模式图的方法。

`AASHISH KARKI`

## [CockroachDB如何将JSONB引入其分布式数据库](https://www.cockroachlabs.com/blog/json-coming-to-cockroach/)
...加上为什么他们采用Postgres语法。

`COCKROACH LABS` **赞助商**

## [vipsql：用于与'psql'交互的Vim插件](https://github.com/martingms/vipsql)
vipsql2.0版本在几周前问世。

`MARTIN GAMMELSÆTER`

# ![_config.yml]({{ site.baseurl }}/images/Tips-icon.png)   本周提示
由GitPrime提供支持

选择表格行的“样本”

您有一个充满数据的表，您想要选择该数据的随机样本。使用带有RANDOM()指令的SELECT是一种方法，但可能会对大型数据集产生性能问题。 谢天谢地，有一个更好的方法。  
首先，让我们创建一个包含1000行的表 - 数字1到1000：

`CREATE TABLE numbers (number int);`
`INSERT INTO numbers (number)`
`  SELECT id FROM generate_series(1,1000) AS id;`

Postgres 9.5引入了一个新的TABLESAMPLE子句，允许您以不同的方式对表进行采样（默认情况下有2种方式，但可以通过扩展添加更多方式）。让我们从表中检索随机的0.5％的行：

`SELECT * FROM numbers TABLESAMPLE BERNOULLI (0.5);`
` number `
`--------`
`    101`
`    213`
`    278`
`    433`

BERNOULLI从表中选择行的概率为0.5％（统计上我们平均得到5行），但是还有一种更有效的SYSTEM方法，它使用基于块的技术（返回表中的范围/行组时可能有一些缺点）。
您还可以将TABLESAMPLE与其他SQL语句（如UPDATE或DELETE）一起使用，例如，无论出于何种原因，如果您想删除表的30％的行。
如果您不了解[generate_series（）](https://www.citusdata.com/blog/2018/03/14/fun-with-sql-generate-sql/)，请考虑额外提示:-)

> 本周提示由[GitPrime](https://resources.gitprime.com/books/20-patterns/?utm_source=nl(pgw)&utm_medium=email-nl&utm_campaign=nl(pgw))提供支持.获取他们新的指南['工程团队需要关注的20种模式'](https://resources.gitprime.com/books/20-patterns/?utm_source=nl(pgw)&utm_medium=email-nl&utm_campaign=nl(pgw))的副本，其中包含可操作的见解，以帮助您使用数据调试开发过程。

🗓  即将举办的Postgres活动  

 [pgconf.de 2019 (5月10日,莱比锡)](https://2019.pgconf.de/) ——最成功的德语PostgreSQL会议。  
 [PGDay.IT 2019 (5月16-17日,博洛尼亚)](https://2019.pgday.it/en/)  
 [PGCon 2019(5月28-31日,渥太华)](https://www.pgcon.org/2019/) ——一个年度会议，供用户和开发人员见面和讨论Postgres。  
 [Postgres Vision 2019(6月24日,波士顿)](https://postgresvision.com/)  
 
