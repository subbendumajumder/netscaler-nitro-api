#sslservicegroup

Configuration for SSL service group resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>servicegroupname</td><td>&lt;String></td><td>Read-write</td><td>Name of the SSL service group for which to set advanced configuration.&lt;br>Minimum length = 1</td><tr><tr><td>sslprofile</td><td>&lt;String></td><td>Read-write</td><td>Name of the SSL profile that contains SSL settings for the Service Group.&lt;br>Minimum length = 1&lt;br>Maximum length = 127</td><tr><tr><td>sessreuse</td><td>&lt;String></td><td>Read-write</td><td>State of session reuse. Establishing the initial handshake requires CPU-intensive public key encryption operations. With the ENABLED setting, session key exchange is avoided for session resumption requests received from the client.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>sesstimeout</td><td>&lt;Double></td><td>Read-write</td><td>Time, in seconds, for which to keep the session active. Any session resumption request received after the timeout period will require a fresh SSL handshake and establishment of a new SSL session.&lt;br>Default value: 300&lt;br>Minimum value = 0&lt;br>Maximum value = 4294967294</td><tr><tr><td>nonfipsciphers</td><td>&lt;String></td><td>Read-write</td><td>State of usage of ciphers that are not FIPS approved. Valid only for an SSL service bound with a FIPS key and certificate.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>ssl3</td><td>&lt;String></td><td>Read-write</td><td>State of SSLv3 protocol support for the SSL service group.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>tls1</td><td>&lt;String></td><td>Read-write</td><td>State of TLSv1.0 protocol support for the SSL service group.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>tls11</td><td>&lt;String></td><td>Read-write</td><td>State of TLSv1.1 protocol support for the SSL service group.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>tls12</td><td>&lt;String></td><td>Read-write</td><td>State of TLSv1.2 protocol support for the SSL service group.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>serverauth</td><td>&lt;String></td><td>Read-write</td><td>State of server authentication support for the SSL service group.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>commonname</td><td>&lt;String></td><td>Read-write</td><td>Name to be checked against the CommonName (CN) field in the server certificate bound to the SSL server.&lt;br>Minimum length = 1</td><tr><tr><td>sendclosenotify</td><td>&lt;String></td><td>Read-write</td><td>Enable sending SSL Close-Notify at the end of a transaction.&lt;br>Default value: YES&lt;br>Possible values = YES, NO</td><tr><tr><td>cipherdetails</td><td>&lt;Boolean></td><td>Read-write</td><td>Display details of the individual ciphers bound to the SSL service group.</td><tr><tr><td>dh</td><td>&lt;String></td><td>Read-only</td><td>The state of DH key exchange support for the SSL service group.&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>dhfile</td><td>&lt;String></td><td>Read-only</td><td>The file name and path for the DH parameter.</td><tr><tr><td>dhcount</td><td>&lt;Double></td><td>Read-only</td><td>The refresh count for the re-generation of DH public-key and private-key from the DH parameter.</td><tr><tr><td>dhkeyexpsizelimit</td><td>&lt;String></td><td>Read-only</td><td>This option enables the use of NIST recommended (NIST Special Publication 800-56A) bit size for private-key size. For example, for DH params of size 2048bit, the private-key size recommended is 224bits. This is rounded-up to 256bits.&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>ersa</td><td>&lt;String></td><td>Read-only</td><td>The state of Ephemeral RSA key exchange support for the SSL service group.Ephemeral RSA is used for export ciphers.&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>ersacount</td><td>&lt;Double></td><td>Read-only</td><td>The refresh count for the re-generation of RSA public-key and private-key pair.</td><tr><tr><td>cipherredirect</td><td>&lt;String></td><td>Read-only</td><td>The state of Cipher Redirect feature. Cipher Redirect feature can be used to provide more readable information to SSL clients about mismatch in ciphers between the client and the SSL vserver.&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>cipherurl</td><td>&lt;String></td><td>Read-only</td><td>The redirect URL to be used with the Cipher Redirect feature.</td><tr><tr><td>sslv2redirect</td><td>&lt;String></td><td>Read-only</td><td>The state of SSLv2 Redirect feature.SSLv2 Redirect feature can be used to provide more readable information to SSL client about non-support of SSLv2 protocol on the SSL vserver.&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>sslv2url</td><td>&lt;String></td><td>Read-only</td><td>The redirect URL to be used with SSLv2 Redirect feature.</td><tr><tr><td>clientauth</td><td>&lt;String></td><td>Read-only</td><td>The state of Client-Authentication support for the SSL service group.&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>clientcert</td><td>&lt;String></td><td>Read-only</td><td>The rule for client certificate requirement in client authentication.&lt;br>Possible values = Mandatory, Optional</td><tr><tr><td>sslredirect</td><td>&lt;String></td><td>Read-only</td><td>The state of HTTPS redirects for the SSL service group. This is required for the proper functioning of the redirect messages from the server. The redirect message from the server provides the new location for the moved object. This is contained in the HTTP header field: Location, e.g. Location: http://www.moved.org/here.html For the SSL session, if the client browser receives this message, the browser will try to connect to the new location. This will break the secure SSL session, as the object has moved from a secure site (https://) to an un-secure one (http://). Generally browsers flash a warning message on the screen and prompt the user, either to continue or disconnect. The above feature, when enabled will automatically convert all such http:// redirect message to https://. This will not break the client SSL session. Note: The set ssl service command can be used for configuring a front-end SSL service for service based SSL Off-Loading, or a backend SSL service for backend-encryption setup.&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>redirectportrewrite</td><td>&lt;String></td><td>Read-only</td><td>The state of port-rewrite feature.&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>ssl2</td><td>&lt;String></td><td>Read-only</td><td>The state of SSLv2 protocol support for the SSL service group.&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>ocspcheck</td><td>&lt;String></td><td>Read-only</td><td>The state of the OCSP check parameter. (Mandatory/Optional).&lt;br>Possible values = Mandatory, Optional</td><tr><tr><td>crlcheck</td><td>&lt;String></td><td>Read-only</td><td>The state of the CRL check parameter. (Mandatory/Optional).&lt;br>Possible values = Mandatory, Optional</td><tr><tr><td>cleartextport</td><td>&lt;Integer></td><td>Read-only</td><td>The port on the back-end web-servers where the clear-text data is sent by system. Use this setting for the wildcard IP based SSL Acceleration configuration (*:443).&lt;br>Range 1 - 65535</td><tr><tr><td>servicename</td><td>&lt;String></td><td>Read-only</td><td>The service name.</td><tr><tr><td>ca</td><td>&lt;Boolean></td><td>Read-only</td><td>CA certificate.</td><tr><tr><td>snicert</td><td>&lt;Boolean></td><td>Read-only</td><td>The name of the CertKey. Use this option to bind Certkey(s) which will be used in SNI processing.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[UPDATE](#update) | [UNSET](#unset) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","sslservicegroup":{      "servicegroupname":<String_value>,      "sslprofile":<String_value>,      "sessreuse":<String_value>,                  "sesstimeout":<Double_value>,      "nonfipsciphers":<String_value>,      "ssl3":<String_value>,      "tls1":<String_value>,      "tls11":<String_value>,      "tls12":<String_value>,      "serverauth":<String_value>,                  "commonname":<String_value>,      "sendclosenotify":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","sslservicegroup":{      "servicegroupname":<String_value>,      "sslprofile":true,      "sessreuse":true,      "sesstimeout":true,      "nonfipsciphers":true,      "ssl3":true,      "tls1":true,      "tls11":true,      "tls12":true,      "serverauth":true,      "commonname":true,      "sendclosenotify":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/sslservicegroup
Query-parameters:
args
http://&lt;NSIP&gt;/nitro/v1/config/sslservicegroup?args=      "servicegroupname":&lt;String_value&gt;,      "cipherdetails":&lt;Boolean_value&gt;,
Use this query-parameter to get sslservicegroup resources based on additional properties.


