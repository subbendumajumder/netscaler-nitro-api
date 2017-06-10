#csvserver_binding

Binding object which returns the resources bound to csvserver.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name of a content switching virtual server for which to display information, including the policies bound to the virtual server. To display a list of all configured Content Switching virtual servers, do not specify a value for this parameter.&lt;br>Minimum length = 1</td><tr><tr><td>csvserver_spilloverpolicy_binding</td><td>&lt;csvserver_spilloverpolicy_binding[]></td><td>Read-only</td><td>spilloverpolicy that can be bound to csvserver.</td><tr><tr><td>csvserver_auditnslogpolicy_binding</td><td>&lt;csvserver_auditnslogpolicy_binding[]></td><td>Read-only</td><td>auditnslogpolicy that can be bound to csvserver.</td><tr><tr><td>csvserver_domain_binding</td><td>&lt;csvserver_domain_binding[]></td><td>Read-only</td><td>domain that can be bound to csvserver.</td><tr><tr><td>csvserver_filterpolicy_binding</td><td>&lt;csvserver_filterpolicy_binding[]></td><td>Read-only</td><td>filterpolicy that can be bound to csvserver.</td><tr><tr><td>csvserver_cmppolicy_binding</td><td>&lt;csvserver_cmppolicy_binding[]></td><td>Read-only</td><td>cmppolicy that can be bound to csvserver.</td><tr><tr><td>csvserver_lbvserver_binding</td><td>&lt;csvserver_lbvserver_binding[]></td><td>Read-only</td><td>lbvserver that can be bound to csvserver.</td><tr><tr><td>csvserver_appflowpolicy_binding</td><td>&lt;csvserver_appflowpolicy_binding[]></td><td>Read-only</td><td>appflowpolicy that can be bound to csvserver.</td><tr><tr><td>csvserver_responderpolicy_binding</td><td>&lt;csvserver_responderpolicy_binding[]></td><td>Read-only</td><td>responderpolicy that can be bound to csvserver.</td><tr><tr><td>csvserver_transformpolicy_binding</td><td>&lt;csvserver_transformpolicy_binding[]></td><td>Read-only</td><td>transformpolicy that can be bound to csvserver.</td><tr><tr><td>csvserver_vpnvserver_binding</td><td>&lt;csvserver_vpnvserver_binding[]></td><td>Read-only</td><td>vpnvserver that can be bound to csvserver.</td><tr><tr><td>csvserver_feopolicy_binding</td><td>&lt;csvserver_feopolicy_binding[]></td><td>Read-only</td><td>feopolicy that can be bound to csvserver.</td><tr><tr><td>csvserver_authorizationpolicy_binding</td><td>&lt;csvserver_authorizationpolicy_binding[]></td><td>Read-only</td><td>authorizationpolicy that can be bound to csvserver.</td><tr><tr><td>csvserver_cachepolicy_binding</td><td>&lt;csvserver_cachepolicy_binding[]></td><td>Read-only</td><td>cachepolicy that can be bound to csvserver.</td><tr><tr><td>csvserver_rewritepolicy_binding</td><td>&lt;csvserver_rewritepolicy_binding[]></td><td>Read-only</td><td>rewritepolicy that can be bound to csvserver.</td><tr><tr><td>csvserver_cspolicy_binding</td><td>&lt;csvserver_cspolicy_binding[]></td><td>Read-only</td><td>cspolicy that can be bound to csvserver.</td><tr><tr><td>csvserver_gslbvserver_binding</td><td>&lt;csvserver_gslbvserver_binding[]></td><td>Read-only</td><td>gslbvserver that can be bound to csvserver.</td><tr><tr><td>csvserver_appqoepolicy_binding</td><td>&lt;csvserver_appqoepolicy_binding[]></td><td>Read-only</td><td>appqoepolicy that can be bound to csvserver.</td><tr><tr><td>csvserver_tmtrafficpolicy_binding</td><td>&lt;csvserver_tmtrafficpolicy_binding[]></td><td>Read-only</td><td>tmtrafficpolicy that can be bound to csvserver.</td><tr><tr><td>csvserver_auditsyslogpolicy_binding</td><td>&lt;csvserver_auditsyslogpolicy_binding[]></td><td>Read-only</td><td>auditsyslogpolicy that can be bound to csvserver.</td><tr><tr><td>csvserver_appfwpolicy_binding</td><td>&lt;csvserver_appfwpolicy_binding[]></td><td>Read-only</td><td>appfwpolicy that can be bound to csvserver.</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[GET](#get) | [GET (ALL)](#get-(all))


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/csvserver_binding/name_value&lt;String&gt;
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "csvserver_binding": [ {      "name":<String_value>,      "csvserver_auditnslogpolicy_binding":<csvserver_auditnslogpolicy_binding[]_value>,      "csvserver_tmtrafficpolicy_binding":<csvserver_tmtrafficpolicy_binding[]_value>,      "csvserver_lbvserver_binding":<csvserver_lbvserver_binding[]_value>,      "csvserver_responderpolicy_binding":<csvserver_responderpolicy_binding[]_value>,      "csvserver_gslbvserver_binding":<csvserver_gslbvserver_binding[]_value>,      "csvserver_cachepolicy_binding":<csvserver_cachepolicy_binding[]_value>,      "csvserver_filterpolicy_binding":<csvserver_filterpolicy_binding[]_value>,      "csvserver_transformpolicy_binding":<csvserver_transformpolicy_binding[]_value>,      "csvserver_appflowpolicy_binding":<csvserver_appflowpolicy_binding[]_value>,      "csvserver_appfwpolicy_binding":<csvserver_appfwpolicy_binding[]_value>,      "csvserver_authorizationpolicy_binding":<csvserver_authorizationpolicy_binding[]_value>,      "csvserver_auditsyslogpolicy_binding":<csvserver_auditsyslogpolicy_binding[]_value>,      "csvserver_cmppolicy_binding":<csvserver_cmppolicy_binding[]_value>,      "csvserver_rewritepolicy_binding":<csvserver_rewritepolicy_binding[]_value>,      "csvserver_cspolicy_binding":<csvserver_cspolicy_binding[]_value>,      "csvserver_spilloverpolicy_binding":<csvserver_spilloverpolicy_binding[]_value>,      "csvserver_appqoepolicy_binding":<csvserver_appqoepolicy_binding[]_value>,      "csvserver_feopolicy_binding":<csvserver_feopolicy_binding[]_value>,      "csvserver_vpnvserver_binding":<csvserver_vpnvserver_binding[]_value>,      "csvserver_domain_binding":<csvserver_domain_binding[]_value>}]}```



###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/csvserver_binding
Query-parameters:
bulkbindings
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/csvserver_binding?bulkbindings=yes
NITRO allows you to fetch bindings in bulk.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "csvserver_binding": [ {      "name":<String_value>,      "csvserver_auditnslogpolicy_binding":<csvserver_auditnslogpolicy_binding[]_value>,      "csvserver_tmtrafficpolicy_binding":<csvserver_tmtrafficpolicy_binding[]_value>,      "csvserver_lbvserver_binding":<csvserver_lbvserver_binding[]_value>,      "csvserver_responderpolicy_binding":<csvserver_responderpolicy_binding[]_value>,      "csvserver_gslbvserver_binding":<csvserver_gslbvserver_binding[]_value>,      "csvserver_cachepolicy_binding":<csvserver_cachepolicy_binding[]_value>,      "csvserver_filterpolicy_binding":<csvserver_filterpolicy_binding[]_value>,      "csvserver_transformpolicy_binding":<csvserver_transformpolicy_binding[]_value>,      "csvserver_appflowpolicy_binding":<csvserver_appflowpolicy_binding[]_value>,      "csvserver_appfwpolicy_binding":<csvserver_appfwpolicy_binding[]_value>,      "csvserver_authorizationpolicy_binding":<csvserver_authorizationpolicy_binding[]_value>,      "csvserver_auditsyslogpolicy_binding":<csvserver_auditsyslogpolicy_binding[]_value>,      "csvserver_cmppolicy_binding":<csvserver_cmppolicy_binding[]_value>,      "csvserver_rewritepolicy_binding":<csvserver_rewritepolicy_binding[]_value>,      "csvserver_cspolicy_binding":<csvserver_cspolicy_binding[]_value>,      "csvserver_spilloverpolicy_binding":<csvserver_spilloverpolicy_binding[]_value>,      "csvserver_appqoepolicy_binding":<csvserver_appqoepolicy_binding[]_value>,      "csvserver_feopolicy_binding":<csvserver_feopolicy_binding[]_value>,      "csvserver_vpnvserver_binding":<csvserver_vpnvserver_binding[]_value>,      "csvserver_domain_binding":<csvserver_domain_binding[]_value>}]}```



