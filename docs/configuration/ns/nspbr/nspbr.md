#nspbr

Configuration for Policy Based Routing(PBR) entry resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the PBR. Must begin with an ASCII alphabetic or underscore \\(_\\) character, and must contain only ASCII alphanumeric, underscore, hash \\(\\#\\), period \\(.\\), space, colon \\(:\\), at \\(@\\), equals \\(=\\), and hyphen \\(-\\) characters. Cannot be changed after the PBR is created.&lt;br>Minimum length = 1</td><tr><tr><td>action</td><td>&lt;String></td><td>Read-write</td><td>Action to perform on the outgoing IPv4 packets that match the PBR. Available settings function as follows: * ALLOW - The NetScaler appliance sends the packet to the designated next-hop router. * DENY - The NetScaler appliance applies the routing table for normal destination-based routing.&lt;br>Possible values = ALLOW, DENY</td><tr><tr><td>td</td><td>&lt;Double></td><td>Read-write</td><td>Integer value that uniquely identifies the traffic domain in which you want to configure the entity. If you do not specify an ID, the entity becomes part of the default traffic domain, which has an ID of 0.&lt;br>Minimum value = 0&lt;br>Maximum value = 4094</td><tr><tr><td>srcip</td><td>&lt;Boolean></td><td>Read-write</td><td>IP address or range of IP addresses to match against the source IP address of an outgoing IPv4 packet. In the command line interface, separate the range with a hyphen and enclose within brackets. For example: [10.102.29.30-10.102.29.189].</td><tr><tr><td>srcipop</td><td>&lt;String></td><td>Read-write</td><td>Either the equals (=) or does not equal (!=) logical operator.&lt;br>Possible values = =, !=, EQ, NEQ</td><tr><tr><td>srcipval</td><td>&lt;String></td><td>Read-write</td><td>IP address or range of IP addresses to match against the source IP address of an outgoing IPv4 packet. In the command line interface, separate the range with a hyphen and enclose within brackets. For example: [10.102.29.30-10.102.29.189].</td><tr><tr><td>srcport</td><td>&lt;Boolean></td><td>Read-write</td><td>Port number or range of port numbers to match against the source port number of an outgoing IPv4 packet. In the command line interface, separate the range with a hyphen and enclose within brackets. For example: [40-90]. Note: The destination port can be specified only for TCP and UDP protocols.</td><tr><tr><td>srcportop</td><td>&lt;String></td><td>Read-write</td><td>Logical operator.&lt;br>Possible values = =, !=, EQ, NEQ</td><tr><tr><td>srcportval</td><td>&lt;String></td><td>Read-write</td><td>Port number or range of port numbers to match against the source port number of an outgoing IPv4 packet. In the command line interface, separate the range with a hyphen and enclose within brackets. For example: [40-90]. Note: The destination port can be specified only for TCP and UDP protocols.&lt;br>Maximum length = 65535</td><tr><tr><td>destip</td><td>&lt;Boolean></td><td>Read-write</td><td>IP address or range of IP addresses to match against the destination IP address of an outgoing IPv4 packet. In the command line interface, separate the range with a hyphen and enclose within brackets. For example: [10.102.29.30-10.102.29.189].</td><tr><tr><td>destipop</td><td>&lt;String></td><td>Read-write</td><td>Logical operator.&lt;br>Possible values = =, !=, EQ, NEQ</td><tr><tr><td>destipval</td><td>&lt;String></td><td>Read-write</td><td>IP address or range of IP addresses to match against the destination IP address of an outgoing IPv4 packet. In the command line interface, separate the range with a hyphen and enclose within brackets. For example: [10.102.29.30-10.102.29.189].</td><tr><tr><td>destport</td><td>&lt;Boolean></td><td>Read-write</td><td>Port number or range of port numbers to match against the destination port number of an outgoing IPv4 packet. In the command line interface, separate the range with a hyphen and enclose within brackets. For example: [40-90]. Note: The destination port can be specified only for TCP and UDP protocols.</td><tr><tr><td>destportop</td><td>&lt;String></td><td>Read-write</td><td>Logical operator.&lt;br>Possible values = =, !=, EQ, NEQ</td><tr><tr><td>destportval</td><td>&lt;String></td><td>Read-write</td><td>Port number or range of port numbers to match against the destination port number of an outgoing IPv4 packet. In the command line interface, separate the range with a hyphen and enclose within brackets. For example: [40-90]. Note: The destination port can be specified only for TCP and UDP protocols.&lt;br>Maximum length = 65535</td><tr><tr><td>nexthop</td><td>&lt;Boolean></td><td>Read-write</td><td>IP address of the next hop router or the name of the link load balancing virtual server to which to send matching packets if action is set to ALLOW. If you specify a link load balancing (LLB) virtual server, which can provide a backup if a next hop link fails, first make sure that the next hops bound to the LLB virtual server are actually next hops that are directly connected to the NetScaler appliance. Otherwise, the NetScaler throws an error when you attempt to create the PBR.</td><tr><tr><td>nexthopval</td><td>&lt;String></td><td>Read-write</td><td>The Next Hop IP address or gateway name.</td><tr><tr><td>iptunnel</td><td>&lt;Boolean></td><td>Read-write</td><td>The Tunnel name.</td><tr><tr><td>iptunnelname</td><td>&lt;String></td><td>Read-write</td><td>The iptunnel name where packets need to be forwarded upon.</td><tr><tr><td>srcmac</td><td>&lt;String></td><td>Read-write</td><td>MAC address to match against the source MAC address of an outgoing IPv4 packet.</td><tr><tr><td>srcmacmask</td><td>&lt;String></td><td>Read-write</td><td>Used to define range of Source MAC address. It takes string of 0 and 1, 0s are for exact match and 1s for wildcard. For matching first 3 bytes of MAC address, srcMacMask value "000000111111". .&lt;br>Default value: "000000000000"</td><tr><tr><td>protocol</td><td>&lt;String></td><td>Read-write</td><td>Protocol, identified by protocol name, to match against the protocol of an outgoing IPv4 packet.&lt;br>Possible values = ICMP, IGMP, TCP, EGP, IGP, ARGUS, UDP, RDP, RSVP, EIGRP, L2TP, ISIS</td><tr><tr><td>protocolnumber</td><td>&lt;Double></td><td>Read-write</td><td>Protocol, identified by protocol number, to match against the protocol of an outgoing IPv4 packet.&lt;br>Minimum value = 1&lt;br>Maximum value = 255</td><tr><tr><td>vlan</td><td>&lt;Double></td><td>Read-write</td><td>ID of the VLAN. The NetScaler appliance compares the PBR only to the outgoing packets on the specified VLAN. If you do not specify any interface ID, the appliance compares the PBR to the outgoing packets on all VLANs.&lt;br>Minimum value = 1&lt;br>Maximum value = 4094</td><tr><tr><td>vxlan</td><td>&lt;Double></td><td>Read-write</td><td>ID of the VXLAN. The NetScaler appliance compares the PBR only to the outgoing packets on the specified VXLAN. If you do not specify any interface ID, the appliance compares the PBR to the outgoing packets on all VXLANs.&lt;br>Minimum value = 1&lt;br>Maximum value = 16777215</td><tr><tr><td>Interface</td><td>&lt;String></td><td>Read-write</td><td>ID of an interface. The NetScaler appliance compares the PBR only to the outgoing packets on the specified interface. If you do not specify any value, the appliance compares the PBR to the outgoing packets on all interfaces.</td><tr><tr><td>priority</td><td>&lt;Double></td><td>Read-write</td><td>Priority of the PBR, which determines the order in which it is evaluated relative to the other PBRs. If you do not specify priorities while creating PBRs, the PBRs are evaluated in the order in which they are created.&lt;br>Minimum value = 1&lt;br>Maximum value = 81920</td><tr><tr><td>msr</td><td>&lt;String></td><td>Read-write</td><td>Monitor the route specified byte Next Hop parameter. This parameter is not applicable if you specify a link load balancing (LLB) virtual server name with the Next Hop parameter.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>monitor</td><td>&lt;String></td><td>Read-write</td><td>The name of the monitor.(Can be only of type ping or ARP ).&lt;br>Minimum length = 1</td><tr><tr><td>state</td><td>&lt;String></td><td>Read-write</td><td>Enable or disable the PBR. After you apply the PBRs, the NetScaler appliance compares outgoing packets to the enabled PBRs.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>detail</td><td>&lt;Boolean></td><td>Read-write</td><td>To get a detailed view.</td><tr><tr><td>hits</td><td>&lt;Double></td><td>Read-only</td><td>The hits of this PBR.</td><tr><tr><td>kernelstate</td><td>&lt;String></td><td>Read-only</td><td>The commit status of the PBR.&lt;br>Default value: NOTAPPLIED&lt;br>Possible values = APPLIED, NOTAPPLIED, RE-APPLY, SFAPPLIED, SFNOTAPPLIED, SFAPPLIED61, SFNOTAPPLIED61</td><tr><tr><td>curstate</td><td>&lt;Double></td><td>Read-only</td><td>If this route is UP/DOWN.</td><tr><tr><td>totalprobes</td><td>&lt;Double></td><td>Read-only</td><td>The total number of probes sent.</td><tr><tr><td>totalfailedprobes</td><td>&lt;Double></td><td>Read-only</td><td>The total number of failed probes.</td><tr><tr><td>failedprobes</td><td>&lt;Double></td><td>Read-only</td><td>Number of the current failed monitoring probes.</td><tr><tr><td>monstatcode</td><td>&lt;Integer></td><td>Read-only</td><td>The code indicating the monitor response.</td><tr><tr><td>monstatparam1</td><td>&lt;Integer></td><td>Read-only</td><td>First parameter for use with message code.</td><tr><tr><td>monstatparam2</td><td>&lt;Integer></td><td>Read-only</td><td>Second parameter for use with message code.</td><tr><tr><td>monstatparam3</td><td>&lt;Integer></td><td>Read-only</td><td>Third parameter for use with message code.</td><tr><tr><td>data</td><td>&lt;Boolean></td><td>Read-only</td><td>Internal data of this route.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [DELETE](#delete) | [UPDATE](#update) | [UNSET](#unset) | [ENABLE](#enable) | [DISABLE](#disable) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>},"sessionid":"##sessionid","nspbr":{      "name":<String_value>,      "action":<String_value>,      "td":<Double_value>,      "srcip":<Boolean_value>,                  "srcipop":<String_value>,                  "srcipval":<String_value>,      "srcport":<Boolean_value>,                  "srcportop":<String_value>,                  "srcportval":<String_value>,      "destip":<Boolean_value>,                  "destipop":<String_value>,                  "destipval":<String_value>,      "destport":<Boolean_value>,                  "destportop":<String_value>,                  "destportval":<String_value>,      "nexthop":<Boolean_value>,                  "nexthopval":<String_value>,      "iptunnel":<Boolean_value>,                  "iptunnelname":<String_value>,      "srcmac":<String_value>,                  "srcmacmask":<String_value>,      "protocol":<String_value>,      "protocolnumber":<Double_value>,      "vlan":<Double_value>,      "vxlan":<Double_value>,      "Interface":<String_value>,      "priority":<Double_value>,      "msr":<String_value>,                  "monitor":<String_value>,      "state":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/nspbr/name_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/nspbr/name_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","nspbr":{      "name":<String_value>,      "action":<String_value>,      "srcip":<Boolean_value>,                  "srcipop":<String_value>,                  "srcipval":<String_value>,      "srcport":<Boolean_value>,                  "srcportop":<String_value>,                  "srcportval":<String_value>,      "destip":<Boolean_value>,                  "destipop":<String_value>,                  "destipval":<String_value>,      "destport":<Boolean_value>,                  "destportop":<String_value>,                  "destportval":<String_value>,      "nexthop":<Boolean_value>,                  "nexthopval":<String_value>,      "iptunnel":<Boolean_value>,                  "iptunnelname":<String_value>,      "srcmac":<String_value>,                  "srcmacmask":<String_value>,      "protocol":<String_value>,      "protocolnumber":<Double_value>,      "vlan":<Double_value>,      "vxlan":<Double_value>,      "Interface":<String_value>,      "priority":<Double_value>,      "msr":<String_value>,                  "monitor":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","nspbr":{      "name":<String_value>,      "srcip":true,      "srcport":true,      "destip":true,      "destport":true,      "nexthop":true,      "iptunnel":true,      "srcmac":true,      "srcmacmask":true,      "protocol":true,      "vlan":true,      "vxlan":true,      "Interface":true,      "msr":true,      "monitor":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###enable



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"enable"},"sessionid":"##sessionid","nspbr":{      "name":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###disable



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"disable"},"sessionid":"##sessionid","nspbr":{      "name":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/nspbr
Query-parameters:
args
http://&lt;NSIP&gt;/nitro/v1/config/nspbr?args=      "name":&lt;String_value&gt;,      "detail":&lt;Boolean_value&gt;,
Use this query-parameter to get nspbr resources based on additional properties.


filter
http://&lt;NSIP&gt;/nitro/v1/config/nspbr?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of nspbr resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/nspbr?view=summary
Use this query-parameter to get the summary output of nspbr resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/nspbr?pagesize=#no;pageno=#no
Use this query-parameter to get the nspbr resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/nspbr?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "nspbr": [ {      "name":<String_value>,      "detail":<Boolean_value>,      "action":<String_value>,      "srcmac":<String_value>,      "srcmacmask":<String_value>,      "protocol":<String_value>,      "protocolnumber":<Double_value>,      "srcportval":<String_value>,      "td":<Double_value>,      "destportval":<String_value>,      "srcipval":<String_value>,      "destipval":<String_value>,      "vlan":<Double_value>,      "vxlan":<Double_value>,      "state":<String_value>,      "Interface":<String_value>,      "hits":<Double_value>,      "priority":<Double_value>,      "srcipop":<String_value>,      "destipop":<String_value>,      "srcportop":<String_value>,      "destportop":<String_value>,      "kernelstate":<String_value>,      "nexthopval":<String_value>,      "iptunnelname":<String_value>,      "msr":<String_value>,      "monitor":<String_value>,      "curstate":<Double_value>,      "totalprobes":<Double_value>,      "totalfailedprobes":<Double_value>,      "failedprobes":<Double_value>,      "monstatcode":<Integer_value>,      "monstatparam1":<Integer_value>,      "monstatparam2":<Integer_value>,      "monstatparam3":<Integer_value>,      "data":<Boolean_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/nspbr/name_value&lt;String&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "nspbr": [ {      "name":<String_value>,      "detail":<Boolean_value>,      "action":<String_value>,      "srcmac":<String_value>,      "srcmacmask":<String_value>,      "protocol":<String_value>,      "protocolnumber":<Double_value>,      "srcportval":<String_value>,      "td":<Double_value>,      "destportval":<String_value>,      "srcipval":<String_value>,      "destipval":<String_value>,      "vlan":<Double_value>,      "vxlan":<Double_value>,      "state":<String_value>,      "Interface":<String_value>,      "hits":<Double_value>,      "priority":<Double_value>,      "srcipop":<String_value>,      "destipop":<String_value>,      "srcportop":<String_value>,      "destportop":<String_value>,      "kernelstate":<String_value>,      "nexthopval":<String_value>,      "iptunnelname":<String_value>,      "msr":<String_value>,      "monitor":<String_value>,      "curstate":<Double_value>,      "totalprobes":<Double_value>,      "totalfailedprobes":<Double_value>,      "failedprobes":<Double_value>,      "monstatcode":<Integer_value>,      "monstatparam1":<Integer_value>,      "monstatparam2":<Integer_value>,      "monstatparam3":<Integer_value>,      "data":<Boolean_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/nspbr?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",nspbr: [ { "__count": "#no"} ] }


