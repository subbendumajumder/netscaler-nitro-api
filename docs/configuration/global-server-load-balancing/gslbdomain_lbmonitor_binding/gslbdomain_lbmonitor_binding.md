#gslbdomain_lbmonitor_binding

Binding object showing the lbmonitor that can be bound to gslbdomain.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name of the Domain.&lt;br>Minimum length = 1</td><tr><tr><td>monitorname</td><td>&lt;String></td><td>Read-write</td><td>Monitor name.</td><tr><tr><td>monstatcode</td><td>&lt;Integer></td><td>Read-only</td><td>The code indicating the monitor response.</td><tr><tr><td>customheaders</td><td>&lt;String></td><td>Read-only</td><td>The string that is sent to the service. Applicable to HTTP ,HTTP-ECV and RTSP monitor types.</td><tr><tr><td>iptunnel</td><td>&lt;String></td><td>Read-only</td><td>The state of the monitor for tunneled devices.&lt;br>Possible values = YES, NO</td><tr><tr><td>responsetime</td><td>&lt;Double></td><td>Read-only</td><td>Response time of this monitor.</td><tr><tr><td>monstate</td><td>&lt;String></td><td>Read-only</td><td>Monitor state.&lt;br>Possible values = UP, DOWN, UNKNOWN, BUSY, OUT OF SERVICE, GOING OUT OF SERVICE, DOWN WHEN GOING OUT OF SERVICE, NS_EMPTY_STR, Unknown, DISABLED</td><tr><tr><td>lastresponse</td><td>&lt;String></td><td>Read-only</td><td>The string form of monstatcode.</td><tr><tr><td>servicename</td><td>&lt;String></td><td>Read-only</td><td>The service name.</td><tr><tr><td>monitortotalprobes</td><td>&lt;Double></td><td>Read-only</td><td>Total monitor probes.</td><tr><tr><td>respcode</td><td>&lt;String></td><td>Read-only</td><td>The response codes.</td><tr><tr><td>vservername</td><td>&lt;String></td><td>Read-only</td><td>.</td><tr><tr><td>httprequest</td><td>&lt;String></td><td>Read-only</td><td>HTTP request to the backend server.</td><tr><tr><td>monitortotalfailedprobes</td><td>&lt;Double></td><td>Read-only</td><td>Total probes failed.</td><tr><tr><td>monitorcurrentfailedprobes</td><td>&lt;Double></td><td>Read-only</td><td>Total number of current failed probes.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[GET](#get) | [GET (ALL)](#get-(all)) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbdomain_lbmonitor_binding/name_value&lt;String&gt;
Query-parameters:
filter
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbdomain_lbmonitor_binding/name_value&lt;String&gt;?filter=property-name1:property-value1,property-name2:property-value2
Use this query-parameter to get the filtered set of gslbdomain_lbmonitor_binding resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


pagination
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbdomain_lbmonitor_binding/name_value&lt;String&gt;?pagesize=#no;pageno=#no
Use this query-parameter to get the gslbdomain_lbmonitor_binding resources in chunks.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "gslbdomain_lbmonitor_binding": [ {      "name":<String_value>,      "monitorname":<String_value>,      "monstatcode":<Integer_value>,      "customheaders":<String_value>,      "iptunnel":<String_value>,      "responsetime":<Double_value>,      "monstate":<String_value>,      "lastresponse":<String_value>,      "servicename":<String_value>,      "monitortotalprobes":<Double_value>,      "respcode":<String_value>,      "vservername":<String_value>,      "httprequest":<String_value>,      "monitortotalfailedprobes":<Double_value>,      "monitorcurrentfailedprobes":<Double_value>}]}```



###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbdomain_lbmonitor_binding
Query-parameters:
bulkbindings
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbdomain_lbmonitor_binding?bulkbindings=yes
NITRO allows you to fetch bindings in bulk.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "gslbdomain_lbmonitor_binding": [ {      "name":<String_value>,      "monitorname":<String_value>,      "monstatcode":<Integer_value>,      "customheaders":<String_value>,      "iptunnel":<String_value>,      "responsetime":<Double_value>,      "monstate":<String_value>,      "lastresponse":<String_value>,      "servicename":<String_value>,      "monitortotalprobes":<Double_value>,      "respcode":<String_value>,      "vservername":<String_value>,      "httprequest":<String_value>,      "monitortotalfailedprobes":<Double_value>,      "monitorcurrentfailedprobes":<Double_value>}]}```



###count



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbdomain_lbmonitor_binding/name_value&lt;String&gt;?count=yes
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: 
{"gslbdomain_lbmonitor_binding": [ { "__count": "#no"} ] }


