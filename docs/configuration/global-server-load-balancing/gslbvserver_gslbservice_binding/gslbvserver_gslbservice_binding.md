#gslbvserver_gslbservice_binding

Binding object showing the gslbservice that can be bound to gslbvserver.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>weight</td><td>&lt;Double></td><td>Read-write</td><td>Weight to assign to the GSLB service.&lt;br>Minimum value = 1&lt;br>Maximum value = 100</td><tr><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name of the virtual server on which to perform the binding operation.&lt;br>Minimum length = 1</td><tr><tr><td>servicename</td><td>&lt;String></td><td>Read-write</td><td>Name of the GSLB service for which to change the weight.&lt;br>Minimum length = 1</td><tr><tr><td>domainname</td><td>&lt;String></td><td>Read-write</td><td>Domain name for which to change the time to live (TTL) and/or backup service IP address.&lt;br>Minimum length = 1</td><tr><tr><td>cnameentry</td><td>&lt;String></td><td>Read-only</td><td>The cname of the gslb service.</td><tr><tr><td>svcsitepersistence</td><td>&lt;String></td><td>Read-only</td><td>Type of Site Persistence set on the bound service.&lt;br>Possible values = ConnectionProxy, HTTPRedirect, NONE</td><tr><tr><td>gslbboundsvctype</td><td>&lt;String></td><td>Read-only</td><td>Protocol used by services bound to the GSLBvirtual server.&lt;br>Possible values = HTTP, FTP, TCP, UDP, SSL, SSL_BRIDGE, SSL_TCP, NNTP, ANY, SIP_UDP, SIP_TCP, SIP_SSL, RADIUS, RDP, RTSP, MYSQL, MSSQL, ORACLE</td><tr><tr><td>preferredlocation</td><td>&lt;String></td><td>Read-only</td><td>The target site to be returned in the DNS response when a policy is successfully evaluated against the incoming DNS request. Target site is specified in dotted notation with up to 6 qualifiers. Wildcard `* is accepted as a valid qualifier token.</td><tr><tr><td>dynamicconfwt</td><td>&lt;Double></td><td>Read-only</td><td>Weight obtained by the virtue of bound service count or weight.</td><tr><tr><td>cumulativeweight</td><td>&lt;Double></td><td>Read-only</td><td>Cumulative weight is the weight of GSLB service considering both its configured weight and dynamic weight. It is equal to product of dynamic weight and configured weight of the gslb service .</td><tr><tr><td>gslbthreshold</td><td>&lt;Integer></td><td>Read-only</td><td>Indicates if gslb svc has reached threshold.</td><tr><tr><td>sitepersistcookie</td><td>&lt;String></td><td>Read-only</td><td>This field is introduced for displaying the cookie in cluster setup.&lt;br>Minimum length = 1</td><tr><tr><td>port</td><td>&lt;Integer></td><td>Read-only</td><td>Port number.&lt;br>Range 1 - 65535&lt;br>* in CLI is represented as 65535 in NITRO API</td><tr><tr><td>iscname</td><td>&lt;String></td><td>Read-only</td><td>is cname feature set on vserver.&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>curstate</td><td>&lt;String></td><td>Read-only</td><td>State of the gslb vserver.&lt;br>Possible values = UP, DOWN, UNKNOWN, BUSY, OUT OF SERVICE, GOING OUT OF SERVICE, DOWN WHEN GOING OUT OF SERVICE, NS_EMPTY_STR, Unknown, DISABLED</td><tr><tr><td>svreffgslbstate</td><td>&lt;String></td><td>Read-only</td><td>Effective state of the gslb svc.&lt;br>Possible values = UP, DOWN, UNKNOWN, BUSY, OUT OF SERVICE, GOING OUT OF SERVICE, DOWN WHEN GOING OUT OF SERVICE, NS_EMPTY_STR, Unknown, DISABLED</td><tr><tr><td>thresholdvalue</td><td>&lt;Integer></td><td>Read-only</td><td>Tells whether threshold exceeded for this service participating in CUSTOMLB.</td><tr><tr><td>ipaddress</td><td>&lt;String></td><td>Read-only</td><td>IP address.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD:](#add:) | [DELETE:](#delete:) | [GET](#get) | [GET (ALL)](#get-(all)) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add:



URL: http://&lt;netscaler-ip-address/nitro/v1/config/gslbvserver_gslbservice_binding
HTTP Method: PUT
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"gslbvserver_gslbservice_binding":{      "name":<String_value>,      "servicename":<String_value>,      "weight":<Double_value>,      "domainname":<String_value>}}```
Response:
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete:



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbvserver_gslbservice_binding/name_value&lt;String&gt;
HTTP Method: DELETE
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbvserver_gslbservice_binding/name_value&lt;String&gt;
Query-parameters:
filter
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbvserver_gslbservice_binding/name_value&lt;String&gt;?filter=property-name1:property-value1,property-name2:property-value2
Use this query-parameter to get the filtered set of gslbvserver_gslbservice_binding resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


pagination
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbvserver_gslbservice_binding/name_value&lt;String&gt;?pagesize=#no;pageno=#no
Use this query-parameter to get the gslbvserver_gslbservice_binding resources in chunks.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "gslbvserver_gslbservice_binding": [ {      "weight":<Double_value>,      "name":<String_value>,      "servicename":<String_value>,      "domainname":<String_value>,      "cnameentry":<String_value>,      "svcsitepersistence":<String_value>,      "gslbboundsvctype":<String_value>,      "preferredlocation":<String_value>,      "dynamicconfwt":<Double_value>,      "cumulativeweight":<Double_value>,      "gslbthreshold":<Integer_value>,      "sitepersistcookie":<String_value>,      "port":<Integer_value>,      "iscname":<String_value>,      "curstate":<String_value>,      "svreffgslbstate":<String_value>,      "thresholdvalue":<Integer_value>,      "ipaddress":<String_value>}]}```



###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbvserver_gslbservice_binding
Query-parameters:
bulkbindings
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbvserver_gslbservice_binding?bulkbindings=yes
NITRO allows you to fetch bindings in bulk.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "gslbvserver_gslbservice_binding": [ {      "weight":<Double_value>,      "name":<String_value>,      "servicename":<String_value>,      "domainname":<String_value>,      "cnameentry":<String_value>,      "svcsitepersistence":<String_value>,      "gslbboundsvctype":<String_value>,      "preferredlocation":<String_value>,      "dynamicconfwt":<Double_value>,      "cumulativeweight":<Double_value>,      "gslbthreshold":<Integer_value>,      "sitepersistcookie":<String_value>,      "port":<Integer_value>,      "iscname":<String_value>,      "curstate":<String_value>,      "svreffgslbstate":<String_value>,      "thresholdvalue":<Integer_value>,      "ipaddress":<String_value>}]}```



###count



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbvserver_gslbservice_binding/name_value&lt;String&gt;?count=yes
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: 
{"gslbvserver_gslbservice_binding": [ { "__count": "#no"} ] }


