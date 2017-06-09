#vpnicadtlsconnection

Configuration for active ica connections resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>username</td><td>&lt;String></td><td>Read-write</td><td>User name for which to display connections.&lt;br>Minimum length = 1</td><tr><tr><td>nodeid</td><td>&lt;Double></td><td>Read-write</td><td>Unique number that identifies the cluster node.&lt;br>Minimum value = 0&lt;br>Maximum value = 31</td><tr><tr><td>domain</td><td>&lt;String></td><td>Read-only</td><td>The domain name.</td><tr><tr><td>srcip</td><td>&lt;String></td><td>Read-only</td><td>The client IP address.</td><tr><tr><td>srcport</td><td>&lt;Integer></td><td>Read-only</td><td>The client port.&lt;br>Range 1 - 65535&lt;br>* in CLI is represented as 65535 in NITRO API</td><tr><tr><td>destip</td><td>&lt;String></td><td>Read-only</td><td>The CPS server IP address.</td><tr><tr><td>destport</td><td>&lt;Integer></td><td>Read-only</td><td>The CPS server port.&lt;br>Range 1 - 65535&lt;br>* in CLI is represented as 65535 in NITRO API</td><tr><tr><td>channelnumber</td><td>&lt;Double></td><td>Read-only</td><td>The channel number.</td><tr><tr><td>peid</td><td>&lt;Double></td><td>Read-only</td><td>Core id of the session owner.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[GET (ALL)](#get-(all)) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnicadtlsconnection
Query-parameters:
args
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnicadtlsconnection?args=username:&lt;String_value&gt;,nodeid:&lt;Double_value&gt;
Use this query-parameter to get vpnicadtlsconnection resources based on additional properties.


attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnicadtlsconnection?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


filter
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnicadtlsconnection?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of vpnicadtlsconnection resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnicadtlsconnection?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).


pagination
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnicadtlsconnection?pagesize=#no;pageno=#no
Use this query-parameter to get the vpnicadtlsconnection resources in chunks.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "vpnicadtlsconnection": [ {username:<String_value>,nodeid:<Double_value>      "domain":<String_value>,      "srcip":<String_value>,      "srcport":<Integer_value>,      "destip":<String_value>,      "destport":<Integer_value>,      "channelnumber":<Double_value>,      "peid":<Double_value>}]}```



###count



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnicadtlsconnection?count=yes
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: 
{ "vpnicadtlsconnection": [ { "__count": "#no"} ] }


