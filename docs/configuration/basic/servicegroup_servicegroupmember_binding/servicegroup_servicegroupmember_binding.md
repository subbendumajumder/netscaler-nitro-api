#servicegroup_servicegroupmember_binding

Binding object showing the servicegroupmember that can be bound to servicegroup.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>servicegroupname</td><td>&lt;String></td><td>Read-write</td><td>Name of the service group.&lt;br>Minimum length = 1</td><tr><tr><td>ip</td><td>&lt;String></td><td>Read-write</td><td>IP Address.</td><tr><tr><td>port</td><td>&lt;Integer></td><td>Read-write</td><td>Server port number.&lt;br>Range 1 - 65535</td><tr><tr><td>state</td><td>&lt;String></td><td>Read-write</td><td>Initial state of the service group.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>hashid</td><td>&lt;Double></td><td>Read-write</td><td>The hash identifier for the service. This must be unique for each service. This parameter is used by hash based load balancing methods.&lt;br>Minimum value = 1</td><tr><tr><td>serverid</td><td>&lt;Double></td><td>Read-write</td><td>The identifier for the service. This is used when the persistency type is set to Custom Server ID.</td><tr><tr><td>servername</td><td>&lt;String></td><td>Read-write</td><td>Name of the server to which to bind the service group.&lt;br>Minimum length = 1</td><tr><tr><td>customserverid</td><td>&lt;String></td><td>Read-write</td><td>The identifier for this IP:Port pair. Used when the persistency type is set to Custom Server ID.&lt;br>Default value: "None"</td><tr><tr><td>weight</td><td>&lt;Double></td><td>Read-write</td><td>Weight to assign to the servers in the service group. Specifies the capacity of the servers relative to the other servers in the load balancing configuration. The higher the weight, the higher the percentage of requests sent to the service.&lt;br>Minimum value = 1&lt;br>Maximum value = 100</td><tr><tr><td>delay</td><td>&lt;Double></td><td>Read-only</td><td>Time, in seconds, allocated for a shutdown of the services in the service group. During this period, new requests are sent to the service only for clients who already have persistent sessions on the appliance. Requests from new clients are load balanced among other available services. After the delay time expires, no requests are sent to the service, and the service is marked as unavailable (OUT OF SERVICE).</td><tr><tr><td>svrstate</td><td>&lt;String></td><td>Read-only</td><td>The state of the service.&lt;br>Possible values = UP, DOWN, UNKNOWN, BUSY, OUT OF SERVICE, GOING OUT OF SERVICE, DOWN WHEN GOING OUT OF SERVICE, NS_EMPTY_STR, Unknown, DISABLED</td><tr><tr><td>graceful</td><td>&lt;String></td><td>Read-only</td><td>Wait for all existing connections to the service to terminate before shutting down the service.&lt;br>Default value: NO&lt;br>Possible values = YES, NO</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD:](#add:) | [DELETE:](#delete:) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add:



URL: http://NS_IP/nitro/v1/config
HTTP Method: PUT
Request Payload: ```{"params":{      "warning":<String_value>,      "onerror":<String_value>},sessionid":"##sessionid","servicegroup_servicegroupmember_binding":{      "servicegroupname":<String_value>,      "ip":<String_value>,      "servername":<String_value>,      "port":<Integer_value>,      "weight":<Double_value>,      "customserverid":<String_value>,      "serverid":<Double_value>,      "state":<String_value>,      "hashid":<Double_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete:



URL: http://&lt;NS_IP&gt;/nitro/v1/config/servicegroup_servicegroupmember_binding/servicegroupname_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/servicegroup_servicegroupmember_binding/servicegroupname_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/servicegroup_servicegroupmember_binding/servicegroupname_value&lt;String&gt;
Query-parameters:
filter
http://&lt;NS_IP&gt;/nitro/v1/config/servicegroup_servicegroupmember_binding/servicegroupname_value&lt;String&gt;?filter=property-name1:property-value1,property-name2:property-value2
Use this query-parameter to get the filtered set of servicegroup_servicegroupmember_binding resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/servicegroup_servicegroupmember_binding/servicegroupname_value&lt;String&gt;?pagesize=#no;pageno=#no
Use this query-parameter to get the servicegroup_servicegroupmember_binding resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/servicegroup_servicegroupmember_binding?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "servicegroup_servicegroupmember_binding": [ {      "servicegroupname":<String_value>,      "ip":<String_value>,      "port":<Integer_value>,      "state":<String_value>,      "hashid":<Double_value>,      "serverid":<Double_value>,      "servername":<String_value>,      "customserverid":<String_value>,      "weight":<Double_value>,      "delay":<Double_value>,      "svrstate":<String_value>,      "graceful":<String_value>,}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/servicegroup_servicegroupmember_binding/servicegroupname_value&lt;String&gt;?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",servicegroup_servicegroupmember_binding: [ { "__count": "#no"} ] }


