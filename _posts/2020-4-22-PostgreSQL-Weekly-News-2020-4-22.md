---
layout: post
title: PostgreSQL 每周新闻 2020-4-22
---
### PostgreSQL每周新闻#352 - 2020年4月22日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)
备注：[英文原文地址](https://postgresweekly.com/issues/352)
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/qejzzsreeflhuel6ipcq.jpg)
## [Postgres Explain Visualizer 2：显示执行计划的Vue.js组件](https://postgresweekly.com/link/87076/web)
Vue.js 是一个能帮助你在构建自己的Postgres时会用到的工具。 这里有一个演示。结果真是好极了。


`Dalibo `
## [Postgres13中auto vacuum只限插入的表（但为什么？）](https://postgresweekly.com/link/87078/web)
autovacuming清除了更新或删除表中数据时经常留下的死元组，那么为什么在Postgres 13中只限插入表的auto vacuum是一个大问题呢？劳伦兹解释道。


`Laurenz Albe `
## [使用Buildkite为所有软件项目提供更快的CI/CD](https://postgresweekly.com/link/87079/web)
看看Shopify如何将300名工程师扩展到1800名，同时将他们的构建时间控制在5分钟以内。


`Buildkite `
## [使用Rails和Postgres以毫秒为单位进行全文搜索](https://postgresweekly.com/link/87080/web)
如果你从来没有玩过Postgres和Rails的全文搜索，这是一个很好的开始。它包括LIKE/ILIKE、trigrams和“适当的”全文搜索。我们还可以看到Leigh是如何将查询从130毫秒减少到7毫秒的。


`Leigh Halliday `
## [一个简单的Postgres 12和pgAdmin 4的Docker设置](https://postgresweekly.com/link/87081/web)
Docker提供了一种简单且松散耦合的方法，可以在开发环境中设置东西。


`Jonathan S. Katz `
## [Postgres处理的分区数量有限制吗？](https://postgresweekly.com/link/87082/web)
有点限制，但你真的必须努力去扩展Postgres12在这方面的能力。


`Denish Patel `
## [我的Postgres设置来自哪里？](https://postgresweekly.com/link/87083/web)
这是一个对参数和设置的互相关联或覆盖的说明。


`My DBA Notebook `
## [使用Datadog快速识别运行缓慢的PostgreSQL的查询语句](https://postgresweekly.com/link/87084/web)
通过在Datadog中使用颗粒状、和快速且可视化仪表板来识别错误，进而提高PostgreSQL的性能。


`Datadog `
## [使用逻辑解码输出插件将多个Postgres服务器复制到单个MongoDB服务器](https://postgresweekly.com/link/87085/web)


`David Zhang `
## [Postgres中连接方法综述](https://postgresweekly.com/link/87086/web)


`Kumar Rajeev Rastogi `
# 💡本周提示


Luca Ferrari对意大利Postgres社区产生了巨大影响，过去曾担任意大利PostgreSQL用户组主席，并帮助组织了受欢迎的PGDay.it活动。他还经常撰写有关Postgres的博客，并为Packt编写PostgreSQL 11服务器端编程快速入门指南。


注：本次采访的更完整版本已在网上公布。


我们采访了他，特别询问了服务器端Postgres用例：

###对于那些使用Postgres作为简单数据库并且还没有涉及到更深层次元素的人，您认为他们应该从哪里开始呢？


这个问题没有单一的答案，因为Postgres是一个如此庞大的项目，有如此多的功能和丰富的社区。我从来没有找到一个项目不适合。Postgres在某种程度上类似于Unix：你不能把它当作“仅仅是一个数据库”，你需要致力于它的文化才能从中受益。

在课堂上，我可以看到人们通常会对执行服务器端编程的能力着迷，这就是为什么我决定写这本书的原因。通常，人们不希望能够将自己的Perl，Java或Python库直接嵌入到PostgreSQL中，而不必用类似SQL的语言重写其业务逻辑。

如今，另一个重要功能是对数据库中JSON的支持，这使得PostgreSQL既可以用作关系数据库又可以用作 “NoSQL” 存储引擎，从而在基础架构中提供了很大的灵活性。

我一直提出的一个建议是加入邮件列表(email list)：有几个主题和流量不同。他们中的大多数人都很活跃，并且有高质量的撰稿人，他们会认真回答用户的问题，花费时间重现错误和极端情况，并由谁来帮助您。我认为，这是一个必须开始的地方，您必须先开始才能更好地了解该项目，其功能和文化。

### 在外部编程语言中进行处理与在Postgres中进行处理之间应该划清界限吗？

通常，正确的选择是将业务逻辑放在它所引用的数据附近，也就是数据库本身。但是，要考虑一些因素，包括开发人员的经验以及诸如pl / PgSQL之类的SQL衍生语言的表达能力。

现在有一种习惯是让ORM（对象关系映射器）执行大多数数据库交互，从而将数据库缩减为“简单存储”。当然，数据库可以做更多的事情，尤其是PostgreSQL可以帮助您迁移自己的业务逻辑并将其嵌入数据库本身。

我已经帮助一些公司将自己的Java库嵌入到Postgres中，从而导致了一种更健壮和一致的方式来访问数据（真正的价值），而无需考虑他们使用的应用程序。因为一旦开始拥有数据，您很快就会发现，不同技术和不同平台上的多个应用程序都需要这些数据，因此一遍又一遍地实现相同的业务逻辑规则将是一项巨大的工作。另一方面，在数据库中移动这样的逻辑可以简化并保持数据处理方式的统一。

### 您认为人们应该学习什么一件事？

存储过程。它们是触发器的通用基础，并且与例程非常相似，因此允许您将更复杂的片段构建到自己的集群中。学习完定义函数的常用方法后，您可以更深入地使用其他语言（例如C）编写自己的本机函数。这更加复杂，但是由于Postgres的可扩展性，这并不是一项不可能的任务，它可以帮助您将越来越多的代码迁移到数据库中。创建新功能后，请回馈它，以便其他人可以使用它！

...

最后，请允许我宣布我正在写另一本书：我和我的一个朋友正在写一本关于Postgres的更通用的书，通过引导读者了解使Postgres与众不同的主要功能，并且回答读者可能有的问题。
