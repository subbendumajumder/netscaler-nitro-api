#sslservice

Configuration for SSL service resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>servicename</td><td>&lt;String></td><td>Read-write</td><td>Name of the SSL service.&lt;br>Minimum length = 1</td><tr><tr><td>dh</td><td>&lt;String></td><td>Read-write</td><td>State of Diffie-Hellman (DH) key exchange. This parameter is not applicable when configuring a backend service.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>dhfile</td><td>&lt;String></td><td>Read-write</td><td>Name for and, optionally, path to the PEM-format DH parameter file to be installed. /nsconfig/ssl/ is the default path. This parameter is not applicable when configuring a backend service.&lt;br>Minimum length = 1</td><tr><tr><td>dhcount</td><td>&lt;Double></td><td>Read-write</td><td>Number of interactions, between the client and the NetScaler appliance, after which the DH private-public pair is regenerated. A value of zero (0) specifies infinite use (no refresh). This parameter is not applicable when configuring a backend service.&lt;br>Minimum value = 0&lt;br>Maximum value = 65534</td><tr><tr><td>ersa</td><td>&lt;String></td><td>Read-write</td><td>State of Ephemeral RSA (eRSA) key exchange. Ephemeral RSA allows clients that support only export ciphers to communicate with the secure server even if the server certificate does not support export clients. The ephemeral RSA key is automatically generated when you bind an export cipher to an SSL or TCP-based SSL virtual server or service. When you remove the export cipher, the eRSA key is not deleted. It is reused at a later date when another export cipher is bound to an SSL or TCP-based SSL virtual server or service. The eRSA key is deleted when the appliance restarts. This parameter is not applicable when configuring a backend service.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>ersacount</td><td>&lt;Double></td><td>Read-write</td><td>Refresh count for regeneration of RSA public-key and private-key pair. Zero (0) specifies infinite usage (no refresh). This parameter is not applicable when configuring a backend service.&lt;br>Minimum value = 0&lt;br>Maximum value = 65534</td><tr><tr><td>sessreuse</td><td>&lt;String></td><td>Read-write</td><td>State of session reuse. Establishing the initial handshake requires CPU-intensive public key encryption operations. With the ENABLED setting, session key exchange is avoided for session resumption requests received from the client.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>sesstimeout</td><td>&lt;Double></td><td>Read-write</td><td>Time, in seconds, for which to keep the session active. Any session resumption request received after the timeout period will require a fresh SSL handshake and establishment of a new SSL session.&lt;br>Default value: 300&lt;br>Minimum value = 0&lt;br>Maximum value = 4294967294</td><tr><tr><td>cipherredirect</td><td>&lt;String></td><td>Read-write</td><td>State of Cipher Redirect. If this parameter is set to ENABLED, you can configure an SSL virtual server or service to display meaningful error messages if the SSL handshake fails because of a cipher mismatch between the virtual server or service and the client. This parameter is not applicable when configuring a backend service.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>cipherurl</td><td>&lt;String></td><td>Read-write</td><td>URL of the page to which to redirect the client in case of a cipher mismatch. Typically, this page has a clear explanation of the error or an alternative location that the transaction can continue from. This parameter is not applicable when configuring a backend service.</td><tr><tr><td>sslv2redirect</td><td>&lt;String></td><td>Read-write</td><td>State of SSLv2 Redirect. If this parameter is set to ENABLED, you can configure an SSL virtual server or service to display meaningful error messages if the SSL handshake fails because of a protocol version mismatch between the virtual server or service and the client. This parameter is not applicable when configuring a backend service.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>sslv2url</td><td>&lt;String></td><td>Read-write</td><td>URL of the page to which to redirect the client in case of a protocol version mismatch. Typically, this page has a clear explanation of the error or an alternative location that the transaction can continue from. This parameter is not applicable when configuring a backend service.</td><tr><tr><td>clientauth</td><td>&lt;String></td><td>Read-write</td><td>State of client authentication. In service-based SSL offload, the service terminates the SSL handshake if the SSL client does not provide a valid certificate. This parameter is not applicable when configuring a backend service.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>clientcert</td><td>&lt;String></td><td>Read-write</td><td>Type of client authentication. If this parameter is set to MANDATORY, the appliance terminates the SSL handshake if the SSL client does not provide a valid certificate. With the OPTIONAL setting, the appliance requests a certificate from the SSL clients but proceeds with the SSL transaction even if the client presents an invalid certificate. This parameter is not applicable when configuring a backend SSL service. Caution: Define proper access control policies before changing this setting to Optional.&lt;br>Possible values = Mandatory, Optional</td><tr><tr><td>sslredirect</td><td>&lt;String></td><td>Read-write</td><td>State of HTTPS redirects for the SSL service. For an SSL session, if the client browser receives a redirect message, the browser tries to connect to the new location. However, the secure SSL session breaks if the object has moved from a secure site (https://) to an unsecure site (http://). Typically, a warning message appears on the screen, prompting the user to continue or disconnect. If SSL Redirect is ENABLED, the redirect message is automatically converted from http:// to https:// and the SSL session does not break. This parameter is not applicable when configuring a backend service.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>redirectportrewrite</td><td>&lt;String></td><td>Read-write</td><td>State of the port rewrite while performing HTTPS redirect. If this parameter is set to ENABLED, and the URL from the server does not contain the standard port, the port is rewritten to the standard.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>nonfipsciphers</td><td>&lt;String></td><td>Read-write</td><td>State of usage of ciphers that are not FIPS approved. Valid only for an SSL service bound with a FIPS key and certificate.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>ssl2</td><td>&lt;String></td><td>Read-write</td><td>State of SSLv2 protocol support for the SSL service. This parameter is not applicable when configuring a backend service.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>ssl3</td><td>&lt;String></td><td>Read-write</td><td>State of SSLv3 protocol support for the SSL service.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>tls1</td><td>&lt;String></td><td>Read-write</td><td>State of TLSv1.0 protocol support for the SSL service.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>tls11</td><td>&lt;String></td><td>Read-write</td><td>State of TLSv1.1 protocol support for the SSL service.Enabled for Front-end service on MPX-CVM platform only.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>tls12</td><td>&lt;String></td><td>Read-write</td><td>State of TLSv1.2 protocol support for the SSL service.Enabled for Front-end service on MPX-CVM platform only.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>snienable</td><td>&lt;String></td><td>Read-write</td><td>State of the Server Name Indication (SNI) feature on the virtual server and service-based offload. SNI helps to enable SSL encryption on multiple domains on a single virtual server or service if the domains are controlled by the same organization and share the same second-level domain name. For example, *.sports.net can be used to secure domains such as login.sports.net and help.sports.net.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>serverauth</td><td>&lt;String></td><td>Read-write</td><td>State of server authentication support for the SSL service.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>commonname</td><td>&lt;String></td><td>Read-write</td><td>Name to be checked against the CommonName (CN) field in the server certificate bound to the SSL server.&lt;br>Minimum length = 1</td><tr><tr><td>pushenctrigger</td><td>&lt;String></td><td>Read-write</td><td>Trigger encryption on the basis of the PUSH flag value. Available settings function as follows: * ALWAYS - Any PUSH packet triggers encryption. * IGNORE - Ignore PUSH packet for triggering encryption. * MERGE - For a consecutive sequence of PUSH packets, the last PUSH packet triggers encryption. * TIMER - PUSH packet triggering encryption is delayed by the time defined in the set ssl parameter command or in the Change Advanced SSL Settings dialog box.&lt;br>Possible values = Always, Merge, Ignore, Timer</td><tr><tr><td>sendclosenotify</td><td>&lt;String></td><td>Read-write</td><td>Enable sending SSL Close-Notify at the end of a transaction.&lt;br>Default value: YES&lt;br>Possible values = YES, NO</td><tr><tr><td>dtlsprofilename</td><td>&lt;String></td><td>Read-write</td><td>Name of the DTLS profile whose settings are to be applied to the virtual server.&lt;br>Minimum length = 1&lt;br>Maximum length = 127</td><tr><tr><td>sslprofile</td><td>&lt;String></td><td>Read-write</td><td>SSL profile associated to service.&lt;br>Minimum length = 1&lt;br>Maximum length = 127</td><tr><tr><td>cipherdetails</td><td>&lt;Boolean></td><td>Read-write</td><td>Display details of the individual ciphers bound to the SSL service.</td><tr><tr><td>service</td><td>&lt;Double></td><td>Read-only</td><td>.</td><tr><tr><td>skipcaname</td><td>&lt;Boolean></td><td>Read-only</td><td>The flag is used to indicate whether this particular CA certificates CA_Name needs to be sent to the SSL client while requesting for client certificate in a SSL handshake.</td><tr><tr><td>dtlsflag</td><td>&lt;Boolean></td><td>Read-only</td><td>The flag is used to indicate whether DTLS is set or not.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
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
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","sslservice":{      "servicename":<String_value>,      "dh":<String_value>,                  "dhfile":<String_value>,      "dhcount":<Double_value>,      "ersa":<String_value>,                  "ersacount":<Double_value>,      "sessreuse":<String_value>,                  "sesstimeout":<Double_value>,      "cipherredirect":<String_value>,                  "cipherurl":<String_value>,      "sslv2redirect":<String_value>,                  "sslv2url":<String_value>,      "clientauth":<String_value>,                  "clientcert":<String_value>,      "sslredirect":<String_value>,      "redirectportrewrite":<String_value>,      "nonfipsciphers":<String_value>,      "ssl2":<String_value>,      "ssl3":<String_value>,      "tls1":<String_value>,      "tls11":<String_value>,      "tls12":<String_value>,      "snienable":<String_value>,      "serverauth":<String_value>,                  "commonname":<String_value>,      "pushenctrigger":<String_value>,      "sendclosenotify":<String_value>,      "dtlsprofilename":<String_value>,      "sslprofile":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","sslservice":{      "servicename":<String_value>,      "dh":true,      "dhfile":true,      "dhcount":true,      "ersa":true,      "ersacount":true,      "sessreuse":true,      "sesstimeout":true,      "cipherredirect":true,      "cipherurl":true,      "sslv2redirect":true,      "sslv2url":true,      "clientauth":true,      "clientcert":true,      "sslredirect":true,      "redirectportrewrite":true,      "nonfipsciphers":true,      "ssl2":true,      "ssl3":true,      "tls1":true,      "tls11":true,      "tls12":true,      "snienable":true,      "serverauth":true,      "commonname":true,      "sendclosenotify":true,      "dtlsprofilename":true,      "sslprofile":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/sslservice
Query-parameters:
args
http://&lt;NSIP&gt;/nitro/v1/config/sslservice?args=      "servicename":&lt;String_value&gt;,      "cipherdetails":&lt;Boolean_value&gt;,
Use this query-parameter to get sslservice resources based on additional properties.


filter
http://&lt;NSIP&gt;/nitro/v1/config/sslservice?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of sslservice resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/sslservice?view=summary
Use this query-parameter to get the summary output of sslservice resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/sslservice?pagesize=#no;pageno=#no
Use this query-parameter to get the sslservice resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/sslservice?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "sslservice": [ {      "servicename":<String_value>,      "cipherdetails":<Boolean_value>,      "dh":<String_value>,      "dhfile":<String_value>,      "dhcount":<Double_value>,      "ersa":<String_value>,      "ersacount":<Double_value>,      "sessreuse":<String_value>,      "sesstimeout":<Double_value>,      "cipherredirect":<String_value>,      "cipherurl":<String_value>,      "sslv2redirect":<String_value>,      "sslv2url":<String_value>,      "clientauth":<String_value>,      "clientcert":<String_value>,      "sslredirect":<String_value>,      "redirectportrewrite":<String_value>,      "nonfipsciphers":<String_value>,      "ssl2":<String_value>,      "ssl3":<String_value>,      "tls1":<String_value>,      "tls11":<String_value>,      "tls12":<String_value>,      "snienable":<String_value>,      "serverauth":<String_value>,      "commonname":<String_value>,      "service":<Double_value>,      "pushenctrigger":<String_value>,      "skipcaname":<Boolean_value>,      "sendclosenotify":<String_value>,      "dtlsprofilename":<String_value>,      "dtlsflag":<Boolean_value>,      "sslprofile":<String_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/sslservice/servicename_value&lt;String&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "sslservice": [ {      "servicename":<String_value>,      "cipherdetails":<Boolean_value>,      "dh":<String_value>,      "dhfile":<String_value>,      "dhcount":<Double_value>,      "ersa":<String_value>,      "ersacount":<Double_value>,      "sessreuse":<String_value>,      "sesstimeout":<Double_value>,      "cipherredirect":<String_value>,      "cipherurl":<String_value>,      "sslv2redirect":<String_value>,      "sslv2url":<String_value>,      "clientauth":<String_value>,      "clientcert":<String_value>,      "sslredirect":<String_value>,      "redirectportrewrite":<String_value>,      "nonfipsciphers":<String_value>,      "ssl2":<String_value>,      "ssl3":<String_value>,      "tls1":<String_value>,      "tls11":<String_value>,      "tls12":<String_value>,      "snienable":<String_value>,      "serverauth":<String_value>,      "commonname":<String_value>,      "service":<Double_value>,      "pushenctrigger":<String_value>,      "skipcaname":<Boolean_value>,      "sendclosenotify":<String_value>,      "dtlsprofilename":<String_value>,      "dtlsflag":<Boolean_value>,      "sslprofile":<String_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/sslservice?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",sslservice: [ { "__count": "#no"} ] }


