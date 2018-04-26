#appqoepolicy

Statistics for AppQoS policy resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>policyName.<br>Minimum length = 1</td></tr><tr><td>clearstats</td><td>&lt;String></td><td>Read-write</td><td>Clear the statsistics / counters.<br>Possible values = basic, full</td></tr><tr><td>qosavgserverttfb</td><td>&lt;Double></td><td>Read-only</td><td>Average Server Time-To-First-Byte in milliseconds calculated for this AppQoE policy.</td></tr><tr><td>qosavgserverttfbrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for qosavgserverttfb</td></tr><tr><td>qosavgserverttlb</td><td>&lt;Double></td><td>Read-only</td><td>Average Server Time-To-Last-Byte in milliseconds calculated for this AppQoE policy.</td></tr><tr><td>qosavgserverttlbrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for qosavgserverttlb</td></tr><tr><td>qosavgclientttlb</td><td>&lt;Double></td><td>Read-only</td><td>Average Client Time-To-Last-Byte in milliseconds calculated for this AppQoE policy.</td></tr><tr><td>qosavgclientttlbrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for qosavgclientttlb</td></tr><tr><td>totthroughput</td><td>&lt;Double></td><td>Read-only</td><td>Throughput in Kbps calculated on this AppQoE policy</td></tr><tr><td>throughputrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for totthroughput</td></tr><tr><td>totsvrlinkedto</td><td>&lt;Double></td><td>Read-only</td><td>Total number of server connections that were established through this AppQoE Policy</td></tr><tr><td>svrlinkedtorate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for totsvrlinkedto</td></tr><tr><td>totcltrequests</td><td>&lt;Double></td><td>Read-only</td><td>Total number of client connections that were requested through this AppQoE Policy</td></tr><tr><td>cltrequestsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for totcltrequests</td></tr><tr><td>totrequests</td><td>&lt;Double></td><td>Read-only</td><td>Total number of requests that were requested through this AppQoE policy</td></tr><tr><td>requestsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for totrequests</td></tr><tr><td>totrequestbytes</td><td>&lt;Double></td><td>Read-only</td><td>Total number of requests bytes that were requested through this AppQoE policy</td></tr><tr><td>requestbytesrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for totrequestbytes</td></tr><tr><td>totresponse</td><td>&lt;Double></td><td>Read-only</td><td>Total number of responses received by this AppQoE policy</td></tr><tr><td>responserate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for totresponse</td></tr><tr><td>totresponsebytes</td><td>&lt;Double></td><td>Read-only</td><td>Total number of response bytes received by this AppQoE policy</td></tr><tr><td>responsebytesrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for totresponsebytes</td></tr><tr><td>totjssent</td><td>&lt;Double></td><td>Read-only</td><td>Total number of in-memory responses sent instead of expected responses through this AppQoE policy</td></tr><tr><td>jssentrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for totjssent</td></tr><tr><td>totjsbytessent</td><td>&lt;Double></td><td>Read-only</td><td>Total bytes of in-memory responses sent through this AppQoE policy</td></tr><tr><td>jsbytessentrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for totjsbytessent</td></tr><tr><td>pipolicyhits</td><td>&lt;Double></td><td>Read-only</td><td>Number of hits on the policy</td></tr><tr><td>pipolicyhitsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for pipolicyhits</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[GET (ALL)](#get-)| [GET]()


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/appqoepolicy
<b>Query-parameters:</b>
<b>args</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/appqoepolicy?<b>args=name:&lt;String_value&gt;,detail:&lt;Boolean_value&gt;,fullvalues:&lt;Boolean_value&gt;,ntimes:&lt;Double_value&gt;,logfile:&lt;String_value&gt;,clearstats:&lt;String_value&gt;</b>
Use this query-parameter to get appqoepolicy resources based on additional properties.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "appqoepolicy": [ {"name":<String_value>,"qosavgclientttlbrate":<Double_value>,"totjssent":<Double_value>,"responsebytesrate":<Double_value>,"totthroughput":<Double_value>,"requestbytesrate":<Double_value>,"totjsbytessent":<Double_value>,"svrlinkedtorate":<Double_value>,"totresponse":<Double_value>,"totresponsebytes":<Double_value>,"jssentrate":<Double_value>,"qosavgserverttfbrate":<Double_value>,"pipolicyhits":<Double_value>,"qosavgclientttlb":<Double_value>,"totcltrequests":<Double_value>,"totrequests":<Double_value>,"qosavgserverttlbrate":<Double_value>,"totrequestbytes":<Double_value>,"cltrequestsrate":<Double_value>,"throughputrate":<Double_value>,"totsvrlinkedto":<Double_value>,"qosavgserverttfb":<Double_value>,"pipolicyhitsrate":<Double_value>,"jsbytessentrate":<Double_value>,"responserate":<Double_value>,"requestsrate":<Double_value>,"qosavgserverttlb":<Double_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/appqoepolicy/name_value&gt;&lt;String&gt;
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "appqoepolicy": [ {"name":<String_value>,"qosavgclientttlbrate":<Double_value>,"totjssent":<Double_value>,"responsebytesrate":<Double_value>,"totthroughput":<Double_value>,"requestbytesrate":<Double_value>,"totjsbytessent":<Double_value>,"svrlinkedtorate":<Double_value>,"totresponse":<Double_value>,"totresponsebytes":<Double_value>,"jssentrate":<Double_value>,"qosavgserverttfbrate":<Double_value>,"pipolicyhits":<Double_value>,"qosavgclientttlb":<Double_value>,"totcltrequests":<Double_value>,"totrequests":<Double_value>,"qosavgserverttlbrate":<Double_value>,"totrequestbytes":<Double_value>,"cltrequestsrate":<Double_value>,"throughputrate":<Double_value>,"totsvrlinkedto":<Double_value>,"qosavgserverttfb":<Double_value>,"pipolicyhitsrate":<Double_value>,"jsbytessentrate":<Double_value>,"responserate":<Double_value>,"requestsrate":<Double_value>,"qosavgserverttlb":<Double_value>}]}```



