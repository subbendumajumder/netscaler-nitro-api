#route

Configuration for route resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>network</td><td>&lt;String></td><td>Read-write</td><td>IPv4 network address for which to add a route entry in the routing table of the NetScaler appliance.</td><tr><tr><td>netmask</td><td>&lt;String></td><td>Read-write</td><td>The subnet mask associated with the network address.</td><tr><tr><td>gateway</td><td>&lt;String></td><td>Read-write</td><td>IP address of the gateway for this route. Can be either the IP address of the gateway, or can be null to specify a null interface route.&lt;br>Minimum length = 1</td><tr><tr><td>cost</td><td>&lt;Double></td><td>Read-write</td><td>Positive integer used by the routing algorithms to determine preference for using this route. The lower the cost, the higher the preference.&lt;br>Minimum value = 0&lt;br>Maximum value = 65535</td><tr><tr><td>td</td><td>&lt;Double></td><td>Read-write</td><td>Integer value that uniquely identifies the traffic domain in which you want to configure the entity. If you do not specify an ID, the entity becomes part of the default traffic domain, which has an ID of 0.&lt;br>Minimum value = 0&lt;br>Maximum value = 4094</td><tr><tr><td>distance</td><td>&lt;Double></td><td>Read-write</td><td>Administrative distance of this route, which determines the preference of this route over other routes, with same destination, from different routing protocols. A lower value is preferred.&lt;br>Default value: 1&lt;br>Minimum value = 0&lt;br>Maximum value = 255</td><tr><tr><td>cost1</td><td>&lt;Double></td><td>Read-write</td><td>The cost of a route is used to compare routes of the same type. The route having the lowest cost is the most preferred route. Possible values: 0 through 65535. Default: 0.&lt;br>Minimum value = 0&lt;br>Maximum value = 65535</td><tr><tr><td>weight</td><td>&lt;Double></td><td>Read-write</td><td>Positive integer used by the routing algorithms to determine preference for this route over others of equal cost. The lower the weight, the higher the preference.&lt;br>Default value: 1&lt;br>Minimum value = 1&lt;br>Maximum value = 65535</td><tr><tr><td>advertise</td><td>&lt;String></td><td>Read-write</td><td>Advertise this route.&lt;br>Possible values = DISABLED, ENABLED</td><tr><tr><td>protocol</td><td>&lt;String[]></td><td>Read-write</td><td>Routing protocol used for advertising this route.&lt;br>Default value: ADV_ROUTE_FLAGS&lt;br>Possible values = OSPF, ISIS, RIP, BGP</td><tr><tr><td>msr</td><td>&lt;String></td><td>Read-write</td><td>Monitor this route using a monitor of type ARP or PING.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>monitor</td><td>&lt;String></td><td>Read-write</td><td>Name of the monitor, of type ARP or PING, configured on the NetScaler appliance to monitor this route.&lt;br>Minimum length = 1</td><tr><tr><td>ownergroup</td><td>&lt;String></td><td>Read-write</td><td>The owner node group in a Cluster for this route. If owner node group is not specified then the route is treated as Striped route.&lt;br>Default value: DEFAULT_NG&lt;br>Minimum length = 1</td><tr><tr><td>routetype</td><td>&lt;String></td><td>Read-write</td><td>Protocol used by routes that you want to remove from the routing table of the NetScaler appliance.&lt;br>Possible values = CONNECTED, STATIC, DYNAMIC, OSPF, ISIS, RIP, BGP, VPATH</td><tr><tr><td>detail</td><td>&lt;Boolean></td><td>Read-write</td><td>Display a detailed view.</td><tr><tr><td>gatewayname</td><td>&lt;String></td><td>Read-only</td><td>The name of the gateway for this route. For a route other than a link load balancing (LLB) route, this value is null.</td><tr><tr><td>type</td><td>&lt;Boolean></td><td>Read-only</td><td>State of the RNAT.</td><tr><tr><td>dynamic</td><td>&lt;Boolean></td><td>Read-only</td><td>State of the route.</td><tr><tr><td>Static</td><td>&lt;Boolean></td><td>Read-only</td><td>.</td><tr><tr><td>permanent</td><td>&lt;Boolean></td><td>Read-only</td><td>.</td><tr><tr><td>direct</td><td>&lt;Boolean></td><td>Read-only</td><td>.</td><tr><tr><td>nat</td><td>&lt;Boolean></td><td>Read-only</td><td>.</td><tr><tr><td>lbroute</td><td>&lt;Boolean></td><td>Read-only</td><td>.</td><tr><tr><td>adv</td><td>&lt;Boolean></td><td>Read-only</td><td>.</td><tr><tr><td>tunnel</td><td>&lt;Boolean></td><td>Read-only</td><td>Show whether it is a tunnel route or not.</td><tr><tr><td>data</td><td>&lt;Boolean></td><td>Read-only</td><td>Internal data of this route.</td><tr><tr><td>data0</td><td>&lt;Boolean></td><td>Read-only</td><td>Internal route type is stored, used for get.</td><tr><tr><td>flags</td><td>&lt;Boolean></td><td>Read-only</td><td>If this route is dynamic, the name of the routing protocol from which it was learned.</td><tr><tr><td>routeowners</td><td>&lt;String[]></td><td>Read-only</td><td>Use this option with -dynamic and in a cluster only to specify the set of nodes from which this dynamic route has been learnt.&lt;br>Possible values = 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, 29, 30, 31</td><tr><tr><td>retain</td><td>&lt;Integer></td><td>Read-only</td><td>.</td><tr><tr><td>ospf</td><td>&lt;Boolean></td><td>Read-only</td><td>OSPF protocol.</td><tr><tr><td>isis</td><td>&lt;Boolean></td><td>Read-only</td><td>ISIS protocol.</td><tr><tr><td>rip</td><td>&lt;Boolean></td><td>Read-only</td><td>RIP protocol.</td><tr><tr><td>bgp</td><td>&lt;Boolean></td><td>Read-only</td><td>BGP protocol.</td><tr><tr><td>dhcp</td><td>&lt;Boolean></td><td>Read-only</td><td>.</td><tr><tr><td>advospf</td><td>&lt;Boolean></td><td>Read-only</td><td>Advertised through OSPF protocol.</td><tr><tr><td>advisis</td><td>&lt;Boolean></td><td>Read-only</td><td>Advertised through ISIS protocol.</td><tr><tr><td>advrip</td><td>&lt;Boolean></td><td>Read-only</td><td>Advertised through RIP protocol.</td><tr><tr><td>advbgp</td><td>&lt;Boolean></td><td>Read-only</td><td>Advertised through BGP protocol.</td><tr><tr><td>state</td><td>&lt;Double></td><td>Read-only</td><td>The state of the static route. Possible values: UP, DOWN.</td><tr><tr><td>totalprobes</td><td>&lt;Double></td><td>Read-only</td><td>The total number of probes sent.</td><tr><tr><td>totalfailedprobes</td><td>&lt;Double></td><td>Read-only</td><td>The total number of failed probes.</td><tr><tr><td>failedprobes</td><td>&lt;Double></td><td>Read-only</td><td>Number of the current failed monitoring probes.</td><tr><tr><td>monstatcode</td><td>&lt;Integer></td><td>Read-only</td><td>The code indicating the monitor response.</td><tr><tr><td>monstatparam1</td><td>&lt;Integer></td><td>Read-only</td><td>First parameter used with the message code.</td><tr><tr><td>monstatparam2</td><td>&lt;Integer></td><td>Read-only</td><td>Second parameter used with the message code.</td><tr><tr><td>monstatparam3</td><td>&lt;Integer></td><td>Read-only</td><td>Third parameter used with the message code.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [CLEAR](#clear) | [DELETE](#delete) | [UPDATE](#update) | [UNSET](#unset) | [GET (ALL)](#get-(all)) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>},"sessionid":"##sessionid","route":{      "network":<String_value>,      "netmask":<String_value>,      "gateway":<String_value>,      "cost":<Double_value>,      "td":<Double_value>,      "distance":<Double_value>,      "cost1":<Double_value>,      "weight":<Double_value>,      "advertise":<String_value>,      "protocol":<String[]_value>,      "msr":<String_value>,                  "monitor":<String_value>,      "ownergroup":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###clear



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"clear"},"sessionid":"##sessionid","route":{      "routetype":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/route/network_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/route/network_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","route":{      "network":<String_value>,      "netmask":<String_value>,      "gateway":<String_value>,      "td":<Double_value>,      "distance":<Double_value>,      "cost1":<Double_value>,      "weight":<Double_value>,      "advertise":<String_value>,      "protocol":<String[]_value>,      "msr":<String_value>,                  "monitor":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","route":{      "network":<String_value>,      "netmask":<String_value>,      "gateway":<String_value>,      "td":<Double_value>,      "advertise":true,      "distance":true,      "cost1":true,      "weight":true,      "protocol":true,      "msr":true,      "monitor":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/route
Query-parameters:
args
http://&lt;NSIP&gt;/nitro/v1/config/route?args=      "network":&lt;String_value&gt;,                  "netmask":&lt;String_value&gt;,                  "gateway":&lt;String_value&gt;,                  "td":&lt;Double_value&gt;,      "routetype":&lt;String_value&gt;,      "detail":&lt;Boolean_value&gt;,
Use this query-parameter to get route resources based on additional properties.


filter
http://&lt;NSIP&gt;/nitro/v1/config/route?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of route resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/route?view=summary
Use this query-parameter to get the summary output of route resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/route?pagesize=#no;pageno=#no
Use this query-parameter to get the route resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/route?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "route": [ {      "network":<String_value>,                  "netmask":<String_value>,                  "gateway":<String_value>,                  "td":<Double_value>,      "routetype":<String_value>,      "detail":<Boolean_value>,      "gatewayname":<String_value>,      "advertise":<String_value>,      "type":<Boolean_value>,      "dynamic":<Boolean_value>,      "Static":<Boolean_value>,      "permanent":<Boolean_value>,      "direct":<Boolean_value>,      "nat":<Boolean_value>,      "lbroute":<Boolean_value>,      "adv":<Boolean_value>,      "tunnel":<Boolean_value>,      "cost":<Double_value>,      "distance":<Double_value>,      "cost1":<Double_value>,      "weight":<Double_value>,      "protocol":<String[]_value>,      "data":<Boolean_value>,      "data0":<Boolean_value>,      "flags":<Boolean_value>,      "routeowners":<String[]_value>,      "retain":<Integer_value>,      "ospf":<Boolean_value>,      "isis":<Boolean_value>,      "rip":<Boolean_value>,      "bgp":<Boolean_value>,      "dhcp":<Boolean_value>,      "advospf":<Boolean_value>,      "advisis":<Boolean_value>,      "advrip":<Boolean_value>,      "advbgp":<Boolean_value>,      "msr":<String_value>,      "monitor":<String_value>,      "state":<Double_value>,      "totalprobes":<Double_value>,      "totalfailedprobes":<Double_value>,      "failedprobes":<Double_value>,      "monstatcode":<Integer_value>,      "monstatparam1":<Integer_value>,      "monstatparam2":<Integer_value>,      "monstatparam3":<Integer_value>,      "ownergroup":<String_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/route?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",route: [ { "__count": "#no"} ] }


