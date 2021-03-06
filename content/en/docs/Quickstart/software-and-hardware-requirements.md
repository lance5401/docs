# Software and Hardware Requirements<a name="EN-US_TOPIC_0251900888"></a>

This section describes hardware and software requirements of openGauss. It is recommended that servers to be deployed on openGauss have the same software and hardware configurations.

## Hardware Requirements<a name="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_sdd36768784254b8ba03c77c86b831cae"></a>

[Table 1](#en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_t62cd0eed17004265b1b8ad98f302a4bc)  describes the minimum hardware requirements of openGauss. When planning the hardware configuration of a product, consider the data scale and expected database response speed. Plan hardware as required.

**Table  1**  Hardware requirements

<a name="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_t62cd0eed17004265b1b8ad98f302a4bc"></a>
<table><thead align="left"><tr id="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_r22159407d305418785de8468729ae773"><th class="cellrowborder" valign="top" width="12.64%" id="mcps1.2.3.1.1"><p id="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_aeb26fbf45f264229a75a015d5e872c73"><a name="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_aeb26fbf45f264229a75a015d5e872c73"></a><a name="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_aeb26fbf45f264229a75a015d5e872c73"></a>Hardware</p>
</th>
<th class="cellrowborder" valign="top" width="87.36%" id="mcps1.2.3.1.2"><p id="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_ae6742eb120254caba0d2e3e8d78d3ce6"><a name="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_ae6742eb120254caba0d2e3e8d78d3ce6"></a><a name="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_ae6742eb120254caba0d2e3e8d78d3ce6"></a>Description</p>
</th>
</tr>
</thead>
<tbody><tr id="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_r6e9f20e9463c41fa8ce77903aa38e901"><td class="cellrowborder" valign="top" width="12.64%" headers="mcps1.2.3.1.1 "><p id="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_aac597314796e4f32be5624781db96791"><a name="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_aac597314796e4f32be5624781db96791"></a><a name="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_aac597314796e4f32be5624781db96791"></a>Minimum memory</p>
</td>
<td class="cellrowborder" valign="top" width="87.36%" headers="mcps1.2.3.1.2 "><p id="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_a1eb44a187b20406fa74eee0a502319b1"><a name="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_a1eb44a187b20406fa74eee0a502319b1"></a><a name="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_a1eb44a187b20406fa74eee0a502319b1"></a>Minimum 32 GB of memory is required for function debugging.</p>
<p id="en-us_topic_0249784577_en-us_topic_0241802565_p2733433132815"><a name="en-us_topic_0249784577_en-us_topic_0241802565_p2733433132815"></a><a name="en-us_topic_0249784577_en-us_topic_0241802565_p2733433132815"></a>In performance tests and commercial deployment, the single-instance deployment is performed. It is recommended that the memory be greater than 128 GB.</p>
<p id="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_ab636748c0876485b987945069966473e"><a name="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_ab636748c0876485b987945069966473e"></a><a name="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_ab636748c0876485b987945069966473e"></a>Complex queries require much memory but the memory may be insufficient in high-concurrency scenarios. In this case, it is recommended that a large-memory server or load management be used to restrict concurrences on the system.</p>
</td>
</tr>
<tr id="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_row18457708163752"><td class="cellrowborder" valign="top" width="12.64%" headers="mcps1.2.3.1.1 "><p id="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_p18679412163752"><a name="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_p18679412163752"></a><a name="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_p18679412163752"></a>CPU</p>
</td>
<td class="cellrowborder" valign="top" width="87.36%" headers="mcps1.2.3.1.2 "><p id="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_p36637388163752"><a name="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_p36637388163752"></a><a name="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_p36637388163752"></a>Minimum one 8-core 2.0 GHz CPU is required for function debugging.</p>
<p id="en-us_topic_0249784577_en-us_topic_0241802565_p655107143013"><a name="en-us_topic_0249784577_en-us_topic_0241802565_p655107143013"></a><a name="en-us_topic_0249784577_en-us_topic_0241802565_p655107143013"></a>In performance tests and commercial deployment, the single-instance deployment is performed. It is recommended that one 16-core 2.0 GHz CPU be used.</p>
<p id="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_p2939854163851"><a name="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_p2939854163851"></a><a name="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_p2939854163851"></a>You can set CPUs to hyper-threading or non-hyper-threading mode, but ensure the setting is consistent across all the <span id="en-us_topic_0249784577_text115011549754"><a name="en-us_topic_0249784577_text115011549754"></a><a name="en-us_topic_0249784577_text115011549754"></a>openGauss</span> nodes.</p>
</td>
</tr>
<tr id="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_rc2f89a29186544e79e7995d19878a617"><td class="cellrowborder" valign="top" width="12.64%" headers="mcps1.2.3.1.1 "><p id="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_aeb29f61cf13345269542500c96fa3370"><a name="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_aeb29f61cf13345269542500c96fa3370"></a><a name="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_aeb29f61cf13345269542500c96fa3370"></a>Hard disk</p>
</td>
<td class="cellrowborder" valign="top" width="87.36%" headers="mcps1.2.3.1.2 "><p id="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_p27815444154057"><a name="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_p27815444154057"></a><a name="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_p27815444154057"></a>Hard disks used for installing the <span id="en-us_topic_0249784577_text434316502057"><a name="en-us_topic_0249784577_text434316502057"></a><a name="en-us_topic_0249784577_text434316502057"></a>openGauss</span> must meet the following requirements:</p>
<a name="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_ul38458483154057"></a><a name="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_ul38458483154057"></a><ul id="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_ul38458483154057"><li>At least 1 GB is used to install the <span id="en-us_topic_0249784577_text119716545518"><a name="en-us_topic_0249784577_text119716545518"></a><a name="en-us_topic_0249784577_text119716545518"></a>openGauss</span> application package.</li><li>About 300 MB is used for each host to store metadata.</li><li>More than 70% of available disk space is reserved to store data.</li></ul>
<p id="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_p1864232295654"><a name="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_p1864232295654"></a><a name="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_p1864232295654"></a>You are advised to configure the system disk to RAID 1 and data disk to RAID 5 and plan four groups of RAID 5 data disks for installing <span id="en-us_topic_0249784577_text977517418"><a name="en-us_topic_0249784577_text977517418"></a><a name="en-us_topic_0249784577_text977517418"></a>openGauss</span>. RAID configuration is not described in this document. You can configure RAID by following instructions in the hardware vendors' manuals or using common methods found on the Internet. Set <strong id="en-us_topic_0249784577_b1171114154153"><a name="en-us_topic_0249784577_b1171114154153"></a><a name="en-us_topic_0249784577_b1171114154153"></a>Disk Cache Policy</strong> to <strong id="en-us_topic_0249784577_b15716111561518"><a name="en-us_topic_0249784577_b15716111561518"></a><a name="en-us_topic_0249784577_b15716111561518"></a>Disabled</strong> to avoid data loss in an unexpected power-off.</p>
<p id="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_p32157354152912"><a name="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_p32157354152912"></a><a name="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_p32157354152912"></a><span id="en-us_topic_0249784577_text283517517410"><a name="en-us_topic_0249784577_text283517517410"></a><a name="en-us_topic_0249784577_text283517517410"></a>openGauss</span> supports using an SSD with the SAS interface and NVMe protocol deployed in RAID mode as the primary storage device of the database.</p>
</td>
</tr>
<tr id="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_rfd1c9b77d83d4ffba092bdfbdc322881"><td class="cellrowborder" valign="top" width="12.64%" headers="mcps1.2.3.1.1 "><p id="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_a176cf03cd96e4828a9fcb162c5013968"><a name="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_a176cf03cd96e4828a9fcb162c5013968"></a><a name="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_a176cf03cd96e4828a9fcb162c5013968"></a>Network requirements</p>
</td>
<td class="cellrowborder" valign="top" width="87.36%" headers="mcps1.2.3.1.2 "><p id="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_a3f99d3fb009c4aeaae03e63a481f33ff"><a name="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_a3f99d3fb009c4aeaae03e63a481f33ff"></a><a name="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_a3f99d3fb009c4aeaae03e63a481f33ff"></a>Minimum 300 Mbit/s Ethernet is required.</p>
<p id="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_p64430430154726"><a name="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_p64430430154726"></a><a name="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_p64430430154726"></a>You are advised to bond two NICs for redundancy. The configuration is not described in this document. You can configure it by following instructions in the manual provided by the hardware manufacturer or using the methods provided on the Internet.</p>
<p id="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_p35810156152855"><a name="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_p35810156152855"></a><a name="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_p35810156152855"></a>If bonds are configured for the <span id="en-us_topic_0249784577_text957712554514"><a name="en-us_topic_0249784577_text957712554514"></a><a name="en-us_topic_0249784577_text957712554514"></a>openGauss</span>, ensure the consistency among these bond modes, because inconsistent bond modes may cause <span id="en-us_topic_0249784577_text13501356558"><a name="en-us_topic_0249784577_text13501356558"></a><a name="en-us_topic_0249784577_text13501356558"></a>openGauss</span> running exceptions.</p>
</td>
</tr>
</tbody>
</table>

## Software Requirements<a name="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_s3124e90db74142ddaf11e2e8fd69cadb"></a>

**Table  2**  Software requirements

<a name="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_tfb195a8129b24c709d238b091e57405a"></a>
<table><thead align="left"><tr id="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_rbb0bb8c17c0c49fc9666f58bdd5487bb"><th class="cellrowborder" valign="top" width="25.240000000000002%" id="mcps1.2.3.1.1"><p id="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_a177f29c592264a53a346a3b6c33a3ea0"><a name="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_a177f29c592264a53a346a3b6c33a3ea0"></a><a name="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_a177f29c592264a53a346a3b6c33a3ea0"></a>Software</p>
</th>
<th class="cellrowborder" valign="top" width="74.76%" id="mcps1.2.3.1.2"><p id="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_a39384e588fc744db804eb3f5beecaa53"><a name="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_a39384e588fc744db804eb3f5beecaa53"></a><a name="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_a39384e588fc744db804eb3f5beecaa53"></a>Description</p>
</th>
</tr>
</thead>
<tbody><tr id="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_rd18980a861d444ad8e87a077e7785e40"><td class="cellrowborder" valign="top" width="25.240000000000002%" headers="mcps1.2.3.1.1 "><p id="en-us_topic_0249784577_en-us_topic_0085434629_en-us_topic_0059782022_a6036b745c87c44ab85a2f6cec7c4e5da"><a name="en-us_topic_0249784577_en-us_topic_0085434629_en-us_topic_0059782022_a6036b745c87c44ab85a2f6cec7c4e5da"></a><a name="en-us_topic_0249784577_en-us_topic_0085434629_en-us_topic_0059782022_a6036b745c87c44ab85a2f6cec7c4e5da"></a>Linux OS</p>
</td>
<td class="cellrowborder" valign="top" width="74.76%" headers="mcps1.2.3.1.2 "><p id="en-us_topic_0249784577_p4796111023815"><a name="en-us_topic_0249784577_p4796111023815"></a><a name="en-us_topic_0249784577_p4796111023815"></a>openEuler 20.3LTS and CentOS 7.6</p>
</td>
</tr>
<tr id="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_rf52ebb45df8e4f57882a97bef3b36ca6"><td class="cellrowborder" valign="top" width="25.240000000000002%" headers="mcps1.2.3.1.1 "><p id="en-us_topic_0249784577_en-us_topic_0085434629_en-us_topic_0059782022_a6f023000ee654c70b98c163f8c9b5d99"><a name="en-us_topic_0249784577_en-us_topic_0085434629_en-us_topic_0059782022_a6f023000ee654c70b98c163f8c9b5d99"></a><a name="en-us_topic_0249784577_en-us_topic_0085434629_en-us_topic_0059782022_a6f023000ee654c70b98c163f8c9b5d99"></a>Linux file system</p>
</td>
<td class="cellrowborder" valign="top" width="74.76%" headers="mcps1.2.3.1.2 "><p id="en-us_topic_0249784577_p537517310381"><a name="en-us_topic_0249784577_p537517310381"></a><a name="en-us_topic_0249784577_p537517310381"></a>It is recommended that the number of remaining inodes be greater than 1.5 billion.</p>
</td>
</tr>
<tr id="en-us_topic_0249784577_en-us_topic_0241802565_en-us_topic_0085434629_en-us_topic_0059782022_r1f5aefa904854b5bbf1f82931d9fc9b5"><td class="cellrowborder" valign="top" width="25.240000000000002%" headers="mcps1.2.3.1.1 "><p id="en-us_topic_0249784577_en-us_topic_0085434629_en-us_topic_0059782022_a9b2d673c90f94bd49a7d4bfdb277e3fb"><a name="en-us_topic_0249784577_en-us_topic_0085434629_en-us_topic_0059782022_a9b2d673c90f94bd49a7d4bfdb277e3fb"></a><a name="en-us_topic_0249784577_en-us_topic_0085434629_en-us_topic_0059782022_a9b2d673c90f94bd49a7d4bfdb277e3fb"></a>Tools</p>
</td>
<td class="cellrowborder" valign="top" width="74.76%" headers="mcps1.2.3.1.2 "><p id="en-us_topic_0249784577_en-us_topic_0085434629_en-us_topic_0059782022_p61224722154556"><a name="en-us_topic_0249784577_en-us_topic_0085434629_en-us_topic_0059782022_p61224722154556"></a><a name="en-us_topic_0249784577_en-us_topic_0085434629_en-us_topic_0059782022_p61224722154556"></a>Huawei JDK 1.8.0 and bzip2</p>
</td>
</tr>
<tr id="en-us_topic_0249784577_row109998493614"><td class="cellrowborder" valign="top" width="25.240000000000002%" headers="mcps1.2.3.1.1 "><p id="en-us_topic_0249784577_p075762219324"><a name="en-us_topic_0249784577_p075762219324"></a><a name="en-us_topic_0249784577_p075762219324"></a>Python</p>
</td>
<td class="cellrowborder" valign="top" width="74.76%" headers="mcps1.2.3.1.2 "><a name="en-us_topic_0249784577_ul1537120034117"></a><a name="en-us_topic_0249784577_ul1537120034117"></a><ul id="en-us_topic_0249784577_ul1537120034117"><li>openEuler: Python 3.7.X is supported.</li><li>CentOS: Python 3.6.X is supported.</li></ul>
</td>
</tr>
</tbody>
</table>

## Software Dependency Requirements<a name="en-us_topic_0249784577_section5459315183816"></a>

[Table 3](#en-us_topic_0249784577_table11459151513383)  lists the software dependency requirements for the openGauss.

You are advised to use the default installation packages of the following dependent software in the listed OS installation CD-ROMs or sources. If the following software does not exist, refer to the recommended versions of the software.

**Table  3**  Software dependency requirements

<a name="en-us_topic_0249784577_table11459151513383"></a>
<table><thead align="left"><tr id="en-us_topic_0249784577_en-us_topic_0241496992_row317811661910"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="en-us_topic_0249784577_en-us_topic_0241496992_p14178216101910"><a name="en-us_topic_0249784577_en-us_topic_0241496992_p14178216101910"></a><a name="en-us_topic_0249784577_en-us_topic_0241496992_p14178216101910"></a>Software</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="en-us_topic_0249784577_en-us_topic_0241496992_p1117815167195"><a name="en-us_topic_0249784577_en-us_topic_0241496992_p1117815167195"></a><a name="en-us_topic_0249784577_en-us_topic_0241496992_p1117815167195"></a>Recommended Version</p>
</th>
</tr>
</thead>
<tbody><tr id="en-us_topic_0249784577_en-us_topic_0241496992_row17179141619198"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="en-us_topic_0249784577_en-us_topic_0241496992_p111791816141910"><a name="en-us_topic_0249784577_en-us_topic_0241496992_p111791816141910"></a><a name="en-us_topic_0249784577_en-us_topic_0241496992_p111791816141910"></a>libaio-devel</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="en-us_topic_0249784577_en-us_topic_0241496992_p101791116151915"><a name="en-us_topic_0249784577_en-us_topic_0241496992_p101791116151915"></a><a name="en-us_topic_0249784577_en-us_topic_0241496992_p101791116151915"></a>0.3.109-13</p>
</td>
</tr>
<tr id="en-us_topic_0249784577_en-us_topic_0241496992_row1617981631914"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="en-us_topic_0249784577_en-us_topic_0241496992_p171794161195"><a name="en-us_topic_0249784577_en-us_topic_0241496992_p171794161195"></a><a name="en-us_topic_0249784577_en-us_topic_0241496992_p171794161195"></a>flex</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="en-us_topic_0249784577_en-us_topic_0241496992_p1317921651912"><a name="en-us_topic_0249784577_en-us_topic_0241496992_p1317921651912"></a><a name="en-us_topic_0249784577_en-us_topic_0241496992_p1317921651912"></a>2.5.31 or later</p>
</td>
</tr>
<tr id="en-us_topic_0249784577_en-us_topic_0241496992_row1017911165191"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="en-us_topic_0249784577_en-us_topic_0241496992_p1617931661912"><a name="en-us_topic_0249784577_en-us_topic_0241496992_p1617931661912"></a><a name="en-us_topic_0249784577_en-us_topic_0241496992_p1617931661912"></a>bison</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="en-us_topic_0249784577_en-us_topic_0241496992_p917919167196"><a name="en-us_topic_0249784577_en-us_topic_0241496992_p917919167196"></a><a name="en-us_topic_0249784577_en-us_topic_0241496992_p917919167196"></a>2.7-4</p>
</td>
</tr>
<tr id="en-us_topic_0249784577_en-us_topic_0241496992_row8179181610191"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="en-us_topic_0249784577_en-us_topic_0241496992_p101791416191912"><a name="en-us_topic_0249784577_en-us_topic_0241496992_p101791416191912"></a><a name="en-us_topic_0249784577_en-us_topic_0241496992_p101791416191912"></a>ncurses-devel</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="en-us_topic_0249784577_en-us_topic_0241496992_p0179161651913"><a name="en-us_topic_0249784577_en-us_topic_0241496992_p0179161651913"></a><a name="en-us_topic_0249784577_en-us_topic_0241496992_p0179161651913"></a>5.9-13.20130511</p>
</td>
</tr>
<tr id="en-us_topic_0249784577_en-us_topic_0241496992_row10179416191912"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="en-us_topic_0249784577_en-us_topic_0241496992_p1117941618198"><a name="en-us_topic_0249784577_en-us_topic_0241496992_p1117941618198"></a><a name="en-us_topic_0249784577_en-us_topic_0241496992_p1117941618198"></a>glibc.devel</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="en-us_topic_0249784577_en-us_topic_0241496992_p5179191616190"><a name="en-us_topic_0249784577_en-us_topic_0241496992_p5179191616190"></a><a name="en-us_topic_0249784577_en-us_topic_0241496992_p5179191616190"></a>2.17-111</p>
</td>
</tr>
<tr id="en-us_topic_0249784577_en-us_topic_0241496992_row317914169193"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="en-us_topic_0249784577_en-us_topic_0241496992_p201791916201910"><a name="en-us_topic_0249784577_en-us_topic_0241496992_p201791916201910"></a><a name="en-us_topic_0249784577_en-us_topic_0241496992_p201791916201910"></a>patch</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="en-us_topic_0249784577_en-us_topic_0241496992_p1018051610198"><a name="en-us_topic_0249784577_en-us_topic_0241496992_p1018051610198"></a><a name="en-us_topic_0249784577_en-us_topic_0241496992_p1018051610198"></a>2.7.1-10</p>
</td>
</tr>
<tr id="en-us_topic_0249784577_en-us_topic_0241496992_row136701325154914"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="en-us_topic_0249784577_en-us_topic_0241496992_p76711825134912"><a name="en-us_topic_0249784577_en-us_topic_0241496992_p76711825134912"></a><a name="en-us_topic_0249784577_en-us_topic_0241496992_p76711825134912"></a>lsb_release</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="en-us_topic_0249784577_en-us_topic_0241496992_p1567262515496"><a name="en-us_topic_0249784577_en-us_topic_0241496992_p1567262515496"></a><a name="en-us_topic_0249784577_en-us_topic_0241496992_p1567262515496"></a>4.1</p>
</td>
</tr>
</tbody>
</table>

