#sc

Statistics for sc.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>clearstats</td><td>&lt;String></td><td>Read-write</td><td>Clear the statsistics / counters.&lt;br>Possible values = basic, full</td><tr><tr><td>sctotcondtriggered</td><td>&lt;Double></td><td>Read-only</td><td>Number of times that SureConnect conditions were triggered.</td><tr><tr><td>sccondtriggeredrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for sctotcondtriggered</td><tr><tr><td>scpolicyurlhits</td><td>&lt;Double></td><td>Read-only</td><td>Total number of incoming requests that matched configured sureconnect policies.</td><tr><tr><td>scpolicyurlhitsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for scpolicyurlhits</td><tr><tr><td>scpopups</td><td>&lt;Double></td><td>Read-only</td><td>Total number of in-memory java script served which throws the pop-up window.</td><tr><tr><td>scpopupsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for scpopups</td><tr><tr><td>sctotreissuedrequests</td><td>&lt;Double></td><td>Read-only</td><td>Total number of reissued SureConnect requests.</td><tr><tr><td>screissuedrequestsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for sctotreissuedrequests</td><tr><tr><td>scsessionreqs</td><td>&lt;Double></td><td>Read-only</td><td>Total number of requests that were handled in a single SureConnect session.</td><tr><tr><td>scsessionreqsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for scsessionreqs</td><tr><tr><td>scaltconturls</td><td>&lt;Double></td><td>Read-only</td><td>Total number of alternate content served which throws the pop-up window.</td><tr><tr><td>scaltconturlsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for scaltconturls</td><tr><tr><td>scpostreqs</td><td>&lt;Double></td><td>Read-only</td><td>Total number of HTTP POST requests that triggered SureConnect feature.</td><tr><tr><td>scpostreqsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for scpostreqs</td><tr><tr><td>scresetstats</td><td>&lt;Double></td><td>Read-only</td><td>Toal number of times that SureConnect statistics were reset.</td><tr><tr><td>scresetstatsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for scresetstats</td><tr><tr><td>scunsupbrow</td><td>&lt;Double></td><td>Read-only</td><td>Total number of requests that came from all unsupported browsers.</td><tr><tr><td>scunsupbrowrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for scunsupbrow</td><tr><tr><td>scfaultycookies</td><td>&lt;Double></td><td>Read-only</td><td>Total number of corrupted SureConnect cookies.</td><tr><tr><td>scfaultycookiesrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for scfaultycookies</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[GET (ALL)](#get-(all))


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



URL: http://NS_IP/nitro/v1/stat/sc
Query-parameters:
args
http://&lt;NSIP&gt;/nitro/v1/stat/sc?args=      detail:&lt;Boolean_value&gt;,      fullvalues:&lt;Boolean_value&gt;,      ntimes:&lt;Double_value&gt;,      logfile:&lt;String_value&gt;,      clearstats:&lt;String_value&gt;,
Use this query-parameter to get sc resources based on additional properties.



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "sc": [ {      "scpopups":<Double_value>,      "scfaultycookiesrate":<Double_value>,      "screissuedrequestsrate":<Double_value>,      "scpostreqs":<Double_value>,      "scaltconturls":<Double_value>,      "scresetstatsrate":<Double_value>,      "scpopupsrate":<Double_value>,      "sctotreissuedrequests":<Double_value>,      "scunsupbrow":<Double_value>,      "scpolicyurlhitsrate":<Double_value>,      "sccondtriggeredrate":<Double_value>,      "scpolicyurlhits":<Double_value>,      "scsessionreqsrate":<Double_value>,      "scresetstats":<Double_value>,      "sctotcondtriggered":<Double_value>,      "scfaultycookies":<Double_value>,      "scsessionreqs":<Double_value>,      "scaltconturlsrate":<Double_value>,      "scunsupbrowrate":<Double_value>,      "scpostreqsrate":<Double_value>}]}```



