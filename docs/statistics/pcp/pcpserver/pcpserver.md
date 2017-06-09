#pcpserver

Statistics for server resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>PCP Statistics per Server.</td><tr><tr><td>clearstats</td><td>&lt;String></td><td>Read-write</td><td>Clear the statsistics / counters.&lt;br>Possible values = basic, full</td><tr><tr><td>pcptotrequests</td><td>&lt;Double></td><td>Read-only</td><td>PCP Request received.</td><tr><tr><td>pcprequestsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for pcptotrequests</td><tr><tr><td>pcptotresponses</td><td>&lt;Double></td><td>Read-only</td><td>Number PCP responces sent.</td><tr><tr><td>pcpresponsesrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for pcptotresponses</td><tr><tr><td>pcptotmaprequests</td><td>&lt;Double></td><td>Read-only</td><td>PCP MAP Requests received.</td><tr><tr><td>pcpmaprequestsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for pcptotmaprequests</td><tr><tr><td>pcptotpeerrequests</td><td>&lt;Double></td><td>Read-only</td><td>PCP PEER Requests received.</td><tr><tr><td>pcppeerrequestsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for pcptotpeerrequests</td><tr><tr><td>pcptoterrinrquest</td><td>&lt;Double></td><td>Read-only</td><td>total PCP request with error.</td><tr><tr><td>pcperrinrquestrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for pcptoterrinrquest</td><tr><tr><td>pcptoterrinres</td><td>&lt;Double></td><td>Read-only</td><td>Total PCP responses with errors.</td><tr><tr><td>pcperrinresrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for pcptoterrinres</td><tr><tr><td>pcptotunsuppvers</td><td>&lt;Double></td><td>Read-only</td><td>PCP request with unsupported version.</td><tr><tr><td>pcpunsuppversrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for pcptotunsuppvers</td><tr><tr><td>pcptotmalformedreq</td><td>&lt;Double></td><td>Read-only</td><td>total PCP request having malformed PCP packets.</td><tr><tr><td>pcpmalformedreqrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for pcptotmalformedreq</td><tr><tr><td>pcptotunsuppopcode</td><td>&lt;Double></td><td>Read-only</td><td>total Unsupproted OPCODES received Requests.</td><tr><tr><td>pcpunsuppopcoderate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for pcptotunsuppopcode</td><tr><tr><td>pcptotunsuppoption</td><td>&lt;Double></td><td>Read-only</td><td>total Unsupproted OPTIONS received in requests.</td><tr><tr><td>pcpunsuppoptionrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for pcptotunsuppoption</td><tr><tr><td>pcptotmalformedoption</td><td>&lt;Double></td><td>Read-only</td><td>total malformed OPTIONS received in requests.</td><tr><tr><td>pcpmalformedoptionrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for pcptotmalformedoption</td><tr><tr><td>pcptotnetfailure</td><td>&lt;Double></td><td>Read-only</td><td>Total Network Failures.</td><tr><tr><td>pcpnetfailurerate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for pcptotnetfailure</td><tr><tr><td>pcptotnoresources</td><td>&lt;Double></td><td>Read-only</td><td>no resources</td><tr><tr><td>pcpnoresourcesrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for pcptotnoresources</td><tr><tr><td>pcptotunsupportedprotocol</td><td>&lt;Double></td><td>Read-only</td><td>Total Unsupported Protocols requests.</td><tr><tr><td>pcpunsupportedprotocolrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for pcptotunsupportedprotocol</td><tr><tr><td>pcptotuserexqouta</td><td>&lt;Double></td><td>Read-only</td><td>Total user ex quota.</td><tr><tr><td>pcpuserexqoutarate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for pcptotuserexqouta</td><tr><tr><td>pcptotnoexternal</td><td>&lt;Double></td><td>Read-only</td><td>Total responses with opcode can not provide external.</td><tr><tr><td>pcpnoexternalrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for pcptotnoexternal</td><tr><tr><td>pcptotaddrmismatch</td><td>&lt;Double></td><td>Read-only</td><td>Total address mismatch.</td><tr><tr><td>pcpaddrmismatchrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for pcptotaddrmismatch</td><tr><tr><td>pcptotexcesspeers</td><td>&lt;Double></td><td>Read-only</td><td>Total responses with opcode excessive remote peers.</td><tr><tr><td>pcpexcesspeersrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for pcptotexcesspeers</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[GET (ALL)](#get-(all)) | [GET](#get)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/pcpserver
Query-parameters:
args
http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/pcpserver?args=name:&lt;String_value&gt;,detail:&lt;Boolean_value&gt;,fullvalues:&lt;Boolean_value&gt;,ntimes:&lt;Double_value&gt;,logfile:&lt;String_value&gt;,clearstats:&lt;String_value&gt;
Use this query-parameter to get pcpserver resources based on additional properties.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx   (for general HTTP errors) or 5xx     (for NetScaler-specific errors). The response payload provides details of the error Response Headers:

Content-Type:application/json

Response Payload: ```{ "pcpserver": [ {      "name":<String_value>,      "pcpaddrmismatchrate":<Double_value>,      "pcptotmalformedreq":<Double_value>,      "pcpnoresourcesrate":<Double_value>,      "pcpunsuppopcoderate":<Double_value>,      "pcptotpeerrequests":<Double_value>,      "pcpnetfailurerate":<Double_value>,      "pcptoterrinrquest":<Double_value>,      "pcptotmalformedoption":<Double_value>,      "pcptotresponses":<Double_value>,      "pcpunsupportedprotocolrate":<Double_value>,      "pcptotnoresources":<Double_value>,      "pcptotnetfailure":<Double_value>,      "pcppeerrequestsrate":<Double_value>,      "pcptotnoexternal":<Double_value>,      "pcperrinresrate":<Double_value>,      "pcptotunsuppopcode":<Double_value>,      "pcpunsuppversrate":<Double_value>,      "pcptotuserexqouta":<Double_value>,      "pcptotunsuppvers":<Double_value>,      "pcpuserexqoutarate":<Double_value>,      "pcptotunsupportedprotocol":<Double_value>,      "pcpexcesspeersrate":<Double_value>,      "pcpmalformedoptionrate":<Double_value>,      "pcptotrequests":<Double_value>,      "pcperrinrquestrate":<Double_value>,      "pcpresponsesrate":<Double_value>,      "pcpunsuppoptionrate":<Double_value>,      "pcpmaprequestsrate":<Double_value>,      "pcpnoexternalrate":<Double_value>,      "pcptotunsuppoption":<Double_value>,      "pcptoterrinres":<Double_value>,      "pcptotmaprequests":<Double_value>,      "pcptotexcesspeers":<Double_value>,      "pcpmalformedreqrate":<Double_value>,      "pcprequestsrate":<Double_value>,      "pcptotaddrmismatch":<Double_value>}]}```



###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/pcpserver/name_value&gt;&lt;String&gt;
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx   (for general HTTP errors) or 5xx     (for NetScaler-specific errors). The response payload provides details of the error Response Headers:

Content-Type:application/json

Response Payload: ```{ "pcpserver": [ {      "name":<String_value>,      "pcpaddrmismatchrate":<Double_value>,      "pcptotmalformedreq":<Double_value>,      "pcpnoresourcesrate":<Double_value>,      "pcpunsuppopcoderate":<Double_value>,      "pcptotpeerrequests":<Double_value>,      "pcpnetfailurerate":<Double_value>,      "pcptoterrinrquest":<Double_value>,      "pcptotmalformedoption":<Double_value>,      "pcptotresponses":<Double_value>,      "pcpunsupportedprotocolrate":<Double_value>,      "pcptotnoresources":<Double_value>,      "pcptotnetfailure":<Double_value>,      "pcppeerrequestsrate":<Double_value>,      "pcptotnoexternal":<Double_value>,      "pcperrinresrate":<Double_value>,      "pcptotunsuppopcode":<Double_value>,      "pcpunsuppversrate":<Double_value>,      "pcptotuserexqouta":<Double_value>,      "pcptotunsuppvers":<Double_value>,      "pcpuserexqoutarate":<Double_value>,      "pcptotunsupportedprotocol":<Double_value>,      "pcpexcesspeersrate":<Double_value>,      "pcpmalformedoptionrate":<Double_value>,      "pcptotrequests":<Double_value>,      "pcperrinrquestrate":<Double_value>,      "pcpresponsesrate":<Double_value>,      "pcpunsuppoptionrate":<Double_value>,      "pcpmaprequestsrate":<Double_value>,      "pcpnoexternalrate":<Double_value>,      "pcptotunsuppoption":<Double_value>,      "pcptoterrinres":<Double_value>,      "pcptotmaprequests":<Double_value>,      "pcptotexcesspeers":<Double_value>,      "pcpmalformedreqrate":<Double_value>,      "pcprequestsrate":<Double_value>,      "pcptotaddrmismatch":<Double_value>}]}```



