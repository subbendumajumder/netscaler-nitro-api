#hanode_binding

Binding object which returns the resources bound to hanode.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>&lt;Double></td><td>Read-write</td><td>ID of the node whose HA settings you want to display. (The ID of the local node is always 0.).&lt;br>Minimum value = 0&lt;br>Maximum value = 64</td><tr><tr><td>hanode_partialfailureinterfaces_binding</td><td>&lt;hanode_partialfailureinterfaces_binding[]></td><td>Read-only</td><td>partialfailureinterfaces that can be bound to hanode.</td><tr><tr><td>hanode_routemonitor6_binding</td><td>&lt;hanode_routemonitor6_binding[]></td><td>Read-only</td><td>routemonitor6 that can be bound to hanode.</td><tr><tr><td>hanode_ci_binding</td><td>&lt;hanode_ci_binding[]></td><td>Read-only</td><td>ci that can be bound to hanode.</td><tr><tr><td>hanode_routemonitor_binding</td><td>&lt;hanode_routemonitor_binding[]></td><td>Read-only</td><td>routemonitor that can be bound to hanode.</td><tr><tr><td>hanode_fis_binding</td><td>&lt;hanode_fis_binding[]></td><td>Read-only</td><td>fis that can be bound to hanode.</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[GET](#get) | [GET (ALL)](#get-(all))


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/hanode_binding/id_value&lt;Double&gt;
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "hanode_binding": [ {      "id":<Double_value>,      "hanode_routemonitor_binding":<hanode_routemonitor_binding[]_value>,      "hanode_partialfailureinterfaces_binding":<hanode_partialfailureinterfaces_binding[]_value>,      "hanode_fis_binding":<hanode_fis_binding[]_value>,      "hanode_routemonitor6_binding":<hanode_routemonitor6_binding[]_value>,      "hanode_ci_binding":<hanode_ci_binding[]_value>}]}```



###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/hanode_binding
Query-parameters:
bulkbindings
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/hanode_binding?bulkbindings=yes
NITRO allows you to fetch bindings in bulk.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "hanode_binding": [ {      "id":<Double_value>,      "hanode_routemonitor_binding":<hanode_routemonitor_binding[]_value>,      "hanode_partialfailureinterfaces_binding":<hanode_partialfailureinterfaces_binding[]_value>,      "hanode_fis_binding":<hanode_fis_binding[]_value>,      "hanode_routemonitor6_binding":<hanode_routemonitor6_binding[]_value>,      "hanode_ci_binding":<hanode_ci_binding[]_value>}]}```



