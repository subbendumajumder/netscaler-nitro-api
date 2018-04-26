#clusternode

Configuration for cluster node resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>nodeid</td><td>&lt;Double></td><td>Read-write</td><td>Unique number that identifies the cluster node.<br>Minimum value = 0<br>Maximum value = 31</td></tr><tr><td>ipaddress</td><td>&lt;String></td><td>Read-write</td><td>NetScaler IP (NSIP) address of the appliance to add to the cluster. Must be an IPv4 address.<br>Minimum length = 1</td></tr><tr><td>state</td><td>&lt;String></td><td>Read-write</td><td>Admin state of the cluster node. The available settings function as follows:<br>ACTIVE - The node serves traffic.<br>SPARE - The node does not serve traffic unless an ACTIVE node goes down.<br>PASSIVE - The node does not serve traffic, unless you change its state. PASSIVE state is useful during temporary maintenance activities in which you want the node to take part in the consensus protocol but not to serve traffic.<br>Default value: PASSIVE<br>Possible values = ACTIVE, SPARE, PASSIVE</td></tr><tr><td>backplane</td><td>&lt;String></td><td>Read-write</td><td>Interface through which the node communicates with the other nodes in the cluster. Must be specified in the three-tuple form n/c/u, where n represents the node ID and c/u refers to the interface on the appliance.<br>Minimum length = 1</td></tr><tr><td>priority</td><td>&lt;Double></td><td>Read-write</td><td>Preference for selecting a node as the configuration coordinator. The node with the lowest priority value is selected as the configuration coordinator.<br>When the current configuration coordinator goes down, the node with the next lowest priority is made the new configuration coordinator. When the original node comes back up, it will preempt the new configuration coordinator and take over as the configuration coordinator.<br>Note: When priority is not configured for any of the nodes or if multiple nodes have the same priority, the cluster elects one of the nodes as the configuration coordinator.<br>Default value: 31<br>Minimum value = 0<br>Maximum value = 31</td></tr><tr><td>nodegroup</td><td>&lt;String></td><td>Read-write</td><td>The default node group in a Cluster system.<br>Default value: DEFAULT_NG<br>Minimum length = 1</td></tr><tr><td>delay</td><td>&lt;Double></td><td>Read-write</td><td>Applicable for Passive node and node becomes passive after this timeout (in minutes).<br>Default value: 0<br>Minimum value = 0<br>Maximum value = 1440</td></tr><tr><td>clearnodegroupconfig</td><td>&lt;String></td><td>Read-write</td><td>Option to remove nodegroup config.<br>Default value: YES<br>Possible values = YES, NO</td></tr><tr><td>clusterhealth</td><td>&lt;String></td><td>Read-only</td><td>Node clusterd state.<br>Possible values = UP, Configurations of the node are lagging behind the cluster by more than 256 commands, The config sync operation has exceeded the time limit of 60 seconds, The config sync operation (full sync) is in progress, The node is not in sync with the cluster configurations as sync is disabled on this node, The execution of a configuration command has failed on this node, UNKNOWN</td></tr><tr><td>effectivestate</td><td>&lt;String></td><td>Read-only</td><td>Node effective health state.<br>Possible values = UP, NOT UP, UNKNOWN, INIT</td></tr><tr><td>operationalsyncstate</td><td>&lt;String></td><td>Read-only</td><td>Node Operational Reconciliation state.<br>Default value: ENABLED<br>Possible values = ENABLED, SUCCESS, IN PROGRESS, FAILED, INCREMENTAL SYNC DISABLED, DISABLED, UNKNOWN</td></tr><tr><td>masterstate</td><td>&lt;String></td><td>Read-only</td><td>Node Master state.<br>Possible values = INACTIVE, ACTIVE, UNKNOWN</td></tr><tr><td>health</td><td>&lt;String></td><td>Read-only</td><td>Node Health state.<br>Possible values = UNKNOWN, INIT, DOWN, UP, Some enabled and HAMON interfaces of the node are down, All interfaces of the node are down or disabled, SSL card(s) of the node have failed, Route Monitor(s) of the node have failed, Service state is being synchronized with the cluster, The backplane interface is not set, is down, or is disabled, The CLAG member(s) of the node are down, Persistence sessions are being synchronized with the cluster, The Syn Cookie is being synchronized with the cluster, Unknown Health, AAA keys are being sychronized with the cluster</td></tr><tr><td>syncstate</td><td>&lt;String></td><td>Read-only</td><td>Enable/Disable the synchronization of cluster configurations on the node.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>isconfigurationcoordinator</td><td>&lt;Boolean></td><td>Read-only</td><td>This argument is used to determine whether the node is configuration coordinator (CCO).</td></tr><tr><td>islocalnode</td><td>&lt;Boolean></td><td>Read-only</td><td>This argument is used to determine whether it is local node.</td></tr><tr><td>nodersskeymismatch</td><td>&lt;Boolean></td><td>Read-only</td><td>This argument is used to determine if there is a RSS key mismatch at cluster node level.</td></tr><tr><td>nodelicensemismatch</td><td>&lt;Boolean></td><td>Read-only</td><td>This argument is used to determine if there is a License mismatch at cluster node level.</td></tr><tr><td>nodejumbonotsupported</td><td>&lt;Boolean></td><td>Read-only</td><td>This argument is used to determine if Jumbo framework not supported at cluster node level.</td></tr><tr><td>nodelist</td><td>&lt;Double[]></td><td>Read-only</td><td>Nodelist for displaying Heartbeat not seen interfaces on a cluster node.</td></tr><tr><td>ifaceslist</td><td>&lt;String[]></td><td>Read-only</td><td>Interface list corresponding to nodelist for Heartbeat not seen interfaces on a cluster node.</td></tr><tr><td>enabledifaces</td><td>&lt;String></td><td>Read-only</td><td>Enabled Interfaces on a cluster node.</td></tr><tr><td>disabledifaces</td><td>&lt;String></td><td>Read-only</td><td>Disabled Interfaces on a cluster node.</td></tr><tr><td>partialfailifaces</td><td>&lt;String></td><td>Read-only</td><td>Partial Failure Interfaces on a cluster node.</td></tr><tr><td>hamonifaces</td><td>&lt;String></td><td>Read-only</td><td>Hamon Interfaces on a cluster node.</td></tr><tr><td>name</td><td>&lt;String></td><td>Read-only</td><td>Name of the state specific nodegroup.<br>Minimum length = 1</td></tr><tr><td>cfgflags</td><td>&lt;Double></td><td>Read-only</td><td>Flag indicates whether the node is bound to cluster nodegroup.</td></tr><tr><td>routemonitor</td><td>&lt;String></td><td>Read-only</td><td>The IP address (IPv4 or IPv6).</td></tr><tr><td>netmask</td><td>&lt;String></td><td>Read-only</td><td>The netmask.</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD]()| [UPDATE](#u)| [UNSET](#)| [DELETE](#d)| [GET (ALL)](#get-)| [GET]()| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/clusternode
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"clusternode":{<b>"nodeid":<Double_value>,</b><b>"ipaddress":<String_value>,</b>"state":<String_value>,"backplane":<String_value>,"priority":<Double_value>,"nodegroup":<String_value>,"delay":<Double_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/clusternode
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"clusternode":{<b>"nodeid":<Double_value>,</b>"state":<String_value>,"backplane":<String_value>,"priority":<Double_value>,"delay":<Double_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/clusternode?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"clusternode":{<b>"nodeid":<Double_value>,</b>"state":true,"backplane":true,"priority":true,"delay":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/clusternode/nodeid_value&lt;Double&gt;
<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/clusternode
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/clusternode?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/clusternode?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of clusternode resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/clusternode?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/clusternode?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the clusternode resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "clusternode": [ {"nodeid":<Double_value>,"ipaddress":<String_value>,"clusterhealth":<String_value>,"effectivestate":<String_value>,"operationalsyncstate":<String_value>,"masterstate":<String_value>,"health":<String_value>,"state":<String_value>,"backplane":<String_value>,"syncstate":<String_value>,"priority":<Double_value>,"isconfigurationcoordinator":<Boolean_value>,"islocalnode":<Boolean_value>,"nodersskeymismatch":<Boolean_value>,"nodelicensemismatch":<Boolean_value>,"nodejumbonotsupported":<Boolean_value>,"nodelist":<Double[]_value>,"ifaceslist":<String[]_value>,"enabledifaces":<String_value>,"disabledifaces":<String_value>,"partialfailifaces":<String_value>,"hamonifaces":<String_value>,"nodegroup":<String_value>,"name":<String_value>,"cfgflags":<Double_value>,"routemonitor":<String_value>,"netmask":<String_value>,"delay":<Double_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/clusternode/nodeid_value&lt;Double&gt;
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/clusternode/nodeid_value&lt;Double&gt;?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/clusternode/nodeid_value&lt;Double&gt;?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "clusternode": [ {"nodeid":<Double_value>,"ipaddress":<String_value>,"clusterhealth":<String_value>,"effectivestate":<String_value>,"operationalsyncstate":<String_value>,"masterstate":<String_value>,"health":<String_value>,"state":<String_value>,"backplane":<String_value>,"syncstate":<String_value>,"priority":<Double_value>,"isconfigurationcoordinator":<Boolean_value>,"islocalnode":<Boolean_value>,"nodersskeymismatch":<Boolean_value>,"nodelicensemismatch":<Boolean_value>,"nodejumbonotsupported":<Boolean_value>,"nodelist":<Double[]_value>,"ifaceslist":<String[]_value>,"enabledifaces":<String_value>,"disabledifaces":<String_value>,"partialfailifaces":<String_value>,"hamonifaces":<String_value>,"nodegroup":<String_value>,"name":<String_value>,"cfgflags":<Double_value>,"routemonitor":<String_value>,"netmask":<String_value>,"delay":<Double_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/clusternode?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "clusternode": [ { "__count": "#no"} ] }```



