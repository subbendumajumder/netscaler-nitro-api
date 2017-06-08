#sslcertkey

Configuration for certificate key resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>certkey</td><td>&lt;String></td><td>Read-write</td><td>Name for the certificate and private-key pair. Must begin with an ASCII alphanumeric or underscore (_) character, and must contain only ASCII alphanumeric, underscore, hash (#), period (.), space, colon (:), at (@), equals (=), and hyphen (-) characters. Cannot be changed after the certificate-key pair is created. The following requirement applies only to the NetScaler CLI: If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my cert" or my cert).&lt;br>Minimum length = 1</td><tr><tr><td>cert</td><td>&lt;String></td><td>Read-write</td><td>Name of and, optionally, path to the X509 certificate file that is used to form the certificate-key pair. The certificate file should be present on the appliances hard-disk drive or solid-state drive. Storing a certificate in any location other than the default might cause inconsistency in a high availability setup. /nsconfig/ssl/ is the default path.&lt;br>Minimum length = 1</td><tr><tr><td>key</td><td>&lt;String></td><td>Read-write</td><td>Name of and, optionally, path to the private-key file that is used to form the certificate-key pair. The certificate file should be present on the appliances hard-disk drive or solid-state drive. Storing a certificate in any location other than the default might cause inconsistency in a high availability setup. /nsconfig/ssl/ is the default path.&lt;br>Minimum length = 1</td><tr><tr><td>password</td><td>&lt;Boolean></td><td>Read-write</td><td>Passphrase that was used to encrypt the private-key. Use this option to load encrypted private-keys in PEM format.</td><tr><tr><td>fipskey</td><td>&lt;String></td><td>Read-write</td><td>Name of the FIPS key that was created inside the Hardware Security Module (HSM) of a FIPS appliance, or a key that was imported into the HSM.&lt;br>Minimum length = 1</td><tr><tr><td>inform</td><td>&lt;String></td><td>Read-write</td><td>Input format of the certificate and the private-key files. The two formats supported by the appliance are: PEM - Privacy Enhanced Mail DER - Distinguished Encoding Rule.&lt;br>Default value: PEM&lt;br>Possible values = DER, PEM</td><tr><tr><td>passplain</td><td>&lt;String></td><td>Read-write</td><td>Pass phrase used to encrypt the private-key. Required when adding an encrypted private-key in PEM format.&lt;br>Minimum length = 1</td><tr><tr><td>expirymonitor</td><td>&lt;String></td><td>Read-write</td><td>Issue an alert when the certificate is about to expire.&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>notificationperiod</td><td>&lt;Double></td><td>Read-write</td><td>Time, in number of days, before certificate expiration, at which to generate an alert that the certificate is about to expire.&lt;br>Minimum value = 10&lt;br>Maximum value = 100</td><tr><tr><td>bundle</td><td>&lt;String></td><td>Read-write</td><td>Parse the certificate chain as a single file after linking the server certificate to its issuers certificate within the file.&lt;br>Default value: NO&lt;br>Possible values = YES, NO</td><tr><tr><td>linkcertkeyname</td><td>&lt;String></td><td>Read-write</td><td>Name of the Certificate Authority certificate-key pair to which to link a certificate-key pair.&lt;br>Minimum length = 1</td><tr><tr><td>nodomaincheck</td><td>&lt;Boolean></td><td>Read-write</td><td>Override the check for matching domain names during a certificate update operation.</td><tr><tr><td>signaturealg</td><td>&lt;String></td><td>Read-only</td><td>Signature algorithm.</td><tr><tr><td>serial</td><td>&lt;String></td><td>Read-only</td><td>Serial number.</td><tr><tr><td>issuer</td><td>&lt;String></td><td>Read-only</td><td>Issuer name.</td><tr><tr><td>clientcertnotbefore</td><td>&lt;String></td><td>Read-only</td><td>Not-Before date.</td><tr><tr><td>clientcertnotafter</td><td>&lt;String></td><td>Read-only</td><td>Not-After date.</td><tr><tr><td>daystoexpiration</td><td>&lt;Integer></td><td>Read-only</td><td>Days remaining for the certificate to expire.</td><tr><tr><td>subject</td><td>&lt;String></td><td>Read-only</td><td>Subject name.</td><tr><tr><td>publickey</td><td>&lt;String></td><td>Read-only</td><td>Public key algorithm.</td><tr><tr><td>publickeysize</td><td>&lt;Integer></td><td>Read-only</td><td>Size of the public key.</td><tr><tr><td>version</td><td>&lt;Integer></td><td>Read-only</td><td>Version.</td><tr><tr><td>priority</td><td>&lt;Double></td><td>Read-only</td><td>ocsp priority.</td><tr><tr><td>status</td><td>&lt;String></td><td>Read-only</td><td>Status of the certificate.&lt;br>Possible values = Valid, Not yet valid, Expired</td><tr><tr><td>passcrypt</td><td>&lt;String></td><td>Read-only</td><td>Passcrypt.&lt;br>Minimum length = 1</td><tr><tr><td>data</td><td>&lt;Double></td><td>Read-only</td><td>Vserver Id.</td><tr><tr><td>servicename</td><td>&lt;String></td><td>Read-only</td><td>Service name to which the certificate key pair is bound.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [DELETE](#delete) | [UPDATE](#update) | [UNSET](#unset) | [LINK](#link) | [UNLINK](#unlink) | [CHANGE](#change) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>},"sessionid":"##sessionid","sslcertkey":{      "certkey":<String_value>,      "cert":<String_value>,      "key":<String_value>,                  "password":<Boolean_value>,      "fipskey":<String_value>,      "inform":<String_value>,      "passplain":<String_value>,      "expirymonitor":<String_value>,      "notificationperiod":<Double_value>,      "bundle":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/sslcertkey/certkey_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/sslcertkey/certkey_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","sslcertkey":{      "certkey":<String_value>,      "expirymonitor":<String_value>,                  "notificationperiod":<Double_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","sslcertkey":{      "certkey":<String_value>,      "expirymonitor":true,      "notificationperiod":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###link



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"link"},"sessionid":"##sessionid","sslcertkey":{      "certkey":<String_value>,      "linkcertkeyname":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unlink



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unlink"},"sessionid":"##sessionid","sslcertkey":{      "certkey":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###change



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"update"},"sessionid":"##sessionid","sslcertkey":{      "certkey":<String_value>,      "cert":<String_value>,      "key":<String_value>,                  "password":<Boolean_value>,      "fipskey":<String_value>,      "inform":<String_value>,      "passplain":<String_value>,      "nodomaincheck":<Boolean_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/sslcertkey
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/sslcertkey?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of sslcertkey resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/sslcertkey?view=summary
Use this query-parameter to get the summary output of sslcertkey resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/sslcertkey?pagesize=#no;pageno=#no
Use this query-parameter to get the sslcertkey resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/sslcertkey?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "sslcertkey": [ {      "certkey":<String_value>,      "cert":<String_value>,      "key":<String_value>,      "inform":<String_value>,      "signaturealg":<String_value>,      "serial":<String_value>,      "issuer":<String_value>,      "clientcertnotbefore":<String_value>,      "clientcertnotafter":<String_value>,      "daystoexpiration":<Integer_value>,      "subject":<String_value>,      "publickey":<String_value>,      "publickeysize":<Integer_value>,      "version":<Integer_value>,      "priority":<Double_value>,      "status":<String_value>,      "fipskey":<String_value>,      "passcrypt":<String_value>,      "data":<Double_value>,      "servicename":<String_value>,      "expirymonitor":<String_value>,      "notificationperiod":<Double_value>,      "linkcertkeyname":<String_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/sslcertkey/certkey_value&lt;String&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "sslcertkey": [ {      "certkey":<String_value>,      "cert":<String_value>,      "key":<String_value>,      "inform":<String_value>,      "signaturealg":<String_value>,      "serial":<String_value>,      "issuer":<String_value>,      "clientcertnotbefore":<String_value>,      "clientcertnotafter":<String_value>,      "daystoexpiration":<Integer_value>,      "subject":<String_value>,      "publickey":<String_value>,      "publickeysize":<Integer_value>,      "version":<Integer_value>,      "priority":<Double_value>,      "status":<String_value>,      "fipskey":<String_value>,      "passcrypt":<String_value>,      "data":<Double_value>,      "servicename":<String_value>,      "expirymonitor":<String_value>,      "notificationperiod":<Double_value>,      "linkcertkeyname":<String_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/sslcertkey?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",sslcertkey: [ { "__count": "#no"} ] }


