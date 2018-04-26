#clusterinstance

Configuration for cluster instance resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>clid</td><td>&lt;Double></td><td>Read-write</td><td>Unique number that identifies the cluster.<br>Minimum value = 1<br>Maximum value = 16</td></tr><tr><td>deadinterval</td><td>&lt;Double></td><td>Read-write</td><td>Amount of time, in seconds, after which nodes that do not respond to the heartbeats are assumed to be down.If the value is less than 3 sec, set the helloInterval parameter to 200 msec.<br>Default value: 3<br>Minimum value = 1<br>Maximum value = 60</td></tr><tr><td>hellointerval</td><td>&lt;Double></td><td>Read-write</td><td>Interval, in milliseconds, at which heartbeats are sent to each cluster node to check the health status.Set the value to 200 msec, if the deadInterval parameter is less than 3 sec.<br>Default value: 200<br>Minimum value = 200<br>Maximum value = 1000</td></tr><tr><td>preemption</td><td>&lt;String></td><td>Read-write</td><td>Preempt a cluster node that is configured as a SPARE if an ACTIVE node becomes available.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>quorumtype</td><td>&lt;String></td><td>Read-write</td><td>Quorum Configuration Choices - "Majority" (recommended) requires majority of nodes to be online for the cluster to be UP. "None" relaxes this requirement.<br>Default value: MAJORITY<br>Possible values = MAJORITY, NONE</td></tr><tr><td>inc</td><td>&lt;String></td><td>Read-write</td><td>This option is required if the cluster nodes reside on different networks.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>processlocal</td><td>&lt;String></td><td>Read-write</td><td>By turning on this option packets destined to a service in a cluster will not under go any steering.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>retainconnectionsoncluster</td><td>&lt;String></td><td>Read-write</td><td>This option enables you to retain existing connections on a node joining a Cluster system or when a node is being configured for passive timeout. By default, this option is disabled.<br>Default value: NO<br>Possible values = YES, NO</td></tr><tr><td>nodegroup</td><td>&lt;String></td><td>Read-write</td><td>The node group in a Cluster system used for transition from L2 to L3.</td></tr><tr><td>adminstate</td><td>&lt;String></td><td>Read-only</td><td>Cluster Admin State.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>propstate</td><td>&lt;String></td><td>Read-only</td><td>Enable/Disable the execution of commands on the cluster. This will not impact the execution of commands on individual cluster nodes by using the NSIP.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>validmtu</td><td>&lt;Double></td><td>Read-only</td><td>Correct MTU value that has to be set on backplane.</td></tr><tr><td>operationalstate</td><td>&lt;String></td><td>Read-only</td><td>Cluster Operational State.<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>status</td><td>&lt;String></td><td>Read-only</td><td>Cluster Operational State.<br>Possible values = DOWN, UP, PARTIAL-UP, UNKNOWN</td></tr><tr><td>rsskeymismatch</td><td>&lt;Boolean></td><td>Read-only</td><td>This argument is used to determine if there is a RSS key mismatch at cluster instance level.</td></tr><tr><td>nodegroupstatewarning</td><td>&lt;Boolean></td><td>Read-only</td><td>This argumnt is used to determind whether all the cluster nodes are bound to nodegroup with state set.</td></tr><tr><td>licensemismatch</td><td>&lt;Boolean></td><td>Read-only</td><td>This argument is used to determine if there is a License mismatch at cluster instance level.</td></tr><tr><td>jumbonotsupported</td><td>&lt;Boolean></td><td>Read-only</td><td>This argument is used to determine if Jumbo framework is not supported at cluster instance level.</td></tr><tr><td>clusternoheartbeatonnode</td><td>&lt;Boolean></td><td>Read-only</td><td>HB is not seen on the backplane interface of member node.</td></tr><tr><td>clusternolinksetmbf</td><td>&lt;Boolean></td><td>Read-only</td><td>MBF is enabled but linkset is not configured .</td></tr><tr><td>clusternospottedip</td><td>&lt;Boolean></td><td>Read-only</td><td>There is no spotted SNIP or MIP.</td></tr><tr><td>operationalpropstate</td><td>&lt;String></td><td>Read-only</td><td>Cluster Operational Propagation State.<br>Default value: ENABLED<br>Possible values = UNKNOWN, ENABLED, DISABLED, AUTO DISABLED</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD]()| [DELETE](#d)| [UPDATE](#u)| [UNSET](#)| [ENABLE](#e)| [DISABLE](#di)| [GET (ALL)](#get-)| [GET]()| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/clusterinstance
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"clusterinstance":{<b>"clid":<Double_value>,</b>"deadinterval":<Double_value>,"hellointerval":<Double_value>,"preemption":<String_value>,"quorumtype":<String_value>,"inc":<String_value>,"processlocal":<String_value>,"retainconnectionsoncluster":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/clusterinstance/clid_value&lt;Double&gt;
<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/clusterinstance
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"clusterinstance":{<b>"clid":<Double_value>,</b>"deadinterval":<Double_value>,"hellointerval":<Double_value>,"preemption":<String_value>,"quorumtype":<String_value>,"inc":<String_value>,"processlocal":<String_value>,"nodegroup":<String_value>,"retainconnectionsoncluster":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/clusterinstance?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"clusterinstance":{<b>"clid":<Double_value>,</b>"deadinterval":true,"hellointerval":true,"preemption":true,"quorumtype":true,"inc":true,"processlocal":true,"nodegroup":true,"retainconnectionsoncluster":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###enable



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/clusterinstance?<b>action=enable</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"clusterinstance":{<b>"clid":<Double_value></b>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###disable



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/clusterinstance?<b>action=disable</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"clusterinstance":{<b>"clid":<Double_value></b>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/clusterinstance
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/clusterinstance?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/clusterinstance?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of clusterinstance resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/clusterinstance?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/clusterinstance?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the clusterinstance resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "clusterinstance": [ {"clid":<Double_value>,"deadinterval":<Double_value>,"hellointerval":<Double_value>,"preemption":<String_value>,"adminstate":<String_value>,"quorumtype":<String_value>,"propstate":<String_value>,"inc":<String_value>,"nodegroup":<String_value>,"processlocal":<String_value>,"validmtu":<Double_value>,"retainconnectionsoncluster":<String_value>,"operationalstate":<String_value>,"status":<String_value>,"rsskeymismatch":<Boolean_value>,"nodegroupstatewarning":<Boolean_value>,"licensemismatch":<Boolean_value>,"jumbonotsupported":<Boolean_value>,"clusternoheartbeatonnode":<Boolean_value>,"clusternolinksetmbf":<Boolean_value>,"clusternospottedip":<Boolean_value>,"operationalpropstate":<String_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/clusterinstance/clid_value&lt;Double&gt;
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/clusterinstance/clid_value&lt;Double&gt;?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/clusterinstance/clid_value&lt;Double&gt;?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "clusterinstance": [ {"clid":<Double_value>,"deadinterval":<Double_value>,"hellointerval":<Double_value>,"preemption":<String_value>,"adminstate":<String_value>,"quorumtype":<String_value>,"propstate":<String_value>,"inc":<String_value>,"nodegroup":<String_value>,"processlocal":<String_value>,"validmtu":<Double_value>,"retainconnectionsoncluster":<String_value>,"operationalstate":<String_value>,"status":<String_value>,"rsskeymismatch":<Boolean_value>,"nodegroupstatewarning":<Boolean_value>,"licensemismatch":<Boolean_value>,"jumbonotsupported":<Boolean_value>,"clusternoheartbeatonnode":<Boolean_value>,"clusternolinksetmbf":<Boolean_value>,"clusternospottedip":<Boolean_value>,"operationalpropstate":<String_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/clusterinstance?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "clusterinstance": [ { "__count": "#no"} ] }```



