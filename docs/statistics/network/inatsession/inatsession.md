#inatsession

Statistics for stateful INAT resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>INAT name.&lt;br>Minimum length = 1</td><tr><tr><td>clearstats</td><td>&lt;String></td><td>Read-write</td><td>Clear the statsistics / counters.&lt;br>Possible values = basic, full</td><tr><tr><td>inattothits</td><td>&lt;Double></td><td>Read-only</td><td>INAT total sessions</td><tr><tr><td>inathitsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for inattothits</td><tr><tr><td>inatcursessions</td><td>&lt;Double></td><td>Read-only</td><td>INAT current sessions</td><tr><tr><td>inatcursessionsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for inatcursessions</td><tr><tr><td>inattotreceivebytes</td><td>&lt;Double></td><td>Read-only</td><td>INAT total Received Bytes</td><tr><tr><td>inatreceivebytesrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for inattotreceivebytes</td><tr><tr><td>inattotsentbytes</td><td>&lt;Double></td><td>Read-only</td><td>INAT total Sent Bytes</td><tr><tr><td>inatsentbytesrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for inattotsentbytes</td><tr><tr><td>inattotpktreceived</td><td>&lt;Double></td><td>Read-only</td><td>INAT total Packets Received</td><tr><tr><td>inatpktreceivedrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for inattotpktreceived</td><tr><tr><td>inattotpktsent</td><td>&lt;Double></td><td>Read-only</td><td>INAT total Packets Sent</td><tr><tr><td>inatpktsentrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for inattotpktsent</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[GET (ALL)](#get-(all)) | [GET](#get)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/inatsession
Query-parameters:
args
http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/inatsession?args=name:&lt;String_value&gt;,detail:&lt;Boolean_value&gt;,fullvalues:&lt;Boolean_value&gt;,ntimes:&lt;Double_value&gt;,logfile:&lt;String_value&gt;,clearstats:&lt;String_value&gt;
Use this query-parameter to get inatsession resources based on additional properties.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "inatsession": [ {      "name":<String_value>,      "inattotsentbytes":<Double_value>,      "inatreceivebytesrate":<Double_value>,      "inathitsrate":<Double_value>,      "inattotreceivebytes":<Double_value>,      "inatcursessionsrate":<Double_value>,      "inatcursessions":<Double_value>,      "inatsentbytesrate":<Double_value>,      "inatpktsentrate":<Double_value>,      "inattotpktreceived":<Double_value>,      "inattothits":<Double_value>,      "inattotpktsent":<Double_value>,      "inatpktreceivedrate":<Double_value>}]}```



###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/inatsession/name_value&gt;&lt;String&gt;
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "inatsession": [ {      "name":<String_value>,      "inattotsentbytes":<Double_value>,      "inatreceivebytesrate":<Double_value>,      "inathitsrate":<Double_value>,      "inattotreceivebytes":<Double_value>,      "inatcursessionsrate":<Double_value>,      "inatcursessions":<Double_value>,      "inatsentbytesrate":<Double_value>,      "inatpktsentrate":<Double_value>,      "inattotpktreceived":<Double_value>,      "inattothits":<Double_value>,      "inattotpktsent":<Double_value>,      "inatpktreceivedrate":<Double_value>}]}```



