---
layout: post
title: PostgreSQL 每周新闻 2020-7-29
---
### PostgreSQL每周新闻#366 - 2020年7月29日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)
备注：[英文原文地址](https://postgresweekly.com/issues/366)
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/v1595950939/pdxtnv3dfcatkcqy8k0d.png)
## [什么是“填充因子”及其如何影响性能？](https://postgresweekly.com/link/92500/web)
“填充因子”定义了表存储的紧密程度。例如，当更新一行时，由于大小限制，“新”行可能会在不同的存储页中结束，而紧凑的表可以使更新几乎就地进行。


`Kaarel Moppel `
## [SQL样式指南](https://postgresweekly.com/link/92501/web)
几年前我们已链接到此指南，但Bruce Momjian提醒我们该方便的SQL样式指南，以确保可读性和可维护性的查询。


`Simon Holywell `
## [案例研究:全球游戏公司成功迁移到PostreSQL](https://postgresweekly.com/link/92502/web)
了解2ndQuadrant如何帮助国际游戏技术（IGT）从昂贵且专有的DBMS成功迁移到PostgreSQL，从而在全球范围内提供高质量的游戏体验，以及他们如何体验零体验自切换以来发生中断。


`2ndQuadrant PostgreSQL Services `
## [Postgres 13中的Unicode规范化](https://postgresweekly.com/link/92503/web)
如果您对Unicode的“完全组合”或“完全分解”的含义一无所知，或者在考虑Unicode字符串的相等性时Postgres所做的工作一无所知，那么这是对您的一些想法的简短而精妙的介绍。可能不需要详细了解，但应该了解。


`Peter Eisentraut `
## [避免在日志文件中输入密码](https://postgresweekly.com/link/92504/web)
“因为Postgres使用SQL查询来管理用户帐户，包括密码分配，所以密码可能会出现在服务器日志中。”


`Bruce Momjian `
## [Postgres中更安全的价格类型](https://postgresweekly.com/link/92505/web)
是否值得通过创建域/类型而不是仅在数字列中遵循美分来对价格进行建模？ 


`Vados `
## [Postgres 13的解释现在包括WAL信息](https://postgresweekly.com/link/92507/web)
您将能够看到创建了多少WAL记录以及类似信息。


`Luca Ferrari `
## [端到端监视和可视化Postgres数据库度量标准](https://postgresweekly.com/link/92508/web)
使用OOTB，Datadog中的可自定义的拖放式仪表板端到端监视PostgreSQL性能。免费尝试


`Datadog `
## [使用Postgres.app在macOS上安装TimescaleDB](https://postgresweekly.com/link/92509/web)
TimescaleDB是流行的时间序列数据Postgres扩展，而Postgres.app是在Mac上运行Postgres的同样流行的方式。本教程将两者结合在一起。


`Prathamesh Sonpatki `
## [将自定义类型与Citus和Postgres结合使用，从流行的技巧到透明功能](https://postgresweekly.com/link/92512/web)
自定义类型如何与Citus一起使用，以及用户定义的PostgreSQL类型如何自动传播到Citus集群中的所有节点。


`Nils Dijk `
## [Postgres性能调优和优化](https://postgresweekly.com/link/92513/web)
▶长达一个小时的演讲，着重于调优配置设置（在Postgres和Linux中都是如此）以及它们各自会影响什么。


`Ibrar Ahmed (Percona) `
## [在EuroPython 2020上在线演讲的感觉](https://postgresweekly.com/link/92514/web)
一位演讲者分享了在在线会议上演讲的一些经验。


`Paolo Melchiorre `
## [GGoodJob：一个新的基于Postgres的Ruby on Rails多线程后台作业系统](https://postgresweekly.com/link/92515/web)
Ben称GoodJob为“第二代”后端，因为它着重于与ActiveJob的兼容性。它适合每天排队少于100万个工作的用例。


`Ben Sheldon `
# 💡本周提示


向JSON对象添加约束

我发现将JSONB列开放给任何事物很容易–我经常创建一个JSONB“元数据”列，并将其用作一种通用的存储桶，将数据放入以后可能需要或可能不需要的地方。他们表现出色。

尽管您可以以非常动态的“裤子就座”的方式使用JSON，但是您也可以通过查询，函数和约束将其带入结构化世界。

例如，您可能有一个books表，并在其中将有关书的数据存储为JSON文档：


```
create table books(k serial primary key, doc jsonb not null);

insert into books(doc) values
  ('
    { "ISBN"    : 4582546494267,
      "title"   : "Macbeth", 
      "author"  :
        {"given_name": "William",
         "family_name": "Shakespeare"},
      "year"    : 1623
    }
  ');
```


在这样的表中可能有用的一种约束类型是确保我们甚至拥有某种类型的JSON文档。您可以通过检查文档的类型并确保它是一个对象（即，它具有键和值，而不只是数字10）来实现此目的：


```
alter table books
add constraint books_doc_is_object
check(
  jsonb_typeof(doc) is not null and
  jsonb_typeof(doc) = 'object'
);
```


我们可以通过验证JSON文档中的数据来更进一步。例如，ISBN是一个13位整数，唯一表示一本书（或其他形式的书面材料）。我们可以确保JSON文档中提供的“ ISBN”值是十三位整数，如下所示：


```
alter table books
add constraint books_doc_isbn_ok
check(
  doc->>'ISBN' is not null              and
  jsonb_typeof(doc->'ISBN') = 'number'  and
  (doc->>'ISBN')::bigint > 0            and
  length(doc->>'ISBN') = 13
);
```


此验证将进行一些深度检查，以确认是否存在“ ISBN”值（它是一个数字），然后将其转换为整数以检查其值为正，然后检查其长度等于13。


您可以进一步了解更多，但是新闻通讯会太长，因此请参阅Bryn Llewellyn的JSON数据类型文档数据建模文章，以获取更多信息。它是关于YugabyteDB编写的，但是由于它的JSON支持是基于Postgres构建的，因此大部分内容也适用于Postgres。


**🗓即将举办的Postgres活动**

本周的技巧是由YugabyteDB赞助的，YugabyteDB是用于Internet规模应用程序的高性能分布式SQL数据库。为应用程序提供SQL查询灵活性和云原生敏捷性。
