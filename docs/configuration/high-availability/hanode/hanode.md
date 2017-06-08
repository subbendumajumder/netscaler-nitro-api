#hanode

Configuration for node resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>&lt;Double></td><td>Read-write</td><td>Number that uniquely identifies the node. For self node, it will always be 0. Peer node values can range from 1-64.&lt;br>Minimum value = 1&lt;br>Maximum value = 64</td><tr><tr><td>ipaddress</td><td>&lt;String></td><td>Read-write</td><td>The NSIP or NSIP6 address of the node to be added for an HA configuration. This setting is neither propagated nor synchronized.&lt;br>Minimum length = 1</td><tr><tr><td>inc</td><td>&lt;String></td><td>Read-write</td><td>This option is required if the HA nodes reside on different networks. When this mode is enabled, the following independent network entities and configurations are neither propagated nor synced to the other node: MIPs, SNIPs, VLANs, routes (except LLB routes), route monitors, RNAT rules (except any RNAT rule with a VIP as the NAT IP), and dynamic routing configurations. They are maintained independently on each node.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>hastatus</td><td>&lt;String></td><td>Read-write</td><td>The HA status of the node. The HA status STAYSECONDARY is used to force the secondary device stay as secondary independent of the state of the Primary device. For example, in an existing HA setup, the Primary node has to be upgraded and this process would take few seconds. During the upgradation, it is possible that the Primary node may suffer from a downtime for a few seconds. However, the Secondary should not take over as the Primary node. Thus, the Secondary node should remain as Secondary even if there is a failure in the Primary node. STAYPRIMARY configuration keeps the node in primary state in case if it is healthy, even if the peer node was the primary node initially. If the node with STAYPRIMARY setting (and no peer node) is added to a primary node (which has this node as the peer) then this node takes over as the new primary and the older node becomes secondary. ENABLED state means normal HA operation without any constraints/preferences. DISABLED state disables the normal HA operation of the node.&lt;br>Possible values = ENABLED, STAYSECONDARY, DISABLED, STAYPRIMARY</td><tr><tr><td>hasync</td><td>&lt;String></td><td>Read-write</td><td>Automatically maintain synchronization by duplicating the configuration of the primary node on the secondary node. This setting is not propagated. Automatic synchronization requires that this setting be enabled (the default) on the current secondary node. Synchronization uses TCP port 3010.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>haprop</td><td>&lt;String></td><td>Read-write</td><td>Automatically propagate all commands from the primary to the secondary node, except the following: * All HA configuration related commands. For example, add ha node, set ha node, and bind ha node. * All Interface related commands. For example, set interface and unset interface. * All channels related commands. For example, add channel, set channel, and bind channel. The propagated command is executed on the secondary node before it is executed on the primary. If command propagation fails, or if command execution fails on the secondary, the primary node executes the command and logs an error. Command propagation uses port 3010. Note: After enabling propagation, run force synchronization on either node.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>hellointerval</td><td>&lt;Double></td><td>Read-write</td><td>Interval, in milliseconds, between heartbeat messages sent to the peer node. The heartbeat messages are UDP packets sent to port 3003 of the peer node.&lt;br>Default value: 200&lt;br>Minimum value = 200&lt;br>Maximum value = 1000</td><tr><tr><td>deadinterval</td><td>&lt;Double></td><td>Read-write</td><td>Number of seconds after which a peer node is marked DOWN if heartbeat messages are not received from the peer node.&lt;br>Default value: 3&lt;br>Minimum value = 3&lt;br>Maximum value = 60</td><tr><tr><td>failsafe</td><td>&lt;String></td><td>Read-write</td><td>Keep one node primary if both nodes fail the health check, so that a partially available node can back up data and handle traffic. This mode is set independently on each node.&lt;br>Default value: OFF&lt;br>Possible values = ON, OFF</td><tr><tr><td>maxflips</td><td>&lt;Double></td><td>Read-write</td><td>Max number of flips allowed before becoming sticky primary.&lt;br>Default value: 0</td><tr><tr><td>maxfliptime</td><td>&lt;Double></td><td>Read-write</td><td>Interval after which flipping of node states can again start.&lt;br>Default value: 0</td><tr><tr><td>syncvlan</td><td>&lt;Double></td><td>Read-write</td><td>Vlan on which HA related communication is sent. This include sync, propagation , connection mirroring , LB persistency config sync, persistent session sync and session state sync. However HA heartbeats can go all interfaces.&lt;br>Minimum value = 1&lt;br>Maximum value = 4094</td><tr><tr><td>name</td><td>&lt;String></td><td>Read-only</td><td>Node Name.</td><tr><tr><td>flags</td><td>&lt;Double></td><td>Read-only</td><td>The flags for this entry.</td><tr><tr><td>state</td><td>&lt;String></td><td>Read-only</td><td>HA Master State.&lt;br>Possible values = Primary, Secondary, UNKNOWN</td><tr><tr><td>enaifaces</td><td>&lt;String></td><td>Read-only</td><td>Enabled interfaces.</td><tr><tr><td>disifaces</td><td>&lt;String></td><td>Read-only</td><td>Disabled interfaces.</td><tr><tr><td>hamonifaces</td><td>&lt;String></td><td>Read-only</td><td>HAMON ON interfaces.</td><tr><tr><td>pfifaces</td><td>&lt;String></td><td>Read-only</td><td>Interfaces causing Partial Failure.</td><tr><tr><td>ifaces</td><td>&lt;String></td><td>Read-only</td><td>Interfaces on which non-multicast is not seen.</td><tr><tr><td>network</td><td>&lt;String></td><td>Read-only</td><td>The network.</td><tr><tr><td>netmask</td><td>&lt;String></td><td>Read-only</td><td>The netmask.</td><tr><tr><td>ssl2</td><td>&lt;String></td><td>Read-only</td><td>SSL card status.&lt;br>Possible values = DOWN, UP, NOT PRESENT, UNKNOWN</td><tr><tr><td>masterstatetime</td><td>&lt;Double></td><td>Read-only</td><td>Time elapsed in current master state.</td><tr><tr><td>routemonitor</td><td>&lt;String></td><td>Read-only</td><td>The IP address (IPv4 or IPv6).</td><tr><tr><td>curflips</td><td>&lt;Double></td><td>Read-only</td><td>Keeps track of number of flips that have happened till now in current interval.</td><tr><tr><td>completedfliptime</td><td>&lt;Double></td><td>Read-only</td><td>To inform user whether flip time is elapsed or not.</td><tr><tr><td>routemonitorstate</td><td>&lt;String></td><td>Read-only</td><td>State for route monitor.&lt;br>Possible values = UP, DOWN</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [DELETE](#delete) | [UPDATE](#update) | [UNSET](#unset) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>},"sessionid":"##sessionid","hanode":{      "id":<Double_value>,      "ipaddress":<String_value>,      "inc":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/hanode/id_value&lt;Double&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/hanode/id_value&lt;Double&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","hanode":{      "id":<Double_value>,      "hastatus":<String_value>,      "hasync":<String_value>,      "haprop":<String_value>,      "hellointerval":<Double_value>,      "deadinterval":<Double_value>,      "failsafe":<String_value>,      "maxflips":<Double_value>,      "maxfliptime":<Double_value>,      "syncvlan":<Double_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","hanode":{      "id":<Double_value>,      "hastatus":true,      "hasync":true,      "haprop":true,      "hellointerval":true,      "deadinterval":true,      "failsafe":true,      "maxflips":true,      "maxfliptime":true,      "syncvlan":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/hanode
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/hanode?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of hanode resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/hanode?view=summary
Use this query-parameter to get the summary output of hanode resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/hanode?pagesize=#no;pageno=#no
Use this query-parameter to get the hanode resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/hanode?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "hanode": [ {      "id":<Double_value>,      "name":<String_value>,      "ipaddress":<String_value>,      "flags":<Double_value>,      "hastatus":<String_value>,      "state":<String_value>,      "hasync":<String_value>,      "haprop":<String_value>,      "enaifaces":<String_value>,      "disifaces":<String_value>,      "hamonifaces":<String_value>,      "pfifaces":<String_value>,      "ifaces":<String_value>,      "network":<String_value>,      "netmask":<String_value>,      "inc":<String_value>,      "ssl2":<String_value>,      "hellointerval":<Double_value>,      "deadinterval":<Double_value>,      "masterstatetime":<Double_value>,      "failsafe":<String_value>,      "routemonitor":<String_value>,      "maxflips":<Double_value>,      "maxfliptime":<Double_value>,      "curflips":<Double_value>,      "completedfliptime":<Double_value>,      "syncvlan":<Double_value>,      "routemonitorstate":<String_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/hanode/id_value&lt;Double&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "hanode": [ {      "id":<Double_value>,      "name":<String_value>,      "ipaddress":<String_value>,      "flags":<Double_value>,      "hastatus":<String_value>,      "state":<String_value>,      "hasync":<String_value>,      "haprop":<String_value>,      "enaifaces":<String_value>,      "disifaces":<String_value>,      "hamonifaces":<String_value>,      "pfifaces":<String_value>,      "ifaces":<String_value>,      "network":<String_value>,      "netmask":<String_value>,      "inc":<String_value>,      "ssl2":<String_value>,      "hellointerval":<Double_value>,      "deadinterval":<Double_value>,      "masterstatetime":<Double_value>,      "failsafe":<String_value>,      "routemonitor":<String_value>,      "maxflips":<Double_value>,      "maxfliptime":<Double_value>,      "curflips":<Double_value>,      "completedfliptime":<Double_value>,      "syncvlan":<Double_value>,      "routemonitorstate":<String_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/hanode?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",hanode: [ { "__count": "#no"} ] }


