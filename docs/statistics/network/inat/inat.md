#inat

Statistics for inbound nat resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>The INAT.&lt;br>Minimum length = 1</td><tr><tr><td>clearstats</td><td>&lt;String></td><td>Read-write</td><td>Clear the statsistics / counters.&lt;br>Possible values = basic, full</td><tr><tr><td>nat46tottcp46</td><td>&lt;Double></td><td>Read-only</td><td>Total TCP packets translated (V4-;gt;v6).</td><tr><tr><td>nat46tcp46rate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for nat46tottcp46</td><tr><tr><td>nat46totudp46</td><td>&lt;Double></td><td>Read-only</td><td>Total UDP packets translated (V4-;gt;v6).</td><tr><tr><td>nat46udp46rate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for nat46totudp46</td><tr><tr><td>nat46toticmp46</td><td>&lt;Double></td><td>Read-only</td><td>Total ICMP packets translated (V4-;gt;v6).</td><tr><tr><td>nat46icmp46rate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for nat46toticmp46</td><tr><tr><td>nat46totdrop46</td><td>&lt;Double></td><td>Read-only</td><td>Total IPV4 packets dropped.</td><tr><tr><td>nat46drop46rate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for nat46totdrop46</td><tr><tr><td>nat46tottcp64</td><td>&lt;Double></td><td>Read-only</td><td>Total TCP packets translated (V6-;gt;v4).</td><tr><tr><td>nat46tcp64rate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for nat46tottcp64</td><tr><tr><td>nat46totudp64</td><td>&lt;Double></td><td>Read-only</td><td>Total UDP packets translated (V6-;gt;v4).</td><tr><tr><td>nat46udp64rate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for nat46totudp64</td><tr><tr><td>nat46toticmp64</td><td>&lt;Double></td><td>Read-only</td><td>Total ICMP packets translated (V6-;gt;v4).</td><tr><tr><td>nat46icmp64rate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for nat46toticmp64</td><tr><tr><td>nat46totdrop64</td><td>&lt;Double></td><td>Read-only</td><td>Total IPV6 packets dropped.</td><tr><tr><td>nat46drop64rate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for nat46totdrop64</td><tr><tr><td>inatnat46tcp46</td><td>&lt;Double></td><td>Read-only</td><td>TCP packets translated (V4-;gt;v6).</td><tr><tr><td>inatnat46tcp46rate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for inatnat46tcp46</td><tr><tr><td>inatnat46udp46</td><td>&lt;Double></td><td>Read-only</td><td>UDP packets translated (V4-;gt;v6).</td><tr><tr><td>inatnat46udp46rate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for inatnat46udp46</td><tr><tr><td>inatnat46icmp46</td><td>&lt;Double></td><td>Read-only</td><td>ICMP packets translated (V4-;gt;v6).</td><tr><tr><td>inatnat46icmp46rate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for inatnat46icmp46</td><tr><tr><td>inatnat46drop46</td><td>&lt;Double></td><td>Read-only</td><td>IPV4 packets dropped.</td><tr><tr><td>inatnat46drop46rate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for inatnat46drop46</td><tr><tr><td>inatnat46tcp64</td><td>&lt;Double></td><td>Read-only</td><td>TCP packets translated (V6-;gt;v4).</td><tr><tr><td>inatnat46tcp64rate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for inatnat46tcp64</td><tr><tr><td>inatnat46udp64</td><td>&lt;Double></td><td>Read-only</td><td>UDP packets translated (V6-;gt;v4).</td><tr><tr><td>inatnat46udp64rate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for inatnat46udp64</td><tr><tr><td>inatnat46icmp64</td><td>&lt;Double></td><td>Read-only</td><td>ICMP packets translated (V6-;gt;v4).</td><tr><tr><td>inatnat46icmp64rate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for inatnat46icmp64</td><tr><tr><td>inatnat46drop64</td><td>&lt;Double></td><td>Read-only</td><td>IPV6 packets dropped.</td><tr><tr><td>inatnat46drop64rate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for inatnat46drop64</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[GET (ALL)](#get-(all)) | [GET](#get)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



URL: http://NS_IP/nitro/v1/stat/inat
Query-parameters:
args
http://&lt;NSIP&gt;/nitro/v1/stat/inat?args=      name:&lt;String_value&gt;,      detail:&lt;Boolean_value&gt;,      fullvalues:&lt;Boolean_value&gt;,      ntimes:&lt;Double_value&gt;,      logfile:&lt;String_value&gt;,      clearstats:&lt;String_value&gt;,
Use this query-parameter to get inat resources based on additional properties.



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "inat": [ {      "name":<String_value>,      "nat46udp64rate":<Double_value>,      "nat46totdrop64":<Double_value>,      "nat46totudp46":<Double_value>,      "nat46icmp64rate":<Double_value>,      "inatnat46tcp46":<Double_value>,      "nat46totdrop46":<Double_value>,      "inatnat46tcp64":<Double_value>,      "inatnat46drop46":<Double_value>,      "inatnat46drop64":<Double_value>,      "inatnat46udp46":<Double_value>,      "nat46tottcp64":<Double_value>,      "nat46drop46rate":<Double_value>,      "inatnat46drop46rate":<Double_value>,      "inatnat46tcp64rate":<Double_value>,      "inatnat46icmp64":<Double_value>,      "nat46drop64rate":<Double_value>,      "inatnat46tcp46rate":<Double_value>,      "nat46tottcp46":<Double_value>,      "nat46toticmp46":<Double_value>,      "inatnat46icmp46rate":<Double_value>,      "inatnat46udp64":<Double_value>,      "nat46tcp46rate":<Double_value>,      "inatnat46drop64rate":<Double_value>,      "inatnat46udp64rate":<Double_value>,      "nat46icmp46rate":<Double_value>,      "inatnat46icmp46":<Double_value>,      "inatnat46icmp64rate":<Double_value>,      "nat46tcp64rate":<Double_value>,      "nat46totudp64":<Double_value>,      "nat46udp46rate":<Double_value>,      "nat46toticmp64":<Double_value>,      "inatnat46udp46rate":<Double_value>}]}```



###get



URL: http://NS_IP/nitro/v1/stat/inat/name_value&lt;String&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "inat": [ {      "name":<String_value>,      "nat46udp64rate":<Double_value>,      "nat46totdrop64":<Double_value>,      "nat46totudp46":<Double_value>,      "nat46icmp64rate":<Double_value>,      "inatnat46tcp46":<Double_value>,      "nat46totdrop46":<Double_value>,      "inatnat46tcp64":<Double_value>,      "inatnat46drop46":<Double_value>,      "inatnat46drop64":<Double_value>,      "inatnat46udp46":<Double_value>,      "nat46tottcp64":<Double_value>,      "nat46drop46rate":<Double_value>,      "inatnat46drop46rate":<Double_value>,      "inatnat46tcp64rate":<Double_value>,      "inatnat46icmp64":<Double_value>,      "nat46drop64rate":<Double_value>,      "inatnat46tcp46rate":<Double_value>,      "nat46tottcp46":<Double_value>,      "nat46toticmp46":<Double_value>,      "inatnat46icmp46rate":<Double_value>,      "inatnat46udp64":<Double_value>,      "nat46tcp46rate":<Double_value>,      "inatnat46drop64rate":<Double_value>,      "inatnat46udp64rate":<Double_value>,      "nat46icmp46rate":<Double_value>,      "inatnat46icmp46":<Double_value>,      "inatnat46icmp64rate":<Double_value>,      "nat46tcp64rate":<Double_value>,      "nat46totudp64":<Double_value>,      "nat46udp46rate":<Double_value>,      "nat46toticmp64":<Double_value>,      "inatnat46udp46rate":<Double_value>}]}```



