#servicegroup_servicegroupentitymonbindings_binding

Binding object showing the servicegroupentitymonbindings that can be bound to servicegroup.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>servicegroupname</td><td>&lt;String></td><td>Read-write</td><td>Name of the service group.<br>Minimum length = 1</td></tr><tr><td>servicegroupentname2</td><td>&lt;String></td><td>Read-write</td><td>.</td></tr><tr><td>port</td><td>&lt;Integer></td><td>Read-write</td><td>Port number of the service. Each service must have a unique port number.<br>Range 1 - 65535<br>* in CLI is represented as 65535 in NITRO API</td></tr><tr><td>state</td><td>&lt;String></td><td>Read-write</td><td>Initial state of the service after binding.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>hashid</td><td>&lt;Double></td><td>Read-write</td><td>Unique numerical identifier used by hash based load balancing methods to identify a service.<br>Minimum value = 1</td></tr><tr><td>serverid</td><td>&lt;Double></td><td>Read-write</td><td>The identifier for the service. This is used when the persistency type is set to Custom Server ID.</td></tr><tr><td>customserverid</td><td>&lt;String></td><td>Read-write</td><td>Unique service identifier. Used when the persistency type for the virtual server is set to Custom Server ID.<br>Default value: "None"</td></tr><tr><td>weight</td><td>&lt;Double></td><td>Read-write</td><td>.<br>Default value: 1<br>Minimum value = 1<br>Maximum value = 100</td></tr><tr><td>monitor_name</td><td>&lt;String></td><td>Read-write</td><td>Monitor name.</td></tr><tr><td>passive</td><td>&lt;Boolean></td><td>Read-write</td><td>Indicates if load monitor is passive. A passive load monitor does not remove service from LB decision when threshold is breached.</td></tr><tr><td>lastresponse</td><td>&lt;String></td><td>Read-only</td><td>The string form of monstatcode.</td></tr><tr><td>monitor_state</td><td>&lt;String></td><td>Read-only</td><td>The running state of the monitor on this service.<br>Possible values = UP, DOWN, UNKNOWN, BUSY, OUT OF SERVICE, GOING OUT OF SERVICE, DOWN WHEN GOING OUT OF SERVICE, NS_EMPTY_STR, Unknown, DISABLED</td></tr><tr><td>monitortotalprobes</td><td>&lt;Double></td><td>Read-only</td><td>Total number of probes sent to monitor this service.</td></tr><tr><td>monitortotalfailedprobes</td><td>&lt;Double></td><td>Read-only</td><td>Total number of failed probes.</td></tr><tr><td>monitorcurrentfailedprobes</td><td>&lt;Double></td><td>Read-only</td><td>Total number of currently failed probes.</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[GET]()| [GET (ALL)](#get-)| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/servicegroup_servicegroupentitymonbindings_binding/servicegroupname_value&lt;String&gt;
<b>Query-parameters:</b>
<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/servicegroup_servicegroupentitymonbindings_binding/servicegroupname_value&lt;String&gt;?<b>filter=property-name1:property-value1,property-name2:property-value2</b>
Use this query-parameter to get the filtered set of servicegroup_servicegroupentitymonbindings_binding resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/servicegroup_servicegroupentitymonbindings_binding/servicegroupname_value&lt;String&gt;?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the servicegroup_servicegroupentitymonbindings_binding resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "servicegroup_servicegroupentitymonbindings_binding": [ {"servicegroupname":<String_value>,"servicegroupentname2":<String_value>,"port":<Integer_value>,"state":<String_value>,"hashid":<Double_value>,"serverid":<Double_value>,"customserverid":<String_value>,"weight":<Double_value>,"monitor_name":<String_value>,"passive":<Boolean_value>,"lastresponse":<String_value>,"monitor_state":<String_value>,"monitortotalprobes":<Double_value>,"monitortotalfailedprobes":<Double_value>,"monitorcurrentfailedprobes":<Double_value>}]}```



###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/servicegroup_servicegroupentitymonbindings_binding
<b>Query-parameters:</b>
<b>bulkbindings</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/servicegroup_servicegroupentitymonbindings_binding?<b>bulkbindings=yes</b>
NITRO allows you to fetch bindings in bulk.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "servicegroup_servicegroupentitymonbindings_binding": [ {"servicegroupname":<String_value>,"servicegroupentname2":<String_value>,"port":<Integer_value>,"state":<String_value>,"hashid":<Double_value>,"serverid":<Double_value>,"customserverid":<String_value>,"weight":<Double_value>,"monitor_name":<String_value>,"passive":<Boolean_value>,"lastresponse":<String_value>,"monitor_state":<String_value>,"monitortotalprobes":<Double_value>,"monitortotalfailedprobes":<Double_value>,"monitorcurrentfailedprobes":<Double_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/servicegroup_servicegroupentitymonbindings_binding/servicegroupname_value&lt;String&gt;?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{"servicegroup_servicegroupentitymonbindings_binding": [ { "__count": "#no"} ] }```



