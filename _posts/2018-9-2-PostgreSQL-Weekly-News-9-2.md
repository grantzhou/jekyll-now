---
layout: post
title: PostgreSQL 2018-09-02 每周新闻
---
### PostgreSQL每周新闻 - 2018年9月2日
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
Michaël Paquier 的提交：

* 通过避免早期锁定队列来改进VACUUM和ANALYZE。 
> VACUUM的调用者可以执行早期查找争用，这可能导致其他会话阻止完成请求，
> 从而导致潜在的DOS攻击，因为即使是非特权用户也可以尝试对关键目录表进行VACCUUM填充，以阻止所有传入的连接尝试。
> 与TRUNCATE相反，客户端可以在构建与VACUUM的关系列表之后尝试系统范围的VACUUM，这可能导致vacuum_rel（）或analyze_rel（）尝试锁定关系，
> 但只会阻塞操作。当客户端指定关系列表并且需要跳过关系时，在构建要处理的关系列表时完成所有权检查，从而防止稍后的锁定尝试。
> vacuum_rel（）已经进行了所需的完整性检查，除了那些太晚的应用。
> 这次的重构代码提交，对于具有和不具有指定关系列表的手动VACUUM，可以跳过事先检查关系，从而更安全地避免过早锁定。
> 添加了隔离测试，模拟早期锁不再发生的情况，如果用户调用VACUUM不是关系所有者，则更早发出WARNING消息。
> 当手动VACUUM或ANALYZE命令中列出分区表时，将获取其完整的分区列表，所有分区都将添加到列表中以进行处理，然后逐个处理每个分区，
> 并在vacuum_rel（）或analyze_rel（）的后期阶段在所有位置进行所有权检查。
> 尝试对每个分区进行早期所有权检查被证明是乏味的，因为这会导致锁升级的死锁风险，
> 并且如果列出不归属的分区表，则跳过所有分区将导致与Postgres 10实现的用于分区表的VACUUM方式相比的行为不同。
> 无论如何，报告的与关键关系的早期锁定队列相关的原始问题是固定的，因此优先考虑避免向后不兼容的行为。

问题提交者：Lloyd Albin, Jeremy Schneider

作者：Michael Paquier

代码审核：Nathan Bossart，Kyotaro Horiguchi

讨论：

  https://postgr.es/m/152512087100.19803.12733865831237526317@wrigleys.postgresql.org
  
讨论：

  https://postgr.es/m/20180812222142.GA6097@paquier.xyz
  
  https://git.postgresql.org/pg/commitdiff/a556549d7e6dce15fe216bd4130ea64239f4d83f

* 返工`oid2nameq`的选项集
> oid2name 很少用于保持接口与其他二进制实用程序一致,oid2name几乎没有让其接口与其他二进制实用程序保持一致：
> 使用 `--H` 代替 `-h/-host`。 此选项现在标记为已弃用，但仍接受其输出向后兼容。
> `--P`已从代码中删除，仍有文档记录。
> `-ALL` 选项都获得长别名，使连接选项更类似于其他二进制文件。
> `-Document` 可以使用的环境变量：PGHOST，PGPORT和PGUSER。
>  过程中添加了一组基本的TAP测试，并且清理文档以与其他事物更加一致。

> 作者：Tatsuro Yamada(山田达郎)
> 评论人：Michael Paquier
> 讨论：
>  https://postgr.es/m/c7e7f25c-1747-cd0f-9335-390bc97b2db5@lab.ntt.co.jp
>  https://git.postgresql.org/pg/commitdiff/1aaf532deabfa356c99abc80fc78d988ad1f1355
 
- Rework option set of oid2name oid2name has done little effort to keep an
  interface consistent with other binary utilities: - -H was used instead of
  -h/-host.  This option is now marked as deprecated, still its output is
  accepted to be backward-compatible.  - -P has been removed from the code, and
  was still documented.  - All options gain long aliases, making connection
  options more similar to other binaries.  - Document environment variables
  which could be used: PGHOST, PGPORT and.  PGUSER.  A basic set of TAP tests is
  added on the way, and documentation is cleaned up to be more consistent with
  other things.  Author: Tatsuro Yamada Reviewed-by: Michael Paquier Discussion:
  https://postgr.es/m/c7e7f25c-1747-cd0f-9335-390bc97b2db5@lab.ntt.co.jp
  https://git.postgresql.org/pg/commitdiff/1aaf532deabfa356c99abc80fc78d988ad1f1355 


