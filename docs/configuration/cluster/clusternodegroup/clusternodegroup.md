#clusternodegroup

Configuration for Node group object type resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name of the nodegroup. The name uniquely identifies the nodegroup on the cluster.&lt;br>Minimum length = 1</td><tr><tr><td>strict</td><td>&lt;String></td><td>Read-write</td><td>Specifies whether cluster nodes, that are not part of the nodegroup, will be used as backup for the nodegroup.&lt;br> * Enabled - When one of the nodes goes down, no other cluster node is picked up to replace it. When the node comes up, it will continue being part of the nodegroup.&lt;br> * Disabled - When one of the nodes goes down, a non-nodegroup cluster node is picked up and acts as part of the nodegroup. When the original node of the nodegroup comes up, the backup node will be replaced.&lt;br>Default value: NO&lt;br>Possible values = YES, NO</td><tr><tr><td>sticky</td><td>&lt;String></td><td>Read-write</td><td>Only one node can be bound to nodegroup with this option enabled. It specifies whether to prempt the traffic for the entities bound to nodegroup when owner node goes down and rejoins the cluster.&lt;br> * Enabled - When owner node goes down, backup node will become the owner node and takes the traffic for the entities bound to the nodegroup. When bound node rejoins the cluster, traffic for the entities bound to nodegroup will not be steered back to this bound node. Current owner will have the ownership till it goes down.&lt;br> * Disabled - When one of the nodes goes down, a non-nodegroup cluster node is picked up and acts as part of the nodegroup. When the original node of the nodegroup comes up, the backup node will be replaced.&lt;br>Default value: NO&lt;br>Possible values = YES, NO</td><tr><tr><td>state</td><td>&lt;String></td><td>Read-write</td><td>State of the nodegroup. All the nodes binding to this nodegroup must have the same state. ACTIVE/SPARE/PASSIVE.&lt;br>Possible values = ACTIVE, SPARE, PASSIVE</td><tr><tr><td>priority</td><td>&lt;Double></td><td>Read-write</td><td>Priority of Nodegroup. This priority is used for all the nodes bound to the nodegroup for Nodegroup selection.&lt;br>Minimum value = 0&lt;br>Maximum value = 31</td><tr><tr><td>currentnodemask</td><td>&lt;Double></td><td>Read-only</td><td>Bitmap of current nodes in this nodegroup.</td><tr><tr><td>backupnodemask</td><td>&lt;Double></td><td>Read-only</td><td>Bitmap of backup nodes in this nodegroup.</td><tr><tr><td>boundedentitiescntfrompe</td><td>&lt;Double></td><td>Read-only</td><td>Count of bounded entities to this nodegroup accoding to PE.</td><tr><tr><td>activelist</td><td>&lt;Double[]></td><td>Read-only</td><td>Active node list of this nodegroup.</td><tr><tr><td>backuplist</td><td>&lt;Double[]></td><td>Read-only</td><td>Backup node list of this nodegroup.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [UPDATE](#update) | [UNSET](#unset) | [DELETE](#delete) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/clusternodegroup
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"clusternodegroup":{      "name":<String_value>,      "strict":<String_value>,      "sticky":<String_value>,      "state":<String_value>,      "priority":<Double_value>}}```
Response:
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/clusternodegroup
HTTP Method: PUT
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"clusternodegroup":{      "name":<String_value>,      "strict":<String_value>,      "state":<String_value>,      "priority":<Double_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/clusternodegroup?action=unset
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"clusternodegroup":{      "name":<String_value>,      "strict":true}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/clusternodegroup/name_value&lt;String&gt;
HTTP Method: DELETE
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/clusternodegroup
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/clusternodegroup?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


filter
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/clusternodegroup?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of clusternodegroup resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/clusternodegroup?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).


pagination
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/clusternodegroup?pagesize=#no;pageno=#no
Use this query-parameter to get the clusternodegroup resources in chunks.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "clusternodegroup": [ {      "name":<String_value>,      "strict":<String_value>,      "sticky":<String_value>,      "currentnodemask":<Double_value>,      "backupnodemask":<Double_value>,      "boundedentitiescntfrompe":<Double_value>,      "activelist":<Double[]_value>,      "backuplist":<Double[]_value>,      "state":<String_value>,      "priority":<Double_value>}]}```



###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/clusternodegroup/name_value&lt;String&gt;
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/clusternodegroup/name_value&lt;String&gt;?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/clusternodegroup/name_value&lt;String&gt;?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "clusternodegroup": [ {      "name":<String_value>,      "strict":<String_value>,      "sticky":<String_value>,      "currentnodemask":<Double_value>,      "backupnodemask":<Double_value>,      "boundedentitiescntfrompe":<Double_value>,      "activelist":<Double[]_value>,      "backuplist":<Double[]_value>,      "state":<String_value>,      "priority":<Double_value>}]}```



###count



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/clusternodegroup?count=yes
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: 
{ "clusternodegroup": [ { "__count": "#no"} ] }


