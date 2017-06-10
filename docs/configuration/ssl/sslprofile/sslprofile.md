#sslprofile

Configuration for SSL profile resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the SSL profile. Must begin with an ASCII alphanumeric or underscore (_) character, and must contain only ASCII alphanumeric, underscore, hash (#), period (.), space, colon (:), at (@), equals (=), and hyphen (-) characters. Cannot be changed after the profile is created.&lt;br>Minimum length = 1&lt;br>Maximum length = 127</td><tr><tr><td>sslprofiletype</td><td>&lt;String></td><td>Read-write</td><td>Type of profile. Front end profiles apply to the entity that receives requests from a client. Backend profiles apply to the entity that sends client requests to a server.&lt;br>Default value: FrontEnd&lt;br>Possible values = BackEnd, FrontEnd</td><tr><tr><td>dhcount</td><td>&lt;Double></td><td>Read-write</td><td>Number of interactions, between the client and the NetScaler appliance, after which the DH private-public pair is regenerated. A value of zero (0) specifies infinite use (no refresh).&lt;br>This parameter is not applicable when configuring a backend profile.&lt;br>Minimum value = 0&lt;br>Maximum value = 65534</td><tr><tr><td>dh</td><td>&lt;String></td><td>Read-write</td><td>State of Diffie-Hellman (DH) key exchange.&lt;br>This parameter is not applicable when configuring a backend profile.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>dhfile</td><td>&lt;String></td><td>Read-write</td><td>The file name and path for the DH parameter.&lt;br>Minimum length = 1</td><tr><tr><td>ersa</td><td>&lt;String></td><td>Read-write</td><td>State of Ephemeral RSA (eRSA) key exchange. Ephemeral RSA allows clients that support only export ciphers to communicate with the secure server even if the server certificate does not support export clients. The ephemeral RSA key is automatically generated when you bind an export cipher to an SSL or TCP-based SSL virtual server or service. When you remove the export cipher, the eRSA key is not deleted. It is reused at a later date when another export cipher is bound to an SSL or TCP-based SSL virtual server or service. The eRSA key is deleted when the appliance restarts.&lt;br>This parameter is not applicable when configuring a backend profile.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>ersacount</td><td>&lt;Double></td><td>Read-write</td><td>The refresh count for the re-generation of RSA public-key and private-key pair.&lt;br>Minimum value = 0&lt;br>Maximum value = 65534</td><tr><tr><td>sessreuse</td><td>&lt;String></td><td>Read-write</td><td>State of session reuse. Establishing the initial handshake requires CPU-intensive public key encryption operations. With the ENABLED setting, session key exchange is avoided for session resumption requests received from the client.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>sesstimeout</td><td>&lt;Double></td><td>Read-write</td><td>The Session timeout value in seconds.&lt;br>Minimum value = 0&lt;br>Maximum value = 4294967294</td><tr><tr><td>cipherredirect</td><td>&lt;String></td><td>Read-write</td><td>State of Cipher Redirect. If this parameter is set to ENABLED, you can configure an SSL virtual server or service to display meaningful error messages if the SSL handshake fails because of a cipher mismatch between the virtual server or service and the client.&lt;br>This parameter is not applicable when configuring a backend profile.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>cipherurl</td><td>&lt;String></td><td>Read-write</td><td>The redirect URL to be used with the Cipher Redirect feature.</td><tr><tr><td>clientauth</td><td>&lt;String></td><td>Read-write</td><td>State of client authentication. In service-based SSL offload, the service terminates the SSL handshake if the SSL client does not provide a valid certificate. &lt;br>This parameter is not applicable when configuring a backend profile.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>clientcert</td><td>&lt;String></td><td>Read-write</td><td>The rule for client certificate requirement in client authentication.&lt;br>Possible values = Mandatory, Optional</td><tr><tr><td>dhkeyexpsizelimit</td><td>&lt;String></td><td>Read-write</td><td>This option enables the use of NIST recommended (NIST Special Publication 800-56A) bit size for private-key size. For example, for DH params of size 2048bit, the private-key size recommended is 224bits. This is rounded-up to 256bits.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>sslredirect</td><td>&lt;String></td><td>Read-write</td><td>State of HTTPS redirects for the SSL service. &lt;br>For an SSL session, if the client browser receives a redirect message, the browser tries to connect to the new location. However, the secure SSL session breaks if the object has moved from a secure site (https://) to an unsecure site (http://). Typically, a warning message appears on the screen, prompting the user to continue or disconnect.&lt;br>If SSL Redirect is ENABLED, the redirect message is automatically converted from http:// to https:// and the SSL session does not break.&lt;br>This parameter is not applicable when configuring a backend profile.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>redirectportrewrite</td><td>&lt;String></td><td>Read-write</td><td>State of the port rewrite while performing HTTPS redirect. If this parameter is set to ENABLED, and the URL from the server does not contain the standard port, the port is rewritten to the standard.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>ssl3</td><td>&lt;String></td><td>Read-write</td><td>State of SSLv3 protocol support for the SSL profile.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>tls1</td><td>&lt;String></td><td>Read-write</td><td>State of TLSv1.0 protocol support for the SSL profile.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>tls11</td><td>&lt;String></td><td>Read-write</td><td>State of TLSv1.1 protocol support for the SSL profile.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>tls12</td><td>&lt;String></td><td>Read-write</td><td>State of TLSv1.2 protocol support for the SSL profile.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>snienable</td><td>&lt;String></td><td>Read-write</td><td>State of the Server Name Indication (SNI) feature on the virtual server and service-based offload. SNI helps to enable SSL encryption on multiple domains on a single virtual server or service if the domains are controlled by the same organization and share the same second-level domain name. For example, *.sports.net can be used to secure domains such as login.sports.net and help.sports.net.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>ocspstapling</td><td>&lt;String></td><td>Read-write</td><td>State of OCSP stapling support on the SSL virtual server. Supported only if the protocol used is higher than SSLv3. Possible values:&lt;br>ENABLED: The appliance sends a request to the OCSP responder to check the status of the server certificate and caches the response for the specified time. If the response is valid at the time of SSL handshake with the client, the OCSP-based server certificate status is sent to the client during the handshake.&lt;br>DISABLED: The appliance does not check the status of the server certificate. .&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>serverauth</td><td>&lt;String></td><td>Read-write</td><td>State of server authentication support for the SSL Backend profile.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>commonname</td><td>&lt;String></td><td>Read-write</td><td>Name to be checked against the CommonName (CN) field in the server certificate bound to the SSL server.&lt;br>Minimum length = 1</td><tr><tr><td>pushenctrigger</td><td>&lt;String></td><td>Read-write</td><td>Trigger encryption on the basis of the PUSH flag value. Available settings function as follows:&lt;br>* ALWAYS - Any PUSH packet triggers encryption.&lt;br>* IGNORE - Ignore PUSH packet for triggering encryption.&lt;br>* MERGE - For a consecutive sequence of PUSH packets, the last PUSH packet triggers encryption.&lt;br>* TIMER - PUSH packet triggering encryption is delayed by the time defined in the set ssl parameter command or in the Change Advanced SSL Settings dialog box.&lt;br>Possible values = Always, Merge, Ignore, Timer</td><tr><tr><td>sendclosenotify</td><td>&lt;String></td><td>Read-write</td><td>Enable sending SSL Close-Notify at the end of a transaction.&lt;br>Default value: YES&lt;br>Possible values = YES, NO</td><tr><tr><td>cleartextport</td><td>&lt;Integer></td><td>Read-write</td><td>Port on which clear-text data is sent by the appliance to the server. Do not specify this parameter for SSL offloading with end-to-end encryption.&lt;br>Range 1 - 65535&lt;br>* in CLI is represented as 65535 in NITRO API</td><tr><tr><td>insertionencoding</td><td>&lt;String></td><td>Read-write</td><td>Encoding method used to insert the subject or issuers name in HTTP requests to servers.&lt;br>Default value: Unicode&lt;br>Possible values = Unicode, UTF-8</td><tr><tr><td>denysslreneg</td><td>&lt;String></td><td>Read-write</td><td>Deny renegotiation in specified circumstances. Available settings function as follows:&lt;br>* NO - Allow SSL renegotiation.&lt;br>* FRONTEND_CLIENT - Deny secure and nonsecure SSL renegotiation initiated by the client.&lt;br>* FRONTEND_CLIENTSERVER - Deny secure and nonsecure SSL renegotiation initiated by the client or the NetScaler during policy-based client authentication. &lt;br>* ALL - Deny all secure and nonsecure SSL renegotiation.&lt;br>* NONSECURE - Deny nonsecure SSL renegotiation. Allows only clients that support RFC 5746.&lt;br>Default value: ALL&lt;br>Possible values = NO, FRONTEND_CLIENT, FRONTEND_CLIENTSERVER, ALL, NONSECURE</td><tr><tr><td>quantumsize</td><td>&lt;String></td><td>Read-write</td><td>Amount of data to collect before the data is pushed to the crypto hardware for encryption. For large downloads, a larger quantum size better utilizes the crypto resources.&lt;br>Default value: 8192&lt;br>Possible values = 4096, 8192, 16384</td><tr><tr><td>strictcachecks</td><td>&lt;String></td><td>Read-write</td><td>Enable strict CA certificate checks on the appliance.&lt;br>Default value: NO&lt;br>Possible values = YES, NO</td><tr><tr><td>encrypttriggerpktcount</td><td>&lt;Double></td><td>Read-write</td><td>Maximum number of queued packets after which encryption is triggered. Use this setting for SSL transactions that send small packets from server to NetScaler.&lt;br>Default value: 45&lt;br>Minimum value = 10&lt;br>Maximum value = 50</td><tr><tr><td>pushflag</td><td>&lt;Double></td><td>Read-write</td><td>Insert PUSH flag into decrypted, encrypted, or all records. If the PUSH flag is set to a value other than 0, the buffered records are forwarded on the basis of the value of the PUSH flag. Available settings function as follows:&lt;br>0 - Auto (PUSH flag is not set.)&lt;br>1 - Insert PUSH flag into every decrypted record.&lt;br>2 -Insert PUSH flag into every encrypted record.&lt;br>3 - Insert PUSH flag into every decrypted and encrypted record.&lt;br>Minimum value = 0&lt;br>Maximum value = 3</td><tr><tr><td>dropreqwithnohostheader</td><td>&lt;String></td><td>Read-write</td><td>Host header check for SNI enabled sessions. If this check is enabled and the HTTP request does not contain the host header for SNI enabled sessions, the request is dropped.&lt;br>Default value: NO&lt;br>Possible values = YES, NO</td><tr><tr><td>pushenctriggertimeout</td><td>&lt;Double></td><td>Read-write</td><td>PUSH encryption trigger timeout value. The timeout value is applied only if you set the Push Encryption Trigger parameter to Timer in the SSL virtual server settings.&lt;br>Default value: 1&lt;br>Minimum value = 1&lt;br>Maximum value = 200</td><tr><tr><td>ssltriggertimeout</td><td>&lt;Double></td><td>Read-write</td><td>Time, in milliseconds, after which encryption is triggered for transactions that are not tracked on the NetScaler appliance because their length is not known. There can be a delay of up to 10ms from the specified timeout value before the packet is pushed into the queue.&lt;br>Default value: 100&lt;br>Minimum value = 1&lt;br>Maximum value = 200</td><tr><tr><td>clientauthuseboundcachain</td><td>&lt;String></td><td>Read-write</td><td>Certficates bound on the VIP are used for validating the client cert. Certficates came along with client cert are not used for validating the client cert.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>sessionticket</td><td>&lt;String></td><td>Read-write</td><td>This option enables the use of session tickets, as per the RFC 5077.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>sessionticketlifetime</td><td>&lt;Double></td><td>Read-write</td><td>This option sets the life time of session tickets issued by NS in secs.&lt;br>Default value: 300&lt;br>Minimum value = 0&lt;br>Maximum value = 172800</td><tr><tr><td>hsts</td><td>&lt;String></td><td>Read-write</td><td>State of TLSv1.0 protocol support for the SSL Virtual Server.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>maxage</td><td>&lt;Double></td><td>Read-write</td><td>Set max-age value for STS header.&lt;br>Default value: 0&lt;br>Minimum value = 0&lt;br>Maximum value = 4294967294</td><tr><tr><td>includesubdomains</td><td>&lt;String></td><td>Read-write</td><td>Set include sub domain value for STS header.&lt;br>Default value: NO&lt;br>Possible values = YES, NO</td><tr><tr><td>ciphername</td><td>&lt;String></td><td>Read-write</td><td>The cipher group/alias/individual cipher configuration.</td><tr><tr><td>cipherpriority</td><td>&lt;Double></td><td>Read-write</td><td>cipher priority.&lt;br>Minimum value = 1</td><tr><tr><td>strictsigdigestcheck</td><td>&lt;String></td><td>Read-write</td><td>Parameter indicating to check whether peer entity certificate during TLS1.2 handshake is signed with one of signature-hash combination supported by Netscaler.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>nonfipsciphers</td><td>&lt;String></td><td>Read-only</td><td>State of usage of ciphers that are not FIPS approved. Valid only for an SSL service bound with a FIPS key and certificate.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>crlcheck</td><td>&lt;String></td><td>Read-only</td><td>The state of the CRL check parameter. (Mandatory/Optional).&lt;br>Possible values = Mandatory, Optional</td><tr><tr><td>ocspcheck</td><td>&lt;String></td><td>Read-only</td><td>The state of the OCSP check parameter. (Mandatory/Optional).&lt;br>Possible values = Mandatory, Optional</td><tr><tr><td>snicert</td><td>&lt;Boolean></td><td>Read-only</td><td>The name of the CertKey. Use this option to bind Certkey(s) which will be used in SNI processing.</td><tr><tr><td>skipcaname</td><td>&lt;Boolean></td><td>Read-only</td><td>The flag is used to indicate whether this&lt;br> particular CA certificates CA_Name needs to be sent to&lt;br> the SSL client while requesting for client certificate&lt;br> in a SSL handshake.</td><tr><tr><td>invoke</td><td>&lt;Boolean></td><td>Read-only</td><td>Invoke flag. This attribute is relevant only for ADVANCED policies.</td><tr><tr><td>labeltype</td><td>&lt;String></td><td>Read-only</td><td>Type of policy label invocation.&lt;br>Possible values = vserver, service, policylabel</td><tr><tr><td>service</td><td>&lt;Double></td><td>Read-only</td><td>Service.</td><tr><tr><td>builtin</td><td>&lt;String[]></td><td>Read-only</td><td>Flag to determine whether ssl profile is built-in or not.&lt;br>Possible values = MODIFIABLE, DELETABLE, IMMUTABLE, PARTITION_ALL</td><tr><tr><td>sslpfobjecttype</td><td>&lt;Double></td><td>Read-only</td><td>Internal flag to indicate what type of object binds this profile: monitor or service.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [DELETE](#delete) | [UPDATE](#update) | [UNSET](#unset) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslprofile
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"sslprofile":{      "name":<String_value>,      "sslprofiletype":<String_value>,      "dhcount":<Double_value>,      "dh":<String_value>,      "dhfile":<String_value>,      "ersa":<String_value>,      "ersacount":<Double_value>,      "sessreuse":<String_value>,      "sesstimeout":<Double_value>,      "cipherredirect":<String_value>,      "cipherurl":<String_value>,      "clientauth":<String_value>,      "clientcert":<String_value>,      "dhkeyexpsizelimit":<String_value>,      "sslredirect":<String_value>,      "redirectportrewrite":<String_value>,      "ssl3":<String_value>,      "tls1":<String_value>,      "tls11":<String_value>,      "tls12":<String_value>,      "snienable":<String_value>,      "ocspstapling":<String_value>,      "serverauth":<String_value>,      "commonname":<String_value>,      "pushenctrigger":<String_value>,      "sendclosenotify":<String_value>,      "cleartextport":<Integer_value>,      "insertionencoding":<String_value>,      "denysslreneg":<String_value>,      "quantumsize":<String_value>,      "strictcachecks":<String_value>,      "encrypttriggerpktcount":<Double_value>,      "pushflag":<Double_value>,      "dropreqwithnohostheader":<String_value>,      "pushenctriggertimeout":<Double_value>,      "ssltriggertimeout":<Double_value>,      "clientauthuseboundcachain":<String_value>,      "sessionticket":<String_value>,      "sessionticketlifetime":<Double_value>,      "hsts":<String_value>,      "maxage":<Double_value>,      "includesubdomains":<String_value>}}```
Response:
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslprofile/name_value&lt;String&gt;
HTTP Method: DELETE
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslprofile
HTTP Method: PUT
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"sslprofile":{      "name":<String_value>,      "dh":<String_value>,      "dhfile":<String_value>,      "dhcount":<Double_value>,      "dhkeyexpsizelimit":<String_value>,      "ersa":<String_value>,      "ersacount":<Double_value>,      "sessreuse":<String_value>,      "sesstimeout":<Double_value>,      "cipherredirect":<String_value>,      "cipherurl":<String_value>,      "clientauth":<String_value>,      "clientcert":<String_value>,      "sslredirect":<String_value>,      "redirectportrewrite":<String_value>,      "ssl3":<String_value>,      "tls1":<String_value>,      "tls11":<String_value>,      "tls12":<String_value>,      "snienable":<String_value>,      "ocspstapling":<String_value>,      "serverauth":<String_value>,      "commonname":<String_value>,      "pushenctrigger":<String_value>,      "sendclosenotify":<String_value>,      "cleartextport":<Integer_value>,      "insertionencoding":<String_value>,      "denysslreneg":<String_value>,      "quantumsize":<String_value>,      "strictcachecks":<String_value>,      "encrypttriggerpktcount":<Double_value>,      "pushflag":<Double_value>,      "dropreqwithnohostheader":<String_value>,      "pushenctriggertimeout":<Double_value>,      "ssltriggertimeout":<Double_value>,      "clientauthuseboundcachain":<String_value>,      "hsts":<String_value>,      "maxage":<Double_value>,      "includesubdomains":<String_value>,      "sessionticket":<String_value>,      "sessionticketlifetime":<Double_value>,      "ciphername":<String_value>,      "cipherpriority":<Double_value>,      "strictsigdigestcheck":<String_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslprofile?action=unset
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"sslprofile":{      "name":<String_value>,      "dh":true,      "dhfile":true,      "dhcount":true,      "dhkeyexpsizelimit":true,      "ersa":true,      "ersacount":true,      "sessreuse":true,      "sesstimeout":true,      "cipherredirect":true,      "cipherurl":true,      "clientauth":true,      "clientcert":true,      "sslredirect":true,      "redirectportrewrite":true,      "ssl3":true,      "tls1":true,      "tls11":true,      "tls12":true,      "snienable":true,      "ocspstapling":true,      "serverauth":true,      "commonname":true,      "pushenctrigger":true,      "sendclosenotify":true,      "cleartextport":true,      "insertionencoding":true,      "denysslreneg":true,      "quantumsize":true,      "strictcachecks":true,      "encrypttriggerpktcount":true,      "pushflag":true,      "dropreqwithnohostheader":true,      "pushenctriggertimeout":true,      "ssltriggertimeout":true,      "clientauthuseboundcachain":true,      "hsts":true,      "maxage":true,      "includesubdomains":true,      "sessionticket":true,      "sessionticketlifetime":true,      "ciphername":true,      "cipherpriority":true,      "strictsigdigestcheck":true}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslprofile
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslprofile?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


filter
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslprofile?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of sslprofile resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslprofile?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).


pagination
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslprofile?pagesize=#no;pageno=#no
Use this query-parameter to get the sslprofile resources in chunks.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "sslprofile": [ {      "name":<String_value>,      "dh":<String_value>,      "dhfile":<String_value>,      "dhcount":<Double_value>,      "dhkeyexpsizelimit":<String_value>,      "ersa":<String_value>,      "ersacount":<Double_value>,      "sessreuse":<String_value>,      "sesstimeout":<Double_value>,      "cipherredirect":<String_value>,      "cipherurl":<String_value>,      "clientauth":<String_value>,      "clientcert":<String_value>,      "sslredirect":<String_value>,      "redirectportrewrite":<String_value>,      "nonfipsciphers":<String_value>,      "ssl3":<String_value>,      "tls1":<String_value>,      "tls11":<String_value>,      "tls12":<String_value>,      "snienable":<String_value>,      "ocspstapling":<String_value>,      "serverauth":<String_value>,      "commonname":<String_value>,      "pushenctrigger":<String_value>,      "sendclosenotify":<String_value>,      "cleartextport":<Integer_value>,      "insertionencoding":<String_value>,      "denysslreneg":<String_value>,      "quantumsize":<String_value>,      "strictcachecks":<String_value>,      "encrypttriggerpktcount":<Double_value>,      "pushflag":<Double_value>,      "dropreqwithnohostheader":<String_value>,      "pushenctriggertimeout":<Double_value>,      "ssltriggertimeout":<Double_value>,      "cipherpriority":<Double_value>,      "ciphername":<String_value>,      "crlcheck":<String_value>,      "ocspcheck":<String_value>,      "snicert":<Boolean_value>,      "skipcaname":<Boolean_value>,      "invoke":<Boolean_value>,      "labeltype":<String_value>,      "sslprofiletype":<String_value>,      "clientauthuseboundcachain":<String_value>,      "service":<Double_value>,      "builtin":<String[]_value>,      "sslpfobjecttype":<Double_value>,      "sessionticket":<String_value>,      "sessionticketlifetime":<Double_value>,      "hsts":<String_value>,      "maxage":<Double_value>,      "includesubdomains":<String_value>,      "strictsigdigestcheck":<String_value>}]}```



