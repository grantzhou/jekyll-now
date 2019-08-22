---
layout: post
title: PostgreSQL 每周新闻 2019-8-21
---

### PostgreSQL每周新闻#319 - 2019年8月21日

![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)

备注：[英文原文地址](https://postgresweekly.com/issues/319)

![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/lz4jeabpf7tiuxv8qpna.jpg)

## [Percona推出基于Postgres11的分布式数据库](https://www.percona.com/blog/2019/08/19/percona-distribution-for-postgresql-11-beta-is-now-available/)

Percona，也许因其MySQL性能专业知识而闻名，现在也在活跃在PostgreSQL中。这种Percona风格的Postgres 11分布式数据库包括各种工具和扩展，使Postgres更强大和可扩展。

`BORYS BELINSKY (PERCONA)`

## [使用C创建更快的轻量级触发器函数](https://www.percona.com/blog/2019/08/15/faster-lightweight-trigger-function-in-c-for-postgresql/)

触发器函数或者存储过程经常会用PL/pgSQL编写，如果你要求高性能，你可以尝试使用C来编写它。

`JOBIN AUGUSTINE`

## [在工程团队中需要注意的20种模式](https://resources.gitprime.com/books/20-patterns/?utm_source=nl(pgw)&utm_medium=email-nl&utm_campaign=nl(pgw))

Gitprime的新书汇集了一些最常见的软件团队动态，这是在与数百个企业工程组织合作时观察到的。可操作的洞察力，帮助您用数据调试开发过程。拿到你的拷贝。

`GITPRIME`**赞助商**

## [在不停机的情况下改变Postgres的用户密码](https://www.jannikarndt.de/blog/2018/08/rotating_postgresql_passwords_with_no_downtime/)

实现思想是创建分离的role，使得在删除旧的密码之前有两个活动的密码同时存在。

`JANNIK ARNDT`



## [移植Postgres插件到windows系统](http://www.myrkraverk.com/blog/2019/08/porting-a-postgresql-extension-from-unix-to-windows-10/)

从头开始构建自己的Postgres扩展是一回事，移植现有的扩展以支持不同的操作系统是另一回事，特别是当Windows是目标时。你们中很少有人不太可能需要这样做，但这些笔记可能是非常宝贵的。

`JOHANN ‘MYRKRAVERK’ OSKARSSON`



## [同时开发很多Postgres版本的过程](https://www.2ndquadrant.com/en/blog/developing-on-many-versions-of-postgresql-at-once/)

`CRAIG RINGER`



## [怎么简单的管理Postgres的权限](https://www.percona.com/blog/2019/08/02/out-of-memory-killer-or-savior/)

strongDM可以让您了解发生的事情，replay和分析事件。你无法在其他地方获得这样的功能。

`STRONGDM`



## [克隆模式的函数](http://www.pateldenish.com/2019/08/clone-schema-in-postgres.html)

开发人员需要一个函数来克隆/复制Postgres中的模式，将其修复以支持物化视图，并在此处重新发布。

`DENISH PATEL`



## [pgsodium:一个使用libsodium的Postgres插件](https://github.com/michelp/pgsodium)

libsodium是一个用于加密，解密，签名，密码散列等的加密库。

`MICHEL PELLETIER`



# 💡本周提示

###### 在你的数据库对象中添加注释

由CHAOS CONF提供



您是否知道Postgres支持在数据库中存储几乎任何内容（例如列，角色，域，表，触发器等）的注释？这个过程非常简单。

```sql
COMMENT ON [thing] IS 'your comment goes here'
```

这是一个例子

假设你有一个Postgres数据库。如果使用psql并运行\ dt，则会获得数据库中表的视图以及（空）描述列：

![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/v1566337414/dow9wrabnhefhs5hfaq5.jpg)

'description'字段即为注释评论。让我们设置一个我们自己的：

```sql
COMMENT ON TABLE issues IS 'Newsletter issues';
```

![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/v1566337576/buh3yj5cdcg8rfqfj0jx.jpg)

这是使用注释的绝对最基本的示例，但它们具有更多实用程序（例如，您可以提供更复杂的索引，触发器，过程等的基本描述，这将有助于项目中的其他人理解您的数据库）。您可以在[COMMENT命令文档](https://www.postgresql.org/docs/10/sql-comment.html)中了解更多信息。



本周提示由[Chaos Conf](https://postgresweekly.com/link/68608/web)赞助。



🗓  **即将举办的Postgres活动**  

• [PGDay Austria 2019](https://pgday.at/en/)（9月6日， 维纳·纽斯塔特，奥地利）

• [PostgreSQL Conference Asia 2019](https://2019.pgconf.asia/)（9月8-11日，巴厘岛，印度尼西亚）

• [PostgresOpen 2019](https://postgresweekly.com/link/68304/web) (9月11-13日， 佛罗里达)——两天包含有关PostgreSQL和相关技术的教程和演示文稿。

[PostgresConf Silicon Valley 2019](https://postgresweekly.com/link/68305/web)（9月18-20日，圣荷西）——时间表（包括培训）现已公布

[PostgresConf South Africa 2019](https://postgresweekly.com/link/68306/web)（10月8-9日， 约翰内斯堡）——提供给使用Postgres的数据库管理和开发人员互相了解的机会。

[PostgreSQL Conference Europe 2019](https://postgresweekly.com/link/68391/web)（10月15-18日， 米兰）