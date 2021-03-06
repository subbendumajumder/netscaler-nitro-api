#videooptimizationglobal_videooptimizationpolicy_binding

Binding object showing the videooptimizationpolicy that can be bound to videooptimizationglobal.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>priority</td><td>&lt;Double></td><td>Read-write</td><td>Specifies the priority of the policy.</td><tr><tr><td>globalbindtype</td><td>&lt;String></td><td>Read-write</td><td>.&lt;br>Default value: SYSTEM_GLOBAL&lt;br>Possible values = SYSTEM_GLOBAL, VPN_GLOBAL, RNAT_GLOBAL</td><tr><tr><td>policyname</td><td>&lt;String></td><td>Read-write</td><td>Name of the video optimization policy.</td><tr><tr><td>labelname</td><td>&lt;String></td><td>Read-write</td><td>Name of the policy label to invoke. If the current policy evaluates to TRUE, the invoke parameter is set, and Label Type is policylabel.</td><tr><tr><td>gotopriorityexpression</td><td>&lt;String></td><td>Read-write</td><td>Expression specifying the priority of the next policy which will get evaluated if the current policy rule evaluates to TRUE.</td><tr><tr><td>type</td><td>&lt;String></td><td>Read-write</td><td>Specifies the bind point whose policies you want to display.&lt;br>Possible values = REQ_OVERRIDE, REQ_DEFAULT, RES_OVERRIDE, RES_DEFAULT</td><tr><tr><td>invoke</td><td>&lt;Boolean></td><td>Read-write</td><td>If the current policy evaluates to TRUE, terminate evaluation of policies bound to the current policy label, and then forward the request to the specified virtual server or evaluate the specified policy label.</td><tr><tr><td>labeltype</td><td>&lt;String></td><td>Read-write</td><td>Type of invocation, Available settings function as follows: * vserver - Forward the request to the specified virtual server. * policylabel - Invoke the specified policy label.&lt;br>Possible values = vserver, policylabel</td><tr><tr><td>numpol</td><td>&lt;Double></td><td>Read-only</td><td>number of polices bound.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD:](#add:) | [DELETE:](#delete:) | [GET](#get) | [GET (ALL)](#get-(all)) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add:



URL: http://&lt;netscaler-ip-address/nitro/v1/config/videooptimizationglobal_videooptimizationpolicy_binding
HTTP Method: PUT
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"videooptimizationglobal_videooptimizationpolicy_binding":{      "policyname":<String_value>,      "priority":<Double_value>,      "gotopriorityexpression":<String_value>,      "type":<String_value>,      "invoke":<Boolean_value>,      "labeltype":<String_value>,      "labelname":<String_value>}}```
Response:
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete:



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/videooptimizationglobal_videooptimizationpolicy_binding
HTTP Method: DELETE
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/videooptimizationglobal_videooptimizationpolicy_binding
Query-parameters:
filter
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/videooptimizationglobal_videooptimizationpolicy_binding?filter=property-name1:property-value1,property-name2:property-value2
Use this query-parameter to get the filtered set of videooptimizationglobal_videooptimizationpolicy_binding resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


pagination
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/videooptimizationglobal_videooptimizationpolicy_binding?pagesize=#no;pageno=#no
Use this query-parameter to get the videooptimizationglobal_videooptimizationpolicy_binding resources in chunks.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "videooptimizationglobal_videooptimizationpolicy_binding": [ {      "priority":<Double_value>,      "globalbindtype":<String_value>,      "policyname":<String_value>,      "labelname":<String_value>,      "gotopriorityexpression":<String_value>,      "type":<String_value>,      "invoke":<Boolean_value>,      "labeltype":<String_value>,      "numpol":<Double_value>}]}```



###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/videooptimizationglobal_videooptimizationpolicy_binding
Query-parameters:
bulkbindings
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/videooptimizationglobal_videooptimizationpolicy_binding?bulkbindings=yes
NITRO allows you to fetch bindings in bulk.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "videooptimizationglobal_videooptimizationpolicy_binding": [ {      "priority":<Double_value>,      "globalbindtype":<String_value>,      "policyname":<String_value>,      "labelname":<String_value>,      "gotopriorityexpression":<String_value>,      "type":<String_value>,      "invoke":<Boolean_value>,      "labeltype":<String_value>,      "numpol":<Double_value>}]}```



###count



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/videooptimizationglobal_videooptimizationpolicy_binding?count=yes
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: 
{ "videooptimizationglobal_videooptimizationpolicy_binding": [ { "__count": "#no"} ] }


