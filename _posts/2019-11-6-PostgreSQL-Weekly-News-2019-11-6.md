---
layout: post
title: PostgreSQL 每周新闻 2019-11-6
---
### PostgreSQL每周新闻#330 - 2019年11月6日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)
备注：[英文原文地址](https://postgresweekly.com/issues/330)
## [Postgres 12查询性能测试](https://postgresweekly.com/link/79523/web)
我们很久之前就在期待Postgres12了，但它到底表现如何呢？Kaarel建立了不同规模的压力测试，然而没有明显的结论。


`Kaarel Moppel `
## [在面向行的数据库中构建列压缩](https://postgresweekly.com/link/79524/web)
如何在最新版本的Postgres TimescaleDB时间序列数据扩展中实现91%-96%的压缩。


`Timescale `
## [postgres检查：postgres健康检查工具](https://postgresweekly.com/link/79526/web)
一种诊断工具，对Postgres数据库的运行状况进行“深入分析”，检测问题，并为发现的问题提供建议。v1.3.0刚刚发布。


`Postgres.ai `
## [使用带有Xinetd的HAProxy进行应用程序连接故障转移](https://postgresweekly.com/link/79528/web)
我非常喜欢haproxy，它是一个功能强大但易于管理的TCP和HTTP代理/负载平衡器，所以我期待着本系列的其他部分。


`Jobin Augustine `
## [ K-nearest neighbor 空间分区广义搜索树索引的实现](https://postgresweekly.com/link/79530/web)

`Kirk Roybal `



## [在FreeBSD上安装PostgreSQL 12包](https://postgresweekly.com/link/79531/web)
你必须做一些工作，因为Postgres 12的最终版本还没有在季度包更新中。


`Luca Ferrari `
## [通过ansibe在FreeBSD上安装Postgres](https://postgresweekly.com/link/79532/web)


`Luca Ferrari `
## [PostgREST 6.0：从Postgres数据库提供RESTful API](https://postgresweekly.com/link/79533/web)
这不是新鲜事务，而是一个成熟的项目。

`Joe Nelson et al. `



## [用Ruby管理PostgreSQL的分区表](https://postgresweekly.com/link/79535/web)
pg_partition_manager是一个新的gem，用于在应用程序中添加和过期基于时间的数据时维护需要创建和删除的分区表。


`Benjamin Curtis `
## [发布Pgpool II 4.1.0](https://postgresweekly.com/link/79536/web)
将连接池和负载平衡添加到Postgres4.1引入了语句级负载均衡和自动故障转移。

`Pgpool Global Development Group `



# 💡本周提示

对列内容执行任意搜索的一种简单方法是在查询中使用LIKE子句例如，在一个blog posts表中，此查询可以找到标题包含字符串“Java”的所有posts：

```
SELECT * FROM posts WHERE title LIKE '%Java%';
```

如果您想要创建更详细的查询：

```
SELECT * FROM posts WHERE title LIKE '%Java%' OR title LIKE '%Perl%' OR title LIKE '%Python%';
```

Postgres支持两个名为ANY的SQL操作符和所有可用于对一组值执行单个检查的SQL操作符，我们可以将其与LIKE查询一起使用。

ANY和ALL更常用于子查询，但我们可以将多个相似的匹配模式放入一个数组中，然后将其提供给任意或所有相似的子查询：

```
SELECT * FROM posts WHERE title LIKE ANY(ARRAY['%Java%', '%Perl%', '%Python%']);
```

如果您愿意，还可以使用一种较短的样式编写数组文本：

```
SELECT * FROM posts WHERE title LIKE ANY('{%Java%,%Perl%,%Python%}');
```

当然，虽然这些查询会找到任何与提供的任何模式匹配的标题行，但您也可以使用ALL来确保只返回包含所有模式的标题。

**🗓即将举办的Postgres活动**

- [PG Down Under](https://postgresweekly.com/link/79538/web)（11月15日，澳大利亚悉尼）
- [2Q PGCONF 2019](https://postgresweekly.com/link/79539/web)（2019年12月4日至5日，芝加哥）-一个致力于交流关于世界上最先进的开源数据库的知识的会议：PostgreSQL
- [PgDaySF](https://postgresweekly.com/link/79540/web)（2020年1月21日，旧金山）-将PostgreSQL国际社区带到旧金山和硅谷中心。
- [PgConf.Russia](https://postgresweekly.com/link/79541/web)（2020年2月3日至5日，俄罗斯莫斯科）
- [PGConf India ](https://postgresweekly.com/link/79542/web)（2020年2月26日至28日，印度马哈拉施特拉邦班加罗鲁）
- [pgDay Paris 2020](https://postgresweekly.com/link/79543/web)（2020年3月26日，法国巴黎）