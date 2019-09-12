---
layout: post
title: PostgreSQL 每周新闻 2019-9-11
---
### PostgreSQL每周新闻#322 - 2019年9月11日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)
备注：[英文原文地址](https://postgresweekly.com/issues/322)
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/v1568155380/jqkp0qfoibvzfmh6l31h.png)
## [postgres升级方法初探](https://postgresweekly.com/link/69678/web)
Postgres12就在眼前了，因此有必要重新了解一下升级Postgres安装所涉及的内容。kaarel研究了三种不同方法的利弊。


`Kaarel Moppel `
## [容器中postgres的高可用性选择探讨](https://postgresweekly.com/link/69679/web)
运行postgres的集群容器需要一个控制器来监视和管理集群。跟着我找寻适合你的方案。


`EnterpriseDB `
## [管理Postgres用户和角色](https://postgresweekly.com/link/69680/web)
这是几个月前的文章了，但我们当时错过了。这真是一个遗憾，因为这是一个关于在postgres中与用户和角色合作的非常好的介绍。


`Yaser Raja `
## [postgres 12的Vacuum改进](https://postgresweekly.com/link/69681/web)
postgres用户有时会抱怨Vacuum维护任务。好吧，Postgres12让这些东西不那么痛苦，而且更容易经常使用。


`Shaun Thomas `
## [什么是sql“关系”？](https://postgresweekly.com/link/69683/web)
这是对“关系”概念的简短而甜蜜的介绍。这不仅仅是您熟悉的持久表，而是“事实上，任何sql查询都定义了一个新的关系。”dmitri本周还发布了一些相关文章，重新介绍了连接和聚合。


`Dimitri Fontaine `
## [从postgres数据库中获取更多信息](https://postgresweekly.com/link/69686/web)
pganalyze总结了他们在如何提高postgres数据库3倍性能方面的经验。很多有用的最佳实践都在这里。


`pganalyze `
## [amazon rds中postgres 12数据库参数的优化](https://postgresweekly.com/link/69687/web)
上周，jignesh向我们展示了如何在amazon rds上使用postgres 12的beta版，现在他将研究如何调整其设置以获得更好的性能。


`Jignesh Shah `
## [如何使用robin操作符在openshift上部署和管理postgres](https://postgresweekly.com/link/69689/web)


`Ankur Desai `
## [在Debian 10上安装pgadmin 4](https://postgresweekly.com/link/69690/web)


`Shahriar Shovon `
## [将postgresql复制到memsql的columnstore中](https://postgresweekly.com/link/69691/web)
如何在postgresql中保存事务数据进行更新的同时，获得memsql查询的columnstore的高性能。


`Oryan Moshe `
# 💡本周提示


将查询结果转换为json


您知道postgres包含一个将查询结果行转换为json的函数吗？它被称为row_to_json。让我们创建一个包含两个人的记录的基本表，以及一个“兴趣”数组列，来处理：


```
CREATE TABLE people
  (name text, age int, interests text[]);

INSERT INTO people (name, age, interests)
  VALUES
  ('Jon', 12, ARRAY ['Golf', 'Food']),
  ('Jane', 45, ARRAY ['Art']);
```


使用row_to_json的最基本方法是使用行构造函数ROW，如下所示：


```
SELECT row_to_json(ROW(name, age, interests)) FROM people;

row_to_json
-----------------------------------
{"f1":"Jon","f2":12,"f3":["Golf","Food"]}
{"f1":"Jane","f2":45,"f3":["Art"]}
```


我们可以看到表中不同类型的数据（字符串、整数、数组）对应输出到结果中，但列名却没有！幸运的是，有一种更好的方法可以通过使用子查询来解决这个问题：


```
SELECT row_to_json(q1) FROM
  (SELECT * FROM people LIMIT 1) q1;

row_to_json
-----------------------------------
{"name":"Jon","age":12,"interests":["Golf","Food"]}
```


它与我们这里的示例没有关系，但是row_to_json有一个可选的第二个参数，可以在某些情况下“美化”输出—要启用它，您可以在上面的示例查询中使用row_to_json（q1，true）。


**🗓即将举办的Postgres活动**
- [PostgresConf Silicon Valley 2019](https://postgresweekly.com/link/69693/web)（9月18日至20日，圣何塞）-时间表（包括培训）现已公布。
- [PostgresConf South Africa 2019](https://postgresweekly.com/link/69694/web)（10月8日至9日，约翰内斯堡）-这是数据库管理和使用postgres的开发人员相互了解的机会。
- [PostgreSQL Conference Europe 2019](https://postgresweekly.com/link/69695/web)（10月15日至18日，意大利米兰）
