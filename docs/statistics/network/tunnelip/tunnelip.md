#tunnelip

Statistics for TUNNEL Remote ipaddress resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>tunnelip</td><td>&lt;String></td><td>Read-write</td><td>remote IP address of the configured tunnel.&lt;br>Minimum length = 1</td><tr><tr><td>clearstats</td><td>&lt;String></td><td>Read-write</td><td>Clear the statsistics / counters.&lt;br>Possible values = basic, full</td><tr><tr><td>tnltotrxpkts</td><td>&lt;Double></td><td>Read-only</td><td>Total number of packets received on the tunnel.</td><tr><tr><td>tnlrxpktsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for tnltotrxpkts</td><tr><tr><td>tnltottxpkts</td><td>&lt;Double></td><td>Read-only</td><td>Total number of packets transmitted on the tunnel.</td><tr><tr><td>tnltxpktsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for tnltottxpkts</td><tr><tr><td>tnltotrxbytes</td><td>&lt;Double></td><td>Read-only</td><td>Total number of bytes received on the tunnel.</td><tr><tr><td>tnlrxbytesrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for tnltotrxbytes</td><tr><tr><td>tnltottxbytes</td><td>&lt;Double></td><td>Read-only</td><td>Total number of bytes transmitted on the tunnel.</td><tr><tr><td>tnltxbytesrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for tnltottxbytes</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[GET (ALL)](#get-(all)) | [GET](#get)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



URL: http://NS_IP/nitro/v1/stat/tunnelip
Query-parameters:
args
http://&lt;NSIP&gt;/nitro/v1/stat/tunnelip?args=      tunnelip:&lt;String_value&gt;,      detail:&lt;Boolean_value&gt;,      fullvalues:&lt;Boolean_value&gt;,      ntimes:&lt;Double_value&gt;,      logfile:&lt;String_value&gt;,      clearstats:&lt;String_value&gt;,
Use this query-parameter to get tunnelip resources based on additional properties.



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "tunnelip": [ {      "tunnelip":<String_value>,      "tnltottxbytes":<Double_value>,      "tnltottxpkts":<Double_value>,      "tnltxpktsrate":<Double_value>,      "tnlrxbytesrate":<Double_value>,      "tnltotrxbytes":<Double_value>,      "tnltxbytesrate":<Double_value>,      "tnlrxpktsrate":<Double_value>,      "tnltotrxpkts":<Double_value>}]}```



###get



URL: http://NS_IP/nitro/v1/stat/tunnelip/tunnelip_value&lt;String&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "tunnelip": [ {      "tunnelip":<String_value>,      "tnltottxbytes":<Double_value>,      "tnltottxpkts":<Double_value>,      "tnltxpktsrate":<Double_value>,      "tnlrxbytesrate":<Double_value>,      "tnltotrxbytes":<Double_value>,      "tnltxbytesrate":<Double_value>,      "tnlrxpktsrate":<Double_value>,      "tnltotrxpkts":<Double_value>}]}```



