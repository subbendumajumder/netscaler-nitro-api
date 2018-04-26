#gslbdomain_gslbservice_binding

Binding object showing the gslbservice that can be bound to gslbdomain.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name of the Domain.<br>Minimum length = 1</td></tr><tr><td>servicename</td><td>&lt;String></td><td>Read-write</td><td>The service name.</td></tr><tr><td>cnameentry</td><td>&lt;String></td><td>Read-only</td><td>The cname of the gslb service.</td></tr><tr><td>gslbthreshold</td><td>&lt;Integer></td><td>Read-only</td><td>The threshold value of the service.</td></tr><tr><td>port</td><td>&lt;Integer></td><td>Read-only</td><td>Port Number.<br>Minimum value = 1<br>Range 1 - 65535<br>* in CLI is represented as 65535 in NITRO API</td></tr><tr><td>state</td><td>&lt;String></td><td>Read-only</td><td>The state of the vserver.<br>Possible values = UP, DOWN, UNKNOWN, BUSY, OUT OF SERVICE, GOING OUT OF SERVICE, DOWN WHEN GOING OUT OF SERVICE, NS_EMPTY_STR, Unknown, DISABLED</td></tr><tr><td>vservername</td><td>&lt;String></td><td>Read-only</td><td>.</td></tr><tr><td>svreffgslbstate</td><td>&lt;String></td><td>Read-only</td><td>GSLB server state.<br>Possible values = UP, DOWN, UNKNOWN, BUSY, OUT OF SERVICE, GOING OUT OF SERVICE, DOWN WHEN GOING OUT OF SERVICE, NS_EMPTY_STR, Unknown, DISABLED</td></tr><tr><td>dynamicconfwt</td><td>&lt;Double></td><td>Read-only</td><td>dynamic weight.</td></tr><tr><td>weight</td><td>&lt;Double></td><td>Read-only</td><td>weight assigned.<br>Minimum value = 1<br>Maximum value = 100</td></tr><tr><td>ipaddress</td><td>&lt;String></td><td>Read-only</td><td>The Ip address of the service.</td></tr><tr><td>servicetype</td><td>&lt;String></td><td>Read-only</td><td>The type GSLB service.<br>Possible values = HTTP, FTP, TCP, UDP, SSL, SSL_BRIDGE, SSL_TCP, NNTP, ANY, SIP_UDP, SIP_TCP, SIP_SSL, RADIUS, RDP, RTSP, MYSQL, MSSQL, ORACLE</td></tr><tr><td>cumulativeweight</td><td>&lt;Double></td><td>Read-only</td><td>cumlative weight.</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[GET]()| [GET (ALL)](#get-)| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbdomain_gslbservice_binding/name_value&lt;String&gt;
<b>Query-parameters:</b>
<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbdomain_gslbservice_binding/name_value&lt;String&gt;?<b>filter=property-name1:property-value1,property-name2:property-value2</b>
Use this query-parameter to get the filtered set of gslbdomain_gslbservice_binding resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbdomain_gslbservice_binding/name_value&lt;String&gt;?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the gslbdomain_gslbservice_binding resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "gslbdomain_gslbservice_binding": [ {"name":<String_value>,"servicename":<String_value>,"cnameentry":<String_value>,"gslbthreshold":<Integer_value>,"port":<Integer_value>,"state":<String_value>,"vservername":<String_value>,"svreffgslbstate":<String_value>,"dynamicconfwt":<Double_value>,"weight":<Double_value>,"ipaddress":<String_value>,"servicetype":<String_value>,"cumulativeweight":<Double_value>}]}```



###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbdomain_gslbservice_binding
<b>Query-parameters:</b>
<b>bulkbindings</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbdomain_gslbservice_binding?<b>bulkbindings=yes</b>
NITRO allows you to fetch bindings in bulk.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "gslbdomain_gslbservice_binding": [ {"name":<String_value>,"servicename":<String_value>,"cnameentry":<String_value>,"gslbthreshold":<Integer_value>,"port":<Integer_value>,"state":<String_value>,"vservername":<String_value>,"svreffgslbstate":<String_value>,"dynamicconfwt":<Double_value>,"weight":<Double_value>,"ipaddress":<String_value>,"servicetype":<String_value>,"cumulativeweight":<Double_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbdomain_gslbservice_binding/name_value&lt;String&gt;?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{"gslbdomain_gslbservice_binding": [ { "__count": "#no"} ] }```



