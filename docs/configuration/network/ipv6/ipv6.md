#ipv6

Configuration for ip v6 resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>ralearning</td><td>&lt;String></td><td>Read-write</td><td>Enable the NetScaler appliance to learn about various routes from Router Advertisement (RA) and Router Solicitation (RS) messages sent by the routers.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>routerredirection</td><td>&lt;String></td><td>Read-write</td><td>Enable the NetScaler appliance to do Router Redirection.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>ndbasereachtime</td><td>&lt;Double></td><td>Read-write</td><td>Base reachable time of the Neighbor Discovery (ND6) protocol. The time, in milliseconds, that the NetScaler appliance assumes an adjacent device is reachable after receiving a reachability confirmation.&lt;br>Default value: 30000&lt;br>Minimum value = 1</td><tr><tr><td>ndretransmissiontime</td><td>&lt;Double></td><td>Read-write</td><td>Retransmission time of the Neighbor Discovery (ND6) protocol. The time, in milliseconds, between retransmitted Neighbor Solicitation (NS) messages, to an adjacent device.&lt;br>Default value: 1000&lt;br>Minimum value = 1</td><tr><tr><td>natprefix</td><td>&lt;String></td><td>Read-write</td><td>Prefix used for translating packets from private IPv6 servers to IPv4 packets. This prefix has a length of 96 bits (128-32 = 96). The IPv6 servers embed the destination IP address of the IPv4 servers or hosts in the last 32 bits of the destination IP address field of the IPv6 packets. The first 96 bits of the destination IP address field are set as the IPv6 NAT prefix. IPv6 packets addressed to this prefix have to be routed to the NetScaler appliance to ensure that the IPv6-IPv4 translation is done by the appliance.</td><tr><tr><td>td</td><td>&lt;Double></td><td>Read-write</td><td>Integer value that uniquely identifies the traffic domain in which you want to configure the entity. If you do not specify an ID, the entity becomes part of the default traffic domain, which has an ID of 0.&lt;br>Minimum value = 0&lt;br>Maximum value = 4094</td><tr><tr><td>dodad</td><td>&lt;String></td><td>Read-write</td><td>Enable the NetScaler appliance to do Duplicate Address Detection (DAD) for all the NetScaler owned IPv6 addresses regardless of whether they are obtained through stateless auto configuration, DHCPv6, or manual configuration.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>basereachtime</td><td>&lt;Integer></td><td>Read-only</td><td>ND6 base reachable time (ms).</td><tr><tr><td>reachtime</td><td>&lt;Integer></td><td>Read-only</td><td>ND6 computed reachable time (ms).</td><tr><tr><td>ndreachtime</td><td>&lt;Double></td><td>Read-only</td><td>ND6 computed reachable time (ms).</td><tr><tr><td>retransmissiontime</td><td>&lt;Integer></td><td>Read-only</td><td>ND6 retransmission time (ms).</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[UPDATE](#update) | [UNSET](#unset) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","ipv6":{      "ralearning":<String_value>,      "routerredirection":<String_value>,      "ndbasereachtime":<Double_value>,      "ndretransmissiontime":<Double_value>,      "natprefix":<String_value>,                  "td":<Double_value>,      "dodad":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","ipv6":{      "ralearning":true,      "routerredirection":true,      "ndbasereachtime":true,      "ndretransmissiontime":true,      "natprefix":true,                  "td":<Double_value>,      "dodad":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/ipv6
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/ipv6?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of ipv6 resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/ipv6?view=summary
Use this query-parameter to get the summary output of ipv6 resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/ipv6?pagesize=#no;pageno=#no
Use this query-parameter to get the ipv6 resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/ipv6?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "ipv6": [ {      "td":<Double_value>,      "ralearning":<String_value>,      "routerredirection":<String_value>,      "basereachtime":<Integer_value>,      "ndbasereachtime":<Double_value>,      "reachtime":<Integer_value>,      "ndreachtime":<Double_value>,      "retransmissiontime":<Integer_value>,      "ndretransmissiontime":<Double_value>,      "natprefix":<String_value>,      "dodad":<String_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/ipv6/td_value&lt;Double&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "ipv6": [ {      "td":<Double_value>,      "ralearning":<String_value>,      "routerredirection":<String_value>,      "basereachtime":<Integer_value>,      "ndbasereachtime":<Double_value>,      "reachtime":<Integer_value>,      "ndreachtime":<Double_value>,      "retransmissiontime":<Integer_value>,      "ndretransmissiontime":<Double_value>,      "natprefix":<String_value>,      "dodad":<String_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/ipv6?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",ipv6: [ { "__count": "#no"} ] }


