---
layout: post
title: PostgreSQL 2018-09-02 每周新闻
---
# PostgreSQL每周新闻 - 2018年9月2日
备注：[英文原文地址](https://www.postgresql.org/message-id/20180902223553.GA29881%40fetter.org)
## PostgreSQL产品新闻
[pspg 1.6.0，一个专为PostgreSQL设计的寻呼机(pager)，发布了。](https://github.com/okbob/pspg/releases/tag/1.6.0)

### PostgreSQL 地方新闻
[**PostgreOpen硅谷2018** 将于2018年9月5日至7日在旧金山举行。](https://2018.postgresopen.org/)

[波特兰PostgreSQL用户组将于2018年9月10日在俄勒冈州波特兰市举行PGDay](https://pdx.postgresql.us/pdxpgday2018)

[**南非 PostgresConf 2018** 将于2018年10月9日在约翰内斯堡举行](https://postgresconf.org/conferences/SouthAfrica2018)

[**欧洲 PostgreSQL会议 2018** 将于2018年10月23日至26日在里斯本万豪酒店,里斯本，葡萄牙。](https://2018.pgconf.eu/ )

[**2Q PGConf** 将于2018年12月4日至5日在伊利诺伊州芝加哥市举行。](http://www.2qpgconf.com/)

[**PGConf.ASIA 2018** 将于2018年12月10日至12日在日本东京秋叶原举行 ](http://www.pgconf.asia/EN/2018/）


### 新闻中的PostgreSQL
[Planet PostgreSQL](http：//planet.postgresql.org/)
本周的PostgreSQL每周新闻将由David Fetter为您带来，请在本周日下午3点（太平洋标准时间晚上9点）提交新闻和公告到 david(at)fetter(dot)org

### 应用补丁
Michaël Paquier 推动：
  ```
  通过避免早期锁定队列来改进VACUUM和ANALYZE。 VACUUM的调用者可以执行早期查找争用，这可能导致其他会话阻止完成请求，
  从而导致潜在的DOS攻击，因为即使是非特权用户也可以尝试对关键目录表进行VACCUUM填充，以阻止所有传入的连接尝试。
  与TRUNCATE相反，客户端可以在构建与VACUUM的关系列表之后尝试系统范围的VACUUM，这可能导致vacuum_rel（）或analyze_rel（）尝试锁定关系，
  但只会阻塞操作。当客户端指定关系列表并且需要跳过关系时，在构建要处理的关系列表时完成所有权检查，从而防止稍后的锁定尝试。
  vacuum_rel（）已经进行了所需的完整性检查，除了那些太晚的应用。
  这次的重构代码提交，对于具有和不具有指定关系列表的手动VACUUM，可以跳过事先检查关系，从而更安全地避免过早锁定。
  添加了隔离测试，模拟早期锁不再发生的情况，如果用户调用VACUUM不是关系所有者，则更早发出WARNING消息。
  当手动VACUUM或ANALYZE命令中列出分区表时，将获取其完整的分区列表，所有分区都将添加到列表中以进行处理，然后逐个处理每个分区，
  并在vacuum_rel（）或analyze_rel（）的后期阶段在所有位置进行所有权检查。
  尝试对每个分区进行早期所有权检查被证明是乏味的，因为这会导致锁升级的死锁风险，
  并且如果列出不归属的分区表，则跳过所有分区将导致与Postgres 10实现的用于分区表的VACUUM方式相比的行为不同。
  无论如何，报告的与关键关系的早期锁定队列相关的原始问题是固定的，因此优先考虑避免向后不兼容的行为。
```
问题提交者：Lloyd Albin, Jeremy Schneider

作者：Michael Paquier

代码审核：Nathan Bossart，Kyotaro Horiguchi

讨论：

  https://postgr.es/m/152512087100.19803.12733865831237526317@wrigleys.postgresql.org
  
讨论：
  https://postgr.es/m/20180812222142.GA6097@paquier.xyz
  
  https://git.postgresql.org/pg/commitdiff/a556549d7e6dce15fe216bd4130ea64239f4d83f
  
 
