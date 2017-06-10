#aaa

Statistics for aaa.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>clearstats</td><td>&lt;String></td><td>Read-write</td><td>Clear the statsistics / counters.&lt;br>Possible values = basic, full</td><tr><tr><td>aaaauthsuccess</td><td>&lt;Double></td><td>Read-only</td><td>Count of authentication successes.</td><tr><tr><td>aaaauthsuccessrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for aaaauthsuccess</td><tr><tr><td>aaaauthfail</td><td>&lt;Double></td><td>Read-only</td><td>Count of authentication failures.</td><tr><tr><td>aaaauthfailrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for aaaauthfail</td><tr><tr><td>aaaauthonlyhttpsuccess</td><td>&lt;Double></td><td>Read-only</td><td>Count of HTTP connections that succeeded authorization.</td><tr><tr><td>aaaauthonlyhttpsuccessrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for aaaauthonlyhttpsuccess</td><tr><tr><td>aaaauthonlyhttpfail</td><td>&lt;Double></td><td>Read-only</td><td>Count of HTTP connections that failed authorization.</td><tr><tr><td>aaaauthonlyhttpfailrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for aaaauthonlyhttpfail</td><tr><tr><td>aaaauthnonhttpsuccess</td><td>&lt;Double></td><td>Read-only</td><td>Count of non HTTP connections that succeeded authorization.</td><tr><tr><td>aaaauthnonhttpsuccessrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for aaaauthnonhttpsuccess</td><tr><tr><td>aaaauthnonhttpfail</td><td>&lt;Double></td><td>Read-only</td><td>Count of non HTTP connections that failed authorization.</td><tr><tr><td>aaaauthnonhttpfailrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for aaaauthnonhttpfail</td><tr><tr><td>aaacursessions</td><td>&lt;Double></td><td>Read-only</td><td>Count of current SmartAccess AAA sessions.</td><tr><tr><td>aaacursessionsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for aaacursessions</td><tr><tr><td>aaatotsessions</td><td>&lt;Double></td><td>Read-only</td><td>Count of all SmartAccess AAA sessions.</td><tr><tr><td>aaasessionsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for aaatotsessions</td><tr><tr><td>aaatotsessiontimeout</td><td>&lt;Double></td><td>Read-only</td><td>Count of AAA sessions that have timed out.</td><tr><tr><td>aaasessiontimeoutrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for aaatotsessiontimeout</td><tr><tr><td>aaacuricasessions</td><td>&lt;Double></td><td>Read-only</td><td>Count of current Basic ICA only sessions.</td><tr><tr><td>aaacuricasessionsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for aaacuricasessions</td><tr><tr><td>aaacuricaonlyconn</td><td>&lt;Double></td><td>Read-only</td><td>Count of current Basic ICA only connections.</td><tr><tr><td>aaacuricaonlyconnrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for aaacuricaonlyconn</td><tr><tr><td>aaacuricaconn</td><td>&lt;Double></td><td>Read-only</td><td>Count of current SmartAccess ICA connections.</td><tr><tr><td>aaacuricaconnrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for aaacuricaconn</td><tr><tr><td>aaacurtmsessions</td><td>&lt;Double></td><td>Read-only</td><td>Count of current AAATM sessions.</td><tr><tr><td>aaacurtmsessionsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for aaacurtmsessions</td><tr><tr><td>aaatottmsessions</td><td>&lt;Double></td><td>Read-only</td><td>Count of all AAATM sessions.</td><tr><tr><td>aaatmsessionsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for aaatottmsessions</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[GET (ALL)](#get-(all))


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/aaa
Query-parameters:
args
http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/aaa?args=detail:&lt;Boolean_value&gt;,fullvalues:&lt;Boolean_value&gt;,ntimes:&lt;Double_value&gt;,logfile:&lt;String_value&gt;,clearstats:&lt;String_value&gt;
Use this query-parameter to get aaa resources based on additional properties.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "aaa": [ {      "aaatotsessiontimeout":<Double_value>,      "aaaauthfail":<Double_value>,      "aaaauthsuccess":<Double_value>,      "aaatottmsessions":<Double_value>,      "aaaauthonlyhttpfailrate":<Double_value>,      "aaaauthnonhttpsuccess":<Double_value>,      "aaacuricaonlyconnrate":<Double_value>,      "aaaauthonlyhttpsuccessrate":<Double_value>,      "aaacurtmsessions":<Double_value>,      "aaacuricasessions":<Double_value>,      "aaatotsessions":<Double_value>,      "aaaauthonlyhttpfail":<Double_value>,      "aaacuricaonlyconn":<Double_value>,      "aaatmsessionsrate":<Double_value>,      "aaaauthfailrate":<Double_value>,      "aaacursessionsrate":<Double_value>,      "aaaauthnonhttpsuccessrate":<Double_value>,      "aaacuricaconn":<Double_value>,      "aaaauthnonhttpfailrate":<Double_value>,      "aaaauthnonhttpfail":<Double_value>,      "aaacuricaconnrate":<Double_value>,      "aaaauthsuccessrate":<Double_value>,      "aaaauthonlyhttpsuccess":<Double_value>,      "aaacurtmsessionsrate":<Double_value>,      "aaasessiontimeoutrate":<Double_value>,      "aaacuricasessionsrate":<Double_value>,      "aaacursessions":<Double_value>,      "aaasessionsrate":<Double_value>}]}```



