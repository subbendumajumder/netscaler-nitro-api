#aaasession

Configuration for active connection resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>username</td><td>&lt;String></td><td>Read-write</td><td>Name of the AAA user.&lt;br>Minimum length = 1</td><tr><tr><td>groupname</td><td>&lt;String></td><td>Read-write</td><td>Name of the AAA group.&lt;br>Minimum length = 1</td><tr><tr><td>iip</td><td>&lt;String></td><td>Read-write</td><td>IP address or the first address in the intranet IP range.&lt;br>Minimum length = 1</td><tr><tr><td>netmask</td><td>&lt;String></td><td>Read-write</td><td>Subnet mask for the intranet IP range.&lt;br>Minimum length = 1</td><tr><tr><td>all</td><td>&lt;Boolean></td><td>Read-write</td><td>Terminate all active AAA-TM/VPN sessions.</td><tr><tr><td>publicip</td><td>&lt;String></td><td>Read-only</td><td>Clients public IP address.</td><tr><tr><td>publicport</td><td>&lt;Integer></td><td>Read-only</td><td>Clients public port.&lt;br>Range 1 - 65535</td><tr><tr><td>ipaddress</td><td>&lt;String></td><td>Read-only</td><td>NetScalers IP address.</td><tr><tr><td>port</td><td>&lt;Integer></td><td>Read-only</td><td>NetScalers port.&lt;br>Range 1 - 65535</td><tr><tr><td>privateip</td><td>&lt;String></td><td>Read-only</td><td>Clients private/mapped IP address.</td><tr><tr><td>privateport</td><td>&lt;Integer></td><td>Read-only</td><td>Clients private/mapped port.&lt;br>Range 1 - 65535</td><tr><tr><td>destip</td><td>&lt;String></td><td>Read-only</td><td>Destination IP address.</td><tr><tr><td>destport</td><td>&lt;Integer></td><td>Read-only</td><td>Destination port.&lt;br>Range 1 - 65535</td><tr><tr><td>intranetip</td><td>&lt;String></td><td>Read-only</td><td>Specifies the Intranet IP.</td><tr><tr><td>peid</td><td>&lt;Double></td><td>Read-only</td><td>Core id of the session owner.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[KILL](#kill) | [GET (ALL)](#get-(all)) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###kill



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"kill"},"sessionid":"##sessionid","aaasession":{      "username":<String_value>,      "groupname":<String_value>,      "iip":<String_value>,                  "netmask":<String_value>,      "all":<Boolean_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/aaasession
Query-parameters:
args
http://&lt;NSIP&gt;/nitro/v1/config/aaasession?args=      "username":&lt;String_value&gt;,      "groupname":&lt;String_value&gt;,      "iip":&lt;String_value&gt;,                  "netmask":&lt;String_value&gt;,
Use this query-parameter to get aaasession resources based on additional properties.


filter
http://&lt;NSIP&gt;/nitro/v1/config/aaasession?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of aaasession resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/aaasession?view=summary
Use this query-parameter to get the summary output of aaasession resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/aaasession?pagesize=#no;pageno=#no
Use this query-parameter to get the aaasession resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/aaasession?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "aaasession": [ {      "username":<String_value>,      "groupname":<String_value>,      "iip":<String_value>,                  "netmask":<String_value>,      "publicip":<String_value>,      "publicport":<Integer_value>,      "ipaddress":<String_value>,      "port":<Integer_value>,      "privateip":<String_value>,      "privateport":<Integer_value>,      "destip":<String_value>,      "destport":<Integer_value>,      "intranetip":<String_value>,      "peid":<Double_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/aaasession?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",aaasession: [ { "__count": "#no"} ] }


