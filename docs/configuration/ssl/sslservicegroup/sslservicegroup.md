#sslservicegroup

Configuration for SSL service group resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>servicegroupname</td><td>&lt;String></td><td>Read-write</td><td>Name of the SSL service group for which to set advanced configuration.<br>Minimum length = 1</td></tr><tr><td>sslprofile</td><td>&lt;String></td><td>Read-write</td><td>Name of the SSL profile that contains SSL settings for the Service Group.<br>Minimum length = 1<br>Maximum length = 127</td></tr><tr><td>sessreuse</td><td>&lt;String></td><td>Read-write</td><td>State of session reuse. Establishing the initial handshake requires CPU-intensive public key encryption operations. With the ENABLED setting, session key exchange is avoided for session resumption requests received from the client.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>sesstimeout</td><td>&lt;Double></td><td>Read-write</td><td>Time, in seconds, for which to keep the session active. Any session resumption request received after the timeout period will require a fresh SSL handshake and establishment of a new SSL session.<br>Default value: 300<br>Minimum value = 0<br>Maximum value = 4294967294</td></tr><tr><td>ssl3</td><td>&lt;String></td><td>Read-write</td><td>State of SSLv3 protocol support for the SSL service group.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>tls1</td><td>&lt;String></td><td>Read-write</td><td>State of TLSv1.0 protocol support for the SSL service group.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>tls11</td><td>&lt;String></td><td>Read-write</td><td>State of TLSv1.1 protocol support for the SSL service group.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>tls12</td><td>&lt;String></td><td>Read-write</td><td>State of TLSv1.2 protocol support for the SSL service group.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>snienable</td><td>&lt;String></td><td>Read-write</td><td>State of the Server Name Indication (SNI) feature on the service. SNI helps to enable SSL encryption on multiple domains on a single virtual server or service if the domains are controlled by the same organization and share the same second-level domain name. For example, *.sports.net can be used to secure domains such as login.sports.net and help.sports.net.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>ocspstapling</td><td>&lt;String></td><td>Read-write</td><td>State of OCSP stapling support on the SSL virtual server. Supported only if the protocol used is higher than SSLv3. Possible values:<br>ENABLED: The appliance sends a request to the OCSP responder to check the status of the server certificate and caches the response for the specified time. If the response is valid at the time of SSL handshake with the client, the OCSP-based server certificate status is sent to the client during the handshake.<br>DISABLED: The appliance does not check the status of the server certificate.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>serverauth</td><td>&lt;String></td><td>Read-write</td><td>State of server authentication support for the SSL service group.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>commonname</td><td>&lt;String></td><td>Read-write</td><td>Name to be checked against the CommonName (CN) field in the server certificate bound to the SSL server.<br>Minimum length = 1</td></tr><tr><td>sendclosenotify</td><td>&lt;String></td><td>Read-write</td><td>Enable sending SSL Close-Notify at the end of a transaction.<br>Default value: YES<br>Possible values = YES, NO</td></tr><tr><td>strictsigdigestcheck</td><td>&lt;String></td><td>Read-write</td><td>Parameter indicating to check whether peer's certificate is signed with one of signature-hash combination supported by Netscaler.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>dh</td><td>&lt;String></td><td>Read-only</td><td>The state of DH key exchange support for the SSL service group.<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>dhfile</td><td>&lt;String></td><td>Read-only</td><td>The file name and path for the DH parameter.</td></tr><tr><td>dhcount</td><td>&lt;Double></td><td>Read-only</td><td>The refresh count for the re-generation of DH public-key and private-key from the DH parameter.<br>Minimum value = 0<br>Maximum value = 65534</td></tr><tr><td>dhkeyexpsizelimit</td><td>&lt;String></td><td>Read-only</td><td>This option enables the use of NIST recommended (NIST Special Publication 800-56A) bit size for private-key size. For example, for DH params of size 2048bit, the private-key size recommended is 224bits. This is rounded-up to 256bits.<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>ersa</td><td>&lt;String></td><td>Read-only</td><td>The state of Ephemeral RSA key exchange support for the SSL service group.Ephemeral RSA is used for export ciphers.<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>ersacount</td><td>&lt;Double></td><td>Read-only</td><td>The refresh count for the re-generation of RSA public-key and private-key pair.<br>Minimum value = 0<br>Maximum value = 65534</td></tr><tr><td>cipherredirect</td><td>&lt;String></td><td>Read-only</td><td>The state of Cipher Redirect feature. Cipher Redirect feature can be used to provide more readable information to SSL clients about mismatch in ciphers between the client and the SSL vserver.<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>cipherurl</td><td>&lt;String></td><td>Read-only</td><td>The redirect URL to be used with the Cipher Redirect feature.</td></tr><tr><td>sslv2redirect</td><td>&lt;String></td><td>Read-only</td><td>The state of SSLv2 Redirect feature.SSLv2 Redirect feature can be used to provide more readable information to SSL client about non-support of SSLv2 protocol on the SSL vserver.<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>sslv2url</td><td>&lt;String></td><td>Read-only</td><td>The redirect URL to be used with SSLv2 Redirect feature.</td></tr><tr><td>clientauth</td><td>&lt;String></td><td>Read-only</td><td>The state of Client-Authentication support for the SSL service group.<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>clientcert</td><td>&lt;String></td><td>Read-only</td><td>The rule for client certificate requirement in client authentication.<br>Possible values = Mandatory, Optional</td></tr><tr><td>sslredirect</td><td>&lt;String></td><td>Read-only</td><td>The state of HTTPS redirects for the SSL service group.<br><br><br>This is required for the proper functioning of the redirect messages from the server. The redirect message from the server provides the new location for the moved object. This is contained in the HTTP header field: Location, e.g. Location: http://www.moved.org/here.html<br><br>For the SSL session, if the client browser receives this message, the browser will try to connect to the new location. This will break the secure SSL session, as the object has moved from a secure site (https://) to an un-secure one (http://). Generally browsers flash a warning message on the screen and prompt the user, either to continue or disconnect.<br><br>The above feature, when enabled will automatically convert all such http:// redirect message to https://. This will not break the client SSL session.<br><br>Note: The set ssl service command can be used for configuring a front-end SSL service for service based SSL Off-Loading, or a backend SSL service for backend-encryption setup.<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>redirectportrewrite</td><td>&lt;String></td><td>Read-only</td><td>The state of port-rewrite feature.<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>nonfipsciphers</td><td>&lt;String></td><td>Read-only</td><td>The state of usage of non FIPS approved ciphers.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>ssl2</td><td>&lt;String></td><td>Read-only</td><td>The state of SSLv2 protocol support for the SSL service group.<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>ocspcheck</td><td>&lt;String></td><td>Read-only</td><td>The state of the OCSP check parameter. (Mandatory/Optional).<br>Possible values = Mandatory, Optional</td></tr><tr><td>crlcheck</td><td>&lt;String></td><td>Read-only</td><td>The state of the CRL check parameter. (Mandatory/Optional).<br>Possible values = Mandatory, Optional</td></tr><tr><td>cleartextport</td><td>&lt;Integer></td><td>Read-only</td><td>The port on the back-end web-servers where the clear-text data is sent by system. Use this setting for the wildcard IP based SSL Acceleration configuration (*:443).<br>Minimum value = 0<br>Maximum value = 65534<br>Range 1 - 65535<br>* in CLI is represented as 65535 in NITRO API</td></tr><tr><td>servicename</td><td>&lt;String></td><td>Read-only</td><td>The service name.</td></tr><tr><td>ca</td><td>&lt;Boolean></td><td>Read-only</td><td>CA certificate.</td></tr><tr><td>snicert</td><td>&lt;Boolean></td><td>Read-only</td><td>The name of the CertKey. Use this option to bind Certkey(s) which will be used in SNI processing.</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[UPDATE](#u)| [UNSET](#)| [GET (ALL)](#get-)| [GET]()| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslservicegroup
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"sslservicegroup":{<b>"servicegroupname":<String_value>,</b>"sslprofile":<String_value>,"sessreuse":<String_value>,"sesstimeout":<Double_value>,"ssl3":<String_value>,"tls1":<String_value>,"tls11":<String_value>,"tls12":<String_value>,"snienable":<String_value>,"ocspstapling":<String_value>,"serverauth":<String_value>,"commonname":<String_value>,"sendclosenotify":<String_value>,"strictsigdigestcheck":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslservicegroup?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"sslservicegroup":{<b>"servicegroupname":<String_value>,</b>"sslprofile":true,"sessreuse":true,"sesstimeout":true,"ssl3":true,"tls1":true,"tls11":true,"tls12":true,"snienable":true,"ocspstapling":true,"serverauth":true,"commonname":true,"sendclosenotify":true,"strictsigdigestcheck":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslservicegroup
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslservicegroup?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslservicegroup?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of sslservicegroup resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslservicegroup?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslservicegroup?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the sslservicegroup resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "sslservicegroup": [ {"servicegroupname":<String_value>,"dh":<String_value>,"dhfile":<String_value>,"dhcount":<Double_value>,"dhkeyexpsizelimit":<String_value>,"ersa":<String_value>,"ersacount":<Double_value>,"sessreuse":<String_value>,"sesstimeout":<Double_value>,"cipherredirect":<String_value>,"cipherurl":<String_value>,"sslv2redirect":<String_value>,"sslv2url":<String_value>,"clientauth":<String_value>,"clientcert":<String_value>,"sslredirect":<String_value>,"redirectportrewrite":<String_value>,"nonfipsciphers":<String_value>,"ssl2":<String_value>,"ssl3":<String_value>,"tls1":<String_value>,"tls11":<String_value>,"tls12":<String_value>,"snienable":<String_value>,"ocspstapling":<String_value>,"serverauth":<String_value>,"commonname":<String_value>,"ocspcheck":<String_value>,"crlcheck":<String_value>,"cleartextport":<Integer_value>,"servicename":<String_value>,"ca":<Boolean_value>,"snicert":<Boolean_value>,"sendclosenotify":<String_value>,"sslprofile":<String_value>,"strictsigdigestcheck":<String_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslservicegroup/servicegroupname_value&lt;String&gt;
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslservicegroup/servicegroupname_value&lt;String&gt;?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslservicegroup/servicegroupname_value&lt;String&gt;?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "sslservicegroup": [ {"servicegroupname":<String_value>,"dh":<String_value>,"dhfile":<String_value>,"dhcount":<Double_value>,"dhkeyexpsizelimit":<String_value>,"ersa":<String_value>,"ersacount":<Double_value>,"sessreuse":<String_value>,"sesstimeout":<Double_value>,"cipherredirect":<String_value>,"cipherurl":<String_value>,"sslv2redirect":<String_value>,"sslv2url":<String_value>,"clientauth":<String_value>,"clientcert":<String_value>,"sslredirect":<String_value>,"redirectportrewrite":<String_value>,"nonfipsciphers":<String_value>,"ssl2":<String_value>,"ssl3":<String_value>,"tls1":<String_value>,"tls11":<String_value>,"tls12":<String_value>,"snienable":<String_value>,"ocspstapling":<String_value>,"serverauth":<String_value>,"commonname":<String_value>,"ocspcheck":<String_value>,"crlcheck":<String_value>,"cleartextport":<Integer_value>,"servicename":<String_value>,"ca":<Boolean_value>,"snicert":<Boolean_value>,"sendclosenotify":<String_value>,"sslprofile":<String_value>,"strictsigdigestcheck":<String_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslservicegroup?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "sslservicegroup": [ { "__count": "#no"} ] }```



