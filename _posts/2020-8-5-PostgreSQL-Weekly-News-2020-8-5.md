---
layout: post
title: PostgreSQL 每周新闻 2020-8-5
---
### PostgreSQL每周新闻#367 - 2020年8月5日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)
备注：[英文原文地址](https://postgresweekly.com/issues/367)
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/v1596547416/qmn0lierqiaaytaamyxd.jpg)
## [要注意关于Postgres 13的不兼容性](https://postgresweekly.com/link/92880/web)
Postgres 13即将正式发布（目前处于Beta测试版），尽管随着时间的推移，Postgres趋向于向后兼容，但是在进行迁移之前，有一些变化值得注意，请参见此文章


`Ibrar Ahmed `
## [如何安全的身份验证与SCRAM Postgres里13](https://postgresweekly.com/link/92897/web)
设置基于SCRAM密码认证的教程。


`Jeff Davis `
## [在Postgres 13中如何使用SCRAM安全地进行身份验证](https://postgresweekly.com/link/92883/web)
这是基于SCRAM的密码身份验证的设置教程。 有趣的不仅是教程，而是了解什么是SCRAM以及为什么通道绑定可以提高整体的安全性。


`EDB `
## [测量日期之间的差异](https://postgresweekly.com/link/92884/web)
“两个日期之间有什么差异？ 您会以为答案只有一个，但没有答案。” 有趣的是，在Postgres中如何用多种方法获得两个日期或时间戳之间的差异，以及它们如何返回略有不同的答案。


`Bruce Momjian `
## [effective_cache_size：一个实际示例](https://postgresweekly.com/link/92885/web)
有关effective_cache_size设置的作用的一些见解和一个实际示例。


`Hans-Jürgen Schönig `
## [宣布兼容Azure的pgBackRest：一个快速，可靠的Postgres备份工具](https://postgresweekly.com/link/92886/web)
备份是运行任何数据库的重要环节。 pgBackRest的目标是成为一种快速，可靠，易于使用的备份和还原的解决方案，能够无缝扩展到最大的数据库，现在正式支持Azure。


`Craig Kerstiens `
## [Pgpool-II中的连接池](https://postgresweekly.com/link/92888/web)
Pgpool-II是Postgres的连接池工具-这篇文章讲述其操作的基础知识。


`B Peng `
## [如何加快Postgres查询的最佳实践](https://postgresweekly.com/link/92890/web)
免费电子书-Robinhood和Atlassian等公司可以将查询速度提高几个数量级。 这本电子书分享了我们优化Postgres性能的最佳实践。


`pganalyze `
## [如何在Postgres中使用SSL正确的方法：在传输过程中加密数据](https://postgresweekly.com/link/92891/web)
▶


`Kirill Shirinkin `
## [使用WAL-G进行连续备份](https://postgresweekly.com/link/92892/web)
WAL-G使您可以管理Postgres数据和备份的归档，还可以使您在特定时间将数据库恢复到其状态。


`Angelico de los Reyes `
## [计算INTERVAL值](https://postgresweekly.com/link/92894/web)
布鲁斯（Bruce）看来在本周处于日期和时间的研究上，在这里他介绍了一些日期/时间间隔的特殊用法。


`Bruce Momjian `
## [高性能HTAP在Postgres和超大规模（西特斯）](https://postgresweekly.com/link/92898/web)
▶


`Marco Slot and Claire Giordano `
# 💡本周提示

###FROMAT功能
当没有立即想到新的Postgres技巧时，我最喜欢的技术之一就是浏览（写的超级好的）Postgres文档，直到我发现以前不知道的东西，但我认为可能对未来有些帮助。 而今天我找到了FORMAT函数！

如果您熟悉各种语言（例如Python，C或Ruby）的format，printf或sprintf，您将知道格式字符串是什么-使用由特殊分隔符组成的简单模板语言的字符串，可以用分隔符替换value。 Postgres在FORMAT函数中提供了相同的想法：


```
SELECT FORMAT('%s %s', 'hello', 'world');
/* => 'Hello world' */

SELECT FORMAT('|%10s|', 'test');
/* => '|      test|' */

SELECT FORMAT('INSERT INTO %I VALUES(%L, %L)',
  'people', 'pat', null);
/* => 'INSERT INTO people VALUES('pat', NULL)' */
```

遗憾的是，FORMAT的功能远不如非SQL语言中的字符串格式语言（例如，没有％d或％f）强大，但是您会发现它对于将多个列组合成首选输出形式非常有用（例如 （以美分表示为格式的价格）：

```
SELECT FORMAT('$%s', ROUND(cents / 100, 2));
```

如果您打算使用FORMAT，请务必查看官方文档以获取更多信息。
