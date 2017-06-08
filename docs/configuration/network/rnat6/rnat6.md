#rnat6

Configuration for IPv6 RNAT configured route resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the RNAT6 rule. Must begin with a letter, number, or the underscore character (_), and can consist of letters, numbers, and the hyphen (-), period (.) pound (#), space ( ), at sign (@), equals (=), colon (:), and underscore characters. Cannot be changed after the rule is created. Choose a name that helps identify the RNAT6 rule.&lt;br>Minimum length = 1</td><tr><tr><td>network</td><td>&lt;String></td><td>Read-write</td><td>IPv6 address of the network on whose traffic you want the NetScaler appliance to do RNAT processing.&lt;br>Minimum length = 1</td><tr><tr><td>acl6name</td><td>&lt;String></td><td>Read-write</td><td>Name of any configured ACL6 whose action is ALLOW. The rule of the ACL6 is used as an RNAT6 rule.&lt;br>Minimum length = 1</td><tr><tr><td>redirectport</td><td>&lt;Integer></td><td>Read-write</td><td>Port number to which the IPv6 packets are redirected. Applicable to TCP and UDP protocols.&lt;br>Minimum value = 1&lt;br>Maximum value = 65535</td><tr><tr><td>td</td><td>&lt;Double></td><td>Read-write</td><td>Integer value that uniquely identifies the traffic domain in which you want to configure the entity. If you do not specify an ID, the entity becomes part of the default traffic domain, which has an ID of 0.&lt;br>Minimum value = 0&lt;br>Maximum value = 4094</td><tr><tr><td>srcippersistency</td><td>&lt;String></td><td>Read-write</td><td>Enable source ip persistency, which enables the NetScaler appliance to use the RNAT ips using source ip.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [UPDATE](#update) | [UNSET](#unset) | [CLEAR](#clear) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>},"sessionid":"##sessionid","rnat6":{      "name":<String_value>,      "network":<String_value>,      "acl6name":<String_value>,                  "redirectport":<Integer_value>,      "td":<Double_value>,      "srcippersistency":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","rnat6":{      "name":<String_value>,      "redirectport":<Integer_value>,      "srcippersistency":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","rnat6":{      "name":<String_value>,      "redirectport":true,      "srcippersistency":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###clear



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"clear"},"sessionid":"##sessionid","rnat6":{      "name":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/rnat6
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/rnat6?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of rnat6 resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/rnat6?view=summary
Use this query-parameter to get the summary output of rnat6 resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/rnat6?pagesize=#no;pageno=#no
Use this query-parameter to get the rnat6 resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/rnat6?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "rnat6": [ {      "name":<String_value>,      "network":<String_value>,      "td":<Double_value>,      "acl6name":<String_value>,      "redirectport":<Integer_value>,      "srcippersistency":<String_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/rnat6/name_value&lt;String&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "rnat6": [ {      "name":<String_value>,      "network":<String_value>,      "td":<Double_value>,      "acl6name":<String_value>,      "redirectport":<Integer_value>,      "srcippersistency":<String_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/rnat6?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",rnat6: [ { "__count": "#no"} ] }


