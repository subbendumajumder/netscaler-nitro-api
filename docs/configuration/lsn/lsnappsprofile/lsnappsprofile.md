#lsnappsprofile

Configuration for LSN Application Profile resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>appsprofilename</td><td>&lt;String></td><td>Read-write</td><td>Name for the LSN application profile. Must begin with an ASCII alphanumeric or underscore (_) character, and must contain only ASCII alphanumeric, underscore, hash (#), period (.), space, colon (:), at (@), equals (=), and hyphen (-) characters. Cannot be changed after the LSN application profile is created. The following requirement applies only to the NetScaler CLI: If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "lsn application profile1" or lsn application profile1).&lt;br>Minimum length = 1&lt;br>Maximum length = 127</td><tr><tr><td>transportprotocol</td><td>&lt;String></td><td>Read-write</td><td>Name of the protocol for which the parameters of this LSN application profile applies.&lt;br>Possible values = TCP, UDP, ICMP</td><tr><tr><td>ippooling</td><td>&lt;String></td><td>Read-write</td><td>NAT IP address allocation options for sessions associated with the same subscriber. Available options function as follows: * Paired - The NetScaler ADC allocates the same NAT IP address for all sessions associated with the same subscriber. When all the ports of a NAT IP address are used in LSN sessions (for same or multiple subscribers), the NetScaler ADC drops any new connection from the subscriber. * Random - The NetScaler ADC allocates random NAT IP addresses, from the pool, for different sessions associated with the same subscriber. This parameter is applicable to dynamic NAT allocation only.&lt;br>Default value: RANDOM&lt;br>Possible values = PAIRED, RANDOM</td><tr><tr><td>mapping</td><td>&lt;String></td><td>Read-write</td><td>Type of LSN mapping to apply to subsequent packets originating from the same subscriber IP address and port. Consider an example of an LSN mapping that includes the mapping of the subscriber IP:port (X:x), NAT IP:port (N:n), and external host IP:port (Y:y). Available options function as follows: * ENDPOINT-INDEPENDENT - Reuse the LSN mapping for subsequent packets sent from the same subscriber IP address and port (X:x) to any external IP address and port. * ADDRESS-DEPENDENT - Reuse the LSN mapping for subsequent packets sent from the same subscriber IP address and port (X:x) to the same external IP address (Y), regardless of the external port. * ADDRESS-PORT-DEPENDENT - Reuse the LSN mapping for subsequent packets sent from the same internal IP address and port (X:x) to the same external IP address and port (Y:y) while the mapping is still active.&lt;br>Default value: ADDRESS-PORT-DEPENDENT&lt;br>Possible values = ENDPOINT-INDEPENDENT, ADDRESS-DEPENDENT, ADDRESS-PORT-DEPENDENT</td><tr><tr><td>filtering</td><td>&lt;String></td><td>Read-write</td><td>Type of filter to apply to packets originating from external hosts. Consider an example of an LSN mapping that includes the mapping of subscriber IP:port (X:x), NAT IP:port (N:n), and external host IP:port (Y:y). Available options function as follows: * ENDPOINT INDEPENDENT - Filters out only packets not destined to the subscriber IP address and port X:x, regardless of the external host IP address and port source (Z:z). The NetScaler ADC forwards any packets destined to X:x. In other words, sending packets from the subscriber to any external IP address is sufficient to allow packets from any external hosts to the subscriber. * ADDRESS DEPENDENT - Filters out packets not destined to subscriber IP address and port X:x. In addition, the ADC filters out packets from Y:y destined for the subscriber (X:x) if the client has not previously sent packets to Y:anyport (external port independent). In other words, receiving packets from a specific external host requires that the subscriber first send packets to that specific external hosts IP address. * ADDRESS PORT DEPENDENT (the default) - Filters out packets not destined to subscriber IP address and port (X:x). In addition, the NetScaler ADC filters out packets from Y:y destined for the subscriber (X:x) if the subscriber has not previously sent packets to Y:y. In other words, receiving packets from a specific external host requires that the subscriber first send packets first to that external IP address and port.&lt;br>Default value: ADDRESS-PORT-DEPENDENT&lt;br>Possible values = ENDPOINT-INDEPENDENT, ADDRESS-DEPENDENT, ADDRESS-PORT-DEPENDENT</td><tr><tr><td>tcpproxy</td><td>&lt;String></td><td>Read-write</td><td>Enable TCP proxy, which enables the NetScaler appliance to optimize the TCP traffic by using Layer 4 features.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>td</td><td>&lt;Double></td><td>Read-write</td><td>ID of the traffic domain through which the NetScaler ADC sends the outbound traffic after performing LSN. If you do not specify an ID, the ADC sends the outbound traffic through the default traffic domain, which has an ID of 0.&lt;br>Default value: 65535</td><tr><tr><td>l2info</td><td>&lt;String></td><td>Read-write</td><td>Enable l2info by creating natpcbs for LSN, which enables the NetScaler appliance to use L2CONN/MBF with LSN.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
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
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>},"sessionid":"##sessionid","lsnappsprofile":{      "appsprofilename":<String_value>,      "transportprotocol":<String_value>,      "ippooling":<String_value>,      "mapping":<String_value>,      "filtering":<String_value>,      "tcpproxy":<String_value>,      "td":<Double_value>,      "l2info":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/lsnappsprofile/appsprofilename_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/lsnappsprofile/appsprofilename_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","lsnappsprofile":{      "appsprofilename":<String_value>,      "ippooling":<String_value>,      "mapping":<String_value>,      "filtering":<String_value>,      "tcpproxy":<String_value>,      "td":<Double_value>,      "l2info":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","lsnappsprofile":{      "appsprofilename":<String_value>,      "ippooling":true,      "mapping":true,      "filtering":true,      "tcpproxy":true,      "td":true,      "l2info":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/lsnappsprofile
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/lsnappsprofile?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of lsnappsprofile resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/lsnappsprofile?view=summary
Use this query-parameter to get the summary output of lsnappsprofile resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/lsnappsprofile?pagesize=#no;pageno=#no
Use this query-parameter to get the lsnappsprofile resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/lsnappsprofile?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "lsnappsprofile": [ {      "appsprofilename":<String_value>,      "transportprotocol":<String_value>,      "ippooling":<String_value>,      "mapping":<String_value>,      "filtering":<String_value>,      "tcpproxy":<String_value>,      "td":<Double_value>,      "l2info":<String_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/lsnappsprofile/appsprofilename_value&lt;String&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "lsnappsprofile": [ {      "appsprofilename":<String_value>,      "transportprotocol":<String_value>,      "ippooling":<String_value>,      "mapping":<String_value>,      "filtering":<String_value>,      "tcpproxy":<String_value>,      "td":<Double_value>,      "l2info":<String_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/lsnappsprofile?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",lsnappsprofile: [ { "__count": "#no"} ] }


