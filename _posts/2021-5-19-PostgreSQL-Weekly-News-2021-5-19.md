---
layout: post
title: PostgreSQL 每周新闻 2021-5-19
---
### PostgreSQL每周新闻#406 - 2021年5月19日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)
备注：[英文原文地址](https://postgresweekly.com/issues/406)
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/aqkusmfbpbimyreqevdc.jpg)
## [Postgres 2021状态报告](https://postgresweekly.com/link/108161/web)
最近，Timescale，TimescaleDB Postgres扩展背后的人们进行了一项调查，以了解Postgres社区的“状态”。 正如承诺的那样，他们共享了结果（包括原始的匿名数据，如果您想进行自己的分析），尽管受访者的数量不是特别多，但得出了一些有趣的结果：
* 大多数用户将其称为“ Postgres”，而不是“ PostgreSQL”。
* 大多数受访者都在自我管理他们的Postgres安装。
* 到目前为止，AWS是拥有GCP的用户中最受欢迎的云，仅次于第二名。
* pgAdmin 4是使用Postgres的最常用的第三方工具。


`Timescale `
## [PostgreSQL数据库监控仪表板](https://postgresweekly.com/link/108165/web)
使用此InfluxDB模板收集有关PostgreSQL数据库性能的指标，例如IO等待，CPU，使用的数据，磁盘读取时间，磁盘写入时间。 使用InfluxDB Cloud帐户免费试用。


`InfluxData `
## [Postgres 13.3、12.7、11.12、10.17和9.6.22发布](https://postgresweekly.com/link/108166/web)
是的，这是所有Postgres维护的完整更新。 为什么？ 除了通常的错误修复之外，还需要解决三个安全漏洞，包括数组下标计算中的缓冲区溢出以及INSERT ..ON CONFLICT ... DO UPDATE和UPDATE ... RETURNING查询在某些情况下的内存泄漏问题。


`PostgreSQL News `
## [Postgres Pulse：有关Postgres主题的14个视频系列](https://postgresweekly.com/link/108167/web)
▶如果您有一些空余时间，那么比检查EDB涵盖各种Postgres主题的视频（从解决LDAP身份验证问题或使用同步复制到Acrobat）更糟糕。 研究EXPLAIN ANALYZE或减少数据库膨胀。

PSA：三年前，我们链接到annotated.conf，这是postgres.conf数百种设置的便捷注释集合。 现在需要将其更新为Postgres 13标准，但原来的创建者已不在这个领域。 如果可以的话，建议您提出pull request。 （当然，该项目仍然是有用的。）

`Various Speakers `
## [在Postgres中调试随机慢写](https://postgresweekly.com/link/108173/web)
有趣地看一下逐步解决问题并弄清楚需要调整哪些设置以及如何进行调整。


`Sergios Aftsidis `
## [博客文章：使用Postgres运行安全的数据库迁移](https://postgresweekly.com/link/108174/web)
最近的数据库迁移使我们停滞了2分钟。 了解发生了什么以及如何避免相同的错误。


`Retool `
## [另一个Postgres 14亮点：创建表压缩](https://postgresweekly.com/link/108175/web)
即将发布的Postgres 14将具有一个选项，让您可以选择为过大的列指定其他形式的TOAST压缩。


`Michael Paquier `

![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/vanqpuihnkutqcdvb5bl.jpg)
## [彩虹色的psql输出](https://postgresweekly.com/link/108177/web)
如果您想在psql设置中表现出一点自豪感，并且拥有一个可以支持真彩色的终端，那么这是一个适用于macOS和Linux的有趣解决方案。


`Alexander Korotkov `
# 💡本周提示


快速发现性能问题

您是否正在寻找服务器上的性能问题？ 可以考虑pg_stat_statements。 它提供了一种快速有效的方法来查找缓慢的查询。

pg_stat_statements是Postgres随附的模块，但需要通过在postgresql.conf中添加以下行来专门加载：


```
shared_preload_libraries = 'pg_stat_statements';
```

然后重新启动服务器并运行：

```
CREATE EXTENSION pg_stat_statements;
```

pg_stat_statements系统视图将为您提供所有相关信息。 您可以在我们的博客文章“ PostgreSQL：快速检测慢速查询”中了解有关如何执行此操作以及如何发现性能问题的更多信息。

CYBERTEC是您本周的秘诀赞助者，CYBERTEC是您自2000年以来PostgreSQL和Data Science的专业合作伙伴。请在[CYBERTEC](https://postgresweekly.com/link/108178/web)的博客中了解有关PostgreSQL性能的更多信息。