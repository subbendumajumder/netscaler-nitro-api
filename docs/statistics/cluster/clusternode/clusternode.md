#clusternode

Statistics for cluster node resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>nodeid</td><td>&lt;Double></td><td>Read-write</td><td>ID of the cluster node for which to display statistics. If an ID is not provided, statistics are shown for all nodes.&lt;br>Minimum value = 0&lt;br>Maximum value = 31</td><tr><tr><td>clearstats</td><td>&lt;String></td><td>Read-write</td><td>Clear the statsistics / counters.&lt;br>Possible values = basic, full</td><tr><tr><td>clsyncstate</td><td>&lt;String></td><td>Read-only</td><td>Sync state of the cluster node.</td><tr><tr><td>clnodeeffectivehealth</td><td>&lt;String></td><td>Read-only</td><td>Health of the cluster node.</td><tr><tr><td>clnodeip</td><td>&lt;String></td><td>Read-only</td><td>NSIP address of the cluster node.</td><tr><tr><td>clmasterstate</td><td>&lt;String></td><td>Read-only</td><td>Operational state of the cluster node.</td><tr><tr><td>cltothbtx</td><td>&lt;Double></td><td>Read-only</td><td>Number of heartbeats sent. When executed from the NSIP address, shows the statistics for local node only. For remote node it shows a value of 0. When executed from the cluster IP address, shows all the statistics.</td><tr><tr><td>cltothbrx</td><td>&lt;Double></td><td>Read-only</td><td>Number of heartbeats received. When executed from the NSIP address, shows the statistics for local node only. For remote node it shows a value of 0. When executed from the cluster IP address, shows all the statistics.</td><tr><tr><td>nnmcurconn</td><td>&lt;Double></td><td>Read-only</td><td>Number of connections open for node-to-node communication.</td><tr><tr><td>nnmtotconntx</td><td>&lt;Double></td><td>Read-only</td><td>Number of node-to-node messages sent. When executed from the NSIP address, shows the statistics for local node only. For remote node it shows a value of 0. When executed from the cluster IP address, shows all the statistics.</td><tr><tr><td>nnmtotconnrx</td><td>&lt;Double></td><td>Read-only</td><td>Number of node-to-node messages received. When executed from the NSIP address, shows the statistics for local node only. For remote node it shows a value of 0. When executed from the cluster IP address, shows all the statistics.</td><tr><tr><td>clptpstate</td><td>&lt;String></td><td>Read-only</td><td>PTP state of the node. This state is Master for one node and Slave for the rest. When executed from the NSIP address, shows the statistics for local node only. For remote node it shows UNKNOWN. When executed from the cluster IP address, shows all the statistics.</td><tr><tr><td>clptptx</td><td>&lt;Double></td><td>Read-only</td><td>Number of PTP packets transmitted by the node. When executed from the NSIP address, shows the statistics for local node only. For remote node it shows a value of 0. When executed from the cluster IP address, shows all the statistics.</td><tr><tr><td>clptprx</td><td>&lt;Double></td><td>Read-only</td><td>Number of PTP packets received on the node. When executed from the NSIP address, shows the statistics for local node only. For remote node it shows a value of 0. When executed from the cluster IP address, shows all the statistics.</td><tr><tr><td>nnmerrmsend</td><td>&lt;Double></td><td>Read-only</td><td>Number of errors in sending node-to-node multicast/broadcast messages. When executed from the NSIP address, shows the statistics for local node only. For remote node it shows a value of 0. When executed from the cluster IP address, shows all the statistics.</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[GET (ALL)](#get-(all)) | [GET](#get)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



URL: http://NS_IP/nitro/v1/stat/clusternode
Query-parameters:
args
http://&lt;NSIP&gt;/nitro/v1/stat/clusternode?args=      nodeid:&lt;Double_value&gt;,      detail:&lt;Boolean_value&gt;,      fullvalues:&lt;Boolean_value&gt;,      ntimes:&lt;Double_value&gt;,      logfile:&lt;String_value&gt;,      clearstats:&lt;String_value&gt;,
Use this query-parameter to get clusternode resources based on additional properties.



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "clusternode": [ {      "nodeid":<Double_value>,      "clnodeip":<String_value>,      "clsyncstate":<String_value>,      "nnmcurconn":<Double_value>,      "nnmerrmsend":<Double_value>,      "clnodeeffectivehealth":<String_value>,      "nnmtotconnrx":<Double_value>,      "cltothbrx":<Double_value>,      "clptprx":<Double_value>,      "nnmtotconntx":<Double_value>,      "clmasterstate":<String_value>,      "clptptx":<Double_value>,      "clptpstate":<String_value>,      "cltothbtx":<Double_value>}]}```



###get



URL: http://NS_IP/nitro/v1/stat/clusternode/nodeid_value&lt;Double&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "clusternode": [ {      "nodeid":<Double_value>,      "clnodeip":<String_value>,      "clsyncstate":<String_value>,      "nnmcurconn":<Double_value>,      "nnmerrmsend":<Double_value>,      "clnodeeffectivehealth":<String_value>,      "nnmtotconnrx":<Double_value>,      "cltothbrx":<Double_value>,      "clptprx":<Double_value>,      "nnmtotconntx":<Double_value>,      "clmasterstate":<String_value>,      "clptptx":<Double_value>,      "clptpstate":<String_value>,      "cltothbtx":<Double_value>}]}```



