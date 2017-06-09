#authenticationloginschema

Configuration for 0 resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the new login schema. Must begin with an ASCII alphanumeric or underscore (_) character, and must contain only ASCII alphanumeric, underscore, hash (#), period (.), space, colon (:), at (@), equals (=), and hyphen (-) characters. Cannot be changed after an action is created. The following requirement applies only to the NetScaler CLI: If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my action" or my action).&lt;br>Minimum length = 1</td><tr><tr><td>authenticationschema</td><td>&lt;String></td><td>Read-write</td><td>Name of the file for reading authentication schema to be sent for Login Page UI. This file should contain xml definition of elements as per Citrix Forms Authentication Protocol to be able to render login form.&lt;br>Minimum length = 1</td><tr><tr><td>userexpression</td><td>&lt;String></td><td>Read-write</td><td>Expression for username extraction during login.&lt;br>Minimum length = 1</td><tr><tr><td>passwdexpression</td><td>&lt;String></td><td>Read-write</td><td>Expression for password extraction during login.&lt;br>Minimum length = 1</td><tr><tr><td>usercredentialindex</td><td>&lt;Double></td><td>Read-write</td><td>The index at which user entered username should be stored in session.&lt;br>Minimum value = 1&lt;br>Maximum value = 16</td><tr><tr><td>passwordcredentialindex</td><td>&lt;Double></td><td>Read-write</td><td>The index at which user entered password should be stored in session.&lt;br>Minimum value = 1&lt;br>Maximum value = 16</td><tr><tr><td>authenticationstrength</td><td>&lt;Double></td><td>Read-write</td><td>Weight of the current authentication.&lt;br>Minimum value = 0&lt;br>Maximum value = 65535</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
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
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>},"sessionid":"##sessionid","authenticationloginschema":{      "name":<String_value>,      "authenticationschema":<String_value>,      "userexpression":<String_value>,      "passwdexpression":<String_value>,      "usercredentialindex":<Double_value>,      "passwordcredentialindex":<Double_value>,      "authenticationstrength":<Double_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/authenticationloginschema/name_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/authenticationloginschema/name_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","authenticationloginschema":{      "name":<String_value>,      "authenticationschema":<String_value>,      "userexpression":<String_value>,      "passwdexpression":<String_value>,      "usercredentialindex":<Double_value>,      "passwordcredentialindex":<Double_value>,      "authenticationstrength":<Double_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","authenticationloginschema":{      "name":<String_value>,      "userexpression":true,      "passwdexpression":true,      "usercredentialindex":true,      "passwordcredentialindex":true,      "authenticationstrength":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/authenticationloginschema
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/authenticationloginschema?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of authenticationloginschema resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/authenticationloginschema?view=summary
Use this query-parameter to get the summary output of authenticationloginschema resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/authenticationloginschema?pagesize=#no;pageno=#no
Use this query-parameter to get the authenticationloginschema resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/authenticationloginschema?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "authenticationloginschema": [ {      "name":<String_value>,      "authenticationschema":<String_value>,      "userexpression":<String_value>,      "passwdexpression":<String_value>,      "usercredentialindex":<Double_value>,      "passwordcredentialindex":<Double_value>,      "authenticationstrength":<Double_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/authenticationloginschema/name_value&lt;String&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "authenticationloginschema": [ {      "name":<String_value>,      "authenticationschema":<String_value>,      "userexpression":<String_value>,      "passwdexpression":<String_value>,      "usercredentialindex":<Double_value>,      "passwordcredentialindex":<Double_value>,      "authenticationstrength":<Double_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/authenticationloginschema?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",authenticationloginschema: [ { "__count": "#no"} ] }