- Stop bgworkers during fast shutdown with postmaster in startup phase.  When a
  postmaster gets into its phase PM_STARTUP, it would start background workers
  using BgWorkerStart_PostmasterStart mode immediately, which would cause
  problems for a fast shutdown as the postmaster forgets to send SIGTERM to
  already-started background workers.  With smart and immediate shutdowns, this
  correctly happened, and fast shutdown is the only mode missing the shot.
  Author: Alexander Kukushkin Reviewed-by: Michael Paquier Discussion:
  https://postgr.es/m/CAFh8B=mvnD8+DZUfzpi50DoaDfZRDfd7S=gwj5vU9GYn8UvHkA@mail.gmail.com
  Backpatch-through: 9.5
  https://git.postgresql.org/pg/commitdiff/55875b6d2aa0946226e9261ee691cb519d92f8c1


- Rework option set of vacuumlo.  Like oid2name, vacuumlo has been lacking
  consistency with other utilities for its options: - Connection options gain
  long aliases.  - Document environment variables which could be used: PGHOST,
  PGPORT and PGUSER.  Documentation and code is reordered to be more consistent.
  A basic set of TAP tests has been added while on it.  Author: Tatsuro Yamada
  Reviewed-by: Michael Paquier Discussion:
  https://postgr.es/m/c7e7f25c-1747-cd0f-9335-390bc97b2db5@lab.ntt.co.jp
  https://git.postgresql.org/pg/commitdiff/bfea331a5e1b993d22071fc1696e6e8811d2d0d4


- Ensure correct minimum consistent point on standbys.  Startup process has
  improved its calculation of incorrect minimum consistent point in 8d68ee6,
  which ensures that all WAL available gets replayed when doing crash recovery,
  and has introduced an incorrect calculation of the minimum recovery point for
  non-startup processes, which can cause incorrect page references on a standby
  when for example the background writer flushed a couple of pages on-disk but
  was not updating the control file to let a subsequent crash recovery replay to
  where it should have.  The only case where this has been reported to be a
  problem is when a standby needs to calculate the latest removed xid when
  replaying a btree deletion record, so one would need connections on a standby
  that happen just after recovery has thought it reached a consistent point.
  Using a background worker which is started after the consistent point is
  reached would be the easiest way to get into problems if it connects to a
  database.  Having clients which attempt to connect periodically could also be
  a problem, but the odds of seeing this problem are much lower.  The fix used
  is pretty simple, as the idea is to give access to the minimum recovery point
  written in the control file to non-startup processes so as they use a
  reference, while the startup process still initializes its own references of
  the minimum consistent point so as the original problem with incorrect page
  references happening post-promotion with a crash do not show up.  Reported-by:
  Alexander Kukushkin Diagnosed-by: Alexander Kukushkin Author: Michael Paquier
  Reviewed-by: Kyotaro Horiguchi, Alexander Kukushkin Discussion:
  https://postgr.es/m/153492341830.1368.3936905691758473953@wrigleys.postgresql.org
  Backpatch-through: 9.3
  https://git.postgresql.org/pg/commitdiff/c186ba135ecafe987842920829629ef466ce6ce1


- Fix initial sync of slot parent directory when restoring status.  At the
  beginning of recovery, information from replication slots is recovered from
  disk to memory.  In order to ensure the durability of the information, the
  status file as well as its parent directory are synced.  It happens that the
  sync on the parent directory was done directly using the status file path,
  which is logically incorrect, and the current code has been doing a sync on
  the same object twice in a row.  Reported-by: Konstantin Knizhnik
  Diagnosed-by: Konstantin Knizhnik Author: Michael Paquier Discussion:
  https://postgr.es/m/9eb1a6d5-b66f-2640-598d-c5ea46b8f68a@postgrespro.ru
  Backpatch-through: 9.4-
  https://git.postgresql.org/pg/commitdiff/caa0c6ceba1fd6ec7b027532d68cecf5dfbbb2db


Peter Eisentraut pushed:


- Add some not null constraints to catalogs.  Use BKI_FORCE_NOT_NULL on some
  catalog field declarations that are never null (according to the source code
  that accesses them).
  https://git.postgresql.org/pg/commitdiff/9b39b799db781642dd0c1424c28e827d19663e20


