---
layout: post
title: PostgreSQL 每周新闻 2019-03-13
---

### PostgreSQL每周新闻#296 - 2019年3月13日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)  


备注：[英文原文地址](https://postgresweekly.com/issues/296)  

![pg_img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/knlxlvjcpegpbjnkhsi9.jpg)  

## [LOCK TABLE是如何危害数据库健康的？](https://www.cybertec-postgresql.com/en/lock-table-can-harm-your-database/)
当与自动清空冲突时，经常使用LOCK TABLE会损害您的数据库：“如果经常在表上使用LOCK，那么autovacuum很有可能永远无法成功处理该表。”

`LAURENZ ALBE`

## [数据是您的业务根本](https://pgexperts.com/)
![pgx_img](https://copm.s3.amazonaws.com/27676a9c.png)  
PGX的开源专家提供解决数据库问题，加速现有应用程序，重构基础架构和开发新应用程序所需的数据库和应用程序技能。

`POSTGRESQL EXPERTS, INC.` **赞助商**

## [一些Postgres最佳实践](https://blog.digitalocean.com/some-postgres-best-practices/)
对主键使用BIGINT或UUID，保持凭证轮换，并使用连接池。

`KENNETH REITZ (DIGITALOCEAN)`

## [Postgres的地理定位](https://tapoueh.org/blog/2018/08/geolocation-with-postgresql/)
查看将地理位置数据加载到Postgres数据库，然后进行查询来根据地理位置定位IP的过程。

`DIMITRI FONTAINE`

## [对Amazon Aurora PostgreSQL进行基准测试](https://severalnines.com/blog/benchmarking-managed-postgresql-cloud-solutions-part-one-amazon-aurora)
管理PostgreSQL服务的一系列文章中的第一篇。

`SEVERALNINES`

## [PostgreSQL部署时要注意的7件事](https://pgdash.io/blog/postgres-things-to-monitor.html)
最大化性能并建立PostgreSQL部署的可靠预测。

`PGDASH` **赞助商**

## [获得2个表中列的平均值的差异](https://stackoverflow.com/questions/55111576/difference-of-averages-of-columns-in-2-tables-in-postgres-database)
这个方法非常直观。

`STACK OVERFLOW`

## ▶[调整PostgreSQL以实现高写入](https://www.youtube.com/watch?v=xrMbzHdPLKM)
来自硅谷PostgresOpen的怀旧经典。
**译者：** 访问Youtube需要翻墙软件，我们已经提前下载好，在本公众号发送 PGWV19031301 , 我们将回复您一个百度下载链接。

`GRANT MCALISTER`

## [快速了解Hasura：Postgres上的GraphQL守护进程](https://redmonk.com/jgovernor/2019/03/11/quick-take-on-hasura-a-daemon-for-graphql-on-postgres/)

`JAMES GOVERNOR`

## [PostGIS 2.5.2,2.4.7,2.3.9发布](http://postgis.net/2019/03/11/postgis-patches/)
这是一个相对较小的错误修复版本，但如果您希望使用的话，需要首先能够对[Proj 6](http://blog.cleverelephant.ca/2019/02/proj4-postgis.html)进行编译。

`POSTGIS DEVELOPERS`

# ![_config.yml]({{ site.baseurl }}/images/Tips-icon.png)   本周提示
由strongdm提供支持

用于将数字四舍五入十分位、百分位的SQL技巧

您可能熟悉SQL ROUND函数，它允许您将数字舍入到最接近的整数或一定数量的小数位：

`SELECT ROUND(123.456); `
`   # => 123  `

`SELECT ROUND(123.456, 2);  `
`   # => 123.46 `

但是，你也可以用负数来舍掉数十、数百和其他数量级的数字：


`SELECT ROUND(123.456, -2);  `
`  # => 100  `
` ` 
`SELECT ROUND(123.456, -1);  `
`  # => 120  `
  

这也适用于MySQL，Oracle和SQL Server，但不适用于SQLite。

> 这个“本周提示”由[strongDM](https://www.strongdm.com/product/?utm_source=email&utm_medium=email&utm_campaign=2019-03-08%20-%20%5BNL%5D%20-%20%5BSchD%5D%20-%20%5BSDM%5D%20-%20COMPANY-LIST)赞助。Hearst，SoFi和Peloton的团队信任strongDM来管理工程师对所有事物的访问。

🗓  即将举办的Postgres活动  

 [pgDay Israel 2019 (3月14日，以色列)](https://pgday.org.il/)  
 [Nordic PGDay 2019 (3月19日，哥本哈根)](https://2019.nordicpgday.org/)  
 [PGConf APAC 2019 (3月19日，新加坡)](https://2019.pgconfapac.org/)  
 [pgconf.de 2019 (3月10日,莱比锡)](https://2019.pgconf.de/)  
