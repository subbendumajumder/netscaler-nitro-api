#clusterinstance_clusternode_binding

Binding object showing the clusternode that can be bound to clusterinstance.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>nodeid</td><td>&lt;Double></td><td>Read-write</td><td>The unique number that identiies a cluster.<br>Minimum value = 0<br>Maximum value = 31</td></tr><tr><td>clid</td><td>&lt;Double></td><td>Read-write</td><td>Unique number that identifies the cluster.<br>Minimum value = 1<br>Maximum value = 16</td></tr><tr><td>state</td><td>&lt;String></td><td>Read-only</td><td>Active, Spare or Passive. An active node serves traffic. A spare node serves as a backup for active nodes. A passive node does not serve traffic. This may be useful during temporary maintenance activity where it is desirable that the node takes part in the consensus protocol, but not serve traffic.<br>Default value: PASSIVE<br>Possible values = ACTIVE, SPARE, PASSIVE</td></tr><tr><td>nodersskeymismatch</td><td>&lt;Boolean></td><td>Read-only</td><td>This argument is used to determine if there is a RSS key mismatch at cluster node level.</td></tr><tr><td>nodelicensemismatch</td><td>&lt;Boolean></td><td>Read-only</td><td>This argument is used to determine if there is a License mismatch at cluster node level.</td></tr><tr><td>effectivestate</td><td>&lt;String></td><td>Read-only</td><td>Node effective health state.<br>Possible values = UP, NOT UP, UNKNOWN, INIT</td></tr><tr><td>islocalnode</td><td>&lt;Boolean></td><td>Read-only</td><td>This argument is used to determine whether it is local node.</td></tr><tr><td>isconfigurationcoordinator</td><td>&lt;Boolean></td><td>Read-only</td><td>This argument is used to determine whether the node is configuration coordinator (CCO).</td></tr><tr><td>nodejumbonotsupported</td><td>&lt;Boolean></td><td>Read-only</td><td>This argument is used to determine if Jumbo framework not supported at cluster node level.</td></tr><tr><td>health</td><td>&lt;String></td><td>Read-only</td><td>Node Health state.<br>Possible values = UNKNOWN, INIT, DOWN, UP, Some enabled and HAMON interfaces of the node are down, All interfaces of the node are down or disabled, SSL card(s) of the node have failed, Route Monitor(s) of the node have failed, Service state is being synchronized with the cluster, The backplane interface is not set, is down, or is disabled, The CLAG member(s) of the node are down, Persistence sessions are being synchronized with the cluster, The Syn Cookie is being synchronized with the cluster, Unknown Health, AAA keys are being sychronized with the cluster</td></tr><tr><td>clusterhealth</td><td>&lt;String></td><td>Read-only</td><td>Node clusterd state.<br>Possible values = UP, Configurations of the node are lagging behind the cluster by more than 256 commands, The config sync operation has exceeded the time limit of 60 seconds, The config sync operation (full sync) is in progress, The node is not in sync with the cluster configurations as sync is disabled on this node, The execution of a configuration command has failed on this node, UNKNOWN</td></tr><tr><td>masterstate</td><td>&lt;String></td><td>Read-only</td><td>Master state.<br>Possible values = INACTIVE, ACTIVE, UNKNOWN</td></tr><tr><td>ipaddress</td><td>&lt;String></td><td>Read-only</td><td>The IP Address of the node.</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[GET]()| [GET (ALL)](#get-)| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/clusterinstance_clusternode_binding/clid_value&lt;Double&gt;
<b>Query-parameters:</b>
<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/clusterinstance_clusternode_binding/clid_value&lt;Double&gt;?<b>filter=property-name1:property-value1,property-name2:property-value2</b>
Use this query-parameter to get the filtered set of clusterinstance_clusternode_binding resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/clusterinstance_clusternode_binding/clid_value&lt;Double&gt;?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the clusterinstance_clusternode_binding resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "clusterinstance_clusternode_binding": [ {"nodeid":<Double_value>,"clid":<Double_value>,"state":<String_value>,"nodersskeymismatch":<Boolean_value>,"nodelicensemismatch":<Boolean_value>,"effectivestate":<String_value>,"islocalnode":<Boolean_value>,"isconfigurationcoordinator":<Boolean_value>,"nodejumbonotsupported":<Boolean_value>,"health":<String_value>,"clusterhealth":<String_value>,"masterstate":<String_value>,"ipaddress":<String_value>}]}```



###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/clusterinstance_clusternode_binding
<b>Query-parameters:</b>
<b>bulkbindings</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/clusterinstance_clusternode_binding?<b>bulkbindings=yes</b>
NITRO allows you to fetch bindings in bulk.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "clusterinstance_clusternode_binding": [ {"nodeid":<Double_value>,"clid":<Double_value>,"state":<String_value>,"nodersskeymismatch":<Boolean_value>,"nodelicensemismatch":<Boolean_value>,"effectivestate":<String_value>,"islocalnode":<Boolean_value>,"isconfigurationcoordinator":<Boolean_value>,"nodejumbonotsupported":<Boolean_value>,"health":<String_value>,"clusterhealth":<String_value>,"masterstate":<String_value>,"ipaddress":<String_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/clusterinstance_clusternode_binding/clid_value&lt;Double&gt;?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{"clusterinstance_clusternode_binding": [ { "__count": "#no"} ] }```



