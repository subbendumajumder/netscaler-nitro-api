#aaauser_binding

Binding object which returns the resources bound to aaauser.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>username</td><td>&lt;String></td><td>Read-write</td><td>Name of the user who has the account.<br>Minimum length = 1</td></tr><tr><td>aaauser_auditnslogpolicy_binding</td><td>&lt;aaauser_auditnslogpolicy_binding[]></td><td>Read-only</td><td>auditnslogpolicy that can be bound to aaauser.</td></tr><tr><td>aaauser_intranetip6_binding</td><td>&lt;aaauser_intranetip6_binding[]></td><td>Read-only</td><td>intranetip6 that can be bound to aaauser.</td></tr><tr><td>aaauser_vpnsessionpolicy_binding</td><td>&lt;aaauser_vpnsessionpolicy_binding[]></td><td>Read-only</td><td>vpnsessionpolicy that can be bound to aaauser.</td></tr><tr><td>aaauser_authorizationpolicy_binding</td><td>&lt;aaauser_authorizationpolicy_binding[]></td><td>Read-only</td><td>authorizationpolicy that can be bound to aaauser.</td></tr><tr><td>aaauser_intranetip_binding</td><td>&lt;aaauser_intranetip_binding[]></td><td>Read-only</td><td>intranetip that can be bound to aaauser.</td></tr><tr><td>aaauser_auditsyslogpolicy_binding</td><td>&lt;aaauser_auditsyslogpolicy_binding[]></td><td>Read-only</td><td>auditsyslogpolicy that can be bound to aaauser.</td></tr><tr><td>aaauser_aaagroup_binding</td><td>&lt;aaauser_aaagroup_binding[]></td><td>Read-only</td><td>aaagroup that can be bound to aaauser.</td></tr><tr><td>aaauser_vpnurl_binding</td><td>&lt;aaauser_vpnurl_binding[]></td><td>Read-only</td><td>vpnurl that can be bound to aaauser.</td></tr><tr><td>aaauser_vpntrafficpolicy_binding</td><td>&lt;aaauser_vpntrafficpolicy_binding[]></td><td>Read-only</td><td>vpntrafficpolicy that can be bound to aaauser.</td></tr><tr><td>aaauser_vpnintranetapplication_binding</td><td>&lt;aaauser_vpnintranetapplication_binding[]></td><td>Read-only</td><td>vpnintranetapplication that can be bound to aaauser.</td></tr><tr><td>aaauser_tmsessionpolicy_binding</td><td>&lt;aaauser_tmsessionpolicy_binding[]></td><td>Read-only</td><td>tmsessionpolicy that can be bound to aaauser.</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[GET]()| [GET (ALL)](#get-)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/aaauser_binding/username_value&lt;String&gt;
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "aaauser_binding": [ {"username":<String_value>,"aaauser_authorizationpolicy_binding":<aaauser_authorizationpolicy_binding[]_value>,"aaauser_vpnurl_binding":<aaauser_vpnurl_binding[]_value>,"aaauser_vpntrafficpolicy_binding":<aaauser_vpntrafficpolicy_binding[]_value>,"aaauser_aaagroup_binding":<aaauser_aaagroup_binding[]_value>,"aaauser_vpnsessionpolicy_binding":<aaauser_vpnsessionpolicy_binding[]_value>,"aaauser_intranetip_binding":<aaauser_intranetip_binding[]_value>,"aaauser_intranetip6_binding":<aaauser_intranetip6_binding[]_value>,"aaauser_auditsyslogpolicy_binding":<aaauser_auditsyslogpolicy_binding[]_value>,"aaauser_tmsessionpolicy_binding":<aaauser_tmsessionpolicy_binding[]_value>,"aaauser_vpnintranetapplication_binding":<aaauser_vpnintranetapplication_binding[]_value>,"aaauser_auditnslogpolicy_binding":<aaauser_auditnslogpolicy_binding[]_value>}]}```



###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/aaauser_binding
<b>Query-parameters:</b>
<b>bulkbindings</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/aaauser_binding?<b>bulkbindings=yes</b>
NITRO allows you to fetch bindings in bulk.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "aaauser_binding": [ {"username":<String_value>,"aaauser_authorizationpolicy_binding":<aaauser_authorizationpolicy_binding[]_value>,"aaauser_vpnurl_binding":<aaauser_vpnurl_binding[]_value>,"aaauser_vpntrafficpolicy_binding":<aaauser_vpntrafficpolicy_binding[]_value>,"aaauser_aaagroup_binding":<aaauser_aaagroup_binding[]_value>,"aaauser_vpnsessionpolicy_binding":<aaauser_vpnsessionpolicy_binding[]_value>,"aaauser_intranetip_binding":<aaauser_intranetip_binding[]_value>,"aaauser_intranetip6_binding":<aaauser_intranetip6_binding[]_value>,"aaauser_auditsyslogpolicy_binding":<aaauser_auditsyslogpolicy_binding[]_value>,"aaauser_tmsessionpolicy_binding":<aaauser_tmsessionpolicy_binding[]_value>,"aaauser_vpnintranetapplication_binding":<aaauser_vpnintranetapplication_binding[]_value>,"aaauser_auditnslogpolicy_binding":<aaauser_auditnslogpolicy_binding[]_value>}]}```



