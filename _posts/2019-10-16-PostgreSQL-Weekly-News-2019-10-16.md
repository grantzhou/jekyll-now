---
layout: post
title: PostgreSQL 每周新闻 2019-10-16
---
### PostgreSQL每周新闻#327 - 2019年10月16日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)
备注：[英文原文地址](https://postgresweekly.com/issues/327)
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/v1571171920/atzjvqowzsi1oceo6pxu.png)
## [不确定排序](https://postgresweekly.com/link/78480/web)
postgres 12支持一个新的确定性属性，在创建排序规则时可以将其设置为false，这使得两个字节不同的字符串可以在既定的排序规则下呗判断为是相等的。这开创了许多与文本匹配的方法，而无需使用显式函数。


`Daniel Verité `
## [预热Postgres的I/O缓存](https://postgresweekly.com/link/78481/web)
postgres缓存的数据的命中率越高，性能就越好。在没有人为干预下，这需要花费很长的时间使内存加载达到最优的状态。我们怎么样能加快这个过程呢？


`Hans-Jürgen Schönig `
## [电子书：要在Postgres日志中监视的最重要事件](https://postgresweekly.com/link/78482/web)
在这本pganalyze电子书中，我们将查看前6个postgres日志事件，用于监视查询性能和防止停机。


`pganalyze `
## [如何在Postgres12中设置流复制](https://postgresweekly.com/link/78483/web)
Percona的Avinash Vallarapu谈到了如何在Postgres12中设置流复制，这基本上是一种让其他服务器对你的实时数据保持同步的方法。


`Avinash Vallarapu `
## [autovacuum是否作用于临时表](https://postgresweekly.com/link/78484/web)
临时表不会被Postgres的vacuum清理，你必须自己清理。下面是原因和方法，并用一个例子来说明。

`Hans-Jürgen Schönig `



## [检查Postgres对象所有权](https://postgresweekly.com/link/78486/web)

一个的查询，它可以列出不属于这个角色的表、视图、外部表和序列。


`Euler Taveira `
## [用于Postgres v2.2.0的Oracle FDW](https://postgresweekly.com/link/78487/web)
用于轻松访问Oracle数据库的外部数据包装器。v2.2.0增加了对foreign表和oracle的xmltype的拷贝支持。

`Laurenz Albe `

## [创建多层安全postgres数据库](https://postgresweekly.com/link/78488/web)
通过观看此按需网络研讨会，了解管理Postgres数据库的安全最佳实践。


`EnterpriseDB `
## [AsyncPg0.19.0:Python/AsyncIO的快速Postgres客户端库](https://postgresweekly.com/link/78489/web)
要使用全新的Python3.8（这周发布），为什么不为Asyncio更新一个新的高性能客户端库呢？现在支持postgres 12和scram-sha-256身份验证。


`magicstack `
## [mobilitydb：一个基于postgresql和postgis的移动对象数据库（mod）](https://postgresweekly.com/link/78490/web)
随着postgis将地理空间对象带到postgres，mobilitydb旨在进一步发挥时间的作用，以表示地理空间中项目的移动。这是目前正在开发/原型，但可能会引起一些人的兴趣。


`ULB-CoDE-WIT `
## [一种传统的手写体识别算法的sql实现](https://postgresweekly.com/link/78491/web)

`Noah Doersing `
# 💡本周提示

你如果经常使用psql，并且想出了一些优秀的的SQL。当你想回顾一下你的SQL，或者想向别人展示一下你在会话中所执行的SQL。如何看你的历史SQL。


检查查询历史记录的最简单方法是：


```
\s
```


很简单，但是你知道你也可以用它将你的历史记录保存到一个文件中吗？


```
# \s queries.log
Wrote history to file "queries.log".
```


**🗓即将举办的Postgres活动**
- [pgDay Santiago](https://postgresweekly.com/link/78492/web)（10月29日在智利圣地亚哥）-面向所有级别的PostgreSQL用户，为每个人提供会谈，并有机会与您的同行见面。
- [PG Down Under](https://postgresweekly.com/link/78493/web)（11月15日，澳大利亚悉尼）-本年度澳大利亚邮政会议的第二次出游。
- [PgConf.Russia](https://postgresweekly.com/link/78494/web)（2020年2月3日至5日，俄罗斯莫斯科）-一天的辅导和两天的三次平行会谈。
- [PGConf India ](https://postgresweekly.com/link/78495/web)（2020年2月26日至28日，印度马哈拉施特拉邦班加罗鲁）-一个专门的培训日和一个多轨道两天会议。

