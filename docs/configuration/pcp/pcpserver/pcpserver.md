#pcpserver

Configuration for server resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the PCP server. Must begin with an ASCII alphanumeric or underscore (_) character, and must contain only ASCII alphanumeric, underscore CLI Users: If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my pcpServer" or my pcpServer).</td><tr><tr><td>ipaddress</td><td>&lt;String></td><td>Read-write</td><td>The IP address of the PCP server.</td><tr><tr><td>port</td><td>&lt;Integer></td><td>Read-write</td><td>Port number for the PCP server.&lt;br>Default value: 5351&lt;br>Range 1 - 65535</td><tr><tr><td>pcpprofile</td><td>&lt;String></td><td>Read-write</td><td>pcp profile name.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [DELETE](#delete) | [UPDATE](#update) | [UNSET](#unset) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/pcpserver
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"pcpserver":{      "name":<String_value>,      "ipaddress":<String_value>,      "port":<Integer_value>,      "pcpprofile":<String_value>}}```
Response:
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx   (for general HTTP errors) or 5xx     (for NetScaler-specific errors). The response payload provides details of the error 


###delete



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/pcpserver/name_value&lt;String&gt;
HTTP Method: DELETE
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx   (for general HTTP errors) or 5xx     (for NetScaler-specific errors). The response payload provides details of the error 


###update



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/pcpserver
HTTP Method: PUT
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"pcpserver":{      "name":<String_value>,      "port":<Integer_value>,      "pcpprofile":<String_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx   (for general HTTP errors) or 5xx     (for NetScaler-specific errors). The response payload provides details of the error 


###unset



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/pcpserver?action=unset
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"pcpserver":{      "name":<String_value>,      "port":true,      "pcpprofile":true}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx   (for general HTTP errors) or 5xx     (for NetScaler-specific errors). The response payload provides details of the error 


###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/pcpserver
Query-parameters:
args
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/pcpserver?args=      "name":&lt;String_value&gt;
Use this query-parameter to get pcpserver resources based on additional properties.


attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/pcpserver?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


filter
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/pcpserver?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of pcpserver resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/pcpserver?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).


pagesize=#no;pageno=#no
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/pcpserver?pagesize=#no;pageno=#no
Use this query-parameter to get the pcpserver resources in chunks.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx   (for general HTTP errors) or 5xx     (for NetScaler-specific errors). The response payload provides details of the error Response Headers:

Content-Type:application/json

Response Payload: ```{ "pcpserver": [ {      "name":<String_value>,      "ipaddress":<String_value>,      "port":<Integer_value>,      "pcpprofile":<String_value>}]}```



###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/pcpserver/name_value&lt;String&gt;
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/pcpserver/name_value&lt;String&gt;?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/pcpserver/name_value&lt;String&gt;?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx   (for general HTTP errors) or 5xx     (for NetScaler-specific errors). The response payload provides details of the error Response Headers:

Content-Type:application/json

Response Payload: ```{ "pcpserver": [ {      "name":<String_value>,      "ipaddress":<String_value>,      "port":<Integer_value>,      "pcpprofile":<String_value>}]}```



###count



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/pcpserver?count=yes
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx   (for general HTTP errors) or 5xx     (for NetScaler-specific errors). The response payload provides details of the error Response Headers:

Content-Type:application/json

Response Payload: 
{ "pcpserver": [ { "__count": "#no"} ] }


