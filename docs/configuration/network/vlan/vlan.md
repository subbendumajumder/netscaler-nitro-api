#vlan

Configuration for "VLAN" resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>&lt;Double></td><td>Read-write</td><td>A positive integer that uniquely identifies a VLAN.&lt;br>Minimum value = 1&lt;br>Maximum value = 4094</td><tr><tr><td>aliasname</td><td>&lt;String></td><td>Read-write</td><td>A name for the VLAN. Must begin with a letter, a number, or the underscore symbol, and can consist of from 1 to 31 letters, numbers, and the hyphen (-), period (.) pound (#), space ( ), at sign (@), equals (=), colon (:), and underscore (_) characters. You should choose a name that helps identify the VLAN. However, you cannot perform any VLAN operation by specifying this name instead of the VLAN ID.&lt;br>Maximum length = 31</td><tr><tr><td>ipv6dynamicrouting</td><td>&lt;String></td><td>Read-write</td><td>Enable all IPv6 dynamic routing protocols on this VLAN. Note: For the ENABLED setting to work, you must configure IPv6 dynamic routing protocols from the VTYSH command line.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>mtu</td><td>&lt;Double></td><td>Read-write</td><td>Specifies the maximum transmission unit (MTU), in bytes. The MTU is the largest packet size, excluding 14 bytes of ethernet header and 4 bytes of crc, that can be transmitted and received over this VLAN.&lt;br>Default value: 0&lt;br>Minimum value = 500&lt;br>Maximum value = 9216</td><tr><tr><td>linklocalipv6addr</td><td>&lt;String></td><td>Read-only</td><td>The link-local IP address assigned to the VLAN.</td><tr><tr><td>rnat</td><td>&lt;Boolean></td><td>Read-only</td><td>Temporary flag used for internal purpose.</td><tr><tr><td>portbitmap</td><td>&lt;Double></td><td>Read-only</td><td>Member interfaces of this vlan.</td><tr><tr><td>lsbitmap</td><td>&lt;Double></td><td>Read-only</td><td>Member linksets of this vlan.</td><tr><tr><td>tagbitmap</td><td>&lt;Double></td><td>Read-only</td><td>Tagged members of this vlan.</td><tr><tr><td>lstagbitmap</td><td>&lt;Double></td><td>Read-only</td><td>Tagged linksets of this vlan.</td><tr><tr><td>ifaces</td><td>&lt;String></td><td>Read-only</td><td>Names of all member interfaces of this vlan.</td><tr><tr><td>tagifaces</td><td>&lt;String></td><td>Read-only</td><td>Names of all tagged member interfaces of this vlan.</td><tr><tr><td>ifnum</td><td>&lt;String></td><td>Read-only</td><td>The interface to be bound to the VLAN, specified in slot/port notation (for example, 1/3).&lt;br>Minimum length = 1</td><tr><tr><td>tagged</td><td>&lt;Boolean></td><td>Read-only</td><td>Make the interface an 802.1q tagged interface. Packets sent on this interface on this VLAN have an additional 4-byte 802.1q tag, which identifies the VLAN. To use 802.1q tagging, you must also configure the switch connected to the appliances interfaces.</td><tr><tr><td>vlantd</td><td>&lt;Double></td><td>Read-only</td><td>Traffic domain associated with vlan.&lt;br>Minimum value = 0&lt;br>Maximum value = 4094</td><tr><tr><td>sdxvlan</td><td>&lt;String></td><td>Read-only</td><td>SDX vlan.&lt;br>Default value: NO&lt;br>Possible values = YES, NO</td><tr><tr><td>vxlan</td><td>&lt;Double></td><td>Read-only</td><td>The VXLAN that extends this vlan.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
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
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>},"sessionid":"##sessionid","vlan":{      "id":<Double_value>,      "aliasname":<String_value>,      "ipv6dynamicrouting":<String_value>,      "mtu":<Double_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/vlan/id_value&lt;Double&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/vlan/id_value&lt;Double&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","vlan":{      "id":<Double_value>,      "aliasname":<String_value>,      "ipv6dynamicrouting":<String_value>,      "mtu":<Double_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","vlan":{      "id":<Double_value>,      "aliasname":true,      "ipv6dynamicrouting":true,      "mtu":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/vlan
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/vlan?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of vlan resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/vlan?view=summary
Use this query-parameter to get the summary output of vlan resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/vlan?pagesize=#no;pageno=#no
Use this query-parameter to get the vlan resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/vlan?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "vlan": [ {      "id":<Double_value>,      "aliasname":<String_value>,      "linklocalipv6addr":<String_value>,      "rnat":<Boolean_value>,      "portbitmap":<Double_value>,      "lsbitmap":<Double_value>,      "tagbitmap":<Double_value>,      "lstagbitmap":<Double_value>,      "ifaces":<String_value>,      "tagifaces":<String_value>,      "ipv6dynamicrouting":<String_value>,      "ifnum":<String_value>,      "tagged":<Boolean_value>,      "vlantd":<Double_value>,      "sdxvlan":<String_value>,      "mtu":<Double_value>,      "vxlan":<Double_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/vlan/id_value&lt;Double&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "vlan": [ {      "id":<Double_value>,      "aliasname":<String_value>,      "linklocalipv6addr":<String_value>,      "rnat":<Boolean_value>,      "portbitmap":<Double_value>,      "lsbitmap":<Double_value>,      "tagbitmap":<Double_value>,      "lstagbitmap":<Double_value>,      "ifaces":<String_value>,      "tagifaces":<String_value>,      "ipv6dynamicrouting":<String_value>,      "ifnum":<String_value>,      "tagged":<Boolean_value>,      "vlantd":<Double_value>,      "sdxvlan":<String_value>,      "mtu":<Double_value>,      "vxlan":<Double_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/vlan?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",vlan: [ { "__count": "#no"} ] }