###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslprofile/name_value&lt;String&gt;
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslprofile/name_value&lt;String&gt;?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslprofile/name_value&lt;String&gt;?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "sslprofile": [ {      "name":<String_value>,      "dh":<String_value>,      "dhfile":<String_value>,      "dhcount":<Double_value>,      "dhkeyexpsizelimit":<String_value>,      "ersa":<String_value>,      "ersacount":<Double_value>,      "sessreuse":<String_value>,      "sesstimeout":<Double_value>,      "cipherredirect":<String_value>,      "cipherurl":<String_value>,      "clientauth":<String_value>,      "clientcert":<String_value>,      "sslredirect":<String_value>,      "redirectportrewrite":<String_value>,      "nonfipsciphers":<String_value>,      "ssl3":<String_value>,      "tls1":<String_value>,      "tls11":<String_value>,      "tls12":<String_value>,      "snienable":<String_value>,      "ocspstapling":<String_value>,      "serverauth":<String_value>,      "commonname":<String_value>,      "pushenctrigger":<String_value>,      "sendclosenotify":<String_value>,      "cleartextport":<Integer_value>,      "insertionencoding":<String_value>,      "denysslreneg":<String_value>,      "quantumsize":<String_value>,      "strictcachecks":<String_value>,      "encrypttriggerpktcount":<Double_value>,      "pushflag":<Double_value>,      "dropreqwithnohostheader":<String_value>,      "pushenctriggertimeout":<Double_value>,      "ssltriggertimeout":<Double_value>,      "cipherpriority":<Double_value>,      "ciphername":<String_value>,      "crlcheck":<String_value>,      "ocspcheck":<String_value>,      "snicert":<Boolean_value>,      "skipcaname":<Boolean_value>,      "invoke":<Boolean_value>,      "labeltype":<String_value>,      "sslprofiletype":<String_value>,      "clientauthuseboundcachain":<String_value>,      "service":<Double_value>,      "builtin":<String[]_value>,      "sslpfobjecttype":<Double_value>,      "sessionticket":<String_value>,      "sessionticketlifetime":<Double_value>,      "hsts":<String_value>,      "maxage":<Double_value>,      "includesubdomains":<String_value>,      "strictsigdigestcheck":<String_value>}]}```



###count



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslprofile?count=yes
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: 
{ "sslprofile": [ { "__count": "#no"} ] }


