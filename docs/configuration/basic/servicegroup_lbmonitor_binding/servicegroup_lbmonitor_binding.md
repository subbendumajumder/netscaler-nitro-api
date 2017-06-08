#servicegroup_lbmonitor_binding

Binding object showing the lbmonitor that can be bound to servicegroup.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>servicegroupname</td><td>&lt;String></td><td>Read-write</td><td>Name of the service group.&lt;br>Minimum length = 1</td><tr><tr><td>port</td><td>&lt;Integer></td><td>Read-write</td><td>Port number of the service. Each service must have a unique port number.&lt;br>Range 1 - 65535</td><tr><tr><td>state</td><td>&lt;String></td><td>Read-write</td><td>Initial state of the service after binding.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>hashid</td><td>&lt;Double></td><td>Read-write</td><td>Unique numerical identifier used by hash based load balancing methods to identify a service.&lt;br>Minimum value = 1</td><tr><tr><td>serverid</td><td>&lt;Double></td><td>Read-write</td><td>The identifier for the service. This is used when the persistency type is set to Custom Server ID.</td><tr><tr><td>customserverid</td><td>&lt;String></td><td>Read-write</td><td>Unique service identifier. Used when the persistency type for the virtual server is set to Custom Server ID.&lt;br>Default value: "None"</td><tr><tr><td>weight</td><td>&lt;Double></td><td>Read-write</td><td>Weight to assign to the servers in the service group. Specifies the capacity of the servers relative to the other servers in the load balancing configuration. The higher the weight, the higher the percentage of requests sent to the service.&lt;br>Minimum value = 1&lt;br>Maximum value = 100</td><tr><tr><td>monitor_name</td><td>&lt;String></td><td>Read-write</td><td>Monitor name.</td><tr><tr><td>passive</td><td>&lt;Boolean></td><td>Read-write</td><td>Indicates if load monitor is passive. A passive load monitor does not remove service from LB decision when threshold is breached.</td><tr><tr><td>monstate</td><td>&lt;String></td><td>Read-write</td><td>Monitor state.&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>monweight</td><td>&lt;Double></td><td>Read-only</td><td>weight of the monitor that is bound to servicegroup.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
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
Request Payload: ```{"params":{      "warning":<String_value>,      "onerror":<String_value>},sessionid":"##sessionid","servicegroup_lbmonitor_binding":{      "servicegroupname":<String_value>,      "port":<Integer_value>,      "monitor_name":<String_value>,                  "monstate":<String_value>,                  "passive":<Boolean_value>,      "weight":<Double_value>,      "customserverid":<String_value>,      "serverid":<Double_value>,      "state":<String_value>,      "hashid":<Double_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete:



URL: http://&lt;NS_IP&gt;/nitro/v1/config/servicegroup_lbmonitor_binding/servicegroupname_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/servicegroup_lbmonitor_binding/servicegroupname_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/servicegroup_lbmonitor_binding/servicegroupname_value&lt;String&gt;
Query-parameters:
filter
http://&lt;NS_IP&gt;/nitro/v1/config/servicegroup_lbmonitor_binding/servicegroupname_value&lt;String&gt;?filter=property-name1:property-value1,property-name2:property-value2
Use this query-parameter to get the filtered set of servicegroup_lbmonitor_binding resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/servicegroup_lbmonitor_binding/servicegroupname_value&lt;String&gt;?pagesize=#no;pageno=#no
Use this query-parameter to get the servicegroup_lbmonitor_binding resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/servicegroup_lbmonitor_binding?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "servicegroup_lbmonitor_binding": [ {      "servicegroupname":<String_value>,      "port":<Integer_value>,      "state":<String_value>,      "hashid":<Double_value>,      "serverid":<Double_value>,      "customserverid":<String_value>,      "weight":<Double_value>,      "monitor_name":<String_value>,      "passive":<Boolean_value>,      "monstate":<String_value>,      "monweight":<Double_value>,}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/servicegroup_lbmonitor_binding/servicegroupname_value&lt;String&gt;?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",servicegroup_lbmonitor_binding: [ { "__count": "#no"} ] }


