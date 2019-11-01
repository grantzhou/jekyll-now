---
layout: post
title: PostgreSQL 每周新闻 2019-10-30
---
### PostgreSQL每周新闻#329 - 2019年10月30日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)
备注：[英文原文地址](https://postgresweekly.com/issues/329)
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/bog6obt6hjzfyor3p6fz.jpg)
## [使用逻辑复制执行主版本升级](https://postgresweekly.com/link/79143/web)
如果您只是想升级到postgres 12，这里有一些指导。本文将重点介绍一种新的基于逻辑复制升级方法。它提供了安全性和少量的停机时间，但它可能比其他方法更复杂。


`Kaarel Moppel `
## [使用Postgres 12微调全文搜索](https://postgresweekly.com/link/79145/web)
通过各种调整和考虑，让postgres中全文搜索场景的结果更加相关，这是一个有趣而详细的演练。


`Rob Conery `
## [Postgres 12中的虚拟列](https://postgresweekly.com/link/79147/web)
Rob深入研究了生成的列，这些列与其他列一样存储。在这篇文章讲述了生成列的工作原理。


`Rob Conery `
## [使用Percona监控PostgreSQL数据库](https://postgresweekly.com/link/79148/web)
Percona以其专业的数据库服务和工具而闻名，他们有一个名为PMM的开源监控工具，可以与Postgres一起使用。


`Avinash Vallarapu (Percona) `
## [case语句基础](https://postgresweekly.com/link/79150/web)
在第324期中，我们提供了一个关于按顺序使用case的提示。本基本教程提供了更广泛的概述。


`Lori Brok `
## [postgres中使用libpq特性完成无缝应用程序故障转移](https://postgresweekly.com/link/79152/web)


`Avinash Vallarapu `
## [pspg 2.5.0：现在有了“监视模式”](https://postgresweekly.com/link/79153/web)
pspg最初只是一个简单的“分页器”，用于从psql输出查询结果，但现在它可以自己作为一个简单的postgres客户端工作，并在选定的间隔刷新结果。


`Pavel Stěhule `
## [pg_checksums1.0发布](https://postgresweekly.com/link/79156/web)
数据校验和通过检查关机前后的校验和是否匹配来防止数据损坏。


`Michael Banck `
## [64位windows的file_textarray_fdw和odbc_fdw](https://postgresweekly.com/link/79157/web)


`Leo Hsu and Regina Obe `
# 💡本周提示

在第308期中，我们分享了一个使用psql的readline支持搜索旧查询的技巧。

例如，按ctrl+r并键入sel将显示以前运行的select查询，而反复按ctrl+r将返回旧的匹配示例。如果你没有意识到这一点，那条建议很值得一读。

Ctrl+R技术的一个问题是，它依赖于搜索查询中存在的内容，如果我们想添加更多的上下文信息，以便将来查找查询，我们可以做什么？

注释！SQL允许您在查询上添加注释，如下所示：

```
SELECT * FROM users; -- find all people
```

现在，如果您执行Ctrl+R，您可以键入“find all”（或者“people”，比如说“find all”），上面的查询就会出现这是一个简单的、精心设计的示例，在现实世界中，您可以将它用于更复杂的查询，这些查询可能会相互混淆

# 🗓即将举办的Postgres活动

- [PG Down Under](https://postgresweekly.com/link/79158/web)（11月15日，澳大利亚悉尼）-本年度澳大利亚第二次postgres会议。
- [2Q PGCONF 2019](https://postgresweekly.com/link/79159/web)（2019年12月4日至5日，芝加哥）-一个致力于交流关于世界上最先进的开源数据库的知识的会议：postgresql
- [PgDaySF](https://postgresweekly.com/link/79160/web)（2020年1月21日，旧金山）-将PostgreSQL国际社区带到旧金山和硅谷。
- [PgConf.Russia](https://postgresweekly.com/link/79161/web)（2020年2月3日至5日，俄罗斯莫斯科）-一天的辅导和两天的三次会谈。
- [PGConf India ](https://postgresweekly.com/link/79162/web)（2020年2月26日至28日，印度马哈拉施特拉邦班加罗鲁）
- [pgDay Paris 2020](https://postgresweekly.com/link/79163/web)（2020年3月26日，法国巴黎）-了解更多关于世界上最先进的开源数据库的信息。