#rnatip

Statistics for RNAT ipaddress resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>Rnatip</td><td>&lt;String></td><td>Read-write</td><td>Specifies the NAT IP address of the configured RNAT entry for which you want to see the statistics. If you do not specify an IP address, this displays the statistics for all the configured RNAT entries.&lt;br>Minimum length = 1</td><tr><tr><td>clearstats</td><td>&lt;String></td><td>Read-write</td><td>Clear the statsistics / counters.&lt;br>Possible values = basic, full</td><tr><tr><td>iptd</td><td>&lt;Double></td><td>Read-only</td><td>Traffic domain for ipaddr.</td><tr><tr><td>iprnattotrxbytes</td><td>&lt;Double></td><td>Read-only</td><td>Bytes received on this IP address during RNAT sessions.</td><tr><tr><td>iprnatrxbytesrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for iprnattotrxbytes</td><tr><tr><td>iprnattottxbytes</td><td>&lt;Double></td><td>Read-only</td><td>Bytes sent from this IP address during RNAT sessions.</td><tr><tr><td>iprnattxbytesrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for iprnattottxbytes</td><tr><tr><td>iprnattotrxpkts</td><td>&lt;Double></td><td>Read-only</td><td>Packets received on this IP address during RNAT sessions.</td><tr><tr><td>iprnatrxpktsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for iprnattotrxpkts</td><tr><tr><td>iprnattottxpkts</td><td>&lt;Double></td><td>Read-only</td><td>Packets sent from this IP address during RNAT sessions.</td><tr><tr><td>iprnattxpktsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for iprnattottxpkts</td><tr><tr><td>iprnattottxsyn</td><td>&lt;Double></td><td>Read-only</td><td>Requests for connections sent from this IP address during RNAT sessions.</td><tr><tr><td>iprnattxsynrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for iprnattottxsyn</td><tr><tr><td>iprnatcursessions</td><td>&lt;Double></td><td>Read-only</td><td>Currently active RNAT sessions started from this IP address.</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[GET (ALL)](#get-(all)) | [GET](#get)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/rnatip
Query-parameters:
args
http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/rnatip?args=Rnatip:&lt;String_value&gt;,detail:&lt;Boolean_value&gt;,fullvalues:&lt;Boolean_value&gt;,ntimes:&lt;Double_value&gt;,logfile:&lt;String_value&gt;,clearstats:&lt;String_value&gt;
Use this query-parameter to get rnatip resources based on additional properties.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "rnatip": [ {      "Rnatip":<String_value>,      "iprnatrxpktsrate":<Double_value>,      "iprnattxpktsrate":<Double_value>,      "iprnattottxpkts":<Double_value>,      "iptd":<Double_value>,      "iprnattottxbytes":<Double_value>,      "iprnatcursessions":<Double_value>,      "iprnatrxbytesrate":<Double_value>,      "iprnattotrxbytes":<Double_value>,      "iprnattxsynrate":<Double_value>,      "iprnattxbytesrate":<Double_value>,      "iprnattotrxpkts":<Double_value>,      "iprnattottxsyn":<Double_value>}]}```



###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/rnatip/Rnatip_value&gt;&lt;String&gt;
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "rnatip": [ {      "Rnatip":<String_value>,      "iprnatrxpktsrate":<Double_value>,      "iprnattxpktsrate":<Double_value>,      "iprnattottxpkts":<Double_value>,      "iptd":<Double_value>,      "iprnattottxbytes":<Double_value>,      "iprnatcursessions":<Double_value>,      "iprnatrxbytesrate":<Double_value>,      "iprnattotrxbytes":<Double_value>,      "iprnattxsynrate":<Double_value>,      "iprnattxbytesrate":<Double_value>,      "iprnattotrxpkts":<Double_value>,      "iprnattottxsyn":<Double_value>}]}```



