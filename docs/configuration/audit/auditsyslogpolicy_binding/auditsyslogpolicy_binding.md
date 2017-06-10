#auditsyslogpolicy_binding

Binding object which returns the resources bound to auditsyslogpolicy.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name of the policy.&lt;br>Minimum length = 1</td><tr><tr><td>auditsyslogpolicy_rnatglobal_binding</td><td>&lt;auditsyslogpolicy_rnatglobal_binding[]></td><td>Read-only</td><td>rnatglobal that can be bound to auditsyslogpolicy.</td><tr><tr><td>auditsyslogpolicy_vpnvserver_binding</td><td>&lt;auditsyslogpolicy_vpnvserver_binding[]></td><td>Read-only</td><td>vpnvserver that can be bound to auditsyslogpolicy.</td><tr><tr><td>auditsyslogpolicy_csvserver_binding</td><td>&lt;auditsyslogpolicy_csvserver_binding[]></td><td>Read-only</td><td>csvserver that can be bound to auditsyslogpolicy.</td><tr><tr><td>auditsyslogpolicy_tmglobal_binding</td><td>&lt;auditsyslogpolicy_tmglobal_binding[]></td><td>Read-only</td><td>tmglobal that can be bound to auditsyslogpolicy.</td><tr><tr><td>auditsyslogpolicy_systemglobal_binding</td><td>&lt;auditsyslogpolicy_systemglobal_binding[]></td><td>Read-only</td><td>systemglobal that can be bound to auditsyslogpolicy.</td><tr><tr><td>auditsyslogpolicy_lbvserver_binding</td><td>&lt;auditsyslogpolicy_lbvserver_binding[]></td><td>Read-only</td><td>lbvserver that can be bound to auditsyslogpolicy.</td><tr><tr><td>auditsyslogpolicy_authenticationvserver_binding</td><td>&lt;auditsyslogpolicy_authenticationvserver_binding[]></td><td>Read-only</td><td>authenticationvserver that can be bound to auditsyslogpolicy.</td><tr><tr><td>auditsyslogpolicy_aaagroup_binding</td><td>&lt;auditsyslogpolicy_aaagroup_binding[]></td><td>Read-only</td><td>aaagroup that can be bound to auditsyslogpolicy.</td><tr><tr><td>auditsyslogpolicy_aaauser_binding</td><td>&lt;auditsyslogpolicy_aaauser_binding[]></td><td>Read-only</td><td>aaauser that can be bound to auditsyslogpolicy.</td><tr><tr><td>auditsyslogpolicy_auditsyslogglobal_binding</td><td>&lt;auditsyslogpolicy_auditsyslogglobal_binding[]></td><td>Read-only</td><td>auditsyslogglobal that can be bound to auditsyslogpolicy.</td><tr><tr><td>auditsyslogpolicy_vpnglobal_binding</td><td>&lt;auditsyslogpolicy_vpnglobal_binding[]></td><td>Read-only</td><td>vpnglobal that can be bound to auditsyslogpolicy.</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[GET](#get) | [GET (ALL)](#get-(all))


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/auditsyslogpolicy_binding/name_value&lt;String&gt;
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "auditsyslogpolicy_binding": [ {      "name":<String_value>,      "auditsyslogpolicy_aaauser_binding":<auditsyslogpolicy_aaauser_binding[]_value>,      "auditsyslogpolicy_vpnglobal_binding":<auditsyslogpolicy_vpnglobal_binding[]_value>,      "auditsyslogpolicy_authenticationvserver_binding":<auditsyslogpolicy_authenticationvserver_binding[]_value>,      "auditsyslogpolicy_lbvserver_binding":<auditsyslogpolicy_lbvserver_binding[]_value>,      "auditsyslogpolicy_aaagroup_binding":<auditsyslogpolicy_aaagroup_binding[]_value>,      "auditsyslogpolicy_auditsyslogglobal_binding":<auditsyslogpolicy_auditsyslogglobal_binding[]_value>,      "auditsyslogpolicy_tmglobal_binding":<auditsyslogpolicy_tmglobal_binding[]_value>,      "auditsyslogpolicy_rnatglobal_binding":<auditsyslogpolicy_rnatglobal_binding[]_value>,      "auditsyslogpolicy_csvserver_binding":<auditsyslogpolicy_csvserver_binding[]_value>,      "auditsyslogpolicy_systemglobal_binding":<auditsyslogpolicy_systemglobal_binding[]_value>,      "auditsyslogpolicy_vpnvserver_binding":<auditsyslogpolicy_vpnvserver_binding[]_value>}]}```



###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/auditsyslogpolicy_binding
Query-parameters:
bulkbindings
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/auditsyslogpolicy_binding?bulkbindings=yes
NITRO allows you to fetch bindings in bulk.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "auditsyslogpolicy_binding": [ {      "name":<String_value>,      "auditsyslogpolicy_aaauser_binding":<auditsyslogpolicy_aaauser_binding[]_value>,      "auditsyslogpolicy_vpnglobal_binding":<auditsyslogpolicy_vpnglobal_binding[]_value>,      "auditsyslogpolicy_authenticationvserver_binding":<auditsyslogpolicy_authenticationvserver_binding[]_value>,      "auditsyslogpolicy_lbvserver_binding":<auditsyslogpolicy_lbvserver_binding[]_value>,      "auditsyslogpolicy_aaagroup_binding":<auditsyslogpolicy_aaagroup_binding[]_value>,      "auditsyslogpolicy_auditsyslogglobal_binding":<auditsyslogpolicy_auditsyslogglobal_binding[]_value>,      "auditsyslogpolicy_tmglobal_binding":<auditsyslogpolicy_tmglobal_binding[]_value>,      "auditsyslogpolicy_rnatglobal_binding":<auditsyslogpolicy_rnatglobal_binding[]_value>,      "auditsyslogpolicy_csvserver_binding":<auditsyslogpolicy_csvserver_binding[]_value>,      "auditsyslogpolicy_systemglobal_binding":<auditsyslogpolicy_systemglobal_binding[]_value>,      "auditsyslogpolicy_vpnvserver_binding":<auditsyslogpolicy_vpnvserver_binding[]_value>}]}```



