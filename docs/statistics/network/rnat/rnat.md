#rnat

Statistics for RNAT configured route resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>clearstats</td><td>&lt;String></td><td>Read-write</td><td>Clear the statsistics / counters.&lt;br>Possible values = basic, full</td><tr><tr><td>rnattotrxbytes</td><td>&lt;Double></td><td>Read-only</td><td>Bytes received during RNAT sessions.</td><tr><tr><td>rnatrxbytesrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for rnattotrxbytes</td><tr><tr><td>rnattottxbytes</td><td>&lt;Double></td><td>Read-only</td><td>Bytes sent during RNAT sessions.</td><tr><tr><td>rnattxbytesrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for rnattottxbytes</td><tr><tr><td>rnattotrxpkts</td><td>&lt;Double></td><td>Read-only</td><td>Packets received during RNAT sessions.</td><tr><tr><td>rnatrxpktsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for rnattotrxpkts</td><tr><tr><td>rnattottxpkts</td><td>&lt;Double></td><td>Read-only</td><td>Packets sent during RNAT sessions.</td><tr><tr><td>rnattxpktsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for rnattottxpkts</td><tr><tr><td>rnattottxsyn</td><td>&lt;Double></td><td>Read-only</td><td>Requests for connections sent during RNAT sessions.</td><tr><tr><td>rnattxsynrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for rnattottxsyn</td><tr><tr><td>rnatcursessions</td><td>&lt;Double></td><td>Read-only</td><td>Currently active RNAT sessions.</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[GET (ALL)](#get-(all))


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



URL: http://NS_IP/nitro/v1/stat/rnat
Query-parameters:
args
http://&lt;NSIP&gt;/nitro/v1/stat/rnat?args=      detail:&lt;Boolean_value&gt;,      fullvalues:&lt;Boolean_value&gt;,      ntimes:&lt;Double_value&gt;,      logfile:&lt;String_value&gt;,      clearstats:&lt;String_value&gt;,
Use this query-parameter to get rnat resources based on additional properties.



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "rnat": [ {      "rnattottxpkts":<Double_value>,      "rnatrxbytesrate":<Double_value>,      "rnattxsynrate":<Double_value>,      "rnattxpktsrate":<Double_value>,      "rnattottxsyn":<Double_value>,      "rnattxbytesrate":<Double_value>,      "rnatrxpktsrate":<Double_value>,      "rnatcursessions":<Double_value>,      "rnattotrxpkts":<Double_value>,      "rnattotrxbytes":<Double_value>,      "rnattottxbytes":<Double_value>}]}```



