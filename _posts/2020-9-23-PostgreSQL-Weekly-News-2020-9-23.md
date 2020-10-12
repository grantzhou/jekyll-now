---
layout: post
title: PostgreSQL 每周新闻 2020-9-23
---
### PostgreSQL每周新闻#374 - 2020年9月23日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)
备注：[英文原文地址](https://postgresweekly.com/issues/374)
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/xwbqrpvcn9myi1fqzxmh.jpg)

## [用Postgres实现的一款战舰游戏](https://postgresweekly.com/link/95548/web)
请参阅SQL在Postgres中运行的工作游戏，并以创造性的方式获取玩家输入。

`Firemoon777 `

## [PostgreSQL 13发布RC1](https://postgresweekly.com/link/95532/web)
如果你没有注意到的话，我们会一直链接到postgres13的东西，而且它正在形成一个巨大的发行版-所以很高兴看到它接近完成这个第一个RC。beta版发行说明涵盖了基本内容，但我们将在最终发行版中对功能进行全面汇总。

`PostgreSQL Global Development Group `

## [迅速的零停机PostgreSQL升级](https://postgresweekly.com/link/95535/web)
获取一个全面的演练如何执行一个“接近”零停机时间升级使用pglogical在这个免费的网络研讨会。了解逻辑解码如何为需要很少停机时间的升级带来全新的机会。

`2ndQuadrant PostgreSQL Webinars `

## [Crunchy Bridge：最新的“Postgres即服务”](https://postgresweekly.com/link/95536/web)
Crunchy Data是最新一家推出了“Postgres as managed service”潮流的公司，它采用AWS和Azure上提供的Crunchy Bridge（并支持两者之间的迁移和复制）。

`Craig Kerstiens (Crunchy Data) `

## [工程师日记：使用Postgres、Citus和t-digest将百分位数提高45倍](https://postgresweekly.com/link/95623/web)
Nils有一个问题要为客户解决，但无法满足30秒的SLA要求，而且没有客户的数据可供实验。。尽管如此，他发现了一种创造性的方法来估计哪种类型的百分位计算能够满足他们的SLA，并使用t-digest进行了计算。

`Nils Dijk (Microsoft) `

## [PostgreSQL13的LIMIT ... WITH TIES](https://postgresweekly.com/link/95537/web)
WITH TIES是Postgres中实现的一个新的SQL标准特性，它使LIMIT（或FETCH FIRST）子句不仅在指定的限制处被截断，而且还包括具有与最后一个（或多个）绑定的值的行。

`Álvaro Herrera `

## [从运行postgres13中学到的经验：更好的性能、监控等](https://postgresweekly.com/link/95540/web)
我们研究了具有B-Tree重复数据消除、并行vacuum、改进的WAL使用情况统计等功能。


`Pganalyze `
## [“HOT”更新如何产生更好的性能](https://postgresweekly.com/link/95538/web)
介绍了Postgres8.3中最早包含的一个特性，但据称这些特性在文档中没有得到适当的介绍。HOT（仅堆元组）发生在后台，并在发生大量更新的特定情况下提高性能。

`Laurenz Albe `

## [用户称，AWS极光Postgres版本“消失”数日](https://postgresweekly.com/link/95539/web)
使用AWS的软件工程师Greg Clough注意到，AWS Aurora上的几个Postgres版本上周“消失”（从某种意义上说，它们无法被部署——现有的数据库并没有消失）。大多数人现在似乎回来了，但这是一个奇怪的故事。

`The Register `

## [PostgreSQL与人工智能](https://postgresweekly.com/link/95541/web)
📄这目前只是PPT），但Bruce的幻灯片往往很有价值。

`Bruce Momjian `

## [探索PL/Python：将Postgres表数据转换为NumPy数组](https://postgresweekly.com/link/95543/web)

`Kat Batuigas `

## [为什么RudderStack使用Postgres而不是ApacheKafka作为流引擎](https://postgresweekly.com/link/95544/web)
卡夫卡很自然地适合于数据平台RudderStack所做的事情，但他们发现了足够多的缺点，转而在Postgres上构建自己的排队系统。

`RudderStack `

# 💡本周提示


```
CREATE TABLE user_login(name TEXT, login_time TIMESTAMP);
```


时间戳类型存储一个完整的日期和时间，包括或不包含时区，而不是分别存储这些特定元素的日期或时间。但是如果你只想返回时间戳所指的日期，那又会怎样呢？


Postgres中有很多日期和时间函数，您可以使用extract逐个提取日期元素：


```
SELECT EXTRACT(MONTH FROM TIMESTAMP '2020-09-21 12:21:13');
SELECT EXTRACT(DAY FROM TIMESTAMP '2020-09-21 12:21:13');
SELECT EXTRACT(YEAR FROM TIMESTAMP '2020-09-21 12:21:13');
```


但最简单的方法是将时间戳类型强制转换为日期，该日期会自动执行所需的转换：


```
SELECT name, login_time::date FROM user_login;
 name | login_time
------+------------
 john | 2019-11-11
 bill | 2020-10-22
 jane | 2020-04-01
(3 rows)
```


（票据从未来登录…）


也可以使用DATE函数以类似的方式创建日期：


```
SELECT DATE('2020-09-21 12:21:13');
# => 2020-09-21T00:00:00.000Z
```


**🗓即将举办的Postgres活动**
