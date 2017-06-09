#lbvserver_binding

Binding object which returns the resources bound to lbvserver.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name of the virtual server. If no name is provided, statistical data of all configured virtual servers is displayed.&lt;br>Minimum length = 1</td><tr><tr><td>lbvserver_cmppolicy_binding</td><td>&lt;lbvserver_cmppolicy_binding[]></td><td>Read-only</td><td>cmppolicy that can be bound to lbvserver.</td><tr><tr><td>lbvserver_authorizationpolicy_binding</td><td>&lt;lbvserver_authorizationpolicy_binding[]></td><td>Read-only</td><td>authorizationpolicy that can be bound to lbvserver.</td><tr><tr><td>lbvserver_rewritepolicy_binding</td><td>&lt;lbvserver_rewritepolicy_binding[]></td><td>Read-only</td><td>rewritepolicy that can be bound to lbvserver.</td><tr><tr><td>lbvserver_pqpolicy_binding</td><td>&lt;lbvserver_pqpolicy_binding[]></td><td>Read-only</td><td>pqpolicy that can be bound to lbvserver.</td><tr><tr><td>lbvserver_service_binding</td><td>&lt;lbvserver_service_binding[]></td><td>Read-only</td><td>service that can be bound to lbvserver.</td><tr><tr><td>lbvserver_tmtrafficpolicy_binding</td><td>&lt;lbvserver_tmtrafficpolicy_binding[]></td><td>Read-only</td><td>tmtrafficpolicy that can be bound to lbvserver.</td><tr><tr><td>lbvserver_auditsyslogpolicy_binding</td><td>&lt;lbvserver_auditsyslogpolicy_binding[]></td><td>Read-only</td><td>auditsyslogpolicy that can be bound to lbvserver.</td><tr><tr><td>lbvserver_appfwpolicy_binding</td><td>&lt;lbvserver_appfwpolicy_binding[]></td><td>Read-only</td><td>appfwpolicy that can be bound to lbvserver.</td><tr><tr><td>lbvserver_spilloverpolicy_binding</td><td>&lt;lbvserver_spilloverpolicy_binding[]></td><td>Read-only</td><td>spilloverpolicy that can be bound to lbvserver.</td><tr><tr><td>lbvserver_csvserver_binding</td><td>&lt;lbvserver_csvserver_binding[]></td><td>Read-only</td><td>csvserver that can be bound to lbvserver.</td><tr><tr><td>lbvserver_capolicy_binding</td><td>&lt;lbvserver_capolicy_binding[]></td><td>Read-only</td><td>capolicy that can be bound to lbvserver.</td><tr><tr><td>lbvserver_auditnslogpolicy_binding</td><td>&lt;lbvserver_auditnslogpolicy_binding[]></td><td>Read-only</td><td>auditnslogpolicy that can be bound to lbvserver.</td><tr><tr><td>lbvserver_filterpolicy_binding</td><td>&lt;lbvserver_filterpolicy_binding[]></td><td>Read-only</td><td>filterpolicy that can be bound to lbvserver.</td><tr><tr><td>lbvserver_appflowpolicy_binding</td><td>&lt;lbvserver_appflowpolicy_binding[]></td><td>Read-only</td><td>appflowpolicy that can be bound to lbvserver.</td><tr><tr><td>lbvserver_responderpolicy_binding</td><td>&lt;lbvserver_responderpolicy_binding[]></td><td>Read-only</td><td>responderpolicy that can be bound to lbvserver.</td><tr><tr><td>lbvserver_transformpolicy_binding</td><td>&lt;lbvserver_transformpolicy_binding[]></td><td>Read-only</td><td>transformpolicy that can be bound to lbvserver.</td><tr><tr><td>lbvserver_dospolicy_binding</td><td>&lt;lbvserver_dospolicy_binding[]></td><td>Read-only</td><td>dospolicy that can be bound to lbvserver.</td><tr><tr><td>lbvserver_feopolicy_binding</td><td>&lt;lbvserver_feopolicy_binding[]></td><td>Read-only</td><td>feopolicy that can be bound to lbvserver.</td><tr><tr><td>lbvserver_servicegroupmember_binding</td><td>&lt;lbvserver_servicegroupmember_binding[]></td><td>Read-only</td><td>servicegroupmember that can be bound to lbvserver.</td><tr><tr><td>lbvserver_dnspolicy64_binding</td><td>&lt;lbvserver_dnspolicy64_binding[]></td><td>Read-only</td><td>dnspolicy64 that can be bound to lbvserver.</td><tr><tr><td>lbvserver_cachepolicy_binding</td><td>&lt;lbvserver_cachepolicy_binding[]></td><td>Read-only</td><td>cachepolicy that can be bound to lbvserver.</td><tr><tr><td>lbvserver_scpolicy_binding</td><td>&lt;lbvserver_scpolicy_binding[]></td><td>Read-only</td><td>scpolicy that can be bound to lbvserver.</td><tr><tr><td>lbvserver_servicegroup_binding</td><td>&lt;lbvserver_servicegroup_binding[]></td><td>Read-only</td><td>servicegroup that can be bound to lbvserver.</td><tr><tr><td>lbvserver_appqoepolicy_binding</td><td>&lt;lbvserver_appqoepolicy_binding[]></td><td>Read-only</td><td>appqoepolicy that can be bound to lbvserver.</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[GET](#get) | [GET (ALL)](#get-(all))


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lbvserver_binding/name_value&lt;String&gt;
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "lbvserver_binding": [ {      "name":<String_value>,      "lbvserver_appfwpolicy_binding":<lbvserver_appfwpolicy_binding[]_value>,      "lbvserver_spilloverpolicy_binding":<lbvserver_spilloverpolicy_binding[]_value>,      "lbvserver_appqoepolicy_binding":<lbvserver_appqoepolicy_binding[]_value>,      "lbvserver_feopolicy_binding":<lbvserver_feopolicy_binding[]_value>,      "lbvserver_csvserver_binding":<lbvserver_csvserver_binding[]_value>,      "lbvserver_capolicy_binding":<lbvserver_capolicy_binding[]_value>,      "lbvserver_authorizationpolicy_binding":<lbvserver_authorizationpolicy_binding[]_value>,      "lbvserver_servicegroupmember_binding":<lbvserver_servicegroupmember_binding[]_value>,      "lbvserver_dospolicy_binding":<lbvserver_dospolicy_binding[]_value>,      "lbvserver_tmtrafficpolicy_binding":<lbvserver_tmtrafficpolicy_binding[]_value>,      "lbvserver_cmppolicy_binding":<lbvserver_cmppolicy_binding[]_value>,      "lbvserver_auditsyslogpolicy_binding":<lbvserver_auditsyslogpolicy_binding[]_value>,      "lbvserver_pqpolicy_binding":<lbvserver_pqpolicy_binding[]_value>,      "lbvserver_dnspolicy64_binding":<lbvserver_dnspolicy64_binding[]_value>,      "lbvserver_rewritepolicy_binding":<lbvserver_rewritepolicy_binding[]_value>,      "lbvserver_auditnslogpolicy_binding":<lbvserver_auditnslogpolicy_binding[]_value>,      "lbvserver_transformpolicy_binding":<lbvserver_transformpolicy_binding[]_value>,      "lbvserver_filterpolicy_binding":<lbvserver_filterpolicy_binding[]_value>,      "lbvserver_scpolicy_binding":<lbvserver_scpolicy_binding[]_value>,      "lbvserver_appflowpolicy_binding":<lbvserver_appflowpolicy_binding[]_value>,      "lbvserver_servicegroup_binding":<lbvserver_servicegroup_binding[]_value>,      "lbvserver_cachepolicy_binding":<lbvserver_cachepolicy_binding[]_value>,      "lbvserver_service_binding":<lbvserver_service_binding[]_value>,      "lbvserver_responderpolicy_binding":<lbvserver_responderpolicy_binding[]_value>}]}```



###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lbvserver_binding
Query-parameters:
bulkbindings
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lbvserver_binding?bulkbindings=yes
NITRO allows you to fetch bindings in bulk.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "lbvserver_binding": [ {      "name":<String_value>,      "lbvserver_appfwpolicy_binding":<lbvserver_appfwpolicy_binding[]_value>,      "lbvserver_spilloverpolicy_binding":<lbvserver_spilloverpolicy_binding[]_value>,      "lbvserver_appqoepolicy_binding":<lbvserver_appqoepolicy_binding[]_value>,      "lbvserver_feopolicy_binding":<lbvserver_feopolicy_binding[]_value>,      "lbvserver_csvserver_binding":<lbvserver_csvserver_binding[]_value>,      "lbvserver_capolicy_binding":<lbvserver_capolicy_binding[]_value>,      "lbvserver_authorizationpolicy_binding":<lbvserver_authorizationpolicy_binding[]_value>,      "lbvserver_servicegroupmember_binding":<lbvserver_servicegroupmember_binding[]_value>,      "lbvserver_dospolicy_binding":<lbvserver_dospolicy_binding[]_value>,      "lbvserver_tmtrafficpolicy_binding":<lbvserver_tmtrafficpolicy_binding[]_value>,      "lbvserver_cmppolicy_binding":<lbvserver_cmppolicy_binding[]_value>,      "lbvserver_auditsyslogpolicy_binding":<lbvserver_auditsyslogpolicy_binding[]_value>,      "lbvserver_pqpolicy_binding":<lbvserver_pqpolicy_binding[]_value>,      "lbvserver_dnspolicy64_binding":<lbvserver_dnspolicy64_binding[]_value>,      "lbvserver_rewritepolicy_binding":<lbvserver_rewritepolicy_binding[]_value>,      "lbvserver_auditnslogpolicy_binding":<lbvserver_auditnslogpolicy_binding[]_value>,      "lbvserver_transformpolicy_binding":<lbvserver_transformpolicy_binding[]_value>,      "lbvserver_filterpolicy_binding":<lbvserver_filterpolicy_binding[]_value>,      "lbvserver_scpolicy_binding":<lbvserver_scpolicy_binding[]_value>,      "lbvserver_appflowpolicy_binding":<lbvserver_appflowpolicy_binding[]_value>,      "lbvserver_servicegroup_binding":<lbvserver_servicegroup_binding[]_value>,      "lbvserver_cachepolicy_binding":<lbvserver_cachepolicy_binding[]_value>,      "lbvserver_service_binding":<lbvserver_service_binding[]_value>,      "lbvserver_responderpolicy_binding":<lbvserver_responderpolicy_binding[]_value>}]}```



