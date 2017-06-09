#policypatset_pattern_binding

Binding object showing the pattern that can be bound to policypatset.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>String</td><td>&lt;String></td><td>Read-write</td><td>String of characters that constitutes a pattern. For more information about the characters that can be used, refer to the character set parameter. Note: Minimum length for pattern sets used in rewrite actions of type REPLACE_ALL, DELETE_ALL, INSERT_AFTER_ALL, and INSERT_BEFORE_ALL, is three characters.</td><tr><tr><td>builtin</td><td>&lt;String[]></td><td>Read-write</td><td>Indicates that a variable is a built-in (SYSTEM INTERNAL) type.&lt;br>Possible values = MODIFIABLE, DELETABLE, IMMUTABLE, PARTITION_ALL</td><tr><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name of the pattern set to which to bind the string.&lt;br>Minimum length = 1</td><tr><tr><td>charset</td><td>&lt;String></td><td>Read-write</td><td>Character set associated with the characters in the string. Note: UTF-8 characters can be entered directly (if the UI supports it) or can be encoded as a sequence of hexadecimal bytes \\xNN. For example, the UTF-8 character ? can be encoded as \\xC3\\xBC.&lt;br>Possible values = ASCII, UTF_8</td><tr><tr><td>index</td><td>&lt;Double></td><td>Read-write</td><td>The index of the string associated with the patset.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-write</td><td>count parameter</td><tr></tbody></table>
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
Request Payload: ```{"params":{      "warning":<String_value>,      "onerror":<String_value>},sessionid":"##sessionid","policypatset_pattern_binding":{      "name":<String_value>,      "String":<String_value>,                  "index":<Double_value>,                  "charset":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete:



URL: http://&lt;NS_IP&gt;/nitro/v1/config/policypatset_pattern_binding/name_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/policypatset_pattern_binding/name_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/policypatset_pattern_binding/name_value&lt;String&gt;
Query-parameters:
filter
http://&lt;NS_IP&gt;/nitro/v1/config/policypatset_pattern_binding/name_value&lt;String&gt;?filter=property-name1:property-value1,property-name2:property-value2
Use this query-parameter to get the filtered set of policypatset_pattern_binding resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/policypatset_pattern_binding/name_value&lt;String&gt;?pagesize=#no;pageno=#no
Use this query-parameter to get the policypatset_pattern_binding resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/policypatset_pattern_binding?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "policypatset_pattern_binding": [ {      "String":<String_value>,      "builtin":<String[]_value>,      "name":<String_value>,      "charset":<String_value>,      "index":<Double_value>,}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/policypatset_pattern_binding/name_value&lt;String&gt;?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",policypatset_pattern_binding: [ { "__count": "#no"} ] }


