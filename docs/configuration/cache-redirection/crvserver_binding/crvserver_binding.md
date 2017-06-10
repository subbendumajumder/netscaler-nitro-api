#crvserver_binding

Binding object which returns the resources bound to crvserver.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name of a cache redirection virtual server about which to display detailed information.&lt;br>Minimum length = 1</td><tr><tr><td>crvserver_spilloverpolicy_binding</td><td>&lt;crvserver_spilloverpolicy_binding[]></td><td>Read-only</td><td>spilloverpolicy that can be bound to crvserver.</td><tr><tr><td>crvserver_filterpolicy_binding</td><td>&lt;crvserver_filterpolicy_binding[]></td><td>Read-only</td><td>filterpolicy that can be bound to crvserver.</td><tr><tr><td>crvserver_icapolicy_binding</td><td>&lt;crvserver_icapolicy_binding[]></td><td>Read-only</td><td>icapolicy that can be bound to crvserver.</td><tr><tr><td>crvserver_cmppolicy_binding</td><td>&lt;crvserver_cmppolicy_binding[]></td><td>Read-only</td><td>cmppolicy that can be bound to crvserver.</td><tr><tr><td>crvserver_lbvserver_binding</td><td>&lt;crvserver_lbvserver_binding[]></td><td>Read-only</td><td>lbvserver that can be bound to crvserver.</td><tr><tr><td>crvserver_appflowpolicy_binding</td><td>&lt;crvserver_appflowpolicy_binding[]></td><td>Read-only</td><td>appflowpolicy that can be bound to crvserver.</td><tr><tr><td>crvserver_responderpolicy_binding</td><td>&lt;crvserver_responderpolicy_binding[]></td><td>Read-only</td><td>responderpolicy that can be bound to crvserver.</td><tr><tr><td>crvserver_policymap_binding</td><td>&lt;crvserver_policymap_binding[]></td><td>Read-only</td><td>policymap that can be bound to crvserver.</td><tr><tr><td>crvserver_feopolicy_binding</td><td>&lt;crvserver_feopolicy_binding[]></td><td>Read-only</td><td>feopolicy that can be bound to crvserver.</td><tr><tr><td>crvserver_cachepolicy_binding</td><td>&lt;crvserver_cachepolicy_binding[]></td><td>Read-only</td><td>cachepolicy that can be bound to crvserver.</td><tr><tr><td>crvserver_rewritepolicy_binding</td><td>&lt;crvserver_rewritepolicy_binding[]></td><td>Read-only</td><td>rewritepolicy that can be bound to crvserver.</td><tr><tr><td>crvserver_cspolicy_binding</td><td>&lt;crvserver_cspolicy_binding[]></td><td>Read-only</td><td>cspolicy that can be bound to crvserver.</td><tr><tr><td>crvserver_appqoepolicy_binding</td><td>&lt;crvserver_appqoepolicy_binding[]></td><td>Read-only</td><td>appqoepolicy that can be bound to crvserver.</td><tr><tr><td>crvserver_appfwpolicy_binding</td><td>&lt;crvserver_appfwpolicy_binding[]></td><td>Read-only</td><td>appfwpolicy that can be bound to crvserver.</td><tr><tr><td>crvserver_crpolicy_binding</td><td>&lt;crvserver_crpolicy_binding[]></td><td>Read-only</td><td>crpolicy that can be bound to crvserver.</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[GET](#get) | [GET (ALL)](#get-(all))


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/crvserver_binding/name_value&lt;String&gt;
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "crvserver_binding": [ {      "name":<String_value>,      "crvserver_spilloverpolicy_binding":<crvserver_spilloverpolicy_binding[]_value>,      "crvserver_policymap_binding":<crvserver_policymap_binding[]_value>,      "crvserver_icapolicy_binding":<crvserver_icapolicy_binding[]_value>,      "crvserver_cachepolicy_binding":<crvserver_cachepolicy_binding[]_value>,      "crvserver_lbvserver_binding":<crvserver_lbvserver_binding[]_value>,      "crvserver_appfwpolicy_binding":<crvserver_appfwpolicy_binding[]_value>,      "crvserver_responderpolicy_binding":<crvserver_responderpolicy_binding[]_value>,      "crvserver_filterpolicy_binding":<crvserver_filterpolicy_binding[]_value>,      "crvserver_cmppolicy_binding":<crvserver_cmppolicy_binding[]_value>,      "crvserver_appqoepolicy_binding":<crvserver_appqoepolicy_binding[]_value>,      "crvserver_feopolicy_binding":<crvserver_feopolicy_binding[]_value>,      "crvserver_cspolicy_binding":<crvserver_cspolicy_binding[]_value>,      "crvserver_crpolicy_binding":<crvserver_crpolicy_binding[]_value>,      "crvserver_rewritepolicy_binding":<crvserver_rewritepolicy_binding[]_value>,      "crvserver_appflowpolicy_binding":<crvserver_appflowpolicy_binding[]_value>}]}```



###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/crvserver_binding
Query-parameters:
bulkbindings
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/crvserver_binding?bulkbindings=yes
NITRO allows you to fetch bindings in bulk.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "crvserver_binding": [ {      "name":<String_value>,      "crvserver_spilloverpolicy_binding":<crvserver_spilloverpolicy_binding[]_value>,      "crvserver_policymap_binding":<crvserver_policymap_binding[]_value>,      "crvserver_icapolicy_binding":<crvserver_icapolicy_binding[]_value>,      "crvserver_cachepolicy_binding":<crvserver_cachepolicy_binding[]_value>,      "crvserver_lbvserver_binding":<crvserver_lbvserver_binding[]_value>,      "crvserver_appfwpolicy_binding":<crvserver_appfwpolicy_binding[]_value>,      "crvserver_responderpolicy_binding":<crvserver_responderpolicy_binding[]_value>,      "crvserver_filterpolicy_binding":<crvserver_filterpolicy_binding[]_value>,      "crvserver_cmppolicy_binding":<crvserver_cmppolicy_binding[]_value>,      "crvserver_appqoepolicy_binding":<crvserver_appqoepolicy_binding[]_value>,      "crvserver_feopolicy_binding":<crvserver_feopolicy_binding[]_value>,      "crvserver_cspolicy_binding":<crvserver_cspolicy_binding[]_value>,      "crvserver_crpolicy_binding":<crvserver_crpolicy_binding[]_value>,      "crvserver_rewritepolicy_binding":<crvserver_rewritepolicy_binding[]_value>,      "crvserver_appflowpolicy_binding":<crvserver_appflowpolicy_binding[]_value>}]}```



