#aaagroup_binding

Binding object showing the resources that can be bound to aaagroup.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>groupname</td><td>&lt;String></td><td>Read-write</td><td>Name of the group.&lt;br>Minimum length = 1</td><tr><tr><td>aaagroup_auditnslogpolicy_binding</td><td>&lt;aaagroup_auditnslogpolicy_binding[]></td><td>Read-only</td><td>auditnslogpolicy that can be bound to aaagroup.</td><tr><tr><td>aaagroup_intranetip6_binding</td><td>&lt;aaagroup_intranetip6_binding[]></td><td>Read-only</td><td>intranetip6 that can be bound to aaagroup.</td><tr><tr><td>aaagroup_vpnsessionpolicy_binding</td><td>&lt;aaagroup_vpnsessionpolicy_binding[]></td><td>Read-only</td><td>vpnsessionpolicy that can be bound to aaagroup.</td><tr><tr><td>aaagroup_intranetip_binding</td><td>&lt;aaagroup_intranetip_binding[]></td><td>Read-only</td><td>intranetip that can be bound to aaagroup.</td><tr><tr><td>aaagroup_aaauser_binding</td><td>&lt;aaagroup_aaauser_binding[]></td><td>Read-only</td><td>aaauser that can be bound to aaagroup.</td><tr><tr><td>aaagroup_vpntrafficpolicy_binding</td><td>&lt;aaagroup_vpntrafficpolicy_binding[]></td><td>Read-only</td><td>vpntrafficpolicy that can be bound to aaagroup.</td><tr><tr><td>aaagroup_vpnintranetapplication_binding</td><td>&lt;aaagroup_vpnintranetapplication_binding[]></td><td>Read-only</td><td>vpnintranetapplication that can be bound to aaagroup.</td><tr><tr><td>aaagroup_authorizationpolicy_binding</td><td>&lt;aaagroup_authorizationpolicy_binding[]></td><td>Read-only</td><td>authorizationpolicy that can be bound to aaagroup.</td><tr><tr><td>aaagroup_auditsyslogpolicy_binding</td><td>&lt;aaagroup_auditsyslogpolicy_binding[]></td><td>Read-only</td><td>auditsyslogpolicy that can be bound to aaagroup.</td><tr><tr><td>aaagroup_vpnurl_binding</td><td>&lt;aaagroup_vpnurl_binding[]></td><td>Read-only</td><td>vpnurl that can be bound to aaagroup.</td><tr><tr><td>aaagroup_tmsessionpolicy_binding</td><td>&lt;aaagroup_tmsessionpolicy_binding[]></td><td>Read-only</td><td>tmsessionpolicy that can be bound to aaagroup.</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[GET](#get)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/aaagroup_binding/groupname_value&lt;String&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "aaagroup_binding": [ {      "groupname":<String_value>,      "aaagroup_vpntrafficpolicy_binding":<aaagroup_vpntrafficpolicy_binding[]_value>,      "aaagroup_authorizationpolicy_binding":<aaagroup_authorizationpolicy_binding[]_value>,      "aaagroup_intranetip_binding":<aaagroup_intranetip_binding[]_value>,      "aaagroup_intranetip6_binding":<aaagroup_intranetip6_binding[]_value>,      "aaagroup_auditnslogpolicy_binding":<aaagroup_auditnslogpolicy_binding[]_value>,      "aaagroup_vpnurl_binding":<aaagroup_vpnurl_binding[]_value>,      "aaagroup_auditsyslogpolicy_binding":<aaagroup_auditsyslogpolicy_binding[]_value>,      "aaagroup_aaauser_binding":<aaagroup_aaauser_binding[]_value>,      "aaagroup_tmsessionpolicy_binding":<aaagroup_tmsessionpolicy_binding[]_value>,      "aaagroup_vpnsessionpolicy_binding":<aaagroup_vpnsessionpolicy_binding[]_value>,      "aaagroup_vpnintranetapplication_binding":<aaagroup_vpnintranetapplication_binding[]_value>,}]}```



