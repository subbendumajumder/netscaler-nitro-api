#wisite_translationinternalip_binding

Binding object showing the translationinternalip that can be bound to wisite.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>sitepath</td><td>&lt;String></td><td>Read-write</td><td>Path to the Web Interface site.&lt;br>Minimum length = 1&lt;br>Maximum length = 250</td><tr><tr><td>accesstype</td><td>&lt;String></td><td>Read-write</td><td>Type of access to the XenApp or XenDesktop server. Available settings function as follows: * User Device - Clients can use the translated address of the mapping entry to connect to the XenApp or XenDesktop server. * Gateway - Access Gateway can use the translated address of the mapping entry to connect to the XenApp or XenDesktop server. * User Device and Gateway - Both clients and Access Gateway can use the translated address of the mapping entry to connect to the XenApp or XenDesktop server.&lt;br>Default value: UserDevice&lt;br>Possible values = UserDevice, Gateway, UserDeviceAndGateway</td><tr><tr><td>translationexternalport</td><td>&lt;Integer></td><td>Read-write</td><td>External port number associated with the servers port number.&lt;br>Range 1 - 65535&lt;br>* in CLI is represented as 65535 in NITRO API</td><tr><tr><td>translationinternalip</td><td>&lt;String></td><td>Read-write</td><td>IP address of the server for which you want to associate an external IP address. (Clients access the server through the associated external address and port.).&lt;br>Default value: 0</td><tr><tr><td>translationexternalip</td><td>&lt;String></td><td>Read-write</td><td>External IP address associated with servers IP address.</td><tr><tr><td>translationinternalport</td><td>&lt;Integer></td><td>Read-write</td><td>Port number of the server for which you want to associate an external port. (Clients access the server through the associated external address and port.).&lt;br>Range 1 - 65535&lt;br>* in CLI is represented as 65535 in NITRO API</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-write</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD:](#add:) | [DELETE:](#delete:) | [GET](#get) | [GET (ALL)](#get-(all)) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add:



URL: http://&lt;netscaler-ip-address/nitro/v1/config/wisite_translationinternalip_binding
HTTP Method: PUT
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"wisite_translationinternalip_binding":{      "sitepath":<String_value>,      "translationinternalip":<String_value>,      "translationinternalport":<Integer_value>,      "translationexternalip":<String_value>,      "translationexternalport":<Integer_value>,      "accesstype":<String_value>}}```
Response:
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete:



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/wisite_translationinternalip_binding/sitepath_value&lt;String&gt;
HTTP Method: DELETE
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/wisite_translationinternalip_binding/sitepath_value&lt;String&gt;
Query-parameters:
filter
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/wisite_translationinternalip_binding/sitepath_value&lt;String&gt;?filter=property-name1:property-value1,property-name2:property-value2
Use this query-parameter to get the filtered set of wisite_translationinternalip_binding resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


pagination
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/wisite_translationinternalip_binding/sitepath_value&lt;String&gt;?pagesize=#no;pageno=#no
Use this query-parameter to get the wisite_translationinternalip_binding resources in chunks.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "wisite_translationinternalip_binding": [ {      "sitepath":<String_value>,      "accesstype":<String_value>,      "translationexternalport":<Integer_value>,      "translationinternalip":<String_value>,      "translationexternalip":<String_value>,      "translationinternalport":<Integer_value>}]}```



###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/wisite_translationinternalip_binding
Query-parameters:
bulkbindings
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/wisite_translationinternalip_binding?bulkbindings=yes
NITRO allows you to fetch bindings in bulk.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "wisite_translationinternalip_binding": [ {      "sitepath":<String_value>,      "accesstype":<String_value>,      "translationexternalport":<Integer_value>,      "translationinternalip":<String_value>,      "translationexternalip":<String_value>,      "translationinternalport":<Integer_value>}]}```



###count



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/wisite_translationinternalip_binding/sitepath_value&lt;String&gt;?count=yes
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: 
{"wisite_translationinternalip_binding": [ { "__count": "#no"} ] }


