#service_lbmonitor_binding

Binding object showing the lbmonitor that can be bound to service.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>weight</td><td>&lt;Double></td><td>Read-write</td><td>Weight to assign to the monitor-service binding. When a monitor is UP, the weight assigned to its binding with the service determines how much the monitor contributes toward keeping the health of the service above the value configured for the Monitor Threshold parameter.&lt;br>Minimum value = 1&lt;br>Maximum value = 100</td><tr><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name of the service to which to bind a policy or monitor.&lt;br>Minimum length = 1</td><tr><tr><td>passive</td><td>&lt;Boolean></td><td>Read-write</td><td>Indicates if load monitor is passive. A passive load monitor does not remove service from LB decision when threshold is breached.</td><tr><tr><td>monitor_name</td><td>&lt;String></td><td>Read-write</td><td>The monitor Names.</td><tr><tr><td>monstate</td><td>&lt;String></td><td>Read-write</td><td>The configured state (enable/disable) of the monitor on this server.&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>monstatcode</td><td>&lt;Integer></td><td>Read-only</td><td>The code indicating the monitor response.</td><tr><tr><td>dup_weight</td><td>&lt;Double></td><td>Read-only</td><td>The weight of the monitor.</td><tr><tr><td>responsetime</td><td>&lt;Double></td><td>Read-only</td><td>Response time of this monitor.</td><tr><tr><td>totalfailedprobes</td><td>&lt;Double></td><td>Read-only</td><td>The total number of failed probs.</td><tr><tr><td>monstatparam2</td><td>&lt;Integer></td><td>Read-only</td><td>Second parameter for use with message code.</td><tr><tr><td>lastresponse</td><td>&lt;String></td><td>Read-only</td><td>The string form of monstatcode.</td><tr><tr><td>failedprobes</td><td>&lt;Double></td><td>Read-only</td><td>Number of the current failed monitoring probes.</td><tr><tr><td>monstatparam3</td><td>&lt;Integer></td><td>Read-only</td><td>Third parameter for use with message code.</td><tr><tr><td>totalprobes</td><td>&lt;Double></td><td>Read-only</td><td>The total number of probs sent.</td><tr><tr><td>monitor_state</td><td>&lt;String></td><td>Read-only</td><td>The running state of the monitor on this service.&lt;br>Possible values = UP, DOWN, UNKNOWN, BUSY, OUT OF SERVICE, GOING OUT OF SERVICE, DOWN WHEN GOING OUT OF SERVICE, NS_EMPTY_STR, Unknown, DISABLED</td><tr><tr><td>dup_state</td><td>&lt;String></td><td>Read-only</td><td>Added this field for getting state value from table.&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>monitortotalprobes</td><td>&lt;Double></td><td>Read-only</td><td>Total number of probes sent to monitor this service.</td><tr><tr><td>monstatparam1</td><td>&lt;Integer></td><td>Read-only</td><td>First parameter for use with message code.</td><tr><tr><td>monitortotalfailedprobes</td><td>&lt;Double></td><td>Read-only</td><td>Total number of failed probes.</td><tr><tr><td>monitorcurrentfailedprobes</td><td>&lt;Double></td><td>Read-only</td><td>Total number of currently failed probes.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
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
Request Payload: ```{"params":{      "warning":<String_value>,      "onerror":<String_value>},sessionid":"##sessionid","service_lbmonitor_binding":{      "name":<String_value>,      "monitor_name":<String_value>,                  "monstate":<String_value>,                  "weight":<Double_value>,                  "passive":<Boolean_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete:



URL: http://&lt;NS_IP&gt;/nitro/v1/config/service_lbmonitor_binding/name_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/service_lbmonitor_binding/name_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/service_lbmonitor_binding/name_value&lt;String&gt;
Query-parameters:
filter
http://&lt;NS_IP&gt;/nitro/v1/config/service_lbmonitor_binding/name_value&lt;String&gt;?filter=property-name1:property-value1,property-name2:property-value2
Use this query-parameter to get the filtered set of service_lbmonitor_binding resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/service_lbmonitor_binding/name_value&lt;String&gt;?pagesize=#no;pageno=#no
Use this query-parameter to get the service_lbmonitor_binding resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/service_lbmonitor_binding?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "service_lbmonitor_binding": [ {      "weight":<Double_value>,      "name":<String_value>,      "passive":<Boolean_value>,      "monitor_name":<String_value>,      "monstate":<String_value>,      "monstatcode":<Integer_value>,      "dup_weight":<Double_value>,      "responsetime":<Double_value>,      "totalfailedprobes":<Double_value>,      "monstatparam2":<Integer_value>,      "lastresponse":<String_value>,      "failedprobes":<Double_value>,      "monstatparam3":<Integer_value>,      "totalprobes":<Double_value>,      "monitor_state":<String_value>,      "dup_state":<String_value>,      "monitortotalprobes":<Double_value>,      "monstatparam1":<Integer_value>,      "monitortotalfailedprobes":<Double_value>,      "monitorcurrentfailedprobes":<Double_value>,}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/service_lbmonitor_binding/name_value&lt;String&gt;?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",service_lbmonitor_binding: [ { "__count": "#no"} ] }


