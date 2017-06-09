#iptunnel

Configuration for ip Tunnel resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the IP tunnel. Leading character must be a number or letter. Other characters allowed, after the first character, are @ _ - . (period) : (colon) # and space ( ).&lt;br>Minimum length = 1</td><tr><tr><td>remote</td><td>&lt;String></td><td>Read-write</td><td>Public IPv4 address, of the remote device, used to set up the tunnel. For this parameter, you can alternatively specify a network address.&lt;br>Minimum length = 1</td><tr><tr><td>remotesubnetmask</td><td>&lt;String></td><td>Read-write</td><td>Subnet mask of the remote IP address of the tunnel.</td><tr><tr><td>local</td><td>&lt;String></td><td>Read-write</td><td>Type ofNetScaler owned public IPv4 address, configured on the local NetScaler appliance and used to set up the tunnel.</td><tr><tr><td>protocol</td><td>&lt;String></td><td>Read-write</td><td>Name of the protocol to be used on this tunnel.&lt;br>Default value: IPIP&lt;br>Possible values = IPIP, GRE, IPSEC, VXLAN</td><tr><tr><td>grepayload</td><td>&lt;String></td><td>Read-write</td><td>The payload GRE will carry.&lt;br>Default value: ETHERNETwithDOT1Q&lt;br>Possible values = ETHERNETwithDOT1Q, ETHERNET, IP</td><tr><tr><td>ipsecprofilename</td><td>&lt;String></td><td>Read-write</td><td>Name of IPSec profile to be associated.&lt;br>Default value: "ns_ipsec_default_profile"</td><tr><tr><td>vlan</td><td>&lt;Double></td><td>Read-write</td><td>The vlan for mulicast packets.&lt;br>Minimum value = 1&lt;br>Maximum value = 4094</td><tr><tr><td>ownergroup</td><td>&lt;String></td><td>Read-write</td><td>The owner node group in a Cluster for the iptunnel.&lt;br>Default value: DEFAULT_NG&lt;br>Minimum length = 1</td><tr><tr><td>sysname</td><td>&lt;String></td><td>Read-only</td><td>The name of the ip tunnel.</td><tr><tr><td>type</td><td>&lt;Double></td><td>Read-only</td><td>The type of this tunnel.</td><tr><tr><td>encapip</td><td>&lt;String></td><td>Read-only</td><td>The effective local IP address of the tunnel. Used as the source of the encapsulated packets.</td><tr><tr><td>channel</td><td>&lt;Double></td><td>Read-only</td><td>The tunnel that is bound to a netbridge.</td><tr><tr><td>tunneltype</td><td>&lt;String[]></td><td>Read-only</td><td>Indicates that a tunnel is User-Configured, Internal or DELETE-IN-PROGRESS.&lt;br>Possible values = Configured, Delete-In-Progress</td><tr><tr><td>ipsectunnelstatus</td><td>&lt;String></td><td>Read-only</td><td>Whether the ipsec on this tunnel is up or down.&lt;br>Possible values = DOWN, UP, PARTIAL-UP, UNKNOWN</td><tr><tr><td>pbrname</td><td>&lt;String></td><td>Read-only</td><td>Name for the PBR.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [DELETE](#delete) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>},"sessionid":"##sessionid","iptunnel":{      "name":<String_value>,      "remote":<String_value>,      "remotesubnetmask":<String_value>,      "local":<String_value>,      "protocol":<String_value>,      "grepayload":<String_value>,      "ipsecprofilename":<String_value>,      "vlan":<Double_value>,      "ownergroup":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/iptunnel/name_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/iptunnel/name_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/iptunnel
Query-parameters:
args
http://&lt;NSIP&gt;/nitro/v1/config/iptunnel?args=      "remote":&lt;String_value&gt;,                  "remotesubnetmask":&lt;String_value&gt;,      "name":&lt;String_value&gt;,
Use this query-parameter to get iptunnel resources based on additional properties.


filter
http://&lt;NSIP&gt;/nitro/v1/config/iptunnel?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of iptunnel resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/iptunnel?view=summary
Use this query-parameter to get the summary output of iptunnel resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/iptunnel?pagesize=#no;pageno=#no
Use this query-parameter to get the iptunnel resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/iptunnel?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "iptunnel": [ {      "remote":<String_value>,                  "remotesubnetmask":<String_value>,      "name":<String_value>,      "sysname":<String_value>,      "local":<String_value>,      "protocol":<String_value>,      "grepayload":<String_value>,      "type":<Double_value>,      "encapip":<String_value>,      "channel":<Double_value>,      "ipsecprofilename":<String_value>,      "vlan":<Double_value>,      "tunneltype":<String[]_value>,      "ipsectunnelstatus":<String_value>,      "pbrname":<String_value>,      "ownergroup":<String_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/iptunnel/name_value&lt;String&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "iptunnel": [ {      "remote":<String_value>,                  "remotesubnetmask":<String_value>,      "name":<String_value>,      "sysname":<String_value>,      "local":<String_value>,      "protocol":<String_value>,      "grepayload":<String_value>,      "type":<Double_value>,      "encapip":<String_value>,      "channel":<Double_value>,      "ipsecprofilename":<String_value>,      "vlan":<Double_value>,      "tunneltype":<String[]_value>,      "ipsectunnelstatus":<String_value>,      "pbrname":<String_value>,      "ownergroup":<String_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/iptunnel?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",iptunnel: [ { "__count": "#no"} ] }