- Fix snapshot leak warning for some procedures.  The problem arises with the
  combination of CALL with output parameters and doing a COMMIT inside the
  procedure.  When a CALL has output parameters, the portal uses the strategy
  PORTAL_UTIL_SELECT instead of PORTAL_MULTI_QUERY.  Using PORTAL_UTIL_SELECT
  causes the portal's snapshot to be registered with the current resource owner
  (portal->holdSnapshot); see 9ee1cf04ab6bcefe03a11837b53f29ca9dc24c7a for the
  reason.  Normally, PortalDrop() unregisters the snapshot.  If not, then
  ResourceOwnerRelease() will print a warning about a snapshot leak on
  transaction commit.  A transaction commit normally drops all portals
  (PreCommit_Portals()), except the active portal.  So in case of the active
  portal, we need to manually release the snapshot to avoid the warning.
  Reported-by: Prabhat Sahu <prabhat(dot)sahu(at)enterprisedb(dot)com> Reviewed-by:
  Jonathan S. Katz <jkatz(at)postgresql(dot)org>
  https://git.postgresql.org/pg/commitdiff/7a3b7bbfded3142aaa8edae2dbc88999568cc1cd


- pg_verify_checksums: Message style improvements and NLS support.  The source
  code was already set up for NLS support, so just a nls.mk file needed to be
  added.  Also, fix the old problem of putting the int64 format specifier right
  into the string, which breaks NLS.
  https://git.postgresql.org/pg/commitdiff/3e2ceb231ef0bbd04bb98aa3d3b58ebcac88c00a


- Error position support for partition specifications.  Add support for error
  position reporting for partition specifications.  Reviewed-by: Fabien COELHO
  <coelho(at)cri(dot)ensmp(dot)fr>
  https://git.postgresql.org/pg/commitdiff/1e5e4efd02b614908cae62d9452528462d307224


- Error position support for defaults and check constraints.  Add support for
  error position reporting for the expressions contained in defaults and check
  constraint definitions.  This currently works only for CREATE TABLE, not ALTER
  TABLE, because the latter is not set up to pass around the original query
  string.  Reviewed-by: Fabien COELHO <coelho(at)cri(dot)ensmp(dot)fr>
  https://git.postgresql.org/pg/commitdiff/a4a232b1e70229a6ba0e592f6775c019bb171d9a


- pg_dump: Reorganize getTableAttrs().  Instead of repeating the almost same
  large query in each version branch, use one query and add a few columns to the
  SELECT list depending on the version.  This saves a lot of duplication.
  Reviewed-by: Tom Lane <tgl(at)sss(dot)pgh(dot)pa(dot)us>
  https://git.postgresql.org/pg/commitdiff/daa9fe8a5264a3f192efa5ddee8fb011ad9da365


- Add semicolons to end of internally run queries.  This ensures that the --echo
  output of various tools (under scripts) is valid multiline SQL.  Author:
  Tatsuro Yamada <yamada(dot)tatsuro(at)lab(dot)ntt(dot)co(dot)jp>
  https://git.postgresql.org/pg/commitdiff/7061e03319d9a31f02d3777ca856b6c33e7a0967


Tom Lane pushed:


- Fix missing dependency for pg_dump's ENABLE ROW LEVEL SECURITY items.  The
  archive should show a dependency on the item's table, but it failed to include
  one.  This could cause failures in parallel restore due to emitting ALTER
  TABLE ... ENABLE ROW LEVEL SECURITY before restoring the table's data.  In
  practice the odds of a problem seem low, since you would typically need to
  have set FORCE ROW LEVEL SECURITY as well, and you'd also need a very high
  --jobs count to have any chance of this happening.  That probably explains the
  lack of field reports.  Still, it's a bug, so back-patch to 9.5 where RLS was
  introduced.  Discussion: https://postgr.es/m/19784.1535390902@sss.pgh.pa.us
  https://git.postgresql.org/pg/commitdiff/cbdca00bef59ee204313fe8f0e4f36bc804a38aa


- Include contrib modules in the temp installation even without REGRESS.  Now
  that we have TAP tests, a contrib module may have something useful to do in
  "make check" even if it has no pg_regress-style regression scripts, and hence
  no REGRESS setting.  But the TAP tests will fail, or else test the wrong
  installed files, unless we install the contrib module into the temp
  installation.  So move the bit about adding to EXTRA_INSTALL so that it
  applies regardless.  We might want this in back branches in future, but for
  the moment I only risked adding it to v11.  Discussion:
  https://postgr.es/m/12438.1535488750@sss.pgh.pa.us
  https://git.postgresql.org/pg/commitdiff/42e61c7748eb36b75a05bd0a9a35c370c70a86c8


