#gslbvserver

Configuration for Global Server Load Balancing Virtual Server resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the GSLB virtual server. Must begin with an ASCII alphanumeric or underscore (_) character, and must contain only ASCII alphanumeric, underscore, hash (#), period (.), space, colon (:), at (@), equals (=), and hyphen (-) characters. Can be changed after the virtual server is created.&lt;br>&lt;br>CLI Users:&lt;br>If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my vserver" or my vserver).&lt;br>Minimum length = 1</td><tr><tr><td>servicetype</td><td>&lt;String></td><td>Read-write</td><td>Protocol used by services bound to the virtual server.&lt;br>Possible values = HTTP, FTP, TCP, UDP, SSL, SSL_BRIDGE, SSL_TCP, NNTP, ANY, SIP_UDP, SIP_TCP, SIP_SSL, RADIUS, RDP, RTSP, MYSQL, MSSQL, ORACLE</td><tr><tr><td>iptype</td><td>&lt;String></td><td>Read-write</td><td>The IP type for this GSLB vserver.&lt;br>Default value: IPV4&lt;br>Possible values = IPV4, IPV6</td><tr><tr><td>dnsrecordtype</td><td>&lt;String></td><td>Read-write</td><td>DNS record type to associate with the GSLB virtual servers domain name.&lt;br>Default value: A&lt;br>Possible values = A, AAAA, CNAME, NAPTR</td><tr><tr><td>lbmethod</td><td>&lt;String></td><td>Read-write</td><td>Load balancing method for the GSLB virtual server.&lt;br>Default value: LEASTCONNECTION&lt;br>Possible values = ROUNDROBIN, LEASTCONNECTION, LEASTRESPONSETIME, SOURCEIPHASH, LEASTBANDWIDTH, LEASTPACKETS, STATICPROXIMITY, RTT, CUSTOMLOAD</td><tr><tr><td>backupsessiontimeout</td><td>&lt;Double></td><td>Read-write</td><td>A non zero value enables the feature whose minimum value is 2 minutes. The feature can be disabled by setting the value to zero. The created session is in effect for a specific client per domain.&lt;br>Minimum value = 0&lt;br>Maximum value = 1440</td><tr><tr><td>backuplbmethod</td><td>&lt;String></td><td>Read-write</td><td>Backup load balancing method. Becomes operational if the primary load balancing method fails or cannot be used. Valid only if the primary method is based on either round-trip time (RTT) or static proximity.&lt;br>Possible values = ROUNDROBIN, LEASTCONNECTION, LEASTRESPONSETIME, SOURCEIPHASH, LEASTBANDWIDTH, LEASTPACKETS, STATICPROXIMITY, RTT, CUSTOMLOAD</td><tr><tr><td>netmask</td><td>&lt;String></td><td>Read-write</td><td>IPv4 network mask for use in the SOURCEIPHASH load balancing method.&lt;br>Minimum length = 1</td><tr><tr><td>v6netmasklen</td><td>&lt;Double></td><td>Read-write</td><td>Number of bits to consider, in an IPv6 source IP address, for creating the hash that is required by the SOURCEIPHASH load balancing method.&lt;br>Default value: 128&lt;br>Minimum value = 1&lt;br>Maximum value = 128</td><tr><tr><td>tolerance</td><td>&lt;Double></td><td>Read-write</td><td>Site selection tolerance, in milliseconds, for implementing the RTT load balancing method. If a sites RTT deviates from the lowest RTT by more than the specified tolerance, the site is not considered when the NetScaler appliance makes a GSLB decision. The appliance implements the round robin method of global server load balancing between sites whose RTT values are within the specified tolerance. If the tolerance is 0 (zero), the appliance always sends clients the IP address of the site with the lowest RTT.&lt;br>Minimum value = 0&lt;br>Maximum value = 100</td><tr><tr><td>persistencetype</td><td>&lt;String></td><td>Read-write</td><td>Use source IP address based persistence for the virtual server. &lt;br>After the load balancing method selects a service for the first packet, the IP address received in response to the DNS query is used for subsequent requests from the same client.&lt;br>Possible values = SOURCEIP, NONE</td><tr><tr><td>persistenceid</td><td>&lt;Double></td><td>Read-write</td><td>The persistence ID for the GSLB virtual server. The ID is a positive integer that enables GSLB sites to identify the GSLB virtual server, and is required if source IP address based or spill over based persistence is enabled on the virtual server.&lt;br>Minimum value = 0&lt;br>Maximum value = 65535</td><tr><tr><td>persistmask</td><td>&lt;String></td><td>Read-write</td><td>The optional IPv4 network mask applied to IPv4 addresses to establish source IP address based persistence.&lt;br>Minimum length = 1</td><tr><tr><td>v6persistmasklen</td><td>&lt;Double></td><td>Read-write</td><td>Number of bits to consider in an IPv6 source IP address when creating source IP address based persistence sessions.&lt;br>Default value: 128&lt;br>Minimum value = 1&lt;br>Maximum value = 128</td><tr><tr><td>timeout</td><td>&lt;Double></td><td>Read-write</td><td>Idle time, in minutes, after which a persistence entry is cleared.&lt;br>Default value: 2&lt;br>Minimum value = 2&lt;br>Maximum value = 1440</td><tr><tr><td>edr</td><td>&lt;String></td><td>Read-write</td><td>Send clients an empty DNS response when the GSLB virtual server is DOWN.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>ecs</td><td>&lt;String></td><td>Read-write</td><td>If enabled, respond with EDNS Client Subnet (ECS) option in the response for a DNS query with ECS. The ECS address will be used for persistence and spillover persistence (if enabled) instead of the LDNS address. Persistence mask is ignored if ECS is enabled.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>ecsaddrvalidation</td><td>&lt;String></td><td>Read-write</td><td>Validate if ECS address is a private or unroutable address and in such cases, use the LDNS IP.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>mir</td><td>&lt;String></td><td>Read-write</td><td>Include multiple IP addresses in the DNS responses sent to clients.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>disableprimaryondown</td><td>&lt;String></td><td>Read-write</td><td>Continue to direct traffic to the backup chain even after the primary GSLB virtual server returns to the UP state. Used when spillover is configured for the virtual server.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>dynamicweight</td><td>&lt;String></td><td>Read-write</td><td>Specify if the appliance should consider the service count, service weights, or ignore both when using weight-based load balancing methods. The state of the number of services bound to the virtual server help the appliance to select the service.&lt;br>Default value: DISABLED&lt;br>Possible values = SERVICECOUNT, SERVICEWEIGHT, DISABLED</td><tr><tr><td>state</td><td>&lt;String></td><td>Read-write</td><td>State of the GSLB virtual server.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>considereffectivestate</td><td>&lt;String></td><td>Read-write</td><td>If the primary state of all bound GSLB services is DOWN, consider the effective states of all the GSLB services, obtained through the Metrics Exchange Protocol (MEP), when determining the state of the GSLB virtual server. To consider the effective state, set the parameter to STATE_ONLY. To disregard the effective state, set the parameter to NONE. &lt;br>&lt;br>The effective state of a GSLB service is the ability of the corresponding virtual server to serve traffic. The effective state of the load balancing virtual server, which is transferred to the GSLB service, is UP even if only one virtual server in the backup chain of virtual servers is in the UP state.&lt;br>Default value: NONE&lt;br>Possible values = NONE, STATE_ONLY</td><tr><tr><td>comment</td><td>&lt;String></td><td>Read-write</td><td>Any comments that you might want to associate with the GSLB virtual server.</td><tr><tr><td>somethod</td><td>&lt;String></td><td>Read-write</td><td>Type of threshold that, when exceeded, triggers spillover. Available settings function as follows:&lt;br>* CONNECTION - Spillover occurs when the number of client connections exceeds the threshold.&lt;br>* DYNAMICCONNECTION - Spillover occurs when the number of client connections at the GSLB virtual server exceeds the sum of the maximum client (Max Clients) settings for bound GSLB services. Do not specify a spillover threshold for this setting, because the threshold is implied by the Max Clients settings of the bound GSLB services.&lt;br>* BANDWIDTH - Spillover occurs when the bandwidth consumed by the GSLB virtual servers incoming and outgoing traffic exceeds the threshold. &lt;br>* HEALTH - Spillover occurs when the percentage of weights of the GSLB services that are UP drops below the threshold. For example, if services gslbSvc1, gslbSvc2, and gslbSvc3 are bound to a virtual server, with weights 1, 2, and 3, and the spillover threshold is 50%, spillover occurs if gslbSvc1 and gslbSvc3 or gslbSvc2 and gslbSvc3 transition to DOWN. &lt;br>* NONE - Spillover does not occur.&lt;br>Possible values = CONNECTION, DYNAMICCONNECTION, BANDWIDTH, HEALTH, NONE</td><tr><tr><td>sopersistence</td><td>&lt;String></td><td>Read-write</td><td>If spillover occurs, maintain source IP address based persistence for both primary and backup GSLB virtual servers.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>sopersistencetimeout</td><td>&lt;Double></td><td>Read-write</td><td>Timeout for spillover persistence, in minutes.&lt;br>Default value: 2&lt;br>Minimum value = 2&lt;br>Maximum value = 1440</td><tr><tr><td>sothreshold</td><td>&lt;Double></td><td>Read-write</td><td>Threshold at which spillover occurs. Specify an integer for the CONNECTION spillover method, a bandwidth value in kilobits per second for the BANDWIDTH method (do not enter the units), or a percentage for the HEALTH method (do not enter the percentage symbol).&lt;br>Minimum value = 1&lt;br>Maximum value = 4294967287</td><tr><tr><td>sobackupaction</td><td>&lt;String></td><td>Read-write</td><td>Action to be performed if spillover is to take effect, but no backup chain to spillover is usable or exists.&lt;br>Possible values = DROP, ACCEPT, REDIRECT</td><tr><tr><td>appflowlog</td><td>&lt;String></td><td>Read-write</td><td>Enable logging appflow flow information.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>backupvserver</td><td>&lt;String></td><td>Read-write</td><td>Name of the backup GSLB virtual server to which the appliance should to forward requests if the status of the primary GSLB virtual server is down or exceeds its spillover threshold.&lt;br>Minimum length = 1</td><tr><tr><td>servicename</td><td>&lt;String></td><td>Read-write</td><td>Name of the GSLB service for which to change the weight.&lt;br>Minimum length = 1</td><tr><tr><td>weight</td><td>&lt;Double></td><td>Read-write</td><td>Weight to assign to the GSLB service.&lt;br>Minimum value = 1&lt;br>Maximum value = 100</td><tr><tr><td>domainname</td><td>&lt;String></td><td>Read-write</td><td>Domain name for which to change the time to live (TTL) and/or backup service IP address.&lt;br>Minimum length = 1</td><tr><tr><td>ttl</td><td>&lt;Double></td><td>Read-write</td><td>Time to live (TTL) for the domain.&lt;br>Minimum value = 1</td><tr><tr><td>backupip</td><td>&lt;String></td><td>Read-write</td><td>The IP address of the backup service for the specified domain name. Used when all the services bound to the domain are down, or when the backup chain of virtual servers is down.&lt;br>Minimum length = 1</td><tr><tr><td>cookie_domain</td><td>&lt;String></td><td>Read-write</td><td>The cookie domain for the GSLB site. Used when inserting the GSLB site cookie in the HTTP response.&lt;br>Minimum length = 1</td><tr><tr><td>cookietimeout</td><td>&lt;Double></td><td>Read-write</td><td>Timeout, in minutes, for the GSLB site cookie.&lt;br>Minimum value = 0&lt;br>Maximum value = 1440</td><tr><tr><td>sitedomainttl</td><td>&lt;Double></td><td>Read-write</td><td>TTL, in seconds, for all internally created site domains (created when a site prefix is configured on a GSLB service) that are associated with this virtual server.&lt;br>Minimum value = 1</td><tr><tr><td>newname</td><td>&lt;String></td><td>Read-write</td><td>New name for the GSLB virtual server.&lt;br>Minimum length = 1</td><tr><tr><td>curstate</td><td>&lt;String></td><td>Read-only</td><td>State of the gslb vserver.&lt;br>Possible values = UP, DOWN, UNKNOWN, BUSY, OUT OF SERVICE, GOING OUT OF SERVICE, DOWN WHEN GOING OUT OF SERVICE, NS_EMPTY_STR, Unknown, DISABLED</td><tr><tr><td>status</td><td>&lt;Integer></td><td>Read-only</td><td>Current status of the gslb vserver. During the initial phase if the configured lb method is not round robin , the vserver will adopt round robin to distribute traffic for a predefined number of requests.</td><tr><tr><td>lbrrreason</td><td>&lt;Integer></td><td>Read-only</td><td>Reason why a vserver is in RR. The following are the reasons:&lt;br>1 - MEP is DOWN (GSLB)&lt;br>2 - LB method has changed&lt;br>3 - Bound services state changed to UP&lt;br>4 - A new service is bound&lt;br>5 - Startup RR factor has changed&lt;br>6 - LB feature is enabled&lt;br>7 - Load monitor is not active on a service&lt;br>8 - Vserver is Enabled&lt;br>9 - SSL feature is Enabled&lt;br>10 - All bound services have reached threshold. Using effective state to load balance (GSLB)&lt;br>11 - Primary state of bound services are not UP. Using effective state to load balance (GSLB)&lt;br>12 - No LB decision can be made as all bound services have either reached threshold or are not UP (GSLB)&lt;br>13 - All load monitors are active&lt;br>.</td><tr><tr><td>iscname</td><td>&lt;String></td><td>Read-only</td><td>is cname feature set on vserver.&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>sitepersistence</td><td>&lt;String></td><td>Read-only</td><td>Type of Site Persistence set.&lt;br>Possible values = ConnectionProxy, HTTPRedirect, NONE</td><tr><tr><td>totalservices</td><td>&lt;Double></td><td>Read-only</td><td>Total number of services bound to the vserver.</td><tr><tr><td>activeservices</td><td>&lt;Double></td><td>Read-only</td><td>Total number of active services bound to the vserver.</td><tr><tr><td>statechangetimesec</td><td>&lt;String></td><td>Read-only</td><td>Time when last state change happened. Seconds part.</td><tr><tr><td>statechangetimemsec</td><td>&lt;Double></td><td>Read-only</td><td>Time at which last state change happened. Milliseconds part.</td><tr><tr><td>tickssincelaststatechange</td><td>&lt;Double></td><td>Read-only</td><td>Time in 10 millisecond ticks since the last state change.</td><tr><tr><td>health</td><td>&lt;Double></td><td>Read-only</td><td>Health of vserver based on percentage of weights of active svcs/all svcs. This does not consider administratively disabled svcs.</td><tr><tr><td>policyname</td><td>&lt;String></td><td>Read-only</td><td>Name of the policy bound to the GSLB vserver.</td><tr><tr><td>priority</td><td>&lt;Double></td><td>Read-only</td><td>Priority.&lt;br>Minimum value = 1&lt;br>Maximum value = 2147483647</td><tr><tr><td>gotopriorityexpression</td><td>&lt;String></td><td>Read-only</td><td>Expression specifying the priority of the next policy which will get evaluated if the current policy rule evaluates to TRUE.&lt;br> o If gotoPriorityExpression is not present or if it is equal to END then the policy bank evaluation ends here&lt;br> o Else if the gotoPriorityExpression is equal to NEXT then the next policy in the priority order is evaluated.&lt;br> o Else gotoPriorityExpression is evaluated. The result of gotoPriorityExpression (which has to be a number) is processed as follows:&lt;br> - An UNDEF event is triggered if&lt;br> . gotoPriorityExpression cannot be evaluated&lt;br> . gotoPriorityExpression evaluates to number which is smaller than the maximum priority in the policy bank but is not same as any policys priority&lt;br> . gotoPriorityExpression evaluates to a priority that is smaller than the current policys priority&lt;br> - If the gotoPriorityExpression evaluates to the priority of the current policy then the next policy in the priority order is evaluated.&lt;br> - If the gotoPriorityExpression evaluates to the priority of a policy further ahead in the list then that policy will be evaluated next.&lt;br> This field is applicable only to rewrite and responder policies.</td><tr><tr><td>type</td><td>&lt;String></td><td>Read-only</td><td>The bindpoint to which the policy is bound.&lt;br>Possible values = REQUEST, RESPONSE</td><tr><tr><td>vsvrbindsvcip</td><td>&lt;String></td><td>Read-only</td><td>used for showing the ip of bound entities.</td><tr><tr><td>vsvrbindsvcport</td><td>&lt;Integer></td><td>Read-only</td><td>used for showing ports of bound entities.&lt;br>Range 1 - 65535&lt;br>* in CLI is represented as 65535 in NITRO API</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [DELETE](#delete) | [UPDATE](#update) | [UNSET](#unset) | [ENABLE](#enable) | [DISABLE](#disable) | [RENAME](#rename) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbvserver
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"gslbvserver":{      "name":<String_value>,      "servicetype":<String_value>,      "iptype":<String_value>,      "dnsrecordtype":<String_value>,      "lbmethod":<String_value>,      "backupsessiontimeout":<Double_value>,      "backuplbmethod":<String_value>,      "netmask":<String_value>,      "v6netmasklen":<Double_value>,      "tolerance":<Double_value>,      "persistencetype":<String_value>,      "persistenceid":<Double_value>,      "persistmask":<String_value>,      "v6persistmasklen":<Double_value>,      "timeout":<Double_value>,      "edr":<String_value>,      "ecs":<String_value>,      "ecsaddrvalidation":<String_value>,      "mir":<String_value>,      "disableprimaryondown":<String_value>,      "dynamicweight":<String_value>,      "state":<String_value>,      "considereffectivestate":<String_value>,      "comment":<String_value>,      "somethod":<String_value>,      "sopersistence":<String_value>,      "sopersistencetimeout":<Double_value>,      "sothreshold":<Double_value>,      "sobackupaction":<String_value>,      "appflowlog":<String_value>}}```
Response:
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbvserver/name_value&lt;String&gt;
HTTP Method: DELETE
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbvserver
HTTP Method: PUT
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"gslbvserver":{      "name":<String_value>,      "iptype":<String_value>,      "dnsrecordtype":<String_value>,      "backupvserver":<String_value>,      "backupsessiontimeout":<Double_value>,      "lbmethod":<String_value>,      "backuplbmethod":<String_value>,      "netmask":<String_value>,      "v6netmasklen":<Double_value>,      "tolerance":<Double_value>,      "persistencetype":<String_value>,      "persistenceid":<Double_value>,      "persistmask":<String_value>,      "v6persistmasklen":<Double_value>,      "timeout":<Double_value>,      "edr":<String_value>,      "ecs":<String_value>,      "ecsaddrvalidation":<String_value>,      "mir":<String_value>,      "disableprimaryondown":<String_value>,      "dynamicweight":<String_value>,      "considereffectivestate":<String_value>,      "somethod":<String_value>,      "sopersistence":<String_value>,      "sopersistencetimeout":<Double_value>,      "sothreshold":<Double_value>,      "sobackupaction":<String_value>,      "servicename":<String_value>,      "weight":<Double_value>,      "domainname":<String_value>,      "ttl":<Double_value>,      "backupip":<String_value>,      "cookie_domain":<String_value>,      "cookietimeout":<Double_value>,      "sitedomainttl":<Double_value>,      "comment":<String_value>,      "appflowlog":<String_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbvserver?action=unset
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"gslbvserver":{      "name":<String_value>,      "backupvserver":true,      "sothreshold":true,      "iptype":true,      "dnsrecordtype":true,      "backupsessiontimeout":true,      "lbmethod":true,      "backuplbmethod":true,      "netmask":true,      "v6netmasklen":true,      "tolerance":true,      "persistencetype":true,      "persistenceid":true,      "persistmask":true,      "v6persistmasklen":true,      "timeout":true,      "edr":true,      "ecs":true,      "ecsaddrvalidation":true,      "mir":true,      "disableprimaryondown":true,      "dynamicweight":true,      "considereffectivestate":true,      "somethod":true,      "sopersistence":true,      "sopersistencetimeout":true,      "sobackupaction":true,      "servicename":true,      "weight":true,      "comment":true,      "appflowlog":true}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###enable



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbvserver?action=enable
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"gslbvserver":{      "name":<String_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###disable



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbvserver?action=disable
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"gslbvserver":{      "name":<String_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###rename



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbvserver?action=rename
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"gslbvserver":{      "name":<String_value>,      "newname":<String_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbvserver
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbvserver?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


filter
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbvserver?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of gslbvserver resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbvserver?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).


pagination
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbvserver?pagesize=#no;pageno=#no
Use this query-parameter to get the gslbvserver resources in chunks.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "gslbvserver": [ {      "name":<String_value>,      "servicetype":<String_value>,      "state":<String_value>,      "iptype":<String_value>,      "dnsrecordtype":<String_value>,      "persistencetype":<String_value>,      "persistenceid":<Double_value>,      "lbmethod":<String_value>,      "backuplbmethod":<String_value>,      "tolerance":<Double_value>,      "timeout":<Double_value>,      "curstate":<String_value>,      "netmask":<String_value>,      "v6netmasklen":<Double_value>,      "persistmask":<String_value>,      "v6persistmasklen":<Double_value>,      "servicename":<String_value>,      "weight":<Double_value>,      "domainname":<String_value>,      "ttl":<Double_value>,      "backupip":<String_value>,      "cookie_domain":<String_value>,      "cookietimeout":<Double_value>,      "sitedomainttl":<Double_value>,      "status":<Integer_value>,      "lbrrreason":<Integer_value>,      "backupvserver":<String_value>,      "backupsessiontimeout":<Double_value>,      "edr":<String_value>,      "ecs":<String_value>,      "ecsaddrvalidation":<String_value>,      "mir":<String_value>,      "disableprimaryondown":<String_value>,      "dynamicweight":<String_value>,      "iscname":<String_value>,      "sitepersistence":<String_value>,      "considereffectivestate":<String_value>,      "totalservices":<Double_value>,      "activeservices":<Double_value>,      "statechangetimesec":<String_value>,      "statechangetimemsec":<Double_value>,      "tickssincelaststatechange":<Double_value>,      "comment":<String_value>,      "sopersistencetimeout":<Double_value>,      "somethod":<String_value>,      "sobackupaction":<String_value>,      "sopersistence":<String_value>,      "sothreshold":<Double_value>,      "health":<Double_value>,      "appflowlog":<String_value>,      "policyname":<String_value>,      "priority":<Double_value>,      "gotopriorityexpression":<String_value>,      "type":<String_value>,      "vsvrbindsvcip":<String_value>,      "vsvrbindsvcport":<Integer_value>}]}```



