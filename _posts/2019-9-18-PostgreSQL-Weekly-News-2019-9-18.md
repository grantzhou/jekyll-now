---
layout: post
title: PostgreSQL 每周新闻 2019-9-18
---
### PostgreSQL每周新闻#323 - 2019年9月18日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)
备注：[英文原文地址](https://postgresweekly.com/issues/323)
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/v1568756467/fv8rfbpbbhgwybpch7eh.png)

## [探索Postgres视图的依赖关系](https://postgresweekly.com/link/77091/web)
当您创建涉及相互依赖的表、视图、触发器、函数等的复杂结构时，数据库内部会创建依赖关系。以下是对视图依赖性的探索，以及如何查找视图依赖的其他对象。

`Laurenz Albe `

## [PostgreSQL 12 Beta 4发布](https://postgresweekly.com/link/77092/web)
包含所有功能的预览，这些功能将在postgres 12的最终版本中提供，并且“可能是最终的beta版本”。

`PostgreSQL Global Development Group `

## [向社区核心人员学PG 12的功能](https://postgresweekly.com/link/77114/web)
加入免费的PostgreSQL网络研讨会：与Peter Eisentrut一起加入PostgreSQL 12的新功能，并了解即将发布的PG 12的内部情况。


`2ndQuadrant PostgreSQL Webinars `
## [Postgres备忘单](https://postgresweekly.com/link/77096/web)
15页的Postgres基础使用说明，用于各种Postgres相关任务，包含函数、用户、约束和查询表等。

`Timescale `

## [使用pgpool ii作为负载平衡器可以获得性能吗？](https://postgresweekly.com/link/77097/web)
对少量的连接来说，不会有性能提升。如果有大量的用户连接，YES。运行自己的测试来确定是否需要使用pgpool。

`Muhammad Usama `

## [在postgres 12中分区更快](https://postgresweekly.com/link/77098/web)
postgresql 12对分区做了很多改进。下面是一些基准测试结果，这里您就可以看到性能提升。


`David Rowley `
## [在非postgres数据库中使用distinct on](https://postgresweekly.com/link/77099/web)
我们在321期的技巧文章中提到了distinct on，这是一个用于选择明显匹配各种条件的第一行的简洁功能。但如果你想在其他数据库系统上得到类似的结果呢？


`Lukas Eder `
## [为什么要在关系数据库上使用timescaledb？](https://postgresweekly.com/link/77101/web)
有趣的是，虽然timescaledb是一个时间序列数据库，但它是作为关系数据库postgres之上的扩展而构建的！


`TimescaleDB `
## [Strongdm使管理数据库访问变得轻而易举](https://postgresweekly.com/link/77102/web)
Splunk的CISO说“Strongdm可以让你看到发生了什么，回放和分析事件。”


`strongDM `
## [在RHEL、CentOS或Fedora上安装Postgres 12 Beta/RC](https://postgresweekly.com/link/77103/web)
如何在红帽风格的Linux发行版上测试Postgres的下一个版本。


`Devrim Gunduz `
## [postgres和timescaledb的数据加载性能](https://postgresweekly.com/link/77104/web)
在ec2实例上运行的postgres和timescaledb中加载大量数据（超过十亿行）时测试性能的实验。


`Fabien Coelho `
## [Postgres分页器PSPG 2.0.2发布](https://postgresweekly.com/link/77105/web)
我们在两周前就推出了pspg，但它的创建者已经发布了两个版本，为所有显示的列引入了排序功能。


`Pavel Stěhule `
## [pl/proxy 2.9：基于函数的postgres分片](https://postgresweekly.com/link/77107/web)
如果你不熟悉这个项目，它的主页上会有更多的信息，但是pl/proxy最初是在skype上开发的，目的是通过分片来帮助扩展postgres。

`Luca Ferrari `

# 💡本周提示


神秘的表格命令


做这些小贴士的乐趣之一就是我能发现一些我以前从未见过的有趣的事情。table sql命令是最新的示例。


给出一个简单的示例：


```
CREATE TABLE x (id int);
INSERT INTO x VALUES (10),(20),(30);
```


table允许您快速查看整个表：


```
TABLE x;
  
 id
----
 10
 20
 30
```


它有点幼稚，不支持where或group子句，但支持order、limit和offset。


在我看来，主要的用例是什么？如果您想在psql或类似工具中快速查找表，那么表名比select*from table name；更短，键入起来也不那么麻烦。向不知道的人炫耀是件有趣的事。


如果您有任何文件或参考，为这个命令，尽管，取得联系。我很好奇它是从哪里来的。


**🗓即将举办的Postgres活动**
- [PostgresConf South Africa 2019](https://postgresweekly.com/link/77110/web)（10月8日至9日，约翰内斯堡）-这是数据库管理和使用postgres的开发人员相互了解的机会。
- [PostgreSQL Conference Europe 2019](https://postgresweekly.com/link/77111/web)（10月15日至18日，意大利米兰）
- [pgDay Santiago](https://postgresweekly.com/link/77112/web)（10月29日，智利圣地亚哥）
- [PG Down Under 2019](https://postgresweekly.com/link/77113/web)（11月15日，澳大利亚悉尼）-本年度澳大利亚邮政会议的第二次出游。CFP现在打开了。
