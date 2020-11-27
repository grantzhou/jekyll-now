---
layout: post
title: PostgreSQL 每周新闻 2020-11-25
---
### PostgreSQL每周新闻#383 - 2020年11月25日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)
备注：[英文原文地址](https://postgresweekly.com/issues/383)
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/v1606303422/gfqywyd8zsi60mxgkw50.jpg)
## [Postgres在基于Arm的M1 MacBook Pro上的表现如何？](https://postgresweekly.com/link/99059/web)
苹果公司已经开始推出使用自己基于Arm的M1 CPU的机器，并且最初的性能提升令人印象深刻。 但是，尽管macOS的运行速度比以往更快，但Postgres呢？ 剧透警报..哇？


`Greg Smith `
## [如何将每个类别的行数限制为最多N个](https://postgresweekly.com/link/99061/web)
听起来很简单，但实际上却不那么简单。 这里有很多SQL可以使用（！），如果您有一段时间没有使用触发器，那这篇文将大开你的眼界。


`Hubert depesz Lubaczewski `
## [免费电子书：如何在Postgres数据库上实现3倍的性能提升](https://postgresweekly.com/link/99062/web)
了解为Atlassian等客户优化Postgres查询性能的最佳实践，以及如何将磁盘加载的数据减少500倍。


`pganalyze `
## [在Citus中使Postgres存储过程快9倍](https://postgresweekly.com/link/99063/web)
Citus是长期开发的扩展，用于为Postgres带来更强的水平扩展性和分布式查询。 这是有关如何在Citus 8.3和9.4之间使存储过程速度提高9倍的故事，以及实现该过程的各种技术。


`Marco Slot `
## [呼吁行为准则委员会的新成员](https://postgresweekly.com/link/99064/web)
PostgreSQL社区行为准则委员会正在寻找新成员以填补空缺。可以是你吗？ 申请截止日期是今天结束，您只需要在电子邮件中回答几个问题即可。


`PostgreSQL CoC Committee `
## [Postgres：“包含电池”数据库](https://postgresweekly.com/link/99065/web)
诸如Django或Ruby on Rails之类的框架可以称为“包含电池”系统，因为它们包括现成的身份验证，ORM，工具等。 Craig认为，Postgres就像数据库领域那样-它拥有全部（或者可以添加！）


`Craig Kerstiens `
## [PostgreSQL的Azure数据库的Azure CLI改进](https://postgresweekly.com/link/99066/web)
为Azure用户涵盖了各种改进，包括您现在可以使用单个命令创建单个Postgres服务器实例。


`Microsoft `
## [在Go中为Clickhouse编写Postgres外部数据包装程序](https://postgresweekly.com/link/99067/web)
外部数据包装程序（FDW）为Postgres服务器提供了一种与外部服务（包括此处介绍的ClickHouse OLAP DBMS）进行交互的方式。


`Arun Sori `
## [更多Postgres，更少管理](https://postgresweekly.com/link/99069/web)
对开发和部署人员友好。 对于您的Postgres托管，Crunchy Bridge是更好的选择。


`Crunchy Data `
## [使用“仅插入”数据建模来平滑慢速磁盘上的峰值](https://postgresweekly.com/link/99070/web)
看看一种模式使UPDATE被性能更高的INSERT取代，这对于某些负载模式和受限制的基础架构配置可能会有所帮助。


`Kaarel Moppel `
## [Penkala：用Clojure写的Postgres可组合查询生成器](https://postgresweekly.com/link/99071/web)
它的创建者对其他Clojure数据库库中使用的抽象级别不满意。 Penkala比HugSQL或HoneySQL更高级别，更灵活，可组合，并且对Postgres功能具有一流的支持。。 


`Mihael Konjević `
## [pg-mem：来自Node.js用于测试的实验性内存Postgres实例](https://postgresweekly.com/link/99072/web)
我不确定这种方法是否长期有效，因为它是具有自己的SQL解析器的克隆，其行为与Postgres并不相同，但是如果您 是Node开发人员，也许会很有趣。


`Olivier Guimbal `
