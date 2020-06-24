---
layout: post
title: PostgreSQL 每周新闻 2020-6-10
---
### PostgreSQL每周新闻#359 - 2020年6月10日
![_config.yml]({{ site.baseurl }}/images/PostgresWeekly.png)
备注：[英文原文地址](https://postgresweekly.com/issues/359)
![img](https://res.cloudinary.com/cpress/image/upload/w_1280,e_sharpen:60/v1591718357/nasfptyqnxqgg5uzinqb.png)

## [10个常见的Postgres错误](https://postgresweekly.com/link/89780/web)
有一些常见的错误和警告，包括内存、磁盘空间和权限等方面的现象和解决方案。

`Ibrar Ahmed (Percona) `

## [使解释分析计划更具可读性的工具](https://postgresweekly.com/link/89781/web)
经久不衰（超过11年！）基于Web的工具，允许您粘贴EXPLAIN-ANALYZE查询的结果，并查看更易于理解的版本。现在有很多更新。

`Hubert Lubaczewski, Łukasz Lewandowski `

## [白皮书：专业支持的商业案例](https://postgresweekly.com/link/89783/web)
了解专业团队对您关键PostgreSQL系统进行维护重要性。这可以提高数据库性能、帮助扩展、分发数据、降低成本、避免已知的陷阱等等。

`2ndQuadrant Services `

## [PostgreSQL的HAProxy负载均衡](https://postgresweekly.com/link/89784/web)
我是haproxy TCP和HTTP代理/负载均衡器的忠实粉丝，但不可否认的是，我以前从未在Postgres中使用过它。。本文演示了将HAProxy与severnines的ClusterControl一起用于Postgres的负载平衡，其方式与HTTP服务器类似。


`Severalnines `
## [Postgres的多主复制解决方案](https://postgresweekly.com/link/89798/web)
多年来，为了使Postgres变得更容易，横向扩展Postgres已经足够成为一项挑战，很多公司（如Citus Data）都在寻求其解决方案。不过，有多种方法可以进行多主机复制，本文链接到几种方法。

`Ibrar Ahmed (Percona) `

## [Postgres 13 B-Tree索引中的重复数据消除](https://postgresweekly.com/link/89786/web)
PostgreSQL v13引入了B树索引项的重复数据消除。本文描述了这个新特性，并通过一个简单的测试演示了它。

`Laurenz Albe `

## [逐步将Heroku Postgres数据库备份到AWS S3存储桶](https://postgresweekly.com/link/89787/web)
IMO值得做的另一个变化是启用S3版本控制，这样就可以轻松地获得滚动备份并保持文件名的一致性。

`Paweł Urbanek `

## [查找Postgres配置文件](https://postgresweekly.com/link/89788/web)
SHOW config_file是这里的关键，但是如果使用Docker，可能需要更多操作。

`Luca Ferrari `

## [什么是故障切换插槽？](https://postgresweekly.com/link/89789/web)

`Craig Ringer `

## [使用Datadog实时可视化Postgres的性能](https://postgresweekly.com/link/89790/web)
Datadog的Postgres OOTB仪表板将延迟、错误、读/写容量和限制请求的数据可视化。

`Datadog `

## [pgsql http：Postgres的http客户端扩展](https://postgresweekly.com/link/89791/web)
这个插件实现了直接使用Postgres发出HTTP请求。

`Paul Ramsey `

## [PgHero 2.5：Postgres的性能仪表板](https://postgresweekly.com/link/89792/web)
`Andrew Kane `

## [SQLancer：检测数据库系统逻辑错误的工具](https://postgresweekly.com/link/89794/web)
目前被认为是一个“研究原型”，SQLancer的工作是强调数据库系统返回不一致或不合逻辑的结果。它用Java编写，支持多个数据库（包括Postgres）。


`Manuel Rigger and Zhendong Su `
# 💡本周提示


分组集允许您在比简单的按列分组更复杂的查询中执行分组。


给一张这样的表：


```
name  | dept | location | salary 
--------+------+----------+--------
 Abbey  | IT   | London   |  85000
 Paul   | IT   | Madrid   |  74000
 Clancy | HR   | London   |  71000
 Imani  | HR   | Madrid   |  74000
```


我们可以通过以下查询轻松获得每个“部门”的总工资：


```
SELECT dept, SUM(salary) FROM staff GROUP BY dept;
```


但如果我们希望在同一个查询中以不同的方式得到工资总额呢？例如，假设我们希望每个人的工资总额、每个部门的工资总额和每个位置的工资总额都在同一个查询中。能做到吗？


输入'grouping sets'，它允许您定义多组分组条件，每个分组条件将单独执行并附加到结果集。


例如，让我们将结果按部门分组，然后按位置分组，最后按空集（即总数）分组：


```
SELECT dept, location, SUM(salary) FROM staff
GROUP BY GROUPING SETS ((dept), (location), ());
```


这给了我们一组结果如下：


```
dept | location |  sum   
------+----------+--------
      |          | 304000
 IT   |          | 159000
 HR   |          | 145000
      | London   | 156000
      | Madrid   | 148000
```


现在我们很容易从一组结果中看出，我们例子中的员工在伦敦的工资更高，在IT部门的工资更高，总体工资账单是30.4万英镑。


**🗓即将举办的Postgres活动**
- [Postgres Pulse](https://postgresweekly.com/link/89796/web)-每周一上午11点。每周与Bruce Momjian、Vibhor Kumar和EnterpriseDB的其他人进行zoom的会议。
- [Postgres Vision 2020](https://postgresweekly.com/link/89797/web)6月23-24日。一个完整的在线Postgres多天会议。
