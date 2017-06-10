#sslvserver_sslpolicy_binding

Binding object showing the sslpolicy that can be bound to sslvserver.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>priority</td><td>&lt;Double></td><td>Read-write</td><td>The priority of the policies bound to this SSL service.&lt;br>Minimum value = 0&lt;br>Maximum value = 65534</td><tr><tr><td>policyname</td><td>&lt;String></td><td>Read-write</td><td>The name of the SSL policy binding.</td><tr><tr><td>labelname</td><td>&lt;String></td><td>Read-write</td><td>Name of the label to invoke if the current policy rule evaluates to TRUE.</td><tr><tr><td>vservername</td><td>&lt;String></td><td>Read-write</td><td>Name of the SSL virtual server.&lt;br>Minimum length = 1</td><tr><tr><td>gotopriorityexpression</td><td>&lt;String></td><td>Read-write</td><td>Expression specifying the priority of the next policy which will get evaluated if the current policy rule evaluates to TRUE.</td><tr><tr><td>invoke</td><td>&lt;Boolean></td><td>Read-write</td><td>Invoke flag. This attribute is relevant only for ADVANCED policies.</td><tr><tr><td>type</td><td>&lt;String></td><td>Read-write</td><td>Bind point to which to bind the policy. Possible Values: HANDSHAKE_REQ, HANDSHAKE_RES, CLIENTHELLO_REQ, CLIENTCERT_REQ, SERVERHELLO_RES, SERVERCERT_RES, SERVERHELLO_DONE_RES and REQUEST. These bindpoints mean: 1. HANDSHAKE_REQ: Policy evaluation will be done at the end of handshake on request side (request side means between client and NetScaler) 2. HANDSHAKE_RES: Policy evaluation will be done at the end of hadnshake on response side (response side means between Netscaler and server) 3. INTERCEPT_REQ: Policy evaluation will be done after receiving Client Hello on request side. 4. CLIENTCERT_REQ: Policy evaluation will be done after receiving Client Certificate on request side. 5. SERVERHELLO_RES: Policy evaluation will be done after receiving Server Hello on response side. 6. SERVERCERT_RES: Policy evaluation will be done after receiving Server Certificate on response side. 7. SERVERHELLO_DONE_RES: Policy evaluation will be done after receiving Server Hello Done on response side. 8. REQUEST: Policy evaluation will be done at appplication above SSL. This bindpoint is default and is used for actions based on clientauth and client cert.&lt;br>Default value: REQUEST&lt;br>Possible values = HANDSHAKE_REQ, HANDSHAKE_RES, INTERCEPT_REQ, CLIENTCERT_REQ, SERVERHELLO_RES, SERVERCERT_RES, SERVERHELLO_DONE_RES, REQUEST</td><tr><tr><td>labeltype</td><td>&lt;String></td><td>Read-write</td><td>Type of policy label invocation.&lt;br>Possible values = vserver, service, policylabel</td><tr><tr><td>polinherit</td><td>&lt;Double></td><td>Read-only</td><td>Whether the bound policy is a inherited policy or not.&lt;br>Minimum value = 0&lt;br>Maximum value = 254</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD:](#add:) | [DELETE:](#delete:) | [GET](#get) | [GET (ALL)](#get-(all)) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add:



URL: http://&lt;netscaler-ip-address/nitro/v1/config/sslvserver_sslpolicy_binding
HTTP Method: PUT
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"sslvserver_sslpolicy_binding":{      "vservername":<String_value>,      "policyname":<String_value>,      "priority":<Double_value>,      "gotopriorityexpression":<String_value>,      "invoke":<Boolean_value>,      "labeltype":<String_value>,      "labelname":<String_value>}}```
Response:
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete:



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslvserver_sslpolicy_binding/vservername_value&lt;String&gt;
HTTP Method: DELETE
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslvserver_sslpolicy_binding/vservername_value&lt;String&gt;
Query-parameters:
filter
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslvserver_sslpolicy_binding/vservername_value&lt;String&gt;?filter=property-name1:property-value1,property-name2:property-value2
Use this query-parameter to get the filtered set of sslvserver_sslpolicy_binding resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


pagination
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslvserver_sslpolicy_binding/vservername_value&lt;String&gt;?pagesize=#no;pageno=#no
Use this query-parameter to get the sslvserver_sslpolicy_binding resources in chunks.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "sslvserver_sslpolicy_binding": [ {      "priority":<Double_value>,      "policyname":<String_value>,      "labelname":<String_value>,      "vservername":<String_value>,      "gotopriorityexpression":<String_value>,      "invoke":<Boolean_value>,      "type":<String_value>,      "labeltype":<String_value>,      "polinherit":<Double_value>}]}```



###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslvserver_sslpolicy_binding
Query-parameters:
bulkbindings
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslvserver_sslpolicy_binding?bulkbindings=yes
NITRO allows you to fetch bindings in bulk.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "sslvserver_sslpolicy_binding": [ {      "priority":<Double_value>,      "policyname":<String_value>,      "labelname":<String_value>,      "vservername":<String_value>,      "gotopriorityexpression":<String_value>,      "invoke":<Boolean_value>,      "type":<String_value>,      "labeltype":<String_value>,      "polinherit":<Double_value>}]}```



###count



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslvserver_sslpolicy_binding/vservername_value&lt;String&gt;?count=yes
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: 
{"sslvserver_sslpolicy_binding": [ { "__count": "#no"} ] }