filter
http://&lt;NSIP&gt;/nitro/v1/config/sslservicegroup?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of sslservicegroup resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/sslservicegroup?view=summary
Use this query-parameter to get the summary output of sslservicegroup resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/sslservicegroup?pagesize=#no;pageno=#no
Use this query-parameter to get the sslservicegroup resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/sslservicegroup?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "sslservicegroup": [ {      "servicegroupname":<String_value>,      "cipherdetails":<Boolean_value>,      "dh":<String_value>,      "dhfile":<String_value>,      "dhcount":<Double_value>,      "dhkeyexpsizelimit":<String_value>,      "ersa":<String_value>,      "ersacount":<Double_value>,      "sessreuse":<String_value>,      "sesstimeout":<Double_value>,      "cipherredirect":<String_value>,      "cipherurl":<String_value>,      "sslv2redirect":<String_value>,      "sslv2url":<String_value>,      "clientauth":<String_value>,      "clientcert":<String_value>,      "sslredirect":<String_value>,      "redirectportrewrite":<String_value>,      "nonfipsciphers":<String_value>,      "ssl2":<String_value>,      "ssl3":<String_value>,      "tls1":<String_value>,      "tls11":<String_value>,      "tls12":<String_value>,      "serverauth":<String_value>,      "commonname":<String_value>,      "ocspcheck":<String_value>,      "crlcheck":<String_value>,      "cleartextport":<Integer_value>,      "servicename":<String_value>,      "ca":<Boolean_value>,      "snicert":<Boolean_value>,      "sendclosenotify":<String_value>,      "sslprofile":<String_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/sslservicegroup/servicegroupname_value&lt;String&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "sslservicegroup": [ {      "servicegroupname":<String_value>,      "cipherdetails":<Boolean_value>,      "dh":<String_value>,      "dhfile":<String_value>,      "dhcount":<Double_value>,      "dhkeyexpsizelimit":<String_value>,      "ersa":<String_value>,      "ersacount":<Double_value>,      "sessreuse":<String_value>,      "sesstimeout":<Double_value>,      "cipherredirect":<String_value>,      "cipherurl":<String_value>,      "sslv2redirect":<String_value>,      "sslv2url":<String_value>,      "clientauth":<String_value>,      "clientcert":<String_value>,      "sslredirect":<String_value>,      "redirectportrewrite":<String_value>,      "nonfipsciphers":<String_value>,      "ssl2":<String_value>,      "ssl3":<String_value>,      "tls1":<String_value>,      "tls11":<String_value>,      "tls12":<String_value>,      "serverauth":<String_value>,      "commonname":<String_value>,      "ocspcheck":<String_value>,      "crlcheck":<String_value>,      "cleartextport":<Integer_value>,      "servicename":<String_value>,      "ca":<Boolean_value>,      "snicert":<Boolean_value>,      "sendclosenotify":<String_value>,      "sslprofile":<String_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/sslservicegroup?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",sslservicegroup: [ { "__count": "#no"} ] }


