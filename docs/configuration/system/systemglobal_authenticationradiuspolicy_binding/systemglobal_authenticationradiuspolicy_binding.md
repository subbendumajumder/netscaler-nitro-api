#systemglobal_authenticationradiuspolicy_binding

Binding object showing the authenticationradiuspolicy that can be bound to systemglobal.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>priority</td><td>&lt;Double></td><td>Read-write</td><td>The priority of the command policy.</td><tr><tr><td>builtin</td><td>&lt;String[]></td><td>Read-write</td><td>Indicates that a variable is a built-in (SYSTEM INTERNAL) type.&lt;br>Possible values = MODIFIABLE, DELETABLE, IMMUTABLE, PARTITION_ALL</td><tr><tr><td>policyname</td><td>&lt;String></td><td>Read-write</td><td>The name of the command policy.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-write</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD:](#add:) | [DELETE:](#delete:) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add:



URL: http://NS_IP/nitro/v1/config
HTTP Method: PUT
Request Payload: ```{"params":{      "warning":<String_value>,      "onerror":<String_value>},sessionid":"##sessionid","systemglobal_authenticationradiuspolicy_binding":{      "policyname":<String_value>,                  "priority":<Double_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete:



URL: http://NS_IP/nitro/v1/config/systemglobal_authenticationradiuspolicy_binding
HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/systemglobal_authenticationradiuspolicy_binding
Query-parameters:
filter
http://&lt;NS_IP&gt;/nitro/v1/config/systemglobal_authenticationradiuspolicy_binding?filter=property-name1:property-value1,property-name2:property-value2
Use this query-parameter to get the filtered set of systemglobal_authenticationradiuspolicy_binding resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/systemglobal_authenticationradiuspolicy_binding?pagesize=#no;pageno=#no
Use this query-parameter to get the systemglobal_authenticationradiuspolicy_binding resources in chunks.



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "systemglobal_authenticationradiuspolicy_binding": [ {      "priority":<Double_value>,      "builtin":<String[]_value>,      "policyname":<String_value>,}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/systemglobal_authenticationradiuspolicy_binding?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",systemglobal_authenticationradiuspolicy_binding: [ { "__count": "#no"} ] }


