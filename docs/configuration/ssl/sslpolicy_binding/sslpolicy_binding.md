#sslpolicy_binding

Binding object which returns the resources bound to sslpolicy.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name of the SSL policy for which to display detailed information.&lt;br>Minimum length = 1</td><tr><tr><td>sslpolicy_csvserver_binding</td><td>&lt;sslpolicy_csvserver_binding[]></td><td>Read-only</td><td>csvserver that can be bound to sslpolicy.</td><tr><tr><td>sslpolicy_sslvserver_binding</td><td>&lt;sslpolicy_sslvserver_binding[]></td><td>Read-only</td><td>sslvserver that can be bound to sslpolicy.</td><tr><tr><td>sslpolicy_sslpolicylabel_binding</td><td>&lt;sslpolicy_sslpolicylabel_binding[]></td><td>Read-only</td><td>sslpolicylabel that can be bound to sslpolicy.</td><tr><tr><td>sslpolicy_sslservice_binding</td><td>&lt;sslpolicy_sslservice_binding[]></td><td>Read-only</td><td>sslservice that can be bound to sslpolicy.</td><tr><tr><td>sslpolicy_lbvserver_binding</td><td>&lt;sslpolicy_lbvserver_binding[]></td><td>Read-only</td><td>lbvserver that can be bound to sslpolicy.</td><tr><tr><td>sslpolicy_sslglobal_binding</td><td>&lt;sslpolicy_sslglobal_binding[]></td><td>Read-only</td><td>sslglobal that can be bound to sslpolicy.</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[GET](#get) | [GET (ALL)](#get-(all))


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslpolicy_binding/name_value&lt;String&gt;
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "sslpolicy_binding": [ {      "name":<String_value>,      "sslpolicy_csvserver_binding":<sslpolicy_csvserver_binding[]_value>,      "sslpolicy_sslvserver_binding":<sslpolicy_sslvserver_binding[]_value>,      "sslpolicy_lbvserver_binding":<sslpolicy_lbvserver_binding[]_value>,      "sslpolicy_sslservice_binding":<sslpolicy_sslservice_binding[]_value>,      "sslpolicy_sslpolicylabel_binding":<sslpolicy_sslpolicylabel_binding[]_value>,      "sslpolicy_sslglobal_binding":<sslpolicy_sslglobal_binding[]_value>}]}```



###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslpolicy_binding
Query-parameters:
bulkbindings
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslpolicy_binding?bulkbindings=yes
NITRO allows you to fetch bindings in bulk.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "sslpolicy_binding": [ {      "name":<String_value>,      "sslpolicy_csvserver_binding":<sslpolicy_csvserver_binding[]_value>,      "sslpolicy_sslvserver_binding":<sslpolicy_sslvserver_binding[]_value>,      "sslpolicy_lbvserver_binding":<sslpolicy_lbvserver_binding[]_value>,      "sslpolicy_sslservice_binding":<sslpolicy_sslservice_binding[]_value>,      "sslpolicy_sslpolicylabel_binding":<sslpolicy_sslpolicylabel_binding[]_value>,      "sslpolicy_sslglobal_binding":<sslpolicy_sslglobal_binding[]_value>}]}```



