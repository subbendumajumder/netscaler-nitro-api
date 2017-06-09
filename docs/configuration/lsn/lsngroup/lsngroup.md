#lsngroup

Configuration for LSN group resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>groupname</td><td>&lt;String></td><td>Read-write</td><td>Name for the LSN group. Must begin with an ASCII alphanumeric or underscore (_) character, and must contain only ASCII alphanumeric, underscore, hash (#), period (.), space, colon (:), at (@), equals (=), and hyphen (-) characters. Cannot be changed after the LSN group is created. The following requirement applies only to the NetScaler CLI: If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "lsn group1" or lsn group1).&lt;br>Minimum length = 1&lt;br>Maximum length = 127</td><tr><tr><td>clientname</td><td>&lt;String></td><td>Read-write</td><td>Name of the LSN client entity to be associated with the LSN group. You can associate only one LSN client entity with an LSN group.You cannot remove this association or replace with another LSN client entity once the LSN group is created.</td><tr><tr><td>nattype</td><td>&lt;String></td><td>Read-write</td><td>Type of NAT IP address and port allocation (from the bound LSN pools) for subscribers:&lt;br>&lt;br>Available options function as follows:&lt;br>&lt;br>* Deterministic - Allocate a NAT IP address and a block of ports to each subscriber (of the LSN client bound to the LSN group). The NetScaler ADC sequentially allocates NAT resources to these subscribers. The NetScaler ADC assigns the first block of ports (block size determined by the port block size parameter of the LSN group) on the beginning NAT IP address to the beginning subscriber IP address. The next range of ports is assigned to the next subscriber, and so on, until the NAT address does not have enough ports for the next subscriber. In this case, the first port block on the next NAT address is used for the subscriber, and so on. Because each subscriber now receives a deterministic NAT IP address and a block of ports, a subscriber can be identified without any need for logging. For a connection, a subscriber can be identified based only on the NAT IP address and port, and the destination IP address and port. The maximum number of LSN subscribers allowed, globally, is 1 million. &lt;br>&lt;br>* Dynamic - Allocate a random NAT IP address and a port from the LSN NAT pool for a subscriber\\?s connection. If port block allocation is enabled (in LSN pool) and a port block size is specified (in the LSN group), the NetScaler ADC allocates a random NAT IP address and a block of ports for a subscriber when it initiates a connection for the first time. The ADC allocates this NAT IP address and a port (from the allocated block of ports) for different connections from this subscriber. If all the ports are allocated (for different subscriber\\?s connections) from the subscriber\\?s allocated port block, the ADC allocates a new random port block for the subscriber.&lt;br>Default value: DYNAMIC&lt;br>Possible values = DYNAMIC, DETERMINISTIC</td><tr><tr><td>portblocksize</td><td>&lt;Double></td><td>Read-write</td><td>Size of the NAT port block to be allocated for each subscriber.&lt;br>&lt;br>To set this parameter for Dynamic NAT, you must enable the port block allocation parameter in the bound LSN pool. For Deterministic NAT, the port block allocation parameter is always enabled, and you cannot disable it.&lt;br>&lt;br>In Dynamic NAT, the NetScaler ADC allocates a random NAT port block, from the available NAT port pool of an NAT IP address, for each subscriber. For a subscriber, if all the ports are allocated from the subscriber\\?s allocated port block, the ADC allocates a new random port block for the subscriber.&lt;br>&lt;br>The default port block size is 256 for Deterministic NAT, and 0 for Dynamic NAT.&lt;br>Default value: 0&lt;br>Minimum value = 256&lt;br>Maximum value = 65536</td><tr><tr><td>logging</td><td>&lt;String></td><td>Read-write</td><td>Log mapping entries and sessions created or deleted for this LSN group. The NetScaler ADC logs LSN sessions for this LSN group only when both logging and session logging parameters are enabled.&lt;br>&lt;br>The ADC uses its existing syslog and audit log framework to log LSN information. You must enable global level LSN logging by enabling the LSN parameter in the related NSLOG action and SYLOG action entities. When the Logging parameter is enabled, the NetScaler ADC generates log messages related to LSN mappings and LSN sessions of this LSN group. The ADC then sends these log messages to servers associated with the NSLOG action and SYSLOG actions entities. &lt;br>&lt;br>A log message for an LSN mapping entry consists of the following information:&lt;br>* NSIP address of the NetScaler ADC&lt;br>* Time stamp&lt;br>* Entry type (MAPPING or SESSION)&lt;br>* Whether the LSN mapping entry is created or deleted&lt;br>* Subscribers IP address, port, and traffic domain ID&lt;br>* NAT IP address and port&lt;br>* Protocol name&lt;br>* Destination IP address, port, and traffic domain ID might be present, depending on the following conditions:&lt;br>** Destination IP address and port are not logged for Endpoint-Independent mapping&lt;br>** Only Destination IP address (and not port) is logged for Address-Dependent mapping&lt;br>** Destination IP address and port are logged for Address-Port-Dependent mapping.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>sessionlogging</td><td>&lt;String></td><td>Read-write</td><td>Log sessions created or deleted for the LSN group. The NetScaler ADC logs LSN sessions for this LSN group only when both logging and session logging parameters are enabled.&lt;br>&lt;br>A log message for an LSN session consists of the following information:&lt;br>* NSIP address of the NetScaler ADC&lt;br>* Time stamp&lt;br>* Entry type (MAPPING or SESSION)&lt;br>* Whether the LSN session is created or removed&lt;br>* Subscribers IP address, port, and traffic domain ID&lt;br>* NAT IP address and port&lt;br>* Protocol name&lt;br>* Destination IP address, port, and traffic domain ID.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>sessionsync</td><td>&lt;String></td><td>Read-write</td><td>In a high availability (HA) deployment, synchronize information of all LSN sessions related to this LSN group with the secondary node. After a failover, established TCP connections and UDP packet flows are kept active and resumed on the secondary node (new primary).&lt;br>&lt;br>For this setting to work, you must enable the global session synchronization parameter.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>snmptraplimit</td><td>&lt;Double></td><td>Read-write</td><td>Maximum number of SNMP Trap messages that can be generated for the LSN group in one minute.&lt;br>Default value: 100&lt;br>Minimum value = 0&lt;br>Maximum value = 10000</td><tr><tr><td>ftp</td><td>&lt;String></td><td>Read-write</td><td>Enable Application Layer Gateway (ALG) for the FTP protocol. For some application-layer protocols, the IP addresses and protocol port numbers are usually communicated in the packet?s payload. When acting as an ALG, the NetScaler changes the packet?s payload to ensure that the protocol continues to work over LSN. &lt;br>&lt;br>Note: The NetScaler ADC also includes ALG for ICMP and TFTP protocols. ALG for the ICMP protocol is enabled by default, and there is no provision to disable it. ALG for the TFTP protocol is disabled by default. ALG is enabled automatically for an LSN group when you bind a UDP LSN application profile, with endpoint-independent-mapping, endpoint-independent filtering, and destination port as 69 (well-known port for TFTP), to the LSN group.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>pptp</td><td>&lt;String></td><td>Read-write</td><td>Enable the PPTP Application Layer Gateway.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>sipalg</td><td>&lt;String></td><td>Read-write</td><td>Enable the SIP ALG.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>rtspalg</td><td>&lt;String></td><td>Read-write</td><td>Enable the RTSP ALG.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>ip6profile</td><td>&lt;String></td><td>Read-write</td><td>Name of the LSN ip6 profile to associate with the specified LSN group. An ip6 profile can be associated with a group only during group creation.&lt;br>&lt;br>By default, no LSN ip6 profile is associated with an LSN group during its creation. Only one ip6profile can be associated with a group.&lt;br>Minimum length = 1&lt;br>Maximum length = 127</td><tr><tr><td>groupid</td><td>&lt;Double></td><td>Read-only</td><td>.&lt;br>Minimum value = 1</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [DELETE](#delete) | [UPDATE](#update) | [UNSET](#unset) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsngroup
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"lsngroup":{      "groupname":<String_value>,      "clientname":<String_value>,      "nattype":<String_value>,      "portblocksize":<Double_value>,      "logging":<String_value>,      "sessionlogging":<String_value>,      "sessionsync":<String_value>,      "snmptraplimit":<Double_value>,      "ftp":<String_value>,      "pptp":<String_value>,      "sipalg":<String_value>,      "rtspalg":<String_value>,      "ip6profile":<String_value>}}```
Response:
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsngroup/groupname_value&lt;String&gt;
HTTP Method: DELETE
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsngroup
HTTP Method: PUT
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"lsngroup":{      "groupname":<String_value>,      "portblocksize":<Double_value>,      "logging":<String_value>,      "sessionlogging":<String_value>,      "sessionsync":<String_value>,      "snmptraplimit":<Double_value>,      "ftp":<String_value>,      "pptp":<String_value>,      "sipalg":<String_value>,      "rtspalg":<String_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsngroup?action=unset
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"lsngroup":{      "groupname":<String_value>,      "portblocksize":true,      "logging":true,      "sessionlogging":true,      "sessionsync":true,      "snmptraplimit":true,      "ftp":true,      "pptp":true,      "sipalg":true,      "rtspalg":true}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsngroup
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsngroup?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


filter
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsngroup?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of lsngroup resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsngroup?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).


pagination
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsngroup?pagesize=#no;pageno=#no
Use this query-parameter to get the lsngroup resources in chunks.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "lsngroup": [ {      "groupname":<String_value>,      "clientname":<String_value>,      "nattype":<String_value>,      "portblocksize":<Double_value>,      "logging":<String_value>,      "sessionlogging":<String_value>,      "sessionsync":<String_value>,      "snmptraplimit":<Double_value>,      "ftp":<String_value>,      "pptp":<String_value>,      "groupid":<Double_value>,      "sipalg":<String_value>,      "rtspalg":<String_value>,      "ip6profile":<String_value>}]}```



###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsngroup/groupname_value&lt;String&gt;
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsngroup/groupname_value&lt;String&gt;?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsngroup/groupname_value&lt;String&gt;?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "lsngroup": [ {      "groupname":<String_value>,      "clientname":<String_value>,      "nattype":<String_value>,      "portblocksize":<Double_value>,      "logging":<String_value>,      "sessionlogging":<String_value>,      "sessionsync":<String_value>,      "snmptraplimit":<Double_value>,      "ftp":<String_value>,      "pptp":<String_value>,      "groupid":<Double_value>,      "sipalg":<String_value>,      "rtspalg":<String_value>,      "ip6profile":<String_value>}]}```



###count



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsngroup?count=yes
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: 
{ "lsngroup": [ { "__count": "#no"} ] }


