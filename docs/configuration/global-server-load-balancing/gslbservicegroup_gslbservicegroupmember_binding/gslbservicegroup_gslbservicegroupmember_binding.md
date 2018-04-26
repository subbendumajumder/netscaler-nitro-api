#gslbservicegroup_gslbservicegroupmember_binding

Binding object showing the gslbservicegroupmember that can be bound to gslbservicegroup.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>state</td><td>&lt;String></td><td>Read-write</td><td>Initial state of the GSLB service group.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>publicport</td><td>&lt;Integer></td><td>Read-write</td><td>The public port associated with the GSLB service's public IP address. The port is mapped to the service's private port number. Applicable to the local GSLB service. Optional.<br>Minimum value = 1</td></tr><tr><td>weight</td><td>&lt;Double></td><td>Read-write</td><td>Weight to assign to the servers in the service group. Specifies the capacity of the servers relative to the other servers in the load balancing configuration. The higher the weight, the higher the percentage of requests sent to the service.<br>Minimum value = 1<br>Maximum value = 100</td></tr><tr><td>port</td><td>&lt;Integer></td><td>Read-write</td><td>Server port number.<br>Range 1 - 65535<br>* in CLI is represented as 65535 in NITRO API</td></tr><tr><td>servername</td><td>&lt;String></td><td>Read-write</td><td>Name of the server to which to bind the service group.<br>Minimum length = 1</td></tr><tr><td>ip</td><td>&lt;String></td><td>Read-write</td><td>IP Address.</td></tr><tr><td>servicegroupname</td><td>&lt;String></td><td>Read-write</td><td>Name of the GSLB service group.<br>Minimum length = 1</td></tr><tr><td>hashid</td><td>&lt;Double></td><td>Read-write</td><td>The hash identifier for the service. This must be unique for each service. This parameter is used by hash based load balancing methods.<br>Minimum value = 1</td></tr><tr><td>publicip</td><td>&lt;String></td><td>Read-write</td><td>The public IP address that a NAT device translates to the GSLB service's private IP address. Optional.<br>Minimum length = 1</td></tr><tr><td>threshold</td><td>&lt;String></td><td>Read-only</td><td>.<br>Possible values = ABOVE, BELOW</td></tr><tr><td>delay</td><td>&lt;Double></td><td>Read-only</td><td>The time allowed (in seconds) for a graceful shutdown. During this period, new connections or requests will continue to be sent to this service for clients who already have a persistent session on the system. Connections or requests from fresh or new clients who do not yet have a persistence sessions on the system will not be sent to the service. Instead, they will be load balanced among other available services. After the delay time expires, no new requests or connections will be sent to the service.</td></tr><tr><td>statechangetimesec</td><td>&lt;String></td><td>Read-only</td><td>Time when last state change occurred. Seconds part.</td></tr><tr><td>preferredlocation</td><td>&lt;String></td><td>Read-only</td><td>Prefered location.</td></tr><tr><td>svrstate</td><td>&lt;String></td><td>Read-only</td><td>The state of the GSLB service.<br>Possible values = UP, DOWN, UNKNOWN, BUSY, OUT OF SERVICE, GOING OUT OF SERVICE, DOWN WHEN GOING OUT OF SERVICE, NS_EMPTY_STR, Unknown, DISABLED</td></tr><tr><td>gslbthreshold</td><td>&lt;Integer></td><td>Read-only</td><td>Indicates if gslb svc has reached threshold.</td></tr><tr><td>tickssincelaststatechange</td><td>&lt;Double></td><td>Read-only</td><td>Time in 10 millisecond ticks since the last state change.</td></tr><tr><td>graceful</td><td>&lt;String></td><td>Read-only</td><td>Wait for all existing connections to the service to terminate before shutting down the service.<br>Default value: NO<br>Possible values = YES, NO</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD:]()| [DELETE:](#de)| [GET]()| [GET (ALL)](#get-)| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add:



<b>URL:</b>http://&lt;netscaler-ip-address/nitro/v1/config/gslbservicegroup_gslbservicegroupmember_binding
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"gslbservicegroup_gslbservicegroupmember_binding":{<b>"servicegroupname":<String_value>,</b>"ip":<String_value>,"servername":<String_value>,"port":<Integer_value>,"weight":<Double_value>,"state":<String_value>,"hashid":<Double_value>,"publicip":<String_value>,"publicport":<Integer_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete:



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbservicegroup_gslbservicegroupmember_binding/servicegroupname_value&lt;String&gt;
<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbservicegroup_gslbservicegroupmember_binding/servicegroupname_value&lt;String&gt;
<b>Query-parameters:</b>
<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbservicegroup_gslbservicegroupmember_binding/servicegroupname_value&lt;String&gt;?<b>filter=property-name1:property-value1,property-name2:property-value2</b>
Use this query-parameter to get the filtered set of gslbservicegroup_gslbservicegroupmember_binding resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbservicegroup_gslbservicegroupmember_binding/servicegroupname_value&lt;String&gt;?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the gslbservicegroup_gslbservicegroupmember_binding resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "gslbservicegroup_gslbservicegroupmember_binding": [ {"state":<String_value>,"publicport":<Integer_value>,"weight":<Double_value>,"port":<Integer_value>,"servername":<String_value>,"ip":<String_value>,"servicegroupname":<String_value>,"hashid":<Double_value>,"publicip":<String_value>,"threshold":<String_value>,"delay":<Double_value>,"statechangetimesec":<String_value>,"preferredlocation":<String_value>,"svrstate":<String_value>,"gslbthreshold":<Integer_value>,"tickssincelaststatechange":<Double_value>,"graceful":<String_value>}]}```



###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbservicegroup_gslbservicegroupmember_binding
<b>Query-parameters:</b>
<b>bulkbindings</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbservicegroup_gslbservicegroupmember_binding?<b>bulkbindings=yes</b>
NITRO allows you to fetch bindings in bulk.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "gslbservicegroup_gslbservicegroupmember_binding": [ {"state":<String_value>,"publicport":<Integer_value>,"weight":<Double_value>,"port":<Integer_value>,"servername":<String_value>,"ip":<String_value>,"servicegroupname":<String_value>,"hashid":<Double_value>,"publicip":<String_value>,"threshold":<String_value>,"delay":<Double_value>,"statechangetimesec":<String_value>,"preferredlocation":<String_value>,"svrstate":<String_value>,"gslbthreshold":<Integer_value>,"tickssincelaststatechange":<Double_value>,"graceful":<String_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbservicegroup_gslbservicegroupmember_binding/servicegroupname_value&lt;String&gt;?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{"gslbservicegroup_gslbservicegroupmember_binding": [ { "__count": "#no"} ] }```



