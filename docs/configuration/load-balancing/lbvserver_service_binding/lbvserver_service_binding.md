#lbvserver_service_binding

Binding object showing the service that can be bound to lbvserver.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>weight</td><td>&lt;Double></td><td>Read-write</td><td>Weight to assign to the specified service.&lt;br>Minimum value = 1&lt;br>Maximum value = 100</td><tr><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the virtual server. Must begin with an ASCII alphanumeric or underscore (_) character, and must contain only ASCII alphanumeric, underscore, hash (#), period (.), space, colon (:), at sign (@), equal sign (=), and hyphen (-) characters. Can be changed after the virtual server is created. CLI Users: If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my vserver" or my vserver). .&lt;br>Minimum length = 1</td><tr><tr><td>servicename</td><td>&lt;String></td><td>Read-write</td><td>Service to bind to the virtual server.&lt;br>Minimum length = 1</td><tr><tr><td>servicegroupname</td><td>&lt;String></td><td>Read-write</td><td>Name of the service group.&lt;br>Minimum length = 1</td><tr><tr><td>vserverid</td><td>&lt;String></td><td>Read-only</td><td>Vserver Id.</td><tr><tr><td>vsvrbindsvcip</td><td>&lt;String></td><td>Read-only</td><td>used for showing the ip of bound entities.</td><tr><tr><td>servicetype</td><td>&lt;String></td><td>Read-only</td><td>Protocol used by the service (also called the service type).&lt;br>Possible values = HTTP, FTP, TCP, UDP, SSL, SSL_BRIDGE, SSL_TCP, DTLS, NNTP, DNS, DHCPRA, ANY, SIP_UDP, DNS_TCP, RTSP, PUSH, SSL_PUSH, RADIUS, RDP, MYSQL, MSSQL, DIAMETER, SSL_DIAMETER, TFTP, ORACLE</td><tr><tr><td>cookieipport</td><td>&lt;String></td><td>Read-only</td><td>Encryped Ip address and port of the service that is inserted into the set-cookie http header.</td><tr><tr><td>port</td><td>&lt;Integer></td><td>Read-only</td><td>Port number for the virtual server.&lt;br>Range 1 - 65535</td><tr><tr><td>vsvrbindsvcport</td><td>&lt;Integer></td><td>Read-only</td><td>used for showing ports of bound entities.&lt;br>Range 1 - 65535</td><tr><tr><td>curstate</td><td>&lt;String></td><td>Read-only</td><td>Current LB vserver state.&lt;br>Possible values = UP, DOWN, UNKNOWN, BUSY, OUT OF SERVICE, GOING OUT OF SERVICE, DOWN WHEN GOING OUT OF SERVICE, NS_EMPTY_STR, Unknown, DISABLED</td><tr><tr><td>ipv46</td><td>&lt;String></td><td>Read-only</td><td>IPv4 or IPv6 address to assign to the virtual server.</td><tr><tr><td>dynamicweight</td><td>&lt;Double></td><td>Read-only</td><td>Dynamic weight.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD:](#add:) | [DELETE:](#delete:) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add:



URL: http://NS_IP/nitro/v1/config
HTTP Method: PUT
Request Payload: ```{"params":{      "warning":<String_value>,      "onerror":<String_value>},sessionid":"##sessionid","lbvserver_service_binding":{      "name":<String_value>,      "servicename":<String_value>,                  "weight":<Double_value>,      "servicegroupname":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete:



URL: http://&lt;NS_IP&gt;/nitro/v1/config/lbvserver_service_binding/name_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/lbvserver_service_binding/name_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/lbvserver_service_binding/name_value&lt;String&gt;
Query-parameters:
filter
http://&lt;NS_IP&gt;/nitro/v1/config/lbvserver_service_binding/name_value&lt;String&gt;?filter=property-name1:property-value1,property-name2:property-value2
Use this query-parameter to get the filtered set of lbvserver_service_binding resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/lbvserver_service_binding/name_value&lt;String&gt;?pagesize=#no;pageno=#no
Use this query-parameter to get the lbvserver_service_binding resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/lbvserver_service_binding?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "lbvserver_service_binding": [ {      "weight":<Double_value>,      "name":<String_value>,      "servicename":<String_value>,      "servicegroupname":<String_value>,      "vserverid":<String_value>,      "vsvrbindsvcip":<String_value>,      "servicetype":<String_value>,      "cookieipport":<String_value>,      "port":<Integer_value>,      "vsvrbindsvcport":<Integer_value>,      "curstate":<String_value>,      "ipv46":<String_value>,      "dynamicweight":<Double_value>,}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/lbvserver_service_binding/name_value&lt;String&gt;?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",lbvserver_service_binding: [ { "__count": "#no"} ] }


