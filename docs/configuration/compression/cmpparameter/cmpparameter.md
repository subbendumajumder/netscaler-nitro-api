#cmpparameter

Configuration for CMP parameter resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>cmplevel</td><td>&lt;String></td><td>Read-write</td><td>Specify a compression level. Available settings function as follows: * Optimal - Corresponds to a gzip GZIP level of 5-7. * Best speed - Corresponds to a gzip level of 1. * Best compression - Corresponds to a gzip level of 9.&lt;br>Default value: optimal&lt;br>Possible values = optimal, bestspeed, bestcompression</td><tr><tr><td>quantumsize</td><td>&lt;Double></td><td>Read-write</td><td>Minimum quantum of data to be filled before compression begins.&lt;br>Default value: 57344&lt;br>Minimum value = 8&lt;br>Maximum value = 63488</td><tr><tr><td>servercmp</td><td>&lt;String></td><td>Read-write</td><td>Allow the server to send compressed data to the NetScaler appliance. With the default setting, the NetScaler appliance handles all compression.&lt;br>Default value: ON&lt;br>Possible values = ON, OFF</td><tr><tr><td>heurexpiry</td><td>&lt;String></td><td>Read-write</td><td>Heuristic basefile expiry.&lt;br>Default value: OFF&lt;br>Possible values = ON, OFF</td><tr><tr><td>heurexpirythres</td><td>&lt;Double></td><td>Read-write</td><td>Threshold compression ratio for heuristic basefile expiry, multiplied by 100. For example, to set the threshold ratio to 1.25, specify 125.&lt;br>Default value: 100&lt;br>Minimum value = 1&lt;br>Maximum value = 1000</td><tr><tr><td>heurexpiryhistwt</td><td>&lt;Double></td><td>Read-write</td><td>For heuristic basefile expiry, weightage to be given to historical delta compression ratio, specified as percentage. For example, to give 25% weightage to historical ratio (and therefore 75% weightage to the ratio for current delta compression transaction), specify 25.&lt;br>Default value: 50&lt;br>Minimum value = 1&lt;br>Maximum value = 100</td><tr><tr><td>minressize</td><td>&lt;Double></td><td>Read-write</td><td>Smallest response size, in bytes, to be compressed.</td><tr><tr><td>cmpbypasspct</td><td>&lt;Double></td><td>Read-write</td><td>NetScaler CPU threshold after which compression is not performed. Range: 0 - 100.&lt;br>Default value: 100&lt;br>Minimum value = 0&lt;br>Maximum value = 100</td><tr><tr><td>cmponpush</td><td>&lt;String></td><td>Read-write</td><td>NetScaler appliance does not wait for the quantum to be filled before starting to compress data. Upon receipt of a packet with a PUSH flag, the appliance immediately begins compression of the accumulated packets.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>policytype</td><td>&lt;String></td><td>Read-write</td><td>Type of policy. Available settings function as follows: * Classic - Classic policies evaluate basic characteristics of traffic and other data. * Advanced - Advanced policies (which have been renamed as default syntax policies) can perform the same type of evaluations as classic policies. They also enable you to analyze more data (for example, the body of an HTTP request) and to configure more operations in the policy rule (for example, transforming data in the body of a request into an HTTP header).&lt;br>Default value: CLASSIC&lt;br>Possible values = CLASSIC, ADVANCED</td><tr><tr><td>addvaryheader</td><td>&lt;String></td><td>Read-write</td><td>Control insertion of the Vary header in HTTP responses compressed by NetScaler. Intermediate caches store different versions of the response for different values of the headers present in the Vary response header.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>varyheadervalue</td><td>&lt;String></td><td>Read-write</td><td>The value of the HTTP Vary header for compressed responses. If this argument is not specified, a default value of "Accept-Encoding" will be used.&lt;br>Minimum length = 1</td><tr><tr><td>externalcache</td><td>&lt;String></td><td>Read-write</td><td>Enable insertion of Cache-Control: private response directive to indicate response message is intended for a single user and must not be cached by a shared or proxy cache.&lt;br>Default value: NO&lt;br>Possible values = YES, NO</td><tr><tr><td>builtin</td><td>&lt;String[]></td><td>Read-only</td><td>Flag to determine whether compression is default or not.&lt;br>Possible values = MODIFIABLE, DELETABLE, IMMUTABLE, PARTITION_ALL</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[UPDATE](#update) | [UNSET](#unset) | [GET (ALL)](#get-(all))


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","cmpparameter":{      "cmplevel":<String_value>,      "quantumsize":<Double_value>,      "servercmp":<String_value>,      "heurexpiry":<String_value>,      "heurexpirythres":<Double_value>,      "heurexpiryhistwt":<Double_value>,      "minressize":<Double_value>,      "cmpbypasspct":<Double_value>,      "cmponpush":<String_value>,      "policytype":<String_value>,      "addvaryheader":<String_value>,                  "varyheadervalue":<String_value>,      "externalcache":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","cmpparameter":{      "cmplevel":true,      "quantumsize":true,      "servercmp":true,      "heurexpiry":true,      "heurexpirythres":true,      "heurexpiryhistwt":true,      "minressize":true,      "cmpbypasspct":true,      "cmponpush":true,      "policytype":true,      "addvaryheader":true,      "varyheadervalue":true,      "externalcache":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/cmpparameter
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "cmpparameter": [ {      "cmplevel":<String_value>,      "quantumsize":<Double_value>,      "servercmp":<String_value>,      "heurexpiry":<String_value>,      "heurexpirythres":<Double_value>,      "heurexpiryhistwt":<Double_value>,      "minressize":<Double_value>,      "cmpbypasspct":<Double_value>,      "cmponpush":<String_value>,      "policytype":<String_value>,      "addvaryheader":<String_value>,      "varyheadervalue":<String_value>,      "externalcache":<String_value>,      "builtin":<String[]_value>}]}```



