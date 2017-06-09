#aaakcdaccount

Configuration for Kerberos constrained delegation account resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>kcdaccount</td><td>&lt;String></td><td>Read-write</td><td>The name of the KCD account.&lt;br>Minimum length = 1</td><tr><tr><td>keytab</td><td>&lt;String></td><td>Read-write</td><td>The path to the keytab file. If specified other parameters in this command need not be given.</td><tr><tr><td>realmstr</td><td>&lt;String></td><td>Read-write</td><td>Kerberos Realm.</td><tr><tr><td>delegateduser</td><td>&lt;String></td><td>Read-write</td><td>Username that can perform kerberos constrained delegation.</td><tr><tr><td>kcdpassword</td><td>&lt;String></td><td>Read-write</td><td>Password for Delegated User.</td><tr><tr><td>usercert</td><td>&lt;String></td><td>Read-write</td><td>SSL Cert (including private key) for Delegated User.</td><tr><tr><td>cacert</td><td>&lt;String></td><td>Read-write</td><td>CA Cert for UserCert or when doing PKINIT backchannel.</td><tr><tr><td>userrealm</td><td>&lt;String></td><td>Read-write</td><td>Realm of the user.</td><tr><tr><td>enterpriserealm</td><td>&lt;String></td><td>Read-write</td><td>Enterprise Realm of the user. This should be given only in certain KDC deployments where KDC expects Enterprise username instead of Principal Name.</td><tr><tr><td>servicespn</td><td>&lt;String></td><td>Read-write</td><td>Service SPN. When specified, this will be used to fetch kerberos tickets. If not specified, Netscaler will construct SPN using service fqdn.</td><tr><tr><td>principle</td><td>&lt;String></td><td>Read-only</td><td>SPN extracted from keytab file.</td><tr><tr><td>kcdspn</td><td>&lt;String></td><td>Read-only</td><td>Host SPN extracted from keytab file.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [DELETE](#delete) | [UPDATE](#update) | [UNSET](#unset) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/aaakcdaccount
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"aaakcdaccount":{      "kcdaccount":<String_value>,      "keytab":<String_value>,      "realmstr":<String_value>,      "delegateduser":<String_value>,      "kcdpassword":<String_value>,      "usercert":<String_value>,      "cacert":<String_value>,      "userrealm":<String_value>,      "enterpriserealm":<String_value>,      "servicespn":<String_value>}}```
Response:
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/aaakcdaccount/kcdaccount_value&lt;String&gt;
HTTP Method: DELETE
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/aaakcdaccount
HTTP Method: PUT
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"aaakcdaccount":{      "kcdaccount":<String_value>,      "keytab":<String_value>,      "realmstr":<String_value>,      "delegateduser":<String_value>,      "kcdpassword":<String_value>,      "usercert":<String_value>,      "cacert":<String_value>,      "userrealm":<String_value>,      "enterpriserealm":<String_value>,      "servicespn":<String_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/aaakcdaccount?action=unset
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"aaakcdaccount":{      "kcdaccount":<String_value>,      "keytab":true,      "usercert":true,      "cacert":true,      "userrealm":true,      "enterpriserealm":true,      "servicespn":true}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/aaakcdaccount
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/aaakcdaccount?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


filter
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/aaakcdaccount?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of aaakcdaccount resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/aaakcdaccount?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).


pagination
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/aaakcdaccount?pagesize=#no;pageno=#no
Use this query-parameter to get the aaakcdaccount resources in chunks.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "aaakcdaccount": [ {      "kcdaccount":<String_value>,      "keytab":<String_value>,      "principle":<String_value>,      "kcdspn":<String_value>,      "realmstr":<String_value>,      "delegateduser":<String_value>,      "kcdpassword":<String_value>,      "usercert":<String_value>,      "cacert":<String_value>,      "userrealm":<String_value>,      "enterpriserealm":<String_value>,      "servicespn":<String_value>}]}```



###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/aaakcdaccount/kcdaccount_value&lt;String&gt;
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/aaakcdaccount/kcdaccount_value&lt;String&gt;?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/aaakcdaccount/kcdaccount_value&lt;String&gt;?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "aaakcdaccount": [ {      "kcdaccount":<String_value>,      "keytab":<String_value>,      "principle":<String_value>,      "kcdspn":<String_value>,      "realmstr":<String_value>,      "delegateduser":<String_value>,      "kcdpassword":<String_value>,      "usercert":<String_value>,      "cacert":<String_value>,      "userrealm":<String_value>,      "enterpriserealm":<String_value>,      "servicespn":<String_value>}]}```



###count



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/aaakcdaccount?count=yes
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: 
{ "aaakcdaccount": [ { "__count": "#no"} ] }


