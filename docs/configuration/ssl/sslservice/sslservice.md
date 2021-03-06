#sslservice

Configuration for SSL service resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>servicename</td><td>&lt;String></td><td>Read-write</td><td>Name of the SSL service.<br>Minimum length = 1</td></tr><tr><td>dh</td><td>&lt;String></td><td>Read-write</td><td>State of Diffie-Hellman (DH) key exchange. This parameter is not applicable when configuring a backend service.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>dhfile</td><td>&lt;String></td><td>Read-write</td><td>Name for and, optionally, path to the PEM-format DH parameter file to be installed. /nsconfig/ssl/ is the default path. This parameter is not applicable when configuring a backend service.<br>Minimum length = 1</td></tr><tr><td>dhcount</td><td>&lt;Double></td><td>Read-write</td><td>Number of interactions, between the client and the NetScaler appliance, after which the DH private-public pair is regenerated. A value of zero (0) specifies infinite use (no refresh). This parameter is not applicable when configuring a backend service. Allowed DH count values are 0 and &gt;= 500.<br>Minimum value = 0<br>Maximum value = 65534</td></tr><tr><td>dhkeyexpsizelimit</td><td>&lt;String></td><td>Read-write</td><td>This option enables the use of NIST recommended (NIST Special Publication 800-56A) bit size for private-key size. For example, for DH params of size 2048bit, the private-key size recommended is 224bits. This is rounded-up to 256bits.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>ersa</td><td>&lt;String></td><td>Read-write</td><td>State of Ephemeral RSA (eRSA) key exchange. Ephemeral RSA allows clients that support only export ciphers to communicate with the secure server even if the server certificate does not support export clients. The ephemeral RSA key is automatically generated when you bind an export cipher to an SSL or TCP-based SSL virtual server or service. When you remove the export cipher, the eRSA key is not deleted. It is reused at a later date when another export cipher is bound to an SSL or TCP-based SSL virtual server or service. The eRSA key is deleted when the appliance restarts.<br>This parameter is not applicable when configuring a backend service.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>ersacount</td><td>&lt;Double></td><td>Read-write</td><td>Refresh count for regeneration of RSA public-key and private-key pair. Zero (0) specifies infinite usage (no refresh). <br>This parameter is not applicable when configuring a backend service.<br>Minimum value = 0<br>Maximum value = 65534</td></tr><tr><td>sessreuse</td><td>&lt;String></td><td>Read-write</td><td>State of session reuse. Establishing the initial handshake requires CPU-intensive public key encryption operations. With the ENABLED setting, session key exchange is avoided for session resumption requests received from the client.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>sesstimeout</td><td>&lt;Double></td><td>Read-write</td><td>Time, in seconds, for which to keep the session active. Any session resumption request received after the timeout period will require a fresh SSL handshake and establishment of a new SSL session.<br>Default value: 300<br>Minimum value = 0<br>Maximum value = 4294967294</td></tr><tr><td>cipherredirect</td><td>&lt;String></td><td>Read-write</td><td>State of Cipher Redirect. If this parameter is set to ENABLED, you can configure an SSL virtual server or service to display meaningful error messages if the SSL handshake fails because of a cipher mismatch between the virtual server or service and the client.<br>This parameter is not applicable when configuring a backend service.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>cipherurl</td><td>&lt;String></td><td>Read-write</td><td>URL of the page to which to redirect the client in case of a cipher mismatch. Typically, this page has a clear explanation of the error or an alternative location that the transaction can continue from.<br>This parameter is not applicable when configuring a backend service.</td></tr><tr><td>sslv2redirect</td><td>&lt;String></td><td>Read-write</td><td>State of SSLv2 Redirect. If this parameter is set to ENABLED, you can configure an SSL virtual server or service to display meaningful error messages if the SSL handshake fails because of a protocol version mismatch between the virtual server or service and the client.<br>This parameter is not applicable when configuring a backend service.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>sslv2url</td><td>&lt;String></td><td>Read-write</td><td>URL of the page to which to redirect the client in case of a protocol version mismatch. Typically, this page has a clear explanation of the error or an alternative location that the transaction can continue from.<br>This parameter is not applicable when configuring a backend service.</td></tr><tr><td>clientauth</td><td>&lt;String></td><td>Read-write</td><td>State of client authentication. In service-based SSL offload, the service terminates the SSL handshake if the SSL client does not provide a valid certificate. <br>This parameter is not applicable when configuring a backend service.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>clientcert</td><td>&lt;String></td><td>Read-write</td><td>Type of client authentication. If this parameter is set to MANDATORY, the appliance terminates the SSL handshake if the SSL client does not provide a valid certificate. With the OPTIONAL setting, the appliance requests a certificate from the SSL clients but proceeds with the SSL transaction even if the client presents an invalid certificate.<br>This parameter is not applicable when configuring a backend SSL service.<br>Caution: Define proper access control policies before changing this setting to Optional.<br>Possible values = Mandatory, Optional</td></tr><tr><td>sslredirect</td><td>&lt;String></td><td>Read-write</td><td>State of HTTPS redirects for the SSL service. <br><br>For an SSL session, if the client browser receives a redirect message, the browser tries to connect to the new location. However, the secure SSL session breaks if the object has moved from a secure site (https://) to an unsecure site (http://). Typically, a warning message appears on the screen, prompting the user to continue or disconnect.<br>If SSL Redirect is ENABLED, the redirect message is automatically converted from http:// to https:// and the SSL session does not break.<br><br>This parameter is not applicable when configuring a backend service.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>redirectportrewrite</td><td>&lt;String></td><td>Read-write</td><td>State of the port rewrite while performing HTTPS redirect. If this parameter is set to ENABLED, and the URL from the server does not contain the standard port, the port is rewritten to the standard.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>ssl2</td><td>&lt;String></td><td>Read-write</td><td>State of SSLv2 protocol support for the SSL service.<br>This parameter is not applicable when configuring a backend service.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>ssl3</td><td>&lt;String></td><td>Read-write</td><td>State of SSLv3 protocol support for the SSL service.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>tls1</td><td>&lt;String></td><td>Read-write</td><td>State of TLSv1.0 protocol support for the SSL service.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>tls11</td><td>&lt;String></td><td>Read-write</td><td>State of TLSv1.1 protocol support for the SSL service. Enabled for Front-end service on MPX-CVM platform only.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>tls12</td><td>&lt;String></td><td>Read-write</td><td>State of TLSv1.2 protocol support for the SSL service. Enabled for Front-end service on MPX-CVM platform only.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>snienable</td><td>&lt;String></td><td>Read-write</td><td>State of the Server Name Indication (SNI) feature on the virtual server and service-based offload. SNI helps to enable SSL encryption on multiple domains on a single virtual server or service if the domains are controlled by the same organization and share the same second-level domain name. For example, *.sports.net can be used to secure domains such as login.sports.net and help.sports.net.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>ocspstapling</td><td>&lt;String></td><td>Read-write</td><td>State of OCSP stapling support on the SSL virtual server. Supported only if the protocol used is higher than SSLv3. Possible values:<br>ENABLED: The appliance sends a request to the OCSP responder to check the status of the server certificate and caches the response for the specified time. If the response is valid at the time of SSL handshake with the client, the OCSP-based server certificate status is sent to the client during the handshake.<br>DISABLED: The appliance does not check the status of the server certificate. .<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>serverauth</td><td>&lt;String></td><td>Read-write</td><td>State of server authentication support for the SSL service.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>commonname</td><td>&lt;String></td><td>Read-write</td><td>Name to be checked against the CommonName (CN) field in the server certificate bound to the SSL server.<br>Minimum length = 1</td></tr><tr><td>pushenctrigger</td><td>&lt;String></td><td>Read-write</td><td>Trigger encryption on the basis of the PUSH flag value. Available settings function as follows:<br>* ALWAYS - Any PUSH packet triggers encryption.<br>* IGNORE - Ignore PUSH packet for triggering encryption.<br>* MERGE - For a consecutive sequence of PUSH packets, the last PUSH packet triggers encryption.<br>* TIMER - PUSH packet triggering encryption is delayed by the time defined in the set ssl parameter command or in the Change Advanced SSL Settings dialog box.<br>Possible values = Always, Merge, Ignore, Timer</td></tr><tr><td>sendclosenotify</td><td>&lt;String></td><td>Read-write</td><td>Enable sending SSL Close-Notify at the end of a transaction.<br>Default value: YES<br>Possible values = YES, NO</td></tr><tr><td>dtlsprofilename</td><td>&lt;String></td><td>Read-write</td><td>Name of the DTLS profile that contains DTLS settings for the service.<br>Minimum length = 1<br>Maximum length = 127</td></tr><tr><td>sslprofile</td><td>&lt;String></td><td>Read-write</td><td>Name of the SSL profile that contains SSL settings for the service.<br>Minimum length = 1<br>Maximum length = 127</td></tr><tr><td>strictsigdigestcheck</td><td>&lt;String></td><td>Read-write</td><td>Parameter indicating to check whether peer's certificate during TLS1.2 handshake is signed with one of signature-hash combination supported by Netscaler.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>nonfipsciphers</td><td>&lt;String></td><td>Read-only</td><td>The state of usage of non FIPS approved ciphers.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>service</td><td>&lt;Double></td><td>Read-only</td><td>.</td></tr><tr><td>skipcaname</td><td>&lt;Boolean></td><td>Read-only</td><td>The flag is used to indicate whether this particular CA certificate's CA_Name needs to be sent to the SSL client while requesting for client certificate in a SSL handshake.</td></tr><tr><td>dtlsflag</td><td>&lt;Boolean></td><td>Read-only</td><td>The flag is used to indicate whether DTLS is set or not.</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[UPDATE](#u)| [UNSET](#)| [GET (ALL)](#get-)| [GET]()| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslservice
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"sslservice":{<b>"servicename":<String_value>,</b>"dh":<String_value>,"dhfile":<String_value>,"dhcount":<Double_value>,"dhkeyexpsizelimit":<String_value>,"ersa":<String_value>,"ersacount":<Double_value>,"sessreuse":<String_value>,"sesstimeout":<Double_value>,"cipherredirect":<String_value>,"cipherurl":<String_value>,"sslv2redirect":<String_value>,"sslv2url":<String_value>,"clientauth":<String_value>,"clientcert":<String_value>,"sslredirect":<String_value>,"redirectportrewrite":<String_value>,"ssl2":<String_value>,"ssl3":<String_value>,"tls1":<String_value>,"tls11":<String_value>,"tls12":<String_value>,"snienable":<String_value>,"ocspstapling":<String_value>,"serverauth":<String_value>,"commonname":<String_value>,"pushenctrigger":<String_value>,"sendclosenotify":<String_value>,"dtlsprofilename":<String_value>,"sslprofile":<String_value>,"strictsigdigestcheck":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslservice?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"sslservice":{<b>"servicename":<String_value>,</b>"dh":true,"dhfile":true,"dhcount":true,"dhkeyexpsizelimit":true,"ersa":true,"ersacount":true,"sessreuse":true,"sesstimeout":true,"cipherredirect":true,"cipherurl":true,"sslv2redirect":true,"sslv2url":true,"clientauth":true,"clientcert":true,"sslredirect":true,"redirectportrewrite":true,"ssl2":true,"ssl3":true,"tls1":true,"tls11":true,"tls12":true,"snienable":true,"ocspstapling":true,"serverauth":true,"commonname":true,"sendclosenotify":true,"dtlsprofilename":true,"sslprofile":true,"strictsigdigestcheck":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslservice
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslservice?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslservice?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of sslservice resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslservice?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslservice?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the sslservice resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "sslservice": [ {"servicename":<String_value>,"dh":<String_value>,"dhfile":<String_value>,"dhcount":<Double_value>,"dhkeyexpsizelimit":<String_value>,"ersa":<String_value>,"ersacount":<Double_value>,"sessreuse":<String_value>,"sesstimeout":<Double_value>,"cipherredirect":<String_value>,"cipherurl":<String_value>,"sslv2redirect":<String_value>,"sslv2url":<String_value>,"clientauth":<String_value>,"clientcert":<String_value>,"sslredirect":<String_value>,"redirectportrewrite":<String_value>,"nonfipsciphers":<String_value>,"ssl2":<String_value>,"ssl3":<String_value>,"tls1":<String_value>,"tls11":<String_value>,"tls12":<String_value>,"snienable":<String_value>,"ocspstapling":<String_value>,"serverauth":<String_value>,"commonname":<String_value>,"service":<Double_value>,"pushenctrigger":<String_value>,"skipcaname":<Boolean_value>,"sendclosenotify":<String_value>,"dtlsprofilename":<String_value>,"dtlsflag":<Boolean_value>,"sslprofile":<String_value>,"strictsigdigestcheck":<String_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslservice/servicename_value&lt;String&gt;
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslservice/servicename_value&lt;String&gt;?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslservice/servicename_value&lt;String&gt;?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "sslservice": [ {"servicename":<String_value>,"dh":<String_value>,"dhfile":<String_value>,"dhcount":<Double_value>,"dhkeyexpsizelimit":<String_value>,"ersa":<String_value>,"ersacount":<Double_value>,"sessreuse":<String_value>,"sesstimeout":<Double_value>,"cipherredirect":<String_value>,"cipherurl":<String_value>,"sslv2redirect":<String_value>,"sslv2url":<String_value>,"clientauth":<String_value>,"clientcert":<String_value>,"sslredirect":<String_value>,"redirectportrewrite":<String_value>,"nonfipsciphers":<String_value>,"ssl2":<String_value>,"ssl3":<String_value>,"tls1":<String_value>,"tls11":<String_value>,"tls12":<String_value>,"snienable":<String_value>,"ocspstapling":<String_value>,"serverauth":<String_value>,"commonname":<String_value>,"service":<Double_value>,"pushenctrigger":<String_value>,"skipcaname":<Boolean_value>,"sendclosenotify":<String_value>,"dtlsprofilename":<String_value>,"dtlsflag":<Boolean_value>,"sslprofile":<String_value>,"strictsigdigestcheck":<String_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslservice?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "sslservice": [ { "__count": "#no"} ] }```



