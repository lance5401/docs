# Configuring OS Parameters<a name="EN-US_TOPIC_0249784554"></a>

openGauss requires that the OS parameters on every host be set to specified values to ensure system running performance.

Some of these parameters are set during the openGauss installation environment preparation phase, and these parameters directly affect the running status of the openGauss. You need to manually adjust these parameters only when necessary. You can use the following methods:

1.  Log in to a server as user  **root**.
2.  Modify the  **/etc/sysctl.conf**  file.

    For details about how to modify parameters, see  [OS Parameters](#en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_section3705271819540).

3.  Run the following command to make the modifications take effect:

    ```
    sysctl -p
    ```


## OS Parameters<a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_section3705271819540"></a>

**Table  1**  OS parameters

<a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_table174711620568"></a>
<table><thead align="left"><tr id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_row134711465560"><th class="cellrowborder" valign="top" width="24.08240824082408%" id="mcps1.2.4.1.1"><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p258931915710"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p258931915710"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p258931915710"></a>Parameter</p>
</th>
<th class="cellrowborder" valign="top" width="52.04520452045204%" id="mcps1.2.4.1.2"><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1358931917574"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1358931917574"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1358931917574"></a>Description</p>
</th>
<th class="cellrowborder" valign="top" width="23.87238723872387%" id="mcps1.2.4.1.3"><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p6590119125718"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p6590119125718"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p6590119125718"></a>Recommended Value</p>
</th>
</tr>
</thead>
<tbody><tr id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_row647214625611"><td class="cellrowborder" valign="top" width="24.08240824082408%" headers="mcps1.2.4.1.1 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1125722695711"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1125722695711"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1125722695711"></a>net.ipv4.tcp_max_tw_buckets</p>
</td>
<td class="cellrowborder" valign="top" width="52.04520452045204%" headers="mcps1.2.4.1.2 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p182571426125710"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p182571426125710"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p182571426125710"></a>Specifies the maximum number of TCP/IP connections concurrently remaining in the <strong id="b20454121619520"><a name="b20454121619520"></a><a name="b20454121619520"></a>TIME_WAIT</strong> state. If the number of TCP/IP connections concurrently remaining in the <strong id="b565720239528"><a name="b565720239528"></a><a name="b565720239528"></a>TIME_WAIT</strong> state exceeds the value of this parameter, the TCP/IP connections in the <strong id="b186651623135210"><a name="b186651623135210"></a><a name="b186651623135210"></a>TIME_WAIT</strong> state will be released immediately, and alarm information will be printed.</p>
</td>
<td class="cellrowborder" valign="top" width="23.87238723872387%" headers="mcps1.2.4.1.3 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p42571268571"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p42571268571"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p42571268571"></a>10000</p>
</td>
</tr>
<tr id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_row4472364569"><td class="cellrowborder" valign="top" width="24.08240824082408%" headers="mcps1.2.4.1.1 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p59261713115813"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p59261713115813"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p59261713115813"></a>net.ipv4.tcp_tw_reuse</p>
</td>
<td class="cellrowborder" valign="top" width="52.04520452045204%" headers="mcps1.2.4.1.2 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p169261713135818"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p169261713135818"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p169261713135818"></a>Reuses sockets whose status is <strong id="b9668733125216"><a name="b9668733125216"></a><a name="b9668733125216"></a>TIME-WAIT</strong> for new TCP connections.</p>
<a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_ul99261213185819"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_ul99261213185819"></a><ul id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_ul99261213185819"><li><strong id="b1922443965212"><a name="b1922443965212"></a><a name="b1922443965212"></a>0</strong>: This function is disabled.</li><li><strong id="b13542174055211"><a name="b13542174055211"></a><a name="b13542174055211"></a>1</strong>: This function is enabled.</li></ul>
</td>
<td class="cellrowborder" valign="top" width="23.87238723872387%" headers="mcps1.2.4.1.3 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1692713134587"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1692713134587"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1692713134587"></a>1</p>
</td>
</tr>
<tr id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_row94736616569"><td class="cellrowborder" valign="top" width="24.08240824082408%" headers="mcps1.2.4.1.1 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p292717139588"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p292717139588"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p292717139588"></a>net.ipv4.tcp_tw_recycle</p>
</td>
<td class="cellrowborder" valign="top" width="52.04520452045204%" headers="mcps1.2.4.1.2 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1992811310580"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1992811310580"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1992811310580"></a>Rapidly reclaims sockets whose status is <strong id="b12266104255218"><a name="b12266104255218"></a><a name="b12266104255218"></a>TIME-WAIT</strong> in TCP connections.</p>
<a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_ul17928101395817"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_ul17928101395817"></a><ul id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_ul17928101395817"><li><strong id="b1416194710527"><a name="b1416194710527"></a><a name="b1416194710527"></a>0</strong>: This function is disabled.</li><li><strong id="b047948165213"><a name="b047948165213"></a><a name="b047948165213"></a>1</strong>: This function is enabled.</li></ul>
</td>
<td class="cellrowborder" valign="top" width="23.87238723872387%" headers="mcps1.2.4.1.3 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1928613155814"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1928613155814"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1928613155814"></a>1</p>
</td>
</tr>
<tr id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_row4676171295719"><td class="cellrowborder" valign="top" width="24.08240824082408%" headers="mcps1.2.4.1.1 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p11929181313586"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p11929181313586"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p11929181313586"></a>net.ipv4.tcp_keepalive_time</p>
</td>
<td class="cellrowborder" valign="top" width="52.04520452045204%" headers="mcps1.2.4.1.2 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p199291139588"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p199291139588"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p199291139588"></a>Specifies how often keep-alive messages are sent through TCP connections when Keep-Alive is enabled.</p>
</td>
<td class="cellrowborder" valign="top" width="23.87238723872387%" headers="mcps1.2.4.1.3 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p892911355817"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p892911355817"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p892911355817"></a>30</p>
</td>
</tr>
<tr id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_row17677191218575"><td class="cellrowborder" valign="top" width="24.08240824082408%" headers="mcps1.2.4.1.1 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1492941395814"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1492941395814"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1492941395814"></a>net.ipv4.tcp_keepalive_probes</p>
</td>
<td class="cellrowborder" valign="top" width="52.04520452045204%" headers="mcps1.2.4.1.2 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p49291138584"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p49291138584"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p49291138584"></a>Specifies the number of keep-alive detection packets sent through a TCP connection before the connection is regarded invalid. The product of the parameter value multiplied by the value of the <strong id="b860162215539"><a name="b860162215539"></a><a name="b860162215539"></a>tcp_keepalive_intvl</strong> parameter determines the response timeout after a keep-alive message is sent through a connection.</p>
</td>
<td class="cellrowborder" valign="top" width="23.87238723872387%" headers="mcps1.2.4.1.3 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p5930181310585"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p5930181310585"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p5930181310585"></a>9</p>
</td>
</tr>
<tr id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_row1467720124571"><td class="cellrowborder" valign="top" width="24.08240824082408%" headers="mcps1.2.4.1.1 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1593010138588"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1593010138588"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1593010138588"></a>net.ipv4.tcp_keepalive_intvl</p>
</td>
<td class="cellrowborder" valign="top" width="52.04520452045204%" headers="mcps1.2.4.1.2 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p59301313185815"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p59301313185815"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p59301313185815"></a>Specifies how often a detection packet is re-sent when the previous packets are not acknowledged.</p>
</td>
<td class="cellrowborder" valign="top" width="23.87238723872387%" headers="mcps1.2.4.1.3 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p4931151314582"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p4931151314582"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p4931151314582"></a>30</p>
</td>
</tr>
<tr id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_row885193417577"><td class="cellrowborder" valign="top" width="24.08240824082408%" headers="mcps1.2.4.1.1 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p209310131583"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p209310131583"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p209310131583"></a>net.ipv4.tcp_retries1</p>
</td>
<td class="cellrowborder" valign="top" width="52.04520452045204%" headers="mcps1.2.4.1.2 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p6932131313581"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p6932131313581"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p6932131313581"></a>Specifies the maximum TCP reattempts during the connection establishment process.</p>
</td>
<td class="cellrowborder" valign="top" width="23.87238723872387%" headers="mcps1.2.4.1.3 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p793281355810"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p793281355810"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p793281355810"></a>5</p>
</td>
</tr>
<tr id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_row785253455720"><td class="cellrowborder" valign="top" width="24.08240824082408%" headers="mcps1.2.4.1.1 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p17932713145816"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p17932713145816"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p17932713145816"></a>net.ipv4.tcp_syn_retries</p>
</td>
<td class="cellrowborder" valign="top" width="52.04520452045204%" headers="mcps1.2.4.1.2 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p189321613175819"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p189321613175819"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p189321613175819"></a>Specifies the maximum SYN packet reattempts in the TCP.</p>
</td>
<td class="cellrowborder" valign="top" width="23.87238723872387%" headers="mcps1.2.4.1.3 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p693313136582"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p693313136582"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p693313136582"></a>5</p>
</td>
</tr>
<tr id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_row10853153425712"><td class="cellrowborder" valign="top" width="24.08240824082408%" headers="mcps1.2.4.1.1 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1293371305814"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1293371305814"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1293371305814"></a>net.ipv4.tcp_synack_retries</p>
</td>
<td class="cellrowborder" valign="top" width="52.04520452045204%" headers="mcps1.2.4.1.2 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p17933201318587"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p17933201318587"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p17933201318587"></a>Specifies the maximum SYN response packet reattempts in the TCP.</p>
</td>
<td class="cellrowborder" valign="top" width="23.87238723872387%" headers="mcps1.2.4.1.3 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p99331013155811"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p99331013155811"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p99331013155811"></a>5</p>
</td>
</tr>
<tr id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_row16854153425715"><td class="cellrowborder" valign="top" width="24.08240824082408%" headers="mcps1.2.4.1.1 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p20306163975820"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p20306163975820"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p20306163975820"></a>net.sctp.path_max_retrans</p>
</td>
<td class="cellrowborder" valign="top" width="52.04520452045204%" headers="mcps1.2.4.1.2 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1930673905818"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1930673905818"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1930673905818"></a>Specifies the maximum SCTP reattempts.</p>
</td>
<td class="cellrowborder" valign="top" width="23.87238723872387%" headers="mcps1.2.4.1.3 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p13062395586"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p13062395586"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p13062395586"></a>10</p>
</td>
</tr>
<tr id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_row48543346572"><td class="cellrowborder" valign="top" width="24.08240824082408%" headers="mcps1.2.4.1.1 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p18307113975816"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p18307113975816"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p18307113975816"></a>net.sctp.max_init_retransmits</p>
</td>
<td class="cellrowborder" valign="top" width="52.04520452045204%" headers="mcps1.2.4.1.2 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p73071396587"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p73071396587"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p73071396587"></a>Specifies the maximum INIT packet reattempts in the SCTP.</p>
</td>
<td class="cellrowborder" valign="top" width="23.87238723872387%" headers="mcps1.2.4.1.3 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p5307193935812"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p5307193935812"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p5307193935812"></a>10</p>
</td>
</tr>
<tr id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_row15187154135712"><td class="cellrowborder" valign="top" width="24.08240824082408%" headers="mcps1.2.4.1.1 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p183081739155818"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p183081739155818"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p183081739155818"></a>net.sctp.association_max_retrans</p>
</td>
<td class="cellrowborder" valign="top" width="52.04520452045204%" headers="mcps1.2.4.1.2 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p183081397580"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p183081397580"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p183081397580"></a>Specifies the maximum reattempts of a single logical connection in the SCTP.</p>
</td>
<td class="cellrowborder" valign="top" width="23.87238723872387%" headers="mcps1.2.4.1.3 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p93081394588"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p93081394588"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p93081394588"></a>10</p>
</td>
</tr>
<tr id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_row141877415577"><td class="cellrowborder" valign="top" width="24.08240824082408%" headers="mcps1.2.4.1.1 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1530815395588"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1530815395588"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1530815395588"></a>net.sctp.hb_interval</p>
</td>
<td class="cellrowborder" valign="top" width="52.04520452045204%" headers="mcps1.2.4.1.2 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p3309739105813"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p3309739105813"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p3309739105813"></a>Specifies the retransmission interval of heartbeat detection packets in the SCTP.</p>
</td>
<td class="cellrowborder" valign="top" width="23.87238723872387%" headers="mcps1.2.4.1.3 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p33093399584"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p33093399584"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p33093399584"></a>30000</p>
</td>
</tr>
<tr id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_row0188144110571"><td class="cellrowborder" valign="top" width="24.08240824082408%" headers="mcps1.2.4.1.1 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p203091939195813"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p203091939195813"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p203091939195813"></a>net.ipv4.tcp_retries2</p>
</td>
<td class="cellrowborder" valign="top" width="52.04520452045204%" headers="mcps1.2.4.1.2 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1331013399587"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1331013399587"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1331013399587"></a>Specifies the number of times that the kernel re-sends data to a connected remote host. A smaller value leads to earlier detection of an invalid connection to the remote host, and the server can quickly release this connection.</p>
<p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p133103392585"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p133103392585"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p133103392585"></a>If "connection reset by peer" is displayed, increase the value of this parameter to avoid the problem.</p>
</td>
<td class="cellrowborder" valign="top" width="23.87238723872387%" headers="mcps1.2.4.1.3 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p83101739145811"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p83101739145811"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p83101739145811"></a>12</p>
</td>
</tr>
<tr id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_row0188184135716"><td class="cellrowborder" valign="top" width="24.08240824082408%" headers="mcps1.2.4.1.1 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p10310183915815"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p10310183915815"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p10310183915815"></a>vm.overcommit_memory</p>
</td>
<td class="cellrowborder" valign="top" width="52.04520452045204%" headers="mcps1.2.4.1.2 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p12311173912584"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p12311173912584"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p12311173912584"></a>Specifies the kernel check method during memory allocation.</p>
<a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_ul14311183913587"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_ul14311183913587"></a><ul id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_ul14311183913587"><li><strong id="b6953815145419"><a name="b6953815145419"></a><a name="b6953815145419"></a>0</strong>: The system accurately calculates the current available memory.</li><li><strong id="b19366171814545"><a name="b19366171814545"></a><a name="b19366171814545"></a>1</strong>: The system returns a success message without a kernel check.</li><li><strong id="b161722020135420"><a name="b161722020135420"></a><a name="b161722020135420"></a>2</strong>: The system returns a failure message if the memory size you have applied for exceeds the result of the following formula: Total memory size x Value of <strong id="b51735207548"><a name="b51735207548"></a><a name="b51735207548"></a>vm.overcommit_ratio</strong>/100 + Total SWAP size.</li></ul>
<p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p193123394589"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p193123394589"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p193123394589"></a>The default value is <strong id="b1755911284545"><a name="b1755911284545"></a><a name="b1755911284545"></a>2</strong>, which is too conservative. The recommended value is <strong id="b135647281546"><a name="b135647281546"></a><a name="b135647281546"></a>0</strong>. If memory usage is high, set this parameter to <strong id="b35649287549"><a name="b35649287549"></a><a name="b35649287549"></a>1</strong>.</p>
</td>
<td class="cellrowborder" valign="top" width="23.87238723872387%" headers="mcps1.2.4.1.3 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p13313153945816"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p13313153945816"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p13313153945816"></a>0</p>
</td>
</tr>
<tr id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_row518920412574"><td class="cellrowborder" valign="top" width="24.08240824082408%" headers="mcps1.2.4.1.1 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1852316514595"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1852316514595"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1852316514595"></a>net.sctp.sndbuf_policy</p>
</td>
<td class="cellrowborder" valign="top" width="52.04520452045204%" headers="mcps1.2.4.1.2 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p552314515913"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p552314515913"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p552314515913"></a>Specifies the buffer allocation policy on the SCTP sender.</p>
<a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_ul1352319514598"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_ul1352319514598"></a><ul id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_ul1352319514598"><li><strong id="b193096311556"><a name="b193096311556"></a><a name="b193096311556"></a>0</strong>: The buffer is allocated by connection.</li><li><strong id="b2328510135520"><a name="b2328510135520"></a><a name="b2328510135520"></a>1</strong>: The buffer is allocated by association.</li></ul>
</td>
<td class="cellrowborder" valign="top" width="23.87238723872387%" headers="mcps1.2.4.1.3 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1952565185913"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1952565185913"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1952565185913"></a>0</p>
</td>
</tr>
<tr id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_row734759175715"><td class="cellrowborder" valign="top" width="24.08240824082408%" headers="mcps1.2.4.1.1 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1652514545918"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1652514545918"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1652514545918"></a>net.sctp.rcvbuf_policy</p>
</td>
<td class="cellrowborder" valign="top" width="52.04520452045204%" headers="mcps1.2.4.1.2 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p13525115165918"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p13525115165918"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p13525115165918"></a>Specifies the buffer allocation policy on the SCTP receiver.</p>
<a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_ul6525145195911"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_ul6525145195911"></a><ul id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_ul6525145195911"><li><strong id="b1594443155515"><a name="b1594443155515"></a><a name="b1594443155515"></a>0</strong>: The buffer is allocated by connection.</li><li><strong id="b1144612332554"><a name="b1144612332554"></a><a name="b1144612332554"></a>1</strong>: The buffer is allocated by association.</li></ul>
</td>
<td class="cellrowborder" valign="top" width="23.87238723872387%" headers="mcps1.2.4.1.3 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1652614565913"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1652614565913"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1652614565913"></a>0</p>
</td>
</tr>
<tr id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_row334559165716"><td class="cellrowborder" valign="top" width="24.08240824082408%" headers="mcps1.2.4.1.1 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1852712519597"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1852712519597"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1852712519597"></a>net.sctp.sctp_mem</p>
</td>
<td class="cellrowborder" valign="top" width="52.04520452045204%" headers="mcps1.2.4.1.2 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1952719585918"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1952719585918"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1952719585918"></a>Specifies the maximum free memory of the kernel SCTP stack. Three memory size ranges in the unit of page are provided: <strong id="b1011347558"><a name="b1011347558"></a><a name="b1011347558"></a>min</strong>, <strong id="b1518345553"><a name="b1518345553"></a><a name="b1518345553"></a>default</strong>, and <strong id="b191163405518"><a name="b191163405518"></a><a name="b191163405518"></a>max</strong>. If the value is <strong id="b521034115512"><a name="b521034115512"></a><a name="b521034115512"></a>max</strong>, packet loss occurs.</p>
</td>
<td class="cellrowborder" valign="top" width="23.87238723872387%" headers="mcps1.2.4.1.3 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p2052714595917"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p2052714595917"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p2052714595917"></a>94500000 915000000 927000000</p>
</td>
</tr>
<tr id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_row103535911574"><td class="cellrowborder" valign="top" width="24.08240824082408%" headers="mcps1.2.4.1.1 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p8528125155919"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p8528125155919"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p8528125155919"></a>net.sctp.sctp_rmem</p>
</td>
<td class="cellrowborder" valign="top" width="52.04520452045204%" headers="mcps1.2.4.1.2 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p4528953598"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p4528953598"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p4528953598"></a>Specifies the total free memory for receiving data in the kernel SCTP stack. Three memory size ranges in the unit of page are provided: <strong id="b660503785510"><a name="b660503785510"></a><a name="b660503785510"></a>min</strong>, <strong id="b260593717551"><a name="b260593717551"></a><a name="b260593717551"></a>default</strong>, and <strong id="b1260513711551"><a name="b1260513711551"></a><a name="b1260513711551"></a>max</strong>. If the value is <strong id="b1160511376555"><a name="b1160511376555"></a><a name="b1160511376555"></a>max</strong>, packet loss occurs.</p>
</td>
<td class="cellrowborder" valign="top" width="23.87238723872387%" headers="mcps1.2.4.1.3 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p452875125919"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p452875125919"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p452875125919"></a>8192 250000 16777216</p>
</td>
</tr>
<tr id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_row1236175915571"><td class="cellrowborder" valign="top" width="24.08240824082408%" headers="mcps1.2.4.1.1 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p452885125914"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p452885125914"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p452885125914"></a>net.sctp.sctp_wmem</p>
</td>
<td class="cellrowborder" valign="top" width="52.04520452045204%" headers="mcps1.2.4.1.2 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p13529165115911"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p13529165115911"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p13529165115911"></a>Specifies the total free memory for sending data in the kernel SCTP stack. Three memory size ranges in the unit of page are provided: <strong id="b227663805513"><a name="b227663805513"></a><a name="b227663805513"></a>min</strong>, <strong id="b727663815512"><a name="b727663815512"></a><a name="b727663815512"></a>default</strong>, and <strong id="b1227693815510"><a name="b1227693815510"></a><a name="b1227693815510"></a>max</strong>. If the value is <strong id="b9276133813552"><a name="b9276133813552"></a><a name="b9276133813552"></a>max</strong>, packet loss occurs.</p>
</td>
<td class="cellrowborder" valign="top" width="23.87238723872387%" headers="mcps1.2.4.1.3 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p85291751593"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p85291751593"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p85291751593"></a>8192 250000 16777216</p>
</td>
</tr>
<tr id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_row3361592574"><td class="cellrowborder" valign="top" width="24.08240824082408%" headers="mcps1.2.4.1.1 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p19529155145913"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p19529155145913"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p19529155145913"></a>net.ipv4.tcp_rmem</p>
</td>
<td class="cellrowborder" valign="top" width="52.04520452045204%" headers="mcps1.2.4.1.2 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1452915511595"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1452915511595"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1452915511595"></a>Specifies the free memory in the TCP receiver buffer. Three memory size ranges in the unit of page are provided: <strong id="b1088810432553"><a name="b1088810432553"></a><a name="b1088810432553"></a>min</strong>, <strong id="b28932431554"><a name="b28932431554"></a><a name="b28932431554"></a>default</strong>, and <strong id="b17893643175514"><a name="b17893643175514"></a><a name="b17893643175514"></a>max</strong>.</p>
</td>
<td class="cellrowborder" valign="top" width="23.87238723872387%" headers="mcps1.2.4.1.3 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p5529155105915"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p5529155105915"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p5529155105915"></a>8192 250000 16777216</p>
</td>
</tr>
<tr id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_row10378590579"><td class="cellrowborder" valign="top" width="24.08240824082408%" headers="mcps1.2.4.1.1 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p953010511591"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p953010511591"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p953010511591"></a>net.ipv4.tcp_wmem</p>
</td>
<td class="cellrowborder" valign="top" width="52.04520452045204%" headers="mcps1.2.4.1.2 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1153017545918"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1153017545918"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1153017545918"></a>Specifies the free memory in the TCP sender buffer. Three memory size ranges in the unit of page are provided: <strong id="b20324164545512"><a name="b20324164545512"></a><a name="b20324164545512"></a>min</strong>, <strong id="b232416452553"><a name="b232416452553"></a><a name="b232416452553"></a>default</strong>, and <strong id="b8325445155511"><a name="b8325445155511"></a><a name="b8325445155511"></a>max</strong>.</p>
</td>
<td class="cellrowborder" valign="top" width="23.87238723872387%" headers="mcps1.2.4.1.3 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p195301356597"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p195301356597"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p195301356597"></a>8192 250000 16777216</p>
</td>
</tr>
<tr id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_row2387595578"><td class="cellrowborder" valign="top" width="24.08240824082408%" headers="mcps1.2.4.1.1 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p163351922125910"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p163351922125910"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p163351922125910"></a>net.core.wmem_max</p>
</td>
<td class="cellrowborder" valign="top" width="52.04520452045204%" headers="mcps1.2.4.1.2 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p14335132214593"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p14335132214593"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p14335132214593"></a>Specifies the maximum size of the socket sender buffer.</p>
</td>
<td class="cellrowborder" valign="top" width="23.87238723872387%" headers="mcps1.2.4.1.3 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p633582217598"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p633582217598"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p633582217598"></a>21299200</p>
</td>
</tr>
<tr id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_row33995910574"><td class="cellrowborder" valign="top" width="24.08240824082408%" headers="mcps1.2.4.1.1 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p12336132225915"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p12336132225915"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p12336132225915"></a>net.core.rmem_max</p>
</td>
<td class="cellrowborder" valign="top" width="52.04520452045204%" headers="mcps1.2.4.1.2 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p2336172218596"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p2336172218596"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p2336172218596"></a>Specifies the maximum size of the socket receiver buffer.</p>
</td>
<td class="cellrowborder" valign="top" width="23.87238723872387%" headers="mcps1.2.4.1.3 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p163361222205919"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p163361222205919"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p163361222205919"></a>21299200</p>
</td>
</tr>
<tr id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_row1739559195711"><td class="cellrowborder" valign="top" width="24.08240824082408%" headers="mcps1.2.4.1.1 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p8336142211595"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p8336142211595"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p8336142211595"></a>net.core.wmem_default</p>
</td>
<td class="cellrowborder" valign="top" width="52.04520452045204%" headers="mcps1.2.4.1.2 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p6337182218592"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p6337182218592"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p6337182218592"></a>Specifies the default size of the socket sender buffer.</p>
</td>
<td class="cellrowborder" valign="top" width="23.87238723872387%" headers="mcps1.2.4.1.3 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p193371222105920"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p193371222105920"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p193371222105920"></a>21299200</p>
</td>
</tr>
<tr id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_row14011595570"><td class="cellrowborder" valign="top" width="24.08240824082408%" headers="mcps1.2.4.1.1 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p333715223593"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p333715223593"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p333715223593"></a>net.core.rmem_default</p>
</td>
<td class="cellrowborder" valign="top" width="52.04520452045204%" headers="mcps1.2.4.1.2 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p163371922175915"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p163371922175915"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p163371922175915"></a>Specifies the default size of the socket receiver buffer.</p>
</td>
<td class="cellrowborder" valign="top" width="23.87238723872387%" headers="mcps1.2.4.1.3 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p13338122275917"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p13338122275917"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p13338122275917"></a>21299200</p>
</td>
</tr>
<tr id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_row1041959195714"><td class="cellrowborder" valign="top" width="24.08240824082408%" headers="mcps1.2.4.1.1 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1833892275911"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1833892275911"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1833892275911"></a>net.ipv4.ip_local_port_range</p>
</td>
<td class="cellrowborder" valign="top" width="52.04520452045204%" headers="mcps1.2.4.1.2 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p0338112235914"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p0338112235914"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p0338112235914"></a>Specifies the range of temporary ports that can be used by a physical server.</p>
</td>
<td class="cellrowborder" valign="top" width="23.87238723872387%" headers="mcps1.2.4.1.3 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p14339142235915"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p14339142235915"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p14339142235915"></a>26000-65535</p>
</td>
</tr>
<tr id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_row0425596573"><td class="cellrowborder" valign="top" width="24.08240824082408%" headers="mcps1.2.4.1.1 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1933992225914"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1933992225914"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1933992225914"></a>kernel.sem</p>
</td>
<td class="cellrowborder" valign="top" width="52.04520452045204%" headers="mcps1.2.4.1.2 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p933942215595"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p933942215595"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p933942215595"></a>Specifies the kernel semaphore.</p>
</td>
<td class="cellrowborder" valign="top" width="23.87238723872387%" headers="mcps1.2.4.1.3 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p12340132213597"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p12340132213597"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p12340132213597"></a>250 6400000 1000 25600</p>
</td>
</tr>
<tr id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_row44385915579"><td class="cellrowborder" valign="top" width="24.08240824082408%" headers="mcps1.2.4.1.1 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p934010229591"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p934010229591"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p934010229591"></a>vm.min_free_kbytes</p>
</td>
<td class="cellrowborder" valign="top" width="52.04520452045204%" headers="mcps1.2.4.1.2 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p183405228591"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p183405228591"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p183405228591"></a>Specifies the minimum free physical memory reserved for unexpected page breaks.</p>
</td>
<td class="cellrowborder" valign="top" width="23.87238723872387%" headers="mcps1.2.4.1.3 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p17341142215591"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p17341142215591"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p17341142215591"></a>5% of the total system memory</p>
</td>
</tr>
<tr id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_row9431359105719"><td class="cellrowborder" valign="top" width="24.08240824082408%" headers="mcps1.2.4.1.1 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p11341322145910"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p11341322145910"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p11341322145910"></a>net.core.somaxconn</p>
</td>
<td class="cellrowborder" valign="top" width="52.04520452045204%" headers="mcps1.2.4.1.2 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1234282213599"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1234282213599"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1234282213599"></a>Specifies the maximum length of the listening queue of each port. This is a global parameter.</p>
</td>
<td class="cellrowborder" valign="top" width="23.87238723872387%" headers="mcps1.2.4.1.3 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p534272295916"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p534272295916"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p534272295916"></a>65535</p>
</td>
</tr>
<tr id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_row11442059175716"><td class="cellrowborder" valign="top" width="24.08240824082408%" headers="mcps1.2.4.1.1 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p163421022125917"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p163421022125917"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p163421022125917"></a>net.ipv4.tcp_syncookies</p>
</td>
<td class="cellrowborder" valign="top" width="52.04520452045204%" headers="mcps1.2.4.1.2 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1534362218593"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1534362218593"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1534362218593"></a>Specifies whether to enable SYN cookies to guard the OS against SYN attacks when the SYN waiting queue overflows.</p>
<a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_ul534318226591"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_ul534318226591"></a><ul id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_ul534318226591"><li><strong id="b1996945416554"><a name="b1996945416554"></a><a name="b1996945416554"></a>0</strong>: The SYN cookies are disabled.</li><li><strong id="b1514455155518"><a name="b1514455155518"></a><a name="b1514455155518"></a>1</strong>: The SYN cookies are enabled.</li></ul>
</td>
<td class="cellrowborder" valign="top" width="23.87238723872387%" headers="mcps1.2.4.1.3 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p133441022135919"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p133441022135919"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p133441022135919"></a>1</p>
</td>
</tr>
<tr id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_row8189114185719"><td class="cellrowborder" valign="top" width="24.08240824082408%" headers="mcps1.2.4.1.1 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1034512214592"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1034512214592"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1034512214592"></a>net.sctp.addip_enable</p>
</td>
<td class="cellrowborder" valign="top" width="52.04520452045204%" headers="mcps1.2.4.1.2 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1434552213599"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1434552213599"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1434552213599"></a>Specifies whether dynamic address reset of the SCTP is enabled.</p>
<a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_ul15345142220596"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_ul15345142220596"></a><ul id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_ul15345142220596"><li><strong id="b16810356175515"><a name="b16810356175515"></a><a name="b16810356175515"></a>0</strong>: This function is disabled.</li><li><strong id="b1543193717"><a name="b1543193717"></a><a name="b1543193717"></a>1</strong>: This function is enabled.</li></ul>
</td>
<td class="cellrowborder" valign="top" width="23.87238723872387%" headers="mcps1.2.4.1.3 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p123461722165910"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p123461722165910"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p123461722165910"></a>0</p>
</td>
</tr>
<tr id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_row119054135715"><td class="cellrowborder" valign="top" width="24.08240824082408%" headers="mcps1.2.4.1.1 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1671381607"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1671381607"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1671381607"></a>net.core.netdev_max_backlog</p>
</td>
<td class="cellrowborder" valign="top" width="52.04520452045204%" headers="mcps1.2.4.1.2 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1975811012"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1975811012"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1975811012"></a>Specifies the maximum number of data packets that can be sent to the queue when the rate at which the network device receives data packets is higher than that at which the kernel processes the data packets.</p>
</td>
<td class="cellrowborder" valign="top" width="23.87238723872387%" headers="mcps1.2.4.1.3 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1287819014"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1287819014"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1287819014"></a>65535</p>
</td>
</tr>
<tr id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_row1319012411575"><td class="cellrowborder" valign="top" width="24.08240824082408%" headers="mcps1.2.4.1.1 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p19813814012"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p19813814012"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p19813814012"></a>net.ipv4.tcp_max_syn_backlog</p>
</td>
<td class="cellrowborder" valign="top" width="52.04520452045204%" headers="mcps1.2.4.1.2 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p13818816015"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p13818816015"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p13818816015"></a>Specifies the maximum number of unacknowledged connection requests to be recorded.</p>
</td>
<td class="cellrowborder" valign="top" width="23.87238723872387%" headers="mcps1.2.4.1.3 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1791986010"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1791986010"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1791986010"></a>65535</p>
</td>
</tr>
<tr id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_row111911441145720"><td class="cellrowborder" valign="top" width="24.08240824082408%" headers="mcps1.2.4.1.1 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p20914818010"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p20914818010"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p20914818010"></a>net.ipv4.tcp_fin_timeout</p>
</td>
<td class="cellrowborder" valign="top" width="52.04520452045204%" headers="mcps1.2.4.1.2 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p7978801"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p7978801"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p7978801"></a>Specifies the default timeout duration.</p>
</td>
<td class="cellrowborder" valign="top" width="23.87238723872387%" headers="mcps1.2.4.1.3 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p17101281003"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p17101281003"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p17101281003"></a>60</p>
</td>
</tr>
<tr id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_row171915417579"><td class="cellrowborder" valign="top" width="24.08240824082408%" headers="mcps1.2.4.1.1 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p61016819012"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p61016819012"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p61016819012"></a>kernel.shmall</p>
</td>
<td class="cellrowborder" valign="top" width="52.04520452045204%" headers="mcps1.2.4.1.2 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1810481505"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1810481505"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1810481505"></a>Specifies the total shared free memory of the kernel.</p>
</td>
<td class="cellrowborder" valign="top" width="23.87238723872387%" headers="mcps1.2.4.1.3 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p8101081004"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p8101081004"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p8101081004"></a>1152921504606846720</p>
</td>
</tr>
<tr id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_row1093874517594"><td class="cellrowborder" valign="top" width="24.08240824082408%" headers="mcps1.2.4.1.1 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p4118812012"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p4118812012"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p4118812012"></a>kernel.shmmax</p>
</td>
<td class="cellrowborder" valign="top" width="52.04520452045204%" headers="mcps1.2.4.1.2 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p131117813014"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p131117813014"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p131117813014"></a>Specifies the maximum value of a shared memory segment.</p>
</td>
<td class="cellrowborder" valign="top" width="23.87238723872387%" headers="mcps1.2.4.1.3 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p181188803"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p181188803"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p181188803"></a>18446744073709551615</p>
</td>
</tr>
<tr id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_row1493934585918"><td class="cellrowborder" valign="top" width="24.08240824082408%" headers="mcps1.2.4.1.1 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p412986019"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p412986019"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p412986019"></a>net.ipv4.tcp_sack</p>
</td>
<td class="cellrowborder" valign="top" width="52.04520452045204%" headers="mcps1.2.4.1.2 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p112881904"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p112881904"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p112881904"></a>Specifies whether selective acknowledgment is enabled. The selective acknowledgment on out-of-order packets can increase system performance. Restricting users to sending only lost packets (for wide area networks) should be enabled, but this will increase CPU usage.</p>
<a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_ul112208308"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_ul112208308"></a><ul id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_ul112208308"><li><strong id="b2102274812"><a name="b2102274812"></a><a name="b2102274812"></a>0</strong>: This function is disabled.</li><li><strong>1</strong>: This function is enabled.</li></ul>
</td>
<td class="cellrowborder" valign="top" width="23.87238723872387%" headers="mcps1.2.4.1.3 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p17131181208"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p17131181208"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p17131181208"></a>1</p>
</td>
</tr>
<tr id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_row199407451592"><td class="cellrowborder" valign="top" width="24.08240824082408%" headers="mcps1.2.4.1.1 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p111418818011"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p111418818011"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p111418818011"></a>net.ipv4.tcp_timestamps</p>
</td>
<td class="cellrowborder" valign="top" width="52.04520452045204%" headers="mcps1.2.4.1.2 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p10141681903"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p10141681903"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p10141681903"></a>Specifies whether the TCP timestamp (12 bytes are added in the TCP packet header) enables a more accurate RTT calculation than the retransmission timeout (for details, see RFC 1323) for better performance.</p>
<a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_ul814881508"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_ul814881508"></a><ul id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_ul814881508"><li><strong id="b589362648"><a name="b589362648"></a><a name="b589362648"></a>0</strong>: This function is disabled.</li><li><strong>1</strong>: This function is enabled.</li></ul>
</td>
<td class="cellrowborder" valign="top" width="23.87238723872387%" headers="mcps1.2.4.1.3 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p18151381901"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p18151381901"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p18151381901"></a>1</p>
</td>
</tr>
<tr id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_row3940154515911"><td class="cellrowborder" valign="top" width="24.08240824082408%" headers="mcps1.2.4.1.1 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p02308185016"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p02308185016"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p02308185016"></a>vm.extfrag_threshold</p>
</td>
<td class="cellrowborder" valign="top" width="52.04520452045204%" headers="mcps1.2.4.1.2 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p62301518909"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p62301518909"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p62301518909"></a>When system memory is insufficient, Linux will score the current system memory fragments. If the score is higher than the value of <strong>vm.extfrag_threshold</strong>, <strong>kswapd</strong> triggers memory compaction. When the value of this parameter is close to <strong>1000</strong>, the system tends to swap out old pages when processing memory fragments to meet the application requirements. When the value of this parameter is close to <strong>0</strong>, the system tends to do memory compaction when processing memory fragments.</p>
</td>
<td class="cellrowborder" valign="top" width="23.87238723872387%" headers="mcps1.2.4.1.3 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p923111816015"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p923111816015"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p923111816015"></a>500</p>
</td>
</tr>
<tr id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_row14114125155912"><td class="cellrowborder" valign="top" width="24.08240824082408%" headers="mcps1.2.4.1.1 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p8231218904"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p8231218904"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p8231218904"></a>vm.overcommit_ratio</p>
</td>
<td class="cellrowborder" valign="top" width="52.04520452045204%" headers="mcps1.2.4.1.2 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1823117183015"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1823117183015"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p1823117183015"></a>When the system uses the algorithms where memory usage never exceeds the thresholds, the total memory address space of the system cannot exceed the value of <strong>swap+RAM</strong> multiplied by the percentage specified by this parameter. When the value of <strong>vm.overcommit_memory</strong> is set to <strong>2</strong>, this parameter takes effect.</p>
</td>
<td class="cellrowborder" valign="top" width="23.87238723872387%" headers="mcps1.2.4.1.3 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p12232121819017"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p12232121819017"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p12232121819017"></a>90</p>
</td>
</tr>
<tr id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_row711514515597"><td class="cellrowborder" valign="top" width="24.08240824082408%" headers="mcps1.2.4.1.1 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p523211182017"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p523211182017"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p523211182017"></a>/sys/module/sctp/parameters/no_checksums</p>
</td>
<td class="cellrowborder" valign="top" width="52.04520452045204%" headers="mcps1.2.4.1.2 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p122324181200"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p122324181200"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p122324181200"></a>Specifies whether <strong>checksum</strong> is disabled in SCTP.</p>
</td>
<td class="cellrowborder" valign="top" width="23.87238723872387%" headers="mcps1.2.4.1.3 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p172331418805"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p172331418805"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p172331418805"></a>0</p>
</td>
</tr>
<tr id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_row151152051125910"><td class="cellrowborder" valign="top" width="24.08240824082408%" headers="mcps1.2.4.1.1 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p2233161813015"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p2233161813015"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p2233161813015"></a>MTU</p>
</td>
<td class="cellrowborder" valign="top" width="52.04520452045204%" headers="mcps1.2.4.1.2 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p32330181404"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p32330181404"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p32330181404"></a>Specifies the maximum transmission unit (MTU) for a node NIC. The default value is <strong>1500</strong> in the OS. You can set it to <strong>8192</strong> to improve the performance of sending and receiving data using SCTP.</p>
</td>
<td class="cellrowborder" valign="top" width="23.87238723872387%" headers="mcps1.2.4.1.3 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p223412181010"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p223412181010"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0085031791_p223412181010"></a>8192</p>
</td>
</tr>
</tbody>
</table>

## File System Parameters<a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_section4118580316369"></a>

-   soft nofile

    Indicates the soft limit. The number of file handles used by a user can exceed this parameter value. However, an alarm will be reported.

    Recommended value:  **1000000**

-   hard nofile

    Indicates the hard limit. The number of file handles used by a user cannot exceed this parameter value.

    Recommended value:  **1000000**

-   stack size

    Indicates the thread stack size.

    Recommended value:  **3072**


## Setting the transparent\_hugepage Service<a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_section38366550113020"></a>

By default, openGauss disables the transparent\_hugepage service and this setting is written into the OS startup file.

## Setting File Handles<a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_section49556455195442"></a>

To manually set the number of file handles, run the following commands to modify the involved parameters as user  **root**:

```
echo "* soft nofile 1000000" >>/etc/security/limits.conf
echo "* hard nofile 1000000" >>/etc/security/limits.conf
```

After the modification is complete, restart the OS to make the setting take effect.

**Table  2**  Parameters for setting the number of file handles

<a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_table66928349154930"></a>
<table><thead align="left"><tr id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_row32458049154930"><th class="cellrowborder" valign="top" width="17.47%" id="mcps1.2.5.1.1"><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p29726478135851"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p29726478135851"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p29726478135851"></a>Parameter</p>
</th>
<th class="cellrowborder" valign="top" width="52.07000000000001%" id="mcps1.2.5.1.2"><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p6791871135943"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p6791871135943"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p6791871135943"></a>Description</p>
</th>
<th class="cellrowborder" valign="top" width="21.060000000000002%" id="mcps1.2.5.1.3"><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p17069230135851"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p17069230135851"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p17069230135851"></a>Automatically Set by Scripts During Pre-Installation</p>
</th>
<th class="cellrowborder" valign="top" width="9.4%" id="mcps1.2.5.1.4"><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p45338003135924"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p45338003135924"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p45338003135924"></a>Recommended Value</p>
</th>
</tr>
</thead>
<tbody><tr id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_row36414898154930"><td class="cellrowborder" valign="top" width="17.47%" headers="mcps1.2.5.1.1 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p53634223135851"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p53634223135851"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p53634223135851"></a>* soft nofile</p>
</td>
<td class="cellrowborder" valign="top" width="52.07000000000001%" headers="mcps1.2.5.1.2 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p1184561135943"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p1184561135943"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p1184561135943"></a>Specifies the soft limit on the number of file handles. For example, if this parameter is set to <span class="parmvalue"><b>1000000</b></span>, any user can open a maximum of 1,000,000 files regardless of how many shells are enabled.</p>
</td>
<td class="cellrowborder" valign="top" width="21.060000000000002%" headers="mcps1.2.5.1.3 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p42366546135851"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p42366546135851"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p42366546135851"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="9.4%" headers="mcps1.2.5.1.4 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p36154703135924"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p36154703135924"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p36154703135924"></a>1000000</p>
</td>
</tr>
<tr id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_row3006053154930"><td class="cellrowborder" valign="top" width="17.47%" headers="mcps1.2.5.1.1 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p15135199135851"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p15135199135851"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p15135199135851"></a>* hard nofile</p>
</td>
<td class="cellrowborder" valign="top" width="52.07000000000001%" headers="mcps1.2.5.1.2 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p58238613135943"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p58238613135943"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p58238613135943"></a>Specifies the hard limit. The soft limit must be less than or equal to the hard limit.</p>
</td>
<td class="cellrowborder" valign="top" width="21.060000000000002%" headers="mcps1.2.5.1.3 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p48031615135851"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p48031615135851"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p48031615135851"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="9.4%" headers="mcps1.2.5.1.4 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p50103914135924"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p50103914135924"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p50103914135924"></a>1000000</p>
</td>
</tr>
</tbody>
</table>

## Setting the Maximum Number of Allowed Processes<a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_section65253147151525"></a>

To manually set the maximum number of allowed processes, run the following command to open the configuration file:

```
vim /etc/security/limits.d/90-nproc.conf
```

Modify the  **\* soft nproc**  parameter in the file.

After the modification is complete, restart the OS to make the setting take effect.

**Table  3**  Setting the maximum number of allowed processes

<a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_table51875363151525"></a>
<table><thead align="left"><tr id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_row23677630151525"><th class="cellrowborder" valign="top" width="17.47%" id="mcps1.2.5.1.1"><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p38839882151525"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p38839882151525"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p38839882151525"></a>Parameter</p>
</th>
<th class="cellrowborder" valign="top" width="52.07000000000001%" id="mcps1.2.5.1.2"><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p59022734151525"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p59022734151525"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p59022734151525"></a>Description</p>
</th>
<th class="cellrowborder" valign="top" width="21.060000000000002%" id="mcps1.2.5.1.3"><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p16112179151525"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p16112179151525"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p16112179151525"></a>Automatically Set by Scripts During Pre-Installation</p>
</th>
<th class="cellrowborder" valign="top" width="9.4%" id="mcps1.2.5.1.4"><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p30018145151525"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p30018145151525"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p30018145151525"></a>Recommended Value</p>
</th>
</tr>
</thead>
<tbody><tr id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_row15550655151525"><td class="cellrowborder" valign="top" width="17.47%" headers="mcps1.2.5.1.1 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p51643509151525"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p51643509151525"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p51643509151525"></a>* soft nproc</p>
</td>
<td class="cellrowborder" valign="top" width="52.07000000000001%" headers="mcps1.2.5.1.2 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p22374700151525"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p22374700151525"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p22374700151525"></a>Specifies the maximum number of processes allowed per user.</p>
</td>
<td class="cellrowborder" valign="top" width="21.060000000000002%" headers="mcps1.2.5.1.3 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p411403151525"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p411403151525"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p411403151525"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="9.4%" headers="mcps1.2.5.1.4 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p33323707151525"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p33323707151525"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p33323707151525"></a>60000</p>
</td>
</tr>
</tbody>
</table>

## Setting NIC Parameters<a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_section6007556195457"></a>

**Table  4**  Setting NIC parameters

<a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_table6110995517616"></a>
<table><thead align="left"><tr id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_row1264128417616"><th class="cellrowborder" valign="top" width="14.511451145114512%" id="mcps1.2.5.1.1"><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p1731111217616"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p1731111217616"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p1731111217616"></a>Parameter</p>
</th>
<th class="cellrowborder" valign="top" width="32.08320832083208%" id="mcps1.2.5.1.2"><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p6002283217616"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p6002283217616"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p6002283217616"></a>Description</p>
</th>
<th class="cellrowborder" valign="top" width="39.663966396639665%" id="mcps1.2.5.1.3"><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p3001123717616"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p3001123717616"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p3001123717616"></a>Automatically Set by Scripts During Pre-Installation</p>
</th>
<th class="cellrowborder" valign="top" width="13.74137413741374%" id="mcps1.2.5.1.4"><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p1499111817616"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p1499111817616"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p1499111817616"></a>Recommended Value</p>
</th>
</tr>
</thead>
<tbody><tr id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_row632104417616"><td class="cellrowborder" valign="top" width="14.511451145114512%" headers="mcps1.2.5.1.1 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p4224252617616"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p4224252617616"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p4224252617616"></a>rx</p>
</td>
<td class="cellrowborder" valign="top" width="32.08320832083208%" headers="mcps1.2.5.1.2 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p6620142817616"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p6620142817616"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p6620142817616"></a>Specifies the receive queue length for an NIC.</p>
</td>
<td class="cellrowborder" valign="top" width="39.663966396639665%" headers="mcps1.2.5.1.3 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p6071548817616"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p6071548817616"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p6071548817616"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="13.74137413741374%" headers="mcps1.2.5.1.4 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p1900746317616"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p1900746317616"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p1900746317616"></a>4096</p>
</td>
</tr>
<tr id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_row23313038172018"><td class="cellrowborder" valign="top" width="14.511451145114512%" headers="mcps1.2.5.1.1 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p8490754172018"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p8490754172018"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p8490754172018"></a>tx</p>
</td>
<td class="cellrowborder" valign="top" width="32.08320832083208%" headers="mcps1.2.5.1.2 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p16662510172018"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p16662510172018"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p16662510172018"></a>Specifies the transmission queue length for an NIC.</p>
</td>
<td class="cellrowborder" valign="top" width="39.663966396639665%" headers="mcps1.2.5.1.3 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p48712694172056"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p48712694172056"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p48712694172056"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="13.74137413741374%" headers="mcps1.2.5.1.4 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p53414171172056"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p53414171172056"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p53414171172056"></a>4096</p>
</td>
</tr>
<tr id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_row3684944517616"><td class="cellrowborder" valign="top" width="14.511451145114512%" headers="mcps1.2.5.1.1 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p3201509117616"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p3201509117616"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p3201509117616"></a>mtu</p>
</td>
<td class="cellrowborder" valign="top" width="32.08320832083208%" headers="mcps1.2.5.1.2 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p4308555317616"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p4308555317616"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p4308555317616"></a>Specifies the maximum transmission unit for an NIC.</p>
</td>
<td class="cellrowborder" valign="top" width="39.663966396639665%" headers="mcps1.2.5.1.3 "><p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p26887117616"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p26887117616"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p26887117616"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="13.74137413741374%" headers="mcps1.2.5.1.4 "><p id="en-us_topic_0241805805_p17892144144616"><a name="en-us_topic_0241805805_p17892144144616"></a><a name="en-us_topic_0241805805_p17892144144616"></a>x86: <strong>1500</strong></p>
<p id="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p2177859017616"><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p2177859017616"></a><a name="en-us_topic_0241805805_en-us_topic_0085434661_en-us_topic_0059782062_p2177859017616"></a>ARM: <strong>8192</strong></p>
</td>
</tr>
</tbody>
</table>

>![](public_sys-resources/icon-notice.gif) **NOTICE:**   
>-   NIC parameters can be configured only for 10GE and larger service NICs, that is, the NIC bound to  **backIp1**.  
>-   The commands for setting NIC parameters are written into the OS startup file only after the parameters are successfully set. Information about command execution failures is recorded in logs on the server.  

