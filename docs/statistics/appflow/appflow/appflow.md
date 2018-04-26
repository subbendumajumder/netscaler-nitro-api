#appflow

Statistics for appflow.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>clearstats</td><td>&lt;String></td><td>Read-write</td><td>Clear the statsistics / counters.<br>Possible values = basic, full</td></tr><tr><td>appflowtotaltxoctets</td><td>&lt;Double></td><td>Read-only</td><td>The total number of AppFlow (IPFIX) octets that the NetScaler has transmitted.</td></tr><tr><td>appflowtxoctetsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for appflowtotaltxoctets</td></tr><tr><td>appflowtotalflows</td><td>&lt;Double></td><td>Read-only</td><td>The total number of AppFlow (IPFIX) flows that the NetScaler has transmitted.</td></tr><tr><td>appflowflowsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for appflowtotalflows</td></tr><tr><td>appflowtotaltxmessagess</td><td>&lt;Double></td><td>Read-only</td><td>The total number of AppFlow (IPFIX) messages that the NetScaler has transmitted.</td></tr><tr><td>appflowtxmessagessrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for appflowtotaltxmessagess</td></tr><tr><td>appflowtotalignoctets</td><td>&lt;Double></td><td>Read-only</td><td>The total number of octets that the NetScaler has ignored for AppFlow (IPFIX).</td></tr><tr><td>appflowignoctetsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for appflowtotalignoctets</td></tr><tr><td>appflowtotalignpacketss</td><td>&lt;Double></td><td>Read-only</td><td>The total number of packets that the NetScaler has ignored for AppFlow (IPFIX).</td></tr><tr><td>appflowignpacketssrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for appflowtotalignpacketss</td></tr><tr><td>appflowtotalnotxoctets</td><td>&lt;Double></td><td>Read-only</td><td>The total number of AppFlow (IPFIX) octets that the NetScaler has not transmitted.</td></tr><tr><td>appflownotxoctetsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for appflowtotalnotxoctets</td></tr><tr><td>appflowtotalnotxflows</td><td>&lt;Double></td><td>Read-only</td><td>The total number of AppFlow (IPFIX) flows that the NetScaler has not transmitted.</td></tr><tr><td>appflownotxflowsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for appflowtotalnotxflows</td></tr><tr><td>appflowtotalnotxpackets</td><td>&lt;Double></td><td>Read-only</td><td>The total number of AppFlow (IPFIX) packets that the NetScaler has not transmitted.</td></tr><tr><td>appflownotxpacketsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for appflowtotalnotxpackets</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[GET (ALL)](#get-)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/appflow
<b>Query-parameters:</b>
<b>args</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/appflow?<b>args=detail:&lt;Boolean_value&gt;,fullvalues:&lt;Boolean_value&gt;,ntimes:&lt;Double_value&gt;,logfile:&lt;String_value&gt;,clearstats:&lt;String_value&gt;</b>
Use this query-parameter to get appflow resources based on additional properties.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "appflow": [ {"appflowtxmessagessrate":<Double_value>,"appflowtotalnotxoctets":<Double_value>,"appflowtotaltxmessagess":<Double_value>,"appflowtotalignpacketss":<Double_value>,"appflowtotalflows":<Double_value>,"appflowtotalnotxflows":<Double_value>,"appflownotxflowsrate":<Double_value>,"appflowtotalnotxpackets":<Double_value>,"appflownotxoctetsrate":<Double_value>,"appflowignpacketssrate":<Double_value>,"appflowtxoctetsrate":<Double_value>,"appflowignoctetsrate":<Double_value>,"appflowtotalignoctets":<Double_value>,"appflowtotaltxoctets":<Double_value>,"appflownotxpacketsrate":<Double_value>,"appflowflowsrate":<Double_value>}]}```



