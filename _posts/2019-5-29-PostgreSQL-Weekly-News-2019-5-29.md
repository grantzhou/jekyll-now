---
layout: post
title: PostgreSQL 每周新闻 2019-5-22
---

### PostgreSQL每周新闻#307 - 2019年5月29日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)

备注：[英文原文地址](https://postgresweekly.com/issues/307)

![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/m6hlvb2bh95gyenivb2v.jpg)

## [可视化 Vacuum进程](http://dtrace.org/blogs/dap/2019/05/22/visualizing-postgresql-vacuum-progress/)
如果你的数据库的vacuum过程花费了大量时间（就像在这篇文章中提到的一样），那么能够可视化其进程肯定是可取的。

`DAVE PACHECO`

## [Postgres 12 Beta 1发布](https://www.postgresql.org/about/news/1943/)
[初版发布说明](https://www.postgresql.org/docs/devel/release-12.html)详细介绍了新的特性有哪些，但是更值得关注的是：
* 内联WITH查询支持（为了CTE粉丝）。
* 2016-compliant JSON路径查询。
* 根据ICU排序规则的大小写不敏感的比较。
* [Generated columns](https://www.postgresql.org/docs/devel/ddl-generated-columns.html)。
* 可插拔的表存储机制。

`POSTGRESQL 全球开发小组`

## [使用自动表统计信息来改进优化器](https://www.cockroachlabs.com/blog/automatic-sql-statistics/)
![img](https://copm.s3.amazonaws.com/0c8e53d3.png)  
自动生成表统计信息如何使花费成本的优化器在选择查询时做出更好的决策。

`COCKROACH LABS` **赞助商**

## [并行PostGIS和PgSQL 12：问题已解决！](http://blog.cleverelephant.ca/2019/05/parallel-postgis-4.html)
空间查询通常受CPU限制，因此能够并行处理它们可能会有很大的优势，Postgres 12现在可以提供这些优势：“PostgreSQL 12和PostGIS 3最终解决了并行空间查询执行问题，在没有特别的干扰下所有主要查询都能并行执行。”

`PAUL RAMSEY`

## [使用Docker Hub的Postgres镜像](https://www.2ndquadrant.com/en/blog/using-docker-hub-postgresql-images/)
如果您想在Postgres中使用Docker托管的镜像并应用于CI jobs或开发中，那么这是非常有用的建议。

`CRAIG RINGER`

## [表继承：它有什么用？](https://ledgersmbdev.blogspot.com/2019/05/table-inheritance-whats-it-good-for.html)
我必须承认，我从未使用过表继承，但Chris演示了表继承如何使某些数据库设计问题更容易处理。

`CHRIS TRAVERS`

## [在Kubernetes上部署Active-Active Postgres](https://info.crunchydata.com/blog/active-active-on-kubernetes)
一个关于如何一步一步使用[Symmetric-DS](https://www.symmetricds.org/)（开源数据库复制工具）在Kubernetes上部署 active-active Postgres群集的指南。

`DAVE CRAMER`

## ▶ [Postgres，C'est le Nouveau NoSQL（它是新的NoSQL）](https://www.youtube.com/watch?v=h_l2z-Ti8gg)
这是一个用法语进行的演讲视频，因为语言限制了观众，但幻灯片很简单，都是用英语写的。

`LAURENT DOGUIN`

## [不要错过Postgres Vision 2019](https://postgresvision.com/)
6月24日至26日，马萨诸塞州波士顿，加入我们。现在注册。

`ENTERPRISEDB` **赞助商**

## [PostgresClientKit：一个不需要libpq的Swift客户端库](https://github.com/codewinsdotcom/PostgresClientKit)

`DAVID PITFIELD`

## [Sequelize：用于Node.js的易于使用的多SQL方言ORM](https://github.com/sequelize/sequelize)
可以与Postgres一起使用，如果你是Node开发人员，也是不错的选择。

`SEQUELIZE`

# ![_config.yml]({{ site.baseurl }}/images/Tips-icon.png)   本周提示
由PERCONA提供支持

使用Docker启动快速，临时的Postgres实例

如果你想尝试一些东西，Docker可以很容易地快速启动一个独立的Postgres服务器和psql。
Craig Ringer的[使用Docker Hub的PostgreSQL 镜像](https://www.2ndquadrant.com/en/blog/using-docker-hub-postgresql-images/)教程（附上链接）非常棒，如果你想在任何严重的等级使用Docker的Postgres镜像，但我也以轻量级的方式使用它们来执行快速任务，例如检查不同版本之间的SQL支持或测试我们在这里提供的提示！确保你已安装Docker并能完全正常的工作，然后专门为你的实验创建一个“网络”（这个'网络'使psql能够在一个单独的容器中运行并连接到Postgres实例）：  

```
docker network create pg1
```  

现在我们可以像这样启动一个Postgres服务器实例：  

```
docker run --name my-pg-server -e \
       POSTGRES_PASSWORD= \
       --network pg1 --rm -d postgres
```

注意：如果你想要一个特定版本的Postgres，在语句最后用'postgres：10.8'替换'postgres'。 你可以在[此处查看支持的版本](https://hub.docker.com/_/postgres)。

要使用psql连接到此实例：  

```
docker run -it --rm --network pg1 \
       postgres psql -h my-pg-server \
       -U postgres
```

一旦你使用完服务器，使用docker stop my-pg-server，你可以在剩余时间做你自己的事了。但是，请勿在生产方案中使用此方法，因为服务器创建时没有密码，这是不安全的。
有关Docker Hub的[更多文档](https://hub.docker.com/_/postgres)。

>本周提示由PERCONA提供支持。通过5月29日至30日在德克萨斯州奥斯汀举行的Percona Live扩展您的Postgres知识。

🗓  即将举办的Postgres活动  
- [PostgreSQL Ibiza(六月19-21日, 伊维萨)](https://www.pgibz.io/index.html) —— 这个在西班牙著名的度假岛上举行的会议将会带来“海滩上的Postgres”，同时仍然在一个漂亮整洁的场地上进行会谈和培训。  
- [Postgres Vision 2019(6月24日,波士顿)](https://postgresvision.com/) 
- [PostgresLondon 2019 (7月2-3日，伦敦)](https://postgreslondon.org/)
- [PostgresConf Beijing 2019(7月3-6日，中国北京)](https://postgresconf.org/conferences/Beijing)


