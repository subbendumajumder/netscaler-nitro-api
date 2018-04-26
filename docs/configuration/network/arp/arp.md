#arp

Configuration for arp resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>ipaddress</td><td>&lt;String></td><td>Read-write</td><td>IP address of the network device that you want to add to the ARP table.<br>Minimum length = 1</td></tr><tr><td>td</td><td>&lt;Double></td><td>Read-write</td><td>Integer value that uniquely identifies the traffic domain in which you want to configure the entity. If you do not specify an ID, the entity becomes part of the default traffic domain, which has an ID of 0.<br>Minimum value = 0<br>Maximum value = 4094</td></tr><tr><td>mac</td><td>&lt;String></td><td>Read-write</td><td>MAC address of the network device.</td></tr><tr><td>ifnum</td><td>&lt;String></td><td>Read-write</td><td>Interface through which the network device is accessible. Specify the interface in (slot/port) notation. For example, 1/3.</td></tr><tr><td>vxlan</td><td>&lt;Double></td><td>Read-write</td><td>ID of the VXLAN on which the IP address of this ARP entry is reachable.<br>Minimum value = 1<br>Maximum value = 16777215</td></tr><tr><td>vtep</td><td>&lt;String></td><td>Read-write</td><td>IP address of the VXLAN tunnel endpoint (VTEP) through which the IP address of this ARP entry is reachable.<br>Minimum length = 1</td></tr><tr><td>vlan</td><td>&lt;Double></td><td>Read-write</td><td>The VLAN ID through which packets are to be sent after matching the ARP entry. This is a numeric value.</td></tr><tr><td>ownernode</td><td>&lt;Double></td><td>Read-write</td><td>The owner node for the Arp entry.<br>Minimum value = 0<br>Maximum value = 31</td></tr><tr><td>all</td><td>&lt;Boolean></td><td>Read-write</td><td>Remove all ARP entries from the ARP table of the NetScaler appliance.</td></tr><tr><td>nodeid</td><td>&lt;Double></td><td>Read-write</td><td>Unique number that identifies the cluster node.<br>Minimum value = 0<br>Maximum value = 31</td></tr><tr><td>timeout</td><td>&lt;Double></td><td>Read-only</td><td>The time, in seconds, after which the entry times out.</td></tr><tr><td>state</td><td>&lt;Double></td><td>Read-only</td><td>The state of the ARP entry.</td></tr><tr><td>flags</td><td>&lt;Double></td><td>Read-only</td><td>The flags for the entry.</td></tr><tr><td>type</td><td>&lt;String></td><td>Read-only</td><td>Indicates whether this ARP entry was added manually or dynamically. When you manually add an ARP entry, the value for this parameter is STATIC. Otherwise, it is DYNAMIC. For the NSIP and loopback IP addresses, the value is PERMANENT.<br>Possible values = STATIC, PERMANENT, DYNAMIC</td></tr><tr><td>channel</td><td>&lt;Double></td><td>Read-only</td><td>The tunnel, channel, or physical interface through which the ARP entry is identified.</td></tr><tr><td>controlplane</td><td>&lt;Boolean></td><td>Read-only</td><td>This arp entry is populated by a control plane protocol.</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD]()| [DELETE](#d)| [SEND]()| [GET (ALL)](#get-)| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/arp
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"arp":{<b>"ipaddress":<String_value>,</b>"td":<Double_value>,<b>"mac":<String_value>,</b>"ifnum":<String_value>,"vxlan":<Double_value>,"vtep":<String_value>,"vlan":<Double_value>,"ownernode":<Double_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/arp/ipaddress_value&lt;String&gt;
<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###send



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/arp?<b>action=send</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"arp":{"ipaddress":<String_value>,"td":<Double_value>,"all":<Boolean_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/arp
<b>Query-parameters:</b>
<b>args</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/arp?<b>args=ipaddress:&lt;String_value&gt;,td:&lt;Double_value&gt;,ownernode:&lt;Double_value&gt;,nodeid:&lt;Double_value&gt;</b>
Use this query-parameter to get arp resources based on additional properties.


<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/arp?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/arp?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of arp resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/arp?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/arp?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the arp resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "arp": [ {ipaddress:<String_value>,td:<Double_value>,ownernode:<Double_value>,nodeid:<Double_value>"mac":<String_value>,"ifnum":<String_value>,"timeout":<Double_value>,"state":<Double_value>,"flags":<Double_value>,"type":<String_value>,"vlan":<Double_value>,"vxlan":<Double_value>,"vtep":<String_value>,"channel":<Double_value>,"controlplane":<Boolean_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/arp?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "arp": [ { "__count": "#no"} ] }```



