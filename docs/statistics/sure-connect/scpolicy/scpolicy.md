#scpolicy

Statistics for SureConnect policy resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name of the policy about which to display statistics. To display statistics about all SureConnect policies, do not set this parameter.<br>Minimum length = 1<br>Maximum length = 31</td></tr><tr><td>clearstats</td><td>&lt;String></td><td>Read-write</td><td>Clear the statsistics / counters.<br>Possible values = basic, full</td></tr><tr><td>avgservertransactiontime</td><td>&lt;Double></td><td>Read-only</td><td>Average server transaction time in seconds for this SureConnect Policy.</td></tr><tr><td>avgservertransactiontimerate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for avgservertransactiontime</td></tr><tr><td>scaverageclientttlb</td><td>&lt;Double></td><td>Read-only</td><td>Average value of the client Time-To-Last-Byte in seconds for this SureConnect policy.</td></tr><tr><td>scaverageclientttlbrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for scaverageclientttlb</td></tr><tr><td>scphysicalserviceip</td><td>&lt;String></td><td>Read-only</td><td>IP address of the service in dotted notation for which these statistics are maintained.</td></tr><tr><td>scphysicalserviceport</td><td>&lt;Integer></td><td>Read-only</td><td>Port of the service for which these statistics are maintained.</td></tr><tr><td>sccurrentclientconnections</td><td>&lt;Double></td><td>Read-only</td><td>Number of clients currently allowed a server connection by this SureConnect policy.</td></tr><tr><td>sccurrentclientconnectionsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for sccurrentclientconnections</td></tr><tr><td>sccurrentwaitingclients</td><td>&lt;Double></td><td>Read-only</td><td>Current number of SureConnect priority clients that are waiting for a server connection.</td></tr><tr><td>sccurrentwaitingclientsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for sccurrentwaitingclients</td></tr><tr><td>totopenconn</td><td>&lt;Double></td><td>Read-only</td><td>Current number of open connections to the servers matching this policy.</td></tr><tr><td>openconnrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for totopenconn</td></tr><tr><td>sccurrentwaitingtime</td><td>&lt;Double></td><td>Read-only</td><td>Value of the currently estimated waiting time in seconds for the configured URL.</td></tr><tr><td>sccurrentwaitingtimerate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for sccurrentwaitingtime</td></tr><tr><td>sctotalclientconnections</td><td>&lt;Double></td><td>Read-only</td><td>Total number of clients that were allowed a server connection by this SureConnect policy.</td></tr><tr><td>scclientconnectionsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for sctotalclientconnections</td></tr><tr><td>sctotalserverconnections</td><td>&lt;Double></td><td>Read-only</td><td>Total number of server connections that were established through this SureConnect policy.</td></tr><tr><td>scserverconnectionsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for sctotalserverconnections</td></tr><tr><td>totclienttransaction</td><td>&lt;Double></td><td>Read-only</td><td>Total number of client transactions processed by this SureConnect policy.</td></tr><tr><td>clienttransactionrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for totclienttransaction</td></tr><tr><td>sctotalservertransactions</td><td>&lt;Double></td><td>Read-only</td><td>Number of 200 OK responses received from the web server by this SureConnect policy.</td></tr><tr><td>scservertransactionsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for sctotalservertransactions</td></tr><tr><td>sctotalrequestsreceived</td><td>&lt;Double></td><td>Read-only</td><td>Total number of requests received by this SureConnect policy.</td></tr><tr><td>screquestsreceivedrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for sctotalrequestsreceived</td></tr><tr><td>sctotalrequestbytes</td><td>&lt;Double></td><td>Read-only</td><td>Total number of request bytes received by this SureConnect policy.</td></tr><tr><td>screquestbytesrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for sctotalrequestbytes</td></tr><tr><td>sctotalresponsesreceived</td><td>&lt;Double></td><td>Read-only</td><td>Total number of server responses received by this SureConnect policy.</td></tr><tr><td>scresponsesreceivedrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for sctotalresponsesreceived</td></tr><tr><td>sctotalresponsebytes</td><td>&lt;Double></td><td>Read-only</td><td>Total number of response bytes received by this SureConnect policy.</td></tr><tr><td>scresponsebytesrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for sctotalresponsebytes</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[GET (ALL)](#get-)| [GET]()


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/scpolicy
<b>Query-parameters:</b>
<b>args</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/scpolicy?<b>args=name:&lt;String_value&gt;,detail:&lt;Boolean_value&gt;,fullvalues:&lt;Boolean_value&gt;,ntimes:&lt;Double_value&gt;,logfile:&lt;String_value&gt;,clearstats:&lt;String_value&gt;</b>
Use this query-parameter to get scpolicy resources based on additional properties.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "scpolicy": [ {"name":<String_value>,"sctotalresponsesreceived":<Double_value>,"sccurrentwaitingtime":<Double_value>,"clienttransactionrate":<Double_value>,"sccurrentwaitingtimerate":<Double_value>,"sccurrentwaitingclients":<Double_value>,"sctotalrequestsreceived":<Double_value>,"screquestsreceivedrate":<Double_value>,"scresponsebytesrate":<Double_value>,"screquestbytesrate":<Double_value>,"sctotalresponsebytes":<Double_value>,"scserverconnectionsrate":<Double_value>,"sctotalservertransactions":<Double_value>,"sccurrentwaitingclientsrate":<Double_value>,"scaverageclientttlb":<Double_value>,"avgservertransactiontime":<Double_value>,"scphysicalserviceip":<String_value>,"sccurrentclientconnectionsrate":<Double_value>,"sccurrentclientconnections":<Double_value>,"openconnrate":<Double_value>,"scclientconnectionsrate":<Double_value>,"scaverageclientttlbrate":<Double_value>,"totclienttransaction":<Double_value>,"scservertransactionsrate":<Double_value>,"sctotalclientconnections":<Double_value>,"scphysicalserviceport":<Integer_value>,"totopenconn":<Double_value>,"avgservertransactiontimerate":<Double_value>,"scresponsesreceivedrate":<Double_value>,"sctotalrequestbytes":<Double_value>,"sctotalserverconnections":<Double_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/scpolicy/name_value&gt;&lt;String&gt;
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "scpolicy": [ {"name":<String_value>,"sctotalresponsesreceived":<Double_value>,"sccurrentwaitingtime":<Double_value>,"clienttransactionrate":<Double_value>,"sccurrentwaitingtimerate":<Double_value>,"sccurrentwaitingclients":<Double_value>,"sctotalrequestsreceived":<Double_value>,"screquestsreceivedrate":<Double_value>,"scresponsebytesrate":<Double_value>,"screquestbytesrate":<Double_value>,"sctotalresponsebytes":<Double_value>,"scserverconnectionsrate":<Double_value>,"sctotalservertransactions":<Double_value>,"sccurrentwaitingclientsrate":<Double_value>,"scaverageclientttlb":<Double_value>,"avgservertransactiontime":<Double_value>,"scphysicalserviceip":<String_value>,"sccurrentclientconnectionsrate":<Double_value>,"sccurrentclientconnections":<Double_value>,"openconnrate":<Double_value>,"scclientconnectionsrate":<Double_value>,"scaverageclientttlbrate":<Double_value>,"totclienttransaction":<Double_value>,"scservertransactionsrate":<Double_value>,"sctotalclientconnections":<Double_value>,"scphysicalserviceport":<Integer_value>,"totopenconn":<Double_value>,"avgservertransactiontimerate":<Double_value>,"scresponsesreceivedrate":<Double_value>,"sctotalrequestbytes":<Double_value>,"sctotalserverconnections":<Double_value>}]}```



