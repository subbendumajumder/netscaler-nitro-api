#tmformssoaction

Configuration for Form sso action resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the new form-based single sign-on profile. Must begin with an ASCII alphanumeric or underscore (_) character, and must contain only ASCII alphanumeric, underscore, hash (#), period (.), space, colon (:), at (@), equals (=), and hyphen (-) characters. Cannot be changed after an SSO action is created.&lt;br>&lt;br>The following requirement applies only to the NetScaler CLI:&lt;br>If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my action" or my action).&lt;br>Minimum length = 1</td><tr><tr><td>actionurl</td><td>&lt;String></td><td>Read-write</td><td>URL to which the completed form is submitted.&lt;br>Minimum length = 1</td><tr><tr><td>userfield</td><td>&lt;String></td><td>Read-write</td><td>Name of the form field in which the user types in the user ID.&lt;br>Minimum length = 1</td><tr><tr><td>passwdfield</td><td>&lt;String></td><td>Read-write</td><td>Name of the form field in which the user types in the password.&lt;br>Minimum length = 1</td><tr><tr><td>ssosuccessrule</td><td>&lt;String></td><td>Read-write</td><td>Expression, that checks to see if single sign-on is successful.</td><tr><tr><td>namevaluepair</td><td>&lt;String></td><td>Read-write</td><td>Name-value pair attributes to send to the server in addition to sending the username and password. Value names are separated by an ampersand (;amp;) (for example, name1=value1;amp;name2=value2).</td><tr><tr><td>responsesize</td><td>&lt;Double></td><td>Read-write</td><td>Number of bytes, in the response, to parse for extracting the forms.&lt;br>Default value: 8096</td><tr><tr><td>nvtype</td><td>&lt;String></td><td>Read-write</td><td>Type of processing of the name-value pair. If you specify STATIC, the values configured by the administrator are used. For DYNAMIC, the response is parsed, and the form is extracted and then submitted.&lt;br>Default value: DYNAMIC&lt;br>Possible values = STATIC, DYNAMIC</td><tr><tr><td>submitmethod</td><td>&lt;String></td><td>Read-write</td><td>HTTP method used by the single sign-on form to send the logon credentials to the logon server. Applies only to STATIC name-value type.&lt;br>Default value: GET&lt;br>Possible values = GET, POST</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [DELETE](#delete) | [UPDATE](#update) | [UNSET](#unset) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/tmformssoaction
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"tmformssoaction":{      "name":<String_value>,      "actionurl":<String_value>,      "userfield":<String_value>,      "passwdfield":<String_value>,      "ssosuccessrule":<String_value>,      "namevaluepair":<String_value>,      "responsesize":<Double_value>,      "nvtype":<String_value>,      "submitmethod":<String_value>}}```
Response:
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/tmformssoaction/name_value&lt;String&gt;
HTTP Method: DELETE
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/tmformssoaction
HTTP Method: PUT
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"tmformssoaction":{      "name":<String_value>,      "actionurl":<String_value>,      "userfield":<String_value>,      "passwdfield":<String_value>,      "ssosuccessrule":<String_value>,      "responsesize":<Double_value>,      "namevaluepair":<String_value>,      "nvtype":<String_value>,      "submitmethod":<String_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/tmformssoaction?action=unset
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"tmformssoaction":{      "name":<String_value>,      "responsesize":true,      "namevaluepair":true,      "nvtype":true,      "submitmethod":true}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/tmformssoaction
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/tmformssoaction?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


filter
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/tmformssoaction?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of tmformssoaction resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/tmformssoaction?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).


pagination
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/tmformssoaction?pagesize=#no;pageno=#no
Use this query-parameter to get the tmformssoaction resources in chunks.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "tmformssoaction": [ {      "name":<String_value>,      "actionurl":<String_value>,      "userfield":<String_value>,      "passwdfield":<String_value>,      "responsesize":<Double_value>,      "namevaluepair":<String_value>,      "nvtype":<String_value>,      "ssosuccessrule":<String_value>,      "submitmethod":<String_value>}]}```



###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/tmformssoaction/name_value&lt;String&gt;
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/tmformssoaction/name_value&lt;String&gt;?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/tmformssoaction/name_value&lt;String&gt;?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "tmformssoaction": [ {      "name":<String_value>,      "actionurl":<String_value>,      "userfield":<String_value>,      "passwdfield":<String_value>,      "responsesize":<Double_value>,      "namevaluepair":<String_value>,      "nvtype":<String_value>,      "ssosuccessrule":<String_value>,      "submitmethod":<String_value>}]}```



###count



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/tmformssoaction?count=yes
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: 
{ "tmformssoaction": [ { "__count": "#no"} ] }


