---
layout: post
title: PostgreSQL 每周新闻 2019-02-20
---


### PostgreSQL每周新闻#293 - 2019年2月20日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)


备注：[英文原文地址](https://postgresweekly.com/issues/293)

![pg_img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/smn8psobpfnmkotvecyz.jpg)

## [Postgres 11重新确立窗口功能领导力](https://modern-sql.com/blog/2019-02/postgresql-11)
在竞争对手中，PostgreSQL 11再次提供了最好的OVER子句支持，以及Postgres 11的过程功能与MariaDB和SQL Server等其他系统的比较。

`MARKUS WINAND`

## [Postgres 11.2,10.7,9.6.12,9.5.16和9.4.21发布](https://www.postgresql.org/about/news/1920/)
一系列版本发布通常意味着许多广泛适用的错误修正已经到位......这也是正确的，但主要的改进是Postgres使用fsync（），就像我们[上周](https://postgresweekly.com/issues/292)报道的那样，到目前为止[有些问题](https://fosdem.org/2019/schedule/event/postgresql_fsync/)。

`POSTGRESQL GLOBAL DEVELOPMENT GROUP`

## [PostgreSQL的监控指标](https://www.influxdata.com/blog/metrics-to-monitor-in-your-postgresql-database/)
![img](https://copm.s3.amazonaws.com/e973d6f1.jpg)
在数据库性能方面，您需要跟踪几个关键指标，并且它们并非都是特定于数据库的。

`INFLUXDATA` **赞助商**

## [SQL：最有价值的技能之一](http://www.craigkerstiens.com/2019/02/12/sql-most-valuable-skill/)
Citus Data的Craig Kerstiens解释了为什么在他职业生涯中所获得的所有技能中，SQL仍然是最有价值的。

`CRAIG KERSTIENS`

## [DigitalOcean推出Managed Postgres服务](https://blog.digitalocean.com/announcing-managed-databases-for-postgresql/)
DigitalOcean加入其他提供商之列，如AWS，Google，MS Azure和Heroku，提供Postgres实例的管理。如果您预算紧张的话，这些看起来特别棒。这是[已安装扩展的列表](https://gist.github.com/peterc/e4f7a288ed0eb7e4ffe2d8383a086306)（包括TimescaleDB）。

`DIGITALOCEAN`

## [你需要多少maintenance_work_mem？](https://rhaas.blogspot.com/2019/01/how-much-maintenanceworkmem-do-i-need.html)
work_mem是数据库的关键配置，但如何配置可能会让您感到困惑。Postgres的提交者Robert Hass强调了这个问题并试图解释原因。

`ROBERT HAAS`

## [使用Barman的Postgres地理冗余备份](https://blog.2ndquadrant.com/geo-redundancy-postgresql-database-backups-barman/)
[Barman 2.6](https://www.pgbarman.org/barman-2-6-released/)引入了对地理冗余的支持，这意味着Barman现在可以从另一个Barman实例复制，而不仅仅是Postgres数据库。

`GABRIELE BARTOLINI`

## [PostgreSQL的Master-Replica和Master-Master架构](https://severalnines.com/blog/postgresql-high-availability-master-slave-master-master-architectures?utm_campaign=Migrate_CS_OS_Campaign_FEB18&utm_content=pgweekly&utm_medium=Email&utm_source=Link_Click)
了解实现PostgreSQL环境高可用的不同方法。

`SEVERALNINES` **赞助商**

## [用Postgres Goggles On查看MySQL 8](https://www.cybertec-postgresql.com/en/looking-at-mysql-8-with-postgresql-goggles-on/)
如果你是一个深度的Postgres用户，你可能多年没有使用过MySQL了。但是，如果你很好奇现在的MySQL是什么样的，Kaarel已经帮你了解了，甚至找到了在Postgres中受欢迎的一些功能。

`KAAREL MOPPEL`

## [如何计算SQL中的累积百分比](https://blog.jooq.org/2019/02/14/how-to-calculate-a-cumulative-percentage-in-sql/)

`LUKAS EDER`

## [什么是Citus？ Postgres的横向扩展集群和分片](https://www.xaprb.com/blog/citus/)
微软几周前[收购Citus Data](https://blogs.microsoft.com/blog/2019/01/24/microsoft-acquires-citus-data-re-affirming-its-commitment-to-open-source-and-accelerating-azure-postgresql-performance-and-scale/)，但他们的技术能做什么？ 这是一个很好的高水平的解释。

`BARON SCHWARTZ`

## [兼容Postgres的Amazon Aurora支持PG 10.6](https://aws.amazon.com/cn/about-aws/whats-new/2019/02/amazon-aurora-with-postgresql-compatibility-supports-postgresql-10-6/)

`AMAZON WEB SERVICES`

# ![_config.yml]({{ site.baseurl }}/images/Tips-icon.png)   本周提示
由Citus Data提供支持

## 如何检查表缓存的有效性

缓存是使任何数据库更快并避免大量不必要的工作的重要因素，例如昂贵的磁盘读取。

Postgres使用各种类型的缓存来保持平稳运行，但我们将专注于检查表缓存的有效性。

在psql中，选择您的数据库，然后运行以下查询：

`SELECT * FROM pg_statio_user_tables;` 

您可能会发现结果本身有点不透明和混乱，但实际上您可以看到每个表的IO统计信息，包括缓存中提供了多少“块”数据（即heap_blks_hit）。

我们可以将所有这些数据整合到一个更易读的格式中，并使用如下查询：

`WITH y AS (`
  `SELECT`
  `sum(heap_blks_read) AS read,`
  `sum(heap_blks_hit) AS hit`
  `FROM pg_statio_user_tables`
 `) SELECT read, hit, hit / (hit+read)`
   `AS ratio FROM y;`

在我的数据库中，我得到了如下结果：
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/wlanefrlhzlcikqtvtdd.jpg)

我们的新查询将所有相关数字加在一起，以显示发生了多少缓存命中，缓存未提供的频率（heap_blks_read是读取的磁盘块数），我们计算命中数与读取总块数之比。

在这种情况下，我们的缓存有效地工作，命中率几乎是100％。 但是在低内存环境中或当服务器处于特别紧张状态时，您可能会看到较低的数字。请注意这些并准备升级数据库服务器。

可以进一步使用这些检查，并深入了解Craig Kerstiens在Understanding Postgres Performance中所涵盖的索引使用和索引缓存等内容。

> 本周提示由[Citus Data](https://www.citusdata.com/?utm_source=PG_Weekly&utm_medium=email&utm_campaign=sponsor_blog)赞助，现在是微软家族的一部分。[预订演示](https://www.citusdata.com/about/book_demo/?utm_source=PG_Weekly&utm_medium=email&utm_campaign=sponsor_blog)，了解Citus如何将Postgres转换为分布式数据库。
