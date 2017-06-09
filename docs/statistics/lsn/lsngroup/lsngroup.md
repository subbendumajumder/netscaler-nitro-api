#lsngroup

Statistics for LSN group resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>groupname</td><td>&lt;String></td><td>Read-write</td><td>Name of the LSN Group.&lt;br>Minimum length = 1&lt;br>Maximum length = 127</td><tr><tr><td>clearstats</td><td>&lt;String></td><td>Read-write</td><td>Clear the statsistics / counters.&lt;br>Possible values = basic, full</td><tr><tr><td>lsngrpcursessions</td><td>&lt;Double></td><td>Read-only</td><td>Number of Current Sessions for LSN group</td><tr><tr><td>lsngrpcursessionsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for lsngrpcursessions</td><tr><tr><td>lsngrptottranslbytes</td><td>&lt;Double></td><td>Read-only</td><td>Number of Translated Bytes for LSN group</td><tr><tr><td>lsngrptranslbytesrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for lsngrptottranslbytes</td><tr><tr><td>lsngrptottranslpkts</td><td>&lt;Double></td><td>Read-only</td><td>Number of Translated Pkts for LSN group</td><tr><tr><td>lsngrptranslpktsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for lsngrptottranslpkts</td><tr><tr><td>lsngrptottcptranslpkts</td><td>&lt;Double></td><td>Read-only</td><td>Number of TCP Translated Pkts for LSN group</td><tr><tr><td>lsngrptcptranslpktsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for lsngrptottcptranslpkts</td><tr><tr><td>lsngrptottcptranslbytes</td><td>&lt;Double></td><td>Read-only</td><td>Number of TCP Translated Bytes for LSN group</td><tr><tr><td>lsngrptcptranslbytesrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for lsngrptottcptranslbytes</td><tr><tr><td>lsngrptottcpdrppkts</td><td>&lt;Double></td><td>Read-only</td><td>Number of TCP Dropped Pkts for LSN group</td><tr><tr><td>lsngrptcpdrppktsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for lsngrptottcpdrppkts</td><tr><tr><td>lsngrpcurtcpsessions</td><td>&lt;Double></td><td>Read-only</td><td>Number of TCP Current Sessions for LSN group</td><tr><tr><td>lsngrpcurtcpsessionsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for lsngrpcurtcpsessions</td><tr><tr><td>lsngrptotudptranslpkts</td><td>&lt;Double></td><td>Read-only</td><td>Number of UDP Translated Pkts for LSN group</td><tr><tr><td>lsngrpudptranslpktsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for lsngrptotudptranslpkts</td><tr><tr><td>lsngrptotudptranslbytes</td><td>&lt;Double></td><td>Read-only</td><td>Number of UDP Translated Bytes for LSN group</td><tr><tr><td>lsngrpudptranslbytesrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for lsngrptotudptranslbytes</td><tr><tr><td>lsngrptotudpdrppkts</td><td>&lt;Double></td><td>Read-only</td><td>Number of UDP Dropped Pkts for LSN group</td><tr><tr><td>lsngrpudpdrppktsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for lsngrptotudpdrppkts</td><tr><tr><td>lsngrpcurudpsessions</td><td>&lt;Double></td><td>Read-only</td><td>Number of UDP Current Sessions for LSN group</td><tr><tr><td>lsngrpcurudpsessionsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for lsngrpcurudpsessions</td><tr><tr><td>lsngrptoticmptranslpkts</td><td>&lt;Double></td><td>Read-only</td><td>Number of ICMP Translated Pkts for LSN group</td><tr><tr><td>lsngrpicmptranslpktsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for lsngrptoticmptranslpkts</td><tr><tr><td>lsngrptoticmptranslbytes</td><td>&lt;Double></td><td>Read-only</td><td>Number of ICMP Translated Bytes for LSN group</td><tr><tr><td>lsngrpicmptranslbytesrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for lsngrptoticmptranslbytes</td><tr><tr><td>lsngrptoticmpdrppkts</td><td>&lt;Double></td><td>Read-only</td><td>Number of ICMP Dropped Pkts for LSN group</td><tr><tr><td>lsngrpicmpdrppktsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for lsngrptoticmpdrppkts</td><tr><tr><td>lsngrpcuricmpsessions</td><td>&lt;Double></td><td>Read-only</td><td>Number of ICMP Current Sessions for LSN group</td><tr><tr><td>lsngrpcuricmpsessionsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for lsngrpcuricmpsessions</td><tr><tr><td>lsngrpcursubscribers</td><td>&lt;Double></td><td>Read-only</td><td>Number of ICMP Current Sessions for LSN group</td><tr><tr><td>lsngrpcursubscribersrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for lsngrpcursubscribers</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[GET (ALL)](#get-(all)) | [GET](#get)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/lsngroup
Query-parameters:
args
http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/lsngroup?args=groupname:&lt;String_value&gt;,detail:&lt;Boolean_value&gt;,fullvalues:&lt;Boolean_value&gt;,ntimes:&lt;Double_value&gt;,logfile:&lt;String_value&gt;,clearstats:&lt;String_value&gt;
Use this query-parameter to get lsngroup resources based on additional properties.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "lsngroup": [ {      "groupname":<String_value>,      "lsngrptcptranslbytesrate":<Double_value>,      "lsngrptottranslpkts":<Double_value>,      "lsngrptoticmptranslpkts":<Double_value>,      "lsngrpcurtcpsessions":<Double_value>,      "lsngrpicmptranslbytesrate":<Double_value>,      "lsngrptotudptranslpkts":<Double_value>,      "lsngrptottcpdrppkts":<Double_value>,      "lsngrptranslbytesrate":<Double_value>,      "lsngrptotudptranslbytes":<Double_value>,      "lsngrptoticmptranslbytes":<Double_value>,      "lsngrpcursubscribersrate":<Double_value>,      "lsngrptottranslbytes":<Double_value>,      "lsngrptoticmpdrppkts":<Double_value>,      "lsngrptcptranslpktsrate":<Double_value>,      "lsngrpudptranslpktsrate":<Double_value>,      "lsngrpcursubscribers":<Double_value>,      "lsngrpudptranslbytesrate":<Double_value>,      "lsngrpcuricmpsessionsrate":<Double_value>,      "lsngrpcurudpsessions":<Double_value>,      "lsngrptottcptranslpkts":<Double_value>,      "lsngrptotudpdrppkts":<Double_value>,      "lsngrpicmptranslpktsrate":<Double_value>,      "lsngrpcuricmpsessions":<Double_value>,      "lsngrpcurtcpsessionsrate":<Double_value>,      "lsngrpcurudpsessionsrate":<Double_value>,      "lsngrptranslpktsrate":<Double_value>,      "lsngrptottcptranslbytes":<Double_value>,      "lsngrpicmpdrppktsrate":<Double_value>,      "lsngrpcursessionsrate":<Double_value>,      "lsngrpudpdrppktsrate":<Double_value>,      "lsngrptcpdrppktsrate":<Double_value>,      "lsngrpcursessions":<Double_value>}]}```



###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/lsngroup/groupname_value&gt;&lt;String&gt;
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "lsngroup": [ {      "groupname":<String_value>,      "lsngrptcptranslbytesrate":<Double_value>,      "lsngrptottranslpkts":<Double_value>,      "lsngrptoticmptranslpkts":<Double_value>,      "lsngrpcurtcpsessions":<Double_value>,      "lsngrpicmptranslbytesrate":<Double_value>,      "lsngrptotudptranslpkts":<Double_value>,      "lsngrptottcpdrppkts":<Double_value>,      "lsngrptranslbytesrate":<Double_value>,      "lsngrptotudptranslbytes":<Double_value>,      "lsngrptoticmptranslbytes":<Double_value>,      "lsngrpcursubscribersrate":<Double_value>,      "lsngrptottranslbytes":<Double_value>,      "lsngrptoticmpdrppkts":<Double_value>,      "lsngrptcptranslpktsrate":<Double_value>,      "lsngrpudptranslpktsrate":<Double_value>,      "lsngrpcursubscribers":<Double_value>,      "lsngrpudptranslbytesrate":<Double_value>,      "lsngrpcuricmpsessionsrate":<Double_value>,      "lsngrpcurudpsessions":<Double_value>,      "lsngrptottcptranslpkts":<Double_value>,      "lsngrptotudpdrppkts":<Double_value>,      "lsngrpicmptranslpktsrate":<Double_value>,      "lsngrpcuricmpsessions":<Double_value>,      "lsngrpcurtcpsessionsrate":<Double_value>,      "lsngrpcurudpsessionsrate":<Double_value>,      "lsngrptranslpktsrate":<Double_value>,      "lsngrptottcptranslbytes":<Double_value>,      "lsngrpicmpdrppktsrate":<Double_value>,      "lsngrpcursessionsrate":<Double_value>,      "lsngrpudpdrppktsrate":<Double_value>,      "lsngrptcpdrppktsrate":<Double_value>,      "lsngrpcursessions":<Double_value>}]}```



