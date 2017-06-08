#crvserver

Configuration for CR virtual server resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the cache redirection virtual server. Must begin with an ASCII alphanumeric or underscore (_) character, and must contain only ASCII alphanumeric, underscore, hash (#), period (.), space, colon (:), at sign (@), equal sign (=), and hyphen (-) characters. Can be changed after the cache redirection virtual server is created. The following requirement applies only to the NetScaler CLI: If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, ?my server? or ?my server?).&lt;br>Minimum length = 1</td><tr><tr><td>td</td><td>&lt;Double></td><td>Read-write</td><td>Integer value that uniquely identifies the traffic domain in which you want to configure the entity. If you do not specify an ID, the entity becomes part of the default traffic domain, which has an ID of 0.&lt;br>Minimum value = 0&lt;br>Maximum value = 4094</td><tr><tr><td>servicetype</td><td>&lt;String></td><td>Read-write</td><td>Protocol (type of service) handled by the virtual server.&lt;br>Possible values = HTTP, SSL, NNTP, HDX</td><tr><tr><td>ipv46</td><td>&lt;String></td><td>Read-write</td><td>IPv4 or IPv6 address of the cache redirection virtual server. Usually a public IP address. Clients send connection requests to this IP address. Note: For a transparent cache redirection virtual server, use an asterisk (*) to specify a wildcard virtual server address.</td><tr><tr><td>port</td><td>&lt;Integer></td><td>Read-write</td><td>Port number of the virtual server.&lt;br>Default value: 80&lt;br>Minimum value = 1&lt;br>Maximum value = 65534</td><tr><tr><td>range</td><td>&lt;Double></td><td>Read-write</td><td>Number of consecutive IP addresses, starting with the address specified by the IPAddress parameter, to include in a range of addresses assigned to this virtual server.&lt;br>Default value: 1&lt;br>Minimum value = 1&lt;br>Maximum value = 254</td><tr><tr><td>cachetype</td><td>&lt;String></td><td>Read-write</td><td>Mode of operation for the cache redirection virtual server. Available settings function as follows: * TRANSPARENT - Intercept all traffic flowing to the appliance and apply cache redirection policies to determine whether content should be served from the cache or from the origin server. * FORWARD - Resolve the hostname of the incoming request, by using a DNS server, and forward requests for non-cacheable content to the resolved origin servers. Cacheable requests are sent to the configured cache servers. * REVERSE - Configure reverse proxy caches for specific origin servers. Incoming traffic directed to the reverse proxy can either be served from a cache server or be sent to the origin server with or without modification to the URL.&lt;br>Default value: TRANSPARENT&lt;br>Possible values = TRANSPARENT, REVERSE, FORWARD</td><tr><tr><td>redirect</td><td>&lt;String></td><td>Read-write</td><td>Type of cache server to which to redirect HTTP requests. Available settings function as follows: * CACHE - Direct all requests to the cache. * POLICY - Apply the cache redirection policy to determine whether the request should be directed to the cache or to the origin. * ORIGIN - Direct all requests to the origin server.&lt;br>Default value: POLICY&lt;br>Possible values = CACHE, POLICY, ORIGIN</td><tr><tr><td>onpolicymatch</td><td>&lt;String></td><td>Read-write</td><td>Redirect requests that match the policy to either the cache or the origin server, as specified. Note: For this option to work, you must set the cache redirection type to POLICY.&lt;br>Default value: ORIGIN&lt;br>Possible values = CACHE, ORIGIN</td><tr><tr><td>redirecturl</td><td>&lt;String></td><td>Read-write</td><td>URL of the server to which to redirect traffic if the cache redirection virtual server configured on the NetScaler appliance becomes unavailable.&lt;br>Minimum length = 1&lt;br>Maximum length = 128</td><tr><tr><td>clttimeout</td><td>&lt;Double></td><td>Read-write</td><td>Time-out value, in seconds, after which to terminate an idle client connection.&lt;br>Minimum value = 0&lt;br>Maximum value = 31536000</td><tr><tr><td>precedence</td><td>&lt;String></td><td>Read-write</td><td>Type of policy (URL or RULE) that takes precedence on the cache redirection virtual server. Applies only to cache redirection virtual servers that have both URL and RULE based policies. If you specify URL, URL based policies are applied first, in the following order: 1. Domain and exact URL 2. Domain, prefix and suffix 3. Domain and suffix 4. Domain and prefix 5. Domain only 6. Exact URL 7. Prefix and suffix 8. Suffix only 9. Prefix only 10. Default If you specify RULE, the rule based policies are applied before URL based policies are applied.&lt;br>Default value: RULE&lt;br>Possible values = RULE, URL</td><tr><tr><td>arp</td><td>&lt;String></td><td>Read-write</td><td>Use ARP to determine the destination MAC address.&lt;br>Possible values = ON, OFF</td><tr><tr><td>ghost</td><td>&lt;String></td><td>Read-write</td><td>.&lt;br>Possible values = ON, OFF</td><tr><tr><td>map</td><td>&lt;String></td><td>Read-write</td><td>Obsolete.&lt;br>Possible values = ON, OFF</td><tr><tr><td>format</td><td>&lt;String></td><td>Read-write</td><td>.&lt;br>Possible values = ON, OFF</td><tr><tr><td>via</td><td>&lt;String></td><td>Read-write</td><td>Insert a via header in each HTTP request. In the case of a cache miss, the request is redirected from the cache server to the origin server. This header indicates whether the request is being sent from a cache server.&lt;br>Default value: ON&lt;br>Possible values = ON, OFF</td><tr><tr><td>cachevserver</td><td>&lt;String></td><td>Read-write</td><td>Name of the default cache virtual server to which to redirect requests (the default target of the cache redirection virtual server).&lt;br>Minimum length = 1</td><tr><tr><td>dnsvservername</td><td>&lt;String></td><td>Read-write</td><td>Name of the DNS virtual server that resolves domain names arriving at the forward proxy virtual server. Note: This parameter applies only to forward proxy virtual servers, not reverse or transparent.&lt;br>Minimum length = 1</td><tr><tr><td>destinationvserver</td><td>&lt;String></td><td>Read-write</td><td>Destination virtual server for a transparent or forward proxy cache redirection virtual server.&lt;br>Minimum length = 1</td><tr><tr><td>domain</td><td>&lt;String></td><td>Read-write</td><td>Default domain for reverse proxies. Domains are configured to direct an incoming request from a specified source domain to a specified target domain. There can be several configured pairs of source and target domains. You can select one pair to be the default. If the host header or URL of an incoming request does not include a source domain, this option sends the request to the specified target domain.&lt;br>Minimum length = 1</td><tr><tr><td>sopersistencetimeout</td><td>&lt;Double></td><td>Read-write</td><td>Time-out, in minutes, for spillover persistence.&lt;br>Minimum value = 2&lt;br>Maximum value = 24</td><tr><tr><td>sothreshold</td><td>&lt;Double></td><td>Read-write</td><td>For CONNECTION (or) DYNAMICCONNECTION spillover, the number of connections above which the virtual server enters spillover mode. For BANDWIDTH spillover, the amount of incoming and outgoing traffic (in Kbps) before spillover. For HEALTH spillover, the percentage of active services (by weight) below which spillover occurs.&lt;br>Minimum value = 1</td><tr><tr><td>reuse</td><td>&lt;String></td><td>Read-write</td><td>Reuse TCP connections to the origin server across client connections. Do not set this parameter unless the Service Type parameter is set to HTTP. If you set this parameter to OFF, the possible settings of the Redirect parameter function as follows: * CACHE - TCP connections to the cache servers are not reused. * ORIGIN - TCP connections to the origin servers are not reused. * POLICY - TCP connections to the origin servers are not reused. If you set the Reuse parameter to ON, connections to origin servers and connections to cache servers are reused.&lt;br>Default value: ON&lt;br>Possible values = ON, OFF</td><tr><tr><td>state</td><td>&lt;String></td><td>Read-write</td><td>Initial state of the cache redirection virtual server.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>downstateflush</td><td>&lt;String></td><td>Read-write</td><td>Perform delayed cleanup of connections to this virtual server.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>backupvserver</td><td>&lt;String></td><td>Read-write</td><td>Name of the backup virtual server to which traffic is forwarded if the active server becomes unavailable.&lt;br>Minimum length = 1</td><tr><tr><td>disableprimaryondown</td><td>&lt;String></td><td>Read-write</td><td>Continue sending traffic to a backup virtual server even after the primary virtual server comes UP from the DOWN state.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>l2conn</td><td>&lt;String></td><td>Read-write</td><td>Use L2 parameters, such as MAC, VLAN, and channel to identify a connection.&lt;br>Possible values = ON, OFF</td><tr><tr><td>backendssl</td><td>&lt;String></td><td>Read-write</td><td>Decides whether the backend connection made by NS to the origin server will be HTTP or SSL. Applicable only for SSL type CR Forward proxy vserver.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>listenpolicy</td><td>&lt;String></td><td>Read-write</td><td>String specifying the listen policy for the cache redirection virtual server. Can be either an in-line expression or the name of a named expression.&lt;br>Default value: "None"</td><tr><tr><td>listenpriority</td><td>&lt;Double></td><td>Read-write</td><td>Priority of the listen policy specified by the Listen Policy parameter. The lower the number, higher the priority.&lt;br>Default value: 101&lt;br>Minimum value = 0&lt;br>Maximum value = 100</td><tr><tr><td>tcpprofilename</td><td>&lt;String></td><td>Read-write</td><td>Name of the profile containing TCP configuration information for the cache redirection virtual server.&lt;br>Minimum length = 1&lt;br>Maximum length = 127</td><tr><tr><td>httpprofilename</td><td>&lt;String></td><td>Read-write</td><td>Name of the profile containing HTTP configuration information for cache redirection virtual server.&lt;br>Minimum length = 1&lt;br>Maximum length = 127</td><tr><tr><td>comment</td><td>&lt;String></td><td>Read-write</td><td>Comments associated with this virtual server.&lt;br>Maximum length = 256</td><tr><tr><td>srcipexpr</td><td>&lt;String></td><td>Read-write</td><td>Expression used to extract the source IP addresses from the requests originating from the cache. Can be either an in-line expression or the name of a named expression.&lt;br>Minimum length = 1&lt;br>Maximum length = 1500</td><tr><tr><td>originusip</td><td>&lt;String></td><td>Read-write</td><td>Use the client?s IP address as the source IP address in requests sent to the origin server. Note: You can enable this parameter to implement fully transparent CR deployment.&lt;br>Default value: OFF&lt;br>Possible values = ON, OFF</td><tr><tr><td>useportrange</td><td>&lt;String></td><td>Read-write</td><td>Use a port number from the port range (set by using the set ns param command, or in the Create Virtual Server (Cache Redirection) dialog box) as the source port in the requests sent to the origin server.&lt;br>Default value: OFF&lt;br>Possible values = ON, OFF</td><tr><tr><td>appflowlog</td><td>&lt;String></td><td>Read-write</td><td>Enable logging of AppFlow information.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>netprofile</td><td>&lt;String></td><td>Read-write</td><td>Name of the network profile containing network configurations for the cache redirection virtual server.&lt;br>Minimum length = 1&lt;br>Maximum length = 127</td><tr><tr><td>icmpvsrresponse</td><td>&lt;String></td><td>Read-write</td><td>Criterion for responding to PING requests sent to this virtual server. If ACTIVE, respond only if the virtual server is available. If PASSIVE, respond even if the virtual server is not available.&lt;br>Default value: PASSIVE&lt;br>Possible values = PASSIVE, ACTIVE</td><tr><tr><td>rhistate</td><td>&lt;String></td><td>Read-write</td><td>A host route is injected according to the setting on the virtual servers * If set to PASSIVE on all the virtual servers that share the IP address, the appliance always injects the hostroute. * If set to ACTIVE on all the virtual servers that share the IP address, the appliance injects even if one virtual server is UP. * If set to ACTIVE on some virtual servers and PASSIVE on the others, the appliance, injects even if one virtual server set to ACTIVE is UP.&lt;br>Default value: PASSIVE&lt;br>Possible values = PASSIVE, ACTIVE</td><tr><tr><td>newname</td><td>&lt;String></td><td>Read-write</td><td>New name for the cache redirection virtual server. Must begin with an ASCII alphanumeric or underscore (_) character, and must contain only ASCII alphanumeric, underscore, hash (#), period (.), space, colon (:), at sign (@), equal sign (=), and hyphen (-) characters. If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, ?my name? or ?my name?).&lt;br>Minimum length = 1</td><tr><tr><td>ip</td><td>&lt;String></td><td>Read-only</td><td>.</td><tr><tr><td>value</td><td>&lt;String></td><td>Read-only</td><td>The ssl card status for the transparent ssl cr vserver.&lt;br>Possible values = Certkey not bound, SSL feature disabled</td><tr><tr><td>ngname</td><td>&lt;String></td><td>Read-only</td><td>Nodegroup devno to which this crvserver belongs to.</td><tr><tr><td>type</td><td>&lt;String></td><td>Read-only</td><td>Virtual server type.&lt;br>Possible values = CONTENT, ADDRESS</td><tr><tr><td>curstate</td><td>&lt;String></td><td>Read-only</td><td>The state of the cr vserver.&lt;br>Possible values = UP, DOWN, UNKNOWN, BUSY, OUT OF SERVICE, GOING OUT OF SERVICE, DOWN WHEN GOING OUT OF SERVICE, NS_EMPTY_STR, Unknown, DISABLED</td><tr><tr><td>status</td><td>&lt;Integer></td><td>Read-only</td><td>Status.</td><tr><tr><td>authentication</td><td>&lt;String></td><td>Read-only</td><td>Authentication.&lt;br>Possible values = ON, OFF</td><tr><tr><td>homepage</td><td>&lt;String></td><td>Read-only</td><td>Home page.</td><tr><tr><td>rule</td><td>&lt;String></td><td>Read-only</td><td>Rule.</td><tr><tr><td>policyname</td><td>&lt;String></td><td>Read-only</td><td>Policies bound to this vserver.</td><tr><tr><td>servicename</td><td>&lt;String></td><td>Read-only</td><td>Service name.</td><tr><tr><td>weight</td><td>&lt;Double></td><td>Read-only</td><td>Weight for this service.</td><tr><tr><td>targetvserver</td><td>&lt;String></td><td>Read-only</td><td>The CSW target server names.</td><tr><tr><td>priority</td><td>&lt;Double></td><td>Read-only</td><td>The priority for the policy.</td><tr><tr><td>somethod</td><td>&lt;String></td><td>Read-only</td><td>The spillover factor. When the main virtual server reaches this spillover threshold, it will give further traffic to the backupvserver.&lt;br>Possible values = CONNECTION, DYNAMICCONNECTION, BANDWIDTH, HEALTH, NONE</td><tr><tr><td>sopersistence</td><td>&lt;String></td><td>Read-only</td><td>The state of spillover persistence.&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>lbvserver</td><td>&lt;String></td><td>Read-only</td><td>The Default target server name.&lt;br>Minimum length = 1</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [DELETE](#delete) | [UPDATE](#update) | [UNSET](#unset) | [ENABLE](#enable) | [DISABLE](#disable) | [RENAME](#rename) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>},"sessionid":"##sessionid","crvserver":{      "name":<String_value>,      "td":<Double_value>,      "servicetype":<String_value>,      "ipv46":<String_value>,                  "port":<Integer_value>,                  "range":<Double_value>,      "cachetype":<String_value>,      "redirect":<String_value>,      "onpolicymatch":<String_value>,      "redirecturl":<String_value>,      "clttimeout":<Double_value>,      "precedence":<String_value>,      "arp":<String_value>,      "ghost":<String_value>,      "map":<String_value>,      "format":<String_value>,      "via":<String_value>,      "cachevserver":<String_value>,      "dnsvservername":<String_value>,      "destinationvserver":<String_value>,      "domain":<String_value>,      "sopersistencetimeout":<Double_value>,      "sothreshold":<Double_value>,      "reuse":<String_value>,      "state":<String_value>,      "downstateflush":<String_value>,      "backupvserver":<String_value>,      "disableprimaryondown":<String_value>,      "l2conn":<String_value>,      "backendssl":<String_value>,      "listenpolicy":<String_value>,      "listenpriority":<Double_value>,      "tcpprofilename":<String_value>,      "httpprofilename":<String_value>,      "comment":<String_value>,      "srcipexpr":<String_value>,      "originusip":<String_value>,      "useportrange":<String_value>,      "appflowlog":<String_value>,      "netprofile":<String_value>,      "icmpvsrresponse":<String_value>,      "rhistate":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/crvserver/name_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/crvserver/name_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","crvserver":{      "name":<String_value>,      "ipv46":<String_value>,      "redirect":<String_value>,      "onpolicymatch":<String_value>,      "precedence":<String_value>,      "arp":<String_value>,      "via":<String_value>,      "cachevserver":<String_value>,      "dnsvservername":<String_value>,      "destinationvserver":<String_value>,      "domain":<String_value>,      "reuse":<String_value>,      "backupvserver":<String_value>,      "disableprimaryondown":<String_value>,      "redirecturl":<String_value>,      "clttimeout":<Double_value>,      "downstateflush":<String_value>,      "l2conn":<String_value>,      "backendssl":<String_value>,      "listenpolicy":<String_value>,      "listenpriority":<Double_value>,      "tcpprofilename":<String_value>,      "httpprofilename":<String_value>,      "netprofile":<String_value>,      "comment":<String_value>,      "srcipexpr":<String_value>,      "originusip":<String_value>,      "useportrange":<String_value>,      "appflowlog":<String_value>,      "icmpvsrresponse":<String_value>,      "rhistate":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","crvserver":{      "name":<String_value>,      "cachevserver":true,      "dnsvservername":true,      "destinationvserver":true,      "domain":true,      "backupvserver":true,      "clttimeout":true,      "redirecturl":true,      "l2conn":true,      "backendssl":true,      "originusip":true,      "useportrange":true,      "srcipexpr":true,      "tcpprofilename":true,      "httpprofilename":true,      "appflowlog":true,      "netprofile":true,      "icmpvsrresponse":true,      "redirect":true,      "onpolicymatch":true,      "precedence":true,      "arp":true,      "via":true,      "reuse":true,      "disableprimaryondown":true,      "downstateflush":true,      "listenpolicy":true,      "listenpriority":true,      "comment":true,      "rhistate":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###enable



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"enable"},"sessionid":"##sessionid","crvserver":{      "name":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###disable



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"disable"},"sessionid":"##sessionid","crvserver":{      "name":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###rename



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"rename"},"sessionid":"##sessionid","crvserver":{      "name":<String_value>,      "newname":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/crvserver
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/crvserver?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of crvserver resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/crvserver?view=summary
Use this query-parameter to get the summary output of crvserver resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/crvserver?pagesize=#no;pageno=#no
Use this query-parameter to get the crvserver resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/crvserver?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "crvserver": [ {      "name":<String_value>,      "ip":<String_value>,      "td":<Double_value>,      "ipv46":<String_value>,      "value":<String_value>,      "port":<Integer_value>,      "range":<Double_value>,      "servicetype":<String_value>,      "ngname":<String_value>,      "type":<String_value>,      "curstate":<String_value>,      "status":<Integer_value>,      "cachetype":<String_value>,      "redirect":<String_value>,      "onpolicymatch":<String_value>,      "precedence":<String_value>,      "redirecturl":<String_value>,      "authentication":<String_value>,      "homepage":<String_value>,      "dnsvservername":<String_value>,      "domain":<String_value>,      "rule":<String_value>,      "policyname":<String_value>,      "servicename":<String_value>,      "weight":<Double_value>,      "cachevserver":<String_value>,      "targetvserver":<String_value>,      "backupvserver":<String_value>,      "priority":<Double_value>,      "clttimeout":<Double_value>,      "somethod":<String_value>,      "sopersistence":<String_value>,      "sopersistencetimeout":<Double_value>,      "sothreshold":<Double_value>,      "reuse":<String_value>,      "arp":<String_value>,      "destinationvserver":<String_value>,      "via":<String_value>,      "downstateflush":<String_value>,      "disableprimaryondown":<String_value>,      "l2conn":<String_value>,      "backendssl":<String_value>,      "comment":<String_value>,      "listenpolicy":<String_value>,      "listenpriority":<Double_value>,      "tcpprofilename":<String_value>,      "httpprofilename":<String_value>,      "srcipexpr":<String_value>,      "originusip":<String_value>,      "useportrange":<String_value>,      "appflowlog":<String_value>,      "netprofile":<String_value>,      "icmpvsrresponse":<String_value>,      "rhistate":<String_value>,      "lbvserver":<String_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/crvserver/name_value&lt;String&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "crvserver": [ {      "name":<String_value>,      "ip":<String_value>,      "td":<Double_value>,      "ipv46":<String_value>,      "value":<String_value>,      "port":<Integer_value>,      "range":<Double_value>,      "servicetype":<String_value>,      "ngname":<String_value>,      "type":<String_value>,      "curstate":<String_value>,      "status":<Integer_value>,      "cachetype":<String_value>,      "redirect":<String_value>,      "onpolicymatch":<String_value>,      "precedence":<String_value>,      "redirecturl":<String_value>,      "authentication":<String_value>,      "homepage":<String_value>,      "dnsvservername":<String_value>,      "domain":<String_value>,      "rule":<String_value>,      "policyname":<String_value>,      "servicename":<String_value>,      "weight":<Double_value>,      "cachevserver":<String_value>,      "targetvserver":<String_value>,      "backupvserver":<String_value>,      "priority":<Double_value>,      "clttimeout":<Double_value>,      "somethod":<String_value>,      "sopersistence":<String_value>,      "sopersistencetimeout":<Double_value>,      "sothreshold":<Double_value>,      "reuse":<String_value>,      "arp":<String_value>,      "destinationvserver":<String_value>,      "via":<String_value>,      "downstateflush":<String_value>,      "disableprimaryondown":<String_value>,      "l2conn":<String_value>,      "backendssl":<String_value>,      "comment":<String_value>,      "listenpolicy":<String_value>,      "listenpriority":<Double_value>,      "tcpprofilename":<String_value>,      "httpprofilename":<String_value>,      "srcipexpr":<String_value>,      "originusip":<String_value>,      "useportrange":<String_value>,      "appflowlog":<String_value>,      "netprofile":<String_value>,      "icmpvsrresponse":<String_value>,      "rhistate":<String_value>,      "lbvserver":<String_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/crvserver?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",crvserver: [ { "__count": "#no"} ] }


