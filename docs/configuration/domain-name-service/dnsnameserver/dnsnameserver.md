#dnsnameserver

Configuration for name server resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>ip</td><td>&lt;String></td><td>Read-write</td><td>IP address of an external name server or, if the Local parameter is set, IP address of a local DNS server (LDNS).&lt;br>Minimum length = 1</td><tr><tr><td>dnsvservername</td><td>&lt;String></td><td>Read-write</td><td>Name of a DNS virtual server. Overrides any IP address-based name servers configured on the NetScaler appliance.&lt;br>Minimum length = 1</td><tr><tr><td>local</td><td>&lt;Boolean></td><td>Read-write</td><td>Mark the IP address as one that belongs to a local recursive DNS server on the NetScaler appliance. The appliance recursively resolves queries received on an IP address that is marked as being local. For recursive resolution to work, the global DNS parameter, Recursion, must also be set. If no name server is marked as being local, the appliance functions as a stub resolver and load balances the name servers.</td><tr><tr><td>state</td><td>&lt;String></td><td>Read-write</td><td>Administrative state of the name server.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>type</td><td>&lt;String></td><td>Read-write</td><td>Protocol used by the name server. UDP_TCP is not valid if the name server is a DNS virtual server configured on the appliance.&lt;br>Default value: UDP&lt;br>Possible values = UDP, TCP, UDP_TCP</td><tr><tr><td>servicename</td><td>&lt;String></td><td>Read-only</td><td>The name of the dns vserver.</td><tr><tr><td>port</td><td>&lt;Integer></td><td>Read-only</td><td>Port of the service.&lt;br>Range 1 - 65535</td><tr><tr><td>nameserverstate</td><td>&lt;String></td><td>Read-only</td><td>State of the server.&lt;br>Possible values = UP, DOWN, UNKNOWN, BUSY, OUT OF SERVICE, GOING OUT OF SERVICE, DOWN WHEN GOING OUT OF SERVICE, NS_EMPTY_STR, Unknown, DISABLED</td><tr><tr><td>clmonowner</td><td>&lt;Double></td><td>Read-only</td><td>Tells the mon owner of the service.</td><tr><tr><td>clmonview</td><td>&lt;Double></td><td>Read-only</td><td>Tells the view id by which state of the service is updated.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [DELETE](#delete) | [ENABLE](#enable) | [DISABLE](#disable) | [GET (ALL)](#get-(all)) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>},"sessionid":"##sessionid","dnsnameserver":{      "ip":<String_value>,      "dnsvservername":<String_value>,      "local":<Boolean_value>,      "state":<String_value>,      "type":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/dnsnameserver/ip_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/dnsnameserver/ip_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###enable



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"enable"},"sessionid":"##sessionid","dnsnameserver":{      "ip":<String_value>,      "dnsvservername":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###disable



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"disable"},"sessionid":"##sessionid","dnsnameserver":{      "ip":<String_value>,      "dnsvservername":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/dnsnameserver
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/dnsnameserver?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of dnsnameserver resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/dnsnameserver?view=summary
Use this query-parameter to get the summary output of dnsnameserver resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/dnsnameserver?pagesize=#no;pageno=#no
Use this query-parameter to get the dnsnameserver resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/dnsnameserver?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "dnsnameserver": [ {      "ip":<String_value>,      "dnsvservername":<String_value>,      "servicename":<String_value>,      "port":<Integer_value>,      "type":<String_value>,      "state":<String_value>,      "nameserverstate":<String_value>,      "local":<Boolean_value>,      "clmonowner":<Double_value>,      "clmonview":<Double_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/dnsnameserver?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",dnsnameserver: [ { "__count": "#no"} ] }


