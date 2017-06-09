#vxlan

Configuration for "VXLAN" resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>&lt;Double></td><td>Read-write</td><td>A positive integer, which is also called VXLAN Network Identifier (VNI), that uniquely identifies a VXLAN.&lt;br>Minimum value = 1&lt;br>Maximum value = 16777215</td><tr><tr><td>vlan</td><td>&lt;Double></td><td>Read-write</td><td>ID of VLANs whose traffic is allowed over this VXLAN. If you do not specify any VLAN IDs, the NetScaler allows traffic of all VLANs that are not part of any other VXLANs.&lt;br>Minimum value = 1&lt;br>Maximum value = 4094</td><tr><tr><td>port</td><td>&lt;Integer></td><td>Read-write</td><td>Specifies UDP destination port for VXLAN packets.&lt;br>Default value: 4789&lt;br>Minimum value = 1&lt;br>Maximum value = 65534</td><tr><tr><td>dynamicrouting</td><td>&lt;String></td><td>Read-write</td><td>Enable dynamic routing on this VXLAN.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>ipv6dynamicrouting</td><td>&lt;String></td><td>Read-write</td><td>Enable all IPv6 dynamic routing protocols on this VXLAN. Note: For the ENABLED setting to work, you must configure IPv6 dynamic routing protocols from the VTYSH command line.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>td</td><td>&lt;Double></td><td>Read-only</td><td>Integer value that uniquely identifies the traffic domain in which you want to configure the entity. If you do not specify an ID, the entity becomes part of the default traffic domain, which has an ID of 0.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
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
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>},"sessionid":"##sessionid","vxlan":{      "id":<Double_value>,      "vlan":<Double_value>,      "port":<Integer_value>,      "dynamicrouting":<String_value>,      "ipv6dynamicrouting":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/vxlan/id_value&lt;Double&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/vxlan/id_value&lt;Double&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","vxlan":{      "id":<Double_value>,      "vlan":<Double_value>,      "port":<Integer_value>,      "dynamicrouting":<String_value>,      "ipv6dynamicrouting":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","vxlan":{      "id":<Double_value>,      "vlan":true,      "port":true,      "dynamicrouting":true,      "ipv6dynamicrouting":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/vxlan
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/vxlan?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of vxlan resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/vxlan?view=summary
Use this query-parameter to get the summary output of vxlan resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/vxlan?pagesize=#no;pageno=#no
Use this query-parameter to get the vxlan resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/vxlan?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "vxlan": [ {      "id":<Double_value>,      "vlan":<Double_value>,      "port":<Integer_value>,      "dynamicrouting":<String_value>,      "ipv6dynamicrouting":<String_value>,      "td":<Double_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/vxlan/id_value&lt;Double&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "vxlan": [ {      "id":<Double_value>,      "vlan":<Double_value>,      "port":<Integer_value>,      "dynamicrouting":<String_value>,      "ipv6dynamicrouting":<String_value>,      "td":<Double_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/vxlan?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",vxlan: [ { "__count": "#no"} ] }


