#nsacl6

Configuration for ACL6 entry resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>acl6name</td><td>&lt;String></td><td>Read-write</td><td>Name for the ACL6 rule. Must begin with an ASCII alphabetic or underscore (_) character, and must contain only ASCII alphanumeric, underscore, hash (#), period (.), space, colon (:), at (@), equals (=), and hyphen (-) characters. Cannot be changed after the ACL6 rule is created.&lt;br>Minimum length = 1</td><tr><tr><td>acl6action</td><td>&lt;String></td><td>Read-write</td><td>Action to perform on the incoming IPv6 packets that match the ACL6 rule.&lt;br>Available settings function as follows:&lt;br>* ALLOW - The NetScaler appliance processes the packet.&lt;br>* BRIDGE - The NetScaler appliance bridges the packet to the destination without processing it.&lt;br>* DENY - The NetScaler appliance drops the packet.&lt;br>Possible values = BRIDGE, DENY, ALLOW</td><tr><tr><td>td</td><td>&lt;Double></td><td>Read-write</td><td>Integer value that uniquely identifies the traffic domain in which you want to configure the entity. If you do not specify an ID, the entity becomes part of the default traffic domain, which has an ID of 0.&lt;br>Minimum value = 0&lt;br>Maximum value = 4094</td><tr><tr><td>srcipv6</td><td>&lt;Boolean></td><td>Read-write</td><td>IP address or range of IP addresses to match against the source IP address of an incoming IPv6 packet. In the command line interface, separate the range with a hyphen and enclose within brackets.</td><tr><tr><td>srcipop</td><td>&lt;String></td><td>Read-write</td><td>Logical operator.&lt;br>Possible values = =, !=, EQ, NEQ</td><tr><tr><td>srcipv6val</td><td>&lt;String></td><td>Read-write</td><td>Source IPv6 address (range).</td><tr><tr><td>srcport</td><td>&lt;Boolean></td><td>Read-write</td><td>Port number or range of port numbers to match against the source port number of an incoming IPv6 packet. In the command line interface, separate the range with a hyphen and enclose within brackets. For example: [40-90].&lt;br>&lt;br>Note: The destination port can be specified only for TCP and UDP protocols.</td><tr><tr><td>srcportop</td><td>&lt;String></td><td>Read-write</td><td>Logical operator.&lt;br>Possible values = =, !=, EQ, NEQ</td><tr><tr><td>srcportval</td><td>&lt;String></td><td>Read-write</td><td>Source port (range).&lt;br>Maximum length = 65535</td><tr><tr><td>destipv6</td><td>&lt;Boolean></td><td>Read-write</td><td>IP address or range of IP addresses to match against the destination IP address of an incoming IPv6 packet. In the command line interface, separate the range with a hyphen and enclose within brackets.</td><tr><tr><td>destipop</td><td>&lt;String></td><td>Read-write</td><td>Logical operator.&lt;br>Possible values = =, !=, EQ, NEQ</td><tr><tr><td>destipv6val</td><td>&lt;String></td><td>Read-write</td><td>Destination IPv6 address (range).</td><tr><tr><td>destport</td><td>&lt;Boolean></td><td>Read-write</td><td>Port number or range of port numbers to match against the destination port number of an incoming IPv6 packet. In the command line interface, separate the range with a hyphen and enclose within brackets. For example: [40-90].&lt;br>&lt;br>Note: The destination port can be specified only for TCP and UDP protocols.</td><tr><tr><td>destportop</td><td>&lt;String></td><td>Read-write</td><td>Logical operator.&lt;br>Possible values = =, !=, EQ, NEQ</td><tr><tr><td>destportval</td><td>&lt;String></td><td>Read-write</td><td>Destination port (range).&lt;br>Maximum length = 65535</td><tr><tr><td>ttl</td><td>&lt;Double></td><td>Read-write</td><td>Time to expire this ACL6 (in seconds).&lt;br>Minimum value = 1&lt;br>Maximum value = 2147483647</td><tr><tr><td>srcmac</td><td>&lt;String></td><td>Read-write</td><td>MAC address to match against the source MAC address of an incoming IPv6 packet.</td><tr><tr><td>srcmacmask</td><td>&lt;String></td><td>Read-write</td><td>Used to define range of Source MAC address. It takes string of 0 and 1, 0s are for exact match and 1s for wildcard. For matching first 3 bytes of MAC address, srcMacMask value "000000111111". .&lt;br>Default value: "000000000000"</td><tr><tr><td>protocol</td><td>&lt;String></td><td>Read-write</td><td>Protocol, identified by protocol name, to match against the protocol of an incoming IPv6 packet.&lt;br>Possible values = ICMPV6, TCP, UDP</td><tr><tr><td>protocolnumber</td><td>&lt;Double></td><td>Read-write</td><td>Protocol, identified by protocol number, to match against the protocol of an incoming IPv6 packet.&lt;br>Minimum value = 1&lt;br>Maximum value = 255</td><tr><tr><td>vlan</td><td>&lt;Double></td><td>Read-write</td><td>ID of the VLAN. The NetScaler appliance applies the ACL6 rule only to the incoming packets on the specified VLAN. If you do not specify a VLAN ID, the appliance applies the ACL6 rule to the incoming packets on all VLANs.&lt;br>Minimum value = 1&lt;br>Maximum value = 4094</td><tr><tr><td>vxlan</td><td>&lt;Double></td><td>Read-write</td><td>ID of the VXLAN. The NetScaler appliance applies the ACL6 rule only to the incoming packets on the specified VXLAN. If you do not specify a VXLAN ID, the appliance applies the ACL6 rule to the incoming packets on all VXLANs.&lt;br>Minimum value = 1&lt;br>Maximum value = 16777215</td><tr><tr><td>Interface</td><td>&lt;String></td><td>Read-write</td><td>ID of an interface. The NetScaler appliance applies the ACL6 rule only to the incoming packets from the specified interface. If you do not specify any value, the appliance applies the ACL6 rule to the incoming packets from all interfaces.</td><tr><tr><td>established</td><td>&lt;Boolean></td><td>Read-write</td><td>Allow only incoming TCP packets that have the ACK or RST bit set if the action set for the ACL6 rule is ALLOW and these packets match the other conditions in the ACL6 rule.</td><tr><tr><td>icmptype</td><td>&lt;Double></td><td>Read-write</td><td>ICMP Message type to match against the message type of an incoming IPv6 ICMP packet. For example, to block DESTINATION UNREACHABLE messages, you must specify 3 as the ICMP type.&lt;br>&lt;br>Note: This parameter can be specified only for the ICMP protocol.&lt;br>Minimum value = 0&lt;br>Maximum value = 65536</td><tr><tr><td>icmpcode</td><td>&lt;Double></td><td>Read-write</td><td>Code of a particular ICMP message type to match against the ICMP code of an incoming IPv6 ICMP packet. For example, to block DESTINATION HOST UNREACHABLE messages, specify 3 as the ICMP type and 1 as the ICMP code.&lt;br>&lt;br>If you set this parameter, you must set the ICMP Type parameter.&lt;br>Minimum value = 0&lt;br>Maximum value = 65536</td><tr><tr><td>priority</td><td>&lt;Double></td><td>Read-write</td><td>Priority for the ACL6 rule, which determines the order in which it is evaluated relative to the other ACL6 rules. If you do not specify priorities while creating ACL6 rules, the ACL6 rules are evaluated in the order in which they are created.&lt;br>Minimum value = 1&lt;br>Maximum value = 80000</td><tr><tr><td>state</td><td>&lt;String></td><td>Read-write</td><td>State of the ACL6.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>aclaction</td><td>&lt;String></td><td>Read-write</td><td>Action associated with the ACL6.&lt;br>Possible values = BRIDGE, DENY, ALLOW</td><tr><tr><td>newname</td><td>&lt;String></td><td>Read-write</td><td>New name for the ACL6 rule. Must begin with an ASCII alphabetic or underscore \\(_\\) character, and must contain only ASCII alphanumeric, underscore, hash \\(\\#\\), period \\(.\\), space, colon \\(:\\), at \\(@\\), equals \\(=\\), and hyphen \\(-\\) characters.&lt;br>Minimum length = 1</td><tr><tr><td>kernelstate</td><td>&lt;String></td><td>Read-only</td><td>Commit status of the ACL6.&lt;br>Default value: NOTAPPLIED&lt;br>Possible values = APPLIED, NOTAPPLIED, RE-APPLY, SFAPPLIED, SFNOTAPPLIED</td><tr><tr><td>hits</td><td>&lt;Double></td><td>Read-only</td><td>Number of hits of this ACL6.</td><tr><tr><td>aclassociate</td><td>&lt;String[]></td><td>Read-only</td><td>ACL6 linked.&lt;br>Possible values = NAT, FORWARDINGSESSION, NAT64, LSN</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [DELETE](#delete) | [UPDATE](#update) | [UNSET](#unset) | [ENABLE](#enable) | [DISABLE](#disable) | [RENAME](#rename) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsacl6
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"nsacl6":{      "acl6name":<String_value>,      "acl6action":<String_value>,      "td":<Double_value>,      "srcipv6":<Boolean_value>,      "srcipop":<String_value>,      "srcipv6val":<String_value>,      "srcport":<Boolean_value>,      "srcportop":<String_value>,      "srcportval":<String_value>,      "destipv6":<Boolean_value>,      "destipop":<String_value>,      "destipv6val":<String_value>,      "destport":<Boolean_value>,      "destportop":<String_value>,      "destportval":<String_value>,      "ttl":<Double_value>,      "srcmac":<String_value>,      "srcmacmask":<String_value>,      "protocol":<String_value>,      "protocolnumber":<Double_value>,      "vlan":<Double_value>,      "vxlan":<Double_value>,      "Interface":<String_value>,      "established":<Boolean_value>,      "icmptype":<Double_value>,      "icmpcode":<Double_value>,      "priority":<Double_value>,      "state":<String_value>}}```
Response:
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsacl6/acl6name_value&lt;String&gt;
HTTP Method: DELETE
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsacl6
HTTP Method: PUT
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"nsacl6":{      "acl6name":<String_value>,      "aclaction":<String_value>,      "srcipv6":<Boolean_value>,      "srcipop":<String_value>,      "srcipv6val":<String_value>,      "srcport":<Boolean_value>,      "srcportop":<String_value>,      "srcportval":<String_value>,      "destipv6":<Boolean_value>,      "destipop":<String_value>,      "destipv6val":<String_value>,      "destport":<Boolean_value>,      "destportop":<String_value>,      "destportval":<String_value>,      "srcmac":<String_value>,      "srcmacmask":<String_value>,      "protocol":<String_value>,      "protocolnumber":<Double_value>,      "icmptype":<Double_value>,      "icmpcode":<Double_value>,      "vlan":<Double_value>,      "vxlan":<Double_value>,      "Interface":<String_value>,      "priority":<Double_value>,      "established":<Boolean_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsacl6?action=unset
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"nsacl6":{      "acl6name":<String_value>,      "srcipv6":true,      "srcport":true,      "destipv6":true,      "destport":true,      "srcmac":true,      "srcmacmask":true,      "protocol":true,      "icmptype":true,      "icmpcode":true,      "vlan":true,      "vxlan":true,      "Interface":true,      "established":true}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###enable



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsacl6?action=enable
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"nsacl6":{      "acl6name":<String_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###disable



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsacl6?action=disable
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"nsacl6":{      "acl6name":<String_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###rename



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsacl6?action=rename
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"nsacl6":{      "acl6name":<String_value>,      "newname":<String_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsacl6
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsacl6?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


filter
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsacl6?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of nsacl6 resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsacl6?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).


pagination
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsacl6?pagesize=#no;pageno=#no
Use this query-parameter to get the nsacl6 resources in chunks.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "nsacl6": [ {      "acl6name":<String_value>,      "acl6action":<String_value>,      "srcmac":<String_value>,      "srcmacmask":<String_value>,      "protocol":<String_value>,      "protocolnumber":<Double_value>,      "srcportval":<String_value>,      "destportval":<String_value>,      "srcipv6val":<String_value>,      "destipv6val":<String_value>,      "vlan":<Double_value>,      "vxlan":<Double_value>,      "state":<String_value>,      "kernelstate":<String_value>,      "ttl":<Double_value>,      "icmptype":<Double_value>,      "icmpcode":<Double_value>,      "Interface":<String_value>,      "hits":<Double_value>,      "established":<Boolean_value>,      "priority":<Double_value>,      "srcipop":<String_value>,      "destipop":<String_value>,      "srcportop":<String_value>,      "destportop":<String_value>,      "td":<Double_value>,      "aclassociate":<String[]_value>}]}```



###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsacl6/acl6name_value&lt;String&gt;
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsacl6/acl6name_value&lt;String&gt;?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsacl6/acl6name_value&lt;String&gt;?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "nsacl6": [ {      "acl6name":<String_value>,      "acl6action":<String_value>,      "srcmac":<String_value>,      "srcmacmask":<String_value>,      "protocol":<String_value>,      "protocolnumber":<Double_value>,      "srcportval":<String_value>,      "destportval":<String_value>,      "srcipv6val":<String_value>,      "destipv6val":<String_value>,      "vlan":<Double_value>,      "vxlan":<Double_value>,      "state":<String_value>,      "kernelstate":<String_value>,      "ttl":<Double_value>,      "icmptype":<Double_value>,      "icmpcode":<Double_value>,      "Interface":<String_value>,      "hits":<Double_value>,      "established":<Boolean_value>,      "priority":<Double_value>,      "srcipop":<String_value>,      "destipop":<String_value>,      "srcportop":<String_value>,      "destportop":<String_value>,      "td":<Double_value>,      "aclassociate":<String[]_value>}]}```



###count



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsacl6?count=yes
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: 
{ "nsacl6": [ { "__count": "#no"} ] }


