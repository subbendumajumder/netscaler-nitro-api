#route6

Configuration for route 6 resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>network</td><td>&lt;String></td><td>Read-write</td><td>IPv6 network address for which to add a route entry to the routing table of the NetScaler appliance.</td></tr><tr><td>gateway</td><td>&lt;String></td><td>Read-write</td><td>The gateway for this route. The value for this parameter is either an IPv6 address or null.<br>Default value: 0</td></tr><tr><td>vlan</td><td>&lt;Double></td><td>Read-write</td><td>Integer value that uniquely identifies a VLAN through which the NetScaler appliance forwards the packets for this route.<br>Default value: 0<br>Minimum value = 0<br>Maximum value = 4094</td></tr><tr><td>vxlan</td><td>&lt;Double></td><td>Read-write</td><td>Integer value that uniquely identifies a VXLAN through which the NetScaler appliance forwards the packets for this route.<br>Minimum value = 1<br>Maximum value = 16777215</td></tr><tr><td>weight</td><td>&lt;Double></td><td>Read-write</td><td>Positive integer used by the routing algorithms to determine preference for this route over others of equal cost. The lower the weight, the higher the preference.<br>Default value: 1<br>Minimum value = 1<br>Maximum value = 65535</td></tr><tr><td>distance</td><td>&lt;Double></td><td>Read-write</td><td>Administrative distance of this route from the appliance.<br>Default value: 1<br>Minimum value = 1<br>Maximum value = 254</td></tr><tr><td>cost</td><td>&lt;Double></td><td>Read-write</td><td>Positive integer used by the routing algorithms to determine preference for this route. The lower the cost, the higher the preference.<br>Default value: 1<br>Minimum value = 0<br>Maximum value = 65535</td></tr><tr><td>advertise</td><td>&lt;String></td><td>Read-write</td><td>Advertise this route.<br>Possible values = DISABLED, ENABLED</td></tr><tr><td>msr</td><td>&lt;String></td><td>Read-write</td><td>Monitor this route with a monitor of type ND6 or PING.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>monitor</td><td>&lt;String></td><td>Read-write</td><td>Name of the monitor, of type ND6 or PING, configured on the NetScaler appliance to monitor this route.<br>Minimum length = 1</td></tr><tr><td>td</td><td>&lt;Double></td><td>Read-write</td><td>Integer value that uniquely identifies the traffic domain in which you want to configure the entity. If you do not specify an ID, the entity becomes part of the default traffic domain, which has an ID of 0.<br>Minimum value = 0<br>Maximum value = 4094</td></tr><tr><td>ownergroup</td><td>&lt;String></td><td>Read-write</td><td>The owner node group in a Cluster for this route6. If owner node group is not specified then the route is treated as Striped route.<br>Default value: DEFAULT_NG<br>Minimum length = 1</td></tr><tr><td>routetype</td><td>&lt;String></td><td>Read-write</td><td>Type of IPv6 routes to remove from the routing table of the NetScaler appliance.<br>Possible values = CONNECTED, STATIC, DYNAMIC, OSPF, ISIS, BGP, RIP, ND-RA-ROUTE, FIB6</td></tr><tr><td>detail</td><td>&lt;Boolean></td><td>Read-write</td><td>To get a detailed view.</td></tr><tr><td>gatewayname</td><td>&lt;String></td><td>Read-only</td><td>The name of the gateway for this route.</td></tr><tr><td>type</td><td>&lt;Boolean></td><td>Read-only</td><td>State of the RNAT.</td></tr><tr><td>dynamic</td><td>&lt;Boolean></td><td>Read-only</td><td>Whether this route is dynamically learned or not.</td></tr><tr><td>data</td><td>&lt;Boolean></td><td>Read-only</td><td>Internal data of this route.</td></tr><tr><td>flags</td><td>&lt;Boolean></td><td>Read-only</td><td>For a dynamic route, the routing protocol from which the route was learned.</td></tr><tr><td>state</td><td>&lt;Double></td><td>Read-only</td><td>Whether this route is UP or DOWN.</td></tr><tr><td>totalprobes</td><td>&lt;Double></td><td>Read-only</td><td>The total number of probes sent.</td></tr><tr><td>totalfailedprobes</td><td>&lt;Double></td><td>Read-only</td><td>The total number of failed probes.</td></tr><tr><td>failedprobes</td><td>&lt;Double></td><td>Read-only</td><td>Current number of failed monitoring probes.</td></tr><tr><td>monstatcode</td><td>&lt;Integer></td><td>Read-only</td><td>The code indicating the monitor response.</td></tr><tr><td>monstatparam1</td><td>&lt;Integer></td><td>Read-only</td><td>First parameter for use with message code.</td></tr><tr><td>monstatparam2</td><td>&lt;Integer></td><td>Read-only</td><td>Second parameter for use with message code.</td></tr><tr><td>monstatparam3</td><td>&lt;Integer></td><td>Read-only</td><td>Third parameter for use with message code.</td></tr><tr><td>data1</td><td>&lt;String></td><td>Read-only</td><td>Internal data of this route.<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>routeowners</td><td>&lt;String[]></td><td>Read-only</td><td>Use this option with -dynamic and in a cluster only to specify the set of nodes from which this dynamic route has been learnt.<br>Possible values = 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, 29, 30, 31</td></tr><tr><td>retain</td><td>&lt;Integer></td><td>Read-only</td><td>.</td></tr><tr><td>Static</td><td>&lt;Boolean></td><td>Read-only</td><td>Static route.</td></tr><tr><td>permanent</td><td>&lt;Boolean></td><td>Read-only</td><td>Permanent Route.</td></tr><tr><td>connected</td><td>&lt;Boolean></td><td>Read-only</td><td>Connected Route.</td></tr><tr><td>ospfv3</td><td>&lt;Boolean></td><td>Read-only</td><td>For a dynamic route, the routing protocol from which the route was learned.</td></tr><tr><td>isis</td><td>&lt;Boolean></td><td>Read-only</td><td>If this route is dynamic then which routing protocol was it learnt from.</td></tr><tr><td>active</td><td>&lt;Boolean></td><td>Read-only</td><td>For a dynamic route, the routing protocol from which the route was learned.</td></tr><tr><td>bgp</td><td>&lt;Boolean></td><td>Read-only</td><td>For a dynamic route, the routing protocol from which the route was learned.</td></tr><tr><td>rip</td><td>&lt;Boolean></td><td>Read-only</td><td>For a dynamic route, the routing protocol from which the route was learned.</td></tr><tr><td>raroute</td><td>&lt;Boolean></td><td>Read-only</td><td>For a dynamic route, the routing protocol from which the route was learned.</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD]()| [CLEAR](#)| [DELETE](#d)| [UPDATE](#u)| [UNSET](#)| [GET (ALL)](#get-)| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/route6
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"route6":{<b>"network":<String_value>,</b>"gateway":<String_value>,"vlan":<Double_value>,"vxlan":<Double_value>,"weight":<Double_value>,"distance":<Double_value>,"cost":<Double_value>,"advertise":<String_value>,"msr":<String_value>,"monitor":<String_value>,"td":<Double_value>,"ownergroup":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###clear



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/route6?<b>action=clear</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"route6":{<b>"routetype":<String_value></b>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/route6/network_value&lt;String&gt;
<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/route6
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"route6":{<b>"network":<String_value>,</b>"gateway":<String_value>,"vlan":<Double_value>,"vxlan":<Double_value>,"weight":<Double_value>,"distance":<Double_value>,"cost":<Double_value>,"advertise":<String_value>,"msr":<String_value>,"monitor":<String_value>,"td":<Double_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/route6?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"route6":{<b>"network":<String_value>,</b>"gateway":<String_value>,"vlan":<Double_value>,"vxlan":<Double_value>,"td":<Double_value>,"weight":true,"distance":true,"cost":true,"advertise":true,"msr":true,"monitor":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/route6
<b>Query-parameters:</b>
<b>args</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/route6?<b>args=network:&lt;String_value&gt;,gateway:&lt;String_value&gt;,vlan:&lt;Double_value&gt;,vxlan:&lt;Double_value&gt;,td:&lt;Double_value&gt;,routetype:&lt;String_value&gt;,detail:&lt;Boolean_value&gt;</b>
Use this query-parameter to get route6 resources based on additional properties.


<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/route6?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/route6?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of route6 resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/route6?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/route6?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the route6 resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "route6": [ {network:<String_value>,gateway:<String_value>,vlan:<Double_value>,vxlan:<Double_value>,td:<Double_value>,routetype:<String_value>,detail:<Boolean_value>"gatewayname":<String_value>,"advertise":<String_value>,"type":<Boolean_value>,"dynamic":<Boolean_value>,"weight":<Double_value>,"distance":<Double_value>,"cost":<Double_value>,"data":<Boolean_value>,"flags":<Boolean_value>,"msr":<String_value>,"monitor":<String_value>,"state":<Double_value>,"totalprobes":<Double_value>,"totalfailedprobes":<Double_value>,"failedprobes":<Double_value>,"monstatcode":<Integer_value>,"monstatparam1":<Integer_value>,"monstatparam2":<Integer_value>,"monstatparam3":<Integer_value>,"data1":<String_value>,"routeowners":<String[]_value>,"retain":<Integer_value>,"Static":<Boolean_value>,"permanent":<Boolean_value>,"connected":<Boolean_value>,"ospfv3":<Boolean_value>,"isis":<Boolean_value>,"active":<Boolean_value>,"bgp":<Boolean_value>,"rip":<Boolean_value>,"raroute":<Boolean_value>,"ownergroup":<String_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/route6?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "route6": [ { "__count": "#no"} ] }```



