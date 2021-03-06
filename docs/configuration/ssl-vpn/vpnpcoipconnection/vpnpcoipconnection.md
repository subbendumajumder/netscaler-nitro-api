#vpnpcoipconnection

Configuration for PCoIP connection resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>username</td><td>&lt;String></td><td>Read-write</td><td>User name for the PCOIP connections.<br>Minimum length = 1</td></tr><tr><td>nodeid</td><td>&lt;Double></td><td>Read-write</td><td>Unique number that identifies the cluster node.<br>Minimum value = 0<br>Maximum value = 31</td></tr><tr><td>all</td><td>&lt;Boolean></td><td>Read-write</td><td>All active pcoip connections.</td></tr><tr><td>srcip</td><td>&lt;String></td><td>Read-only</td><td>The client IP address.</td></tr><tr><td>srcport</td><td>&lt;Integer></td><td>Read-only</td><td>The client port.<br>Range 1 - 65535<br>* in CLI is represented as 65535 in NITRO API</td></tr><tr><td>destip</td><td>&lt;String></td><td>Read-only</td><td>The VDA IP address.</td></tr><tr><td>destport</td><td>&lt;Integer></td><td>Read-only</td><td>The VDA server port.<br>Range 1 - 65535<br>* in CLI is represented as 65535 in NITRO API</td></tr><tr><td>peid</td><td>&lt;Double></td><td>Read-only</td><td>Core id of the session owner.</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[KILL]()| [GET (ALL)](#get-)| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###kill



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnpcoipconnection?<b>action=kill</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"vpnpcoipconnection":{"username":<String_value>,"all":<Boolean_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnpcoipconnection
<b>Query-parameters:</b>
<b>args</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnpcoipconnection?<b>args=username:&lt;String_value&gt;,nodeid:&lt;Double_value&gt;</b>
Use this query-parameter to get vpnpcoipconnection resources based on additional properties.


<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnpcoipconnection?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnpcoipconnection?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of vpnpcoipconnection resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnpcoipconnection?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnpcoipconnection?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the vpnpcoipconnection resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "vpnpcoipconnection": [ {username:<String_value>,nodeid:<Double_value>"srcip":<String_value>,"srcport":<Integer_value>,"destip":<String_value>,"destport":<Integer_value>,"peid":<Double_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnpcoipconnection?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "vpnpcoipconnection": [ { "__count": "#no"} ] }```



