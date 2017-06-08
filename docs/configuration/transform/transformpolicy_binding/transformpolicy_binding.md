#transformpolicy_binding

Binding object showing the resources that can be bound to transformpolicy.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name of the URL Transformation policy.&lt;br>Minimum length = 1</td><tr><tr><td>transformpolicy_csvserver_binding</td><td>&lt;transformpolicy_csvserver_binding[]></td><td>Read-only</td><td>csvserver that can be bound to transformpolicy.</td><tr><tr><td>transformpolicy_transformpolicylabel_binding</td><td>&lt;transformpolicy_transformpolicylabel_binding[]></td><td>Read-only</td><td>transformpolicylabel that can be bound to transformpolicy.</td><tr><tr><td>transformpolicy_lbvserver_binding</td><td>&lt;transformpolicy_lbvserver_binding[]></td><td>Read-only</td><td>lbvserver that can be bound to transformpolicy.</td><tr><tr><td>transformpolicy_transformglobal_binding</td><td>&lt;transformpolicy_transformglobal_binding[]></td><td>Read-only</td><td>transformglobal that can be bound to transformpolicy.</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[GET](#get)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/transformpolicy_binding/name_value&lt;String&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "transformpolicy_binding": [ {      "name":<String_value>,      "transformpolicy_csvserver_binding":<transformpolicy_csvserver_binding[]_value>,      "transformpolicy_transformglobal_binding":<transformpolicy_transformglobal_binding[]_value>,      "transformpolicy_lbvserver_binding":<transformpolicy_lbvserver_binding[]_value>,      "transformpolicy_transformpolicylabel_binding":<transformpolicy_transformpolicylabel_binding[]_value>,}]}```



