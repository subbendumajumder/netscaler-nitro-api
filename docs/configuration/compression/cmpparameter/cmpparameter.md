#cmpparameter

Configuration for CMP parameter resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>cmplevel</td><td>&lt;String></td><td>Read-write</td><td>Specify a compression level. Available settings function as follows:<br>* Optimal - Corresponds to a gzip GZIP level of 5-7.<br>* Best speed - Corresponds to a gzip level of 1.<br>* Best compression - Corresponds to a gzip level of 9.<br>Default value: optimal<br>Possible values = optimal, bestspeed, bestcompression</td></tr><tr><td>quantumsize</td><td>&lt;Double></td><td>Read-write</td><td>Minimum quantum of data to be filled before compression begins.<br>Default value: 57344<br>Minimum value = 8<br>Maximum value = 63488</td></tr><tr><td>servercmp</td><td>&lt;String></td><td>Read-write</td><td>Allow the server to send compressed data to the NetScaler appliance. With the default setting, the NetScaler appliance handles all compression.<br>Default value: ON<br>Possible values = ON, OFF</td></tr><tr><td>heurexpiry</td><td>&lt;String></td><td>Read-write</td><td>Heuristic basefile expiry.<br>Default value: OFF<br>Possible values = ON, OFF</td></tr><tr><td>heurexpirythres</td><td>&lt;Double></td><td>Read-write</td><td>Threshold compression ratio for heuristic basefile expiry, multiplied by 100. For example, to set the threshold ratio to 1.25, specify 125.<br>Default value: 100<br>Minimum value = 1<br>Maximum value = 1000</td></tr><tr><td>heurexpiryhistwt</td><td>&lt;Double></td><td>Read-write</td><td>For heuristic basefile expiry, weightage to be given to historical delta compression ratio, specified as percentage. For example, to give 25% weightage to historical ratio (and therefore 75% weightage to the ratio for current delta compression transaction), specify 25.<br>Default value: 50<br>Minimum value = 1<br>Maximum value = 100</td></tr><tr><td>minressize</td><td>&lt;Double></td><td>Read-write</td><td>Smallest response size, in bytes, to be compressed.</td></tr><tr><td>cmpbypasspct</td><td>&lt;Double></td><td>Read-write</td><td>NetScaler CPU threshold after which compression is not performed. Range: 0 - 100.<br>Default value: 100<br>Minimum value = 0<br>Maximum value = 100</td></tr><tr><td>cmponpush</td><td>&lt;String></td><td>Read-write</td><td>NetScaler appliance does not wait for the quantum to be filled before starting to compress data. Upon receipt of a packet with a PUSH flag, the appliance immediately begins compression of the accumulated packets.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>policytype</td><td>&lt;String></td><td>Read-write</td><td>Type of policy. Available settings function as follows:<br>* Classic - Classic policies evaluate basic characteristics of traffic and other data.<br>* Advanced - Advanced policies (which have been renamed as default syntax policies) can perform the same type of evaluations as classic policies. They also enable you to analyze more data (for example, the body of an HTTP request) and to configure more operations in the policy rule (for example, transforming data in the body of a request into an HTTP header).<br>Possible values = CLASSIC, ADVANCED</td></tr><tr><td>addvaryheader</td><td>&lt;String></td><td>Read-write</td><td>Control insertion of the Vary header in HTTP responses compressed by NetScaler. Intermediate caches store different versions of the response for different values of the headers present in the Vary response header.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>varyheadervalue</td><td>&lt;String></td><td>Read-write</td><td>The value of the HTTP Vary header for compressed responses. If this argument is not specified, a default value of "Accept-Encoding" will be used.<br>Minimum length = 1</td></tr><tr><td>externalcache</td><td>&lt;String></td><td>Read-write</td><td>Enable insertion of Cache-Control: private response directive to indicate response message is intended for a single user and must not be cached by a shared or proxy cache.<br>Default value: NO<br>Possible values = YES, NO</td></tr><tr><td>builtin</td><td>&lt;String[]></td><td>Read-only</td><td>Flag to determine whether compression is default or not.<br>Possible values = MODIFIABLE, DELETABLE, IMMUTABLE, PARTITION_ALL</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[UPDATE](#u)| [UNSET](#)| [GET (ALL)](#get-)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/cmpparameter
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"cmpparameter":{"cmplevel":<String_value>,"quantumsize":<Double_value>,"servercmp":<String_value>,"heurexpiry":<String_value>,"heurexpirythres":<Double_value>,"heurexpiryhistwt":<Double_value>,"minressize":<Double_value>,"cmpbypasspct":<Double_value>,"cmponpush":<String_value>,"policytype":<String_value>,"addvaryheader":<String_value>,"varyheadervalue":<String_value>,"externalcache":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/cmpparameter?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"cmpparameter":{"policytype":true,"cmplevel":true,"quantumsize":true,"servercmp":true,"heurexpiry":true,"heurexpirythres":true,"heurexpiryhistwt":true,"minressize":true,"cmpbypasspct":true,"cmponpush":true,"addvaryheader":true,"varyheadervalue":true,"externalcache":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/cmpparameter
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "cmpparameter": [ {"cmplevel":<String_value>,"quantumsize":<Double_value>,"servercmp":<String_value>,"heurexpiry":<String_value>,"heurexpirythres":<Double_value>,"heurexpiryhistwt":<Double_value>,"minressize":<Double_value>,"cmpbypasspct":<Double_value>,"cmponpush":<String_value>,"policytype":<String_value>,"addvaryheader":<String_value>,"varyheadervalue":<String_value>,"externalcache":<String_value>,"builtin":<String[]_value>}]}```



