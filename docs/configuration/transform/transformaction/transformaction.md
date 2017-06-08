#transformaction

Configuration for transform action resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the URL transformation action. Must begin with a letter, number, or the underscore character (_), and must contain only letters, numbers, and the hyphen (-), period (.) pound (#), space ( ), at (@), equals (=), colon (:), and underscore characters. Cannot be changed after the URL Transformation action is added. The following requirement applies only to the NetScaler CLI: If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, ?my transform action? or ?my transform action).&lt;br>Minimum length = 1</td><tr><tr><td>profilename</td><td>&lt;String></td><td>Read-write</td><td>Name of the URL Transformation profile with which to associate this action.&lt;br>Minimum length = 1</td><tr><tr><td>priority</td><td>&lt;Double></td><td>Read-write</td><td>Positive integer specifying the priority of the action within the profile. A lower number specifies a higher priority. Must be unique within the list of actions bound to the profile. Policies are evaluated in the order of their priority numbers, and the first policy that matches is applied.&lt;br>Minimum value = 1&lt;br>Maximum value = 2147483647</td><tr><tr><td>state</td><td>&lt;String></td><td>Read-write</td><td>Enable or disable this action.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>requrlfrom</td><td>&lt;String></td><td>Read-write</td><td>PCRE-format regular expression that describes the request URL pattern to be transformed.&lt;br>Minimum length = 1</td><tr><tr><td>requrlinto</td><td>&lt;String></td><td>Read-write</td><td>PCRE-format regular expression that describes the transformation to be performed on URLs that match the reqUrlFrom pattern.&lt;br>Minimum length = 1</td><tr><tr><td>resurlfrom</td><td>&lt;String></td><td>Read-write</td><td>PCRE-format regular expression that describes the response URL pattern to be transformed.&lt;br>Minimum length = 1</td><tr><tr><td>resurlinto</td><td>&lt;String></td><td>Read-write</td><td>PCRE-format regular expression that describes the transformation to be performed on URLs that match the resUrlFrom pattern.&lt;br>Minimum length = 1</td><tr><tr><td>cookiedomainfrom</td><td>&lt;String></td><td>Read-write</td><td>Pattern that matches the domain to be transformed in Set-Cookie headers.&lt;br>Minimum length = 1</td><tr><tr><td>cookiedomaininto</td><td>&lt;String></td><td>Read-write</td><td>PCRE-format regular expression that describes the transformation to be performed on cookie domains that match the cookieDomainFrom pattern. NOTE: The cookie domain to be transformed is extracted from the request.&lt;br>Minimum length = 1</td><tr><tr><td>comment</td><td>&lt;String></td><td>Read-write</td><td>Any comments to preserve information about this URL Transformation action.</td><tr><tr><td>continuematching</td><td>&lt;String></td><td>Read-only</td><td>Continue transforming using the next rule in the list.&lt;br>Possible values = ON, OFF</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
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
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>},"sessionid":"##sessionid","transformaction":{      "name":<String_value>,      "profilename":<String_value>,      "priority":<Double_value>,      "state":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/transformaction/name_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/transformaction/name_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","transformaction":{      "name":<String_value>,      "priority":<Double_value>,      "requrlfrom":<String_value>,      "requrlinto":<String_value>,      "resurlfrom":<String_value>,      "resurlinto":<String_value>,      "cookiedomainfrom":<String_value>,      "cookiedomaininto":<String_value>,      "state":<String_value>,      "comment":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","transformaction":{      "name":<String_value>,      "requrlfrom":true,      "requrlinto":true,      "resurlfrom":true,      "resurlinto":true,      "cookiedomainfrom":true,      "cookiedomaininto":true,      "state":true,      "comment":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/transformaction
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/transformaction?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of transformaction resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/transformaction?view=summary
Use this query-parameter to get the summary output of transformaction resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/transformaction?pagesize=#no;pageno=#no
Use this query-parameter to get the transformaction resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/transformaction?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "transformaction": [ {      "name":<String_value>,      "profilename":<String_value>,      "priority":<Double_value>,      "requrlfrom":<String_value>,      "requrlinto":<String_value>,      "resurlfrom":<String_value>,      "resurlinto":<String_value>,      "cookiedomainfrom":<String_value>,      "cookiedomaininto":<String_value>,      "continuematching":<String_value>,      "state":<String_value>,      "comment":<String_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/transformaction/name_value&lt;String&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "transformaction": [ {      "name":<String_value>,      "profilename":<String_value>,      "priority":<Double_value>,      "requrlfrom":<String_value>,      "requrlinto":<String_value>,      "resurlfrom":<String_value>,      "resurlinto":<String_value>,      "cookiedomainfrom":<String_value>,      "cookiedomaininto":<String_value>,      "continuematching":<String_value>,      "state":<String_value>,      "comment":<String_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/transformaction?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",transformaction: [ { "__count": "#no"} ] }


