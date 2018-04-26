#sslcrl

Configuration for Certificate Revocation List resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>crlname</td><td>&lt;String></td><td>Read-write</td><td>Name for the Certificate Revocation List (CRL). Must begin with an ASCII alphanumeric or underscore (_) character, and must contain only ASCII alphanumeric, underscore, hash (#), period (.), space, colon (:), at (@), equals (=), and hyphen (-) characters. Cannot be changed after the CRL is created.<br><br>The following requirement applies only to the NetScaler CLI:<br>If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my crl" or 'my crl').<br>Minimum length = 1</td></tr><tr><td>crlpath</td><td>&lt;String></td><td>Read-write</td><td>Path to the CRL file. /var/netscaler/ssl/ is the default path.<br>Minimum length = 1</td></tr><tr><td>inform</td><td>&lt;String></td><td>Read-write</td><td>Input format of the CRL file. The two formats supported on the appliance are:<br>PEM - Privacy Enhanced Mail.<br>DER - Distinguished Encoding Rule.<br>Default value: PEM<br>Possible values = DER, PEM</td></tr><tr><td>refresh</td><td>&lt;String></td><td>Read-write</td><td>Set CRL auto refresh.<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>cacert</td><td>&lt;String></td><td>Read-write</td><td>CA certificate that has issued the CRL. Required if CRL Auto Refresh is selected. Install the CA certificate on the appliance before adding the CRL.<br>Minimum length = 1</td></tr><tr><td>method</td><td>&lt;String></td><td>Read-write</td><td>Method for CRL refresh. If LDAP is selected, specify the method, CA certificate, base DN, port, and LDAP server name. If HTTP is selected, specify the CA certificate, method, URL, and port. Cannot be changed after a CRL is added.<br>Possible values = HTTP, LDAP</td></tr><tr><td>server</td><td>&lt;String></td><td>Read-write</td><td>IP address of the LDAP server from which to fetch the CRLs.<br>Minimum length = 1</td></tr><tr><td>url</td><td>&lt;String></td><td>Read-write</td><td>URL of the CRL distribution point.</td></tr><tr><td>port</td><td>&lt;Integer></td><td>Read-write</td><td>Port for the LDAP server.<br>Minimum value = 1</td></tr><tr><td>basedn</td><td>&lt;String></td><td>Read-write</td><td>Base distinguished name (DN), which is used in an LDAP search to search for a CRL. Citrix recommends searching for the Base DN instead of the Issuer Name from the CA certificate, because the Issuer Name field might not exactly match the LDAP directory structure's DN.<br>Minimum length = 1</td></tr><tr><td>scope</td><td>&lt;String></td><td>Read-write</td><td>Extent of the search operation on the LDAP server. Available settings function as follows:<br>One - One level below Base DN.<br>Base - Exactly the same level as Base DN.<br>Default value: One<br>Possible values = Base, One</td></tr><tr><td>interval</td><td>&lt;String></td><td>Read-write</td><td>CRL refresh interval. Use the NONE setting to unset this parameter.<br>Possible values = MONTHLY, WEEKLY, DAILY, NONE</td></tr><tr><td>day</td><td>&lt;Integer></td><td>Read-write</td><td>Day on which to refresh the CRL, or, if the Interval parameter is not set, the number of days after which to refresh the CRL. If Interval is set to MONTHLY, specify the date. If Interval is set to WEEKLY, specify the day of the week (for example, Sun=0 and Sat=6). This parameter is not applicable if the Interval is set to DAILY.<br>Minimum value = 0<br>Maximum value = 31</td></tr><tr><td>time</td><td>&lt;String></td><td>Read-write</td><td>Time, in hours (1-24) and minutes (1-60), at which to refresh the CRL.</td></tr><tr><td>binddn</td><td>&lt;String></td><td>Read-write</td><td>Bind distinguished name (DN) to be used to access the CRL object in the LDAP repository if access to the LDAP repository is restricted or anonymous access is not allowed.<br>Minimum length = 1</td></tr><tr><td>password</td><td>&lt;String></td><td>Read-write</td><td>Password to access the CRL in the LDAP repository if access to the LDAP repository is restricted or anonymous access is not allowed.<br>Minimum length = 1</td></tr><tr><td>binary</td><td>&lt;String></td><td>Read-write</td><td>Set the LDAP-based CRL retrieval mode to binary.<br>Default value: NO<br>Possible values = YES, NO</td></tr><tr><td>cacertfile</td><td>&lt;String></td><td>Read-write</td><td>Name of and, optionally, path to the CA certificate file.<br>/nsconfig/ssl/ is the default path.<br>Maximum length = 63</td></tr><tr><td>cakeyfile</td><td>&lt;String></td><td>Read-write</td><td>Name of and, optionally, path to the CA key file. /nsconfig/ssl/ is the default path.<br>Maximum length = 63</td></tr><tr><td>indexfile</td><td>&lt;String></td><td>Read-write</td><td>Name of and, optionally, path to the file containing the serial numbers of all the certificates that are revoked. Revoked certificates are appended to the file. /nsconfig/ssl/ is the default path.<br>Maximum length = 63</td></tr><tr><td>revoke</td><td>&lt;String></td><td>Read-write</td><td>Name of and, optionally, path to the certificate to be revoked. /nsconfig/ssl/ is the default path.<br>Maximum length = 63</td></tr><tr><td>gencrl</td><td>&lt;String></td><td>Read-write</td><td>Name of and, optionally, path to the CRL file to be generated. The list of certificates that have been revoked is obtained from the index file. /nsconfig/ssl/ is the default path.<br>Maximum length = 63</td></tr><tr><td>flags</td><td>&lt;Integer></td><td>Read-only</td><td>CRL status flag.</td></tr><tr><td>lastupdatetime</td><td>&lt;Integer></td><td>Read-only</td><td>Last CRL refresh time.</td></tr><tr><td>version</td><td>&lt;Integer></td><td>Read-only</td><td>CRL version.</td></tr><tr><td>signaturealgo</td><td>&lt;String></td><td>Read-only</td><td>Signature algorithm.</td></tr><tr><td>issuer</td><td>&lt;String></td><td>Read-only</td><td>Issuer name.</td></tr><tr><td>lastupdate</td><td>&lt;String></td><td>Read-only</td><td>Last update time.</td></tr><tr><td>nextupdate</td><td>&lt;String></td><td>Read-only</td><td>Next update time.</td></tr><tr><td>daystoexpiration</td><td>&lt;Integer></td><td>Read-only</td><td>Number of days remaining for the CRL to expire.</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD]()| [CREATE](#c)| [DELETE](#d)| [UPDATE](#u)| [UNSET](#)| [GET (ALL)](#get-)| [GET]()| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslcrl
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"sslcrl":{<b>"crlname":<String_value>,</b><b>"crlpath":<String_value>,</b>"inform":<String_value>,"refresh":<String_value>,"cacert":<String_value>,"method":<String_value>,"server":<String_value>,"url":<String_value>,"port":<Integer_value>,"basedn":<String_value>,"scope":<String_value>,"interval":<String_value>,"day":<Integer_value>,"time":<String_value>,"binddn":<String_value>,"password":<String_value>,"binary":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###create



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslcrl?<b>action=create</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"sslcrl":{<b>"cacertfile":<String_value>,</b><b>"cakeyfile":<String_value>,</b><b>"indexfile":<String_value>,</b>"revoke":<String_value>,"gencrl":<String_value>,"password":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslcrl/crlname_value&lt;String&gt;
<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslcrl
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"sslcrl":{<b>"crlname":<String_value>,</b>"refresh":<String_value>,"cacert":<String_value>,"server":<String_value>,"method":<String_value>,"url":<String_value>,"port":<Integer_value>,"basedn":<String_value>,"scope":<String_value>,"interval":<String_value>,"day":<Integer_value>,"time":<String_value>,"binddn":<String_value>,"password":<String_value>,"binary":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslcrl?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"sslcrl":{<b>"crlname":<String_value>,</b>"refresh":true,"cacert":true,"server":true,"method":true,"url":true,"port":true,"basedn":true,"scope":true,"interval":true,"day":true,"time":true,"binddn":true,"password":true,"binary":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslcrl
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslcrl?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslcrl?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of sslcrl resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslcrl?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslcrl?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the sslcrl resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "sslcrl": [ {"crlname":<String_value>,"crlpath":<String_value>,"inform":<String_value>,"cacert":<String_value>,"refresh":<String_value>,"scope":<String_value>,"server":<String_value>,"port":<Integer_value>,"url":<String_value>,"method":<String_value>,"basedn":<String_value>,"interval":<String_value>,"day":<Integer_value>,"time":<String_value>,"binddn":<String_value>,"password":<String_value>,"flags":<Integer_value>,"lastupdatetime":<Integer_value>,"version":<Integer_value>,"signaturealgo":<String_value>,"issuer":<String_value>,"lastupdate":<String_value>,"nextupdate":<String_value>,"binary":<String_value>,"daystoexpiration":<Integer_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslcrl/crlname_value&lt;String&gt;
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslcrl/crlname_value&lt;String&gt;?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslcrl/crlname_value&lt;String&gt;?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "sslcrl": [ {"crlname":<String_value>,"crlpath":<String_value>,"inform":<String_value>,"cacert":<String_value>,"refresh":<String_value>,"scope":<String_value>,"server":<String_value>,"port":<Integer_value>,"url":<String_value>,"method":<String_value>,"basedn":<String_value>,"interval":<String_value>,"day":<Integer_value>,"time":<String_value>,"binddn":<String_value>,"password":<String_value>,"flags":<Integer_value>,"lastupdatetime":<Integer_value>,"version":<Integer_value>,"signaturealgo":<String_value>,"issuer":<String_value>,"lastupdate":<String_value>,"nextupdate":<String_value>,"binary":<String_value>,"daystoexpiration":<Integer_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslcrl?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "sslcrl": [ { "__count": "#no"} ] }```



