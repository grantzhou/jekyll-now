---
layout: post
title: PostgreSQL 每周新闻 2020-1-22
---
### PostgreSQL每周新闻#339 - 2020年1月22日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)
备注：[英文原文地址](https://postgresweekly.com/issues/339)
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/xpyf1wye3qouyslhgaz7.jpg)

## [追踪Postgres性能问题（Twitter线程）](https://postgresweekly.com/link/82620/web)
一位开发人员发现，在运行了一个新优化的ETL过程之后，只对数据库进行索引扫描的速度慢了3倍，并着手确定原因。

`Felix Geisendörfer on Twitter `

## [pgwatch2 v1.7.0发布](https://postgresweekly.com/link/82621/web)
pgwatch2是一个流行的Postgres度量仪表板和监控系统，1.7.0引入了一些简洁的功能，如日志解析和额外的仪表板。

`Kaarel Moppel `

## [PostgreSQL 13中的vacuum并行处理索引](https://postgresweekly.com/link/82624/web)
在未来，Postgres的vacuum将能够使用多个cpu和内核并行处理索引，从而产生显著的加速。（除此之外，休伯特在本例中设置测试数据的方式非常简洁！）

`Hubert depesz Lubaczewski `

## [在Ruby on Rails中有效地使用物化视图](https://postgresweekly.com/link/82625/web)
Postgres的视图和物化视图提供了通过持久查询查看数据库底层数据的简单替代方法，在Rails中使用它们并不太困难。


`Leigh Halliday `
## [关于如何选择（Postgres）会议演讲的提示](https://postgresweekly.com/link/82626/web)
本周PGDay SF大会的演讲中，有人提供了16条建议。这些小贴士对以后的任何活动都很有用。


`Claire Giordano `
## [Postgres“sleep”的不同方式](https://postgresweekly.com/link/82628/web)
快速看一下pg_sleep，pg_sleep_for和pg_sleep_until，你猜他们会做什么。

`Andreas 'ads' Scherbaum `



## [在Kubernetes上部署高可用PostgreSQL集群](https://postgresweekly.com/link/82630/web)
这依赖于Crunchy Data的（开源）PostgreSQL操作符for Kubernetes。


`Jonathan S. Katz `
## [supabase：将实时和RESTORY API添加到现有PyGRES数据库](https://postgresweekly.com/link/82632/web)
一个使用灵丹妙药的服务器，允许你使用WebSooCube收听插入、更新和删除。

`Supabase `

## [pg_probackup:Postgres的备份和恢复管理器](https://postgresweekly.com/link/82633/web)


`Postgres Professional `
# 💡本周提示


Kaarel Moppel在2020年的文章中总结了一个启动Postgres的技巧和技巧，这篇文章有很多有趣的技巧，值得一看。但最短、最甜蜜的tips突然向我扑来，我想把它放在这里：-）


在处理SQL中的空值时，必须在谓词中使用IS NULL或isnotnull这样的语句：


```
SELECT * FROM people WHERE age IS NOT NULL;
```


但是你知道吗，如果你想保存一些字符，Postgres支持一种较短的（虽然不是标准的）方法？


```
SELECT * FROM people WHERE age NOTNULL;
```


对于IS NULL大小写也有ISNULL，尽管保存的字符数有所减少；-）


如果你想知道为什么你不能去年龄=零或年龄！=NULL，这是因为NULL被定义为“未知”值，而SQL标准要求您不能将“未知”值与另一个值进行比较。


**🗓即将举办的Postgres活动**
- [PgConf.Russia](https://postgresweekly.com/link/82636/web)（2月3日至5日，俄罗斯莫斯科）
- [PgConf India](https://postgresweekly.com/link/82637/web)（2月26日至28日，印度班加罗鲁）
- [Nordic PgDay 2020](https://postgresweekly.com/link/82638/web)（3月24日芬兰赫尔辛基）
- [pgDay Paris 2020](https://postgresweekly.com/link/82639/web)（3月26日，法国巴黎）
- [Swiss PGDay 2020](https://postgresweekly.com/link/82641/web)（6月18日至19日，瑞士）
