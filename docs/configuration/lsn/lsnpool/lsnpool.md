#lsnpool

Configuration for LSN pool resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>poolname</td><td>&lt;String></td><td>Read-write</td><td>Name for the LSN pool. Must begin with an ASCII alphanumeric or underscore (_) character, and must contain only ASCII alphanumeric, underscore, hash (#), period (.), space, colon (:), at (@), equals (=), and hyphen (-) characters. Cannot be changed after the LSN pool is created. The following requirement applies only to the NetScaler CLI: If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "lsn pool1" or lsn pool1).&lt;br>Minimum length = 1&lt;br>Maximum length = 127</td><tr><tr><td>nattype</td><td>&lt;String></td><td>Read-write</td><td>Type of NAT IP address and port allocation (from the LSN pools bound to an LSN group) for subscribers (of the LSN client entity bound to the LSN group): Available options function as follows: * Deterministic - Allocate a NAT IP address and a block of ports to each subscriber (of the LSN client bound to the LSN group). The NetScaler ADC sequentially allocates NAT resources to these subscribers. The NetScaler ADC assigns the first block of ports (block size determined by the port block size parameter of the LSN group) on the beginning NAT IP address to the beginning subscriber IP address. The next range of ports is assigned to the next subscriber, and so on, until the NAT address does not have enough ports for the next subscriber. In this case, the first port block on the next NAT address is used for the subscriber, and so on. Because each subscriber now receives a deterministic NAT IP address and a block of ports, a subscriber can be identified without any need for logging. For a connection, a subscriber can be identified based only on the NAT IP address and port, and the destination IP address and port. * Dynamic - Allocate a random NAT IP address and a port from the LSN NAT pool for a subscriber\\?s connection. If port block allocation is enabled (in LSN pool) and a port block size is specified (in the LSN group), the NetScaler ADC allocates a random NAT IP address and a block of ports for a subscriber when it initiates a connection for the first time. The ADC allocates this NAT IP address and a port (from the allocated block of ports) for different connections from this subscriber. If all the ports are allocated (for different subscriber\\?s connections) from the subscriber\\?s allocated port block, the ADC allocates a new random port block for the subscriber. Only LSN Pools and LSN groups with the same NAT type settings can be bound together. Multiples LSN pools can be bound to an LSN group. A maximum of 16 LSN pools can be bound to an LSN group. .&lt;br>Default value: DYNAMIC&lt;br>Possible values = DYNAMIC, DETERMINISTIC</td><tr><tr><td>portblockallocation</td><td>&lt;String></td><td>Read-write</td><td>Allocate a random NAT port block, from the available NAT port pool of an NAT IP address, for each subscriber when the NAT allocation is set as Dynamic NAT. For any connection initiated from a subscriber, the NetScaler ADC allocates a NAT port from the subscriber\\?s allocated NAT port block to create the LSN session. You must set the port block size in the bound LSN group. For a subscriber, if all the ports are allocated from the subscriber\\?s allocated port block, the NetScaler ADC allocates a new random port block for the subscriber. For Deterministic NAT, this parameter is enabled by default, and you cannot disable it.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>portrealloctimeout</td><td>&lt;Double></td><td>Read-write</td><td>The waiting time, in seconds, between deallocating LSN NAT ports (when an LSN mapping is removed) and reallocating them for a new LSN session. This parameter is necessary in order to prevent collisions between old and new mappings and sessions. It ensures that all established sessions are broken instead of redirected to a different subscriber. This is not applicable for ports used in: * Deterministic NAT * Address-Dependent filtering and Address-Port-Dependent filtering * Dynamic NAT with port block allocation In these cases, ports are immediately reallocated.&lt;br>Default value: 0&lt;br>Minimum value = 0&lt;br>Maximum value = 600</td><tr><tr><td>maxportrealloctmq</td><td>&lt;Double></td><td>Read-write</td><td>Maximum number of ports for which the port reallocation timeout applies for each NAT IP address. In other words, the maximum deallocated-port queue size for which the reallocation timeout applies for each NAT IP address. When the queue size is full, the next port deallocated is reallocated immediately for a new LSN session.&lt;br>Default value: 65536&lt;br>Minimum value = 0&lt;br>Maximum value = 65536</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [DELETE](#delete) | [UPDATE](#update) | [UNSET](#unset) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>},"sessionid":"##sessionid","lsnpool":{      "poolname":<String_value>,      "nattype":<String_value>,      "portblockallocation":<String_value>,      "portrealloctimeout":<Double_value>,      "maxportrealloctmq":<Double_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/lsnpool/poolname_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/lsnpool/poolname_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","lsnpool":{      "poolname":<String_value>,      "portrealloctimeout":<Double_value>,      "maxportrealloctmq":<Double_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","lsnpool":{      "poolname":<String_value>,      "portrealloctimeout":true,      "maxportrealloctmq":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/lsnpool
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/lsnpool?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of lsnpool resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/lsnpool?view=summary
Use this query-parameter to get the summary output of lsnpool resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/lsnpool?pagesize=#no;pageno=#no
Use this query-parameter to get the lsnpool resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/lsnpool?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "lsnpool": [ {      "poolname":<String_value>,      "nattype":<String_value>,      "portrealloctimeout":<Double_value>,      "maxportrealloctmq":<Double_value>,      "portblockallocation":<String_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/lsnpool/poolname_value&lt;String&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "lsnpool": [ {      "poolname":<String_value>,      "nattype":<String_value>,      "portrealloctimeout":<Double_value>,      "maxportrealloctmq":<Double_value>,      "portblockallocation":<String_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/lsnpool?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",lsnpool: [ { "__count": "#no"} ] }


