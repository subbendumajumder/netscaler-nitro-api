#systemuser

Configuration for system user resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>username</td><td>&lt;String></td><td>Read-write</td><td>Name for a user. Must begin with a letter, number, or the underscore (_) character, and must contain only alphanumeric, hyphen (-), period (.), hash (#), space ( ), at (@), equal (=), colon (:), and underscore characters. Cannot be changed after the user is added.&lt;br>&lt;br>CLI Users: If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my user" or my user).&lt;br>Minimum length = 1</td><tr><tr><td>password</td><td>&lt;String></td><td>Read-write</td><td>Password for the system user. Can include any ASCII character.&lt;br>Minimum length = 1</td><tr><tr><td>externalauth</td><td>&lt;String></td><td>Read-write</td><td>Whether to use external authentication servers for the system user authentication or not.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>promptstring</td><td>&lt;String></td><td>Read-write</td><td>String to display at the command-line prompt. Can consist of letters, numbers, hyphen (-), period (.), hash (#), space ( ), at (@), equal (=), colon (:), underscore (_), and the following variables: &lt;br>* %u - Will be replaced by the user name.&lt;br>* %h - Will be replaced by the hostname of the NetScaler appliance.&lt;br>* %t - Will be replaced by the current time in 12-hour format.&lt;br>* %T - Will be replaced by the current time in 24-hour format.&lt;br>* %d - Will be replaced by the current date.&lt;br>* %s - Will be replaced by the state of the NetScaler appliance.&lt;br>&lt;br>Note: The 63-character limit for the length of the string does not apply to the characters that replace the variables.&lt;br>Minimum length = 1</td><tr><tr><td>timeout</td><td>&lt;Double></td><td>Read-write</td><td>CLI session inactivity timeout, in seconds. If Restrictedtimeout argument of system parameter is enabled, Timeout can have values in the range [300-86400] seconds. If Restrictedtimeout argument of system parameter is disabled, Timeout can have values in the range [0, 10-100000000] seconds. Default value is 900 seconds.</td><tr><tr><td>logging</td><td>&lt;String></td><td>Read-write</td><td>Users logging privilege.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>maxsession</td><td>&lt;Double></td><td>Read-write</td><td>Maximum number of client connection allowed per user.&lt;br>Default value: 20&lt;br>Minimum value = 1&lt;br>Maximum value = 40</td><tr><tr><td>encrypted</td><td>&lt;Boolean></td><td>Read-only</td><td>.</td><tr><tr><td>promptinheritedfrom</td><td>&lt;String></td><td>Read-only</td><td>From where the prompt has been inherited.&lt;br>Possible values = User, Group, Global, Climode</td><tr><tr><td>timeoutkind</td><td>&lt;String></td><td>Read-only</td><td>From where the timeout has been inherited.&lt;br>Possible values = User, Group, Global, Climode</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [DELETE](#delete) | [UPDATE](#update) | [UNSET](#unset) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/systemuser
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"systemuser":{      "username":<String_value>,      "password":<String_value>,      "externalauth":<String_value>,      "promptstring":<String_value>,      "timeout":<Double_value>,      "logging":<String_value>,      "maxsession":<Double_value>}}```
Response:
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/systemuser/username_value&lt;String&gt;
HTTP Method: DELETE
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/systemuser
HTTP Method: PUT
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"systemuser":{      "username":<String_value>,      "password":<String_value>,      "externalauth":<String_value>,      "promptstring":<String_value>,      "timeout":<Double_value>,      "logging":<String_value>,      "maxsession":<Double_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/systemuser?action=unset
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"systemuser":{      "username":<String_value>,      "externalauth":true,      "promptstring":true,      "timeout":true,      "logging":true,      "maxsession":true}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/systemuser
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/systemuser?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


filter
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/systemuser?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of systemuser resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/systemuser?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).


pagination
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/systemuser?pagesize=#no;pageno=#no
Use this query-parameter to get the systemuser resources in chunks.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "systemuser": [ {      "username":<String_value>,      "password":<String_value>,      "encrypted":<Boolean_value>,      "externalauth":<String_value>,      "promptstring":<String_value>,      "promptinheritedfrom":<String_value>,      "timeout":<Double_value>,      "timeoutkind":<String_value>,      "logging":<String_value>,      "maxsession":<Double_value>}]}```



###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/systemuser/username_value&lt;String&gt;
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/systemuser/username_value&lt;String&gt;?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/systemuser/username_value&lt;String&gt;?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "systemuser": [ {      "username":<String_value>,      "password":<String_value>,      "encrypted":<Boolean_value>,      "externalauth":<String_value>,      "promptstring":<String_value>,      "promptinheritedfrom":<String_value>,      "timeout":<Double_value>,      "timeoutkind":<String_value>,      "logging":<String_value>,      "maxsession":<Double_value>}]}```



###count



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/systemuser?count=yes
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: 
{ "systemuser": [ { "__count": "#no"} ] }


