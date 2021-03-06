#nspbr

Configuration for Policy Based Routing(PBR) entry resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the PBR. Must begin with an ASCII alphabetic or underscore \(_\) character, and must contain only ASCII alphanumeric, underscore, hash \(\#\), period \(.\), space, colon \(:\), at \(@\), equals \(=\), and hyphen \(-\) characters. Cannot be changed after the PBR is created.<br>Minimum length = 1</td></tr><tr><td>action</td><td>&lt;String></td><td>Read-write</td><td>Action to perform on the outgoing IPv4 packets that match the PBR.<br><br>Available settings function as follows:<br>* ALLOW - The NetScaler appliance sends the packet to the designated next-hop router.<br>* DENY - The NetScaler appliance applies the routing table for normal destination-based routing.<br>Possible values = ALLOW, DENY</td></tr><tr><td>td</td><td>&lt;Double></td><td>Read-write</td><td>Integer value that uniquely identifies the traffic domain in which you want to configure the entity. If you do not specify an ID, the entity becomes part of the default traffic domain, which has an ID of 0.<br>Minimum value = 0<br>Maximum value = 4094</td></tr><tr><td>srcip</td><td>&lt;Boolean></td><td>Read-write</td><td>IP address or range of IP addresses to match against the source IP address of an outgoing IPv4 packet. In the command line interface, separate the range with a hyphen. For example: 10.102.29.30-10.102.29.189.</td></tr><tr><td>srcipop</td><td>&lt;String></td><td>Read-write</td><td>Either the equals (=) or does not equal (!=) logical operator.<br>Possible values = =, !=, EQ, NEQ</td></tr><tr><td>srcipval</td><td>&lt;String></td><td>Read-write</td><td>IP address or range of IP addresses to match against the source IP address of an outgoing IPv4 packet. In the command line interface, separate the range with a hyphen. For example: 10.102.29.30-10.102.29.189.</td></tr><tr><td>srcport</td><td>&lt;Boolean></td><td>Read-write</td><td>Port number or range of port numbers to match against the source port number of an outgoing IPv4 packet. In the command line interface, separate the range with a hyphen. For example: 40-90.<br><br>Note: The destination port can be specified only for TCP and UDP protocols.</td></tr><tr><td>srcportop</td><td>&lt;String></td><td>Read-write</td><td>Either the equals (=) or does not equal (!=) logical operator.<br>Possible values = =, !=, EQ, NEQ</td></tr><tr><td>srcportval</td><td>&lt;String></td><td>Read-write</td><td>Port number or range of port numbers to match against the source port number of an outgoing IPv4 packet. In the command line interface, separate the range with a hyphen. For example: 40-90.<br><br>Note: The destination port can be specified only for TCP and UDP protocols.<br>Maximum length = 65535</td></tr><tr><td>destip</td><td>&lt;Boolean></td><td>Read-write</td><td>IP address or range of IP addresses to match against the destination IP address of an outgoing IPv4 packet. In the command line interface, separate the range with a hyphen. For example: 10.102.29.30-10.102.29.189.</td></tr><tr><td>destipop</td><td>&lt;String></td><td>Read-write</td><td>Either the equals (=) or does not equal (!=) logical operator.<br>Possible values = =, !=, EQ, NEQ</td></tr><tr><td>destipval</td><td>&lt;String></td><td>Read-write</td><td>IP address or range of IP addresses to match against the destination IP address of an outgoing IPv4 packet. In the command line interface, separate the range with a hyphen. For example: 10.102.29.30-10.102.29.189.</td></tr><tr><td>destport</td><td>&lt;Boolean></td><td>Read-write</td><td>Port number or range of port numbers to match against the destination port number of an outgoing IPv4 packet. In the command line interface, separate the range with a hyphen. For example: 40-90.<br><br>Note: The destination port can be specified only for TCP and UDP protocols.</td></tr><tr><td>destportop</td><td>&lt;String></td><td>Read-write</td><td>Either the equals (=) or does not equal (!=) logical operator.<br>Possible values = =, !=, EQ, NEQ</td></tr><tr><td>destportval</td><td>&lt;String></td><td>Read-write</td><td>Port number or range of port numbers to match against the destination port number of an outgoing IPv4 packet. In the command line interface, separate the range with a hyphen. For example: 40-90.<br><br>Note: The destination port can be specified only for TCP and UDP protocols.<br>Maximum length = 65535</td></tr><tr><td>nexthop</td><td>&lt;Boolean></td><td>Read-write</td><td>IP address of the next hop router or the name of the link load balancing virtual server to which to send matching packets if action is set to ALLOW.<br>If you specify a link load balancing (LLB) virtual server, which can provide a backup if a next hop link fails, first make sure that the next hops bound to the LLB virtual server are actually next hops that are directly connected to the NetScaler appliance. Otherwise, the NetScaler throws an error when you attempt to create the PBR. The next hop can be null to represent null routes.</td></tr><tr><td>nexthopval</td><td>&lt;String></td><td>Read-write</td><td>The Next Hop IP address or gateway name.</td></tr><tr><td>iptunnel</td><td>&lt;Boolean></td><td>Read-write</td><td>The Tunnel name.</td></tr><tr><td>iptunnelname</td><td>&lt;String></td><td>Read-write</td><td>The iptunnel name where packets need to be forwarded upon.</td></tr><tr><td>vxlanvlanmap</td><td>&lt;String></td><td>Read-write</td><td>The vlan to vxlan mapping to be applied for incoming packets over this pbr tunnel.</td></tr><tr><td>srcmac</td><td>&lt;String></td><td>Read-write</td><td>MAC address to match against the source MAC address of an outgoing IPv4 packet.</td></tr><tr><td>srcmacmask</td><td>&lt;String></td><td>Read-write</td><td>Used to define range of Source MAC address. It takes string of 0 and 1, 0s are for exact match and 1s for wildcard. For matching first 3 bytes of MAC address, srcMacMask value "000000111111". .<br>Default value: "000000000000"</td></tr><tr><td>protocol</td><td>&lt;String></td><td>Read-write</td><td>Protocol, identified by protocol name, to match against the protocol of an outgoing IPv4 packet.<br>Possible values = ICMP, IGMP, TCP, EGP, IGP, ARGUS, UDP, RDP, RSVP, EIGRP, L2TP, ISIS</td></tr><tr><td>protocolnumber</td><td>&lt;Double></td><td>Read-write</td><td>Protocol, identified by protocol number, to match against the protocol of an outgoing IPv4 packet.<br>Minimum value = 1<br>Maximum value = 255</td></tr><tr><td>vlan</td><td>&lt;Double></td><td>Read-write</td><td>ID of the VLAN. The NetScaler appliance compares the PBR only to the outgoing packets on the specified VLAN. If you do not specify any interface ID, the appliance compares the PBR to the outgoing packets on all VLANs.<br>Minimum value = 1<br>Maximum value = 4094</td></tr><tr><td>vxlan</td><td>&lt;Double></td><td>Read-write</td><td>ID of the VXLAN. The NetScaler appliance compares the PBR only to the outgoing packets on the specified VXLAN. If you do not specify any interface ID, the appliance compares the PBR to the outgoing packets on all VXLANs.<br>Minimum value = 1<br>Maximum value = 16777215</td></tr><tr><td>Interface</td><td>&lt;String></td><td>Read-write</td><td>ID of an interface. The NetScaler appliance compares the PBR only to the outgoing packets on the specified interface. If you do not specify any value, the appliance compares the PBR to the outgoing packets on all interfaces.</td></tr><tr><td>priority</td><td>&lt;Double></td><td>Read-write</td><td>Priority of the PBR, which determines the order in which it is evaluated relative to the other PBRs. If you do not specify priorities while creating PBRs, the PBRs are evaluated in the order in which they are created.<br>Minimum value = 1<br>Maximum value = 81920</td></tr><tr><td>msr</td><td>&lt;String></td><td>Read-write</td><td>Monitor the route specified byte Next Hop parameter. This parameter is not applicable if you specify a link load balancing (LLB) virtual server name with the Next Hop parameter.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>monitor</td><td>&lt;String></td><td>Read-write</td><td>The name of the monitor.(Can be only of type ping or ARP ).<br>Minimum length = 1</td></tr><tr><td>state</td><td>&lt;String></td><td>Read-write</td><td>Enable or disable the PBR. After you apply the PBRs, the NetScaler appliance compares outgoing packets to the enabled PBRs.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>ownergroup</td><td>&lt;String></td><td>Read-write</td><td>The owner node group in a Cluster for this pbr rule. If ownernode is not specified then the pbr rule is treated as Striped pbr rule.<br>Default value: DEFAULT_NG<br>Minimum length = 1</td></tr><tr><td>detail</td><td>&lt;Boolean></td><td>Read-write</td><td>To get a detailed view.</td></tr><tr><td>hits</td><td>&lt;Double></td><td>Read-only</td><td>The hits of this PBR.</td></tr><tr><td>kernelstate</td><td>&lt;String></td><td>Read-only</td><td>The commit status of the PBR.<br>Default value: NOTAPPLIED<br>Possible values = APPLIED, NOTAPPLIED, RE-APPLY, SFAPPLIED, SFNOTAPPLIED, SFAPPLIED61, SFNOTAPPLIED61</td></tr><tr><td>curstate</td><td>&lt;Double></td><td>Read-only</td><td>If this route is UP/DOWN.</td></tr><tr><td>totalprobes</td><td>&lt;Double></td><td>Read-only</td><td>The total number of probes sent.</td></tr><tr><td>totalfailedprobes</td><td>&lt;Double></td><td>Read-only</td><td>The total number of failed probes.</td></tr><tr><td>failedprobes</td><td>&lt;Double></td><td>Read-only</td><td>Number of the current failed monitoring probes.</td></tr><tr><td>monstatcode</td><td>&lt;Integer></td><td>Read-only</td><td>The code indicating the monitor response.</td></tr><tr><td>monstatparam1</td><td>&lt;Integer></td><td>Read-only</td><td>First parameter for use with message code.</td></tr><tr><td>monstatparam2</td><td>&lt;Integer></td><td>Read-only</td><td>Second parameter for use with message code.</td></tr><tr><td>monstatparam3</td><td>&lt;Integer></td><td>Read-only</td><td>Third parameter for use with message code.</td></tr><tr><td>data</td><td>&lt;Boolean></td><td>Read-only</td><td>Internal data of this route.</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD]()| [DELETE](#d)| [UPDATE](#u)| [UNSET](#)| [ENABLE](#e)| [DISABLE](#di)| [GET (ALL)](#get-)| [GET]()| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nspbr
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"nspbr":{<b>"name":<String_value>,</b><b>"action":<String_value>,</b>"td":<Double_value>,"srcip":<Boolean_value>,"srcipop":<String_value>,"srcipval":<String_value>,"srcport":<Boolean_value>,"srcportop":<String_value>,"srcportval":<String_value>,"destip":<Boolean_value>,"destipop":<String_value>,"destipval":<String_value>,"destport":<Boolean_value>,"destportop":<String_value>,"destportval":<String_value>,"nexthop":<Boolean_value>,"nexthopval":<String_value>,"iptunnel":<Boolean_value>,"iptunnelname":<String_value>,"vxlanvlanmap":<String_value>,"srcmac":<String_value>,"srcmacmask":<String_value>,"protocol":<String_value>,"protocolnumber":<Double_value>,"vlan":<Double_value>,"vxlan":<Double_value>,"Interface":<String_value>,"priority":<Double_value>,"msr":<String_value>,"monitor":<String_value>,"state":<String_value>,"ownergroup":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nspbr/name_value&lt;String&gt;
<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nspbr
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"nspbr":{<b>"name":<String_value>,</b>"action":<String_value>,"srcip":<Boolean_value>,"srcipop":<String_value>,"srcipval":<String_value>,"srcport":<Boolean_value>,"srcportop":<String_value>,"srcportval":<String_value>,"destip":<Boolean_value>,"destipop":<String_value>,"destipval":<String_value>,"destport":<Boolean_value>,"destportop":<String_value>,"destportval":<String_value>,"nexthop":<Boolean_value>,"nexthopval":<String_value>,"iptunnel":<Boolean_value>,"iptunnelname":<String_value>,"vxlanvlanmap":<String_value>,"srcmac":<String_value>,"srcmacmask":<String_value>,"protocol":<String_value>,"protocolnumber":<Double_value>,"vlan":<Double_value>,"vxlan":<Double_value>,"Interface":<String_value>,"priority":<Double_value>,"msr":<String_value>,"monitor":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nspbr?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"nspbr":{<b>"name":<String_value>,</b>"srcip":true,"srcport":true,"destip":true,"destport":true,"nexthop":true,"iptunnel":true,"vxlanvlanmap":true,"srcmac":true,"srcmacmask":true,"protocol":true,"vlan":true,"vxlan":true,"Interface":true,"msr":true,"monitor":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###enable



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nspbr?<b>action=enable</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"nspbr":{<b>"name":<String_value></b>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###disable



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nspbr?<b>action=disable</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"nspbr":{<b>"name":<String_value></b>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nspbr
<b>Query-parameters:</b>
<b>args</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nspbr?<b>args=name:&lt;String_value&gt;,detail:&lt;Boolean_value&gt;</b>
Use this query-parameter to get nspbr resources based on additional properties.


<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nspbr?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nspbr?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of nspbr resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nspbr?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nspbr?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the nspbr resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "nspbr": [ {name:<String_value>,detail:<Boolean_value>"action":<String_value>,"srcmac":<String_value>,"srcmacmask":<String_value>,"protocol":<String_value>,"protocolnumber":<Double_value>,"srcportval":<String_value>,"srcportop":<String_value>,"td":<Double_value>,"destportval":<String_value>,"destportop":<String_value>,"srcipval":<String_value>,"srcipop":<String_value>,"destipval":<String_value>,"destipop":<String_value>,"vlan":<Double_value>,"vxlan":<Double_value>,"state":<String_value>,"Interface":<String_value>,"hits":<Double_value>,"priority":<Double_value>,"kernelstate":<String_value>,"nexthopval":<String_value>,"iptunnelname":<String_value>,"vxlanvlanmap":<String_value>,"msr":<String_value>,"monitor":<String_value>,"curstate":<Double_value>,"totalprobes":<Double_value>,"totalfailedprobes":<Double_value>,"failedprobes":<Double_value>,"monstatcode":<Integer_value>,"monstatparam1":<Integer_value>,"monstatparam2":<Integer_value>,"monstatparam3":<Integer_value>,"data":<Boolean_value>,"ownergroup":<String_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nspbr/name_value&lt;String&gt;
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nspbr/name_value&lt;String&gt;?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nspbr/name_value&lt;String&gt;?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "nspbr": [ {name:<String_value>,detail:<Boolean_value>"action":<String_value>,"srcmac":<String_value>,"srcmacmask":<String_value>,"protocol":<String_value>,"protocolnumber":<Double_value>,"srcportval":<String_value>,"srcportop":<String_value>,"td":<Double_value>,"destportval":<String_value>,"destportop":<String_value>,"srcipval":<String_value>,"srcipop":<String_value>,"destipval":<String_value>,"destipop":<String_value>,"vlan":<Double_value>,"vxlan":<Double_value>,"state":<String_value>,"Interface":<String_value>,"hits":<Double_value>,"priority":<Double_value>,"kernelstate":<String_value>,"nexthopval":<String_value>,"iptunnelname":<String_value>,"vxlanvlanmap":<String_value>,"msr":<String_value>,"monitor":<String_value>,"curstate":<Double_value>,"totalprobes":<Double_value>,"totalfailedprobes":<Double_value>,"failedprobes":<Double_value>,"monstatcode":<Integer_value>,"monstatparam1":<Integer_value>,"monstatparam2":<Integer_value>,"monstatparam3":<Integer_value>,"data":<Boolean_value>,"ownergroup":<String_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nspbr?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "nspbr": [ { "__count": "#no"} ] }```



