#vrid6

Configuration for Virtual Router ID for IPv6 resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>&lt;Double></td><td>Read-write</td><td>Integer value that uniquely identifies a VMAC6 address.&lt;br>Minimum value = 1&lt;br>Maximum value = 255</td><tr><tr><td>all</td><td>&lt;Boolean></td><td>Read-write</td><td>Remove all configured VMAC6 addresses from the NetScaler appliance.</td><tr><tr><td>ifaces</td><td>&lt;String></td><td>Read-only</td><td>Interfaces bound to this VRID.</td><tr><tr><td>ifnum</td><td>&lt;String></td><td>Read-only</td><td>Interfaces bound to this vrid.</td><tr><tr><td>type</td><td>&lt;String></td><td>Read-only</td><td>Type (static or dynamic) of this VRID.&lt;br>Possible values = STATIC, DYNAMIC</td><tr><tr><td>priority</td><td>&lt;Double></td><td>Read-only</td><td>The priority of this VRID.</td><tr><tr><td>state</td><td>&lt;Double></td><td>Read-only</td><td>State of this VRID.</td><tr><tr><td>flags</td><td>&lt;Double></td><td>Read-only</td><td>Flags.</td><tr><tr><td>ipaddress</td><td>&lt;String></td><td>Read-only</td><td>The IP address bound to the VRID6.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
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
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>},"sessionid":"##sessionid","vrid6":{      "id":<Double_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/vrid6/id_value&lt;Double&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/vrid6/id_value&lt;Double&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/vrid6
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/vrid6?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of vrid6 resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/vrid6?view=summary
Use this query-parameter to get the summary output of vrid6 resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/vrid6?pagesize=#no;pageno=#no
Use this query-parameter to get the vrid6 resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/vrid6?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "vrid6": [ {      "id":<Double_value>,      "ifaces":<String_value>,      "ifnum":<String_value>,      "type":<String_value>,      "priority":<Double_value>,      "state":<Double_value>,      "flags":<Double_value>,      "ipaddress":<String_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/vrid6/id_value&lt;Double&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "vrid6": [ {      "id":<Double_value>,      "ifaces":<String_value>,      "ifnum":<String_value>,      "type":<String_value>,      "priority":<Double_value>,      "state":<Double_value>,      "flags":<Double_value>,      "ipaddress":<String_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/vrid6?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",vrid6: [ { "__count": "#no"} ] }


