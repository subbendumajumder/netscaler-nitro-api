#rdpconnections

Configuration for active rdp connections resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>username</td><td>&lt;String></td><td>Read-write</td><td>User name for which to display connections.&lt;br>Minimum length = 1</td><tr><tr><td>domain</td><td>&lt;String></td><td>Read-only</td><td>The domain name.</td><tr><tr><td>srcip</td><td>&lt;String></td><td>Read-only</td><td>The client IP address.</td><tr><tr><td>srcport</td><td>&lt;Integer></td><td>Read-only</td><td>The client port.&lt;br>Range 1 - 65535</td><tr><tr><td>destip</td><td>&lt;String></td><td>Read-only</td><td>The Server IP address.</td><tr><tr><td>destport</td><td>&lt;Integer></td><td>Read-only</td><td>The Client IP address.&lt;br>Range 1 - 65535</td><tr><tr><td>peid</td><td>&lt;Double></td><td>Read-only</td><td>Core id of the session owner.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[GET (ALL)](#get-(all)) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/rdpconnections
Query-parameters:
args
http://&lt;NSIP&gt;/nitro/v1/config/rdpconnections?args=      "username":&lt;String_value&gt;,
Use this query-parameter to get rdpconnections resources based on additional properties.


filter
http://&lt;NSIP&gt;/nitro/v1/config/rdpconnections?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of rdpconnections resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/rdpconnections?view=summary
Use this query-parameter to get the summary output of rdpconnections resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/rdpconnections?pagesize=#no;pageno=#no
Use this query-parameter to get the rdpconnections resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/rdpconnections?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "rdpconnections": [ {      "username":<String_value>,      "domain":<String_value>,      "srcip":<String_value>,      "srcport":<Integer_value>,      "destip":<String_value>,      "destport":<Integer_value>,      "peid":<Double_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/rdpconnections?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",rdpconnections: [ { "__count": "#no"} ] }


