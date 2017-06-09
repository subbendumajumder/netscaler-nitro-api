#appfwglobal_appfwpolicy_binding

Binding object showing the appfwpolicy that can be bound to appfwglobal.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>priority</td><td>&lt;Double></td><td>Read-write</td><td>The priority of the policy.</td><tr><tr><td>globalbindtype</td><td>&lt;String></td><td>Read-write</td><td>.&lt;br>Default value: SYSTEM_GLOBAL&lt;br>Possible values = SYSTEM_GLOBAL, VPN_GLOBAL, RNAT_GLOBAL</td><tr><tr><td>policyname</td><td>&lt;String></td><td>Read-write</td><td>Name of the policy.</td><tr><tr><td>labelname</td><td>&lt;String></td><td>Read-write</td><td>Name of the policy label to invoke if the current policy evaluates to TRUE, the invoke parameter is set, and Label Type is set to Policy Label.</td><tr><tr><td>state</td><td>&lt;String></td><td>Read-write</td><td>Enable or disable the binding to activate or deactivate the policy. This is applicable to classic policies only.&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>gotopriorityexpression</td><td>&lt;String></td><td>Read-write</td><td>Expression specifying the priority of the next policy which will get evaluated if the current policy rule evaluates to TRUE.</td><tr><tr><td>type</td><td>&lt;String></td><td>Read-write</td><td>Bind point to which to policy is bound.&lt;br>Possible values = REQ_OVERRIDE, REQ_DEFAULT, NONE</td><tr><tr><td>invoke</td><td>&lt;Boolean></td><td>Read-write</td><td>If the current policy evaluates to TRUE, terminate evaluation of policies bound to the current policy label, and then forward the request to the specified virtual server or evaluate the specified policy label.</td><tr><tr><td>labeltype</td><td>&lt;String></td><td>Read-write</td><td>Type of policy label invocation.&lt;br>Possible values = reqvserver, policylabel</td><tr><tr><td>flowtype</td><td>&lt;Double></td><td>Read-only</td><td>flowtype of the bound application firewall policy.</td><tr><tr><td>numpol</td><td>&lt;Double></td><td>Read-only</td><td>The number of policies bound to the bindpoint.</td><tr><tr><td>policytype</td><td>&lt;String></td><td>Read-only</td><td>.&lt;br>Possible values = Classic Policy, Advanced Policy</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
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
Request Payload: ```{"params":{      "warning":<String_value>,      "onerror":<String_value>},sessionid":"##sessionid","appfwglobal_appfwpolicy_binding":{      "policyname":<String_value>,                  "priority":<Double_value>,                  "state":<String_value>,                  "gotopriorityexpression":<String_value>,                  "type":<String_value>,                  "invoke":<Boolean_value>,                  "labeltype":<String_value>,                  "labelname":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete:



URL: http://NS_IP/nitro/v1/config/appfwglobal_appfwpolicy_binding
HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/appfwglobal_appfwpolicy_binding
Query-parameters:
filter
http://&lt;NS_IP&gt;/nitro/v1/config/appfwglobal_appfwpolicy_binding?filter=property-name1:property-value1,property-name2:property-value2
Use this query-parameter to get the filtered set of appfwglobal_appfwpolicy_binding resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/appfwglobal_appfwpolicy_binding?pagesize=#no;pageno=#no
Use this query-parameter to get the appfwglobal_appfwpolicy_binding resources in chunks.



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "appfwglobal_appfwpolicy_binding": [ {      "priority":<Double_value>,      "globalbindtype":<String_value>,      "policyname":<String_value>,      "labelname":<String_value>,      "state":<String_value>,      "gotopriorityexpression":<String_value>,      "type":<String_value>,      "invoke":<Boolean_value>,      "labeltype":<String_value>,      "flowtype":<Double_value>,      "numpol":<Double_value>,      "policytype":<String_value>,}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/appfwglobal_appfwpolicy_binding?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",appfwglobal_appfwpolicy_binding: [ { "__count": "#no"} ] }


