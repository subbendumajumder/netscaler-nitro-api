#nsacl

Configuration for ACL entry resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>aclname</td><td>&lt;String></td><td>Read-write</td><td>Name for the extended ACL rule. Must begin with an ASCII alphabetic or underscore (_) character, and must contain only ASCII alphanumeric, underscore, hash (#), period (.), space, colon (:), at (@), equals (=), and hyphen (-) characters.<br>Minimum length = 1</td></tr><tr><td>aclaction</td><td>&lt;String></td><td>Read-write</td><td>Action to perform on incoming IPv4 packets that match the extended ACL rule.<br>Available settings function as follows:<br>* ALLOW - The NetScaler appliance processes the packet.<br>* BRIDGE - The NetScaler appliance bridges the packet to the destination without processing it.<br>* DENY - The NetScaler appliance drops the packet.<br>Possible values = BRIDGE, DENY, ALLOW</td></tr><tr><td>td</td><td>&lt;Double></td><td>Read-write</td><td>Integer value that uniquely identifies the traffic domain in which you want to configure the entity. If you do not specify an ID, the entity becomes part of the default traffic domain, which has an ID of 0.<br>Minimum value = 0<br>Maximum value = 4094</td></tr><tr><td>srcip</td><td>&lt;Boolean></td><td>Read-write</td><td>IP address or range of IP addresses to match against the source IP address of an incoming IPv4 packet. In the command line interface, separate the range with a hyphen. For example: 10.102.29.30-10.102.29.189.</td></tr><tr><td>srcipop</td><td>&lt;String></td><td>Read-write</td><td>Either the equals (=) or does not equal (!=) logical operator.<br>Possible values = =, !=, EQ, NEQ</td></tr><tr><td>srcipval</td><td>&lt;String></td><td>Read-write</td><td>IP address or range of IP addresses to match against the source IP address of an incoming IPv4 packet. In the command line interface, separate the range with a hyphen. For example:10.102.29.30-10.102.29.189.</td></tr><tr><td>srcport</td><td>&lt;Boolean></td><td>Read-write</td><td>Port number or range of port numbers to match against the source port number of an incoming IPv4 packet. In the command line interface, separate the range with a hyphen. For example: 40-90.</td></tr><tr><td>srcportop</td><td>&lt;String></td><td>Read-write</td><td>Either the equals (=) or does not equal (!=) logical operator.<br>Possible values = =, !=, EQ, NEQ</td></tr><tr><td>srcportval</td><td>&lt;String></td><td>Read-write</td><td>Port number or range of port numbers to match against the source port number of an incoming IPv4 packet. In the command line interface, separate the range with a hyphen. For example: 40-90.<br>Maximum length = 65535</td></tr><tr><td>destip</td><td>&lt;Boolean></td><td>Read-write</td><td>IP address or range of IP addresses to match against the destination IP address of an incoming IPv4 packet. In the command line interface, separate the range with a hyphen. For example: 10.102.29.30-10.102.29.189.</td></tr><tr><td>destipop</td><td>&lt;String></td><td>Read-write</td><td>Either the equals (=) or does not equal (!=) logical operator.<br>Possible values = =, !=, EQ, NEQ</td></tr><tr><td>destipval</td><td>&lt;String></td><td>Read-write</td><td>IP address or range of IP addresses to match against the destination IP address of an incoming IPv4 packet. In the command line interface, separate the range with a hyphen. For example: 10.102.29.30-10.102.29.189.</td></tr><tr><td>destport</td><td>&lt;Boolean></td><td>Read-write</td><td>Port number or range of port numbers to match against the destination port number of an incoming IPv4 packet. In the command line interface, separate the range with a hyphen. For example: 40-90.<br><br>Note: The destination port can be specified only for TCP and UDP protocols.</td></tr><tr><td>destportop</td><td>&lt;String></td><td>Read-write</td><td>Either the equals (=) or does not equal (!=) logical operator.<br>Possible values = =, !=, EQ, NEQ</td></tr><tr><td>destportval</td><td>&lt;String></td><td>Read-write</td><td>Port number or range of port numbers to match against the destination port number of an incoming IPv4 packet. In the command line interface, separate the range with a hyphen. For example: 40-90.<br><br>Note: The destination port can be specified only for TCP and UDP protocols.<br>Maximum length = 65535</td></tr><tr><td>ttl</td><td>&lt;Double></td><td>Read-write</td><td>Number of seconds, in multiples of four, after which the extended ACL rule expires. If you do not want the extended ACL rule to expire, do not specify a TTL value.<br>Minimum value = 1<br>Maximum value = 2147483647</td></tr><tr><td>srcmac</td><td>&lt;String></td><td>Read-write</td><td>MAC address to match against the source MAC address of an incoming IPv4 packet.</td></tr><tr><td>srcmacmask</td><td>&lt;String></td><td>Read-write</td><td>Used to define range of Source MAC address. It takes string of 0 and 1, 0s are for exact match and 1s for wildcard. For matching first 3 bytes of MAC address, srcMacMask value "000000111111". .<br>Default value: "000000000000"</td></tr><tr><td>protocol</td><td>&lt;String></td><td>Read-write</td><td>Protocol to match against the protocol of an incoming IPv4 packet.<br>Possible values = ICMP, IGMP, TCP, EGP, IGP, ARGUS, UDP, RDP, RSVP, EIGRP, L2TP, ISIS</td></tr><tr><td>protocolnumber</td><td>&lt;Double></td><td>Read-write</td><td>Protocol to match against the protocol of an incoming IPv4 packet.<br>Minimum value = 1<br>Maximum value = 255</td></tr><tr><td>vlan</td><td>&lt;Double></td><td>Read-write</td><td>ID of the VLAN. The NetScaler appliance applies the ACL rule only to the incoming packets of the specified VLAN. If you do not specify a VLAN ID, the appliance applies the ACL rule to the incoming packets on all VLANs.<br>Minimum value = 1<br>Maximum value = 4094</td></tr><tr><td>vxlan</td><td>&lt;Double></td><td>Read-write</td><td>ID of the VXLAN. The NetScaler appliance applies the ACL rule only to the incoming packets of the specified VXLAN. If you do not specify a VXLAN ID, the appliance applies the ACL rule to the incoming packets on all VXLANs.<br>Minimum value = 1<br>Maximum value = 16777215</td></tr><tr><td>Interface</td><td>&lt;String></td><td>Read-write</td><td>ID of an interface. The NetScaler appliance applies the ACL rule only to the incoming packets from the specified interface. If you do not specify any value, the appliance applies the ACL rule to the incoming packets of all interfaces.</td></tr><tr><td>established</td><td>&lt;Boolean></td><td>Read-write</td><td>Allow only incoming TCP packets that have the ACK or RST bit set, if the action set for the ACL rule is ALLOW and these packets match the other conditions in the ACL rule.</td></tr><tr><td>icmptype</td><td>&lt;Double></td><td>Read-write</td><td>ICMP Message type to match against the message type of an incoming ICMP packet. For example, to block DESTINATION UNREACHABLE messages, you must specify 3 as the ICMP type.<br><br>Note: This parameter can be specified only for the ICMP protocol.<br>Minimum value = 0<br>Maximum value = 65536</td></tr><tr><td>icmpcode</td><td>&lt;Double></td><td>Read-write</td><td>Code of a particular ICMP message type to match against the ICMP code of an incoming ICMP packet. For example, to block DESTINATION HOST UNREACHABLE messages, specify 3 as the ICMP type and 1 as the ICMP code.<br><br>If you set this parameter, you must set the ICMP Type parameter.<br>Minimum value = 0<br>Maximum value = 65536</td></tr><tr><td>priority</td><td>&lt;Double></td><td>Read-write</td><td>Priority for the extended ACL rule that determines the order in which it is evaluated relative to the other extended ACL rules. If you do not specify priorities while creating extended ACL rules, the ACL rules are evaluated in the order in which they are created.<br>Minimum value = 1<br>Maximum value = 100000</td></tr><tr><td>state</td><td>&lt;String></td><td>Read-write</td><td>Enable or disable the extended ACL rule. After you apply the extended ACL rules, the NetScaler appliance compares incoming packets against the enabled extended ACL rules.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>logstate</td><td>&lt;String></td><td>Read-write</td><td>Enable or disable logging of events related to the extended ACL rule. The log messages are stored in the configured syslog or auditlog server.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>ratelimit</td><td>&lt;Double></td><td>Read-write</td><td>Maximum number of log messages to be generated per second. If you set this parameter, you must enable the Log State parameter.<br>Default value: 100<br>Minimum value = 1<br>Maximum value = 10000</td></tr><tr><td>newname</td><td>&lt;String></td><td>Read-write</td><td>New name for the extended ACL rule. Must begin with an ASCII alphabetic or underscore (_) character, and must contain only ASCII alphanumeric, underscore, hash (#), period (.), space, colon (:), at (@), equals (=), and hyphen (-) characters.<br>Minimum length = 1</td></tr><tr><td>hits</td><td>&lt;Double></td><td>Read-only</td><td>The hits of this ACL.</td></tr><tr><td>kernelstate</td><td>&lt;String></td><td>Read-only</td><td>The commit status of the ACL.<br>Default value: NOTAPPLIED<br>Possible values = APPLIED, NOTAPPLIED, RE-APPLY, SFAPPLIED, SFNOTAPPLIED, SFAPPLIED61, SFNOTAPPLIED61</td></tr><tr><td>aclassociate</td><td>&lt;String[]></td><td>Read-only</td><td>ACL linked.<br>Possible values = NAT, FORWARDINGSESSION, NAT64, LSN</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD]()| [DELETE](#d)| [UPDATE](#u)| [UNSET](#)| [ENABLE](#e)| [DISABLE](#di)| [RENAME](#r)| [GET (ALL)](#get-)| [GET]()| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsacl
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"nsacl":{<b>"aclname":<String_value>,</b><b>"aclaction":<String_value>,</b>"td":<Double_value>,"srcip":<Boolean_value>,"srcipop":<String_value>,"srcipval":<String_value>,"srcport":<Boolean_value>,"srcportop":<String_value>,"srcportval":<String_value>,"destip":<Boolean_value>,"destipop":<String_value>,"destipval":<String_value>,"destport":<Boolean_value>,"destportop":<String_value>,"destportval":<String_value>,"ttl":<Double_value>,"srcmac":<String_value>,"srcmacmask":<String_value>,"protocol":<String_value>,"protocolnumber":<Double_value>,"vlan":<Double_value>,"vxlan":<Double_value>,"Interface":<String_value>,"established":<Boolean_value>,"icmptype":<Double_value>,"icmpcode":<Double_value>,"priority":<Double_value>,"state":<String_value>,"logstate":<String_value>,"ratelimit":<Double_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsacl/aclname_value&lt;String&gt;
<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsacl
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"nsacl":{<b>"aclname":<String_value>,</b>"aclaction":<String_value>,"srcip":<Boolean_value>,"srcipop":<String_value>,"srcipval":<String_value>,"srcport":<Boolean_value>,"srcportop":<String_value>,"srcportval":<String_value>,"destip":<Boolean_value>,"destipop":<String_value>,"destipval":<String_value>,"destport":<Boolean_value>,"destportop":<String_value>,"destportval":<String_value>,"srcmac":<String_value>,"srcmacmask":<String_value>,"protocol":<String_value>,"protocolnumber":<Double_value>,"icmptype":<Double_value>,"icmpcode":<Double_value>,"vlan":<Double_value>,"vxlan":<Double_value>,"Interface":<String_value>,"priority":<Double_value>,"logstate":<String_value>,"ratelimit":<Double_value>,"established":<Boolean_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsacl?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"nsacl":{<b>"aclname":<String_value>,</b>"srcip":true,"srcport":true,"destip":true,"destport":true,"srcmac":true,"srcmacmask":true,"protocol":true,"icmptype":true,"icmpcode":true,"vlan":true,"vxlan":true,"Interface":true,"logstate":true,"ratelimit":true,"established":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###enable



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsacl?<b>action=enable</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"nsacl":{<b>"aclname":<String_value></b>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###disable



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsacl?<b>action=disable</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"nsacl":{<b>"aclname":<String_value></b>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###rename



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsacl?<b>action=rename</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"nsacl":{<b>"aclname":<String_value>,</b><b>"newname":<String_value></b>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsacl
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsacl?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsacl?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of nsacl resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsacl?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsacl?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the nsacl resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "nsacl": [ {"aclname":<String_value>,"td":<Double_value>,"aclaction":<String_value>,"srcmac":<String_value>,"srcmacmask":<String_value>,"protocol":<String_value>,"protocolnumber":<Double_value>,"srcportval":<String_value>,"srcportop":<String_value>,"destportval":<String_value>,"destportop":<String_value>,"srcipval":<String_value>,"srcipop":<String_value>,"destipval":<String_value>,"destipop":<String_value>,"vlan":<Double_value>,"vxlan":<Double_value>,"state":<String_value>,"ttl":<Double_value>,"icmptype":<Double_value>,"icmpcode":<Double_value>,"Interface":<String_value>,"hits":<Double_value>,"established":<Boolean_value>,"priority":<Double_value>,"kernelstate":<String_value>,"logstate":<String_value>,"ratelimit":<Double_value>,"aclassociate":<String[]_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsacl/aclname_value&lt;String&gt;
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsacl/aclname_value&lt;String&gt;?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsacl/aclname_value&lt;String&gt;?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "nsacl": [ {"aclname":<String_value>,"td":<Double_value>,"aclaction":<String_value>,"srcmac":<String_value>,"srcmacmask":<String_value>,"protocol":<String_value>,"protocolnumber":<Double_value>,"srcportval":<String_value>,"srcportop":<String_value>,"destportval":<String_value>,"destportop":<String_value>,"srcipval":<String_value>,"srcipop":<String_value>,"destipval":<String_value>,"destipop":<String_value>,"vlan":<Double_value>,"vxlan":<Double_value>,"state":<String_value>,"ttl":<Double_value>,"icmptype":<Double_value>,"icmpcode":<Double_value>,"Interface":<String_value>,"hits":<Double_value>,"established":<Boolean_value>,"priority":<Double_value>,"kernelstate":<String_value>,"logstate":<String_value>,"ratelimit":<Double_value>,"aclassociate":<String[]_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsacl?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "nsacl": [ { "__count": "#no"} ] }```



