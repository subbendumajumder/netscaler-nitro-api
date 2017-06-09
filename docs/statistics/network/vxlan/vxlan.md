#vxlan

Statistics for "VXLAN" resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>&lt;Double></td><td>Read-write</td><td>An integer specifying the VXLAN identification number (VNID).&lt;br>Minimum value = 1&lt;br>Maximum value = 16777215</td><tr><tr><td>clearstats</td><td>&lt;String></td><td>Read-write</td><td>Clear the statsistics / counters.&lt;br>Possible values = basic, full</td><tr><tr><td>vxlantotrxpkts</td><td>&lt;Double></td><td>Read-only</td><td>Packets received on the VXLAN.</td><tr><tr><td>vxlanrxpktsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for vxlantotrxpkts</td><tr><tr><td>vxlantotrxbytes</td><td>&lt;Double></td><td>Read-only</td><td>Bytes of data received on the VXLAN.</td><tr><tr><td>vxlanrxbytesrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for vxlantotrxbytes</td><tr><tr><td>vxlantottxpkts</td><td>&lt;Double></td><td>Read-only</td><td>Packets transmitted on the VXLAN.</td><tr><tr><td>vxlantxpktsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for vxlantottxpkts</td><tr><tr><td>vxlantottxbytes</td><td>&lt;Double></td><td>Read-only</td><td>Bytes of data transmitted on the VXLAN.</td><tr><tr><td>vxlantxbytesrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for vxlantottxbytes</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[GET (ALL)](#get-(all)) | [GET](#get)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/vxlan
Query-parameters:
args
http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/vxlan?args=id:&lt;Double_value&gt;,detail:&lt;Boolean_value&gt;,fullvalues:&lt;Boolean_value&gt;,ntimes:&lt;Double_value&gt;,logfile:&lt;String_value&gt;,clearstats:&lt;String_value&gt;
Use this query-parameter to get vxlan resources based on additional properties.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "vxlan": [ {      "id":<Double_value>,      "vxlanrxbytesrate":<Double_value>,      "vxlantottxpkts":<Double_value>,      "vxlanrxpktsrate":<Double_value>,      "vxlantotrxbytes":<Double_value>,      "vxlantxbytesrate":<Double_value>,      "vxlantxpktsrate":<Double_value>,      "vxlantottxbytes":<Double_value>,      "vxlantotrxpkts":<Double_value>}]}```



###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/vxlan/id_value&gt;&lt;Double&gt;
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "vxlan": [ {      "id":<Double_value>,      "vxlanrxbytesrate":<Double_value>,      "vxlantottxpkts":<Double_value>,      "vxlanrxpktsrate":<Double_value>,      "vxlantotrxbytes":<Double_value>,      "vxlantxbytesrate":<Double_value>,      "vxlantxpktsrate":<Double_value>,      "vxlantottxbytes":<Double_value>,      "vxlantotrxpkts":<Double_value>}]}```



