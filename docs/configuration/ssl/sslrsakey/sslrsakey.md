#sslrsakey

Configuration for RSA key resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>keyfile</td><td>&lt;String></td><td>Read-write</td><td>Name for and, optionally, path to the RSA key file. /nsconfig/ssl/ is the default path.&lt;br>Maximum length = 63</td><tr><tr><td>bits</td><td>&lt;Double></td><td>Read-write</td><td>Size, in bits, of the RSA key.&lt;br>Minimum value = 512&lt;br>Maximum value = 4096</td><tr><tr><td>exponent</td><td>&lt;String></td><td>Read-write</td><td>Public exponent for the RSA key. The exponent is part of the cipher algorithm and is required for creating the RSA key.&lt;br>Default value: F4&lt;br>Possible values = 3, F4</td><tr><tr><td>keyform</td><td>&lt;String></td><td>Read-write</td><td>Format in which the RSA key file is stored on the appliance.&lt;br>Default value: PEM&lt;br>Possible values = DER, PEM</td><tr><tr><td>des</td><td>&lt;Boolean></td><td>Read-write</td><td>Encrypt the generated RSA key by using the DES algorithm. On the command line, you are prompted to enter the pass phrase (password) that is used to encrypt the key.</td><tr><tr><td>des3</td><td>&lt;Boolean></td><td>Read-write</td><td>Encrypt the generated RSA key by using the Triple-DES algorithm. On the command line, you are prompted to enter the pass phrase (password) that is used to encrypt the key.</td><tr><tr><td>password</td><td>&lt;String></td><td>Read-write</td><td>Pass phrase to use for encryption if DES or DES3 option is selected.&lt;br>Minimum length = 1&lt;br>Maximum length = 31</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[CREATE](#create)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###create



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslrsakey?action=create
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"sslrsakey":{      "keyfile":<String_value>,      "bits":<Double_value>,      "exponent":<String_value>,      "keyform":<String_value>,      "des":<Boolean_value>,      "des3":<Boolean_value>,      "password":<String_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


