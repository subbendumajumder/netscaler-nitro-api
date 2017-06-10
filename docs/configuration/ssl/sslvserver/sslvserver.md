#sslvserver

Configuration for SSL virtual server resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>vservername</td><td>&lt;String></td><td>Read-write</td><td>Name of the SSL virtual server for which to set advanced configuration.&lt;br>Minimum length = 1</td><tr><tr><td>cleartextport</td><td>&lt;Integer></td><td>Read-write</td><td>Port on which clear-text data is sent by the appliance to the server. Do not specify this parameter for SSL offloading with end-to-end encryption.&lt;br>Default value: 0&lt;br>Minimum value = 0&lt;br>Maximum value = 65534</td><tr><tr><td>dh</td><td>&lt;String></td><td>Read-write</td><td>State of Diffie-Hellman (DH) key exchange.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>dhfile</td><td>&lt;String></td><td>Read-write</td><td>Name of and, optionally, path to the DH parameter file, in PEM format, to be installed. /nsconfig/ssl/ is the default path.&lt;br>Minimum length = 1</td><tr><tr><td>dhcount</td><td>&lt;Double></td><td>Read-write</td><td>Number of interactions, between the client and the NetScaler appliance, after which the DH private-public pair is regenerated. A value of zero (0) specifies infinite use (no refresh).&lt;br>Minimum value = 0&lt;br>Maximum value = 65534</td><tr><tr><td>dhkeyexpsizelimit</td><td>&lt;String></td><td>Read-write</td><td>This option enables the use of NIST recommended (NIST Special Publication 800-56A) bit size for private-key size. For example, for DH params of size 2048bit, the private-key size recommended is 224bits. This is rounded-up to 256bits.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>ersa</td><td>&lt;String></td><td>Read-write</td><td>State of Ephemeral RSA (eRSA) key exchange. Ephemeral RSA allows clients that support only export ciphers to communicate with the secure server even if the server certificate does not support export clients. The ephemeral RSA key is automatically generated when you bind an export cipher to an SSL or TCP-based SSL virtual server or service. When you remove the export cipher, the eRSA key is not deleted. It is reused at a later date when another export cipher is bound to an SSL or TCP-based SSL virtual server or service. The eRSA key is deleted when the appliance restarts.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>ersacount</td><td>&lt;Double></td><td>Read-write</td><td>Refresh count for regeneration of the RSA public-key and private-key pair. Zero (0) specifies infinite usage (no refresh).&lt;br>Minimum value = 0&lt;br>Maximum value = 65534</td><tr><tr><td>sessreuse</td><td>&lt;String></td><td>Read-write</td><td>State of session reuse. Establishing the initial handshake requires CPU-intensive public key encryption operations. With the ENABLED setting, session key exchange is avoided for session resumption requests received from the client.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>sesstimeout</td><td>&lt;Double></td><td>Read-write</td><td>Time, in seconds, for which to keep the session active. Any session resumption request received after the timeout period will require a fresh SSL handshake and establishment of a new SSL session.&lt;br>Default value: 120&lt;br>Minimum value = 0&lt;br>Maximum value = 4294967294</td><tr><tr><td>cipherredirect</td><td>&lt;String></td><td>Read-write</td><td>State of Cipher Redirect. If cipher redirect is enabled, you can configure an SSL virtual server or service to display meaningful error messages if the SSL handshake fails because of a cipher mismatch between the virtual server or service and the client.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>cipherurl</td><td>&lt;String></td><td>Read-write</td><td>The redirect URL to be used with the Cipher Redirect feature.</td><tr><tr><td>sslv2redirect</td><td>&lt;String></td><td>Read-write</td><td>State of SSLv2 Redirect. If SSLv2 redirect is enabled, you can configure an SSL virtual server or service to display meaningful error messages if the SSL handshake fails because of a protocol version mismatch between the virtual server or service and the client.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>sslv2url</td><td>&lt;String></td><td>Read-write</td><td>URL of the page to which to redirect the client in case of a protocol version mismatch. Typically, this page has a clear explanation of the error or an alternative location that the transaction can continue from.</td><tr><tr><td>clientauth</td><td>&lt;String></td><td>Read-write</td><td>State of client authentication. If client authentication is enabled, the virtual server terminates the SSL handshake if the SSL client does not provide a valid certificate.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>clientcert</td><td>&lt;String></td><td>Read-write</td><td>Type of client authentication. If this parameter is set to MANDATORY, the appliance terminates the SSL handshake if the SSL client does not provide a valid certificate. With the OPTIONAL setting, the appliance requests a certificate from the SSL clients but proceeds with the SSL transaction even if the client presents an invalid certificate.&lt;br>Caution: Define proper access control policies before changing this setting to Optional.&lt;br>Possible values = Mandatory, Optional</td><tr><tr><td>sslredirect</td><td>&lt;String></td><td>Read-write</td><td>State of HTTPS redirects for the SSL virtual server. &lt;br>&lt;br>For an SSL session, if the client browser receives a redirect message, the browser tries to connect to the new location. However, the secure SSL session breaks if the object has moved from a secure site (https://) to an unsecure site (http://). Typically, a warning message appears on the screen, prompting the user to continue or disconnect.&lt;br>If SSL Redirect is ENABLED, the redirect message is automatically converted from http:// to https:// and the SSL session does not break.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>redirectportrewrite</td><td>&lt;String></td><td>Read-write</td><td>State of the port rewrite while performing HTTPS redirect. If this parameter is ENABLED and the URL from the server does not contain the standard port, the port is rewritten to the standard.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>ssl2</td><td>&lt;String></td><td>Read-write</td><td>State of SSLv2 protocol support for the SSL Virtual Server.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>ssl3</td><td>&lt;String></td><td>Read-write</td><td>State of SSLv3 protocol support for the SSL Virtual Server.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>tls1</td><td>&lt;String></td><td>Read-write</td><td>State of TLSv1.0 protocol support for the SSL Virtual Server.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>tls11</td><td>&lt;String></td><td>Read-write</td><td>State of TLSv1.1 protocol support for the SSL Virtual Server. TLSv1.1 protocol is supported only on the MPX appliance. Support is not available on a FIPS appliance or on a NetScaler VPX virtual appliance. On an SDX appliance, TLSv1.1 protocol is supported only if an SSL chip is assigned to the instance.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>tls12</td><td>&lt;String></td><td>Read-write</td><td>State of TLSv1.2 protocol support for the SSL Virtual Server. TLSv1.2 protocol is supported only on the MPX appliance. Support is not available on a FIPS appliance or on a NetScaler VPX virtual appliance. On an SDX appliance, TLSv1.2 protocol is supported only if an SSL chip is assigned to the instance.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>snienable</td><td>&lt;String></td><td>Read-write</td><td>State of the Server Name Indication (SNI) feature on the virtual server and service-based offload. SNI helps to enable SSL encryption on multiple domains on a single virtual server or service if the domains are controlled by the same organization and share the same second-level domain name. For example, *.sports.net can be used to secure domains such as login.sports.net and help.sports.net.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>ocspstapling</td><td>&lt;String></td><td>Read-write</td><td>State of OCSP stapling support on the SSL virtual server. Supported only if the protocol used is higher than SSLv3. Possible values:&lt;br>ENABLED: The appliance sends a request to the OCSP responder to check the status of the server certificate and caches the response for the specified time. If the response is valid at the time of SSL handshake with the client, the OCSP-based server certificate status is sent to the client during the handshake.&lt;br>DISABLED: The appliance does not check the status of the server certificate. .&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>pushenctrigger</td><td>&lt;String></td><td>Read-write</td><td>Trigger encryption on the basis of the PUSH flag value. Available settings function as follows:&lt;br>* ALWAYS - Any PUSH packet triggers encryption.&lt;br>* IGNORE - Ignore PUSH packet for triggering encryption.&lt;br>* MERGE - For a consecutive sequence of PUSH packets, the last PUSH packet triggers encryption.&lt;br>* TIMER - PUSH packet triggering encryption is delayed by the time defined in the set ssl parameter command or in the Change Advanced SSL Settings dialog box.&lt;br>Possible values = Always, Merge, Ignore, Timer</td><tr><tr><td>sendclosenotify</td><td>&lt;String></td><td>Read-write</td><td>Enable sending SSL Close-Notify at the end of a transaction.&lt;br>Default value: YES&lt;br>Possible values = YES, NO</td><tr><tr><td>dtlsprofilename</td><td>&lt;String></td><td>Read-write</td><td>Name of the DTLS profile whose settings are to be applied to the virtual server.&lt;br>Minimum length = 1&lt;br>Maximum length = 127</td><tr><tr><td>sslprofile</td><td>&lt;String></td><td>Read-write</td><td>Name of the SSL profile that contains SSL settings for the virtual server.&lt;br>Minimum length = 1&lt;br>Maximum length = 127</td><tr><tr><td>hsts</td><td>&lt;String></td><td>Read-write</td><td>State of TLSv1.0 protocol support for the SSL Virtual Server.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>maxage</td><td>&lt;Double></td><td>Read-write</td><td>Set max-age value for STS header.&lt;br>Default value: 0&lt;br>Minimum value = 0&lt;br>Maximum value = 4294967294</td><tr><tr><td>includesubdomains</td><td>&lt;String></td><td>Read-write</td><td>Set include sub domain value for STS header.&lt;br>Default value: NO&lt;br>Possible values = YES, NO</td><tr><tr><td>strictsigdigestcheck</td><td>&lt;String></td><td>Read-write</td><td>Parameter indicating to check whether peer entity certificate during TLS1.2 handshake is signed with one of signature-hash combination supported by Netscaler.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>crlcheck</td><td>&lt;String></td><td>Read-only</td><td>The state of the CRL check parameter. (Mandatory/Optional).&lt;br>Possible values = Mandatory, Optional</td><tr><tr><td>nonfipsciphers</td><td>&lt;String></td><td>Read-only</td><td>The state of usage of non FIPS approved ciphers.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>service</td><td>&lt;Double></td><td>Read-only</td><td>Service.&lt;br>Minimum value = 0&lt;br>Maximum value = 65534</td><tr><tr><td>ocspcheck</td><td>&lt;String></td><td>Read-only</td><td>The state of the OCSP check parameter. (Mandatory/Optional).&lt;br>Possible values = Mandatory, Optional</td><tr><tr><td>ca</td><td>&lt;Boolean></td><td>Read-only</td><td>CA certificate.</td><tr><tr><td>snicert</td><td>&lt;Boolean></td><td>Read-only</td><td>The name of the CertKey. Use this option to bind Certkey(s) which will be used in SNI processing.</td><tr><tr><td>skipcaname</td><td>&lt;Boolean></td><td>Read-only</td><td>The flag is used to indicate whether this particular CA certificates CA_Name needs to be sent to the SSL client while requesting for client certificate in a SSL handshake.</td><tr><tr><td>dtlsflag</td><td>&lt;Boolean></td><td>Read-only</td><td>The flag is used to indicate whether DTLS is set or not.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[UPDATE](#update) | [UNSET](#unset) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###update



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslvserver
HTTP Method: PUT
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"sslvserver":{      "vservername":<String_value>,      "cleartextport":<Integer_value>,      "dh":<String_value>,      "dhfile":<String_value>,      "dhcount":<Double_value>,      "dhkeyexpsizelimit":<String_value>,      "ersa":<String_value>,      "ersacount":<Double_value>,      "sessreuse":<String_value>,      "sesstimeout":<Double_value>,      "cipherredirect":<String_value>,      "cipherurl":<String_value>,      "sslv2redirect":<String_value>,      "sslv2url":<String_value>,      "clientauth":<String_value>,      "clientcert":<String_value>,      "sslredirect":<String_value>,      "redirectportrewrite":<String_value>,      "ssl2":<String_value>,      "ssl3":<String_value>,      "tls1":<String_value>,      "tls11":<String_value>,      "tls12":<String_value>,      "snienable":<String_value>,      "ocspstapling":<String_value>,      "pushenctrigger":<String_value>,      "sendclosenotify":<String_value>,      "dtlsprofilename":<String_value>,      "sslprofile":<String_value>,      "hsts":<String_value>,      "maxage":<Double_value>,      "includesubdomains":<String_value>,      "strictsigdigestcheck":<String_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslvserver?action=unset
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"sslvserver":{      "vservername":<String_value>,      "cleartextport":true,      "dh":true,      "dhfile":true,      "dhcount":true,      "dhkeyexpsizelimit":true,      "ersa":true,      "ersacount":true,      "sessreuse":true,      "sesstimeout":true,      "cipherredirect":true,      "cipherurl":true,      "sslv2redirect":true,      "sslv2url":true,      "clientauth":true,      "clientcert":true,      "sslredirect":true,      "redirectportrewrite":true,      "ssl2":true,      "ssl3":true,      "tls1":true,      "tls11":true,      "tls12":true,      "snienable":true,      "ocspstapling":true,      "sendclosenotify":true,      "dtlsprofilename":true,      "sslprofile":true,      "hsts":true,      "maxage":true,      "includesubdomains":true,      "strictsigdigestcheck":true}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslvserver
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslvserver?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


filter
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslvserver?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of sslvserver resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslvserver?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).


pagination
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslvserver?pagesize=#no;pageno=#no
Use this query-parameter to get the sslvserver resources in chunks.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "sslvserver": [ {      "vservername":<String_value>,      "cleartextport":<Integer_value>,      "dh":<String_value>,      "dhfile":<String_value>,      "dhcount":<Double_value>,      "dhkeyexpsizelimit":<String_value>,      "ersa":<String_value>,      "ersacount":<Double_value>,      "sessreuse":<String_value>,      "sesstimeout":<Double_value>,      "cipherredirect":<String_value>,      "crlcheck":<String_value>,      "cipherurl":<String_value>,      "sslv2redirect":<String_value>,      "sslv2url":<String_value>,      "clientauth":<String_value>,      "clientcert":<String_value>,      "sslredirect":<String_value>,      "redirectportrewrite":<String_value>,      "nonfipsciphers":<String_value>,      "ssl2":<String_value>,      "ssl3":<String_value>,      "tls1":<String_value>,      "tls11":<String_value>,      "tls12":<String_value>,      "snienable":<String_value>,      "ocspstapling":<String_value>,      "service":<Double_value>,      "servicename":<String_value>,      "ocspcheck":<String_value>,      "pushenctrigger":<String_value>,      "ca":<Boolean_value>,      "snicert":<Boolean_value>,      "skipcaname":<Boolean_value>,      "sendclosenotify":<String_value>,      "dtlsprofilename":<String_value>,      "dtlsflag":<Boolean_value>,      "sslprofile":<String_value>,      "hsts":<String_value>,      "maxage":<Double_value>,      "includesubdomains":<String_value>,      "strictsigdigestcheck":<String_value>}]}```



###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslvserver/vservername_value&lt;String&gt;
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslvserver/vservername_value&lt;String&gt;?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslvserver/vservername_value&lt;String&gt;?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "sslvserver": [ {      "vservername":<String_value>,      "cleartextport":<Integer_value>,      "dh":<String_value>,      "dhfile":<String_value>,      "dhcount":<Double_value>,      "dhkeyexpsizelimit":<String_value>,      "ersa":<String_value>,      "ersacount":<Double_value>,      "sessreuse":<String_value>,      "sesstimeout":<Double_value>,      "cipherredirect":<String_value>,      "crlcheck":<String_value>,      "cipherurl":<String_value>,      "sslv2redirect":<String_value>,      "sslv2url":<String_value>,      "clientauth":<String_value>,      "clientcert":<String_value>,      "sslredirect":<String_value>,      "redirectportrewrite":<String_value>,      "nonfipsciphers":<String_value>,      "ssl2":<String_value>,      "ssl3":<String_value>,      "tls1":<String_value>,      "tls11":<String_value>,      "tls12":<String_value>,      "snienable":<String_value>,      "ocspstapling":<String_value>,      "service":<Double_value>,      "servicename":<String_value>,      "ocspcheck":<String_value>,      "pushenctrigger":<String_value>,      "ca":<Boolean_value>,      "snicert":<Boolean_value>,      "skipcaname":<Boolean_value>,      "sendclosenotify":<String_value>,      "dtlsprofilename":<String_value>,      "dtlsflag":<Boolean_value>,      "sslprofile":<String_value>,      "hsts":<String_value>,      "maxage":<Double_value>,      "includesubdomains":<String_value>,      "strictsigdigestcheck":<String_value>}]}```



###count



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslvserver?count=yes
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: 
{ "sslvserver": [ { "__count": "#no"} ] }


