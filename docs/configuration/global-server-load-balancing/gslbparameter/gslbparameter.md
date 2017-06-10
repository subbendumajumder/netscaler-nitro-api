#gslbparameter

Configuration for GSLB parameter resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>ldnsentrytimeout</td><td>&lt;Double></td><td>Read-write</td><td>Time, in seconds, after which an inactive LDNS entry is removed.&lt;br>Default value: 180&lt;br>Minimum value = 30&lt;br>Maximum value = 65534</td><tr><tr><td>rtttolerance</td><td>&lt;Double></td><td>Read-write</td><td>Tolerance, in milliseconds, for newly learned round-trip time (RTT) values. If the difference between the old RTT value and the newly computed RTT value is less than or equal to the specified tolerance value, the LDNS entry in the network metric table is not updated with the new RTT value. Prevents the exchange of metrics when variations in RTT values are negligible.&lt;br>Default value: 5&lt;br>Minimum value = 1&lt;br>Maximum value = 100</td><tr><tr><td>ldnsmask</td><td>&lt;String></td><td>Read-write</td><td>The IPv4 network mask with which to create LDNS entries.&lt;br>Minimum length = 1</td><tr><tr><td>v6ldnsmasklen</td><td>&lt;Double></td><td>Read-write</td><td>Mask for creating LDNS entries for IPv6 source addresses. The mask is defined as the number of leading bits to consider, in the source IP address, when creating an LDNS entry.&lt;br>Default value: 128&lt;br>Minimum value = 1&lt;br>Maximum value = 128</td><tr><tr><td>ldnsprobeorder</td><td>&lt;String[]></td><td>Read-write</td><td>Order in which monitors should be initiated to calculate RTT.&lt;br>Possible values = PING, DNS, TCP</td><tr><tr><td>dropldnsreq</td><td>&lt;String></td><td>Read-write</td><td>Drop LDNS requests if round-trip time (RTT) information is not available.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>gslbsvcstatedelaytime</td><td>&lt;Double></td><td>Read-write</td><td>Amount of delay in updating the state of GSLB service to DOWN when MEP goes down.&lt;br> This parameter is applicable only if monitors are not bound to GSLB services.&lt;br>Default value: 0&lt;br>Minimum value = 0&lt;br>Maximum value = 3600</td><tr><tr><td>automaticconfigsync</td><td>&lt;String></td><td>Read-write</td><td>GSLB configuration will be synced automatically to remote gslb sites if enabled.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>flags</td><td>&lt;Double></td><td>Read-only</td><td>State of the GSLB parameter.</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[UPDATE](#update) | [UNSET](#unset) | [GET (ALL)](#get-(all))


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###update



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbparameter
HTTP Method: PUT
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"gslbparameter":{      "ldnsentrytimeout":<Double_value>,      "rtttolerance":<Double_value>,      "ldnsmask":<String_value>,      "v6ldnsmasklen":<Double_value>,      "ldnsprobeorder":<String[]_value>,      "dropldnsreq":<String_value>,      "gslbsvcstatedelaytime":<Double_value>,      "automaticconfigsync":<String_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbparameter?action=unset
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"gslbparameter":{      "ldnsentrytimeout":true,      "rtttolerance":true,      "ldnsmask":true,      "v6ldnsmasklen":true,      "ldnsprobeorder":true,      "dropldnsreq":true,      "gslbsvcstatedelaytime":true,      "automaticconfigsync":true}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbparameter
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "gslbparameter": [ {      "flags":<Double_value>,      "ldnsentrytimeout":<Double_value>,      "rtttolerance":<Double_value>,      "ldnsmask":<String_value>,      "v6ldnsmasklen":<Double_value>,      "ldnsprobeorder":<String[]_value>,      "dropldnsreq":<String_value>,      "gslbsvcstatedelaytime":<Double_value>,      "automaticconfigsync":<String_value>}]}```



