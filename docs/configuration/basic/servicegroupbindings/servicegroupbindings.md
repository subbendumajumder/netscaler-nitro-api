#servicegroupbindings

Configuration for servicegroupbind resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>servicegroupname</td><td>&lt;String></td><td>Read-write</td><td>The name of the service.&lt;br>Minimum length = 1</td><tr><tr><td>ipaddress</td><td>&lt;String></td><td>Read-only</td><td>The IP address of the vserver.</td><tr><tr><td>port</td><td>&lt;Integer></td><td>Read-only</td><td>The port of the vserver.&lt;br>Range 1 - 65535</td><tr><tr><td>state</td><td>&lt;String></td><td>Read-only</td><td>The state of the service group.&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>svrstate</td><td>&lt;String></td><td>Read-only</td><td>The state of the vserver.&lt;br>Possible values = UP, DOWN, UNKNOWN, BUSY, OUT OF SERVICE, GOING OUT OF SERVICE, DOWN WHEN GOING OUT OF SERVICE, NS_EMPTY_STR, Unknown, DISABLED</td><tr><tr><td>vservername</td><td>&lt;String></td><td>Read-only</td><td>The name of the vserver.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/servicegroupbindings
Query-parameters:
args
http://&lt;NSIP&gt;/nitro/v1/config/servicegroupbindings?args=      "servicegroupname":&lt;String_value&gt;,
Use this query-parameter to get servicegroupbindings resources based on additional properties.


filter
http://&lt;NSIP&gt;/nitro/v1/config/servicegroupbindings?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of servicegroupbindings resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/servicegroupbindings?view=summary
Use this query-parameter to get the summary output of servicegroupbindings resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/servicegroupbindings?pagesize=#no;pageno=#no
Use this query-parameter to get the servicegroupbindings resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/servicegroupbindings?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "servicegroupbindings": [ {      "servicegroupname":<String_value>,      "ipaddress":<String_value>,      "port":<Integer_value>,      "state":<String_value>,      "svrstate":<String_value>,      "vservername":<String_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/servicegroupbindings/servicegroupname_value&lt;String&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "servicegroupbindings": [ {      "servicegroupname":<String_value>,      "ipaddress":<String_value>,      "port":<Integer_value>,      "state":<String_value>,      "svrstate":<String_value>,      "vservername":<String_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/servicegroupbindings?args=     "servicegroupname":&lt;String_value&gt;,;count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",servicegroupbindings: [ { "__count": "#no"} ] }


