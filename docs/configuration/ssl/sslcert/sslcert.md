#sslcert

Configuration for cerificate resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>certfile</td><td>&lt;String></td><td>Read-write</td><td>Name for and, optionally, path to the generated certificate file. /nsconfig/ssl/ is the default path.&lt;br>Maximum length = 63</td><tr><tr><td>reqfile</td><td>&lt;String></td><td>Read-write</td><td>Name for and, optionally, path to the certificate-signing request (CSR). /nsconfig/ssl/ is the default path.&lt;br>Maximum length = 63</td><tr><tr><td>certtype</td><td>&lt;String></td><td>Read-write</td><td>Type of certificate to generate. Specify one of the following: * ROOT_CERT - Self-signed Root-CA certificate. You must specify the key file name. The generated Root-CA certificate can be used for signing end-user client or server certificates or to create Intermediate-CA certificates. * INTM_CERT - Intermediate-CA certificate. * CLNT_CERT - End-user client certificate used for client authentication. * SRVR_CERT - SSL server certificate used on SSL servers for end-to-end encryption.&lt;br>Possible values = ROOT_CERT, INTM_CERT, CLNT_CERT, SRVR_CERT</td><tr><tr><td>keyfile</td><td>&lt;String></td><td>Read-write</td><td>Name for and, optionally, path to the private key. You can either use an existing RSA or DSA key that you own or create a new private key on the NetScaler appliance. This file is required only when creating a self-signed Root-CA certificate. The key file is stored in the /nsconfig/ssl directory by default. If the input key specified is an encrypted key, you are prompted to enter the PEM pass phrase that was used for encrypting the key.&lt;br>Maximum length = 63</td><tr><tr><td>keyform</td><td>&lt;String></td><td>Read-write</td><td>Format in which the key is stored on the appliance.&lt;br>Default value: PEM&lt;br>Possible values = DER, PEM</td><tr><tr><td>pempassphrase</td><td>&lt;String></td><td>Read-write</td><td>.&lt;br>Minimum length = 1&lt;br>Maximum length = 31</td><tr><tr><td>days</td><td>&lt;Double></td><td>Read-write</td><td>Number of days for which the certificate will be valid, beginning with the time and day (system time) of creation.&lt;br>Default value: 365&lt;br>Minimum value = 1&lt;br>Maximum value = 3650</td><tr><tr><td>certform</td><td>&lt;String></td><td>Read-write</td><td>Format in which the certificate is stored on the appliance.&lt;br>Default value: PEM&lt;br>Possible values = DER, PEM</td><tr><tr><td>cacert</td><td>&lt;String></td><td>Read-write</td><td>Name of the CA certificate file that issues and signs the Intermediate-CA certificate or the end-user client and server certificates.&lt;br>Maximum length = 63</td><tr><tr><td>cacertform</td><td>&lt;String></td><td>Read-write</td><td>Format of the CA certificate.&lt;br>Default value: PEM&lt;br>Possible values = DER, PEM</td><tr><tr><td>cakey</td><td>&lt;String></td><td>Read-write</td><td>Private key, associated with the CA certificate that is used to sign the Intermediate-CA certificate or the end-user client and server certificate. If the CA key file is password protected, the user is prompted to enter the pass phrase that was used to encrypt the key.&lt;br>Maximum length = 63</td><tr><tr><td>cakeyform</td><td>&lt;String></td><td>Read-write</td><td>Format for the CA certificate.&lt;br>Default value: PEM&lt;br>Possible values = DER, PEM</td><tr><tr><td>caserial</td><td>&lt;String></td><td>Read-write</td><td>Serial number file maintained for the CA certificate. This file contains the serial number of the next certificate to be issued or signed by the CA. If the specified file does not exist, a new file is created, with /nsconfig/ssl/ as the default path. If you do not specify a proper path for the existing serial file, a new serial file is created. This might change the certificate serial numbers assigned by the CA certificate to each of the certificates it signs.&lt;br>Maximum length = 63</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[CREATE](#create)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###create



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"create"},"sessionid":"##sessionid","sslcert":{      "certfile":<String_value>,      "reqfile":<String_value>,      "certtype":<String_value>,      "keyfile":<String_value>,      "keyform":<String_value>,      "pempassphrase":<String_value>,      "days":<Double_value>,      "certform":<String_value>,      "cacert":<String_value>,      "cacertform":<String_value>,      "cakey":<String_value>,      "cakeyform":<String_value>,      "caserial":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