- Make pg_restore's identify_locking_dependencies() more bulletproof.  This
  function had a blacklist of dump object types that it believed needed
  exclusive lock ... but we hadn't maintained that, so that it was missing ROW
  SECURITY, POLICY, and INDEX ATTACH items, all of which need (or should be
  treated as needing) exclusive lock.  Since the same oversight seems likely in
  future, let's reverse the sense of the test so that the code has a whitelist
  of safe object types; better to wrongly assume a command can't be run in
  parallel than the opposite.  Currently the only POST_DATA object type that's
  safe is CREATE INDEX ... and that list hasn't changed in a long time.
  Back-patch to 9.5 where RLS came in.  Discussion:
  https://postgr.es/m/11450.1535483506@sss.pgh.pa.us
  https://git.postgresql.org/pg/commitdiff/e0a0cc28d0829bea5d339fc2db6ac26ea13d5ab4


- Code review for pg_dump's handling of ALTER INDEX ATTACH PARTITION.  Ensure
  the TOC entry is marked with the correct schema, so that its name is as unique
  as the index's is.  Fix the dependencies: we want dependencies from this TOC
  entry to the two indexes it depends on, and we don't care (at least not for
  this purpose) what order the indexes are created in.  Also, add dependencies
  on the indexes' underlying tables.  Those might seem pointless given the index
  dependencies, but they are helpful to cue parallel restore to avoid running
  the ATTACH PARTITION in parallel with other DDL on the same tables.
  Discussion: https://postgr.es/m/10817.1535494963@sss.pgh.pa.us
  https://git.postgresql.org/pg/commitdiff/8cff4f5348d075e063100071013f00a900c32b0f


- Make checksum_impl.h safe to compile with -fstrict-aliasing.  In general,
  Postgres requires -fno-strict-aliasing with compilers that implement C99
  strict aliasing rules.  There's little hope of getting rid of that overall.
  But it seems like it would be a good idea if storage/checksum_impl.h in
  particular didn't depend on it, because that header is explicitly intended to
  be included by external programs.  We don't have a lot of control over the
  compiler switches that an external program might use, as shown by Michael
  Banck's report of failure in a privately-modified version of
  pg_verify_checksums.  Hence, switch to using a union in place of willy-nilly
  pointer casting inside this file.  I think this makes the code a bit more
  readable anyway.  checksum_impl.h hasn't changed since it was introduced in
  9.3, so back-patch all the way.  Discussion:
  https://postgr.es/m/1535618100.1286.3.camel@credativ.de
  https://git.postgresql.org/pg/commitdiff/8c62d9d16f014565d5f427506878812219a01604


- Code review for pg_verify_checksums.c.  Use postgres_fe.h, since this is
  frontend code.  Pretend that we've heard of project style guidelines for, eg,
  #include order.  Use BlockNumber not int arithmetic for block numbers, to
  avoid misbehavior with relations exceeding 2^31 blocks.  Avoid an unnecessary
  strict-aliasing warning (per report from Michael Banck).  Const-ify assorted
  stuff.  Avoid scribbling on the output of readdir() -- perhaps that's safe in
  practice, but POSIX forbids it, and this code has so far earned exactly zero
  credibility portability-wise.  Editorialize on an ambiguously-worded message.
  I did not touch the problem of the "buf" local variable being possibly
  insufficiently aligned; that's not specific to this code, and seems like it
  should be fixed as part of a different, larger patch.  Discussion:
  https://postgr.es/m/1535618100.1286.3.camel@credativ.de
  https://git.postgresql.org/pg/commitdiff/d9c366f9e8017306201fe12d27212d8720395c04


- Fix psql's \dC command to annotate I/O conversion casts as such.  A cast
  declared WITH INOUT was described as '(binary coercible)', which seems pretty
  inaccurate; let's print '(with inout)' instead.  Per complaint from
  Jean-Pierre Pelletier.  This definitely seems like a bug fix, but given that
  it's been wrong since 8.4 and nobody complained before, I'm hesitant to
  back-patch a behavior change into stable branches.  It doesn't seem too late
  for v11 though.  Discussion:
  https://postgr.es/m/5b887023.1c69fb81.ff96e.6a1d@mx.google.com
  https://git.postgresql.org/pg/commitdiff/115bf1e79af0114c18d7d5675f4ba7e8bd6e11e9


