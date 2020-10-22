---
layout: post
title: PostgreSQL 每周新闻 2020-10-21
---
### PostgreSQL每周新闻#378 - 2020年10月21日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)
备注：[英文原文地址](https://postgresweekly.com/issues/378)
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/v1603287031/wmzplionqwayyadqvdq1.jpg)
## [中型文本对性能的惊人影响](https://postgresweekly.com/link/97182/web)
您拥有小文本（用户名，电子邮件），大文本（整个文档）和“中”文本（评论，说明）。.虽然TOAST可以提高存储效率对于较大的文档，中型的列可能会使行变得非常宽，并且会不成比例地影响性能。深入整洁的潜水实例。


`Haki Benita `
## [与Bruce Momjian一起进行Postgres的30年持续发展](https://postgresweekly.com/link/97184/web)
这是一次简短的采访，但是Bruce分享了有关Postgres开发过程，质量及其功能的一些花絮。


`Scott Grant `
## [[白皮书]使用PostgreSQL实现高可用性](https://postgresweekly.com/link/97185/web)
关键的业务应用程序需要其后端数据库集群的可用性。探索如何设置和部署最多四个9的企业级高可用性。在高度可用的Postgres集群白皮书中了解功能和优势。


`2ndQuadrant PostgreSQL Products `
## [调整Postgres数据库的高写负载](https://postgresweekly.com/link/97187/web)
如果您将数据库设置为概念证明或为了适应最初的小工作量，一旦事情扩大，就会出现问题，包括“检查点发生得太频繁”之类的警告。发生了什么，可以进行哪些调整？


`Tom Swartz `
## [Postgres如何存储“空”值](https://postgresweekly.com/link/97188/web)
好消息-您几乎肯定不需要知道这一点，但是知道这个秘密总是对我有利。


`Movead Li `
## [Multicorn：由Python驱动的外部数据包装器](https://postgresweekly.com/link/97189/web)
Mulitcorn是FDW，但带有各种可自定义的子包装器（用于诸如SQLAlchemy，RSS，与文件系统或SQLite结合使用），您可以调整..或编写自己的子包装器。


`Kozea `
## [pgFormatter：一种Postgres SQL语法美化工具](https://postgresweekly.com/link/97190/web)
可以从终端或通过CGI在Web服务器上工作。演示在这里。


`Gilles Darold `
## [Prisma的数据指南：PostgreSQL](https://postgresweekly.com/link/97192/web)
PostgreSQL入门教程：了解如何配置和使用Postgres来利用其最佳功能。


`Prisma `
# 💡本周提示


比较不同Postgres版本的功能集

尽管发布的速度并没有像Chrome或Node一样快，但Postgres仍然有许多版本仍在生产中，其功能集以各种有趣的方式重叠。

除了每周阅读一次Postgres并记住有关每个版本的所有文章外，您如何跟上Postgres的版本之间的差异？

输入：功能矩阵！


![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/v1603285176/aatrmu6keidv6g8qcbdr.png)



该矩阵涵盖性能和分区等类别中的数百个子点，通过该矩阵，您可以简单地回答每个重要版本的Postgres包含哪些功能。

感谢Nikolay Samokhvalov引起了我们的注意（他在Twitter线程上也有另外两个很棒的资源）。


**🗓即将举办的Postgres活动**

## [PostgresConf.CN和PGConf.Asia 2020在线峰会（11月17日至20日）](https://2020.postgresconf.cn)

