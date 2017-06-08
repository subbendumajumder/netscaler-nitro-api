#ip6tunnel

Configuration for ip6 Tunnel resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the IPv6 Tunnel. Cannot be changed after the service group is created. Must begin with a number or letter, and can consist of letters, numbers, and the @ _ - . (period) : (colon) # and space ( ) characters.&lt;br>Minimum length = 1&lt;br>Maximum length = 31</td><tr><tr><td>remote</td><td>&lt;String></td><td>Read-write</td><td>An IPv6 address of the remote NetScaler appliance used to set up the tunnel.&lt;br>Minimum length = 1</td><tr><tr><td>local</td><td>&lt;String></td><td>Read-write</td><td>An IPv6 address of the local NetScaler appliance used to set up the tunnel.</td><tr><tr><td>remoteip</td><td>&lt;String></td><td>Read-only</td><td>The remote IP address or subnet of the tunnel.</td><tr><tr><td>type</td><td>&lt;Double></td><td>Read-only</td><td>The type of this tunnel.</td><tr><tr><td>encapip</td><td>&lt;String></td><td>Read-only</td><td>The effective local IP address of the tunnel. Used as the source of the encapsulated packets.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [DELETE](#delete) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>},"sessionid":"##sessionid","ip6tunnel":{      "name":<String_value>,      "remote":<String_value>,      "local":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/ip6tunnel/name_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/ip6tunnel/name_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/ip6tunnel
Query-parameters:
args
http://&lt;NSIP&gt;/nitro/v1/config/ip6tunnel?args=      "name":&lt;String_value&gt;,      "remote":&lt;String_value&gt;,
Use this query-parameter to get ip6tunnel resources based on additional properties.


filter
http://&lt;NSIP&gt;/nitro/v1/config/ip6tunnel?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of ip6tunnel resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/ip6tunnel?view=summary
Use this query-parameter to get the summary output of ip6tunnel resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/ip6tunnel?pagesize=#no;pageno=#no
Use this query-parameter to get the ip6tunnel resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/ip6tunnel?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "ip6tunnel": [ {      "name":<String_value>,      "remote":<String_value>,      "remoteip":<String_value>,      "local":<String_value>,      "type":<Double_value>,      "encapip":<String_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/ip6tunnel/name_value&lt;String&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "ip6tunnel": [ {      "name":<String_value>,      "remote":<String_value>,      "remoteip":<String_value>,      "local":<String_value>,      "type":<Double_value>,      "encapip":<String_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/ip6tunnel?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",ip6tunnel: [ { "__count": "#no"} ] }


