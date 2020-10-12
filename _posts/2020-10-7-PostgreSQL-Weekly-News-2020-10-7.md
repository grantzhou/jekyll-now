---
layout: post
title: PostgreSQL 每周新闻 2020-10-7
---
### PostgreSQL每周新闻#376 - 2020年10月7日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)
备注：[英文原文地址](https://postgresweekly.com/issues/376)
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/rvgcorc4aemdvcmrjxdu.jpg)
## [sqlbench：测量和比较SQL查询的执行时间](https://postgresweekly.com/link/96386/web)
“主要用例是开发过程中做简单的CPU绑定查询的基准测试。” 目前仅支持Postgres，但欢迎对其他数据库支持的请求。 用Go语言编写。


`Felix Geisendörfer `
## [使用CTE对未建立索引的大表进行二进制搜索](https://postgresweekly.com/link/96387/web)
这里很有趣。 必须优化查询，但根本不允许对基础架构进行任何更改，包括索引的生成。 这需要一些聪明的想法！


`David Christensen `
## [ScaleGrid现已提供在GCP上托管PostgreSQL](https://postgresweekly.com/link/96388/web)
ScaleGrid是在Google Cloud 平台上管理PostgreSQL的简单方法。 超级用户访问，自定义扩展和慢查询分析等功能。 带上自己的云（BYOC）以降低托管成本，或使用我们的专用托管。 免费试用。


`ScaleGrid `
## [EDB收购2ndQuadrant ](https://postgresweekly.com/link/96389/web)
“公司收购其他公司”很少是一件令人振奋的故事，但EDB（以前称为EnterpriseDB）和2ndQuadrant在Postgres领域占有很大的份额，EDB承诺通过这一收购“进一步推动Postgres”。


`Ed Boyajian (EDB) `
## [什么是PostgreSQL的Azure数据库中的Flexible Server？](https://postgresweekly.com/link/96390/web)
Flexible Server是用于PostgreSQL的Azure数据库的新部署选项，旨在为扩展和成本优化提供更细粒度的控制（例如停止/启动，大量计算，设置自定义维护窗口之类的东西）。


`Sunil Agarwal (Microsoft) `
## [zheap：重新设计Postgres存储引擎以实现更好的数据膨胀管理](https://postgresweekly.com/link/96391/web)
表“膨胀”是指表或索引的大小增加而并没有在实际数据上反映这一点。 zheap是使用能够更高效地运行UPDATE密集型工作负载的存储引擎来控制此类膨胀的方法。


`Hans-Jürgen Schönig `
## [一些VACUUM和ANALYZE最佳实践技巧](https://postgresweekly.com/link/96392/web)
来看看可能引起混淆的两个重要且常用的功能。这意味着一些最佳实践可能会非常有用。


`Sadequl Hussain `
## [为什么你会想把Heroku Postgres迁移到AWS RDS](https://postgresweekly.com/link/96398/web)
如果您使用的是Heroku，他们的Postgres产品非常棒，但是这里有一些不使用它的论点，如果您在欧洲或担心GDPR，它甚至可能会有不和法规的后果。


`Paweł Urbanek opinion`
## [dropdb --force，Postgres 13的一项新功能](https://postgresweekly.com/link/96393/web)
热衷于即使客户端连接到数据库也能尽快删除数据库？ 现在您可以了！😂您还可以将FORCE与DROP DATABASE一起使用。


`Ibrar Ahmed `
## [如何加快Postgres查询的最佳做法。 免费电子书](https://postgresweekly.com/link/96394/web)
我们分享了帮助Atlassian，Robinhood等公司加快查询速度的经验。


`pganalyze `
## [如何使用PG Extras解决Postgres性能问题](https://postgresweekly.com/link/96395/web)
一个介绍可用于在Node，Elixir和Ruby上发现Postgres相关问题的工具。 node-postgres-extras是您想要的存储库。


`Paweł Urbanek `
## [Postgres 13的功能摘要](https://postgresweekly.com/link/96397/web)
如果您上周没有赶上我们的问题，则可以快速轻松地阅读Postgres 13的主要功能摘要。


`Kovid Rathee `
![img](http://www.dbcrossbar.org/dbcrossbar_guide_0.generated.svg)
## [dbcrossbar：在不同的数据库和格式之间移动大型数据集](https://postgresweekly.com/link/96399/web)
在数据库，CSV文件和云存储之间复制表格数据。 用Rust语言编写


`Faraday, Inc. `
## [Arctype：适用于Postgres和MySQL的桌面SQL客户端](https://postgresweekly.com/link/96400/web)
当我看到有人在推特上说这是“我使用过的最漂亮的客户端”时，我不得不看一下。 电子表格样式的数据编辑。 Beekeeper Studio是另一个值得一试的地方，我们可能会写更多相关文章。


`Arctype `
