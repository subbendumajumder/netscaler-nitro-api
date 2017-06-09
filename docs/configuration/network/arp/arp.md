#arp

Configuration for arp resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>ipaddress</td><td>&lt;String></td><td>Read-write</td><td>IP address of the network device that you want to add to the ARP table.&lt;br>Minimum length = 1</td><tr><tr><td>td</td><td>&lt;Double></td><td>Read-write</td><td>Integer value that uniquely identifies the traffic domain in which you want to configure the entity. If you do not specify an ID, the entity becomes part of the default traffic domain, which has an ID of 0.&lt;br>Minimum value = 0&lt;br>Maximum value = 4094</td><tr><tr><td>mac</td><td>&lt;String></td><td>Read-write</td><td>MAC address of the network device.</td><tr><tr><td>ifnum</td><td>&lt;String></td><td>Read-write</td><td>Interface through which the network device is accessible. Specify the interface in (slot/port) notation. For example, 1/3.</td><tr><tr><td>vxlan</td><td>&lt;Double></td><td>Read-write</td><td>ID of the VXLAN on which the IP address of this ARP entry is reachable.&lt;br>Minimum value = 1&lt;br>Maximum value = 16777215</td><tr><tr><td>vtep</td><td>&lt;String></td><td>Read-write</td><td>IP address of the VXLAN tunnel endpoint (VTEP) through which the IP address of this ARP entry is reachable.&lt;br>Minimum length = 1</td><tr><tr><td>vlan</td><td>&lt;Double></td><td>Read-write</td><td>The VLAN ID through which packets are to be sent after matching the ARP entry. This is a numeric value.</td><tr><tr><td>ownernode</td><td>&lt;Double></td><td>Read-write</td><td>The owner node for the Arp entry.&lt;br>Minimum value = 0&lt;br>Maximum value = 31</td><tr><tr><td>all</td><td>&lt;Boolean></td><td>Read-write</td><td>Remove all ARP entries from the ARP table of the NetScaler appliance.</td><tr><tr><td>timeout</td><td>&lt;Double></td><td>Read-only</td><td>The time, in seconds, after which the entry times out.</td><tr><tr><td>state</td><td>&lt;Double></td><td>Read-only</td><td>The state of the ARP entry.</td><tr><tr><td>flags</td><td>&lt;Double></td><td>Read-only</td><td>The flags for the entry.</td><tr><tr><td>type</td><td>&lt;String></td><td>Read-only</td><td>Indicates whether this ARP entry was added manually or dynamically. When you manually add an ARP entry, the value for this parameter is STATIC. Otherwise, it is DYNAMIC. For the NSIP and loopback IP addresses, the value is PERMANENT.&lt;br>Possible values = STATIC, PERMANENT, DYNAMIC</td><tr><tr><td>channel</td><td>&lt;Double></td><td>Read-only</td><td>The tunnel, channel, or physical interface through which the ARP entry is identified.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [DELETE](#delete) | [SEND](#send) | [GET (ALL)](#get-(all)) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>},"sessionid":"##sessionid","arp":{      "ipaddress":<String_value>,      "td":<Double_value>,      "mac":<String_value>,      "ifnum":<String_value>,      "vxlan":<Double_value>,                  "vtep":<String_value>,      "vlan":<Double_value>,      "ownernode":<Double_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/arp/ipaddress_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/arp/ipaddress_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###send



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"send"},"sessionid":"##sessionid","arp":{      "ipaddress":<String_value>,                  "td":<Double_value>,      "all":<Boolean_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/arp
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/arp?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of arp resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/arp?view=summary
Use this query-parameter to get the summary output of arp resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/arp?pagesize=#no;pageno=#no
Use this query-parameter to get the arp resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/arp?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "arp": [ {      "ipaddress":<String_value>,                  "td":<Double_value>,      "ownernode":<Double_value>,      "mac":<String_value>,      "ifnum":<String_value>,      "timeout":<Double_value>,      "state":<Double_value>,      "flags":<Double_value>,      "type":<String_value>,      "vlan":<Double_value>,      "vxlan":<Double_value>,      "vtep":<String_value>,      "channel":<Double_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/arp?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",arp: [ { "__count": "#no"} ] }


