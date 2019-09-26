---
layout: post
title: PostgreSQL 每周新闻 2019-9-25
---
### PostgreSQL每周新闻#324 - 2019年9月25日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)
备注：[英文原文地址](https://postgresweekly.com/issues/324)
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/zuyhvrqygnckzoxroci6.jpg)
## [高级sql：查看“窗口框架”](https://postgresweekly.com/link/77458/web)
深入了解窗口函数的高级用途（如果需要，这里有一个介绍的文章）。窗口框架（window frames）是postgres引入支持的一种sql特性，它允许您将窗口函数提升到更深层次，以执行复杂的聚合。这里有一些很好的例子，必须阅读。


`Michal Konarski `
## [用于postgres的sqlpro-macos和ios数据库客户端](https://postgresweekly.com/link/77460/web)
一个强大的本地ios和macos postgres数据库客户端。轻松浏览和编辑记录，无论是视觉上还是使用真正优秀的查询编辑器。如果您使用postgres，请尝试sqlpro。现在免费使用一年。


`Hankinsoft Development, Inc `
## [Yugabyte DB 2.0 GA:经过“Jepsen测试”的高性能分布式SQL DBMS](https://postgresweekly.com/link/77461/web)
yugabyte db是一个受google Spanner启发的云本地分布式sql数据库，它是100%开源的，旨在在大多数情况下与postgres兼容。


`Kannan Muthukkaruppan `
## [postgres 12中的一些特殊情况性能增强](https://postgresweekly.com/link/77463/web)
PostgreSQL的每一个新版本都有一系列的性能增强，有些是通用的，有些是非常小的。以下是三个非常具体的利基改进。


`John Naylor `
## [azure数据工厂现在可以使用azure database for postgresql作为接收器](https://postgresweekly.com/link/77464/web)
一个仅适用于azure用户，特别是微软数据集成服务azure数据工厂的用户（或潜在用户）。


`Parikshit Savjani `
## [使用行级安全性的一个实例](https://postgresweekly.com/link/77465/web)
向不同类型的用户授予不同权限以处理同一表的示例。


`Hans-Jürgen Schönig `
## [让PostgreSQL 12 Beta 4在6分钟内运行](https://postgresweekly.com/link/77466/web)
演示pgenv如何使postgres更易于安装。


`Luca Ferrari `
## [用pg_cgroup管理postgres中的linux控制组](https://postgresweekly.com/link/77468/web)
pg_cgroups扩展通过使用控制组（也称为cgroups），使您更容易管理linux上postgres集群的资源限制。


`Laurenz Albe `
## [工程团队要注意的20种模式](https://postgresweekly.com/link/77470/web)
可操作的洞察，帮助您用数据调试开发过程。这里可以拿到你的拷贝。


`GitPrime `
## [什么更快？count（*）或count（1）？](https://postgresweekly.com/link/77471/web)
没关系，除非你用的是postgres！


`Lukas Eder `
## [比较分布式sql性能：yugabyte与aurora postgresql与cockroachdb](https://postgresweekly.com/link/77472/web)
现在，你应该知道用怀疑和训练有素的眼光来看待基准，当然，在这种情况下，很高兴看到一个竞争性的服务实际上被推荐用于许多用例。


`YugaByte `
## [sqltools：面向vs代码用户的数据库工具](https://postgresweekly.com/link/77473/web)
支持各种数据库类型（当然是postgres，但cassandra支持也刚刚添加），并提供了连接资源管理器、查询运行器、intellisense、书签、查询历史记录等。


`Visual Studio Marketplace `
# 💡本周提示

**在ORDER BY中使用CASE**

case表达式本质上是的if/then。给定一个值，case可以返回您选择的另一个值，但是您知道您可以在order by子句中使用它来定义基于其他值的排序规则吗？


这里有一个简单的用例。假设您有一张列出员工及其职务的表格：


```
id | name. | title
-------------------
 1 | Oscar | Cleaner
 2 | Carol | CEO
 3 | Jimbo | CFO
 4 | Bobby | Assistant
```


如果您希望根据职务有某种顺序，您可以使用这样的用例：


```
SELECT * FROM employees ORDER BY
  CASE
  WHEN title = 'CEO' THEN 1
  WHEN title = 'CFO' THEN 2
  WHEN title = 'CTO' THEN 2
  ELSE 3
  END;
```


这只是一个展示这个想法的基本例子。在接下来的几周里，我们将深入研究一些更先进的例子。


**🗓即将举办的Postgres活动**
- [PostgresConf South Africa 2019](https://postgresweekly.com/link/77476/web)（10月8日至9日，约翰内斯堡）-这是数据库管理和使用postgres的开发人员相互了解的机会。
- [PostgreSQL Conference Europe 2019](https://postgresweekly.com/link/77477/web)（10月15日至18日，意大利米兰）
- [pgDay Santiago](https://postgresweekly.com/link/77478/web)（10月29日，智利圣地亚哥）
- [PG Down Under 2019](https://postgresweekly.com/link/77479/web)（11月15日，澳大利亚悉尼）-本年度澳大利亚邮政会议的第二次出游。CFP一直开放到下周。
