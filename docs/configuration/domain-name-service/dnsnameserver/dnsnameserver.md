#dnsnameserver

Configuration for name server resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>ip</td><td>&lt;String></td><td>Read-write</td><td>IP address of an external name server or, if the Local parameter is set, IP address of a local DNS server (LDNS).&lt;br>Minimum length = 1</td><tr><tr><td>dnsvservername</td><td>&lt;String></td><td>Read-write</td><td>Name of a DNS virtual server. Overrides any IP address-based name servers configured on the NetScaler appliance.&lt;br>Minimum length = 1</td><tr><tr><td>local</td><td>&lt;Boolean></td><td>Read-write</td><td>Mark the IP address as one that belongs to a local recursive DNS server on the NetScaler appliance. The appliance recursively resolves queries received on an IP address that is marked as being local. For recursive resolution to work, the global DNS parameter, Recursion, must also be set. &lt;br>&lt;br>If no name server is marked as being local, the appliance functions as a stub resolver and load balances the name servers.</td><tr><tr><td>state</td><td>&lt;String></td><td>Read-write</td><td>Administrative state of the name server.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>type</td><td>&lt;String></td><td>Read-write</td><td>Protocol used by the name server. UDP_TCP is not valid if the name server is a DNS virtual server configured on the appliance.&lt;br>Default value: UDP&lt;br>Possible values = UDP, TCP, UDP_TCP</td><tr><tr><td>dnsprofilename</td><td>&lt;String></td><td>Read-write</td><td>Name of the DNS profile to be associated with the name server.&lt;br>Minimum length = 1</td><tr><tr><td>servicename</td><td>&lt;String></td><td>Read-only</td><td>The name of the dns vserver.</td><tr><tr><td>port</td><td>&lt;Integer></td><td>Read-only</td><td>Port of the service.&lt;br>Range 1 - 65535&lt;br>* in CLI is represented as 65535 in NITRO API</td><tr><tr><td>nameserverstate</td><td>&lt;String></td><td>Read-only</td><td>State of the server.&lt;br>Possible values = UP, DOWN, UNKNOWN, BUSY, OUT OF SERVICE, GOING OUT OF SERVICE, DOWN WHEN GOING OUT OF SERVICE, NS_EMPTY_STR, Unknown, DISABLED</td><tr><tr><td>clmonowner</td><td>&lt;Double></td><td>Read-only</td><td>Tells the mon owner of the service.</td><tr><tr><td>clmonview</td><td>&lt;Double></td><td>Read-only</td><td>Tells the view id by which state of the service is updated.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [UPDATE](#update) | [UNSET](#unset) | [DELETE](#delete) | [ENABLE](#enable) | [DISABLE](#disable) | [GET (ALL)](#get-(all)) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnsnameserver
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"dnsnameserver":{      "ip":<String_value>,      "dnsvservername":<String_value>,      "local":<Boolean_value>,      "state":<String_value>,      "type":<String_value>,      "dnsprofilename":<String_value>}}```
Response:
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnsnameserver
HTTP Method: PUT
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"dnsnameserver":{      "ip":<String_value>,      "dnsprofilename":<String_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnsnameserver?action=unset
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"dnsnameserver":{      "ip":<String_value>,      "dnsprofilename":true}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnsnameserver/ip_value&lt;String&gt;
HTTP Method: DELETE
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###enable



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnsnameserver?action=enable
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"dnsnameserver":{      "ip":<String_value>,      "dnsvservername":<String_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###disable



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnsnameserver?action=disable
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"dnsnameserver":{      "ip":<String_value>,      "dnsvservername":<String_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnsnameserver
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnsnameserver?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


filter
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnsnameserver?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of dnsnameserver resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnsnameserver?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).


pagination
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnsnameserver?pagesize=#no;pageno=#no
Use this query-parameter to get the dnsnameserver resources in chunks.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "dnsnameserver": [ {      "ip":<String_value>,      "dnsvservername":<String_value>,      "servicename":<String_value>,      "port":<Integer_value>,      "type":<String_value>,      "state":<String_value>,      "nameserverstate":<String_value>,      "local":<Boolean_value>,      "clmonowner":<Double_value>,      "clmonview":<Double_value>,      "dnsprofilename":<String_value>}]}```



###count



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnsnameserver?count=yes
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: 
{ "dnsnameserver": [ { "__count": "#no"} ] }


