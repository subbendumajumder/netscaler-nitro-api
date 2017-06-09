#vpnvserver_feopolicy_binding

Binding object showing the feopolicy that can be bound to vpnvserver.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>priority</td><td>&lt;Double></td><td>Read-write</td><td>The priority, if any, of the VPN virtual server policy.</td><tr><tr><td>gotopriorityexpression</td><td>&lt;String></td><td>Read-write</td><td>Next priority expression.</td><tr><tr><td>policy</td><td>&lt;String></td><td>Read-write</td><td>Name of a policy to bind to the virtual server (for example, the name of an authentication, session, or endpoint analysis policy).&lt;br>Minimum length = 1</td><tr><tr><td>groupextraction</td><td>&lt;Boolean></td><td>Read-write</td><td>Binds the authentication policy to a tertiary chain which will be used only for group extraction. The user will not authenticate against this server, and this will only be called if primary and/or secondary authentication has succeeded.</td><tr><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name of the virtual server.&lt;br>Minimum length = 1</td><tr><tr><td>secondary</td><td>&lt;Boolean></td><td>Read-write</td><td>Binds the authentication policy as the secondary policy to use in a two-factor configuration. A user must then authenticate not only via a primary authentication method but also via a secondary authentication method. User groups are aggregated across both. The user name must be exactly the same for both authentication methods, but they can require different passwords.</td><tr><tr><td>bindpoint</td><td>&lt;String></td><td>Read-write</td><td>Bindpoint to which the policy is bound.&lt;br>Possible values = REQUEST, RESPONSE, ICA_REQUEST, OTHERTCP_REQUEST</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-write</td><td>count parameter</td><tr></tbody></table>
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
Request Payload: ```{"params":{      "warning":<String_value>,      "onerror":<String_value>},sessionid":"##sessionid","vpnvserver_feopolicy_binding":{      "name":<String_value>,      "policy":<String_value>,                  "priority":<Double_value>,                  "secondary":<Boolean_value>,                  "groupextraction":<Boolean_value>,                  "gotopriorityexpression":<String_value>,                  "bindpoint":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete:



URL: http://&lt;NS_IP&gt;/nitro/v1/config/vpnvserver_feopolicy_binding/name_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/vpnvserver_feopolicy_binding/name_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/vpnvserver_feopolicy_binding/name_value&lt;String&gt;
Query-parameters:
filter
http://&lt;NS_IP&gt;/nitro/v1/config/vpnvserver_feopolicy_binding/name_value&lt;String&gt;?filter=property-name1:property-value1,property-name2:property-value2
Use this query-parameter to get the filtered set of vpnvserver_feopolicy_binding resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/vpnvserver_feopolicy_binding/name_value&lt;String&gt;?pagesize=#no;pageno=#no
Use this query-parameter to get the vpnvserver_feopolicy_binding resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/vpnvserver_feopolicy_binding?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "vpnvserver_feopolicy_binding": [ {      "priority":<Double_value>,      "gotopriorityexpression":<String_value>,      "policy":<String_value>,      "groupextraction":<Boolean_value>,      "name":<String_value>,      "secondary":<Boolean_value>,      "bindpoint":<String_value>,}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/vpnvserver_feopolicy_binding/name_value&lt;String&gt;?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",vpnvserver_feopolicy_binding: [ { "__count": "#no"} ] }


