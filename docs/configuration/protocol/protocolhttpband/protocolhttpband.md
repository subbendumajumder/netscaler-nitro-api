#protocolhttpband

Configuration for HTTP request/response band resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>reqbandsize</td><td>&lt;Integer></td><td>Read-write</td><td>Band size, in bytes, for HTTP request band statistics. For example, if you specify a band size of 100 bytes, statistics will be maintained and displayed for the following size ranges:<br>0 - 99 bytes<br>100 - 199 bytes<br>200 - 299 bytes and so on.<br>Default value: 100<br>Minimum value = 50</td></tr><tr><td>respbandsize</td><td>&lt;Integer></td><td>Read-write</td><td>Band size, in bytes, for HTTP response band statistics. For example, if you specify a band size of 100 bytes, statistics will be maintained and displayed for the following size ranges:<br>0 - 99 bytes<br>100 - 199 bytes<br>200 - 299 bytes and so on.<br>Default value: 1024<br>Minimum value = 50</td></tr><tr><td>type</td><td>&lt;String></td><td>Read-write</td><td>Type of statistics to display.<br>Possible values = REQUEST, RESPONSE</td></tr><tr><td>nodeid</td><td>&lt;Double></td><td>Read-write</td><td>Unique number that identifies the cluster node.<br>Minimum value = 0<br>Maximum value = 31</td></tr><tr><td>bandrange</td><td>&lt;Integer></td><td>Read-only</td><td>The range of the HTTP request/response size, in bytes.</td></tr><tr><td>numberofbands</td><td>&lt;Integer></td><td>Read-only</td><td>The total number of http bands.</td></tr><tr><td>totalbandsize</td><td>&lt;Double[]></td><td>Read-only</td><td>The total size of all HTTP requests/responses in this size range.</td></tr><tr><td>avgbandsize</td><td>&lt;Double[]></td><td>Read-only</td><td>The average size of all HTTP requests/responses in this size range.</td></tr><tr><td>avgbandsizenew</td><td>&lt;Double[]></td><td>Read-only</td><td>The average size of all HTTP requests/responses in this size range.</td></tr><tr><td>banddata</td><td>&lt;Double[]></td><td>Read-only</td><td>The total size of all HTTP requests/responses in this size range, expressed as a percentage of the total size of all HTTP requests/responses.</td></tr><tr><td>banddatanew</td><td>&lt;Double[]></td><td>Read-only</td><td>The total size of all HTTP requests/responses in this size range, expressed as a percentage of the total size of all HTTP requests/responses.</td></tr><tr><td>accesscount</td><td>&lt;Double[]></td><td>Read-only</td><td>The number of HTTP requests/responses in this size range.</td></tr><tr><td>accessratio</td><td>&lt;Double[]></td><td>Read-only</td><td>The number of HTTP requests/responses in this size range, expressed as a percentage of the total number of HTTP requests/responses.</td></tr><tr><td>accessrationew</td><td>&lt;Double[]></td><td>Read-only</td><td>The number of HTTP requests/responses in this size range, expressed as a percentage of the total number of HTTP requests/responses.</td></tr><tr><td>totals</td><td>&lt;Integer[]></td><td>Read-only</td><td>The total of totalBandSize, avgBandSize, BandData, accessCount, accessRatio respectively.</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[UPDATE](#u)| [UNSET](#)| [CLEAR](#)| [GET (ALL)](#get-)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/protocolhttpband
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"protocolhttpband":{"reqbandsize":<Integer_value>,"respbandsize":<Integer_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/protocolhttpband?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"protocolhttpband":{"reqbandsize":true,"respbandsize":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###clear



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/protocolhttpband?<b>action=clear</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"protocolhttpband":{<b>"type":<String_value></b>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/protocolhttpband
<b>Query-parameters:</b>
<b>args</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/protocolhttpband?<b>args=<b>type:&lt;String_value&gt;,</b>nodeid:&lt;Double_value&gt;</b>
Use this query-parameter to get protocolhttpband resources based on additional properties.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "protocolhttpband": [ {<b>type:<String_value>,</b>nodeid:<Double_value>"bandrange":<Integer_value>,"numberofbands":<Integer_value>,"totalbandsize":<Double[]_value>,"avgbandsize":<Double[]_value>,"avgbandsizenew":<Double[]_value>,"banddata":<Double[]_value>,"banddatanew":<Double[]_value>,"accesscount":<Double[]_value>,"accessratio":<Double[]_value>,"accessrationew":<Double[]_value>,"totals":<Integer[]_value>,"reqbandsize":<Integer_value>,"respbandsize":<Integer_value>}]}```



