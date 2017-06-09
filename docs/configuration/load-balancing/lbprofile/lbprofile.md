#lbprofile

Configuration for LB profile resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>lbprofilename</td><td>&lt;String></td><td>Read-write</td><td>Name of the LB profile.&lt;br>Minimum length = 1</td><tr><tr><td>dbslb</td><td>&lt;String></td><td>Read-write</td><td>Enable database specific load balancing for MySQL and MSSQL service types.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>processlocal</td><td>&lt;String></td><td>Read-write</td><td>By turning on this option packets destined to a vserver in a cluster will not under go any steering. Turn this option for single pa&lt;br>cket request response mode or when the upstream device is performing a proper RSS for connection based distribution.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>httponlycookieflag</td><td>&lt;String></td><td>Read-write</td><td>Include the HttpOnly attribute in persistence cookies. The HttpOnly attribute limits the scope of a cookie to HTTP requests and helps mitigate the risk of cross-site scripting attacks.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>cookiepassphrase</td><td>&lt;String></td><td>Read-write</td><td>Use this parameter to specify the passphrase used to generate secured persistence cookie value. It specifies the passphrase with a maximum of 31 characters.</td><tr><tr><td>usesecuredpersistencecookie</td><td>&lt;String></td><td>Read-write</td><td>Encode persistence cookie values using SHA2 hash.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>vsvrcount</td><td>&lt;Double></td><td>Read-only</td><td>Total number of vservers , the profile is bound to.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [DELETE](#delete) | [UPDATE](#update) | [UNSET](#unset) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lbprofile
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"lbprofile":{      "lbprofilename":<String_value>,      "dbslb":<String_value>,      "processlocal":<String_value>,      "httponlycookieflag":<String_value>,      "cookiepassphrase":<String_value>,      "usesecuredpersistencecookie":<String_value>}}```
Response:
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lbprofile/lbprofilename_value&lt;String&gt;
HTTP Method: DELETE
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lbprofile
HTTP Method: PUT
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"lbprofile":{      "lbprofilename":<String_value>,      "dbslb":<String_value>,      "processlocal":<String_value>,      "httponlycookieflag":<String_value>,      "cookiepassphrase":<String_value>,      "usesecuredpersistencecookie":<String_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lbprofile?action=unset
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"lbprofile":{      "lbprofilename":<String_value>,      "dbslb":true,      "processlocal":true,      "httponlycookieflag":true,      "cookiepassphrase":true,      "usesecuredpersistencecookie":true}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lbprofile
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lbprofile?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


filter
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lbprofile?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of lbprofile resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lbprofile?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).


pagination
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lbprofile?pagesize=#no;pageno=#no
Use this query-parameter to get the lbprofile resources in chunks.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "lbprofile": [ {      "lbprofilename":<String_value>,      "dbslb":<String_value>,      "processlocal":<String_value>,      "httponlycookieflag":<String_value>,      "cookiepassphrase":<String_value>,      "usesecuredpersistencecookie":<String_value>,      "vsvrcount":<Double_value>}]}```



###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lbprofile/lbprofilename_value&lt;String&gt;
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lbprofile/lbprofilename_value&lt;String&gt;?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lbprofile/lbprofilename_value&lt;String&gt;?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "lbprofile": [ {      "lbprofilename":<String_value>,      "dbslb":<String_value>,      "processlocal":<String_value>,      "httponlycookieflag":<String_value>,      "cookiepassphrase":<String_value>,      "usesecuredpersistencecookie":<String_value>,      "vsvrcount":<Double_value>}]}```



###count



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lbprofile?count=yes
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: 
{ "lbprofile": [ { "__count": "#no"} ] }


