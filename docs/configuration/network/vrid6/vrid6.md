#vrid6

Configuration for Virtual Router ID for IPv6 resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>&lt;Double></td><td>Read-write</td><td>Integer value that uniquely identifies a VMAC6 address.&lt;br>Minimum value = 1&lt;br>Maximum value = 255</td><tr><tr><td>priority</td><td>&lt;Double></td><td>Read-write</td><td>Base priority (BP), in an active-active mode configuration, which ordinarily determines the master VIP address.&lt;br>Default value: 255&lt;br>Minimum value = 0&lt;br>Maximum value = 255</td><tr><tr><td>preemption</td><td>&lt;String></td><td>Read-write</td><td>In an active-active mode configuration, make a backup VIP address the master if its priority becomes higher than that of a master VIP address bound to this VMAC address.&lt;br> If you disable pre-emption while a backup VIP address is the master, the backup VIP address remains master until the original master VIPs priority becomes higher than that of the current master.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>sharing</td><td>&lt;String></td><td>Read-write</td><td>In an active-active mode configuration, enable the backup VIP address to process any traffic instead of dropping it.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>tracking</td><td>&lt;String></td><td>Read-write</td><td>The effective priority (EP) value, relative to the base priority (BP) value in an active-active mode configuration. When EP is set to a value other than None, it is EP, not BP, which determines the master VIP address.&lt;br>Available settings function as follows:&lt;br>* NONE - No tracking. EP = BP&lt;br>* ALL - If the status of all virtual servers is UP, EP = BP. Otherwise, EP = 0.&lt;br>* ONE - If the status of at least one virtual server is UP, EP = BP. Otherwise, EP = 0.&lt;br>* PROGRESSIVE - If the status of all virtual servers is UP, EP = BP. If the status of all virtual servers is DOWN, EP = 0. Otherwise EP = BP (1 - K/N), where N is the total number of virtual servers associated with the VIP address and K is the number of virtual servers for which the status is DOWN.&lt;br>Default: NONE.&lt;br>Default value: NONE&lt;br>Possible values = NONE, ONE, ALL, PROGRESSIVE</td><tr><tr><td>preemptiondelaytimer</td><td>&lt;Double></td><td>Read-write</td><td>Preemption delay time in seconds, in an active-active configuration. If any high priority node will come in network, it will wait for these many seconds before becoming master.&lt;br>Default value: 0&lt;br>Minimum value = 1&lt;br>Maximum value = 36000</td><tr><tr><td>trackifnumpriority</td><td>&lt;Double></td><td>Read-write</td><td>Priority by which the Effective priority will be reduced if any of the tracked interfaces goes down in an active-active configuration.&lt;br>Default value: 0&lt;br>Minimum value = 1&lt;br>Maximum value = 255</td><tr><tr><td>ownernode</td><td>&lt;Double></td><td>Read-write</td><td>In a cluster setup, assign a cluster node as the owner of this VMAC address for IP based VRRP configuration. If no owner is configured, ow ner node is displayed as ALL and one node is dynamically elected as the owner.&lt;br>Minimum value = 0&lt;br>Maximum value = 31</td><tr><tr><td>all</td><td>&lt;Boolean></td><td>Read-write</td><td>Remove all configured VMAC6 addresses from the NetScaler appliance.</td><tr><tr><td>ifaces</td><td>&lt;String></td><td>Read-only</td><td>Interfaces bound to this VRID.</td><tr><tr><td>ifnum</td><td>&lt;String></td><td>Read-only</td><td>Interfaces to bind to the VMAC6, specified in (slot/port) notation (for example, 1/2).Use spaces to separate multiple entries.</td><tr><tr><td>type</td><td>&lt;String></td><td>Read-only</td><td>Type (static or dynamic) of this VRID.&lt;br>Possible values = STATIC, DYNAMIC</td><tr><tr><td>state</td><td>&lt;Double></td><td>Read-only</td><td>State of this VRID.</td><tr><tr><td>flags</td><td>&lt;Double></td><td>Read-only</td><td>Flags.</td><tr><tr><td>ipaddress</td><td>&lt;String></td><td>Read-only</td><td>The IP address bound to the VRID6.</td><tr><tr><td>effectivepriority</td><td>&lt;Double></td><td>Read-only</td><td>The effective priority of this VRID.</td><tr><tr><td>operationalownernode</td><td>&lt;Double></td><td>Read-only</td><td>Run time owner node of the vrid.&lt;br>Minimum value = 0&lt;br>Maximum value = 31</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [DELETE](#delete) | [UPDATE](#update) | [UNSET](#unset) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vrid6
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"vrid6":{      "id":<Double_value>,      "priority":<Double_value>,      "preemption":<String_value>,      "sharing":<String_value>,      "tracking":<String_value>,      "preemptiondelaytimer":<Double_value>,      "trackifnumpriority":<Double_value>,      "ownernode":<Double_value>}}```
Response:
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vrid6/id_value&lt;Double&gt;
HTTP Method: DELETE
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vrid6
HTTP Method: PUT
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"vrid6":{      "id":<Double_value>,      "priority":<Double_value>,      "preemption":<String_value>,      "sharing":<String_value>,      "tracking":<String_value>,      "preemptiondelaytimer":<Double_value>,      "trackifnumpriority":<Double_value>,      "ownernode":<Double_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vrid6?action=unset
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"vrid6":{      "id":<Double_value>,      "priority":true,      "preemption":true,      "sharing":true,      "tracking":true,      "preemptiondelaytimer":true,      "trackifnumpriority":true,      "ownernode":true}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vrid6
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vrid6?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


filter
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vrid6?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of vrid6 resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vrid6?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).


pagination
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vrid6?pagesize=#no;pageno=#no
Use this query-parameter to get the vrid6 resources in chunks.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "vrid6": [ {      "id":<Double_value>,      "ifaces":<String_value>,      "ifnum":<String_value>,      "type":<String_value>,      "priority":<Double_value>,      "state":<Double_value>,      "flags":<Double_value>,      "ipaddress":<String_value>,      "preemption":<String_value>,      "sharing":<String_value>,      "preemptiondelaytimer":<Double_value>,      "trackifnumpriority":<Double_value>,      "effectivepriority":<Double_value>,      "tracking":<String_value>,      "operationalownernode":<Double_value>,      "ownernode":<Double_value>}]}```



###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vrid6/id_value&lt;Double&gt;
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vrid6/id_value&lt;Double&gt;?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vrid6/id_value&lt;Double&gt;?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "vrid6": [ {      "id":<Double_value>,      "ifaces":<String_value>,      "ifnum":<String_value>,      "type":<String_value>,      "priority":<Double_value>,      "state":<Double_value>,      "flags":<Double_value>,      "ipaddress":<String_value>,      "preemption":<String_value>,      "sharing":<String_value>,      "preemptiondelaytimer":<Double_value>,      "trackifnumpriority":<Double_value>,      "effectivepriority":<Double_value>,      "tracking":<String_value>,      "operationalownernode":<Double_value>,      "ownernode":<Double_value>}]}```



###count



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vrid6?count=yes
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: 
{ "vrid6": [ { "__count": "#no"} ] }


