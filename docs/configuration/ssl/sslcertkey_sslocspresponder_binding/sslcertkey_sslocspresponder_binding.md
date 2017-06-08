#sslcertkey_sslocspresponder_binding

Binding object showing the sslocspresponder that can be bound to sslcertkey.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>priority</td><td>&lt;Double></td><td>Read-write</td><td>ocsp priority.</td><tr><tr><td>crlcheck</td><td>&lt;String></td><td>Read-write</td><td>The rule for use of CRL corresponding to this CA certificate during client authentication. If crlCheck is set to Mandatory, the system will deny all SSL clients if the CRL is missing, expired - NextUpdate date is in the past, or is incomplete with remote CRL refresh enabled. If crlCheck is set to optional, the system will allow SSL clients in the above error cases.However, in any case if the client certificate is revoked in the CRL, the SSL client will be denied access.&lt;br>Default value: CRLCHECK_OPTIONAL&lt;br>Possible values = Mandatory, Optional</td><tr><tr><td>ca</td><td>&lt;Boolean></td><td>Read-write</td><td>If this option is specified, it indicates that the certificate-key pair being bound to the SSL virtual server is a CA certificate. If this option is not specified, the certificate-key pair is bound as a normal server certificate. Note: In case of a normal server certificate, the certificate-key pair should consist of both the certificate and the private-key.</td><tr><tr><td>certkey</td><td>&lt;String></td><td>Read-write</td><td>Name of the certificate-key pair.&lt;br>Minimum length = 1</td><tr><tr><td>ocspresponder</td><td>&lt;String></td><td>Read-write</td><td>OCSP responders bound to this certkey.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-write</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD:](#add:) | [DELETE:](#delete:) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add:



URL: http://NS_IP/nitro/v1/config
HTTP Method: PUT
Request Payload: ```{"params":{      "warning":<String_value>,      "onerror":<String_value>},sessionid":"##sessionid","sslcertkey_sslocspresponder_binding":{      "certkey":<String_value>,      "ocspresponder":<String_value>,                  "priority":<Double_value>,      "ca":<Boolean_value>,                  "crlcheck":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete:



URL: http://&lt;NS_IP&gt;/nitro/v1/config/sslcertkey_sslocspresponder_binding/certkey_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/sslcertkey_sslocspresponder_binding/certkey_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/sslcertkey_sslocspresponder_binding/certkey_value&lt;String&gt;
Query-parameters:
filter
http://&lt;NS_IP&gt;/nitro/v1/config/sslcertkey_sslocspresponder_binding/certkey_value&lt;String&gt;?filter=property-name1:property-value1,property-name2:property-value2
Use this query-parameter to get the filtered set of sslcertkey_sslocspresponder_binding resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/sslcertkey_sslocspresponder_binding/certkey_value&lt;String&gt;?pagesize=#no;pageno=#no
Use this query-parameter to get the sslcertkey_sslocspresponder_binding resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/sslcertkey_sslocspresponder_binding?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "sslcertkey_sslocspresponder_binding": [ {      "priority":<Double_value>,      "crlcheck":<String_value>,      "ca":<Boolean_value>,      "certkey":<String_value>,      "ocspresponder":<String_value>,}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/sslcertkey_sslocspresponder_binding/certkey_value&lt;String&gt;?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",sslcertkey_sslocspresponder_binding: [ { "__count": "#no"} ] }


