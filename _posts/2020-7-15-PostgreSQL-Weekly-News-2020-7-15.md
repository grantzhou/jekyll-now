---
layout: post
title: PostgreSQL 每周新闻 2020-7-15
---
### PostgreSQL每周新闻#364 - 2020年7月15日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)
备注：[英文原文地址](https://postgresweekly.com/issues/364)
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/v1594744377/p6foxmu22977srw8jh18.png)
## [PGX：使用Rust构建Postgres插件](https://postgresweekly.com/link/91774/web)
Rust是一种非C或C++语言用于Postgres插件开发的框架。 为什么这是一件好事？ 最近，Rust在更多的前沿圈子中变得非常流行，并且该语言的安全功能使其成为一种引人注目的选择。


`ZomboDB `
## [JSONB：类型的容器](https://postgresweekly.com/link/91775/web)
Bruce提醒我们，JSONB列不仅需要保存数组或地图/哈希等集合，您还可以直接存储字符串，数字和布尔值。


`Bruce Momjian `
## [使用PostgreSQL实现高可用性[白皮书]](https://postgresweekly.com/link/91776/web)
关键的业务应用程序需要其后端数据库集群的高可用性。 探索如何设置和部署最多四个9的企业级高可用性。 在高可用的Postgres集群白皮书中了解功能和优势。


`2ndQuadrant PostgreSQL Products `
## [如何查找一个生于1997年的Postgres bug](https://postgresweekly.com/link/91777/web)
讲述了一个隐藏了23年的一个关于circle数据类型的bug的故事。


`David Zhang `
## [如何使用pgBouncer进行SCRAM](https://postgresweekly.com/link/91782/web)
除了讲述了pgBouncer（连接池）如何使用SCRAM来做身份验证，还可以了解什么是SCRAM身份验证及其工作方式。


`Jonathan S. Katz `
## [什么是Postgres模板？](https://postgresweekly.com/link/91784/web)
我们在之前的“一周提示”中介绍了这一点，但是，如果您不知道什么是模板数据库以及如何使用它们，那么这篇文很适合你。


`Angelico de los Reyes `
## [外部数据包装器FDW：Postgres的秘密武器？](https://postgresweekly.com/link/91785/web)
外部数据包装器（通常简称为FDW）使您可以直接从PostgreSQL实例中查询远程数据库，这是它与Splitgraph（用于构建和使用“数据图像”的工具包）一起工作的方式。


`Artjoms Iškovs (Splitgraph) `
## [分布式SQL击败了构建微服务的Polyglot持久性](https://postgresweekly.com/link/91786/web)
Polyglot持久性是版本发布的无声杀手； 分布式SQL是当今多云时代的答案。


`YugabyteDB `
## [PgTyped：TypeScript中的T类型安全 SQL](https://postgresweekly.com/link/91787/web)
在TypeScript中使用具有保证类型安全性的原始SQL。


`Adel Salakh `
## [pgsodium：使用libsodium的Postgres扩展](https://postgresweekly.com/link/91788/web)
libsodium是一个加密，解密，签名，密码哈希等的加密库。 我们之前发布了Alpha，现在是1.0 ：-)


`Michel Pelletier `
# 💡本周提示
RANK和DENSE_RANK用于排名顺序

拿人们最喜欢的数据库系统为例子，产生了以下的例子：
```
CREATE TABLE databases (name TEXT, votes INT);
INSERT INTO databases VALUES
  ('Postgres', 10000),
  ('MySQL', 4522),
  ('SQLite', 9500),
  ('MongoDB', 4522),
  ('Oracle', 4580),
  ('Redis', 9500);
```
我们想要按顺序获得结果以及每个数据库的位置等级：

```
SELECT row_number() OVER (ORDER by votes DESC), * FROM databases;
```
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60,g_north,h_410,c_crop/cxvt9iro8cn0hlby7ey8.png)

尽管Redis与SQLite的票数相同，但Redis仍排名第三，这对我来说似乎并不公平！ 现实世界中的排名通常会记录同等/并列的得分，并对相似得分的项目赋予相同的排名。

输入RANK和DENSE_RANK，这是几个窗口函数中的两个：

```
SELECT DENSE_RANK() OVER (ORDER by votes DESC), * FROM databases;
SELECT RANK() OVER (ORDER by votes DESC), * FROM databases;
```
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/v1594652204/y9ccymacboucz3zeyc5m.png)
区别是细微的，但是RANK为我们提供了一种更传统的排名方法，即如果有两个第二名的条目，就不再有第三名的条目。 使用DENSE_RANK的话，即使有重复，也可以确保连续排名。

⚡️快速事实：
* DigitalOcean的托管数据库服务现在支持Postgres 12。
* 卢卡·法拉利（Luca Ferrari）从PG-US的邮件中收到了Postgres 12纪念币。
* Luca还希望鼓励您测试Postgres 13 beta 2。
* PGConf.EU 2020已取消。

