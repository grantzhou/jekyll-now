---
layout: post
title: PostgreSQL 每周新闻 2019-1-23
---

### PostgreSQL每周新闻#289 - 2019年1月23日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)

备注：[英文原文地址](https://postgresweekly.com/issues/289)

![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/sziczpdxe73ycmfdl5vm.jpg)

## [Postgres的JSON功能概述](https://severalnines.com/blog/overview-json-capabilities-within-postgresql)
大约六年前，本地JSON支持登陆Postgres 9.2，并为Postgres世界带来了文档数据库的一些好处。 尽管如此，事情已经取得了进展，本博客概述了这些进展。

`VENKATA NAGOTHI`

## [如何在不添加单字节存储的情况下解决Postgres中的存储问题](https://hakibenita.com/how-we-solved-a-storage-problem-in-postgre-sql-without-adding-a-single-bytes-of-storage)
关于ETL任务中存储大量查询的简短故事以及解决该问题的方法。

`HAKI BENITA`

## [使用Telegraf和InfluxDB监控PostgreSQL数据库](https://www.influxdata.com/blog/monitoring-your-postgresql-database-with-telegraf-and-influxdb/)
![img_influxdb](https://copm.s3.amazonaws.com/b8367954.jpg)
本教程将专门介绍设置Telegraf和InfluxDB以监控PostgreSQL的过程。

`INFLUXDATA` **赞助商**

## [pg_permission：检查您的安全性和权限](https://www.cybertec-postgresql.com/en/pg_permission-inspecting-your-postgresql-security-system/)
pg_permission是一个工具，它显示数据库的安全设置，以便您快速了解正在进行的操作以及已授予的权限。

`HANS-JÜRGEN SCHÖNIG`

## [PGLoader：在单个命令中迁移到Postgres](https://github.com/dimitri/pgloader)
基于COPY的数据加载工具,既支持并行又可以加载可能部分错误但不会停止的数据（如\ copy）。

`DIMITRI FONTAINE`

## [Postgres逻辑复制陷阱](https://pgdash.io/blog/postgres-replication-gotchas.html)
这篇文章介绍了使用逻辑复制时需要注意的事项。

`RAPIDLOOP`

## [PostgreSQL的内部结构：简介](http://www.interdb.jp/pg/index.html)
这篇文章介绍了一些最近在社交媒体上进行巡回演讲中谈到的并且在过去的一年中获得了更新的经典问题。

`HIRONOBU SUZUKI`

## [部署和管理PostgreSQL 11](https://severalnines.com/blog/deploying-and-managing-postgresql-11-new-clustercontrol-171?utm_campaign=DB_Speed_Campaign_JAN19&utm_content=pgweekly&utm_medium=Paid_Search&utm_source=banner)
了解新的ClusterControl 1.7.1如何为PostgreSQL提供更高级的监控和管理功能。

`SEVERALNINES` **赞助商**

## [通过TDS外部数据包装器在PostgreSQL中使用Microsoft SQL Server的数据](https://fluca1978.github.io/2019/01/18/PostgreSQL-TDS-FDW.html)
想从Postgres中查询存储在SQL Server中的数据？可以使用外部数据包装器，这篇文章介绍这是如何实现的。

`LUCA FERRARI`

## [Postico：macOS的现代Postgres客户端](https://eggerapps.at/postico/)
Postico是一种商业产品（试用版），但外观优雅，像Mac一样。

`EGGER APPS`

# ![_config.yml]({{ site.baseurl }}/images/Tips-icon.png)   本周提示
 >使用排它约束可防止重期范围重叠 -Brendan Carney
 
 >假设我们正在构建一个产品，用于计划员工在给定时间范围内应该处于哪个位置。 由于员工不能同时在两个地方，我们需要一种方法来确保我们的日期范围都不重叠 - 让我们使用排它约束！
 >(必须启用btree_gist扩展：CREATE EXTENSION btree_gist;）
 >我们的表:
 ```
 CREATE TABLE employee_locations (
  name varchar,
  location varchar,
  start_date date,
  end_date date
);
 ``` 
 >约束:
 ```
 ALTER TABLE employee_locations
  ADD CONSTRAINT unique_location_date_range
    EXCLUDE USING gist ( 
      name WITH =, 
      daterange(start_date, end_date, '[]') WITH &&
    );
 ```
 >现在，让我们插入一条记录，说Brendan应该在1月份的办公室：
 ```
 INSERT INTO employee_locations
  (name, location, start_date, end_date) 
 VALUES 
  ('Brendan', 'Office', '2019-01-01', '2019-01-31');
 ```
 >如果我们现在尝试在任何重叠时间将Brendan放在不同的位置，则约束将不允许：
 
 ```
 INSERT INTO employee_locations 
  (name, location, start_date, end_date) 
VALUES 
  ('Brendan', 'Store', '2019-01-15', '2019-02-15');

ERROR: conflicting key value violates exclusion constraint "unique_location_date_range"
 ```
 
 
>这个"本周提示“由[strongDM](https://www.strongdm.com/?utm_source&utm_medium=email&utm_campaign=2019-01-16%20-%20%5BNL%5D%20-%20%5BSchD%5D%20-%20%5BSDM%5D%20-%20PGW-TIP-JAN)赞助提供，保护对服务器/数据库的访问的最佳方法。
>[安排10分钟的演示](https://www.strongdm.com/?utm_source&utm_medium=email&utm_campaign=2019-01-16%20-%20%5BNL%5D%20-%20%5BSchD%5D%20-%20%5BSDM%5D%20-%20PGW-TIP-JAN)
