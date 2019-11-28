---
layout: post
title: PostgreSQL 每周新闻 2019-11-27
---
### PostgreSQL每周新闻#333 - 2019年11月27日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)
备注：[英文原文地址](https://postgresweekly.com/issues/333)
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/vnc1nuiiqncbwmp32vt1.jpg)

## [Postgres 12中B-树索引的改进](https://postgresweekly.com/link/80458/web)
在Postgres v12中，B树索引得到了改进-本文描述了一些易于理解的示例。它不会影响大多数用户，但有一些性能优势，特别是对于存储在随机读取性能差的媒体上的数据库（如磁存储）。

`Laurenz Albe `

## [SQL中的12个常见错误和错过的优化机会](https://postgresweekly.com/link/80459/web)
一个长长的列表，包括时区、范围、格式化查询和联合等主题。

`Haki Benita `

## [Postgres中的多租户选项](https://postgresweekly.com/link/80460/web)
对Postgres体系结构的高级概述有助于对Postgres提供的多租户选项提供一些上下文理解。下载此白皮书以了解有关Postgres三个主要多租户选项的更多信息。

`EnterpriseDB `

## [如何在Postgres 12上开始使用pgBackRest](https://postgresweekly.com/link/80461/web)
pgBackRest是Postgres的备份和恢复工具，现在它利用了Postgres 12中的一些新功能。下面是如何设置和配置它。

`Tom Swartz `

## [使用Puppet部署和配置Postgres](https://postgresweekly.com/link/80463/web)
运行Puppet模块的安装和编程（Puppet是一个流行的开源配置管理和部署系统），用于部署/配置数据库。


`Hugo Dias `
## [PostgreSQL中从异步复制到同步复制的转换](https://postgresweekly.com/link/80465/web)
演示如何从头安装PostgreSQL群集并将异步复制（默认）转换为同步复制。


`Sebastian Insausti `
## [Postgres的VACUUM机制综述](https://postgresweekly.com/link/80466/web)


`Kumar Rajeev Rastogi `
## [关系数据库的求和类型](https://postgresweekly.com/link/80467/web)
查看不同的方法来编码和类型。


`Dmitry Olshansky `
## [等待PostgreSQL 13:允许psql中的不可见PROMPT2](https://postgresweekly.com/link/80468/web)
在总体方案中，这是一个很小的问题，但是Postgres 13中的psql在输入多行查询时会使提示变得更好一些。


`Hubert depesz Lubaczewski `
## [PGLoader：迁移到Postgres的数据加载工具](https://postgresweekly.com/link/80469/web)
一种基于拷贝的数据加载工具，支持并行性，可以加载可能部分错误但不停止的数据（如拷贝）。

`Dimitri Fontaine `

## [pg_simdjson：使用simdjson解析JSON的扩展](https://postgresweekly.com/link/80471/web)
现在这是一个原型/实验，但我喜欢看到这样的东西。这个扩展使用高性能的simdjson解析器（目前为止稍微有点）比Postgres的本地JSON解析器性能好。

`Dmitry Dolgov `

## [pg_query_state：查询进度监控模块](https://postgresweekly.com/link/80479/web)


`Postgres Professional `
# 💡本周提示


**🗓即将举办的Postgres活动**
- [2Q PGCONF 2019](https://postgresweekly.com/link/80473/web)（2019年12月4日至5日，芝加哥）
- [PgDay SF](https://postgresweekly.com/link/80474/web)（2020年1月21日，旧金山）
- [PgConf.Russia](https://postgresweekly.com/link/80475/web)（2020年2月3日至5日，俄罗斯莫斯科）
- [PGConf India ](https://postgresweekly.com/link/80476/web)（2020年2月26日至28日，印度马哈拉施特拉邦班加罗鲁）
- [pgDay Paris 2020](https://postgresweekly.com/link/80477/web)（2020年3月26日，法国巴黎）
- [Swiss PGDay 2020](https://postgresweekly.com/link/80478/web)（2020年6月18日至19日，瑞士）
