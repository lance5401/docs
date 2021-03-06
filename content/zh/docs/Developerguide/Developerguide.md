# 开发者指南<a name="ZH-CN_TOPIC_0242381303"></a>

## 概述<a name="zh-cn_topic_0237649238_section4537382116410"></a>

本文档介绍如何设计、创建、查询和维护数据库。包括SQL语句、存储过程、系统表和视图等。

## 读者对象<a name="zh-cn_topic_0237649238_section4378592816410"></a>

-   数据库管理员。
-   应用程序设计或开发人员。

作为数据库管理员和应用程序开发人员，至少需要了解以下知识：
-   操作系统知识。
-   SQL语法。

## 符号约定<a name="zh-cn_topic_0237649238_section133020216410"></a>

在本文中可能出现下列标志，它们所代表的含义如下。

<a name="zh-cn_topic_0237649238_table2622507016410"></a>
<table><thead align="left"><tr id="zh-cn_topic_0237649238_row1530720816410"><th class="cellrowborder" valign="top" width="20.580000000000002%" id="mcps1.1.3.1.1"><p id="zh-cn_topic_0237649238_p6450074116410"><a name="zh-cn_topic_0237649238_p6450074116410"></a><a name="zh-cn_topic_0237649238_p6450074116410"></a><strong id="zh-cn_topic_0237649238_b2136615816410"><a name="zh-cn_topic_0237649238_b2136615816410"></a><a name="zh-cn_topic_0237649238_b2136615816410"></a>符号</strong></p>
</th>
<th class="cellrowborder" valign="top" width="79.42%" id="mcps1.1.3.1.2"><p id="zh-cn_topic_0237649238_p5435366816410"><a name="zh-cn_topic_0237649238_p5435366816410"></a><a name="zh-cn_topic_0237649238_p5435366816410"></a><strong id="zh-cn_topic_0237649238_b5941558116410"><a name="zh-cn_topic_0237649238_b5941558116410"></a><a name="zh-cn_topic_0237649238_b5941558116410"></a>说明</strong></p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0237649238_row1372280416410"><td class="cellrowborder" valign="top" width="20.580000000000002%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0237649238_p3734547016410"><a name="zh-cn_topic_0237649238_p3734547016410"></a><a name="zh-cn_topic_0237649238_p3734547016410"></a><a name="zh-cn_topic_0237649238_image2670064316410"></a><a name="zh-cn_topic_0237649238_image2670064316410"></a><span><img class="" id="zh-cn_topic_0237649238_image2670064316410" src="figures/zh-cn_image_0242381464.png"></span></p>
</td>
<td class="cellrowborder" valign="top" width="79.42%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0237649238_p1757432116410"><a name="zh-cn_topic_0237649238_p1757432116410"></a><a name="zh-cn_topic_0237649238_p1757432116410"></a>表示如不避免则将会导致死亡或严重伤害的具有高等级风险的危害。</p>
</td>
</tr>
<tr id="zh-cn_topic_0237649238_row466863216410"><td class="cellrowborder" valign="top" width="20.580000000000002%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0237649238_p1432579516410"><a name="zh-cn_topic_0237649238_p1432579516410"></a><a name="zh-cn_topic_0237649238_p1432579516410"></a><a name="zh-cn_topic_0237649238_image4895582316410"></a><a name="zh-cn_topic_0237649238_image4895582316410"></a><span><img class="" id="zh-cn_topic_0237649238_image4895582316410" src="figures/zh-cn_image_0242381460.png"></span></p>
</td>
<td class="cellrowborder" valign="top" width="79.42%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0237649238_p959197916410"><a name="zh-cn_topic_0237649238_p959197916410"></a><a name="zh-cn_topic_0237649238_p959197916410"></a>表示如不避免则可能导致死亡或严重伤害的具有中等级风险的危害。</p>
</td>
</tr>
<tr id="zh-cn_topic_0237649238_row123863216410"><td class="cellrowborder" valign="top" width="20.580000000000002%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0237649238_p1232579516410"><a name="zh-cn_topic_0237649238_p1232579516410"></a><a name="zh-cn_topic_0237649238_p1232579516410"></a><a name="zh-cn_topic_0237649238_image1235582316410"></a><a name="zh-cn_topic_0237649238_image1235582316410"></a><span><img class="" id="zh-cn_topic_0237649238_image1235582316410" src="figures/zh-cn_image_0242381461.png"></span></p>
</td>
<td class="cellrowborder" valign="top" width="79.42%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0237649238_p123197916410"><a name="zh-cn_topic_0237649238_p123197916410"></a><a name="zh-cn_topic_0237649238_p123197916410"></a>表示如不避免则可能导致轻微或中度伤害的具有低等级风险的危害。</p>
</td>
</tr>
<tr id="zh-cn_topic_0237649238_row5786682116410"><td class="cellrowborder" valign="top" width="20.580000000000002%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0237649238_p2204984716410"><a name="zh-cn_topic_0237649238_p2204984716410"></a><a name="zh-cn_topic_0237649238_p2204984716410"></a><a name="zh-cn_topic_0237649238_image4504446716410"></a><a name="zh-cn_topic_0237649238_image4504446716410"></a><span><img class="" id="zh-cn_topic_0237649238_image4504446716410" src="figures/zh-cn_image_0242381462.png"></span></p>
</td>
<td class="cellrowborder" valign="top" width="79.42%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0237649238_p4388861916410"><a name="zh-cn_topic_0237649238_p4388861916410"></a><a name="zh-cn_topic_0237649238_p4388861916410"></a>用于传递设备或环境安全警示信息。如不避免则可能会导致设备损坏、数据丢失、设备性能降低或其它不可预知的结果。</p>
<p id="zh-cn_topic_0237649238_p1238861916410"><a name="zh-cn_topic_0237649238_p1238861916410"></a><a name="zh-cn_topic_0237649238_p1238861916410"></a>“须知”不涉及人身伤害。</p>
</td>
</tr>
<tr id="zh-cn_topic_0237649238_row2856923116410"><td class="cellrowborder" valign="top" width="20.580000000000002%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0237649238_p5555360116410"><a name="zh-cn_topic_0237649238_p5555360116410"></a><a name="zh-cn_topic_0237649238_p5555360116410"></a><a name="zh-cn_topic_0237649238_image799324016410"></a><a name="zh-cn_topic_0237649238_image799324016410"></a><span><img class="" id="zh-cn_topic_0237649238_image799324016410" src="figures/zh-cn_image_0242381463.png"></span></p>
</td>
<td class="cellrowborder" valign="top" width="79.42%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0237649238_p4612588116410"><a name="zh-cn_topic_0237649238_p4612588116410"></a><a name="zh-cn_topic_0237649238_p4612588116410"></a>对正文中重点信息的补充说明。</p>
<p id="zh-cn_topic_0237649238_p1232588116410"><a name="zh-cn_topic_0237649238_p1232588116410"></a><a name="zh-cn_topic_0237649238_p1232588116410"></a>“说明”不是安全警示信息，不涉及人身、设备及环境伤害信息。</p>
</td>
</tr>
</tbody>
</table>
