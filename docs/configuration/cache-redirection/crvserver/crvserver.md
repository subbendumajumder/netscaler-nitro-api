#crvserver

Configuration for CR virtual server resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the cache redirection virtual server. Must begin with an ASCII alphanumeric or underscore (_) character, and must contain only ASCII alphanumeric, underscore, hash (#), period (.), space, colon (:), at sign (@), equal sign (=), and hyphen (-) characters. Can be changed after the cache redirection virtual server is created.<br>The following requirement applies only to the NetScaler CLI: <br>If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my server" or 'my server').<br>Minimum length = 1</td></tr><tr><td>td</td><td>&lt;Double></td><td>Read-write</td><td>Integer value that uniquely identifies the traffic domain in which you want to configure the entity. If you do not specify an ID, the entity becomes part of the default traffic domain, which has an ID of 0.<br>Minimum value = 0<br>Maximum value = 4094</td></tr><tr><td>servicetype</td><td>&lt;String></td><td>Read-write</td><td>Protocol (type of service) handled by the virtual server.<br>Possible values = HTTP, SSL, NNTP, HDX</td></tr><tr><td>ipv46</td><td>&lt;String></td><td>Read-write</td><td>IPv4 or IPv6 address of the cache redirection virtual server. Usually a public IP address. Clients send connection requests to this IP address.<br>Note: For a transparent cache redirection virtual server, use an asterisk (*) to specify a wildcard virtual server address.</td></tr><tr><td>port</td><td>&lt;Integer></td><td>Read-write</td><td>Port number of the virtual server.<br>Default value: 80<br>Minimum value = 1<br>Maximum value = 65534</td></tr><tr><td>range</td><td>&lt;Double></td><td>Read-write</td><td>Number of consecutive IP addresses, starting with the address specified by the IPAddress parameter, to include in a range of addresses assigned to this virtual server.<br>Default value: 1<br>Minimum value = 1<br>Maximum value = 254</td></tr><tr><td>cachetype</td><td>&lt;String></td><td>Read-write</td><td>Mode of operation for the cache redirection virtual server. Available settings function as follows:<br>* TRANSPARENT - Intercept all traffic flowing to the appliance and apply cache redirection policies to determine whether content should be served from the cache or from the origin server.<br>* FORWARD - Resolve the hostname of the incoming request, by using a DNS server, and forward requests for non-cacheable content to the resolved origin servers. Cacheable requests are sent to the configured cache servers.<br>* REVERSE - Configure reverse proxy caches for specific origin servers. Incoming traffic directed to the reverse proxy can either be served from a cache server or be sent to the origin server with or without modification to the URL.<br>Possible values = TRANSPARENT, REVERSE, FORWARD</td></tr><tr><td>redirect</td><td>&lt;String></td><td>Read-write</td><td>Type of cache server to which to redirect HTTP requests. Available settings function as follows:<br>* CACHE - Direct all requests to the cache.<br>* POLICY - Apply the cache redirection policy to determine whether the request should be directed to the cache or to the origin.<br>* ORIGIN - Direct all requests to the origin server.<br>Default value: POLICY<br>Possible values = CACHE, POLICY, ORIGIN</td></tr><tr><td>onpolicymatch</td><td>&lt;String></td><td>Read-write</td><td>Redirect requests that match the policy to either the cache or the origin server, as specified.<br>Note: For this option to work, you must set the cache redirection type to POLICY.<br>Default value: ORIGIN<br>Possible values = CACHE, ORIGIN</td></tr><tr><td>redirecturl</td><td>&lt;String></td><td>Read-write</td><td>URL of the server to which to redirect traffic if the cache redirection virtual server configured on the NetScaler appliance becomes unavailable.<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>clttimeout</td><td>&lt;Double></td><td>Read-write</td><td>Time-out value, in seconds, after which to terminate an idle client connection.<br>Minimum value = 0<br>Maximum value = 31536000</td></tr><tr><td>precedence</td><td>&lt;String></td><td>Read-write</td><td>Type of policy (URL or RULE) that takes precedence on the cache redirection virtual server. Applies only to cache redirection virtual servers that have both URL and RULE based policies. If you specify URL, URL based policies are applied first, in the following order:<br>1. Domain and exact URL<br>2. Domain, prefix and suffix<br>3. Domain and suffix<br>4. Domain and prefix<br>5. Domain only<br>6. Exact URL<br>7. Prefix and suffix<br>8. Suffix only<br>9. Prefix only<br>10. Default<br>If you specify RULE, the rule based policies are applied before URL based policies are applied.<br>Default value: RULE<br>Possible values = RULE, URL</td></tr><tr><td>arp</td><td>&lt;String></td><td>Read-write</td><td>Use ARP to determine the destination MAC address.<br>Possible values = ON, OFF</td></tr><tr><td>ghost</td><td>&lt;String></td><td>Read-write</td><td>.<br>Possible values = ON, OFF</td></tr><tr><td>map</td><td>&lt;String></td><td>Read-write</td><td>Obsolete.<br>Possible values = ON, OFF</td></tr><tr><td>format</td><td>&lt;String></td><td>Read-write</td><td>.<br>Possible values = ON, OFF</td></tr><tr><td>via</td><td>&lt;String></td><td>Read-write</td><td>Insert a via header in each HTTP request. In the case of a cache miss, the request is redirected from the cache server to the origin server. This header indicates whether the request is being sent from a cache server.<br>Default value: ON<br>Possible values = ON, OFF</td></tr><tr><td>cachevserver</td><td>&lt;String></td><td>Read-write</td><td>Name of the default cache virtual server to which to redirect requests (the default target of the cache redirection virtual server).<br>Minimum length = 1</td></tr><tr><td>dnsvservername</td><td>&lt;String></td><td>Read-write</td><td>Name of the DNS virtual server that resolves domain names arriving at the forward proxy virtual server.<br>Note: This parameter applies only to forward proxy virtual servers, not reverse or transparent.<br>Minimum length = 1</td></tr><tr><td>destinationvserver</td><td>&lt;String></td><td>Read-write</td><td>Destination virtual server for a transparent or forward proxy cache redirection virtual server.<br>Minimum length = 1</td></tr><tr><td>domain</td><td>&lt;String></td><td>Read-write</td><td>Default domain for reverse proxies. Domains are configured to direct an incoming request from a specified source domain to a specified target domain. There can be several configured pairs of source and target domains. You can select one pair to be the default. If the host header or URL of an incoming request does not include a source domain, this option sends the request to the specified target domain.<br>Minimum length = 1</td></tr><tr><td>sopersistencetimeout</td><td>&lt;Double></td><td>Read-write</td><td>Time-out, in minutes, for spillover persistence.<br>Minimum value = 2<br>Maximum value = 24</td></tr><tr><td>sothreshold</td><td>&lt;Double></td><td>Read-write</td><td>For CONNECTION (or) DYNAMICCONNECTION spillover, the number of connections above which the virtual server enters spillover mode. For BANDWIDTH spillover, the amount of incoming and outgoing traffic (in Kbps) before spillover. For HEALTH spillover, the percentage of active services (by weight) below which spillover occurs.<br>Minimum value = 1</td></tr><tr><td>reuse</td><td>&lt;String></td><td>Read-write</td><td>Reuse TCP connections to the origin server across client connections. Do not set this parameter unless the Service Type parameter is set to HTTP. If you set this parameter to OFF, the possible settings of the Redirect parameter function as follows:<br>* CACHE - TCP connections to the cache servers are not reused.<br>* ORIGIN - TCP connections to the origin servers are not reused. <br>* POLICY - TCP connections to the origin servers are not reused.<br>If you set the Reuse parameter to ON, connections to origin servers and connections to cache servers are reused.<br>Default value: ON<br>Possible values = ON, OFF</td></tr><tr><td>state</td><td>&lt;String></td><td>Read-write</td><td>Initial state of the cache redirection virtual server.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>downstateflush</td><td>&lt;String></td><td>Read-write</td><td>Perform delayed cleanup of connections to this virtual server.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>backupvserver</td><td>&lt;String></td><td>Read-write</td><td>Name of the backup virtual server to which traffic is forwarded if the active server becomes unavailable.<br>Minimum length = 1</td></tr><tr><td>disableprimaryondown</td><td>&lt;String></td><td>Read-write</td><td>Continue sending traffic to a backup virtual server even after the primary virtual server comes UP from the DOWN state.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>l2conn</td><td>&lt;String></td><td>Read-write</td><td>Use L2 parameters, such as MAC, VLAN, and channel to identify a connection.<br>Possible values = ON, OFF</td></tr><tr><td>backendssl</td><td>&lt;String></td><td>Read-write</td><td>Decides whether the backend connection made by NS to the origin server will be HTTP or SSL. Applicable only for SSL type CR Forward proxy vserver.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>listenpolicy</td><td>&lt;String></td><td>Read-write</td><td>String specifying the listen policy for the cache redirection virtual server. Can be either an in-line expression or the name of a named expression.<br>Default value: "NONE"</td></tr><tr><td>listenpriority</td><td>&lt;Double></td><td>Read-write</td><td>Priority of the listen policy specified by the Listen Policy parameter. The lower the number, higher the priority.<br>Default value: 101<br>Minimum value = 0<br>Maximum value = 100</td></tr><tr><td>tcpprofilename</td><td>&lt;String></td><td>Read-write</td><td>Name of the profile containing TCP configuration information for the cache redirection virtual server.<br>Minimum length = 1<br>Maximum length = 127</td></tr><tr><td>httpprofilename</td><td>&lt;String></td><td>Read-write</td><td>Name of the profile containing HTTP configuration information for cache redirection virtual server.<br>Minimum length = 1<br>Maximum length = 127</td></tr><tr><td>comment</td><td>&lt;String></td><td>Read-write</td><td>Comments associated with this virtual server.<br>Maximum length = 256</td></tr><tr><td>srcipexpr</td><td>&lt;String></td><td>Read-write</td><td>Expression used to extract the source IP addresses from the requests originating from the cache. Can be either an in-line expression or the name of a named expression.<br>Minimum length = 1<br>Maximum length = 1500</td></tr><tr><td>originusip</td><td>&lt;String></td><td>Read-write</td><td>Use the client's IP address as the source IP address in requests sent to the origin server. <br>Note: You can enable this parameter to implement fully transparent CR deployment.<br>Possible values = ON, OFF</td></tr><tr><td>useportrange</td><td>&lt;String></td><td>Read-write</td><td>Use a port number from the port range (set by using the set ns param command, or in the Create Virtual Server (Cache Redirection) dialog box) as the source port in the requests sent to the origin server.<br>Default value: OFF<br>Possible values = ON, OFF</td></tr><tr><td>appflowlog</td><td>&lt;String></td><td>Read-write</td><td>Enable logging of AppFlow information.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>netprofile</td><td>&lt;String></td><td>Read-write</td><td>Name of the network profile containing network configurations for the cache redirection virtual server.<br>Minimum length = 1<br>Maximum length = 127</td></tr><tr><td>icmpvsrresponse</td><td>&lt;String></td><td>Read-write</td><td>Criterion for responding to PING requests sent to this virtual server. If ACTIVE, respond only if the virtual server is available. If PASSIVE, respond even if the virtual server is not available.<br>Default value: PASSIVE<br>Possible values = PASSIVE, ACTIVE</td></tr><tr><td>rhistate</td><td>&lt;String></td><td>Read-write</td><td>A host route is injected according to the setting on the virtual servers<br>* If set to PASSIVE on all the virtual servers that share the IP address, the appliance always injects the hostroute.<br>* If set to ACTIVE on all the virtual servers that share the IP address, the appliance injects even if one virtual server is UP.<br>* If set to ACTIVE on some virtual servers and PASSIVE on the others, the appliance, injects even if one virtual server set to ACTIVE is UP.<br>Default value: PASSIVE<br>Possible values = PASSIVE, ACTIVE</td></tr><tr><td>newname</td><td>&lt;String></td><td>Read-write</td><td>New name for the cache redirection virtual server. Must begin with an ASCII alphanumeric or underscore (_) character, and must contain only ASCII alphanumeric, underscore, hash (#), period (.), space, colon (:), at sign (@), equal sign (=), and hyphen (-) characters. If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my name" or 'my name').<br>Minimum length = 1</td></tr><tr><td>ip</td><td>&lt;String></td><td>Read-only</td><td>.</td></tr><tr><td>value</td><td>&lt;String></td><td>Read-only</td><td>The ssl card status for the transparent ssl cr vserver.<br>Possible values = Certkey not bound, SSL feature disabled</td></tr><tr><td>ngname</td><td>&lt;String></td><td>Read-only</td><td>Nodegroup devno to which this crvserver belongs to.</td></tr><tr><td>type</td><td>&lt;String></td><td>Read-only</td><td>Virtual server type.<br>Possible values = CONTENT, ADDRESS</td></tr><tr><td>curstate</td><td>&lt;String></td><td>Read-only</td><td>The state of the cr vserver.<br>Possible values = UP, DOWN, UNKNOWN, BUSY, OUT OF SERVICE, GOING OUT OF SERVICE, DOWN WHEN GOING OUT OF SERVICE, NS_EMPTY_STR, Unknown, DISABLED</td></tr><tr><td>status</td><td>&lt;Integer></td><td>Read-only</td><td>Status.</td></tr><tr><td>sc</td><td>&lt;String></td><td>Read-only</td><td>The state of SureConnect the specified virtual server.<br>Possible values = ON, OFF</td></tr><tr><td>authentication</td><td>&lt;String></td><td>Read-only</td><td>Authentication.<br>Possible values = ON, OFF</td></tr><tr><td>homepage</td><td>&lt;String></td><td>Read-only</td><td>Home page.</td></tr><tr><td>rule</td><td>&lt;String></td><td>Read-only</td><td>Rule.</td></tr><tr><td>policyname</td><td>&lt;String></td><td>Read-only</td><td>Policies bound to this vserver.</td></tr><tr><td>pipolicyhits</td><td>&lt;Double></td><td>Read-only</td><td>Number of hits.</td></tr><tr><td>servicename</td><td>&lt;String></td><td>Read-only</td><td>Service name.</td></tr><tr><td>weight</td><td>&lt;Double></td><td>Read-only</td><td>Weight for this service.</td></tr><tr><td>targetvserver</td><td>&lt;String></td><td>Read-only</td><td>The CSW target server names.</td></tr><tr><td>priority</td><td>&lt;Double></td><td>Read-only</td><td>The priority for the policy.</td></tr><tr><td>somethod</td><td>&lt;String></td><td>Read-only</td><td>The spillover factor. When the main virtual server reaches this spillover threshold, it will give further traffic to the backupvserver.<br>Possible values = CONNECTION, DYNAMICCONNECTION, BANDWIDTH, HEALTH, NONE</td></tr><tr><td>sopersistence</td><td>&lt;String></td><td>Read-only</td><td>The state of spillover persistence.<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>lbvserver</td><td>&lt;String></td><td>Read-only</td><td>The Default target server name.<br>Minimum length = 1</td></tr><tr><td>bindpoint</td><td>&lt;String></td><td>Read-only</td><td>The bindpoint to which the policy is bound.<br>Possible values = REQUEST, RESPONSE, ICA_REQUEST</td></tr><tr><td>invoke</td><td>&lt;Boolean></td><td>Read-only</td><td>Invoke flag.</td></tr><tr><td>labeltype</td><td>&lt;String></td><td>Read-only</td><td>The invocation type.<br>Possible values = reqvserver, resvserver, policylabel</td></tr><tr><td>labelname</td><td>&lt;String></td><td>Read-only</td><td>Name of the label invoked.</td></tr><tr><td>gotopriorityexpression</td><td>&lt;String></td><td>Read-only</td><td>Expression specifying the priority of the next policy which will get evaluated if the current policy rule evaluates to TRUE.</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD]()| [DELETE](#d)| [UPDATE](#u)| [UNSET](#)| [ENABLE](#e)| [DISABLE](#di)| [RENAME](#r)| [GET (ALL)](#get-)| [GET]()| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/crvserver
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"crvserver":{<b>"name":<String_value>,</b>"td":<Double_value>,<b>"servicetype":<String_value>,</b>"ipv46":<String_value>,"port":<Integer_value>,"range":<Double_value>,"cachetype":<String_value>,"redirect":<String_value>,"onpolicymatch":<String_value>,"redirecturl":<String_value>,"clttimeout":<Double_value>,"precedence":<String_value>,"arp":<String_value>,"ghost":<String_value>,"map":<String_value>,"format":<String_value>,"via":<String_value>,"cachevserver":<String_value>,"dnsvservername":<String_value>,"destinationvserver":<String_value>,"domain":<String_value>,"sopersistencetimeout":<Double_value>,"sothreshold":<Double_value>,"reuse":<String_value>,"state":<String_value>,"downstateflush":<String_value>,"backupvserver":<String_value>,"disableprimaryondown":<String_value>,"l2conn":<String_value>,"backendssl":<String_value>,"listenpolicy":<String_value>,"listenpriority":<Double_value>,"tcpprofilename":<String_value>,"httpprofilename":<String_value>,"comment":<String_value>,"srcipexpr":<String_value>,"originusip":<String_value>,"useportrange":<String_value>,"appflowlog":<String_value>,"netprofile":<String_value>,"icmpvsrresponse":<String_value>,"rhistate":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/crvserver/name_value&lt;String&gt;
<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/crvserver
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"crvserver":{<b>"name":<String_value>,</b>"ipv46":<String_value>,"redirect":<String_value>,"onpolicymatch":<String_value>,"precedence":<String_value>,"arp":<String_value>,"via":<String_value>,"cachevserver":<String_value>,"dnsvservername":<String_value>,"destinationvserver":<String_value>,"domain":<String_value>,"reuse":<String_value>,"backupvserver":<String_value>,"disableprimaryondown":<String_value>,"redirecturl":<String_value>,"clttimeout":<Double_value>,"downstateflush":<String_value>,"l2conn":<String_value>,"backendssl":<String_value>,"listenpolicy":<String_value>,"listenpriority":<Double_value>,"tcpprofilename":<String_value>,"httpprofilename":<String_value>,"netprofile":<String_value>,"comment":<String_value>,"srcipexpr":<String_value>,"originusip":<String_value>,"useportrange":<String_value>,"appflowlog":<String_value>,"icmpvsrresponse":<String_value>,"rhistate":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/crvserver?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"crvserver":{<b>"name":<String_value>,</b>"cachevserver":true,"dnsvservername":true,"destinationvserver":true,"domain":true,"backupvserver":true,"clttimeout":true,"redirecturl":true,"l2conn":true,"backendssl":true,"originusip":true,"useportrange":true,"srcipexpr":true,"tcpprofilename":true,"httpprofilename":true,"appflowlog":true,"netprofile":true,"icmpvsrresponse":true,"redirect":true,"onpolicymatch":true,"precedence":true,"arp":true,"via":true,"reuse":true,"disableprimaryondown":true,"downstateflush":true,"listenpolicy":true,"listenpriority":true,"comment":true,"rhistate":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###enable



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/crvserver?<b>action=enable</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"crvserver":{<b>"name":<String_value></b>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###disable



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/crvserver?<b>action=disable</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"crvserver":{<b>"name":<String_value></b>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###rename



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/crvserver?<b>action=rename</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"crvserver":{<b>"name":<String_value>,</b><b>"newname":<String_value></b>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/crvserver
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/crvserver?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/crvserver?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of crvserver resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/crvserver?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/crvserver?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the crvserver resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "crvserver": [ {"name":<String_value>,"ip":<String_value>,"td":<Double_value>,"ipv46":<String_value>,"value":<String_value>,"port":<Integer_value>,"range":<Double_value>,"servicetype":<String_value>,"ngname":<String_value>,"type":<String_value>,"curstate":<String_value>,"status":<Integer_value>,"sc":<String_value>,"cachetype":<String_value>,"redirect":<String_value>,"onpolicymatch":<String_value>,"precedence":<String_value>,"redirecturl":<String_value>,"authentication":<String_value>,"homepage":<String_value>,"dnsvservername":<String_value>,"domain":<String_value>,"rule":<String_value>,"policyname":<String_value>,"pipolicyhits":<Double_value>,"servicename":<String_value>,"weight":<Double_value>,"cachevserver":<String_value>,"targetvserver":<String_value>,"backupvserver":<String_value>,"priority":<Double_value>,"clttimeout":<Double_value>,"somethod":<String_value>,"sopersistence":<String_value>,"sopersistencetimeout":<Double_value>,"sothreshold":<Double_value>,"reuse":<String_value>,"arp":<String_value>,"destinationvserver":<String_value>,"via":<String_value>,"downstateflush":<String_value>,"disableprimaryondown":<String_value>,"l2conn":<String_value>,"backendssl":<String_value>,"comment":<String_value>,"listenpolicy":<String_value>,"listenpriority":<Double_value>,"tcpprofilename":<String_value>,"httpprofilename":<String_value>,"srcipexpr":<String_value>,"originusip":<String_value>,"useportrange":<String_value>,"appflowlog":<String_value>,"netprofile":<String_value>,"icmpvsrresponse":<String_value>,"rhistate":<String_value>,"lbvserver":<String_value>,"bindpoint":<String_value>,"invoke":<Boolean_value>,"labeltype":<String_value>,"labelname":<String_value>,"gotopriorityexpression":<String_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/crvserver/name_value&lt;String&gt;
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/crvserver/name_value&lt;String&gt;?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/crvserver/name_value&lt;String&gt;?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "crvserver": [ {"name":<String_value>,"ip":<String_value>,"td":<Double_value>,"ipv46":<String_value>,"value":<String_value>,"port":<Integer_value>,"range":<Double_value>,"servicetype":<String_value>,"ngname":<String_value>,"type":<String_value>,"curstate":<String_value>,"status":<Integer_value>,"sc":<String_value>,"cachetype":<String_value>,"redirect":<String_value>,"onpolicymatch":<String_value>,"precedence":<String_value>,"redirecturl":<String_value>,"authentication":<String_value>,"homepage":<String_value>,"dnsvservername":<String_value>,"domain":<String_value>,"rule":<String_value>,"policyname":<String_value>,"pipolicyhits":<Double_value>,"servicename":<String_value>,"weight":<Double_value>,"cachevserver":<String_value>,"targetvserver":<String_value>,"backupvserver":<String_value>,"priority":<Double_value>,"clttimeout":<Double_value>,"somethod":<String_value>,"sopersistence":<String_value>,"sopersistencetimeout":<Double_value>,"sothreshold":<Double_value>,"reuse":<String_value>,"arp":<String_value>,"destinationvserver":<String_value>,"via":<String_value>,"downstateflush":<String_value>,"disableprimaryondown":<String_value>,"l2conn":<String_value>,"backendssl":<String_value>,"comment":<String_value>,"listenpolicy":<String_value>,"listenpriority":<Double_value>,"tcpprofilename":<String_value>,"httpprofilename":<String_value>,"srcipexpr":<String_value>,"originusip":<String_value>,"useportrange":<String_value>,"appflowlog":<String_value>,"netprofile":<String_value>,"icmpvsrresponse":<String_value>,"rhistate":<String_value>,"lbvserver":<String_value>,"bindpoint":<String_value>,"invoke":<Boolean_value>,"labeltype":<String_value>,"labelname":<String_value>,"gotopriorityexpression":<String_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/crvserver?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "crvserver": [ { "__count": "#no"} ] }```



