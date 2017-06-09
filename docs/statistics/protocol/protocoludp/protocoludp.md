#protocoludp

Statistics for UDP Protocol resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>clearstats</td><td>&lt;String></td><td>Read-write</td><td>Clear the statsistics / counters.&lt;br>Possible values = basic, full</td><tr><tr><td>udptotrxpkts</td><td>&lt;Double></td><td>Read-only</td><td>Total number of UDP packets received.</td><tr><tr><td>udprxpktsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for udptotrxpkts</td><tr><tr><td>udptotrxbytes</td><td>&lt;Double></td><td>Read-only</td><td>Total number of UDP data received in bytes.</td><tr><tr><td>udprxbytesrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for udptotrxbytes</td><tr><tr><td>udptottxpkts</td><td>&lt;Double></td><td>Read-only</td><td>Total number of UDP packets transmitted.</td><tr><tr><td>udptxpktsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for udptottxpkts</td><tr><tr><td>udptottxbytes</td><td>&lt;Double></td><td>Read-only</td><td>Total number of UDP data transmitted in bytes.</td><tr><tr><td>udptxbytesrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for udptottxbytes</td><tr><tr><td>udpcurratethreshold</td><td>&lt;Double></td><td>Read-only</td><td>Limit for UDP packets handled every 10 milliseconds. Default value, 0, applies no limit. This is a configurable value using the set rateControl command.</td><tr><tr><td>udptotunknownsvcpkts</td><td>&lt;Double></td><td>Read-only</td><td>Stray UDP packets dropped due to no configured listening service.</td><tr><tr><td>udpbadchecksum</td><td>&lt;Double></td><td>Read-only</td><td>Packets received with a UDP checksum error.</td><tr><tr><td>udpcurratethresholdexceeds</td><td>&lt;Double></td><td>Read-only</td><td>Number of times the UDP rate threshold is exceeded. If this counter continuously increases, first make sure the UDP packets received are genuine. If they are, increase the current rate threshold. This is a configurable value using the set rateControl command.</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[GET (ALL)](#get-(all))


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/protocoludp
Query-parameters:
args
http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/protocoludp?args=detail:&lt;Boolean_value&gt;,fullvalues:&lt;Boolean_value&gt;,ntimes:&lt;Double_value&gt;,logfile:&lt;String_value&gt;,clearstats:&lt;String_value&gt;
Use this query-parameter to get protocoludp resources based on additional properties.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "protocoludp": [ {      "udptxpktsrate":<Double_value>,      "udpcurratethreshold":<Double_value>,      "udptotrxpkts":<Double_value>,      "udptottxpkts":<Double_value>,      "udptotrxbytes":<Double_value>,      "udptxbytesrate":<Double_value>,      "udprxpktsrate":<Double_value>,      "udpbadchecksum":<Double_value>,      "udptottxbytes":<Double_value>,      "udptotunknownsvcpkts":<Double_value>,      "udprxbytesrate":<Double_value>,      "udpcurratethresholdexceeds":<Double_value>}]}```



