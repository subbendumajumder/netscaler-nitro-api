#transformprofile_transformaction_binding

Binding object showing the transformaction that can be bound to transformprofile.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name of the profile.&lt;br>Minimum length = 1</td><tr><tr><td>actionname</td><td>&lt;String></td><td>Read-write</td><td>URL Transformation action name.</td><tr><tr><td>priority</td><td>&lt;Double></td><td>Read-only</td><td>Priority of the Action within the Profile.</td><tr><tr><td>resurlfrom</td><td>&lt;String></td><td>Read-only</td><td>Pattern of original response URLs. It corresponds to the way external users view the server, and acts as a source for response transformations.</td><tr><tr><td>cookiedomainfrom</td><td>&lt;String></td><td>Read-only</td><td>Pattern of the original domain in Set-Cookie headers.</td><tr><tr><td>profilename</td><td>&lt;String></td><td>Read-only</td><td>URL Transformation profile name.</td><tr><tr><td>state</td><td>&lt;String></td><td>Read-only</td><td>Enabled flag.&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>cookiedomaininto</td><td>&lt;String></td><td>Read-only</td><td>Pattern of the transformed domain in Set-Cookie headers.</td><tr><tr><td>actioncomment</td><td>&lt;String></td><td>Read-only</td><td>Comments.</td><tr><tr><td>resurlinto</td><td>&lt;String></td><td>Read-only</td><td>Pattern of transformed response URLs. It corresponds to internal addresses and indicates how they are created.</td><tr><tr><td>requrlinto</td><td>&lt;String></td><td>Read-only</td><td>Pattern of transformed request URLs. It corresponds to internal addresses and indicates how they are created.</td><tr><tr><td>requrlfrom</td><td>&lt;String></td><td>Read-only</td><td>Pattern of original request URLs. It corresponds to the way external users view the server, and acts as a source for request transformations.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[GET](#get) | [GET (ALL)](#get-(all)) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/transformprofile_transformaction_binding/name_value&lt;String&gt;
Query-parameters:
filter
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/transformprofile_transformaction_binding/name_value&lt;String&gt;?filter=property-name1:property-value1,property-name2:property-value2
Use this query-parameter to get the filtered set of transformprofile_transformaction_binding resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


pagination
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/transformprofile_transformaction_binding/name_value&lt;String&gt;?pagesize=#no;pageno=#no
Use this query-parameter to get the transformprofile_transformaction_binding resources in chunks.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "transformprofile_transformaction_binding": [ {      "name":<String_value>,      "actionname":<String_value>,      "priority":<Double_value>,      "resurlfrom":<String_value>,      "cookiedomainfrom":<String_value>,      "profilename":<String_value>,      "state":<String_value>,      "cookiedomaininto":<String_value>,      "actioncomment":<String_value>,      "resurlinto":<String_value>,      "requrlinto":<String_value>,      "requrlfrom":<String_value>}]}```



###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/transformprofile_transformaction_binding
Query-parameters:
bulkbindings
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/transformprofile_transformaction_binding?bulkbindings=yes
NITRO allows you to fetch bindings in bulk.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "transformprofile_transformaction_binding": [ {      "name":<String_value>,      "actionname":<String_value>,      "priority":<Double_value>,      "resurlfrom":<String_value>,      "cookiedomainfrom":<String_value>,      "profilename":<String_value>,      "state":<String_value>,      "cookiedomaininto":<String_value>,      "actioncomment":<String_value>,      "resurlinto":<String_value>,      "requrlinto":<String_value>,      "requrlfrom":<String_value>}]}```



###count



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/transformprofile_transformaction_binding/name_value&lt;String&gt;?count=yes
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: 
{"transformprofile_transformaction_binding": [ { "__count": "#no"} ] }