- Avoid using potentially-under-aligned page buffers.  There's a project policy
  against using plain "char buf[BLCKSZ]" local or static variables as page
  buffers; preferred style is to palloc or malloc each buffer to ensure it is
  MAXALIGN'd.  However, that policy's been ignored in an increasing number of
  places.  We've apparently got away with it so far, probably because (a)
  relatively few people use platforms on which misalignment causes core dumps
  and/or (b) the variables chance to be sufficiently aligned anyway.  But this
  is not something to rely on.  Moreover, even if we don't get a core dump, we
  might be paying a lot of cycles for misaligned accesses.  To fix, invent new
  union types PGAlignedBlock and PGAlignedXLogBlock that the compiler must
  allocate with sufficient alignment, and use those in place of plain char
  arrays.  I used these types even for variables where there's no risk of a
  misaligned access, since ensuring proper alignment should make kernel data
  transfers faster.  I also changed some places where we had been palloc'ing
  short-lived buffers, for coding style uniformity and to save palloc/pfree
  overhead.  Since this seems to be a live portability hazard (despite the lack
  of field reports), back-patch to all supported versions.  Patch by me; thanks
  to Michael Paquier for review.  Discussion:
  https://postgr.es/m/1535618100.1286.3.camel@credativ.de
  https://git.postgresql.org/pg/commitdiff/44cac9346479d4b0cc9195b0267fd13eb4e7442c


- Doc: fix oversights in "Client/Server Character Set Conversions" table.  This
  table claimed that JOHAB could be used as a server encoding, which was true
  originally but hasn't been true since 8.3.  It also lacked entries for
  EUC_JIS_2004 and SHIFT_JIS_2004.  JOHAB problem noted by Lars Kanis, the
  others by me.  Discussion:
  https://postgr.es/m/c0f514a1-b7a9-b9ea-1c02-c34aead56c06@greiz-reinsdorf.de
  https://git.postgresql.org/pg/commitdiff/4299c32316addaad2255e6363b26ba1eec5c3999


Thomas Munro pushed:


- Code review for simplehash.h.  Fix reference to non-existent file in comment.
  Add SH_ prefix to the EMPTY and IN_USE tokens, to reduce likelihood of
  collisions with unrelated macros.  Add include guards around the function
  definitions that are not "parameterized", so the header can be used again in
  the same translation unit.  Undefine SH_EQUAL macro where other "parameter"
  macros are undefined, for the same reason.  Author: Thomas Munro Reviewed-by:
  Tom Lane Discussion:
  https://postgr.es/m/CAEepm%3D1LdXZ3mMTM8tHt_b%3DK1kREit%3Dp8sikesak%3DkzHHM07Nw%40mail.gmail.com
  https://git.postgresql.org/pg/commitdiff/ee0e2745c2f2c8ac47250dde718ac712686a79aa


- Add Greek characters to unaccent.rules.  Author: Tasos Maschalidis
  Reviewed-by: Michael Paquier, Tom Lane Discussion:
  https://postgr.es/m/153495048900.1368.11566580687623014380%40wrigleys.postgresql.org
  Discussion:
  https://postgr.es/m/VI1PR01MB38537EBD529FE5EE3FE9A5FEB5370%40VI1PR01MB3853.eurprd01.prod.exchangelabs.com
  https://git.postgresql.org/pg/commitdiff/5e8d670c313531c0dca245943fb84c94a477ddc4


Andrew Gierth pushed:


- Avoid quadratic slowdown in regexp match/split functions.  regexp_matches,
  regexp_split_to_table and regexp_split_to_array all work by compiling a list
  of match positions as character offsets (NOT byte positions) in the source
  string.  Formerly, they then used text_substr to extract the matched text; but
  in a multi-byte encoding, that counts the characters in the string, and the
  characters needed to reach the starting byte position, on every call.
  Accordingly, the performance degraded as the product of the input string
  length and the number of match positions, such that splitting a string of a
  few hundred kbytes could take many minutes.  Repair by keeping the
  wide-character copy of the input string available (only in the case where
  encoding_max_length is not 1) after performing the match operation, and
  extracting substrings from that instead. This reduces the complexity to being
  linear in the number of result bytes, discounting the actual regexp match
  itself (which is not affected by this patch).  In passing, remove cleanup
  using retail pfree() which was obsoleted by commit ff428cded (Feb 2008) which
  made cleanup of SRF multi-call contexts automatic. Also increase (to ~134
  million) the maximum number of matches and provide an error message when it is
  reached.  Backpatch all the way because this has been wrong forever.  Analysis
  and patch by me; review by Kaiting Chen.  Discussion:
  https://postgr.es/m/87pnyn55qh.fsf@news-spur.riddles.org.uk see also
  https://postgr.es/m/87lg996g4r.fsf@news-spur.riddles.org.uk
  https://git.postgresql.org/pg/commitdiff/c8ea87e4bd950572cba4575e9a62284cebf85ac5


