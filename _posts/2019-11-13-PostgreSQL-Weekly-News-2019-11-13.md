---
layout: post
title: PostgreSQL 每周新闻 2019-11-13
---
### PostgreSQL每周新闻#331 - 2019年11月13日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)
备注：[英文原文地址](https://postgresweekly.com/issues/331)
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/qizvk13bwmujrec9jwd1.jpg)

## [使用auto-explain解决疑难杂症](https://postgresweekly.com/link/79790/web)
`Richard Yen `

## [通过在Azure上扩展Postgres来构建PB级的分析](https://postgresweekly.com/link/79791/web)
这是一个非常严肃的Postgres部署，它在Azure使用Citus的Postgres扩展来扩展Postgres到管理1.5petabytes数据。

`Claire Giordano `



## [使用Postgres作为发布/订阅的服务器](https://postgresweekly.com/link/79793/web)
如果你正在构建一个需要某种发布/订阅机制的应用程序，Postgres可以胜任这项工作，下面介绍LayerCI是如何使用它的。


`LayerCI `
## [利用Postgres实现k-anonymity](https://postgresweekly.com/link/79794/web)
新版本的Postgres anonymity获得了一种新的数据屏蔽形式，即泛化，其中的值被舍入/模糊以降低准确性。这有助于降低仅凭‘简单’值识别数据的几率。

`Damien Clochard `

## [Postgres的gzip扩展](https://postgresweekly.com/link/79796/web)
扩展允许您在Postgres中引入任何您喜欢的功能，Paul构建了一个扩展来引入gzip功能，用于动态压缩和解压缩数据。

`Paul Ramsey `

## [随机查询以揭示顺序相关性](https://postgresweekly.com/link/79797/web)
Conor Cunningham将不带order BY子句的查询顺序等同于驾驶没有安全带的汽车…

`Alex Baldwin `

## [Postgres 12中的流复制设置–如何正确操作](https://postgresweekly.com/link/79798/web)
在Postgres12中，设置流式复制群集的方法略有改变——下面是实践。

`Cary Huang `

## [在Postgres使用pgsql check配置HAProxy](https://postgresweekly.com/link/79799/web)
上周关于使用HAXPROTER和XITED的文章的后续报道，这次查看HaPosits内置的PGSQL检查健康检查功能，用于检测PASGRESs服务器是否仍在运行，以及它是什么类型的服务器。

`Jobin Augustine `

## [PostgreSQL Anonymizer 0.5发布](https://postgresweekly.com/link/79800/web)
对个人识别信息（PII）或商业敏感数据进行屏蔽或替换的扩展。


`Dalibo Labs `
## [设计用于Postgres12的pgAdmin3](https://postgresweekly.com/link/79801/web)
pgAdmin是一个流行的基于Web的Postgres管理，版本4已经发布。。但是如果你需要在Postgres 12中使用版本3（就像Abdul那样），这个fork可以帮助你。

`Abdul Yadi `

## [由DigitalOcean管理PostgreSQL](https://postgresweekly.com/link/79803/web)
部署一个高度可伸缩的PostgreSQL集群，不需要管理开销。


`DigitalOcean `
## [用于FreeBSD引导加载程序的PostgreSQL ASCII徽标](https://postgresweekly.com/link/79804/web)
如果你是一个FreeBSD用户，这是非常有趣的，尽管ASCII艺术在这里（归功于Oleg Bartunov）。

`Luca Ferrari `



**🗓即将举办的Postgres活动**

- [2Q PGCONF 2019](https://postgresweekly.com/link/79806/web)（2019年12月4日至5日，芝加哥）-一个致力于交流关于世界上最先进的开源数据库的知识的会议：PostgreSQL
- [PgDay SF](https://postgresweekly.com/link/79807/web)（2020年1月21日，旧金山）
- [PgConf.Russia](https://postgresweekly.com/link/79808/web)（2020年2月3日至5日，俄罗斯莫斯科）
- [PGConf India ](https://postgresweekly.com/link/79809/web)（2020年2月26日至28日，印度马哈拉施特拉邦班加罗鲁）
- [pgDay Paris 2020](https://postgresweekly.com/link/79810/web)（2020年3月26日，法国巴黎）-在同行中了解更多关于世界上最先进的开源数据库的信息。

