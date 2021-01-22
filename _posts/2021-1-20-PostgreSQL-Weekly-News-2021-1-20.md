---
layout: post
title: PostgreSQL 每周新闻 2021-1-20
---
### PostgreSQL每周新闻#389 - 2021年1月20日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)
备注：[英文原文地址](https://postgresweekly.com/issues/389)
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/oqkytfrlm6w5hm1n2ux7.jpg)
## [pspg 4.0发布：用于Postgres表和更多内容的寻呼机](https://postgresweekly.com/link/101499/web)
pspg是用于处理Postgres查询结果以及CSV或TSV数据的Unix寻呼机。4.0添加了将内容导出到文件或剪贴板的支持。 


`Pavel Stěhule `
## [在Postgres中使用层次结构](https://postgresweekly.com/link/101501/web)
在对数据建模时，通常需要树和类似的层次结构，并且在Postgres中有多种实现方法。这篇文章使用递归CTE和ltree列来查看实例化视图。


`Ana Hobden `
## [几乎零停机时间迁移和自动代码重写](https://postgresweekly.com/link/101503/web)
CYBERTEC Migrator是功能强大但易于使用的软件产品，可用于从Oracle到PostgreSQL的快速数据库迁移。它支持各种数据结构和Oracle概念，并且完全能够处理复杂的设置和环境。


`CYBERTEC `
## [如何审核Postgres数据库](https://postgresweekly.com/link/101504/web)
审核是许多安全法规所必需的，如果您想知道数据库中发生了什么以及何时以及由谁负责，审核也将非常有用。这是PGAudit可以为您完成的基本工作。


`Sebastian Insausti (SeveralNines) `
## [关于2021年启动的Postgres提示和技巧](https://postgresweekly.com/link/101506/web)
您知道我们喜欢这里的提示和技巧（是的，本周的“提示”下周又回来了），Kaarel在这里分享了一些有关部分索引，Postgres升级和检查的内容在中查询结果元数据psql。


`Kaarel Moppel `
## [如何在特定时间没有用户干预的情况下运行某些任务？](https://postgresweekly.com/link/101507/web)
如果cron您的第一个答案是对的，那么您是对的，但是在处理Postgres时，可能还有更多答案。Hubert在这里还简要介绍了pgAdmin和pg_timetable。


`Hubert depesz Lubaczewski `
## [分区计数是否有限制？](https://postgresweekly.com/link/101508/web)
可能不是很严格的，正如Hubert在这里发现的那样。“我可能不鼓励人们制作5000个以上的单个表分区，但Pg绝对可以处理。”


`Hubert depesz Lubaczewski `
## [了解具有138年历史的船运公司如何与无服务器一起运输](https://postgresweekly.com/link/101509/web)
l,null,"en


`New Relic `
## [Postgres中的SQL优化：INvs EXISTSvs ANY/ ALLvsJOIN](https://postgresweekly.com/link/101510/web)
去年的一项内容我们没有涉及。它说明了尽管Postgres进行了优化，但针对同一问题的不同方法如何能够产生不同水平的性能。


`Jobin Augustine `
## [如何使用Homebrew从Postgres 12升级到13](https://postgresweekly.com/link/101511/web)
如果在本地macOS机器上运行基于Homebrew的Postgres安装，该功能将非常有用。


`Nick Quaranto `
## [Postgres如何在表访问方法API的帮助下执行顺序扫描](https://postgresweekly.com/link/101512/web)
HighGo的另一篇低层“幕后”文章。仅在关心Postgres内部工作原理的情况下才可以深入研读。


`Cary Huang `
## [新的Oracle到Postgres的迁移指南Azure的用户](https://postgresweekly.com/link/101513/web)
微软和亚马逊热衷于让Oracle的用户改用其他非Oracle的产品，这让我认为Larry Ellison拒绝参加科技界的亿万富翁“秘密圣诞老人”。尽管如此，如果需要这样做的话，现在有一个新的详细的迁移指南，用于将Oracle工作负载移至PostgreSQL的Azure数据库。


`Arun Kumar Thiagarajan `
# 💡本周提示


**🗓即将举办的Postgres活动**
