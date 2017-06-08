#protocolhttpband

Configuration for HTTP request/response band resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>reqbandsize</td><td>&lt;Integer></td><td>Read-write</td><td>Band size, in bytes, for HTTP request band statistics. For example, if you specify a band size of 100 bytes, statistics will be maintained and displayed for the following size ranges: 0 - 99 bytes 100 - 199 bytes 200 - 299 bytes and so on.&lt;br>Default value: 100&lt;br>Minimum value = 50</td><tr><tr><td>respbandsize</td><td>&lt;Integer></td><td>Read-write</td><td>Band size, in bytes, for HTTP response band statistics. For example, if you specify a band size of 100 bytes, statistics will be maintained and displayed for the following size ranges: 0 - 99 bytes 100 - 199 bytes 200 - 299 bytes and so on.&lt;br>Default value: 1024&lt;br>Minimum value = 50</td><tr><tr><td>type</td><td>&lt;String></td><td>Read-write</td><td>Type of statistics to display.&lt;br>Possible values = REQUEST, RESPONSE</td><tr><tr><td>bandrange</td><td>&lt;Integer></td><td>Read-only</td><td>The range of the HTTP request/response size, in bytes.</td><tr><tr><td>numberofbands</td><td>&lt;Integer></td><td>Read-only</td><td>The total number of http bands.</td><tr><tr><td>totalbandsize</td><td>&lt;Double[]></td><td>Read-only</td><td>The total size of all HTTP requests/responses in this size range.</td><tr><tr><td>avgbandsize</td><td>&lt;Double[]></td><td>Read-only</td><td>The average size of all HTTP requests/responses in this size range.</td><tr><tr><td>avgbandsizenew</td><td>&lt;Double[]></td><td>Read-only</td><td>The average size of all HTTP requests/responses in this size range.</td><tr><tr><td>banddata</td><td>&lt;Double[]></td><td>Read-only</td><td>The total size of all HTTP requests/responses in this size range, expressed as a percentage of the total size of all HTTP requests/responses.</td><tr><tr><td>banddatanew</td><td>&lt;Double[]></td><td>Read-only</td><td>The total size of all HTTP requests/responses in this size range, expressed as a percentage of the total size of all HTTP requests/responses.</td><tr><tr><td>accesscount</td><td>&lt;Double[]></td><td>Read-only</td><td>The number of HTTP requests/responses in this size range.</td><tr><tr><td>accessratio</td><td>&lt;Double[]></td><td>Read-only</td><td>The number of HTTP requests/responses in this size range, expressed as a percentage of the total number of HTTP requests/responses.</td><tr><tr><td>accessrationew</td><td>&lt;Double[]></td><td>Read-only</td><td>The number of HTTP requests/responses in this size range, expressed as a percentage of the total number of HTTP requests/responses.</td><tr><tr><td>totals</td><td>&lt;Integer[]></td><td>Read-only</td><td>The total of totalBandSize, avgBandSize, BandData, accessCount, accessRatio respectively.</td><tr></tbody></table>
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
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","protocolhttpband":{      "reqbandsize":<Integer_value>,      "respbandsize":<Integer_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","protocolhttpband":{      "reqbandsize":true,      "respbandsize":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/protocolhttpband
Query-parameters:
args
http://&lt;NSIP&gt;/nitro/v1/config/protocolhttpband?args=      "type":&lt;String_value&gt;,
Use this query-parameter to get protocolhttpband resources based on additional properties.



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "protocolhttpband": [ {      "type":<String_value>,      "bandrange":<Integer_value>,      "numberofbands":<Integer_value>,      "totalbandsize":<Double[]_value>,      "avgbandsize":<Double[]_value>,      "avgbandsizenew":<Double[]_value>,      "banddata":<Double[]_value>,      "banddatanew":<Double[]_value>,      "accesscount":<Double[]_value>,      "accessratio":<Double[]_value>,      "accessrationew":<Double[]_value>,      "totals":<Integer[]_value>}]}```



