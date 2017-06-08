#vpnvserver

Configuration for VPN virtual server resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the NetScaler Gateway virtual server. Must begin with an ASCII alphabetic or underscore (_) character, and must contain only ASCII alphanumeric, underscore, hash (#), period (.), space, colon (:), at (@), equals (=), and hyphen (-) characters. Can be changed after the virtual server is created. The following requirement applies only to the NetScaler CLI: If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my server" or my server).&lt;br>Minimum length = 1</td><tr><tr><td>servicetype</td><td>&lt;String></td><td>Read-write</td><td>Protocol used by the NetScaler Gateway virtual server.&lt;br>Default value: SSL&lt;br>Possible values = SSL</td><tr><tr><td>ipv46</td><td>&lt;String></td><td>Read-write</td><td>IPv4 or IPv6 address of the NetScaler Gateway virtual server. Usually a public IP address. User devices send connection requests to this IP address.&lt;br>Minimum length = 1</td><tr><tr><td>range</td><td>&lt;Double></td><td>Read-write</td><td>Range of NetScaler Gateway virtual server IP addresses. The consecutively numbered range of IP addresses begins with the address specified by the IP Address parameter. In the configuration utility, select Network VServer to enter a range.&lt;br>Default value: 1&lt;br>Minimum value = 1</td><tr><tr><td>port</td><td>&lt;Integer></td><td>Read-write</td><td>TCP port on which the virtual server listens.&lt;br>Minimum value = 1&lt;br>Range 1 - 65535</td><tr><tr><td>state</td><td>&lt;String></td><td>Read-write</td><td>State of the virtual server. If the virtual server is disabled, requests are not processed.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>authentication</td><td>&lt;String></td><td>Read-write</td><td>Require authentication for users connecting to NetScaler Gateway.&lt;br>Default value: ON&lt;br>Possible values = ON, OFF</td><tr><tr><td>doublehop</td><td>&lt;String></td><td>Read-write</td><td>Use the NetScaler Gateway appliance in a double-hop configuration. A double-hop deployment provides an extra layer of security for the internal network by using three firewalls to divide the DMZ into two stages. Such a deployment can have one appliance in the DMZ and one appliance in the secure network.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>maxaaausers</td><td>&lt;Double></td><td>Read-write</td><td>Maximum number of concurrent user sessions allowed on this virtual server. The actual number of users allowed to log on to this virtual server depends on the total number of user licenses.</td><tr><tr><td>icaonly</td><td>&lt;String></td><td>Read-write</td><td>User can log on in Basic mode only, through either Citrix Receiver or a browser. Users are not allowed to connect by using the NetScaler Gateway Plug-in.&lt;br>Default value: OFF&lt;br>Possible values = ON, OFF</td><tr><tr><td>icaproxysessionmigration</td><td>&lt;String></td><td>Read-write</td><td>This option determines if an existing ICA Proxy session is transferred when the user logs on from another device.&lt;br>Default value: OFF&lt;br>Possible values = ON, OFF</td><tr><tr><td>advancedepa</td><td>&lt;String></td><td>Read-write</td><td>This option tells whether advanced EPA is enabled on this virtual server.&lt;br>Default value: OFF&lt;br>Possible values = ON, OFF</td><tr><tr><td>devicecert</td><td>&lt;String></td><td>Read-write</td><td>Indicates whether device certificate check as a part of EPA is on or off.&lt;br>Default value: OFF&lt;br>Possible values = ON, OFF</td><tr><tr><td>certkeynames</td><td>&lt;String></td><td>Read-write</td><td>Name of the certificate key that was bound to the corresponding SSL virtual server as the Certificate Authority for the device certificate.&lt;br>Minimum length = 1&lt;br>Maximum length = 127</td><tr><tr><td>downstateflush</td><td>&lt;String></td><td>Read-write</td><td>Close existing connections when the virtual server is marked DOWN, which means the server might have timed out. Disconnecting existing connections frees resources and in certain cases speeds recovery of overloaded load balancing setups. Enable this setting on servers in which the connections can safely be closed when they are marked DOWN. Do not enable DOWN state flush on servers that must complete their transactions.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>listenpolicy</td><td>&lt;String></td><td>Read-write</td><td>String specifying the listen policy for the NetScaler Gateway virtual server. Can be either a named expression or a default syntax expression. The NetScaler Gateway virtual server processes only the traffic for which the expression evaluates to true.&lt;br>Default value: "none"</td><tr><tr><td>listenpriority</td><td>&lt;Double></td><td>Read-write</td><td>Integer specifying the priority of the listen policy. A higher number specifies a lower priority. If a request matches the listen policies of more than one virtual server, the virtual server whose listen policy has the highest priority (the lowest priority number) accepts the request.&lt;br>Default value: 101&lt;br>Minimum value = 0&lt;br>Maximum value = 100</td><tr><tr><td>tcpprofilename</td><td>&lt;String></td><td>Read-write</td><td>Name of the TCP profile to assign to this virtual server.&lt;br>Minimum length = 1&lt;br>Maximum length = 127</td><tr><tr><td>httpprofilename</td><td>&lt;String></td><td>Read-write</td><td>Name of the HTTP profile to assign to this virtual server.&lt;br>Minimum length = 1&lt;br>Maximum length = 127</td><tr><tr><td>comment</td><td>&lt;String></td><td>Read-write</td><td>Any comments associated with the virtual server.</td><tr><tr><td>appflowlog</td><td>&lt;String></td><td>Read-write</td><td>Log AppFlow records that contain standard NetFlow or IPFIX information, such as time stamps for the beginning and end of a flow, packet count, and byte count. Also log records that contain application-level information, such as HTTP web addresses, HTTP request methods and response status codes, server response time, and latency.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>icmpvsrresponse</td><td>&lt;String></td><td>Read-write</td><td>Criterion for responding to PING requests sent to this virtual server. If this parameter is set to ACTIVE, respond only if the virtual server is available. With the PASSIVE setting, respond even if the virtual server is not available.&lt;br>Default value: PASSIVE&lt;br>Possible values = PASSIVE, ACTIVE</td><tr><tr><td>rhistate</td><td>&lt;String></td><td>Read-write</td><td>A host route is injected according to the setting on the virtual servers. * If set to PASSIVE on all the virtual servers that share the IP address, the appliance always injects the hostroute. * If set to ACTIVE on all the virtual servers that share the IP address, the appliance injects even if one virtual server is UP. * If set to ACTIVE on some virtual servers and PASSIVE on the others, the appliance injects even if one virtual server set to ACTIVE is UP.&lt;br>Default value: PASSIVE&lt;br>Possible values = PASSIVE, ACTIVE</td><tr><tr><td>netprofile</td><td>&lt;String></td><td>Read-write</td><td>The name of the network profile.&lt;br>Minimum length = 1&lt;br>Maximum length = 127</td><tr><tr><td>cginfrahomepageredirect</td><td>&lt;String></td><td>Read-write</td><td>When client requests ShareFile resources and NetScaler Gateway detects that the user is unauthenticated or the user session has expired, disabling this option takes the user to the originally requested ShareFile resource after authentication (instead of taking the user to the default VPN home page).&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>maxloginattempts</td><td>&lt;Double></td><td>Read-write</td><td>Maximum number of logon attempts.&lt;br>Minimum value = 1&lt;br>Maximum value = 255</td><tr><tr><td>failedlogintimeout</td><td>&lt;Double></td><td>Read-write</td><td>Number of minutes an account will be locked if user exceeds maximum permissible attempts.&lt;br>Minimum value = 1</td><tr><tr><td>l2conn</td><td>&lt;String></td><td>Read-write</td><td>Use Layer 2 parameters (channel number, MAC address, and VLAN ID) in addition to the 4-tuple (;lt;source IP;gt;:;lt;source port;gt;::;lt;destination IP;gt;:;lt;destination port;gt;) that is used to identify a connection. Allows multiple TCP and non-TCP connections with the same 4-tuple to coexist on the NetScaler appliance.&lt;br>Possible values = ON, OFF</td><tr><tr><td>deploymenttype</td><td>&lt;String></td><td>Read-write</td><td>.&lt;br>Default value: 5&lt;br>Possible values = NONE, ICA_WEBINTERFACE, ICA_STOREFRONT, MOBILITY, WIONNS</td><tr><tr><td>newname</td><td>&lt;String></td><td>Read-write</td><td>New name for the NetScaler Gateway virtual server. Must begin with an ASCII alphabetic or underscore (_) character, and must contain only ASCII alphanumeric, underscore, hash (#), period (.), space, colon (:), at (@), equals (=), and hyphen (-) characters. The following requirement applies only to the NetScaler CLI: If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my server" or my server).&lt;br>Minimum length = 1</td><tr><tr><td>ip</td><td>&lt;String></td><td>Read-only</td><td>The Virtual IP address of the VPN virtual server.</td><tr><tr><td>value</td><td>&lt;String></td><td>Read-only</td><td>Indicates whether or not the certificate is bound or if SSL offload is disabled.&lt;br>Possible values = Certkey not bound, SSL feature disabled</td><tr><tr><td>type</td><td>&lt;String></td><td>Read-only</td><td>The type of virtual server; for example, CONTENT based or ADDRESS based.&lt;br>Possible values = CONTENT, ADDRESS</td><tr><tr><td>curstate</td><td>&lt;String></td><td>Read-only</td><td>The current state of the virtual server, as UP, DOWN, BUSY, and so on.&lt;br>Possible values = UP, DOWN, UNKNOWN, BUSY, OUT OF SERVICE, GOING OUT OF SERVICE, DOWN WHEN GOING OUT OF SERVICE, NS_EMPTY_STR, Unknown, DISABLED</td><tr><tr><td>status</td><td>&lt;Integer></td><td>Read-only</td><td>Whether or not this virtual server responds to ARPs and whether or not round-robin selection is temporarily in effect.</td><tr><tr><td>cachetype</td><td>&lt;String></td><td>Read-only</td><td>Virtual server cache type. The options are: TRANSPARENT, REVERSE, and FORWARD.&lt;br>Possible values = TRANSPARENT, REVERSE, FORWARD</td><tr><tr><td>redirect</td><td>&lt;String></td><td>Read-only</td><td>The cache redirect policy. The valid redirect policies are: l. CACHE - Directs all requests to the cache. 2. POLICY - Applies cache redirection policy to determine whether the request should be directed to the cache or origin. This is the default setting. 3. ORIGIN - Directs all requests to the origin server.&lt;br>Possible values = CACHE, POLICY, ORIGIN</td><tr><tr><td>precedence</td><td>&lt;String></td><td>Read-only</td><td>This argument is used only when configuring content switching on the specified virtual server. This is applicable only if both the URL and RULE-based policies have been configured on the same virtual server. It specifies the type of policy (URL or RULE) that takes precedence on the content switching virtual server. The default setting is RULE. l URL - In this case, the incoming request is matched against the URL-based policies before the rule-based policies. l RULE - In this case, the incoming request is matched against the rule-based policies before the URL-based policies. For all URL-based policies, the precedence hierarchy is: 1. Domain and exact URL 2. Domain, prefix, and suffix 3. Domain and suffix 4. Domain and prefix 5. Domain only 6. Exact URL 7. Prefix and suffix 8. Suffix only 9. Prefix only 10. Default.&lt;br>Possible values = RULE, URL</td><tr><tr><td>redirecturl</td><td>&lt;String></td><td>Read-only</td><td>The URL where traffic is redirected if the virtual server in system becomes unavailable. WARNING! Make sure that the domain you specify in the URL does not match the domain specified in the -d domainName argument of the ###add cs policy### command. If the same domain is specified in both arguments, the request will be continuously redirected to the same unavailable virtual server in the system. If so, the user may not get the requested content.</td><tr><tr><td>curaaausers</td><td>&lt;Double></td><td>Read-only</td><td>The number of current users logged on to this virtual server.</td><tr><tr><td>curtotalusers</td><td>&lt;Double></td><td>Read-only</td><td>The total number of current users connected through this virtual server.</td><tr><tr><td>domain</td><td>&lt;String></td><td>Read-only</td><td>The domain name of the server for which a service needs to be added. If the IP address has been specified, the domain name does not need to be specified.</td><tr><tr><td>rule</td><td>&lt;String></td><td>Read-only</td><td>The name of the rule, or expression, if any, that policy for the VPN server is to use. Rules are combinations of expressions. Expressions are simple conditions, such as a test for equality, applied to operands, such as a URL string or an IP address. Expression syntax is described in the Installation and Configuration Guide. The default rule is ns_true.&lt;br>Minimum length = 1</td><tr><tr><td>policy</td><td>&lt;String></td><td>Read-only</td><td>The name of the policy, if any, bound to the VPN virtual server.</td><tr><tr><td>servicename</td><td>&lt;String></td><td>Read-only</td><td>The name of the service, if any, to which the virtual server policy is bound.</td><tr><tr><td>weight</td><td>&lt;Double></td><td>Read-only</td><td>Weight for this service, if any. This weight is used when the system performs load balancing, giving greater priority to a specific service. It is useful when the services bound to a virtual server are of different capacity.</td><tr><tr><td>cachevserver</td><td>&lt;String></td><td>Read-only</td><td>The name of the default target cache virtual server, if any, to which requests are redirected.</td><tr><tr><td>backupvserver</td><td>&lt;String></td><td>Read-only</td><td>The name of the backup VPN virtual server for this VPN virtual server.</td><tr><tr><td>priority</td><td>&lt;Double></td><td>Read-only</td><td>The priority, if any, of the VPN virtual server policy.</td><tr><tr><td>clttimeout</td><td>&lt;Double></td><td>Read-only</td><td>The idle time, if any, in seconds after which the client connection is terminated.</td><tr><tr><td>somethod</td><td>&lt;String></td><td>Read-only</td><td>VPN client applications are allocated from a block of intranet IP addresses. That block may be exhausted after a certain number of connections. This switch specifies the method used to determine whether or not a new connection will spill over, or exhaust, the allocated block of intranet IP addresses for that application. Possible values are CONNECTION or DYNAMICCONNECTION. CONNECTION means that a static integer value is the hard limit for the spillover threshold. The spillover threshold is described below. DYNAMICCONNECTION means that the spillover threshold is set according to the maximum number of connections defined for the VPN virtual server.&lt;br>Possible values = CONNECTION, DYNAMICCONNECTION, BANDWIDTH, HEALTH, NONE</td><tr><tr><td>sothreshold</td><td>&lt;Double></td><td>Read-only</td><td>VPN client applications are allocated from a block of intranet IP addresses. That block may be exhausted after a certain number of connections. The value of this option is the number of client connections after which the mapped IP address is used as the client source IP address instead of an address from the allocated block of intranet IP addresses.</td><tr><tr><td>sopersistence</td><td>&lt;String></td><td>Read-only</td><td>Whether or not cookie-based site persistance is enabled for this VPN vserver. Possible values are ConnectionProxy, HTTPRedirect, or NONE.&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>sopersistencetimeout</td><td>&lt;Double></td><td>Read-only</td><td>The timeout, if any, for cookie-based site persistance of this VPN vserver.</td><tr><tr><td>usemip</td><td>&lt;String></td><td>Read-only</td><td>Deprecated. See map below.&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>map</td><td>&lt;String></td><td>Read-only</td><td>Whether or not mapped IP addresses are ON or OFF. Mapped IP addresses are source IP addresses for the virtual servers running on the NetScaler. Mapped IP addresses are used by the system to connect to the backend servers.&lt;br>Possible values = ON, OFF</td><tr><tr><td>bindpoint</td><td>&lt;String></td><td>Read-only</td><td>Bindpoint to which the policy is bound.&lt;br>Possible values = REQUEST, RESPONSE, ICA_REQUEST, OTHERTCP_REQUEST</td><tr><tr><td>gotopriorityexpression</td><td>&lt;String></td><td>Read-only</td><td>Next priority expression.</td><tr><tr><td>disableprimaryondown</td><td>&lt;String></td><td>Read-only</td><td>Tells whether traffic will continue reaching backup virtual servers even after the primary virtual server comes UP from DOWN state.&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>secondary</td><td>&lt;Boolean></td><td>Read-only</td><td>Binds the authentication policy as the secondary policy to use in a two-factor configuration. A user must then authenticate not only via a primary authentication method but also via a secondary authentication method. User groups are aggregated across both. The user name must be exactly the same for both authentication methods, but they can require different passwords.</td><tr><tr><td>groupextraction</td><td>&lt;Boolean></td><td>Read-only</td><td>Binds the authentication policy to a tertiary chain which will be used only for group extraction. The user will not authenticate against this server, and this will only be called if primary and/or secondary authentication has succeeded.</td><tr><tr><td>epaprofileoptional</td><td>&lt;Boolean></td><td>Read-only</td><td>Mark the EPA profile optional for preauthentication EPA profile. User would be shown a logon page even if the EPA profile fails to evaluate.</td><tr><tr><td>ngname</td><td>&lt;String></td><td>Read-only</td><td>Node group devno to which this authentication virtual sever belongs.</td><tr><tr><td>response</td><td>&lt;String></td><td>Read-only</td><td>.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [DELETE](#delete) | [UPDATE](#update) | [UNSET](#unset) | [ENABLE](#enable) | [DISABLE](#disable) | [RENAME](#rename) | [CHECK](#check) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>},"sessionid":"##sessionid","vpnvserver":{      "name":<String_value>,      "servicetype":<String_value>,      "ipv46":<String_value>,                  "range":<Double_value>,      "port":<Integer_value>,      "state":<String_value>,      "authentication":<String_value>,      "doublehop":<String_value>,      "maxaaausers":<Double_value>,      "icaonly":<String_value>,      "icaproxysessionmigration":<String_value>,      "advancedepa":<String_value>,      "devicecert":<String_value>,      "certkeynames":<String_value>,      "downstateflush":<String_value>,      "listenpolicy":<String_value>,      "listenpriority":<Double_value>,      "tcpprofilename":<String_value>,      "httpprofilename":<String_value>,      "comment":<String_value>,      "appflowlog":<String_value>,      "icmpvsrresponse":<String_value>,      "rhistate":<String_value>,      "netprofile":<String_value>,      "cginfrahomepageredirect":<String_value>,      "maxloginattempts":<Double_value>,                  "failedlogintimeout":<Double_value>,      "l2conn":<String_value>,      "deploymenttype":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/vpnvserver/name_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/vpnvserver/name_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","vpnvserver":{      "name":<String_value>,      "ipv46":<String_value>,      "authentication":<String_value>,      "doublehop":<String_value>,      "icaonly":<String_value>,      "icaproxysessionmigration":<String_value>,      "advancedepa":<String_value>,      "devicecert":<String_value>,      "certkeynames":<String_value>,      "maxaaausers":<Double_value>,      "downstateflush":<String_value>,      "listenpolicy":<String_value>,      "listenpriority":<Double_value>,      "tcpprofilename":<String_value>,      "httpprofilename":<String_value>,      "comment":<String_value>,      "appflowlog":<String_value>,      "icmpvsrresponse":<String_value>,      "rhistate":<String_value>,      "netprofile":<String_value>,      "cginfrahomepageredirect":<String_value>,      "maxloginattempts":<Double_value>,      "failedlogintimeout":<Double_value>,      "l2conn":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","vpnvserver":{      "name":<String_value>,      "authentication":true,      "doublehop":true,      "icaonly":true,      "icaproxysessionmigration":true,      "advancedepa":true,      "devicecert":true,      "certkeynames":true,      "maxaaausers":true,      "downstateflush":true,      "listenpolicy":true,      "listenpriority":true,      "tcpprofilename":true,      "httpprofilename":true,      "comment":true,      "appflowlog":true,      "icmpvsrresponse":true,      "rhistate":true,      "netprofile":true,      "cginfrahomepageredirect":true,      "maxloginattempts":true,      "l2conn":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###enable



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"enable"},"sessionid":"##sessionid","vpnvserver":{      "name":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###disable



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"disable"},"sessionid":"##sessionid","vpnvserver":{      "name":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###rename



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"rename"},"sessionid":"##sessionid","vpnvserver":{      "name":<String_value>,      "newname":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###check



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"check"},"sessionid":"##sessionid","vpnvserver":{      "name":<String_value>,}}```
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "vpnvserver": [ {      "name":<String_value>,      "response":<String_value>}]}```



