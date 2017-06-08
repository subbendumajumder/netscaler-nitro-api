#auditnslogpolicy_binding

Binding object showing the resources that can be bound to auditnslogpolicy.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name of the policy.&lt;br>Minimum length = 1</td><tr><tr><td>auditnslogpolicy_csvserver_binding</td><td>&lt;auditnslogpolicy_csvserver_binding[]></td><td>Read-only</td><td>csvserver that can be bound to auditnslogpolicy.</td><tr><tr><td>auditnslogpolicy_tmglobal_binding</td><td>&lt;auditnslogpolicy_tmglobal_binding[]></td><td>Read-only</td><td>tmglobal that can be bound to auditnslogpolicy.</td><tr><tr><td>auditnslogpolicy_appfwglobal_binding</td><td>&lt;auditnslogpolicy_appfwglobal_binding[]></td><td>Read-only</td><td>appfwglobal that can be bound to auditnslogpolicy.</td><tr><tr><td>auditnslogpolicy_lbvserver_binding</td><td>&lt;auditnslogpolicy_lbvserver_binding[]></td><td>Read-only</td><td>lbvserver that can be bound to auditnslogpolicy.</td><tr><tr><td>auditnslogpolicy_aaauser_binding</td><td>&lt;auditnslogpolicy_aaauser_binding[]></td><td>Read-only</td><td>aaauser that can be bound to auditnslogpolicy.</td><tr><tr><td>auditnslogpolicy_vpnglobal_binding</td><td>&lt;auditnslogpolicy_vpnglobal_binding[]></td><td>Read-only</td><td>vpnglobal that can be bound to auditnslogpolicy.</td><tr><tr><td>auditnslogpolicy_vpnvserver_binding</td><td>&lt;auditnslogpolicy_vpnvserver_binding[]></td><td>Read-only</td><td>vpnvserver that can be bound to auditnslogpolicy.</td><tr><tr><td>auditnslogpolicy_systemglobal_binding</td><td>&lt;auditnslogpolicy_systemglobal_binding[]></td><td>Read-only</td><td>systemglobal that can be bound to auditnslogpolicy.</td><tr><tr><td>auditnslogpolicy_authenticationvserver_binding</td><td>&lt;auditnslogpolicy_authenticationvserver_binding[]></td><td>Read-only</td><td>authenticationvserver that can be bound to auditnslogpolicy.</td><tr><tr><td>auditnslogpolicy_aaagroup_binding</td><td>&lt;auditnslogpolicy_aaagroup_binding[]></td><td>Read-only</td><td>aaagroup that can be bound to auditnslogpolicy.</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[GET](#get)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/auditnslogpolicy_binding/name_value&lt;String&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "auditnslogpolicy_binding": [ {      "name":<String_value>,      "auditnslogpolicy_authenticationvserver_binding":<auditnslogpolicy_authenticationvserver_binding[]_value>,      "auditnslogpolicy_systemglobal_binding":<auditnslogpolicy_systemglobal_binding[]_value>,      "auditnslogpolicy_aaagroup_binding":<auditnslogpolicy_aaagroup_binding[]_value>,      "auditnslogpolicy_vpnvserver_binding":<auditnslogpolicy_vpnvserver_binding[]_value>,      "auditnslogpolicy_lbvserver_binding":<auditnslogpolicy_lbvserver_binding[]_value>,      "auditnslogpolicy_appfwglobal_binding":<auditnslogpolicy_appfwglobal_binding[]_value>,      "auditnslogpolicy_csvserver_binding":<auditnslogpolicy_csvserver_binding[]_value>,      "auditnslogpolicy_vpnglobal_binding":<auditnslogpolicy_vpnglobal_binding[]_value>,      "auditnslogpolicy_aaauser_binding":<auditnslogpolicy_aaauser_binding[]_value>,      "auditnslogpolicy_tmglobal_binding":<auditnslogpolicy_tmglobal_binding[]_value>,}]}```



