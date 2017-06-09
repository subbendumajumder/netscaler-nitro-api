#nshardware

Configuration for hardware resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>hwdescription</td><td>&lt;String></td><td>Read-only</td><td>Hardware and its ports detail.</td><tr><tr><td>sysid</td><td>&lt;Double></td><td>Read-only</td><td>System id.</td><tr><tr><td>manufactureday</td><td>&lt;Integer></td><td>Read-only</td><td>Manufacturing day.</td><tr><tr><td>manufacturemonth</td><td>&lt;Integer></td><td>Read-only</td><td>Manufacturing month.</td><tr><tr><td>manufactureyear</td><td>&lt;Integer></td><td>Read-only</td><td>Manufacturing year.</td><tr><tr><td>cpufrequncy</td><td>&lt;Integer></td><td>Read-only</td><td>CPU Frequency.</td><tr><tr><td>hostid</td><td>&lt;Integer></td><td>Read-only</td><td>host id.</td><tr><tr><td>host</td><td>&lt;String></td><td>Read-only</td><td>host id.</td><tr><tr><td>serialno</td><td>&lt;String></td><td>Read-only</td><td>Serial no.</td><tr><tr><td>encodedserialno</td><td>&lt;String></td><td>Read-only</td><td>Encoded serial no.</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[GET (ALL)](#get-(all))


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nshardware
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "nshardware": [ {      "hwdescription":<String_value>,      "sysid":<Double_value>,      "manufactureday":<Integer_value>,      "manufacturemonth":<Integer_value>,      "manufactureyear":<Integer_value>,      "cpufrequncy":<Integer_value>,      "hostid":<Integer_value>,      "host":<String_value>,      "serialno":<String_value>,      "encodedserialno":<String_value>}]}```



