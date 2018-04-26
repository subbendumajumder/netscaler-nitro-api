#sslcertkey

Configuration for certificate key resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>certkey</td><td>&lt;String></td><td>Read-write</td><td>Name for the certificate and private-key pair. Must begin with an ASCII alphanumeric or underscore (_) character, and must contain only ASCII alphanumeric, underscore, hash (#), period (.), space, colon (:), at (@), equals (=), and hyphen (-) characters. Cannot be changed after the certificate-key pair is created.<br><br>The following requirement applies only to the NetScaler CLI:<br>If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my cert" or 'my cert').<br>Minimum length = 1</td></tr><tr><td>cert</td><td>&lt;String></td><td>Read-write</td><td>Name of and, optionally, path to the X509 certificate file that is used to form the certificate-key pair. The certificate file should be present on the appliance's hard-disk drive or solid-state drive. Storing a certificate in any location other than the default might cause inconsistency in a high availability setup. /nsconfig/ssl/ is the default path.<br>Minimum length = 1</td></tr><tr><td>key</td><td>&lt;String></td><td>Read-write</td><td>Name of and, optionally, path to the private-key file that is used to form the certificate-key pair. The certificate file should be present on the appliance's hard-disk drive or solid-state drive. Storing a certificate in any location other than the default might cause inconsistency in a high availability setup. /nsconfig/ssl/ is the default path.<br>Minimum length = 1</td></tr><tr><td>password</td><td>&lt;Boolean></td><td>Read-write</td><td>Passphrase that was used to encrypt the private-key. Use this option to load encrypted private-keys in PEM format.</td></tr><tr><td>fipskey</td><td>&lt;String></td><td>Read-write</td><td>Name of the FIPS key that was created inside the Hardware Security Module (HSM) of a FIPS appliance, or a key that was imported into the HSM.<br>Minimum length = 1</td></tr><tr><td>hsmkey</td><td>&lt;String></td><td>Read-write</td><td>Name of the HSM key that was created in the External Hardware Security Module (HSM) of a FIPS appliance.<br>Minimum length = 1</td></tr><tr><td>inform</td><td>&lt;String></td><td>Read-write</td><td>Input format of the certificate and the private-key files. The three formats supported by the appliance are:<br>PEM - Privacy Enhanced Mail<br>DER - Distinguished Encoding Rule<br>PFX - Personal Information Exchange.<br>Default value: PEM<br>Possible values = DER, PEM, PFX</td></tr><tr><td>passplain</td><td>&lt;String></td><td>Read-write</td><td>Pass phrase used to encrypt the private-key. Required when adding an encrypted private-key in PEM format.<br>Minimum length = 1</td></tr><tr><td>expirymonitor</td><td>&lt;String></td><td>Read-write</td><td>Issue an alert when the certificate is about to expire.<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>notificationperiod</td><td>&lt;Double></td><td>Read-write</td><td>Time, in number of days, before certificate expiration, at which to generate an alert that the certificate is about to expire.<br>Minimum value = 10<br>Maximum value = 100</td></tr><tr><td>bundle</td><td>&lt;String></td><td>Read-write</td><td>Parse the certificate chain as a single file after linking the server certificate to its issuer's certificate within the file.<br>Default value: NO<br>Possible values = YES, NO</td></tr><tr><td>linkcertkeyname</td><td>&lt;String></td><td>Read-write</td><td>Name of the Certificate Authority certificate-key pair to which to link a certificate-key pair.<br>Minimum length = 1</td></tr><tr><td>nodomaincheck</td><td>&lt;Boolean></td><td>Read-write</td><td>Override the check for matching domain names during a certificate update operation.</td></tr><tr><td>signaturealg</td><td>&lt;String></td><td>Read-only</td><td>Signature algorithm.</td></tr><tr><td>certificatetype</td><td>&lt;String[]></td><td>Read-only</td><td>Specifies whether the certificate is of type root-CA, intermediate-CA, server, client, or client and server.<br>Possible values = ROOT_CERT, INTM_CERT, CLNT_CERT, SRVR_CERT, UNKNOWN_CERT</td></tr><tr><td>serial</td><td>&lt;String></td><td>Read-only</td><td>Serial number.</td></tr><tr><td>issuer</td><td>&lt;String></td><td>Read-only</td><td>Issuer name.</td></tr><tr><td>clientcertnotbefore</td><td>&lt;String></td><td>Read-only</td><td>Not-Before date.</td></tr><tr><td>clientcertnotafter</td><td>&lt;String></td><td>Read-only</td><td>Not-After date.</td></tr><tr><td>daystoexpiration</td><td>&lt;Integer></td><td>Read-only</td><td>Days remaining for the certificate to expire.</td></tr><tr><td>subject</td><td>&lt;String></td><td>Read-only</td><td>Subject name.</td></tr><tr><td>publickey</td><td>&lt;String></td><td>Read-only</td><td>Public key algorithm.</td></tr><tr><td>publickeysize</td><td>&lt;Integer></td><td>Read-only</td><td>Size of the public key.</td></tr><tr><td>version</td><td>&lt;Integer></td><td>Read-only</td><td>Version.</td></tr><tr><td>priority</td><td>&lt;Double></td><td>Read-only</td><td>ocsp priority.</td></tr><tr><td>status</td><td>&lt;String></td><td>Read-only</td><td>Status of the certificate.<br>Possible values = Valid, Not yet valid, Expired</td></tr><tr><td>passcrypt</td><td>&lt;String></td><td>Read-only</td><td>Passcrypt.<br>Minimum length = 1</td></tr><tr><td>data</td><td>&lt;Double></td><td>Read-only</td><td>Vserver Id.</td></tr><tr><td>servicename</td><td>&lt;String></td><td>Read-only</td><td>Service name to which the certificate key pair is bound.</td></tr><tr><td>ocspresponsestatus</td><td>&lt;String></td><td>Read-only</td><td>Ocsp response status of the certificate.<br>Possible values = NONE, EXPIRED, VALID</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD]()| [DELETE](#d)| [UPDATE](#u)| [UNSET](#)| [LINK]()| [UNLINK](#u)| [CHANGE](#c)| [GET (ALL)](#get-)| [GET]()| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslcertkey
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"sslcertkey":{<b>"certkey":<String_value>,</b><b>"cert":<String_value>,</b>"key":<String_value>,"password":<Boolean_value>,"fipskey":<String_value>,"hsmkey":<String_value>,"inform":<String_value>,"passplain":<String_value>,"expirymonitor":<String_value>,"notificationperiod":<Double_value>,"bundle":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslcertkey/certkey_value&lt;String&gt;
<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslcertkey
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"sslcertkey":{<b>"certkey":<String_value>,</b>"expirymonitor":<String_value>,"notificationperiod":<Double_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslcertkey?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"sslcertkey":{<b>"certkey":<String_value>,</b>"expirymonitor":true,"notificationperiod":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###link



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslcertkey?<b>action=link</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"sslcertkey":{<b>"certkey":<String_value>,</b><b>"linkcertkeyname":<String_value></b>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unlink



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslcertkey?<b>action=unlink</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"sslcertkey":{<b>"certkey":<String_value></b>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###change



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslcertkey?<b>action=update</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"sslcertkey":{<b>"certkey":<String_value>,</b>"cert":<String_value>,"key":<String_value>,"password":<Boolean_value>,"fipskey":<String_value>,"inform":<String_value>,"passplain":<String_value>,"nodomaincheck":<Boolean_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslcertkey
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslcertkey?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslcertkey?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of sslcertkey resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslcertkey?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslcertkey?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the sslcertkey resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "sslcertkey": [ {"certkey":<String_value>,"cert":<String_value>,"key":<String_value>,"inform":<String_value>,"signaturealg":<String_value>,"certificatetype":<String[]_value>,"serial":<String_value>,"issuer":<String_value>,"clientcertnotbefore":<String_value>,"clientcertnotafter":<String_value>,"daystoexpiration":<Integer_value>,"subject":<String_value>,"publickey":<String_value>,"publickeysize":<Integer_value>,"version":<Integer_value>,"priority":<Double_value>,"status":<String_value>,"fipskey":<String_value>,"hsmkey":<String_value>,"passcrypt":<String_value>,"data":<Double_value>,"servicename":<String_value>,"expirymonitor":<String_value>,"notificationperiod":<Double_value>,"linkcertkeyname":<String_value>,"ocspresponsestatus":<String_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslcertkey/certkey_value&lt;String&gt;
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslcertkey/certkey_value&lt;String&gt;?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslcertkey/certkey_value&lt;String&gt;?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "sslcertkey": [ {"certkey":<String_value>,"cert":<String_value>,"key":<String_value>,"inform":<String_value>,"signaturealg":<String_value>,"certificatetype":<String[]_value>,"serial":<String_value>,"issuer":<String_value>,"clientcertnotbefore":<String_value>,"clientcertnotafter":<String_value>,"daystoexpiration":<Integer_value>,"subject":<String_value>,"publickey":<String_value>,"publickeysize":<Integer_value>,"version":<Integer_value>,"priority":<Double_value>,"status":<String_value>,"fipskey":<String_value>,"hsmkey":<String_value>,"passcrypt":<String_value>,"data":<Double_value>,"servicename":<String_value>,"expirymonitor":<String_value>,"notificationperiod":<Double_value>,"linkcertkeyname":<String_value>,"ocspresponsestatus":<String_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslcertkey?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "sslcertkey": [ { "__count": "#no"} ] }```



