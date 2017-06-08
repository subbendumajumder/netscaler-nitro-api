#clusternodegroup_binding

Binding object showing the resources that can be bound to clusternodegroup.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name of the nodegroup to be displayed. If a name is not provided, information about all nodegroups is displayed.&lt;br>Minimum length = 1</td><tr><tr><td>clusternodegroup_csvserver_binding</td><td>&lt;clusternodegroup_csvserver_binding[]></td><td>Read-only</td><td>csvserver that can be bound to clusternodegroup.</td><tr><tr><td>clusternodegroup_gslbsite_binding</td><td>&lt;clusternodegroup_gslbsite_binding[]></td><td>Read-only</td><td>gslbsite that can be bound to clusternodegroup.</td><tr><tr><td>clusternodegroup_nslimitidentifier_binding</td><td>&lt;clusternodegroup_nslimitidentifier_binding[]></td><td>Read-only</td><td>nslimitidentifier that can be bound to clusternodegroup.</td><tr><tr><td>clusternodegroup_clusternode_binding</td><td>&lt;clusternodegroup_clusternode_binding[]></td><td>Read-only</td><td>clusternode that can be bound to clusternodegroup.</td><tr><tr><td>clusternodegroup_lbvserver_binding</td><td>&lt;clusternodegroup_lbvserver_binding[]></td><td>Read-only</td><td>lbvserver that can be bound to clusternodegroup.</td><tr><tr><td>clusternodegroup_vpnvserver_binding</td><td>&lt;clusternodegroup_vpnvserver_binding[]></td><td>Read-only</td><td>vpnvserver that can be bound to clusternodegroup.</td><tr><tr><td>clusternodegroup_service_binding</td><td>&lt;clusternodegroup_service_binding[]></td><td>Read-only</td><td>service that can be bound to clusternodegroup.</td><tr><tr><td>clusternodegroup_streamidentifier_binding</td><td>&lt;clusternodegroup_streamidentifier_binding[]></td><td>Read-only</td><td>streamidentifier that can be bound to clusternodegroup.</td><tr><tr><td>clusternodegroup_gslbvserver_binding</td><td>&lt;clusternodegroup_gslbvserver_binding[]></td><td>Read-only</td><td>gslbvserver that can be bound to clusternodegroup.</td><tr><tr><td>clusternodegroup_authenticationvserver_binding</td><td>&lt;clusternodegroup_authenticationvserver_binding[]></td><td>Read-only</td><td>authenticationvserver that can be bound to clusternodegroup.</td><tr><tr><td>clusternodegroup_crvserver_binding</td><td>&lt;clusternodegroup_crvserver_binding[]></td><td>Read-only</td><td>crvserver that can be bound to clusternodegroup.</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[GET](#get)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/clusternodegroup_binding/name_value&lt;String&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "clusternodegroup_binding": [ {      "name":<String_value>,      "clusternodegroup_csvserver_binding":<clusternodegroup_csvserver_binding[]_value>,      "clusternodegroup_vpnvserver_binding":<clusternodegroup_vpnvserver_binding[]_value>,      "clusternodegroup_crvserver_binding":<clusternodegroup_crvserver_binding[]_value>,      "clusternodegroup_nslimitidentifier_binding":<clusternodegroup_nslimitidentifier_binding[]_value>,      "clusternodegroup_gslbsite_binding":<clusternodegroup_gslbsite_binding[]_value>,      "clusternodegroup_clusternode_binding":<clusternodegroup_clusternode_binding[]_value>,      "clusternodegroup_authenticationvserver_binding":<clusternodegroup_authenticationvserver_binding[]_value>,      "clusternodegroup_lbvserver_binding":<clusternodegroup_lbvserver_binding[]_value>,      "clusternodegroup_gslbvserver_binding":<clusternodegroup_gslbvserver_binding[]_value>,      "clusternodegroup_streamidentifier_binding":<clusternodegroup_streamidentifier_binding[]_value>,      "clusternodegroup_service_binding":<clusternodegroup_service_binding[]_value>,}]}```



