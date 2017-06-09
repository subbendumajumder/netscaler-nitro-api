#authenticationnegotiateaction

Configuration for Negotiate action resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the AD KDC server profile (negotiate action). &lt;br>Must begin with a letter, number, or the underscore character (_), and must contain only letters, numbers, and the hyphen (-), period (.) pound (#), space ( ), at (@), equals (=), colon (:), and underscore characters. Cannot be changed after AD KDC server profile is created.&lt;br>&lt;br>The following requirement applies only to the NetScaler CLI:&lt;br>If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my authentication action" or my authentication action).&lt;br>Minimum length = 1</td><tr><tr><td>domain</td><td>&lt;String></td><td>Read-write</td><td>Domain name of the service principal that represnts Netscaler.&lt;br>Minimum length = 1</td><tr><tr><td>domainuser</td><td>&lt;String></td><td>Read-write</td><td>User name of the account that is mapped with Netscaler principal. This can be given along with domain and password when keytab file is not available. If username is given along with keytab file, then that keytab file will be searched for this users credentials.&lt;br>Minimum length = 1</td><tr><tr><td>domainuserpasswd</td><td>&lt;String></td><td>Read-write</td><td>Password of the account that is mapped to the NetScaler principal.&lt;br>Minimum length = 1</td><tr><tr><td>ou</td><td>&lt;String></td><td>Read-write</td><td>Active Directory organizational units (OU) attribute.&lt;br>Minimum length = 1</td><tr><tr><td>defaultauthenticationgroup</td><td>&lt;String></td><td>Read-write</td><td>This is the default group that is chosen when the authentication succeeds in addition to extracted groups.</td><tr><tr><td>keytab</td><td>&lt;String></td><td>Read-write</td><td>The path to the keytab file that is used to decrypt kerberos tickets presented to Netscaler. If keytab is not available, domain/username/password can be specified in the negotiate action configuration.&lt;br>Minimum length = 1</td><tr><tr><td>ntlmpath</td><td>&lt;String></td><td>Read-write</td><td>The path to the site that is enabled for NTLM authentication, including FQDN of the server. This is used when clients fallback to NTLM.&lt;br>Minimum length = 1</td><tr><tr><td>kcdspn</td><td>&lt;String></td><td>Read-only</td><td>Host SPN extracted from keytab file.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [DELETE](#delete) | [UPDATE](#update) | [UNSET](#unset) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationnegotiateaction
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"authenticationnegotiateaction":{      "name":<String_value>,      "domain":<String_value>,      "domainuser":<String_value>,      "domainuserpasswd":<String_value>,      "ou":<String_value>,      "defaultauthenticationgroup":<String_value>,      "keytab":<String_value>,      "ntlmpath":<String_value>}}```
Response:
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationnegotiateaction/name_value&lt;String&gt;
HTTP Method: DELETE
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationnegotiateaction
HTTP Method: PUT
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"authenticationnegotiateaction":{      "name":<String_value>,      "domain":<String_value>,      "domainuser":<String_value>,      "domainuserpasswd":<String_value>,      "ou":<String_value>,      "defaultauthenticationgroup":<String_value>,      "keytab":<String_value>,      "ntlmpath":<String_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationnegotiateaction?action=unset
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"authenticationnegotiateaction":{      "name":<String_value>,      "domain":true,      "domainuser":true,      "domainuserpasswd":true,      "ou":true,      "defaultauthenticationgroup":true,      "ntlmpath":true}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationnegotiateaction
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationnegotiateaction?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


filter
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationnegotiateaction?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of authenticationnegotiateaction resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationnegotiateaction?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).


pagination
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationnegotiateaction?pagesize=#no;pageno=#no
Use this query-parameter to get the authenticationnegotiateaction resources in chunks.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "authenticationnegotiateaction": [ {      "name":<String_value>,      "domain":<String_value>,      "domainuser":<String_value>,      "domainuserpasswd":<String_value>,      "ou":<String_value>,      "defaultauthenticationgroup":<String_value>,      "keytab":<String_value>,      "kcdspn":<String_value>,      "ntlmpath":<String_value>}]}```



###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationnegotiateaction/name_value&lt;String&gt;
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationnegotiateaction/name_value&lt;String&gt;?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationnegotiateaction/name_value&lt;String&gt;?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "authenticationnegotiateaction": [ {      "name":<String_value>,      "domain":<String_value>,      "domainuser":<String_value>,      "domainuserpasswd":<String_value>,      "ou":<String_value>,      "defaultauthenticationgroup":<String_value>,      "keytab":<String_value>,      "kcdspn":<String_value>,      "ntlmpath":<String_value>}]}```



###count



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationnegotiateaction?count=yes
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: 
{ "authenticationnegotiateaction": [ { "__count": "#no"} ] }


