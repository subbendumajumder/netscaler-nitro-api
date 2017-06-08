#nssimpleacl

Configuration for simple ACL resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>aclname</td><td>&lt;String></td><td>Read-write</td><td>Name for the simple ACL rule. Must begin with an ASCII alphabetic or underscore (_) character, and must contain only ASCII alphanumeric, underscore, hash (#), period (.), space, colon (:), at (@), equals (=), and hyphen (-) characters. Cannot be changed after the simple ACL rule is created.&lt;br>Minimum length = 1</td><tr><tr><td>aclaction</td><td>&lt;String></td><td>Read-write</td><td>Drop incoming IPv4 packets that match the simple ACL rule.&lt;br>Possible values = DENY</td><tr><tr><td>td</td><td>&lt;Double></td><td>Read-write</td><td>Integer value that uniquely identifies the traffic domain in which you want to configure the entity. If you do not specify an ID, the entity becomes part of the default traffic domain, which has an ID of 0.&lt;br>Minimum value = 0&lt;br>Maximum value = 4094</td><tr><tr><td>srcip</td><td>&lt;String></td><td>Read-write</td><td>IP address to match against the source IP address of an incoming IPv4 packet.</td><tr><tr><td>destport</td><td>&lt;Integer></td><td>Read-write</td><td>Port number to match against the destination port number of an incoming IPv4 packet. Omitting the port number creates an all-ports simple ACL rule, which matches any port. In that case, you cannot create another simple ACL rule specifying a specific port and the same source IPv4 address.</td><tr><tr><td>protocol</td><td>&lt;String></td><td>Read-write</td><td>Protocol to match against the protocol of an incoming IPv4 packet. You must set this parameter if you have set the Destination Port parameter.&lt;br>Possible values = TCP, UDP</td><tr><tr><td>ttl</td><td>&lt;Double></td><td>Read-write</td><td>Number of seconds, in multiples of four, after which the simple ACL rule expires. If you do not want the simple ACL rule to expire, do not specify a TTL value.&lt;br>Minimum value = 4&lt;br>Maximum value = 2147483647</td><tr><tr><td>estsessions</td><td>&lt;Boolean></td><td>Read-write</td><td>.</td><tr><tr><td>hits</td><td>&lt;Double></td><td>Read-only</td><td>Number of hits for this ACL rule.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [CLEAR](#clear) | [DELETE](#delete) | [FLUSH](#flush) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>},"sessionid":"##sessionid","nssimpleacl":{      "aclname":<String_value>,      "aclaction":<String_value>,      "td":<Double_value>,      "srcip":<String_value>,      "destport":<Integer_value>,                  "protocol":<String_value>,      "ttl":<Double_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###clear



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"clear"},"sessionid":"##sessionid","nssimpleacl":{}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/nssimpleacl/aclname_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/nssimpleacl/aclname_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###flush



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"flush"},"sessionid":"##sessionid","nssimpleacl":{      "estsessions":<Boolean_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/nssimpleacl
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/nssimpleacl?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of nssimpleacl resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/nssimpleacl?view=summary
Use this query-parameter to get the summary output of nssimpleacl resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/nssimpleacl?pagesize=#no;pageno=#no
Use this query-parameter to get the nssimpleacl resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/nssimpleacl?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "nssimpleacl": [ {      "aclname":<String_value>,      "aclaction":<String_value>,      "td":<Double_value>,      "srcip":<String_value>,      "destport":<Integer_value>,      "protocol":<String_value>,      "ttl":<Double_value>,      "hits":<Double_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/nssimpleacl/aclname_value&lt;String&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "nssimpleacl": [ {      "aclname":<String_value>,      "aclaction":<String_value>,      "td":<Double_value>,      "srcip":<String_value>,      "destport":<Integer_value>,      "protocol":<String_value>,      "ttl":<Double_value>,      "hits":<Double_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/nssimpleacl?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",nssimpleacl: [ { "__count": "#no"} ] }


