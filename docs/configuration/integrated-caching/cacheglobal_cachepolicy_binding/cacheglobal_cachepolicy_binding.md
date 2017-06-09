#cacheglobal_cachepolicy_binding

Binding object showing the cachepolicy that can be bound to cacheglobal.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>priority</td><td>&lt;Double></td><td>Read-write</td><td>Specifies the priority of the policy.</td><tr><tr><td>globalbindtype</td><td>&lt;String></td><td>Read-write</td><td>.&lt;br>Default value: SYSTEM_GLOBAL&lt;br>Possible values = SYSTEM_GLOBAL, VPN_GLOBAL, RNAT_GLOBAL</td><tr><tr><td>gotopriorityexpression</td><td>&lt;String></td><td>Read-write</td><td>Expression specifying the priority of the next policy which will get evaluated if the current policy rule evaluates to TRUE.</td><tr><tr><td>policy</td><td>&lt;String></td><td>Read-write</td><td>Name of the cache policy.</td><tr><tr><td>type</td><td>&lt;String></td><td>Read-write</td><td>The bind point to which policy is bound. When you specify the type, detailed information about that bind point appears.&lt;br>Possible values = REQ_OVERRIDE, REQ_DEFAULT, RES_OVERRIDE, RES_DEFAULT</td><tr><tr><td>precededefrules</td><td>&lt;String></td><td>Read-write</td><td>Specify whether this policy should be evaluated.&lt;br>Default value: NO&lt;br>Possible values = YES, NO</td><tr><tr><td>labeltype</td><td>&lt;String></td><td>Read-write</td><td>Type of policy label to invoke.&lt;br>Possible values = reqvserver, resvserver, policylabel</td><tr><tr><td>labelname</td><td>&lt;String></td><td>Read-write</td><td>Name of the label to invoke if the current policy rule evaluates to TRUE. (To invoke a label associated with a virtual server, specify the name of the virtual server.).</td><tr><tr><td>invoke</td><td>&lt;Boolean></td><td>Read-write</td><td>Invoke policies bound to a virtual server or a user-defined policy label. After the invoked policies are evaluated, the flow returns to the policy with the next priority. Applicable only to default-syntax policies.</td><tr><tr><td>numpol</td><td>&lt;Double></td><td>Read-only</td><td>The number of policies bound to the bindpoint.</td><tr><tr><td>flowtype</td><td>&lt;Double></td><td>Read-only</td><td>flowtype of the bound cache policy.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
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
Request Payload: ```{"params":{      "warning":<String_value>,      "onerror":<String_value>},sessionid":"##sessionid","cacheglobal_cachepolicy_binding":{      "policy":<String_value>,                  "priority":<Double_value>,                  "precededefrules":<String_value>,                  "gotopriorityexpression":<String_value>,                  "type":<String_value>,                  "invoke":<Boolean_value>,                  "labeltype":<String_value>,                  "labelname":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete:



URL: http://NS_IP/nitro/v1/config/cacheglobal_cachepolicy_binding
HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/cacheglobal_cachepolicy_binding
Query-parameters:
filter
http://&lt;NS_IP&gt;/nitro/v1/config/cacheglobal_cachepolicy_binding?filter=property-name1:property-value1,property-name2:property-value2
Use this query-parameter to get the filtered set of cacheglobal_cachepolicy_binding resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/cacheglobal_cachepolicy_binding?pagesize=#no;pageno=#no
Use this query-parameter to get the cacheglobal_cachepolicy_binding resources in chunks.



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "cacheglobal_cachepolicy_binding": [ {      "priority":<Double_value>,      "globalbindtype":<String_value>,      "gotopriorityexpression":<String_value>,      "policy":<String_value>,      "type":<String_value>,      "precededefrules":<String_value>,      "labeltype":<String_value>,      "labelname":<String_value>,      "invoke":<Boolean_value>,      "numpol":<Double_value>,      "flowtype":<Double_value>,}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/cacheglobal_cachepolicy_binding?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",cacheglobal_cachepolicy_binding: [ { "__count": "#no"} ] }