- postgres_fdw: don't push ORDER BY with no vars (bug #15352).  Commit aa09cd242
  changed a condition in find_em_expr_for_rel from being a bms_equal comparison
  of relids to bms_is_subset, in order to support order by clauses on foreign
  joins. But this also allows through the degenerate case of expressions with no
  Vars at all (and hence empty relids), including integer constants which will
  be parsed unexpectedly on the remote (viz. "ERROR: ORDER BY position 0 is not
  in select list" as in the bug report).  Repair by adding an additional
  !bms_is_empty test.  Backpatch through to 9.6 where the aforementioned change
  was made.  Per bug #15352 from Maksym Boguk; analysis and patch by me.
  Discussion:
  https://postgr.es/m/153518420278.1478.14875560810251994661@wrigleys.postgresql.org
  https://git.postgresql.org/pg/commitdiff/bf2d0462cd735f76bcf6eb8b399723674b2221ef


Heikki Linnakangas pushed:


- Fix IndexInfo comments.  Recently, ii_KeyAttrNumbers was renamed to
  ii_IndexAttrNumbers, and ii_Am field was added, but the comments were not
  updated.  Author: Yugo Nagata Discussion:
  https://www.postgresql.org/message-id/20180830134831.e35a91b8b978b248c16c8f7b@sraoss.co.jp
  https://git.postgresql.org/pg/commitdiff/4b035841a1bcaadbe4f9e0e174aef773a4fa41f6


Álvaro Herrera pushed:


- Mention change of width of values generated by SERIAL sequences.  This changed
  during pg10 development, but had not been documented.  Co-authored-by:
  Jonathan S. Katz <jkatz(at)postgresql(dot)org> Discussion:
  https://postgr.es/m/20180828163408.vl44nwetdybwffyk@alvherre.pgsql
  https://git.postgresql.org/pg/commitdiff/4db226b756529ea4d357a4af507c6ed2c31415c0


- pg_verify_checksums: rename -d to --verbose.  Using -d is odd, because we
  normally reserve that for a database argument, so rename it to -v and add long
  version --verbose.  Also, reduce it to emit one line per file checked rather
  than one line per block.  Per a complaint from Michael Banck.  Author: Yugo
  Nagata <nagata(at)sraoss(dot)co(dot)jp> Reviewed-by: Michael Banck
  <michael(dot)banck(at)credativ(dot)de> Discussion:
  https://postgr.es/m/20180827113411.GA22768@nighthawk.caipicrew.dd-dns.de
  https://git.postgresql.org/pg/commitdiff/a846e6d0239d24fe9a95c7b12e1905e20f8fdcf0


Etsuro Fujita pushed:


- Remove extra word from src/backend/optimizer/README.
  https://git.postgresql.org/pg/commitdiff/2e39f69b6621bd3d67f650a5647fd0412819712d


- Disable support for partitionwise joins in problematic cases.  Commit f49842d,
  which added support for partitionwise joins, built the child's tlist by
  applying adjust_appendrel_attrs() to the parent's.  So in the case where the
  parent's included a whole-row Var for the parent, the child's contained a
  ConvertRowtypeExpr.  To cope with that, that commit added code to the planner,
  such as setrefs.c, but some code paths still assumed that the tlist for a scan
  (or join) rel would only include Vars and PlaceHolderVars, which was true
  before that commit, causing errors: * When creating an explicit sort node for
  an input path for a mergejoin path for a child join,
  prepare_sort_from_pathkeys() threw the 'could not find pathkey item to sort'
  error.  * When deparsing a relation participating in a pushed down child join
  as a subquery in contrib/postgres_fdw, get_relation_column_alias_ids() threw
  the 'unexpected expression in subquery output' error.  * When performing
  set_plan_references() on a local join plan generated by contrib/postgres_fdw
  for EvalPlanQual support for a pushed down child join, fix_join_expr() threw
  the 'variable not found in subplan target lists' error.  To fix these, two
  approaches have been proposed: one by Ashutosh Bapat and one by me.  While the
  former keeps building the child's tlist with a ConvertRowtypeExpr, the latter
  builds it with a whole-row Var for the child not to violate the planner
  assumption, and tries to fix it up later, But both approaches need more work,
  so refuse to generate partitionwise join paths when whole-row Vars are
  involved, instead.  We don't need to handle ConvertRowtypeExprs in the child's
  tlists for now, so this commit also removes the changes to the planner.
  Previously, partitionwise join computed attr_needed data for each child
  separately, and built the child join's tlist using that data, which also
  required an extra step for adding PlaceHolderVars to that tlist, but it would
  be more efficient to build it from the parent join's tlist through the
  adjust_appendrel_attrs() transformation.  So this commit builds that list that
  way, and simplifies build_joinrel_tlist() and placeholder.c as well as part of
  set_append_rel_size() to basically what they were before partitionwise join
  went in.  Back-patch to PG11 where partitionwise join was introduced.  Report
  by Rajkumar Raghuwanshi.  Analysis by Ashutosh Bapat, who also provided some
  of regression tests.  Patch by me, reviewed by Robert Haas.  Discussion:
  https://postgr.es/m/CAKcux6ktu-8tefLWtQuuZBYFaZA83vUzuRd7c1YHC-yEWyYFpg@mail.gmail.com
  https://git.postgresql.org/pg/commitdiff/7cfdc77023ad50731723e85c215a4127436ed09c


Amit Kapila pushed:


- Fix pg_verify_checksums on Windows.  To verify the checksums, we open the file
  in text mode which doesn't work on Windows as WIN32 treats Control-Z as EOF in
  files opened in text mode.  This leads to "short read of block .." error in
  some cases.  Fix it by opening the files in the binary mode.  Author: Amit
  Kapila Reviewed-by: Magnus Hagander Backpatch-through: 11 Discussion:
  https://postgr.es/m/CAA4eK1+LOnzod+h85FGmyjWzXKy-XV1FYwEyP-Tky2WpD5cxwA@mail.gmail.com
  https://git.postgresql.org/pg/commitdiff/bb60f2cb6ed8361fbf18b92d312776046d9b0103


Alexander Korotkov pushed:


- Enforce cube dimension limit in all cube construction functions.  contrib/cube
  has a limit to 100 dimensions for cube datatype.  However, it's not enforced
  everywhere, and one can actually construct cube with more than 100 dimensions
  having then trouble with dump/restore.  This commit add checks for dimensions
  limit in all functions responsible for cube construction.  Backpatch to all
  supported versions.  Reported-by: Andrew Gierth Discussion:
  https://postgr.es/m/87va7uybt4.fsf%40news-spur.riddles.org.uk Author: Andrey
  Borodin with small additions by me Review: Tom Lane Backpatch-through: 9.3
  https://git.postgresql.org/pg/commitdiff/f919c165ebdc2f85e4584e959e002705a5a0a774


- Split contrib/cube platform-depended checks into separate test.  We're
  currently maintaining two outputs for cube regression test.  But that appears
  to be unsuitable, because these outputs are different in out few checks
  involving scientific notation.  So, split checks involving scientific notation
  into separate test, making contrib/cube easier to maintain.  Backpatch to all
  supported versions in order to make further backpatching easier.  Discussion:
  https://postgr.es/m/CAPpHfdvJgWjxHsJTtT%2Bo1tz3OR8EFHcLQjhp-d3%2BUcmJLh-fQA%40mail.gmail.com
  Author: Alexander Korotkov Backpatch-through: 9.3
  https://git.postgresql.org/pg/commitdiff/38970ce862b906d3b6e3745bff8c75edad378de3


- Implement "pg_ctl logrotate" command.  Currently there are two ways to trigger
  log rotation in logging collector process: call pg_rotate_logfile()
  SQL-function or send SIGUSR1 signal directly to logging collector process.
  However, it's nice to have more suitable way for external tools to do that,
  which wouldn't require SQL connection or knowledge of logging collector pid.
  This commit implements triggering log rotation by "pg_ctl logrotate" command.
  Discussion:
  https://postgr.es/m/20180416.115435.28153375.horiguchi.kyotaro%40lab.ntt.co.jp
  Author: Kyotaro Horiguchi, Alexander Kuzmenkov, Alexander Korotkov
  https://git.postgresql.org/pg/commitdiff/ec74369931687885cfb6ce9dac55deefdb410086


Andres Freund pushed:


- Fix 8a934d677 for libc++ and make more include order resistant.  The previous
  definition was used in C++ mode, which causes problems when using clang with
  libc++ (rather than libstdc++), due to bugs therein.  So just avoid in C++
  mode.  A second problem is that depending on include order and implicit
  includes the previous definition did not guarantee that the current hack was
  effective by the time isinf was used, fix that by forcing math.h to be
  included.  This can cause clang using builds, or gcc using ones with JIT
  enabled, to slow down noticably.  It's likely that we at some point want a
  better solution for the performance problem, but while it's there it should
  better work.  Reported-By: Steven Winfield Bug: #15270 Discussion:
  https://postgr.es/m/153116283147.1401.360416241833049560@wrigleys.postgresql.org
  Author: Andres Freund Backpatch: 11, like the previous commit.
  https://git.postgresql.org/pg/commitdiff/5758685c9f1a51b0a77ae8f415a57670941f2c4b


Noah Misch pushed:


E Ignore server-side delays when enforcing wal_sender_timeout.  Healthy clients
  of servers having poor I/O performance, such as buildfarm members hamster and
  tern, saw unexpected timeouts.  That disagreed with documentation.  This fix
  adds one gettimeofday() call whenever ProcessRepliesIfAny() finds no client
  reply messages.  Back-patch to 9.4; the bug's symptom is rare and mild, and
  the code all moved between 9.3 and 9.4.  Discussion:
  https://postgr.es/m/20180826034600.GA1105084@rfd.leadboat.com
  https://git.postgresql.org/pg/commitdiff/ab0ed6153a58294143d6d66ec5f3471477c59d57


== Pending Patches ==


Daniel Gustafsson sent in another revision of a patch to refactor the backend
signalling code and use the new structure to support an optional message in
backend cancel/terminate.


Konstantin Knizhnik sent in another revision of a patch to implement an internal
connection pooler.


Bradley DeJong sent in another revision of a patch to document the fact that as
of version 3.0 of the wire protocol, the terminal '\.' for COPY is both optional
and deprecated.


Kyotaro HORIGUCHI sent in another revision of a patch to ensure that the
checkpointer not update shared FPW flag during recovery, set the correct value
of full_page_write reloaded during recovery, and ensure that startup process
ignores SIGHUP.


Daniel Vérité sent in another revision of a patch to add a csv output format to
psql.


Surafel Temesgen sent in two more revisions of a patch to add a PERCENT option
to the FETCH FIRST clause.


Ashutosh Bapat sent in another revision of a patch to implement the
TupleTableSlot abstraction.


Noriyoshi Shinoda sent in two more revisions of a patch to add work_mem as a
setting for the PostgreSQL FDW.


Yugo Nagata sent in another revision of a patch to refactor
textToQualifiedNameList().


Andres Freund and Tom Lane traded patches to fix a problem where lmgr.c was
falsely assuming that AcceptInvalidationMessages is an atomic operation.


Alexander Korotkov sent in another revision of a patch to implement
k-Nearest-Neighbor for SP-GiST.


Masahiko Sawada sent in another revision of a patch to implement a copy function
for logical and physical replication slots.


Naoki Yotsunaga sent in another revision of a patch to add an automatic restore
point.


Peter Eisentraut sent in another revision of a patch to add GnuTLS support for
TLS connections.


Antonin Houska sent in another revision of a patch to implement aggregate
pushdown.


Peter Eisentraut sent in two more revisions of a patch to remove ancient
pre-dlopen dynloader code.


Dilip Kumar sent in another revision of a patch to implement UNDO logs.


Peter Eisentraut sent in another revision of a patch to allow using file cloning
in pg_upgrade and CREATE DATABASE where that capability is available.


Thomas Munro sent in another revision of a patch to add a WL_EXIT_ON_PM_DEATH
pseudo-event and clean up places that mishandled postmaster death.


David Rowley sent in two revisions of a patch to fix typos in typcache.c


Peter Eisentraut sent in a patch to PL/PythonU to remove use of simple slicing
API.


Peter Eisentraut sent in two revisions of a patch to add error position support
for defaults, check constraints, and partition specifications, and adds location
support to Value nodes, using same to add error position support to the COPY
command.


Marín Fernández sent in a patch to Fix formatting in pg_upgrade manpage docs
location support to Value nodes, using same to add error position support to the
COPY command.


Martín Fernández sent in a patch to fix the formatting in the pg_upgrade manpage
doc.


Dagfinn Ilmari Mannsåker sent in two revisions of a patch to add tab completion
for ALTER DATABASE ... SET TABLESPACE to psql.


Peter Eisentraut sent in a patch to use C99 designated initializers for some
structs.


Masahiko Sawada sent in a patch to implement CREATE ROUTINE MAPPING in
PostgreSQL and use same in the PostgreSQL FDW.


Amit Kapila sent in two revisions of a patch to speed up planning with
partitions.


Alexander Korotkov sent in a patch to add a notion of startup cost to sequential
scans.


Amit Kapila sent in a patch to fix an issue where pg_verify_checksums failed
with hash indexes.


Kyotaro HORIGUCHI sent in two revisions of a patch to refactor the parameters of
GiST insertion routines and fix gistSplit's error message.


Hubert Zhang and Pavel Stěhule traded patches to add a disk quota feature.


Álvaro Herrera sent in a patch to remove pg_constraint.conincluding on grounds
of uselessness.
