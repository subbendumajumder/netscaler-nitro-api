#tmsessionparameter

Configuration for session parameter resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>sesstimeout</td><td>&lt;Double></td><td>Read-write</td><td>Session timeout, in minutes. If there is no traffic during the timeout period, the user is disconnected and must reauthenticate to access the intranet resources.&lt;br>Default value: 30&lt;br>Minimum value = 1</td><tr><tr><td>defaultauthorizationaction</td><td>&lt;String></td><td>Read-write</td><td>Allow or deny access to content for which there is no specific authorization policy.&lt;br>Default value: ALLOW&lt;br>Possible values = ALLOW, DENY</td><tr><tr><td>sso</td><td>&lt;String></td><td>Read-write</td><td>Log users on to all web applications automatically after they authenticate, or pass users to the web application logon page to authenticate for each application.&lt;br>Default value: OFF&lt;br>Possible values = ON, OFF</td><tr><tr><td>ssocredential</td><td>&lt;String></td><td>Read-write</td><td>Use primary or secondary authentication credentials for single sign-on.&lt;br>Default value: PRIMARY&lt;br>Possible values = PRIMARY, SECONDARY</td><tr><tr><td>ssodomain</td><td>&lt;String></td><td>Read-write</td><td>Domain to use for single sign-on.&lt;br>Minimum length = 1&lt;br>Maximum length = 32</td><tr><tr><td>kcdaccount</td><td>&lt;String></td><td>Read-write</td><td>Kerberos constrained delegation account name.&lt;br>Minimum length = 1&lt;br>Maximum length = 32</td><tr><tr><td>httponlycookie</td><td>&lt;String></td><td>Read-write</td><td>Allow only an HTTP session cookie, in which case the cookie cannot be accessed by scripts.&lt;br>Default value: YES&lt;br>Possible values = YES, NO</td><tr><tr><td>persistentcookie</td><td>&lt;String></td><td>Read-write</td><td>Use persistent SSO cookies for the traffic session. A persistent cookie remains on the user device and is sent with each HTTP request. The cookie becomes stale if the session ends.&lt;br>Default value: OFF&lt;br>Possible values = ON, OFF</td><tr><tr><td>persistentcookievalidity</td><td>&lt;Double></td><td>Read-write</td><td>Integer specifying the number of minutes for which the persistent cookie remains valid. Can be set only if the persistence cookie setting is enabled.&lt;br>Minimum value = 1</td><tr><tr><td>homepage</td><td>&lt;String></td><td>Read-write</td><td>Web address of the home page that a user is displayed when authentication vserver is bookmarked and used to login.&lt;br>Default value: "None"</td><tr><tr><td>name</td><td>&lt;String></td><td>Read-only</td><td>.</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[UPDATE](#update) | [UNSET](#unset) | [GET (ALL)](#get-(all))


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###update



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/tmsessionparameter
HTTP Method: PUT
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"tmsessionparameter":{      "sesstimeout":<Double_value>,      "defaultauthorizationaction":<String_value>,      "sso":<String_value>,      "ssocredential":<String_value>,      "ssodomain":<String_value>,      "kcdaccount":<String_value>,      "httponlycookie":<String_value>,      "persistentcookie":<String_value>,      "persistentcookievalidity":<Double_value>,      "homepage":<String_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/tmsessionparameter?action=unset
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"tmsessionparameter":{      "sesstimeout":true,      "sso":true,      "ssodomain":true,      "kcdaccount":true,      "persistentcookie":true,      "homepage":true,      "defaultauthorizationaction":true,      "ssocredential":true,      "httponlycookie":true,      "persistentcookievalidity":true}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/tmsessionparameter
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "tmsessionparameter": [ {      "name":<String_value>,      "sesstimeout":<Double_value>,      "defaultauthorizationaction":<String_value>,      "sso":<String_value>,      "ssocredential":<String_value>,      "ssodomain":<String_value>,      "kcdaccount":<String_value>,      "httponlycookie":<String_value>,      "homepage":<String_value>,      "persistentcookie":<String_value>,      "persistentcookievalidity":<Double_value>}]}```



