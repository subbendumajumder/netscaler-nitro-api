#sslfipskey

Configuration for FIPS key resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>fipskeyname</td><td>&lt;String></td><td>Read-write</td><td>Name for the FIPS key. Must begin with an ASCII alphanumeric or underscore (_) character, and must contain only ASCII alphanumeric, underscore, hash (#), period (.), space, colon (:), at (@), equals (=), and hyphen (-) characters. Cannot be changed after the FIPS key is created. The following requirement applies only to the NetScaler CLI: If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my fipskey" or my fipskey).&lt;br>Minimum length = 1</td><tr><tr><td>modulus</td><td>&lt;Double></td><td>Read-write</td><td>Modulus, in multiples of 64, of the FIPS key to be created.&lt;br>Minimum value = 0&lt;br>Maximum value = 4096</td><tr><tr><td>exponent</td><td>&lt;String></td><td>Read-write</td><td>Exponent value for the FIPS key to be created. Available values function as follows: 3=3 (hexadecimal) F4=10001 (hexadecimal).&lt;br>Default value: 3&lt;br>Possible values = 3, F4</td><tr><tr><td>key</td><td>&lt;String></td><td>Read-write</td><td>Name of and, optionally, path to the key file to be imported. /nsconfig/ssl/ is the default path.&lt;br>Minimum length = 1</td><tr><tr><td>inform</td><td>&lt;String></td><td>Read-write</td><td>Input format of the key file. Available formats are: SIM - Secure Information Management; select when importing a FIPS key. If the external FIPS key is encrypted, first decrypt it, and then import it. PEM - Privacy Enhanced Mail; select when importing a non-FIPS key. &lt;br>Default value: SIM&lt;br>Possible values = SIM, DER, PEM</td><tr><tr><td>wrapkeyname</td><td>&lt;String></td><td>Read-write</td><td>Name of the wrap key to use for importing the key. Required for importing a non-FIPS key.&lt;br>Minimum length = 1</td><tr><tr><td>iv</td><td>&lt;String></td><td>Read-write</td><td>Initialization Vector (IV) to use for importing the key. Required for importing a non-FIPS key.&lt;br>Minimum length = 1</td><tr><tr><td>size</td><td>&lt;Double></td><td>Read-only</td><td>Size.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[CREATE](#create) | [DELETE](#delete) | [IMPORT](#import) | [EXPORT](#export) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###create



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"create"},"sessionid":"##sessionid","sslfipskey":{      "fipskeyname":<String_value>,      "modulus":<Double_value>,      "exponent":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/sslfipskey/fipskeyname_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/sslfipskey/fipskeyname_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###Import



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"Import"},"sessionid":"##sessionid","sslfipskey":{      "fipskeyname":<String_value>,      "key":<String_value>,      "inform":<String_value>,      "wrapkeyname":<String_value>,      "iv":<String_value>,      "exponent":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###export



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"export"},"sessionid":"##sessionid","sslfipskey":{      "fipskeyname":<String_value>,      "key":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/sslfipskey
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/sslfipskey?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of sslfipskey resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/sslfipskey?view=summary
Use this query-parameter to get the summary output of sslfipskey resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/sslfipskey?pagesize=#no;pageno=#no
Use this query-parameter to get the sslfipskey resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/sslfipskey?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "sslfipskey": [ {      "fipskeyname":<String_value>,      "modulus":<Double_value>,      "exponent":<String_value>,      "size":<Double_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/sslfipskey/fipskeyname_value&lt;String&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "sslfipskey": [ {      "fipskeyname":<String_value>,      "modulus":<Double_value>,      "exponent":<String_value>,      "size":<Double_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/sslfipskey?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",sslfipskey: [ { "__count": "#no"} ] }


