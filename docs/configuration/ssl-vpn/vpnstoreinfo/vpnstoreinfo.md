#vpnstoreinfo

Configuration for Store information for a URL resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>url</td><td>&lt;String></td><td>Read-write</td><td>StoreFront URL to be scanned.</td><tr><tr><td>storeserverstatus</td><td>&lt;String></td><td>Read-only</td><td>Availability of the server for TCP connections.&lt;br>Possible values = UP, DOWN</td><tr><tr><td>storeserverissf</td><td>&lt;String></td><td>Read-only</td><td>Indicates if the server being scanned is running StoreFront.&lt;br>Possible values = YES, NO</td><tr><tr><td>storeapisupport</td><td>&lt;String></td><td>Read-only</td><td>Indicates StoreFront API support status.&lt;br>Possible values = YES, NO</td><tr><tr><td>storelist</td><td>&lt;String></td><td>Read-only</td><td>List of available stores return by StoreFront API.</td><tr><tr><td>storestatus</td><td>&lt;String></td><td>Read-only</td><td>Availability of the specified StoreFront store.&lt;br>Possible values = UP, DOWN</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[GET (ALL)](#get-(all)) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnstoreinfo
Query-parameters:
args
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnstoreinfo?args=url:&lt;String_value&gt;,
Use this query-parameter to get vpnstoreinfo resources based on additional properties.


attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnstoreinfo?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


filter
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnstoreinfo?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of vpnstoreinfo resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnstoreinfo?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).


pagination
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnstoreinfo?pagesize=#no;pageno=#no
Use this query-parameter to get the vpnstoreinfo resources in chunks.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "vpnstoreinfo": [ {url:<String_value>,      "storeserverstatus":<String_value>,      "storeserverissf":<String_value>,      "storeapisupport":<String_value>,      "storelist":<String_value>,      "storestatus":<String_value>}]}```



###count



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnstoreinfo?args=url:&lt;String_value&gt;,;count=yes
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: 
{ "vpnstoreinfo": [ { "__count": "#no"} ] }


