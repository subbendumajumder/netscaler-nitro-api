#tmsessionaction

Configuration for TM session action resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the session action. Must begin with an ASCII alphanumeric or underscore (_) character, and must contain only ASCII alphanumeric, underscore, hash (#), period (.), space, colon (:), at (@), equals (=), and hyphen (-) characters. Cannot be changed after a session action is created.&lt;br>&lt;br>The following requirement applies only to the NetScaler CLI:&lt;br>If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my action" or my action).&lt;br>Minimum length = 1</td><tr><tr><td>sesstimeout</td><td>&lt;Double></td><td>Read-write</td><td>Session timeout, in minutes. If there is no traffic during the timeout period, the user is disconnected and must reauthenticate to access intranet resources.&lt;br>Minimum value = 1</td><tr><tr><td>defaultauthorizationaction</td><td>&lt;String></td><td>Read-write</td><td>Allow or deny access to content for which there is no specific authorization policy.&lt;br>Possible values = ALLOW, DENY</td><tr><tr><td>sso</td><td>&lt;String></td><td>Read-write</td><td>Use single sign-on (SSO) to log users on to all web applications automatically after they authenticate, or pass users to the web application logon page to authenticate to each application individually.&lt;br>Default value: OFF&lt;br>Possible values = ON, OFF</td><tr><tr><td>ssocredential</td><td>&lt;String></td><td>Read-write</td><td>Use the primary or secondary authentication credentials for single sign-on (SSO).&lt;br>Possible values = PRIMARY, SECONDARY</td><tr><tr><td>ssodomain</td><td>&lt;String></td><td>Read-write</td><td>Domain to use for single sign-on (SSO).&lt;br>Minimum length = 1&lt;br>Maximum length = 32</td><tr><tr><td>httponlycookie</td><td>&lt;String></td><td>Read-write</td><td>Allow only an HTTP session cookie, in which case the cookie cannot be accessed by scripts.&lt;br>Possible values = YES, NO</td><tr><tr><td>kcdaccount</td><td>&lt;String></td><td>Read-write</td><td>Kerberos constrained delegation account name.&lt;br>Minimum length = 1&lt;br>Maximum length = 32</td><tr><tr><td>persistentcookie</td><td>&lt;String></td><td>Read-write</td><td>Enable or disable persistent SSO cookies for the traffic management (TM) session. A persistent cookie remains on the user device and is sent with each HTTP request. The cookie becomes stale if the session ends. This setting is overwritten if a traffic action sets persistent cookie to OFF. &lt;br>Note: If persistent cookie is enabled, make sure you set the persistent cookie validity.&lt;br>Possible values = ON, OFF</td><tr><tr><td>persistentcookievalidity</td><td>&lt;Double></td><td>Read-write</td><td>Integer specifying the number of minutes for which the persistent cookie remains valid. Can be set only if the persistent cookie setting is enabled.&lt;br>Minimum value = 1</td><tr><tr><td>homepage</td><td>&lt;String></td><td>Read-write</td><td>Web address of the home page that a user is displayed when authentication vserver is bookmarked and used to login.</td><tr><tr><td>builtin</td><td>&lt;String[]></td><td>Read-only</td><td>Indicates that a variable is a built-in (SYSTEM INTERNAL) type.&lt;br>Possible values = MODIFIABLE, DELETABLE, IMMUTABLE, PARTITION_ALL</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [DELETE](#delete) | [UPDATE](#update) | [UNSET](#unset) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/tmsessionaction
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"tmsessionaction":{      "name":<String_value>,      "sesstimeout":<Double_value>,      "defaultauthorizationaction":<String_value>,      "sso":<String_value>,      "ssocredential":<String_value>,      "ssodomain":<String_value>,      "httponlycookie":<String_value>,      "kcdaccount":<String_value>,      "persistentcookie":<String_value>,      "persistentcookievalidity":<Double_value>,      "homepage":<String_value>}}```
Response:
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/tmsessionaction/name_value&lt;String&gt;
HTTP Method: DELETE
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/tmsessionaction
HTTP Method: PUT
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"tmsessionaction":{      "name":<String_value>,      "sesstimeout":<Double_value>,      "defaultauthorizationaction":<String_value>,      "sso":<String_value>,      "ssocredential":<String_value>,      "ssodomain":<String_value>,      "kcdaccount":<String_value>,      "httponlycookie":<String_value>,      "persistentcookie":<String_value>,      "persistentcookievalidity":<Double_value>,      "homepage":<String_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/tmsessionaction?action=unset
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"tmsessionaction":{      "name":<String_value>,      "sesstimeout":true,      "defaultauthorizationaction":true,      "sso":true,      "ssocredential":true,      "ssodomain":true,      "kcdaccount":true,      "httponlycookie":true,      "persistentcookie":true,      "persistentcookievalidity":true,      "homepage":true}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/tmsessionaction
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/tmsessionaction?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


filter
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/tmsessionaction?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of tmsessionaction resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/tmsessionaction?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).


pagination
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/tmsessionaction?pagesize=#no;pageno=#no
Use this query-parameter to get the tmsessionaction resources in chunks.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "tmsessionaction": [ {      "name":<String_value>,      "sesstimeout":<Double_value>,      "defaultauthorizationaction":<String_value>,      "sso":<String_value>,      "ssocredential":<String_value>,      "ssodomain":<String_value>,      "kcdaccount":<String_value>,      "httponlycookie":<String_value>,      "persistentcookie":<String_value>,      "persistentcookievalidity":<Double_value>,      "homepage":<String_value>,      "builtin":<String[]_value>}]}```



###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/tmsessionaction/name_value&lt;String&gt;
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/tmsessionaction/name_value&lt;String&gt;?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/tmsessionaction/name_value&lt;String&gt;?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "tmsessionaction": [ {      "name":<String_value>,      "sesstimeout":<Double_value>,      "defaultauthorizationaction":<String_value>,      "sso":<String_value>,      "ssocredential":<String_value>,      "ssodomain":<String_value>,      "kcdaccount":<String_value>,      "httponlycookie":<String_value>,      "persistentcookie":<String_value>,      "persistentcookievalidity":<Double_value>,      "homepage":<String_value>,      "builtin":<String[]_value>}]}```



###count



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/tmsessionaction?count=yes
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: 
{ "tmsessionaction": [ { "__count": "#no"} ] }


