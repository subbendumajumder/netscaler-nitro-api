#nspbr6

Configuration for PBR6 entry resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the PBR6. Must begin with an ASCII alphabetic or underscore \(_\) character, and must contain only ASCII alphanumeric, underscore, hash \(\#\), period \(.\), space, colon \(:\), at \(@\), equals \(=\), and hyphen \(-\) characters. Cannot be changed after the PBR6 is created.<br>Minimum length = 1</td></tr><tr><td>td</td><td>&lt;Double></td><td>Read-write</td><td>Integer value that uniquely identifies the traffic domain in which you want to configure the entity. If you do not specify an ID, the entity becomes part of the default traffic domain, which has an ID of 0.<br>Minimum value = 0<br>Maximum value = 4094</td></tr><tr><td>action</td><td>&lt;String></td><td>Read-write</td><td>Action to perform on the outgoing IPv6 packets that match the PBR6.<br><br>Available settings function as follows:<br>* ALLOW - The NetScaler appliance sends the packet to the designated next-hop router.<br>* DENY - The NetScaler appliance applies the routing table for normal destination-based routing.<br>Possible values = ALLOW, DENY</td></tr><tr><td>srcipv6</td><td>&lt;Boolean></td><td>Read-write</td><td>IP address or range of IP addresses to match against the source IP address of an outgoing IPv6 packet. In the command line interface, separate the range with a hyphen.</td></tr><tr><td>srcipop</td><td>&lt;String></td><td>Read-write</td><td>Either the equals (=) or does not equal (!=) logical operator.<br>Possible values = =, !=, EQ, NEQ</td></tr><tr><td>srcipv6val</td><td>&lt;String></td><td>Read-write</td><td>IP address or range of IP addresses to match against the source IP address of an outgoing IPv6 packet. In the command line interface, separate the range with a hyphen.</td></tr><tr><td>srcport</td><td>&lt;Boolean></td><td>Read-write</td><td>Port number or range of port numbers to match against the source port number of an outgoing IPv6 packet. In the command line interface, separate the range with a hyphen. For example: 40-90.</td></tr><tr><td>srcportop</td><td>&lt;String></td><td>Read-write</td><td>Either the equals (=) or does not equal (!=) logical operator.<br>Possible values = =, !=, EQ, NEQ</td></tr><tr><td>srcportval</td><td>&lt;String></td><td>Read-write</td><td>Source port (range).<br>Maximum length = 65535</td></tr><tr><td>destipv6</td><td>&lt;Boolean></td><td>Read-write</td><td>IP address or range of IP addresses to match against the destination IP address of an outgoing IPv6 packet. In the command line interface, separate the range with a hyphen.</td></tr><tr><td>destipop</td><td>&lt;String></td><td>Read-write</td><td>Either the equals (=) or does not equal (!=) logical operator.<br>Possible values = =, !=, EQ, NEQ</td></tr><tr><td>destipv6val</td><td>&lt;String></td><td>Read-write</td><td>IP address or range of IP addresses to match against the destination IP address of an outgoing IPv6 packet. In the command line interface, separate the range with a hyphen.</td></tr><tr><td>destport</td><td>&lt;Boolean></td><td>Read-write</td><td>Port number or range of port numbers to match against the destination port number of an outgoing IPv6 packet. In the command line interface, separate the range with a hyphen. For example: 40-90.<br><br>Note: The destination port can be specified only for TCP and UDP protocols.</td></tr><tr><td>destportop</td><td>&lt;String></td><td>Read-write</td><td>Either the equals (=) or does not equal (!=) logical operator.<br>Possible values = =, !=, EQ, NEQ</td></tr><tr><td>destportval</td><td>&lt;String></td><td>Read-write</td><td>Destination port (range).<br>Maximum length = 65535</td></tr><tr><td>srcmac</td><td>&lt;String></td><td>Read-write</td><td>MAC address to match against the source MAC address of an outgoing IPv6 packet.</td></tr><tr><td>srcmacmask</td><td>&lt;String></td><td>Read-write</td><td>Used to define range of Source MAC address. It takes string of 0 and 1, 0s are for exact match and 1s for wildcard. For matching first 3 bytes of MAC address, srcMacMask value "000000111111". .<br>Default value: "000000000000"</td></tr><tr><td>protocol</td><td>&lt;String></td><td>Read-write</td><td>Protocol, identified by protocol name, to match against the protocol of an outgoing IPv6 packet.<br>Possible values = ICMPV6, TCP, UDP</td></tr><tr><td>protocolnumber</td><td>&lt;Double></td><td>Read-write</td><td>Protocol, identified by protocol number, to match against the protocol of an outgoing IPv6 packet.<br>Minimum value = 1<br>Maximum value = 255</td></tr><tr><td>vlan</td><td>&lt;Double></td><td>Read-write</td><td>ID of the VLAN. The NetScaler appliance compares the PBR6 only to the outgoing packets on the specified VLAN. If you do not specify an interface ID, the appliance compares the PBR6 to the outgoing packets on all VLANs.<br>Minimum value = 1<br>Maximum value = 4094</td></tr><tr><td>vxlan</td><td>&lt;Double></td><td>Read-write</td><td>ID of the VXLAN. The NetScaler appliance compares the PBR6 only to the outgoing packets on the specified VXLAN. If you do not specify an interface ID, the appliance compares the PBR6 to the outgoing packets on all VXLANs.<br>Minimum value = 1<br>Maximum value = 16777215</td></tr><tr><td>Interface</td><td>&lt;String></td><td>Read-write</td><td>ID of an interface. The NetScaler appliance compares the PBR6 only to the outgoing packets on the specified interface. If you do not specify a value, the appliance compares the PBR6 to the outgoing packets on all interfaces.</td></tr><tr><td>priority</td><td>&lt;Double></td><td>Read-write</td><td>Priority of the PBR6, which determines the order in which it is evaluated relative to the other PBR6s. If you do not specify priorities while creating PBR6s, the PBR6s are evaluated in the order in which they are created.<br>Minimum value = 1<br>Maximum value = 81920</td></tr><tr><td>state</td><td>&lt;String></td><td>Read-write</td><td>Enable or disable the PBR6. After you apply the PBR6s, the NetScaler appliance compares outgoing packets to the enabled PBR6s.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>msr</td><td>&lt;String></td><td>Read-write</td><td>Monitor the route specified by the Next Hop parameter.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>monitor</td><td>&lt;String></td><td>Read-write</td><td>The name of the monitor.(Can be only of type ping or ARP ).<br>Minimum length = 1</td></tr><tr><td>nexthop</td><td>&lt;Boolean></td><td>Read-write</td><td>IP address of the next hop router to which to send matching packets if action is set to ALLOW. This next hop should be directly reachable from the appliance.</td></tr><tr><td>nexthopval</td><td>&lt;String></td><td>Read-write</td><td>The Next Hop IPv6 address.</td></tr><tr><td>iptunnel</td><td>&lt;String></td><td>Read-write</td><td>The iptunnel name where packets need to be forwarded upon.</td></tr><tr><td>vxlanvlanmap</td><td>&lt;String></td><td>Read-write</td><td>The vlan to vxlan mapping to be applied for incoming packets over this pbr tunnel.</td></tr><tr><td>nexthopvlan</td><td>&lt;Double></td><td>Read-write</td><td>VLAN number to be used for link local nexthop .<br>Minimum value = 1<br>Maximum value = 4094</td></tr><tr><td>ownergroup</td><td>&lt;String></td><td>Read-write</td><td>The owner node group in a Cluster for this pbr rule. If owner node group is not specified then the pbr rule is treated as Striped pbr rule.<br>Default value: DEFAULT_NG<br>Minimum length = 1</td></tr><tr><td>detail</td><td>&lt;Boolean></td><td>Read-write</td><td>To get a detailed view.</td></tr><tr><td>kernelstate</td><td>&lt;String></td><td>Read-only</td><td>Commit status of the PBR6.<br>Default value: NOTAPPLIED<br>Possible values = APPLIED, NOTAPPLIED, RE-APPLY, SFAPPLIED, SFNOTAPPLIED</td></tr><tr><td>hits</td><td>&lt;Double></td><td>Read-only</td><td>Number of hits of this PBR6.</td></tr><tr><td>curstate</td><td>&lt;Double></td><td>Read-only</td><td>If this route is UP/DOWN.</td></tr><tr><td>totalprobes</td><td>&lt;Double></td><td>Read-only</td><td>The total number of probes sent.</td></tr><tr><td>totalfailedprobes</td><td>&lt;Double></td><td>Read-only</td><td>The total number of failed probes.</td></tr><tr><td>failedprobes</td><td>&lt;Double></td><td>Read-only</td><td>Number of the current failed monitoring probes.</td></tr><tr><td>monstatcode</td><td>&lt;Integer></td><td>Read-only</td><td>The code indicating the monitor response.</td></tr><tr><td>monstatparam1</td><td>&lt;Integer></td><td>Read-only</td><td>First parameter for use with message code.</td></tr><tr><td>monstatparam2</td><td>&lt;Integer></td><td>Read-only</td><td>Second parameter for use with message code.</td></tr><tr><td>monstatparam3</td><td>&lt;Integer></td><td>Read-only</td><td>Third parameter for use with message code.</td></tr><tr><td>data</td><td>&lt;Boolean></td><td>Read-only</td><td>Internal data of this route.</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD]()| [RENUMBER](#ren)| [DELETE](#d)| [UPDATE](#u)| [UNSET](#)| [ENABLE](#e)| [DISABLE](#di)| [CLEAR](#)| [APPLY](#)| [GET (ALL)](#get-)| [GET]()| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nspbr6
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"nspbr6":{<b>"name":<String_value>,</b>"td":<Double_value>,<b>"action":<String_value>,</b>"srcipv6":<Boolean_value>,"srcipop":<String_value>,"srcipv6val":<String_value>,"srcport":<Boolean_value>,"srcportop":<String_value>,"srcportval":<String_value>,"destipv6":<Boolean_value>,"destipop":<String_value>,"destipv6val":<String_value>,"destport":<Boolean_value>,"destportop":<String_value>,"destportval":<String_value>,"srcmac":<String_value>,"srcmacmask":<String_value>,"protocol":<String_value>,"protocolnumber":<Double_value>,"vlan":<Double_value>,"vxlan":<Double_value>,"Interface":<String_value>,"priority":<Double_value>,"state":<String_value>,"msr":<String_value>,"monitor":<String_value>,"nexthop":<Boolean_value>,"nexthopval":<String_value>,"iptunnel":<String_value>,"vxlanvlanmap":<String_value>,"nexthopvlan":<Double_value>,"ownergroup":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###renumber



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nspbr6?<b>action=renumber</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"nspbr6":{}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nspbr6/name_value&lt;String&gt;
<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nspbr6
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"nspbr6":{<b>"name":<String_value>,</b>"action":<String_value>,"srcipv6":<Boolean_value>,"srcipop":<String_value>,"srcipv6val":<String_value>,"srcport":<Boolean_value>,"srcportop":<String_value>,"srcportval":<String_value>,"destipv6":<Boolean_value>,"destipop":<String_value>,"destipv6val":<String_value>,"destport":<Boolean_value>,"destportop":<String_value>,"destportval":<String_value>,"srcmac":<String_value>,"srcmacmask":<String_value>,"protocol":<String_value>,"protocolnumber":<Double_value>,"vlan":<Double_value>,"vxlan":<Double_value>,"Interface":<String_value>,"priority":<Double_value>,"msr":<String_value>,"monitor":<String_value>,"nexthop":<Boolean_value>,"nexthopval":<String_value>,"iptunnel":<String_value>,"vxlanvlanmap":<String_value>,"nexthopvlan":<Double_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nspbr6?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"nspbr6":{<b>"name":<String_value>,</b>"srcipv6":true,"srcport":true,"destipv6":true,"destport":true,"srcmac":true,"srcmacmask":true,"protocol":true,"Interface":true,"vlan":true,"vxlan":true,"msr":true,"monitor":true,"nexthop":true,"iptunnel":true,"nexthopvlan":true,"vxlanvlanmap":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###enable



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nspbr6?<b>action=enable</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"nspbr6":{<b>"name":<String_value></b>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###disable



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nspbr6?<b>action=disable</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"nspbr6":{<b>"name":<String_value></b>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###clear



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nspbr6?<b>action=clear</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"nspbr6":{}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###apply



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nspbr6?<b>action=apply</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"nspbr6":{}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nspbr6
<b>Query-parameters:</b>
<b>args</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nspbr6?<b>args=name:&lt;String_value&gt;,detail:&lt;Boolean_value&gt;</b>
Use this query-parameter to get nspbr6 resources based on additional properties.


<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nspbr6?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nspbr6?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of nspbr6 resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nspbr6?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nspbr6?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the nspbr6 resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "nspbr6": [ {name:<String_value>,detail:<Boolean_value>"td":<Double_value>,"action":<String_value>,"srcmac":<String_value>,"srcmacmask":<String_value>,"protocol":<String_value>,"protocolnumber":<Double_value>,"srcportval":<String_value>,"srcportop":<String_value>,"destportval":<String_value>,"destportop":<String_value>,"srcipv6val":<String_value>,"srcipop":<String_value>,"destipv6val":<String_value>,"destipop":<String_value>,"vlan":<Double_value>,"vxlan":<Double_value>,"state":<String_value>,"kernelstate":<String_value>,"Interface":<String_value>,"hits":<Double_value>,"priority":<Double_value>,"msr":<String_value>,"monitor":<String_value>,"curstate":<Double_value>,"totalprobes":<Double_value>,"totalfailedprobes":<Double_value>,"failedprobes":<Double_value>,"monstatcode":<Integer_value>,"monstatparam1":<Integer_value>,"monstatparam2":<Integer_value>,"monstatparam3":<Integer_value>,"nexthopval":<String_value>,"iptunnel":<String_value>,"vxlanvlanmap":<String_value>,"nexthopvlan":<Double_value>,"data":<Boolean_value>,"ownergroup":<String_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nspbr6/name_value&lt;String&gt;
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nspbr6/name_value&lt;String&gt;?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nspbr6/name_value&lt;String&gt;?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "nspbr6": [ {name:<String_value>,detail:<Boolean_value>"td":<Double_value>,"action":<String_value>,"srcmac":<String_value>,"srcmacmask":<String_value>,"protocol":<String_value>,"protocolnumber":<Double_value>,"srcportval":<String_value>,"srcportop":<String_value>,"destportval":<String_value>,"destportop":<String_value>,"srcipv6val":<String_value>,"srcipop":<String_value>,"destipv6val":<String_value>,"destipop":<String_value>,"vlan":<Double_value>,"vxlan":<Double_value>,"state":<String_value>,"kernelstate":<String_value>,"Interface":<String_value>,"hits":<Double_value>,"priority":<Double_value>,"msr":<String_value>,"monitor":<String_value>,"curstate":<Double_value>,"totalprobes":<Double_value>,"totalfailedprobes":<Double_value>,"failedprobes":<Double_value>,"monstatcode":<Integer_value>,"monstatparam1":<Integer_value>,"monstatparam2":<Integer_value>,"monstatparam3":<Integer_value>,"nexthopval":<String_value>,"iptunnel":<String_value>,"vxlanvlanmap":<String_value>,"nexthopvlan":<Double_value>,"data":<Boolean_value>,"ownergroup":<String_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nspbr6?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "nspbr6": [ { "__count": "#no"} ] }```



