#tmtrafficaction

Configuration for TM traffic action resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the traffic action. Must begin with an ASCII alphanumeric or underscore (_) character, and must contain only ASCII alphanumeric, underscore, hash (#), period (.), space, colon (:), at (@), equals (=), and hyphen (-) characters. Cannot be changed after a traffic action is created.&lt;br>&lt;br>The following requirement applies only to the NetScaler CLI:&lt;br>If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my action" or my action).&lt;br>Minimum length = 1</td><tr><tr><td>apptimeout</td><td>&lt;Double></td><td>Read-write</td><td>Time interval, in minutes, of user inactivity after which the connection is closed.&lt;br>Minimum value = 1&lt;br>Maximum value = 715827</td><tr><tr><td>sso</td><td>&lt;String></td><td>Read-write</td><td>Use single sign-on for the resource that the user is accessing now.&lt;br>Possible values = ON, OFF</td><tr><tr><td>formssoaction</td><td>&lt;String></td><td>Read-write</td><td>Name of the configured form-based single sign-on profile.</td><tr><tr><td>persistentcookie</td><td>&lt;String></td><td>Read-write</td><td>Use persistent cookies for the traffic session. A persistent cookie remains on the user device and is sent with each HTTP request. The cookie becomes stale if the session ends.&lt;br>Possible values = ON, OFF</td><tr><tr><td>initiatelogout</td><td>&lt;String></td><td>Read-write</td><td>Initiate logout for the traffic management (TM) session if the policy evaluates to true. The session is then terminated after two minutes.&lt;br>Possible values = ON, OFF</td><tr><tr><td>kcdaccount</td><td>&lt;String></td><td>Read-write</td><td>Kerberos constrained delegation account name.&lt;br>Default value: "None"&lt;br>Minimum length = 1&lt;br>Maximum length = 32</td><tr><tr><td>samlssoprofile</td><td>&lt;String></td><td>Read-write</td><td>Profile to be used for doing SAML SSO to remote relying party.&lt;br>Minimum length = 1</td><tr><tr><td>forcedtimeout</td><td>&lt;String></td><td>Read-write</td><td>Setting to start, stop or reset TM session force timer.&lt;br>Possible values = START, STOP, RESET</td><tr><tr><td>forcedtimeoutval</td><td>&lt;Double></td><td>Read-write</td><td>Time interval, in minutes, for which force timer should be set.</td><tr><tr><td>userexpression</td><td>&lt;String></td><td>Read-write</td><td>expression that will be evaluated to obtain username for SingleSignOn.&lt;br>Maximum length = 256</td><tr><tr><td>passwdexpression</td><td>&lt;String></td><td>Read-write</td><td>expression that will be evaluated to obtain password for SingleSignOn.&lt;br>Maximum length = 256</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [DELETE](#delete) | [UPDATE](#update) | [UNSET](#unset) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/tmtrafficaction
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"tmtrafficaction":{      "name":<String_value>,      "apptimeout":<Double_value>,      "sso":<String_value>,      "formssoaction":<String_value>,      "persistentcookie":<String_value>,      "initiatelogout":<String_value>,      "kcdaccount":<String_value>,      "samlssoprofile":<String_value>,      "forcedtimeout":<String_value>,      "forcedtimeoutval":<Double_value>,      "userexpression":<String_value>,      "passwdexpression":<String_value>}}```
Response:
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/tmtrafficaction/name_value&lt;String&gt;
HTTP Method: DELETE
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/tmtrafficaction
HTTP Method: PUT
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"tmtrafficaction":{      "name":<String_value>,      "apptimeout":<Double_value>,      "sso":<String_value>,      "formssoaction":<String_value>,      "persistentcookie":<String_value>,      "initiatelogout":<String_value>,      "kcdaccount":<String_value>,      "samlssoprofile":<String_value>,      "forcedtimeout":<String_value>,      "forcedtimeoutval":<Double_value>,      "userexpression":<String_value>,      "passwdexpression":<String_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/tmtrafficaction?action=unset
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"tmtrafficaction":{      "name":<String_value>,      "persistentcookie":true,      "kcdaccount":true,      "forcedtimeout":true,      "userexpression":true,      "passwdexpression":true}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/tmtrafficaction
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/tmtrafficaction?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


filter
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/tmtrafficaction?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of tmtrafficaction resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/tmtrafficaction?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).


pagination
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/tmtrafficaction?pagesize=#no;pageno=#no
Use this query-parameter to get the tmtrafficaction resources in chunks.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "tmtrafficaction": [ {      "name":<String_value>,      "apptimeout":<Double_value>,      "sso":<String_value>,      "formssoaction":<String_value>,      "persistentcookie":<String_value>,      "initiatelogout":<String_value>,      "kcdaccount":<String_value>,      "samlssoprofile":<String_value>,      "forcedtimeout":<String_value>,      "forcedtimeoutval":<Double_value>,      "userexpression":<String_value>,      "passwdexpression":<String_value>}]}```



###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/tmtrafficaction/name_value&lt;String&gt;
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/tmtrafficaction/name_value&lt;String&gt;?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/tmtrafficaction/name_value&lt;String&gt;?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "tmtrafficaction": [ {      "name":<String_value>,      "apptimeout":<Double_value>,      "sso":<String_value>,      "formssoaction":<String_value>,      "persistentcookie":<String_value>,      "initiatelogout":<String_value>,      "kcdaccount":<String_value>,      "samlssoprofile":<String_value>,      "forcedtimeout":<String_value>,      "forcedtimeoutval":<Double_value>,      "userexpression":<String_value>,      "passwdexpression":<String_value>}]}```



###count



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/tmtrafficaction?count=yes
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: 
{ "tmtrafficaction": [ { "__count": "#no"} ] }


