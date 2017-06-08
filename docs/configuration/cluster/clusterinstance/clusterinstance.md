#clusterinstance

Configuration for cluster instance resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>clid</td><td>&lt;Double></td><td>Read-write</td><td>Unique number that identifies the cluster.&lt;br>Minimum value = 1&lt;br>Maximum value = 16</td><tr><tr><td>deadinterval</td><td>&lt;Double></td><td>Read-write</td><td>Amount of time, in seconds, after which nodes that do not respond to the heartbeats are assumed to be down.&lt;br>Default value: 3&lt;br>Minimum value = 3&lt;br>Maximum value = 60</td><tr><tr><td>hellointerval</td><td>&lt;Double></td><td>Read-write</td><td>Interval, in milliseconds, at which heartbeats are sent to each cluster node to check the health status.&lt;br>Default value: 200&lt;br>Minimum value = 200&lt;br>Maximum value = 1000</td><tr><tr><td>preemption</td><td>&lt;String></td><td>Read-write</td><td>Preempt a cluster node that is configured as a SPARE if an ACTIVE node becomes available.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>quorumtype</td><td>&lt;String></td><td>Read-write</td><td>Quorum Configuration Choices - "Majority" (recommended) requires majority of nodes to be online for the cluster to be UP. "None" relaxes this requirement.&lt;br>Default value: MAJORITY&lt;br>Possible values = MAJORITY, NONE</td><tr><tr><td>adminstate</td><td>&lt;String></td><td>Read-only</td><td>Cluster Admin State.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>propstate</td><td>&lt;String></td><td>Read-only</td><td>Enable/Disable the execution of commands on the cluster. This will not impact the execution of commands on individual cluster nodes by using the NSIP.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>operationalstate</td><td>&lt;String></td><td>Read-only</td><td>Cluster Operational State.&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>status</td><td>&lt;String></td><td>Read-only</td><td>Cluster Operational State.&lt;br>Possible values = DOWN, UP, PARTIAL-UP, UNKNOWN</td><tr><tr><td>rsskeymismatch</td><td>&lt;Boolean></td><td>Read-only</td><td>This argument is used to determine if there is a RSS key mismatch at cluster instance level.</td><tr><tr><td>licensemismatch</td><td>&lt;Boolean></td><td>Read-only</td><td>This argument is used to determine if there is a License mismatch at cluster instance level.</td><tr><tr><td>jumbonotsupported</td><td>&lt;Boolean></td><td>Read-only</td><td>This argument is used to determine if Jumbo framework is not supported at cluster instance level.</td><tr><tr><td>operationalpropstate</td><td>&lt;String></td><td>Read-only</td><td>Cluster Operational Propagation State.&lt;br>Default value: ENABLED&lt;br>Possible values = UNKNOWN, ENABLED, DISABLED, AUTO DISABLED</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [DELETE](#delete) | [UPDATE](#update) | [UNSET](#unset) | [ENABLE](#enable) | [DISABLE](#disable) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>},"sessionid":"##sessionid","clusterinstance":{      "clid":<Double_value>,      "deadinterval":<Double_value>,      "hellointerval":<Double_value>,      "preemption":<String_value>,      "quorumtype":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/clusterinstance/clid_value&lt;Double&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/clusterinstance/clid_value&lt;Double&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","clusterinstance":{      "clid":<Double_value>,      "deadinterval":<Double_value>,      "hellointerval":<Double_value>,      "preemption":<String_value>,      "quorumtype":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","clusterinstance":{      "clid":<Double_value>,      "deadinterval":true,      "hellointerval":true,      "preemption":true,      "quorumtype":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###enable



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"enable"},"sessionid":"##sessionid","clusterinstance":{      "clid":<Double_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###disable



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"disable"},"sessionid":"##sessionid","clusterinstance":{      "clid":<Double_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/clusterinstance
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/clusterinstance?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of clusterinstance resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/clusterinstance?view=summary
Use this query-parameter to get the summary output of clusterinstance resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/clusterinstance?pagesize=#no;pageno=#no
Use this query-parameter to get the clusterinstance resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/clusterinstance?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "clusterinstance": [ {      "clid":<Double_value>,      "deadinterval":<Double_value>,      "hellointerval":<Double_value>,      "preemption":<String_value>,      "adminstate":<String_value>,      "quorumtype":<String_value>,      "propstate":<String_value>,      "operationalstate":<String_value>,      "status":<String_value>,      "rsskeymismatch":<Boolean_value>,      "licensemismatch":<Boolean_value>,      "jumbonotsupported":<Boolean_value>,      "operationalpropstate":<String_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/clusterinstance/clid_value&lt;Double&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "clusterinstance": [ {      "clid":<Double_value>,      "deadinterval":<Double_value>,      "hellointerval":<Double_value>,      "preemption":<String_value>,      "adminstate":<String_value>,      "quorumtype":<String_value>,      "propstate":<String_value>,      "operationalstate":<String_value>,      "status":<String_value>,      "rsskeymismatch":<Boolean_value>,      "licensemismatch":<Boolean_value>,      "jumbonotsupported":<Boolean_value>,      "operationalpropstate":<String_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/clusterinstance?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",clusterinstance: [ { "__count": "#no"} ] }