###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbvserver/name_value&lt;String&gt;
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbvserver/name_value&lt;String&gt;?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbvserver/name_value&lt;String&gt;?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "gslbvserver": [ {      "name":<String_value>,      "servicetype":<String_value>,      "state":<String_value>,      "iptype":<String_value>,      "dnsrecordtype":<String_value>,      "persistencetype":<String_value>,      "persistenceid":<Double_value>,      "lbmethod":<String_value>,      "backuplbmethod":<String_value>,      "tolerance":<Double_value>,      "timeout":<Double_value>,      "curstate":<String_value>,      "netmask":<String_value>,      "v6netmasklen":<Double_value>,      "persistmask":<String_value>,      "v6persistmasklen":<Double_value>,      "servicename":<String_value>,      "weight":<Double_value>,      "domainname":<String_value>,      "ttl":<Double_value>,      "backupip":<String_value>,      "cookie_domain":<String_value>,      "cookietimeout":<Double_value>,      "sitedomainttl":<Double_value>,      "status":<Integer_value>,      "lbrrreason":<Integer_value>,      "backupvserver":<String_value>,      "backupsessiontimeout":<Double_value>,      "edr":<String_value>,      "ecs":<String_value>,      "ecsaddrvalidation":<String_value>,      "mir":<String_value>,      "disableprimaryondown":<String_value>,      "dynamicweight":<String_value>,      "iscname":<String_value>,      "sitepersistence":<String_value>,      "considereffectivestate":<String_value>,      "totalservices":<Double_value>,      "activeservices":<Double_value>,      "statechangetimesec":<String_value>,      "statechangetimemsec":<Double_value>,      "tickssincelaststatechange":<Double_value>,      "comment":<String_value>,      "sopersistencetimeout":<Double_value>,      "somethod":<String_value>,      "sobackupaction":<String_value>,      "sopersistence":<String_value>,      "sothreshold":<Double_value>,      "health":<Double_value>,      "appflowlog":<String_value>,      "policyname":<String_value>,      "priority":<Double_value>,      "gotopriorityexpression":<String_value>,      "type":<String_value>,      "vsvrbindsvcip":<String_value>,      "vsvrbindsvcport":<Integer_value>}]}```



###count



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbvserver?count=yes
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: 
{ "gslbvserver": [ { "__count": "#no"} ] }


