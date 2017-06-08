#dospolicy

Statistics for DoS policy resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>The name of the DoS protection policy whose statistics must be displayed. If a name is not provided, statistics of all the DoS protection policies are displayed.&lt;br>Minimum length = 1</td><tr><tr><td>clearstats</td><td>&lt;String></td><td>Read-write</td><td>Clear the statsistics / counters.&lt;br>Possible values = basic, full</td><tr><tr><td>doscurrentcltdetectrate</td><td>&lt;Double></td><td>Read-only</td><td>Current ratio of JavaScript send rate to the server response rate (Client detect rate)</td><tr><tr><td>dosphysicalserviceip</td><td>&lt;String></td><td>Read-only</td><td>IP address of the service to which this policy is bound.</td><tr><tr><td>dosphysicalserviceport</td><td>&lt;Integer></td><td>Read-only</td><td>Port address of the service to which this policy is bound.</td><tr><tr><td>doscurrentqueuesize</td><td>&lt;Double></td><td>Read-only</td><td>Current queue size of the server to which this policy is bound.</td><tr><tr><td>doscurrentqueuesizerate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for doscurrentqueuesize</td><tr><tr><td>dostotjssent</td><td>&lt;Double></td><td>Read-only</td><td>Total number of DoS JavaScript transactions performed for this policy.</td><tr><tr><td>dosjssentrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for dostotjssent</td><tr><tr><td>dostotjsrefused</td><td>&lt;Double></td><td>Read-only</td><td>Number of times the DoS JavaScript was not sent because the set JavaScript rate was not met for this policy.</td><tr><tr><td>dosjsrefusedrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for dostotjsrefused</td><tr><tr><td>dostotvalidclients</td><td>&lt;Double></td><td>Read-only</td><td>Total number of valid DoS cookies received for this policy.</td><tr><tr><td>dosvalidclientsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for dostotvalidclients</td><tr><tr><td>dostotjsbytessent</td><td>&lt;Double></td><td>Read-only</td><td>Total number of DoS JavaScript bytes sent for this policy.</td><tr><tr><td>dosjsbytessentrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for dostotjsbytessent</td><tr><tr><td>dostotnongetpostrequests</td><td>&lt;Double></td><td>Read-only</td><td>Number of non-GET and non-POST requests for which DOS JavaScript was sent.</td><tr><tr><td>dosnongetpostrequestsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for dostotnongetpostrequests</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[GET (ALL)](#get-(all)) | [GET](#get)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



URL: http://NS_IP/nitro/v1/stat/dospolicy
Query-parameters:
args
http://&lt;NSIP&gt;/nitro/v1/stat/dospolicy?args=      name:&lt;String_value&gt;,      detail:&lt;Boolean_value&gt;,      fullvalues:&lt;Boolean_value&gt;,      ntimes:&lt;Double_value&gt;,      logfile:&lt;String_value&gt;,      clearstats:&lt;String_value&gt;,
Use this query-parameter to get dospolicy resources based on additional properties.



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "dospolicy": [ {      "name":<String_value>,      "dosjsrefusedrate":<Double_value>,      "dosphysicalserviceip":<String_value>,      "dosnongetpostrequestsrate":<Double_value>,      "dosjssentrate":<Double_value>,      "dosphysicalserviceport":<Integer_value>,      "dosjsbytessentrate":<Double_value>,      "doscurrentcltdetectrate":<Double_value>,      "dostotnongetpostrequests":<Double_value>,      "dostotvalidclients":<Double_value>,      "dosvalidclientsrate":<Double_value>,      "doscurrentqueuesizerate":<Double_value>,      "dostotjsbytessent":<Double_value>,      "dostotjssent":<Double_value>,      "dostotjsrefused":<Double_value>,      "doscurrentqueuesize":<Double_value>}]}```



###get



URL: http://NS_IP/nitro/v1/stat/dospolicy/name_value&lt;String&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "dospolicy": [ {      "name":<String_value>,      "dosjsrefusedrate":<Double_value>,      "dosphysicalserviceip":<String_value>,      "dosnongetpostrequestsrate":<Double_value>,      "dosjssentrate":<Double_value>,      "dosphysicalserviceport":<Integer_value>,      "dosjsbytessentrate":<Double_value>,      "doscurrentcltdetectrate":<Double_value>,      "dostotnongetpostrequests":<Double_value>,      "dostotvalidclients":<Double_value>,      "dosvalidclientsrate":<Double_value>,      "doscurrentqueuesizerate":<Double_value>,      "dostotjsbytessent":<Double_value>,      "dostotjssent":<Double_value>,      "dostotjsrefused":<Double_value>,      "doscurrentqueuesize":<Double_value>}]}```



