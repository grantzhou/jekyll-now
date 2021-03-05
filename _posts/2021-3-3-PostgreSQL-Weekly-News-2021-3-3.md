---
layout: post
title: PostgreSQL 每周新闻 2021-3-3
---
### PostgreSQL每周新闻#395 - 2021年3月3日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)
备注：[英文原文地址](https://postgresweekly.com/issues/395)
![img](https://res.cloudinary.com/cpress/image/upload/e_grayscale,w_150,h_170,c_pad,g_south/xrupigpv8kyjqotfdgy8.jpg)
## [在Amazon RDS上设计高性能时间序列数据表](https://postgresweekly.com/link/103986/web)
大规模存储时间序列数据足以解决一个独特的数据库问题，即存在诸如TimescaleDB和Timestream之类的东西，但是如果您正确地设计，某些工作负载就可以满足普通Postgres的需求。


`Jim Mlodgenski and Andy Katz `
## [pgBouncer中的连接队列：这是一种神奇的补救方法吗？](https://postgresweekly.com/link/103989/web)
Jobin将连接队列（不，不合并）称为pgBouncer的“非名人”功能，但它可以解决与连接管理有关的一些问题，尤其是在吸收负载峰值时。


`Jobin Augustine `
## [快速，开朗，协作的项目管理](https://postgresweekly.com/link/103990/web)
无论您是在努力争取产品市场契合度的初创企业，还是需要严格交付日期的大型组织，Clubhouse都可以帮助工程团队协作并取得成功。 轻松从Jira或Trello导入。


`Clubhouse.io `
## [Amazon RDS现在支持Postgres 13](https://postgresweekly.com/link/103991/web)
如果您使用的是RDS，现在可以根据需要将数据库升级到Postgres 13。


`Amazon Web Services `
## [实现subscripting工作需要多少工程师？](https://postgresweekly.com/link/103992/web)
如果您经常使用JSONB列，您可能会像我一样，厌倦有时需要使用值来设置值的神秘函数和语法。 这篇文不仅展示了潜力，而且还展示了功能如何组合在一起，以及Postgres中的新功能通常如何吸引许多工程师。


`Dmitry Dolgov `
## [使用新的Postgres统计信息估计连接池大小](https://postgresweekly.com/link/103993/web)
如何使用pg_stat_database的各种添加项来获得连接池正确大小的上限。


`Laurenz Albe `
## [在哪里可以设置Postgres Config参数？](https://postgresweekly.com/link/103994/web)
来证明它不仅在postgresql.conf中。


`Hubert depesz Lubaczewski `
## [Helm，GitOps和Postgres运算符](https://postgresweekly.com/link/103995/web)
您如何将GitOps原理应用于使用Helm在Kubernetes上运行PostgreSQL？


`Jonathan S. Katz `

## 🔧工具和代码

## [pspg 4.3.0发布](https://postgresweekly.com/link/103996/web)
pspg是用于处理Postgres查询结果以及CSV或TSV数据的Unix工具。 现在，您可以通过4.3选择要导出的行，列或数据块。


`Pavel Stěhule `
## [纯PL / pgSQL中的RFC6238 TOTP实现](https://postgresweekly.com/link/103997/web)
在某些使用2FA的网站上，您将QR码扫描到Google Authenticator或Authy之类的应用中，然后获得一个（通常）六位数的代码来登录以登录该服务。 这些是“基于时间的一次性密码”（TOTP），并且计算它们的算法相当简单。


`Dan Lynch `
## [在Postgres之上构建内部应用程序（更快速）](https://postgresweekly.com/link/103998/web)
构建内部应用程序而不会出现平凡而乏味的工作（与UI库进行搏斗或将数据源和API捆绑在一起）。


`Retool `
## [EdgeDB 1.0 Beta 1正式发布](https://postgresweekly.com/link/103999/web)
EdgeDB是一个隐秘的数据库，在过去几年中我们已经讨论过几次，并且正逐步接近其1.0版本。 它建立在Postgres的基础上，旨在提供NoSQL的最佳组成部分，但它具有一种新的基于逻辑的查询语言，旨在解决SQL的缺点。


`Łukasz Langa and Victor Petrovykh `
## [Pgpool-II的六种群集模式](https://postgresweekly.com/link/104001/web)
Pgpool-II是一种比您可能还记得的功能更广泛的工具，它支持流复制，本机复制，快照隔离，逻辑复制，Slony模式以及“您自己”的原始模式 模式。


`Bo Peng `
# 💡本周提示

当心查询计划者和random_page_cost

本周的提示是一个奇怪的提示，因为它基于我今天遇到的一个问题！ 我们将任何新闻通讯中包含的所有链接存储在一个幼稚的数据库中，如下所示：


```
CREATE TABLE links (
  uid CHAR(60) PRIMARY KEY,
  data TEXT,
  timestamp INT
)
 
CREATE INDEX idx_trgm ON links USING GIN (data gin_trgm_ops)
```

是的，这是一个糟糕的设计，但是它仅供内部使用，并且仅是概念的粗糙原型。 愚蠢的是，数据是一个包含JSON（我知道，我知道..）的TEXT列，我们以一种类似的可怕方式检查链接的存在：


```
SELECT * FROM links WHERE data ILIKE '%whatever we want%' LIMIT 1;
```

它在低音量下效果很好，但查询时间有时会推300ms，我对此很感兴趣。

稍后进行一次EXPLAIN ANALYZE，我发现Postgres根本没有使用GIN索引，而是对整个表进行了顺序扫描。 但是，如果我放弃LIMIT 1，查询将使用索引，并且只用了5毫秒！ 为什么Postgres忽略了索引？

Postgres的查询计划程序并不是真正基于做傻事的人，例如使用ILIKE扫描整个表，但它担心索引扫描可能比表扫描更快或更慢。 变量random_page_cost用于通过定义seq_page_cost的相对“成本”来确定使用索引是否“值得”。

在这种情况下，进行索引扫描是值得的，但是由于看起来简单的LIMIT 1查询（毕竟，只要找到单个结果，它就可以停止），查询计划者就不同意了，反而继续进行完整的扫描。 这是我确认对psql的直觉的方法：


```
SET random_page_cost = 1;
EXPLAIN ANALYZE SELECT * ... LIMIT 1;
    [see the index being used]
    
SET random_page_cost = DEFAULT;    
EXPLAIN ANALYZE SELECT * ... LIMIT 1;
    [see the index NOT being used]
```

除了显而易见的“解决那可怕的模式”！ 向前看，这个小技巧可以让您发现Postgres如果感觉到索引扫描与顺序扫描表格相比没有“成本”，该怎么做，这提供了一种奇妙的方法来确认正在发生的事情。

因此，如果您遇到的查询似乎自然地避免了使用表扫描而不是使用索引，那么值得一试的是，查看查询计划程序是否因使用索引的成本而偏离了索引（以及 那么，为什么呢？是因为设计很糟糕，就像我们这样吗？）并且像往常一样，使用EXPLAIN ANALYZE来查看缓慢查询的结果！

