---
layout: post
title: PostgreSQL 每周新闻 2020-8-26
---
### PostgreSQL每周新闻#370 - 2020年8月26日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)
备注：[英文原文地址](https://postgresweekly.com/issues/370)
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/qvohl6d8lsat4yjyyyzj.jpg)
## [为什么Postgres 13是一个”幸运“的版本](https://postgresweekly.com/link/94032/web)
为什么作者认为13（通常被误称为“不幸”数字）会为Postgres带来幸运，它增加了增量排序，并行真空等功能，并改善了B-tree索引。



`Jonathan S. Katz `
## [synchronous_commit选项和同步备用复制](https://postgresweekly.com/link/94013/web)
synchronous_commit使您可以自定义何时将事务执行结果返回客户端，这对复制系统有影响。


`Jobin Augustine `
## [[白皮书]强化数据库的最佳实践](https://postgresweekly.com/link/94015/web)
了解PostgreSQL数据库安全性的基本概念，并对行业的最佳实践有深入的了解。了解如何保护Postgres集群并保护数据安全。确信您的数据库已受到充分保护，免受攻击。


`2ndQuadrant Whitepapers `
## [Postgres 14将有个对大量连接处理的改进](https://postgresweekly.com/link/94016/web)
请注意，这是关于Postgres 14的，因此您还得再等等（因为13还没有发布呢！），但是处理大量连接是一个长期的问题。对于许多人来说，这些与某些讨论线程的链接可能很有趣。


`Hubert depesz Lubaczewski `
## [通过任何Postgres客户端通过”数据传递网络“查询40K+数据集](https://postgresweekly.com/link/94014/web)
Splitgraph提供了他们所谓的“数据传递网络”，其作用类似于与Postgres wire协议兼容的分布式SQL缓存代理。 在此演示中，它使您可以使用psql或您喜欢的其他Postgres客户端，使用SQL查询40,000多个数据集。


`Splitgraph `
## [使用SQL计算标准差](https://postgresweekly.com/link/94018/web)
通常，Postgres为此任务提供了一个函数：stddev（）。


`Bruce Momjian `
## [PostgreSQL13的TLS相关更新概述](https://postgresweekly.com/link/94019/web)
Postgres 13支持最低版本的TLS 1.2，在安全连接方面，包括对通道绑定的支持，Postgres 13发布了一些改进。


`Cary Huang `
## [如何在启用IPv6的网络上设置Postgres](https://postgresweekly.com/link/94021/web)
如果您已经对IPv6非常了解，那么这篇文会比您需要的更深入，但是如果没有，那么您可以在这里找到一些有用的提示。


`David Zhang `
## [针对您所有软件项目来达到更快CI / CD 流程 - 来试试Buildkite✅](https://postgresweekly.com/link/94022/web)
了解Shopify如何将300位工程师扩展到1800位工程师，同时将构建时间保持在5分钟以内。


`Buildkite `
## [pg-costop：向量算术和加权，可变随机余弦相似度搜索](https://postgresweekly.com/link/94017/web)
在数学上，这超出了我一点，但是它是一组PL / pgSQL函数，用于与向量一起计算余弦近似度/相似度排名。


`turbo `
## [pg-shortkey：类似YouTube的短ID作为Postgres主键](https://postgresweekly.com/link/94023/web)
“这工具将会安装触发器和类型，允许您将类似YouTube的短ID（例如1TNhBqYo-6Q）用作Postgres主键。 就像YouTube ID一样，“SHORTKEY” ID是固定长度且URL安全的。”


`turbo `
## [QuestDB：一种注重性能的 “NewSQL” 时间序列数据库系统](https://postgresweekly.com/link/94024/web)
一种关系数据库（它不是基于Postgres构建的，但确实支持其有线协议），专注于快速时间序列数据处理。 内置Java。


`QuestDB Limited `
## [Pgpool-II 4.1.3，4.0.10，3.7.15，3.6.22和3.5.26 的发布](https://postgresweekly.com/link/94026/web)
全面修复了连接池系统的所有维护版本的错误。


`PgPool Development Group `

# 💡本周提示


检查一个行是否存在

您可以通过exists来查看是否返回任何内容来检查行是否存在Postgres表里，但是取决于您执行此操作的方式，结果可能是不明确的或无效的。

EXISTS子查询可用于明确确定另一个查询是否返回任何行，因此可用于检测特定行是否存在：


```
# CREATE TABLE test(id BIGSERIAL PRIMARY KEY);
# INSERT INTO test(id) VALUES (13);
# SELECT EXISTS(SELECT 1 FROM test WHERE id=11) AS "exists";
 exists
--------
 f
(1 row)

# SELECT EXISTS(SELECT 1 FROM test WHERE id=13) AS "exists";
 exists
--------
 t
(1 row)
```

EXISTS始终返回布尔值-true或false。

本周的提示是由YugabyteDB赞助的，YugabyteDB是一种高性能，云原生，开源的分布式SQL数据库。 YugabyteDB EXISTS可帮助您大规模扩展关键业务应用程序。 开始吧！