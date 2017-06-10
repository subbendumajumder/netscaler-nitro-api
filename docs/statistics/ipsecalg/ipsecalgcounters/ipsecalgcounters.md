#ipsecalgcounters

Statistics for counters resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name of IPSec ALG Profile.&lt;br>Minimum length = 1&lt;br>Maximum length = 32</td><tr><tr><td>clearstats</td><td>&lt;String></td><td>Read-write</td><td>Clear the statsistics / counters.&lt;br>Possible values = basic, full</td><tr><tr><td>ipsecalgtotsessions</td><td>&lt;Double></td><td>Read-only</td><td>Total session for IPSec ALG.</td><tr><tr><td>ipsecalgsessionsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for ipsecalgtotsessions</td><tr><tr><td>ipsecalgtotdrsessions</td><td>&lt;Double></td><td>Read-only</td><td>Total Dropped IPsec ALG sessions.</td><tr><tr><td>ipsecalgdrsessionsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for ipsecalgtotdrsessions</td><tr><tr><td>ipsecalgcuractsessions</td><td>&lt;Double></td><td>Read-only</td><td>Currently active IPsec ALG sessions.</td><tr><tr><td>ipsecalgcuractsessionsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for ipsecalgcuractsessions</td><tr><tr><td>ipsecalgcurblksessions</td><td>&lt;Double></td><td>Read-only</td><td>Currently blocked sessions on ESP Gate.</td><tr><tr><td>ipsecalgcurblksessionsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for ipsecalgcurblksessions</td><tr><tr><td>ipsecalgtotrxpkts</td><td>&lt;Double></td><td>Read-only</td><td>Total Packets received during IPsec ALG sessions.</td><tr><tr><td>ipsecalgrxpktsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for ipsecalgtotrxpkts</td><tr><tr><td>ipsecalgtottxpkts</td><td>&lt;Double></td><td>Read-only</td><td>Total Packets sent during IPsec ALG sessions.</td><tr><tr><td>ipsecalgtxpktsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for ipsecalgtottxpkts</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[GET (ALL)](#get-(all)) | [GET](#get)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/ipsecalgcounters
Query-parameters:
args
http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/ipsecalgcounters?args=name:&lt;String_value&gt;,detail:&lt;Boolean_value&gt;,fullvalues:&lt;Boolean_value&gt;,ntimes:&lt;Double_value&gt;,logfile:&lt;String_value&gt;,clearstats:&lt;String_value&gt;
Use this query-parameter to get ipsecalgcounters resources based on additional properties.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "ipsecalgcounters": [ {      "name":<String_value>,      "ipsecalgdrsessionsrate":<Double_value>,      "ipsecalgtotrxpkts":<Double_value>,      "ipsecalgtottxpkts":<Double_value>,      "ipsecalgtxpktsrate":<Double_value>,      "ipsecalgtotsessions":<Double_value>,      "ipsecalgrxpktsrate":<Double_value>,      "ipsecalgtotdrsessions":<Double_value>,      "ipsecalgcuractsessionsrate":<Double_value>,      "ipsecalgsessionsrate":<Double_value>,      "ipsecalgcuractsessions":<Double_value>,      "ipsecalgcurblksessions":<Double_value>,      "ipsecalgcurblksessionsrate":<Double_value>}]}```



###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/ipsecalgcounters/name_value&gt;&lt;String&gt;
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "ipsecalgcounters": [ {      "name":<String_value>,      "ipsecalgdrsessionsrate":<Double_value>,      "ipsecalgtotrxpkts":<Double_value>,      "ipsecalgtottxpkts":<Double_value>,      "ipsecalgtxpktsrate":<Double_value>,      "ipsecalgtotsessions":<Double_value>,      "ipsecalgrxpktsrate":<Double_value>,      "ipsecalgtotdrsessions":<Double_value>,      "ipsecalgcuractsessionsrate":<Double_value>,      "ipsecalgsessionsrate":<Double_value>,      "ipsecalgcuractsessions":<Double_value>,      "ipsecalgcurblksessions":<Double_value>,      "ipsecalgcurblksessionsrate":<Double_value>}]}```



