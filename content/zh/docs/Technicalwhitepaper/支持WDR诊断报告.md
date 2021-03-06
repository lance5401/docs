# 支持WDR诊断报告<a name="ZH-CN_CONCEPT_0252569386"></a>

WDR\(Workload Diagnosis Report\)基于两次不同时间点系统的性能快照数据， 生成这两个时间点之间的性能表现报表，用于诊断数据库内核的性能故障。

WDR主要依赖两个组件：

-   SNAPSHOT性能快照：性能快照可以配置成按一定时间间隔从内核采集一定量的性能数据，持久化在用户表空间。任何一个SNAPSHOT可以作为一个性能基线，其他SNAPSHOT与之比较的结果，可以分析出与基线的性能表现。
-   WDR Reporter：报表生成工具基于两个SNAPSHOT，分析系统总体性能表现，并能计算出更多项具体的性能指标在这两个时间段之间的变化量，生成SUMMARY 和DETAIL两个不同级别的性能数据。如[表1](#zh-cn_concept_0238164494_table14895120191613)、[表2](#zh-cn_concept_0238164494_table23331848193120)所示。

**表 1**  SUMMARY级别诊断报告

<a name="zh-cn_concept_0238164494_table14895120191613"></a>
<table><thead align="left"><tr id="zh-cn_concept_0238164494_row1889513016163"><th class="cellrowborder" valign="top" width="24.77%" id="mcps1.2.3.1.1"><p id="zh-cn_concept_0238164494_p689512091618"><a name="zh-cn_concept_0238164494_p689512091618"></a><a name="zh-cn_concept_0238164494_p689512091618"></a>诊断类别</p>
</th>
<th class="cellrowborder" valign="top" width="75.22999999999999%" id="mcps1.2.3.1.2"><p id="zh-cn_concept_0238164494_p118951404165"><a name="zh-cn_concept_0238164494_p118951404165"></a><a name="zh-cn_concept_0238164494_p118951404165"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_concept_0238164494_row1189517019163"><td class="cellrowborder" valign="top" width="24.77%" headers="mcps1.2.3.1.1 "><p id="zh-cn_concept_0238164494_p16896205162"><a name="zh-cn_concept_0238164494_p16896205162"></a><a name="zh-cn_concept_0238164494_p16896205162"></a>Database Stat</p>
</td>
<td class="cellrowborder" valign="top" width="75.22999999999999%" headers="mcps1.2.3.1.2 "><p id="zh-cn_concept_0238164494_p7110144513222"><a name="zh-cn_concept_0238164494_p7110144513222"></a><a name="zh-cn_concept_0238164494_p7110144513222"></a>主要用于评估当前数据库上的负载，IO状况，负载和IO是衡量TP系统最最要的特性</p>
<p id="zh-cn_concept_0238164494_p15896180171619"><a name="zh-cn_concept_0238164494_p15896180171619"></a><a name="zh-cn_concept_0238164494_p15896180171619"></a>包含当前连接到该数据库的session，提交、回滚的事务数，读取的磁盘块的数量，高速缓存中已经发现的磁盘块的次数，通过数据库查询返回、抓取、插入、更新、删除的行数，冲突、死锁发生的次数，临时文件的使用量，IO读写时间等</p>
</td>
</tr>
<tr id="zh-cn_concept_0238164494_row589614018168"><td class="cellrowborder" valign="top" width="24.77%" headers="mcps1.2.3.1.1 "><p id="zh-cn_concept_0238164494_p2896170181618"><a name="zh-cn_concept_0238164494_p2896170181618"></a><a name="zh-cn_concept_0238164494_p2896170181618"></a>Load Profile</p>
</td>
<td class="cellrowborder" valign="top" width="75.22999999999999%" headers="mcps1.2.3.1.2 "><p id="zh-cn_concept_0238164494_p2089612013161"><a name="zh-cn_concept_0238164494_p2089612013161"></a><a name="zh-cn_concept_0238164494_p2089612013161"></a>从时间，IO，事务，SQL几个维度评估当前系统负载的表现</p>
<p id="zh-cn_concept_0238164494_p161691350122212"><a name="zh-cn_concept_0238164494_p161691350122212"></a><a name="zh-cn_concept_0238164494_p161691350122212"></a>包含作业运行elapse time、CPU time，事务日质量，逻辑和物理读的量，读写IO次数、大小，登入登出次数，SQL、事务执行量，SQL P85、P90响应时间等</p>
</td>
</tr>
<tr id="zh-cn_concept_0238164494_row889614011167"><td class="cellrowborder" valign="top" width="24.77%" headers="mcps1.2.3.1.1 "><p id="zh-cn_concept_0238164494_p11896801161"><a name="zh-cn_concept_0238164494_p11896801161"></a><a name="zh-cn_concept_0238164494_p11896801161"></a>Instance Efficiency Percentages</p>
</td>
<td class="cellrowborder" valign="top" width="75.22999999999999%" headers="mcps1.2.3.1.2 "><p id="zh-cn_concept_0238164494_p146120311858"><a name="zh-cn_concept_0238164494_p146120311858"></a><a name="zh-cn_concept_0238164494_p146120311858"></a>用于评估当前系统的缓存的效率。</p>
<p id="zh-cn_concept_0238164494_p1989610091613"><a name="zh-cn_concept_0238164494_p1989610091613"></a><a name="zh-cn_concept_0238164494_p1989610091613"></a>主要包含数据库缓存命中率</p>
</td>
</tr>
<tr id="zh-cn_concept_0238164494_row189630111613"><td class="cellrowborder" valign="top" width="24.77%" headers="mcps1.2.3.1.1 "><p id="zh-cn_concept_0238164494_p148961007164"><a name="zh-cn_concept_0238164494_p148961007164"></a><a name="zh-cn_concept_0238164494_p148961007164"></a>Events</p>
</td>
<td class="cellrowborder" valign="top" width="75.22999999999999%" headers="mcps1.2.3.1.2 "><p id="zh-cn_concept_0238164494_p115276341657"><a name="zh-cn_concept_0238164494_p115276341657"></a><a name="zh-cn_concept_0238164494_p115276341657"></a>用于评估当前系统内核关键资源，关键事件的性能</p>
<p id="zh-cn_concept_0238164494_p789680191613"><a name="zh-cn_concept_0238164494_p789680191613"></a><a name="zh-cn_concept_0238164494_p789680191613"></a>主要包含数据库内核关键时间的发生次数，时间的等待时间</p>
</td>
</tr>
<tr id="zh-cn_concept_0238164494_row20583178178"><td class="cellrowborder" valign="top" width="24.77%" headers="mcps1.2.3.1.1 "><p id="zh-cn_concept_0238164494_p559717121712"><a name="zh-cn_concept_0238164494_p559717121712"></a><a name="zh-cn_concept_0238164494_p559717121712"></a>Wait Classes</p>
</td>
<td class="cellrowborder" valign="top" width="75.22999999999999%" headers="mcps1.2.3.1.2 "><p id="zh-cn_concept_0238164494_p11553691966"><a name="zh-cn_concept_0238164494_p11553691966"></a><a name="zh-cn_concept_0238164494_p11553691966"></a>用于评估当前系统关键事件类型的性能</p>
<p id="zh-cn_concept_0238164494_p11595172176"><a name="zh-cn_concept_0238164494_p11595172176"></a><a name="zh-cn_concept_0238164494_p11595172176"></a>主要包含数据内核在主要的等待事件的种类上的发布：STATUS、LWLOCK_EVENT、LOCK_EVENT、IO_EVENT</p>
</td>
</tr>
<tr id="zh-cn_concept_0238164494_row1737892971715"><td class="cellrowborder" valign="top" width="24.77%" headers="mcps1.2.3.1.1 "><p id="zh-cn_concept_0238164494_p1437872931714"><a name="zh-cn_concept_0238164494_p1437872931714"></a><a name="zh-cn_concept_0238164494_p1437872931714"></a>CPU</p>
</td>
<td class="cellrowborder" valign="top" width="75.22999999999999%" headers="mcps1.2.3.1.2 "><p id="zh-cn_concept_0238164494_p1437842910178"><a name="zh-cn_concept_0238164494_p1437842910178"></a><a name="zh-cn_concept_0238164494_p1437842910178"></a>主要包含CPU在用户态、内核态、Wait IO、空闲状态下的时间发布</p>
</td>
</tr>
<tr id="zh-cn_concept_0238164494_row13154183712171"><td class="cellrowborder" valign="top" width="24.77%" headers="mcps1.2.3.1.1 "><p id="zh-cn_concept_0238164494_p515514378179"><a name="zh-cn_concept_0238164494_p515514378179"></a><a name="zh-cn_concept_0238164494_p515514378179"></a>IO Profile</p>
</td>
<td class="cellrowborder" valign="top" width="75.22999999999999%" headers="mcps1.2.3.1.2 "><p id="zh-cn_concept_0238164494_p13155133710173"><a name="zh-cn_concept_0238164494_p13155133710173"></a><a name="zh-cn_concept_0238164494_p13155133710173"></a>主要包含数据库Database IO次数、Database IO数据量、Redo IO次数、Redo IO量</p>
</td>
</tr>
<tr id="zh-cn_concept_0238164494_row123476454170"><td class="cellrowborder" valign="top" width="24.77%" headers="mcps1.2.3.1.1 "><p id="zh-cn_concept_0238164494_p934714512178"><a name="zh-cn_concept_0238164494_p934714512178"></a><a name="zh-cn_concept_0238164494_p934714512178"></a>Memory Statistics</p>
</td>
<td class="cellrowborder" valign="top" width="75.22999999999999%" headers="mcps1.2.3.1.2 "><p id="zh-cn_concept_0238164494_p434712455175"><a name="zh-cn_concept_0238164494_p434712455175"></a><a name="zh-cn_concept_0238164494_p434712455175"></a>包含最大进程内存、进程已经使用内存、最大共享内存、已经使用共享内存大小等</p>
</td>
</tr>
</tbody>
</table>

**表 2**  DETAIL 级别诊断报告

<a name="zh-cn_concept_0238164494_table23331848193120"></a>
<table><thead align="left"><tr id="zh-cn_concept_0238164494_row1533312481318"><th class="cellrowborder" valign="top" width="24.93%" id="mcps1.2.3.1.1"><p id="zh-cn_concept_0238164494_p5333948203119"><a name="zh-cn_concept_0238164494_p5333948203119"></a><a name="zh-cn_concept_0238164494_p5333948203119"></a>诊断类别</p>
</th>
<th class="cellrowborder" valign="top" width="75.07000000000001%" id="mcps1.2.3.1.2"><p id="zh-cn_concept_0238164494_p17333144823110"><a name="zh-cn_concept_0238164494_p17333144823110"></a><a name="zh-cn_concept_0238164494_p17333144823110"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_concept_0238164494_row1533315480312"><td class="cellrowborder" valign="top" width="24.93%" headers="mcps1.2.3.1.1 "><p id="zh-cn_concept_0238164494_p113331448163118"><a name="zh-cn_concept_0238164494_p113331448163118"></a><a name="zh-cn_concept_0238164494_p113331448163118"></a>Time Model</p>
</td>
<td class="cellrowborder" valign="top" width="75.07000000000001%" headers="mcps1.2.3.1.2 "><p id="zh-cn_concept_0238164494_p18455944461"><a name="zh-cn_concept_0238164494_p18455944461"></a><a name="zh-cn_concept_0238164494_p18455944461"></a>主要用于评估当前系统在时间维度的性能表现</p>
<p id="zh-cn_concept_0238164494_p33332484313"><a name="zh-cn_concept_0238164494_p33332484313"></a><a name="zh-cn_concept_0238164494_p33332484313"></a>包含系统在各个阶段上消耗的时间：内核时间、CPU时间、执行时间、解析时间、编译时间、查询重写时间、计划生成时间、网络时间、IO时间</p>
</td>
</tr>
<tr id="zh-cn_concept_0238164494_row1233374883113"><td class="cellrowborder" valign="top" width="24.93%" headers="mcps1.2.3.1.1 "><p id="zh-cn_concept_0238164494_p10333948163119"><a name="zh-cn_concept_0238164494_p10333948163119"></a><a name="zh-cn_concept_0238164494_p10333948163119"></a>SQL Statistics</p>
</td>
<td class="cellrowborder" valign="top" width="75.07000000000001%" headers="mcps1.2.3.1.2 "><p id="zh-cn_concept_0238164494_p367217315715"><a name="zh-cn_concept_0238164494_p367217315715"></a><a name="zh-cn_concept_0238164494_p367217315715"></a>主要用于SQL语句性能问题的诊断</p>
<p id="zh-cn_concept_0238164494_p103331848113117"><a name="zh-cn_concept_0238164494_p103331848113117"></a><a name="zh-cn_concept_0238164494_p103331848113117"></a>包含归一化的SQL的性能指标在多个维度上的排序：Elapsed Time、CPU Time、Rows Returned、Tuples Reads、Executions、Physical Reads、Logical Reads。这些指标的种类包括：执行时间，执行次数、行活动、Cache IO等</p>
</td>
</tr>
<tr id="zh-cn_concept_0238164494_row1933324873111"><td class="cellrowborder" valign="top" width="24.93%" headers="mcps1.2.3.1.1 "><p id="zh-cn_concept_0238164494_p183331348193119"><a name="zh-cn_concept_0238164494_p183331348193119"></a><a name="zh-cn_concept_0238164494_p183331348193119"></a>Wait Events</p>
</td>
<td class="cellrowborder" valign="top" width="75.07000000000001%" headers="mcps1.2.3.1.2 "><p id="zh-cn_concept_0238164494_p39281554285"><a name="zh-cn_concept_0238164494_p39281554285"></a><a name="zh-cn_concept_0238164494_p39281554285"></a>主要用于系统关键资源，关键时间的详细性能诊断</p>
<p id="zh-cn_concept_0238164494_p933314823114"><a name="zh-cn_concept_0238164494_p933314823114"></a><a name="zh-cn_concept_0238164494_p933314823114"></a>包含所有关键事件在一段时间内的表现，主要是事件发生的次数，消耗的时间</p>
</td>
</tr>
<tr id="zh-cn_concept_0238164494_row3334148183116"><td class="cellrowborder" valign="top" width="24.93%" headers="mcps1.2.3.1.1 "><p id="zh-cn_concept_0238164494_p4334204817319"><a name="zh-cn_concept_0238164494_p4334204817319"></a><a name="zh-cn_concept_0238164494_p4334204817319"></a>Cache IO Stats</p>
</td>
<td class="cellrowborder" valign="top" width="75.07000000000001%" headers="mcps1.2.3.1.2 "><p id="zh-cn_concept_0238164494_p77092138917"><a name="zh-cn_concept_0238164494_p77092138917"></a><a name="zh-cn_concept_0238164494_p77092138917"></a>用于诊断用户表和索引的性能</p>
<p id="zh-cn_concept_0238164494_p73341848193110"><a name="zh-cn_concept_0238164494_p73341848193110"></a><a name="zh-cn_concept_0238164494_p73341848193110"></a>包含所有用户表、索引上的文件读写，缓存命中</p>
</td>
</tr>
<tr id="zh-cn_concept_0238164494_row233424816311"><td class="cellrowborder" valign="top" width="24.93%" headers="mcps1.2.3.1.1 "><p id="zh-cn_concept_0238164494_p133474810318"><a name="zh-cn_concept_0238164494_p133474810318"></a><a name="zh-cn_concept_0238164494_p133474810318"></a>Utility status</p>
</td>
<td class="cellrowborder" valign="top" width="75.07000000000001%" headers="mcps1.2.3.1.2 "><p id="zh-cn_concept_0238164494_p178211436699"><a name="zh-cn_concept_0238164494_p178211436699"></a><a name="zh-cn_concept_0238164494_p178211436699"></a>用于诊断后端作业性能的诊断</p>
<p id="zh-cn_concept_0238164494_p1334134843114"><a name="zh-cn_concept_0238164494_p1334134843114"></a><a name="zh-cn_concept_0238164494_p1334134843114"></a>包含页面操作，复制等后端操作的性能</p>
</td>
</tr>
<tr id="zh-cn_concept_0238164494_row123341448113113"><td class="cellrowborder" valign="top" width="24.93%" headers="mcps1.2.3.1.1 "><p id="zh-cn_concept_0238164494_p11334848143110"><a name="zh-cn_concept_0238164494_p11334848143110"></a><a name="zh-cn_concept_0238164494_p11334848143110"></a>Object stats</p>
</td>
<td class="cellrowborder" valign="top" width="75.07000000000001%" headers="mcps1.2.3.1.2 "><p id="zh-cn_concept_0238164494_p14405135119915"><a name="zh-cn_concept_0238164494_p14405135119915"></a><a name="zh-cn_concept_0238164494_p14405135119915"></a>用于诊断数据库对象的性能</p>
<p id="zh-cn_concept_0238164494_p6334174863119"><a name="zh-cn_concept_0238164494_p6334174863119"></a><a name="zh-cn_concept_0238164494_p6334174863119"></a>包含用户表、索引上的表、索引扫描活动，insert、update、delete活动，有效行数量，表维护操作的状态等</p>
</td>
</tr>
<tr id="zh-cn_concept_0238164494_row1427793219359"><td class="cellrowborder" valign="top" width="24.93%" headers="mcps1.2.3.1.1 "><p id="zh-cn_concept_0238164494_p32775326355"><a name="zh-cn_concept_0238164494_p32775326355"></a><a name="zh-cn_concept_0238164494_p32775326355"></a>Configuration settings</p>
</td>
<td class="cellrowborder" valign="top" width="75.07000000000001%" headers="mcps1.2.3.1.2 "><p id="zh-cn_concept_0238164494_p1119216811109"><a name="zh-cn_concept_0238164494_p1119216811109"></a><a name="zh-cn_concept_0238164494_p1119216811109"></a>用于判断配置是够有变更</p>
<p id="zh-cn_concept_0238164494_p142774327353"><a name="zh-cn_concept_0238164494_p142774327353"></a><a name="zh-cn_concept_0238164494_p142774327353"></a>包含当前所有配置参数的快照</p>
</td>
</tr>
</tbody>
</table>

应用价值：

-   WDR报表是长期性能问题最主要的诊断手段。基于SNAPSHOT的性能基线，从多维度做性能分析，能帮助DBA 掌握系统负载繁忙程度，各个组件的性能表现，性能瓶颈。
-   SNAPSHOT也是后续性能问题自诊断和自优化建议的重要数据来源。

