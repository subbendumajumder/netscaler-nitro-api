#sslprofile

Configuration for SSL profile resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the SSL profile. Must begin with an ASCII alphanumeric or underscore (_) character, and must contain only ASCII alphanumeric, underscore, hash (#), period (.), space, colon (:), at (@), equals (=), and hyphen (-) characters. Cannot be changed after the profile is created.<br>Minimum length = 1<br>Maximum length = 127</td></tr><tr><td>sslprofiletype</td><td>&lt;String></td><td>Read-write</td><td>Type of profile. Front end profiles apply to the entity that receives requests from a client. Backend profiles apply to the entity that sends client requests to a server.<br>Default value: FrontEnd<br>Possible values = BackEnd, FrontEnd</td></tr><tr><td>dhcount</td><td>&lt;Double></td><td>Read-write</td><td>Number of interactions, between the client and the NetScaler appliance, after which the DH private-public pair is regenerated. A value of zero (0) specifies infinite use (no refresh).<br>This parameter is not applicable when configuring a backend profile. Allowed DH count values are 0 and &gt;= 500.<br>Minimum value = 0<br>Maximum value = 65534</td></tr><tr><td>dh</td><td>&lt;String></td><td>Read-write</td><td>State of Diffie-Hellman (DH) key exchange.<br>This parameter is not applicable when configuring a backend profile.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>dhfile</td><td>&lt;String></td><td>Read-write</td><td>The file name and path for the DH parameter.<br>Minimum length = 1</td></tr><tr><td>ersa</td><td>&lt;String></td><td>Read-write</td><td>State of Ephemeral RSA (eRSA) key exchange. Ephemeral RSA allows clients that support only export ciphers to communicate with the secure server even if the server certificate does not support export clients. The ephemeral RSA key is automatically generated when you bind an export cipher to an SSL or TCP-based SSL virtual server or service. When you remove the export cipher, the eRSA key is not deleted. It is reused at a later date when another export cipher is bound to an SSL or TCP-based SSL virtual server or service. The eRSA key is deleted when the appliance restarts.<br>This parameter is not applicable when configuring a backend profile.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>ersacount</td><td>&lt;Double></td><td>Read-write</td><td>The refresh count for the re-generation of RSA public-key and private-key pair.<br>Minimum value = 0<br>Maximum value = 65534</td></tr><tr><td>sessreuse</td><td>&lt;String></td><td>Read-write</td><td>State of session reuse. Establishing the initial handshake requires CPU-intensive public key encryption operations. With the ENABLED setting, session key exchange is avoided for session resumption requests received from the client.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>sesstimeout</td><td>&lt;Double></td><td>Read-write</td><td>The Session timeout value in seconds.<br>Minimum value = 0<br>Maximum value = 4294967294</td></tr><tr><td>cipherredirect</td><td>&lt;String></td><td>Read-write</td><td>State of Cipher Redirect. If this parameter is set to ENABLED, you can configure an SSL virtual server or service to display meaningful error messages if the SSL handshake fails because of a cipher mismatch between the virtual server or service and the client.<br>This parameter is not applicable when configuring a backend profile.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>cipherurl</td><td>&lt;String></td><td>Read-write</td><td>The redirect URL to be used with the Cipher Redirect feature.</td></tr><tr><td>clientauth</td><td>&lt;String></td><td>Read-write</td><td>State of client authentication. In service-based SSL offload, the service terminates the SSL handshake if the SSL client does not provide a valid certificate. <br>This parameter is not applicable when configuring a backend profile.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>clientcert</td><td>&lt;String></td><td>Read-write</td><td>The rule for client certificate requirement in client authentication.<br>Possible values = Mandatory, Optional</td></tr><tr><td>dhkeyexpsizelimit</td><td>&lt;String></td><td>Read-write</td><td>This option enables the use of NIST recommended (NIST Special Publication 800-56A) bit size for private-key size. For example, for DH params of size 2048bit, the private-key size recommended is 224bits. This is rounded-up to 256bits.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>sslredirect</td><td>&lt;String></td><td>Read-write</td><td>State of HTTPS redirects for the SSL service. <br>For an SSL session, if the client browser receives a redirect message, the browser tries to connect to the new location. However, the secure SSL session breaks if the object has moved from a secure site (https://) to an unsecure site (http://). Typically, a warning message appears on the screen, prompting the user to continue or disconnect.<br>If SSL Redirect is ENABLED, the redirect message is automatically converted from http:// to https:// and the SSL session does not break.<br>This parameter is not applicable when configuring a backend profile.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>redirectportrewrite</td><td>&lt;String></td><td>Read-write</td><td>State of the port rewrite while performing HTTPS redirect. If this parameter is set to ENABLED, and the URL from the server does not contain the standard port, the port is rewritten to the standard.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>ssl3</td><td>&lt;String></td><td>Read-write</td><td>State of SSLv3 protocol support for the SSL profile.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>tls1</td><td>&lt;String></td><td>Read-write</td><td>State of TLSv1.0 protocol support for the SSL profile.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>tls11</td><td>&lt;String></td><td>Read-write</td><td>State of TLSv1.1 protocol support for the SSL profile.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>tls12</td><td>&lt;String></td><td>Read-write</td><td>State of TLSv1.2 protocol support for the SSL profile.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>snienable</td><td>&lt;String></td><td>Read-write</td><td>State of the Server Name Indication (SNI) feature on the virtual server and service-based offload. SNI helps to enable SSL encryption on multiple domains on a single virtual server or service if the domains are controlled by the same organization and share the same second-level domain name. For example, *.sports.net can be used to secure domains such as login.sports.net and help.sports.net.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>ocspstapling</td><td>&lt;String></td><td>Read-write</td><td>State of OCSP stapling support on the SSL virtual server. Supported only if the protocol used is higher than SSLv3. Possible values:<br>ENABLED: The appliance sends a request to the OCSP responder to check the status of the server certificate and caches the response for the specified time. If the response is valid at the time of SSL handshake with the client, the OCSP-based server certificate status is sent to the client during the handshake.<br>DISABLED: The appliance does not check the status of the server certificate. .<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>serverauth</td><td>&lt;String></td><td>Read-write</td><td>State of server authentication support for the SSL Backend profile.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>commonname</td><td>&lt;String></td><td>Read-write</td><td>Name to be checked against the CommonName (CN) field in the server certificate bound to the SSL server.<br>Minimum length = 1</td></tr><tr><td>pushenctrigger</td><td>&lt;String></td><td>Read-write</td><td>Trigger encryption on the basis of the PUSH flag value. Available settings function as follows:<br>* ALWAYS - Any PUSH packet triggers encryption.<br>* IGNORE - Ignore PUSH packet for triggering encryption.<br>* MERGE - For a consecutive sequence of PUSH packets, the last PUSH packet triggers encryption.<br>* TIMER - PUSH packet triggering encryption is delayed by the time defined in the set ssl parameter command or in the Change Advanced SSL Settings dialog box.<br>Possible values = Always, Merge, Ignore, Timer</td></tr><tr><td>sendclosenotify</td><td>&lt;String></td><td>Read-write</td><td>Enable sending SSL Close-Notify at the end of a transaction.<br>Default value: YES<br>Possible values = YES, NO</td></tr><tr><td>cleartextport</td><td>&lt;Integer></td><td>Read-write</td><td>Port on which clear-text data is sent by the appliance to the server. Do not specify this parameter for SSL offloading with end-to-end encryption.<br>Range 1 - 65535<br>* in CLI is represented as 65535 in NITRO API</td></tr><tr><td>insertionencoding</td><td>&lt;String></td><td>Read-write</td><td>Encoding method used to insert the subject or issuer's name in HTTP requests to servers.<br>Default value: Unicode<br>Possible values = Unicode, UTF-8</td></tr><tr><td>denysslreneg</td><td>&lt;String></td><td>Read-write</td><td>Deny renegotiation in specified circumstances. Available settings function as follows:<br>* NO - Allow SSL renegotiation.<br>* FRONTEND_CLIENT - Deny secure and nonsecure SSL renegotiation initiated by the client.<br>* FRONTEND_CLIENTSERVER - Deny secure and nonsecure SSL renegotiation initiated by the client or the NetScaler during policy-based client authentication. <br>* ALL - Deny all secure and nonsecure SSL renegotiation.<br>* NONSECURE - Deny nonsecure SSL renegotiation. Allows only clients that support RFC 5746.<br>Default value: ALL<br>Possible values = NO, FRONTEND_CLIENT, FRONTEND_CLIENTSERVER, ALL, NONSECURE</td></tr><tr><td>quantumsize</td><td>&lt;String></td><td>Read-write</td><td>Amount of data to collect before the data is pushed to the crypto hardware for encryption. For large downloads, a larger quantum size better utilizes the crypto resources.<br>Default value: 8192<br>Possible values = 4096, 8192, 16384</td></tr><tr><td>strictcachecks</td><td>&lt;String></td><td>Read-write</td><td>Enable strict CA certificate checks on the appliance.<br>Default value: NO<br>Possible values = YES, NO</td></tr><tr><td>encrypttriggerpktcount</td><td>&lt;Double></td><td>Read-write</td><td>Maximum number of queued packets after which encryption is triggered. Use this setting for SSL transactions that send small packets from server to NetScaler.<br>Default value: 45<br>Minimum value = 10<br>Maximum value = 50</td></tr><tr><td>pushflag</td><td>&lt;Double></td><td>Read-write</td><td>Insert PUSH flag into decrypted, encrypted, or all records. If the PUSH flag is set to a value other than 0, the buffered records are forwarded on the basis of the value of the PUSH flag. Available settings function as follows:<br>0 - Auto (PUSH flag is not set.)<br>1 - Insert PUSH flag into every decrypted record.<br>2 -Insert PUSH flag into every encrypted record.<br>3 - Insert PUSH flag into every decrypted and encrypted record.<br>Minimum value = 0<br>Maximum value = 3</td></tr><tr><td>dropreqwithnohostheader</td><td>&lt;String></td><td>Read-write</td><td>Host header check for SNI enabled sessions. If this check is enabled and the HTTP request does not contain the host header for SNI enabled sessions, the request is dropped.<br>Default value: NO<br>Possible values = YES, NO</td></tr><tr><td>pushenctriggertimeout</td><td>&lt;Double></td><td>Read-write</td><td>PUSH encryption trigger timeout value. The timeout value is applied only if you set the Push Encryption Trigger parameter to Timer in the SSL virtual server settings.<br>Default value: 1<br>Minimum value = 1<br>Maximum value = 200</td></tr><tr><td>ssltriggertimeout</td><td>&lt;Double></td><td>Read-write</td><td>Time, in milliseconds, after which encryption is triggered for transactions that are not tracked on the NetScaler appliance because their length is not known. There can be a delay of up to 10ms from the specified timeout value before the packet is pushed into the queue.<br>Default value: 100<br>Minimum value = 1<br>Maximum value = 200</td></tr><tr><td>clientauthuseboundcachain</td><td>&lt;String></td><td>Read-write</td><td>Certficates bound on the VIP are used for validating the client cert. Certficates came along with client cert are not used for validating the client cert.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>sslinterception</td><td>&lt;String></td><td>Read-write</td><td>Enable or disable transparent interception of SSL sessions.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>sslireneg</td><td>&lt;String></td><td>Read-write</td><td>Enable or disable triggering the client renegotiation when renegotiation request is received from the origin server.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>ssliocspcheck</td><td>&lt;String></td><td>Read-write</td><td>Enable or disable OCSP check for origin server certificate.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>sslimaxsessperserver</td><td>&lt;Double></td><td>Read-write</td><td>Maximum ssl session to be cached per dynamic origin server. A unique ssl session is created for each SNI received from the client on ClientHello and the matching session is used for server session reuse.<br>Default value: 10<br>Minimum value = 1<br>Maximum value = 1000</td></tr><tr><td>sessionticket</td><td>&lt;String></td><td>Read-write</td><td>This option enables the use of session tickets, as per the RFC 5077.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>sessionticketlifetime</td><td>&lt;Double></td><td>Read-write</td><td>This option sets the life time of session tickets issued by NS in secs.<br>Default value: 300<br>Minimum value = 0<br>Maximum value = 172800</td></tr><tr><td>sessionticketkeyrefresh</td><td>&lt;String></td><td>Read-write</td><td>This option enables the use of session tickets, as per the RFC 5077.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>sessionticketkeydata</td><td>&lt;String></td><td>Read-write</td><td>Session ticket enc/dec key , admin can set it.</td></tr><tr><td>sessionkeylifetime</td><td>&lt;Double></td><td>Read-write</td><td>This option sets the life time of symm key used to generate session tickets issued by NS in secs.<br>Default value: 3000<br>Minimum value = 600<br>Maximum value = 86400</td></tr><tr><td>prevsessionkeylifetime</td><td>&lt;Double></td><td>Read-write</td><td>This option sets the life time of symm key used to generate session tickets issued by NS in secs.<br>Default value: 0<br>Minimum value = 0<br>Maximum value = 1800</td></tr><tr><td>hsts</td><td>&lt;String></td><td>Read-write</td><td>State of TLSv1.0 protocol support for the SSL Virtual Server.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>maxage</td><td>&lt;Double></td><td>Read-write</td><td>Set max-age value for STS header.<br>Default value: 0<br>Minimum value = 0<br>Maximum value = 4294967294</td></tr><tr><td>includesubdomains</td><td>&lt;String></td><td>Read-write</td><td>Set include sub domain value for STS header.<br>Default value: NO<br>Possible values = YES, NO</td></tr><tr><td>skipclientcertpolicycheck</td><td>&lt;String></td><td>Read-write</td><td>This flag controls the processing of X509 certificate policies. If this option is Enabled, then the policy check in Client authentication will be skipped. This option can be used only when Client Authentication is Enabled and ClientCert is set to Mandatory.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>ciphername</td><td>&lt;String></td><td>Read-write</td><td>The cipher group/alias/individual cipher configuration.</td></tr><tr><td>cipherpriority</td><td>&lt;Double></td><td>Read-write</td><td>cipher priority.<br>Minimum value = 1</td></tr><tr><td>strictsigdigestcheck</td><td>&lt;String></td><td>Read-write</td><td>Parameter indicating to check whether peer entity certificate during TLS1.2 handshake is signed with one of signature-hash combination supported by Netscaler.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>nonfipsciphers</td><td>&lt;String></td><td>Read-only</td><td>State of usage of ciphers that are not FIPS approved. Valid only for an SSL service bound with a FIPS key and certificate.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>crlcheck</td><td>&lt;String></td><td>Read-only</td><td>The state of the CRL check parameter. (Mandatory/Optional).<br>Possible values = Mandatory, Optional</td></tr><tr><td>ocspcheck</td><td>&lt;String></td><td>Read-only</td><td>The state of the OCSP check parameter. (Mandatory/Optional).<br>Possible values = Mandatory, Optional</td></tr><tr><td>snicert</td><td>&lt;Boolean></td><td>Read-only</td><td>The name of the CertKey. Use this option to bind Certkey(s) which will be used in SNI processing.</td></tr><tr><td>skipcaname</td><td>&lt;Boolean></td><td>Read-only</td><td>The flag is used to indicate whether this<br>particular CA certificate's CA_Name needs to be sent to<br>the SSL client while requesting for client certificate<br>in a SSL handshake.</td></tr><tr><td>invoke</td><td>&lt;Boolean></td><td>Read-only</td><td>Invoke flag. This attribute is relevant only for ADVANCED policies.</td></tr><tr><td>labeltype</td><td>&lt;String></td><td>Read-only</td><td>Type of policy label invocation.<br>Possible values = vserver, service, policylabel</td></tr><tr><td>service</td><td>&lt;Double></td><td>Read-only</td><td>Service.</td></tr><tr><td>builtin</td><td>&lt;String[]></td><td>Read-only</td><td>Flag to determine whether ssl profile is built-in or not.<br>Possible values = MODIFIABLE, DELETABLE, IMMUTABLE, PARTITION_ALL</td></tr><tr><td>sslpfobjecttype</td><td>&lt;Double></td><td>Read-only</td><td>Internal flag to indicate what type of object binds this profile: monitor or service.</td></tr><tr><td>ssliverifyservercertforreuse</td><td>&lt;String></td><td>Read-only</td><td>Verify the origin server's certificate before reusing the front-end SSL session. Making it hidden since we always verify for now.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD]()| [DELETE](#d)| [UPDATE](#u)| [UNSET](#)| [GET (ALL)](#get-)| [GET]()| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslprofile
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"sslprofile":{<b>"name":<String_value>,</b>"sslprofiletype":<String_value>,"dhcount":<Double_value>,"dh":<String_value>,"dhfile":<String_value>,"ersa":<String_value>,"ersacount":<Double_value>,"sessreuse":<String_value>,"sesstimeout":<Double_value>,"cipherredirect":<String_value>,"cipherurl":<String_value>,"clientauth":<String_value>,"clientcert":<String_value>,"dhkeyexpsizelimit":<String_value>,"sslredirect":<String_value>,"redirectportrewrite":<String_value>,"ssl3":<String_value>,"tls1":<String_value>,"tls11":<String_value>,"tls12":<String_value>,"snienable":<String_value>,"ocspstapling":<String_value>,"serverauth":<String_value>,"commonname":<String_value>,"pushenctrigger":<String_value>,"sendclosenotify":<String_value>,"cleartextport":<Integer_value>,"insertionencoding":<String_value>,"denysslreneg":<String_value>,"quantumsize":<String_value>,"strictcachecks":<String_value>,"encrypttriggerpktcount":<Double_value>,"pushflag":<Double_value>,"dropreqwithnohostheader":<String_value>,"pushenctriggertimeout":<Double_value>,"ssltriggertimeout":<Double_value>,"clientauthuseboundcachain":<String_value>,"sslinterception":<String_value>,"sslireneg":<String_value>,"ssliocspcheck":<String_value>,"sslimaxsessperserver":<Double_value>,"sessionticket":<String_value>,"sessionticketlifetime":<Double_value>,"sessionticketkeyrefresh":<String_value>,"sessionticketkeydata":<String_value>,"sessionkeylifetime":<Double_value>,"prevsessionkeylifetime":<Double_value>,"hsts":<String_value>,"maxage":<Double_value>,"includesubdomains":<String_value>,"skipclientcertpolicycheck":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslprofile/name_value&lt;String&gt;
<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslprofile
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"sslprofile":{<b>"name":<String_value>,</b>"dh":<String_value>,"dhfile":<String_value>,"dhcount":<Double_value>,"dhkeyexpsizelimit":<String_value>,"ersa":<String_value>,"ersacount":<Double_value>,"sessreuse":<String_value>,"sesstimeout":<Double_value>,"cipherredirect":<String_value>,"cipherurl":<String_value>,"clientauth":<String_value>,"clientcert":<String_value>,"sslredirect":<String_value>,"redirectportrewrite":<String_value>,"ssl3":<String_value>,"tls1":<String_value>,"tls11":<String_value>,"tls12":<String_value>,"snienable":<String_value>,"ocspstapling":<String_value>,"serverauth":<String_value>,"commonname":<String_value>,"pushenctrigger":<String_value>,"sendclosenotify":<String_value>,"cleartextport":<Integer_value>,"insertionencoding":<String_value>,"denysslreneg":<String_value>,"quantumsize":<String_value>,"strictcachecks":<String_value>,"encrypttriggerpktcount":<Double_value>,"pushflag":<Double_value>,"dropreqwithnohostheader":<String_value>,"pushenctriggertimeout":<Double_value>,"ssltriggertimeout":<Double_value>,"clientauthuseboundcachain":<String_value>,"sslinterception":<String_value>,"sslireneg":<String_value>,"ssliocspcheck":<String_value>,"sslimaxsessperserver":<Double_value>,"hsts":<String_value>,"maxage":<Double_value>,"includesubdomains":<String_value>,"sessionticket":<String_value>,"sessionticketlifetime":<Double_value>,"sessionticketkeyrefresh":<String_value>,"sessionticketkeydata":<String_value>,"sessionkeylifetime":<Double_value>,"prevsessionkeylifetime":<Double_value>,"ciphername":<String_value>,"cipherpriority":<Double_value>,"strictsigdigestcheck":<String_value>,"skipclientcertpolicycheck":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslprofile?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"sslprofile":{<b>"name":<String_value>,</b>"dh":true,"dhfile":true,"dhcount":true,"dhkeyexpsizelimit":true,"ersa":true,"ersacount":true,"sessreuse":true,"sesstimeout":true,"cipherredirect":true,"cipherurl":true,"clientauth":true,"clientcert":true,"sslredirect":true,"redirectportrewrite":true,"ssl3":true,"tls1":true,"tls11":true,"tls12":true,"snienable":true,"ocspstapling":true,"serverauth":true,"commonname":true,"pushenctrigger":true,"sendclosenotify":true,"cleartextport":true,"insertionencoding":true,"denysslreneg":true,"quantumsize":true,"strictcachecks":true,"encrypttriggerpktcount":true,"pushflag":true,"dropreqwithnohostheader":true,"pushenctriggertimeout":true,"ssltriggertimeout":true,"clientauthuseboundcachain":true,"sslinterception":true,"sslireneg":true,"ssliocspcheck":true,"sslimaxsessperserver":true,"hsts":true,"maxage":true,"includesubdomains":true,"sessionticket":true,"sessionticketlifetime":true,"sessionticketkeyrefresh":true,"sessionticketkeydata":true,"sessionkeylifetime":true,"prevsessionkeylifetime":true,"ciphername":true,"cipherpriority":true,"strictsigdigestcheck":true,"skipclientcertpolicycheck":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslprofile
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslprofile?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslprofile?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of sslprofile resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslprofile?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslprofile?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the sslprofile resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "sslprofile": [ {"name":<String_value>,"dh":<String_value>,"dhfile":<String_value>,"dhcount":<Double_value>,"dhkeyexpsizelimit":<String_value>,"ersa":<String_value>,"ersacount":<Double_value>,"sessreuse":<String_value>,"sesstimeout":<Double_value>,"cipherredirect":<String_value>,"cipherurl":<String_value>,"clientauth":<String_value>,"clientcert":<String_value>,"sslredirect":<String_value>,"redirectportrewrite":<String_value>,"nonfipsciphers":<String_value>,"ssl3":<String_value>,"tls1":<String_value>,"tls11":<String_value>,"tls12":<String_value>,"snienable":<String_value>,"ocspstapling":<String_value>,"serverauth":<String_value>,"commonname":<String_value>,"pushenctrigger":<String_value>,"sendclosenotify":<String_value>,"cleartextport":<Integer_value>,"insertionencoding":<String_value>,"denysslreneg":<String_value>,"quantumsize":<String_value>,"strictcachecks":<String_value>,"encrypttriggerpktcount":<Double_value>,"pushflag":<Double_value>,"dropreqwithnohostheader":<String_value>,"pushenctriggertimeout":<Double_value>,"ssltriggertimeout":<Double_value>,"cipherpriority":<Double_value>,"ciphername":<String_value>,"crlcheck":<String_value>,"ocspcheck":<String_value>,"snicert":<Boolean_value>,"skipcaname":<Boolean_value>,"invoke":<Boolean_value>,"labeltype":<String_value>,"sslprofiletype":<String_value>,"clientauthuseboundcachain":<String_value>,"service":<Double_value>,"builtin":<String[]_value>,"sslpfobjecttype":<Double_value>,"sslinterception":<String_value>,"ssliverifyservercertforreuse":<String_value>,"sslireneg":<String_value>,"ssliocspcheck":<String_value>,"sslimaxsessperserver":<Double_value>,"sessionticket":<String_value>,"sessionticketlifetime":<Double_value>,"sessionticketkeyrefresh":<String_value>,"sessionticketkeydata":<String_value>,"sessionkeylifetime":<Double_value>,"prevsessionkeylifetime":<Double_value>,"hsts":<String_value>,"maxage":<Double_value>,"includesubdomains":<String_value>,"strictsigdigestcheck":<String_value>,"skipclientcertpolicycheck":<String_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslprofile/name_value&lt;String&gt;
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslprofile/name_value&lt;String&gt;?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslprofile/name_value&lt;String&gt;?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "sslprofile": [ {"name":<String_value>,"dh":<String_value>,"dhfile":<String_value>,"dhcount":<Double_value>,"dhkeyexpsizelimit":<String_value>,"ersa":<String_value>,"ersacount":<Double_value>,"sessreuse":<String_value>,"sesstimeout":<Double_value>,"cipherredirect":<String_value>,"cipherurl":<String_value>,"clientauth":<String_value>,"clientcert":<String_value>,"sslredirect":<String_value>,"redirectportrewrite":<String_value>,"nonfipsciphers":<String_value>,"ssl3":<String_value>,"tls1":<String_value>,"tls11":<String_value>,"tls12":<String_value>,"snienable":<String_value>,"ocspstapling":<String_value>,"serverauth":<String_value>,"commonname":<String_value>,"pushenctrigger":<String_value>,"sendclosenotify":<String_value>,"cleartextport":<Integer_value>,"insertionencoding":<String_value>,"denysslreneg":<String_value>,"quantumsize":<String_value>,"strictcachecks":<String_value>,"encrypttriggerpktcount":<Double_value>,"pushflag":<Double_value>,"dropreqwithnohostheader":<String_value>,"pushenctriggertimeout":<Double_value>,"ssltriggertimeout":<Double_value>,"cipherpriority":<Double_value>,"ciphername":<String_value>,"crlcheck":<String_value>,"ocspcheck":<String_value>,"snicert":<Boolean_value>,"skipcaname":<Boolean_value>,"invoke":<Boolean_value>,"labeltype":<String_value>,"sslprofiletype":<String_value>,"clientauthuseboundcachain":<String_value>,"service":<Double_value>,"builtin":<String[]_value>,"sslpfobjecttype":<Double_value>,"sslinterception":<String_value>,"ssliverifyservercertforreuse":<String_value>,"sslireneg":<String_value>,"ssliocspcheck":<String_value>,"sslimaxsessperserver":<Double_value>,"sessionticket":<String_value>,"sessionticketlifetime":<Double_value>,"sessionticketkeyrefresh":<String_value>,"sessionticketkeydata":<String_value>,"sessionkeylifetime":<Double_value>,"prevsessionkeylifetime":<Double_value>,"hsts":<String_value>,"maxage":<Double_value>,"includesubdomains":<String_value>,"strictsigdigestcheck":<String_value>,"skipclientcertpolicycheck":<String_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslprofile?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "sslprofile": [ { "__count": "#no"} ] }```



