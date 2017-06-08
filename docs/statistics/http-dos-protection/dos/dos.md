#dos

Statistics for dos.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>clearstats</td><td>&lt;String></td><td>Read-write</td><td>Clear the statsistics / counters.&lt;br>Possible values = basic, full</td><tr><tr><td>dostotconditiontriggered</td><td>&lt;Double></td><td>Read-only</td><td>Number of times the NetScaler appliance triggered the DOS JavaScript due to a condition match.</td><tr><tr><td>dosconditiontriggeredrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for dostotconditiontriggered</td><tr><tr><td>dostotvalidcookies</td><td>&lt;Double></td><td>Read-only</td><td>Number of clients from whom the NetScaler appliance received a valid DOS cookie.</td><tr><tr><td>dosvalidcookiesrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for dostotvalidcookies</td><tr><tr><td>dostotdospriorityclients</td><td>&lt;Double></td><td>Read-only</td><td>Number of valid clients that were given DOS priority.</td><tr><tr><td>dosdospriorityclientsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for dostotdospriorityclients</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[GET (ALL)](#get-(all))


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



URL: http://NS_IP/nitro/v1/stat/dos
Query-parameters:
args
http://&lt;NSIP&gt;/nitro/v1/stat/dos?args=      detail:&lt;Boolean_value&gt;,      fullvalues:&lt;Boolean_value&gt;,      ntimes:&lt;Double_value&gt;,      logfile:&lt;String_value&gt;,      clearstats:&lt;String_value&gt;,
Use this query-parameter to get dos resources based on additional properties.



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "dos": [ {      "dostotvalidcookies":<Double_value>,      "dosvalidcookiesrate":<Double_value>,      "dosdospriorityclientsrate":<Double_value>,      "dosconditiontriggeredrate":<Double_value>,      "dostotconditiontriggered":<Double_value>,      "dostotdospriorityclients":<Double_value>}]}```



