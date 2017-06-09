#pqpolicy

Statistics for PQ policy resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>policyname</td><td>&lt;String></td><td>Read-write</td><td>Name of the priority queuing policy whose statistics must be displayed. If a name is not provided, statistics of all priority queuing policies are shown.&lt;br>Minimum length = 1</td><tr><tr><td>clearstats</td><td>&lt;String></td><td>Read-write</td><td>Clear the statsistics / counters.&lt;br>Possible values = basic, full</td><tr><tr><td>pqtotavgqueuewaittime</td><td>&lt;Double></td><td>Read-only</td><td>Average wait time for clients for this priority queuing policy.</td><tr><tr><td>pqavgqueuewaittimerate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for pqtotavgqueuewaittime</td><tr><tr><td>pqavgclienttransactiontimems</td><td>&lt;Double></td><td>Read-only</td><td>Average time taken by a priority queuing client to complete its transaction for this priority queuing policy.</td><tr><tr><td>pqavgclienttransactiontimemsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for pqavgclienttransactiontimems</td><tr><tr><td>pqvserverip</td><td>&lt;String></td><td>Read-only</td><td>IP address of the virtual server to which this priority queuing policy is bound.</td><tr><tr><td>pqvserverport</td><td>&lt;Integer></td><td>Read-only</td><td>Port number of the virtual server to which this priority queuing policy is bound.</td><tr><tr><td>pqqdepth</td><td>&lt;Double></td><td>Read-only</td><td>Number of clients waiting currently for this priority queuing policy.</td><tr><tr><td>pqqdepthrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for pqqdepth</td><tr><tr><td>pqcurrentclientconnections</td><td>&lt;Double></td><td>Read-only</td><td>Current number of server connections established for serving clients for this priority queuing policy.</td><tr><tr><td>pqcurrentclientconnectionsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for pqcurrentclientconnections</td><tr><tr><td>pqtotclientconnections</td><td>&lt;Double></td><td>Read-only</td><td>Total number of server connections established for serving clients for this priority queuing policy.</td><tr><tr><td>pqclientconnectionsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for pqtotclientconnections</td><tr><tr><td>pqdropped</td><td>&lt;Double></td><td>Read-only</td><td>Total number of dropped transactions for this priority queuing policy.</td><tr><tr><td>pqdroppedrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for pqdropped</td><tr><tr><td>totclienttransactions</td><td>&lt;Double></td><td>Read-only</td><td>Total number of client transactions for this priority queuing policy.</td><tr><tr><td>clienttransactionsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for totclienttransactions</td><tr><tr><td>pqtotqueuedepth</td><td>&lt;Double></td><td>Read-only</td><td>Total number of waiting clients for this priority queuing policy.</td><tr><tr><td>pqqueuedepthrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for pqtotqueuedepth</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[GET (ALL)](#get-(all)) | [GET](#get)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/pqpolicy
Query-parameters:
args
http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/pqpolicy?args=policyname:&lt;String_value&gt;,detail:&lt;Boolean_value&gt;,fullvalues:&lt;Boolean_value&gt;,ntimes:&lt;Double_value&gt;,logfile:&lt;String_value&gt;,clearstats:&lt;String_value&gt;
Use this query-parameter to get pqpolicy resources based on additional properties.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "pqpolicy": [ {      "policyname":<String_value>,      "pqvserverip":<String_value>,      "pqqueuedepthrate":<Double_value>,      "pqdroppedrate":<Double_value>,      "pqtotqueuedepth":<Double_value>,      "pqvserverport":<Integer_value>,      "totclienttransactions":<Double_value>,      "clienttransactionsrate":<Double_value>,      "pqcurrentclientconnectionsrate":<Double_value>,      "pqqdepthrate":<Double_value>,      "pqqdepth":<Double_value>,      "pqclientconnectionsrate":<Double_value>,      "pqavgclienttransactiontimems":<Double_value>,      "pqavgclienttransactiontimemsrate":<Double_value>,      "pqtotavgqueuewaittime":<Double_value>,      "pqdropped":<Double_value>,      "pqtotclientconnections":<Double_value>,      "pqavgqueuewaittimerate":<Double_value>,      "pqcurrentclientconnections":<Double_value>}]}```



###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/pqpolicy/policyname_value&gt;&lt;String&gt;
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "pqpolicy": [ {      "policyname":<String_value>,      "pqvserverip":<String_value>,      "pqqueuedepthrate":<Double_value>,      "pqdroppedrate":<Double_value>,      "pqtotqueuedepth":<Double_value>,      "pqvserverport":<Integer_value>,      "totclienttransactions":<Double_value>,      "clienttransactionsrate":<Double_value>,      "pqcurrentclientconnectionsrate":<Double_value>,      "pqqdepthrate":<Double_value>,      "pqqdepth":<Double_value>,      "pqclientconnectionsrate":<Double_value>,      "pqavgclienttransactiontimems":<Double_value>,      "pqavgclienttransactiontimemsrate":<Double_value>,      "pqtotavgqueuewaittime":<Double_value>,      "pqdropped":<Double_value>,      "pqtotclientconnections":<Double_value>,      "pqavgqueuewaittimerate":<Double_value>,      "pqcurrentclientconnections":<Double_value>}]}```



