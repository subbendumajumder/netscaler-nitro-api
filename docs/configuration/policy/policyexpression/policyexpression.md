#policyexpression

Configuration for expression resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Unique name for the expression. Not case sensitive. Must begin with an ASCII letter or underscore (_) character, and must consist only of ASCII alphanumeric or underscore characters. Must not begin with re or xp or be a word reserved for use as a default syntax expression qualifier prefix (such as HTTP) or enumeration value (such as ASCII). Must not be the name of an existing named expression, pattern set, dataset, stringmap, or HTTP callout.&lt;br>Minimum length = 1</td><tr><tr><td>value</td><td>&lt;String></td><td>Read-write</td><td>Expression string. For example: http.req.body(100).contains("this").</td><tr><tr><td>description</td><td>&lt;String></td><td>Read-write</td><td>Description for the expression.</td><tr><tr><td>comment</td><td>&lt;String></td><td>Read-write</td><td>Any comments associated with the expression. Displayed upon viewing the policy expression.</td><tr><tr><td>clientsecuritymessage</td><td>&lt;String></td><td>Read-write</td><td>Message to display if the expression fails. Allowed for classic end-point check expressions only.&lt;br>Minimum length = 1</td><tr><tr><td>type</td><td>&lt;String></td><td>Read-write</td><td>Type of expression. Can be a classic or default syntax (advanced) expression.&lt;br>Possible values = CLASSIC, ADVANCED</td><tr><tr><td>hits</td><td>&lt;Double></td><td>Read-only</td><td>The total number of hits.</td><tr><tr><td>pihits</td><td>&lt;Double></td><td>Read-only</td><td>The total number of hits.</td><tr><tr><td>type1</td><td>&lt;String></td><td>Read-only</td><td>The type of expression. This is for output only.&lt;br>Possible values = CLASSIC, ADVANCED</td><tr><tr><td>isdefault</td><td>&lt;Boolean></td><td>Read-only</td><td>A value of true is returned if it is a default policy expression.</td><tr><tr><td>builtin</td><td>&lt;String[]></td><td>Read-only</td><td>Indicates that a variable is a built-in (SYSTEM INTERNAL) type.&lt;br>Possible values = MODIFIABLE, DELETABLE, IMMUTABLE</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [DELETE](#delete) | [UPDATE](#update) | [UNSET](#unset) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>},"sessionid":"##sessionid","policyexpression":{      "name":<String_value>,      "value":<String_value>,      "description":<String_value>,      "comment":<String_value>,      "clientsecuritymessage":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/policyexpression/name_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/policyexpression/name_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","policyexpression":{      "name":<String_value>,      "value":<String_value>,      "description":<String_value>,      "comment":<String_value>,      "clientsecuritymessage":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","policyexpression":{      "name":<String_value>,      "description":true,      "comment":true,      "clientsecuritymessage":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/policyexpression
Query-parameters:
args
http://&lt;NSIP&gt;/nitro/v1/config/policyexpression?args=      "name":&lt;String_value&gt;,      "type":&lt;String_value&gt;,
Use this query-parameter to get policyexpression resources based on additional properties.


filter
http://&lt;NSIP&gt;/nitro/v1/config/policyexpression?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of policyexpression resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/policyexpression?view=summary
Use this query-parameter to get the summary output of policyexpression resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/policyexpression?pagesize=#no;pageno=#no
Use this query-parameter to get the policyexpression resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/policyexpression?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "policyexpression": [ {      "name":<String_value>,      "type":<String_value>,      "value":<String_value>,      "hits":<Double_value>,      "pihits":<Double_value>,      "type1":<String_value>,      "clientsecuritymessage":<String_value>,      "description":<String_value>,      "comment":<String_value>,      "isdefault":<Boolean_value>,      "builtin":<String[]_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/policyexpression/name_value&lt;String&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "policyexpression": [ {      "name":<String_value>,      "type":<String_value>,      "value":<String_value>,      "hits":<Double_value>,      "pihits":<Double_value>,      "type1":<String_value>,      "clientsecuritymessage":<String_value>,      "description":<String_value>,      "comment":<String_value>,      "isdefault":<Boolean_value>,      "builtin":<String[]_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/policyexpression?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",policyexpression: [ { "__count": "#no"} ] }