###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/vpnvserver
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/vpnvserver?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of vpnvserver resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/vpnvserver?view=summary
Use this query-parameter to get the summary output of vpnvserver resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/vpnvserver?pagesize=#no;pageno=#no
Use this query-parameter to get the vpnvserver resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/vpnvserver?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "vpnvserver": [ {      "name":<String_value>,      "ip":<String_value>,      "ipv46":<String_value>,      "value":<String_value>,      "port":<Integer_value>,      "range":<Double_value>,      "servicetype":<String_value>,      "type":<String_value>,      "curstate":<String_value>,      "status":<Integer_value>,      "cachetype":<String_value>,      "redirect":<String_value>,      "precedence":<String_value>,      "redirecturl":<String_value>,      "authentication":<String_value>,      "doublehop":<String_value>,      "icaonly":<String_value>,      "icaproxysessionmigration":<String_value>,      "advancedepa":<String_value>,      "devicecert":<String_value>,      "certkeynames":<String_value>,      "maxaaausers":<Double_value>,      "curaaausers":<Double_value>,      "curtotalusers":<Double_value>,      "domain":<String_value>,      "rule":<String_value>,      "policyname":<String_value>,      "policy":<String_value>,      "servicename":<String_value>,      "weight":<Double_value>,      "cachevserver":<String_value>,      "backupvserver":<String_value>,      "priority":<Double_value>,      "clttimeout":<Double_value>,      "somethod":<String_value>,      "sothreshold":<Double_value>,      "sopersistence":<String_value>,      "sopersistencetimeout":<Double_value>,      "usemip":<String_value>,      "map":<String_value>,      "downstateflush":<String_value>,      "bindpoint":<String_value>,      "gotopriorityexpression":<String_value>,      "disableprimaryondown":<String_value>,      "listenpolicy":<String_value>,      "listenpriority":<Double_value>,      "tcpprofilename":<String_value>,      "httpprofilename":<String_value>,      "comment":<String_value>,      "appflowlog":<String_value>,      "icmpvsrresponse":<String_value>,      "rhistate":<String_value>,      "netprofile":<String_value>,      "cginfrahomepageredirect":<String_value>,      "maxloginattempts":<Double_value>,      "failedlogintimeout":<Double_value>,      "secondary":<Boolean_value>,      "groupextraction":<Boolean_value>,      "deploymenttype":<String_value>,      "epaprofileoptional":<Boolean_value>,      "ngname":<String_value>,      "state":<String_value>,      "l2conn":<String_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/vpnvserver/name_value&lt;String&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "vpnvserver": [ {      "name":<String_value>,      "ip":<String_value>,      "ipv46":<String_value>,      "value":<String_value>,      "port":<Integer_value>,      "range":<Double_value>,      "servicetype":<String_value>,      "type":<String_value>,      "curstate":<String_value>,      "status":<Integer_value>,      "cachetype":<String_value>,      "redirect":<String_value>,      "precedence":<String_value>,      "redirecturl":<String_value>,      "authentication":<String_value>,      "doublehop":<String_value>,      "icaonly":<String_value>,      "icaproxysessionmigration":<String_value>,      "advancedepa":<String_value>,      "devicecert":<String_value>,      "certkeynames":<String_value>,      "maxaaausers":<Double_value>,      "curaaausers":<Double_value>,      "curtotalusers":<Double_value>,      "domain":<String_value>,      "rule":<String_value>,      "policyname":<String_value>,      "policy":<String_value>,      "servicename":<String_value>,      "weight":<Double_value>,      "cachevserver":<String_value>,      "backupvserver":<String_value>,      "priority":<Double_value>,      "clttimeout":<Double_value>,      "somethod":<String_value>,      "sothreshold":<Double_value>,      "sopersistence":<String_value>,      "sopersistencetimeout":<Double_value>,      "usemip":<String_value>,      "map":<String_value>,      "downstateflush":<String_value>,      "bindpoint":<String_value>,      "gotopriorityexpression":<String_value>,      "disableprimaryondown":<String_value>,      "listenpolicy":<String_value>,      "listenpriority":<Double_value>,      "tcpprofilename":<String_value>,      "httpprofilename":<String_value>,      "comment":<String_value>,      "appflowlog":<String_value>,      "icmpvsrresponse":<String_value>,      "rhistate":<String_value>,      "netprofile":<String_value>,      "cginfrahomepageredirect":<String_value>,      "maxloginattempts":<Double_value>,      "failedlogintimeout":<Double_value>,      "secondary":<Boolean_value>,      "groupextraction":<Boolean_value>,      "deploymenttype":<String_value>,      "epaprofileoptional":<Boolean_value>,      "ngname":<String_value>,      "state":<String_value>,      "l2conn":<String_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/vpnvserver?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",vpnvserver: [ { "__count": "#no"} ] }


