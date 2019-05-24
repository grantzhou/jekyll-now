---
layout: post
title: PostgreSQL 每周新闻 2019-5-22
---

### PostgreSQL每周新闻#306 - 2019年5月22日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)

备注：[英文原文地址](https://postgresweekly.com/issues/306)

![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/v1558468462/t1lhkqvr0rd77n10qwn5.jpg)

## [不要如此使用Postgres](https://wiki.postgresql.org/wiki/Don%27t_Do_This)
在PostgreSQL的官方wiki上有一个有趣的页面，这里列出了人们在使用PostgreSQL时经常犯的错误，例如“不要使用char（n）”和“不要使用serial”。其中一些自以为是的看法，但有充分理由支持。
`POSTGRES WIKI`



## [2019年PostgresLondon大会安排 🐘 ](https://postgreslondon.org)
加入我们在伦敦的PGConf UK会议，在这里你将会了解到最前沿的postgres技术。你还可以参与专家培训，包括性能调优，PostgreSQL安全性和多主复制。
`2NDQUADRANT POSTGRESQL EVENTS`



## [使用pg_cron调度数据库任务](https://fluca1978.github.io/2019/05/21/pgcron.html)   
pg_cron是一个Postgres的扩展，他可以在一个正在运行的数据库实例中运行一个类似于cron的命令，你可以随意定义运行命令的时间或时间间隔。
`LUCA FERRARI`



## [RUM索引](https://habr.com/en/company/postgrespro/blog/452116/)
几周之前我们链接了一篇关于GIN索引的文章，还是这个作者，他现在又在深入的研究RUM。RUM本质上是gin索引的一种特殊扩展，但现在它不是POstgres的内置索引类型。
`EGOR ROGOV`


## [滥用SECURITY DEFINER函数](https://www.cybertec-postgresql.com/en/abusing-security-definer-functions/)
使用SECURITY DEFINER创建的函数仅仅有创建者所有的权限，这看似是很安全的。这里是一个使用SECURITY DEFINER创建的看起来很安全函数进行的数据库攻击的例子。
`LAURENZ ALBE`



## [Postgres数据库的健康检查](https://www.citusdata.com/blog/2019/03/29/health-checks-for-your-postgres-database/)
 数据库运行一段时间后，数据库程序将会发生很大的变化 - 在这里，Craig建议您可以经常做一些事情以确保数据库的长期健康。
`CRAIG KERSTIENS`



## [充分利用您的Postgres索引 ](https://pgdash.io/blog/postgres-indexes.html)
覆盖索引，部分索引，多值索引等的快速示例和提示。
`RAPIDLOOP`


## [使用PostgreSQL和TimescaleDB提高时序数据库性能](https://severalnines.com/blog/advanced-database-monitoring-management-timescaledb?utm_campaign=DevOps_Campaign_MAY19&utm_content=pgweekly&utm_medium=Paid_Search&utm_source=banner)
了解ClusterControl如何监控，管理和确保时间序列数据的性能。
`SEVERALNINES`



## [考虑多列索引](https://medium.com/pgmustard/multi-column-indexes-4d17bac764c5)
查看多列索引的一些缺点以及如何考虑它们是否适合您的用例。
`DAVID CONLIN`

## [如何使用ClusterControl将Postgres部署到docker容器](https://severalnines.com/blog/how-deploy-postgresql-docker-container-using-clustercontrol)
`SEBASTIAN INSAUSTI (SEVERALNINES)`

## [pgBackRest:一年成长为优秀的数据库备份方案](https://www.percona.com/blog/2019/05/10/pgbackrest-a-great-backup-solution-and-a-wonderful-year-of-growth/)
pgBackRest添加了一些Postgres数据库备份必须具备的功能
`JOBIN AUGUSTINE`




# ![_config.yml]({{ site.baseurl }}/images/Tips-icon.png)   本周提示
由GitPrime提供支持

Domains：将检查约束和默认值捆绑为简单类型的方法

domain是一种轻量级数据类型，具有自己的可选默认值和约束，是一种SQL:2003功能，已在Postgres中支持多年。
例如，假设您想在表上存储成人年龄（> 18），但不是使用整数和检查约束，您可以创建'domain'来完成相同的功能：
```
CREATE DOMAIN adult_age AS INTEGER CHECK (VALUE >= 18);

```
现在这个新的domain或类型能在一个表中使用。
```
CREATE TABLE adults (name text, age adult_age);
            
INSERT INTO adults VALUES ('Ahmed', 17);
→ ERROR: value for domain adult_age
         violates check constraint
         "adult_age_check"
```
你可以为这个类型创建一个索引或者默认值（使用ALTER DOMAIN）.如下设置默认值：
```
ALTER DOMAIN adult_age SET DEFAULT 18;
```
更多信息详见文档：[the domain feature in Postgres' docs. ](https://www.postgresql.org/docs/9.5/sql-createdomain.html)

>本周提示由GitPrime提供支持。获取他们的新领域指南“[工程团队中需要注意的20个模式](https://resources.gitprime.com/books/20-patterns/?utm_source=nl(pgw)&utm_medium=email-nl&utm_campaign=nl(pgw))”的副本，其中充满了可操作的见解，以帮助用数据调试您的开发过程。

🗓  即将举办的Postgres活动  
- [PGCon 2019(5月28-31日,加拿大渥太华)](https://www.pgcon.org/2019/)
- [PostgreSQL Ibiza(六月19-21日, 伊维萨)](https://www.pgibz.io/index.html) —— 这个在西班牙著名的度假岛上举行的会议将会带来“海滩上的Postgres”，同时仍然在一个漂亮整洁的场地上进行会谈和培训。  
- [Postgres Vision 2019(6月24日,波士顿)](https://postgresvision.com/) 
- [PostgresConf Beijing 2019(7月3-6日，中国北京)](https://postgresconf.org/conferences/Beijing)
