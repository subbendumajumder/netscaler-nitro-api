#csvserver

Configuration for CS virtual server resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the content switching virtual server. Must begin with an ASCII alphanumeric or underscore (_) character, and must contain only ASCII alphanumeric, underscore, hash (#), period (.), space, colon (:), at sign (@), equal sign (=), and hyphen (-) characters. <br>Cannot be changed after the CS virtual server is created.<br>The following requirement applies only to the NetScaler CLI:<br>If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, my server or my server).<br>Minimum length = 1</td></tr><tr><td>td</td><td>&lt;Double></td><td>Read-write</td><td>Integer value that uniquely identifies the traffic domain in which you want to configure the entity. If you do not specify an ID, the entity becomes part of the default traffic domain, which has an ID of 0.<br>Minimum value = 0<br>Maximum value = 4094</td></tr><tr><td>servicetype</td><td>&lt;String></td><td>Read-write</td><td>Protocol used by the virtual server.<br>Possible values = HTTP, SSL, TCP, FTP, RTSP, SSL_TCP, UDP, DNS, SIP_UDP, SIP_TCP, SIP_SSL, ANY, RADIUS, RDP, MYSQL, MSSQL, DIAMETER, SSL_DIAMETER, DNS_TCP, ORACLE, SMPP, PROXY</td></tr><tr><td>ipv46</td><td>&lt;String></td><td>Read-write</td><td>IP address of the content switching virtual server.<br>Minimum length = 1</td></tr><tr><td>targettype</td><td>&lt;String></td><td>Read-write</td><td>Virtual server target type.<br>Possible values = GSLB</td></tr><tr><td>dnsrecordtype</td><td>&lt;String></td><td>Read-write</td><td>.<br>Default value: NSGSLB_IPV4<br>Possible values = A, AAAA, CNAME, NAPTR</td></tr><tr><td>persistenceid</td><td>&lt;Double></td><td>Read-write</td><td>.<br>Minimum value = 0<br>Maximum value = 65535</td></tr><tr><td>ippattern</td><td>&lt;String></td><td>Read-write</td><td>IP address pattern, in dotted decimal notation, for identifying packets to be accepted by the virtual server. The IP Mask parameter specifies which part of the destination IP address is matched against the pattern. Mutually exclusive with the IP Address parameter. <br>For example, if the IP pattern assigned to the virtual server is 198.51.100.0 and the IP mask is 255.255.240.0 (a forward mask), the first 20 bits in the destination IP addresses are matched with the first 20 bits in the pattern. The virtual server accepts requests with IP addresses that range from 198.51.96.1 to 198.51.111.254. You can also use a pattern such as 0.0.2.2 and a mask such as 0.0.255.255 (a reverse mask).<br>If a destination IP address matches more than one IP pattern, the pattern with the longest match is selected, and the associated virtual server processes the request. For example, if the virtual servers, vs1 and vs2, have the same IP pattern, 0.0.100.128, but different IP masks of 0.0.255.255 and 0.0.224.255, a destination IP address of 198.51.100.128 has the longest match with the IP pattern of vs1. If a destination IP address matches two or more virtual servers to the same extent, the request is processed by the virtual server whose port number matches the port number in the request.</td></tr><tr><td>ipmask</td><td>&lt;String></td><td>Read-write</td><td>IP mask, in dotted decimal notation, for the IP Pattern parameter. Can have leading or trailing non-zero octets (for example, 255.255.240.0 or 0.0.255.255). Accordingly, the mask specifies whether the first n bits or the last n bits of the destination IP address in a client request are to be matched with the corresponding bits in the IP pattern. The former is called a forward mask. The latter is called a reverse mask.</td></tr><tr><td>range</td><td>&lt;Double></td><td>Read-write</td><td>Number of consecutive IP addresses, starting with the address specified by the IP Address parameter, to include in a range of addresses assigned to this virtual server.<br>Default value: 1<br>Minimum value = 1<br>Maximum value = 254</td></tr><tr><td>port</td><td>&lt;Integer></td><td>Read-write</td><td>Port number for content switching virtual server.<br>Minimum value = 1<br>Range 1 - 65535<br>* in CLI is represented as 65535 in NITRO API</td></tr><tr><td>state</td><td>&lt;String></td><td>Read-write</td><td>Initial state of the load balancing virtual server.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>stateupdate</td><td>&lt;String></td><td>Read-write</td><td>Enable state updates for a specific content switching virtual server. By default, the Content Switching virtual server is always UP, regardless of the state of the Load Balancing virtual servers bound to it. This parameter interacts with the global setting as follows:<br>Global Level | Vserver Level | Result<br>ENABLED ENABLED ENABLED<br>ENABLED DISABLED ENABLED<br>DISABLED ENABLED ENABLED<br>DISABLED DISABLED DISABLED<br>If you want to enable state updates for only some content switching virtual servers, be sure to disable the state update parameter.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>cacheable</td><td>&lt;String></td><td>Read-write</td><td>Use this option to specify whether a virtual server, used for load balancing or content switching, routes requests to the cache redirection virtual server before sending it to the configured servers.<br>Default value: NO<br>Possible values = YES, NO</td></tr><tr><td>redirecturl</td><td>&lt;String></td><td>Read-write</td><td>URL to which traffic is redirected if the virtual server becomes unavailable. The service type of the virtual server should be either HTTP or SSL.<br>Caution: Make sure that the domain in the URL does not match the domain specified for a content switching policy. If it does, requests are continuously redirected to the unavailable virtual server.<br>Minimum length = 1</td></tr><tr><td>clttimeout</td><td>&lt;Double></td><td>Read-write</td><td>Idle time, in seconds, after which the client connection is terminated. The default values are:<br>180 seconds for HTTP/SSL-based services.<br>9000 seconds for other TCP-based services.<br>120 seconds for DNS-based services.<br>120 seconds for other UDP-based services.<br>Minimum value = 0<br>Maximum value = 31536000</td></tr><tr><td>precedence</td><td>&lt;String></td><td>Read-write</td><td>Type of precedence to use for both RULE-based and URL-based policies on the content switching virtual server. With the default (RULE) setting, incoming requests are evaluated against the rule-based content switching policies. If none of the rules match, the URL in the request is evaluated against the URL-based content switching policies.<br>Default value: RULE<br>Possible values = RULE, URL</td></tr><tr><td>casesensitive</td><td>&lt;String></td><td>Read-write</td><td>Consider case in URLs (for policies that use URLs instead of RULES). For example, with the ON setting, the URLs /a/1.html and /A/1.HTML are treated differently and can have different targets (set by content switching policies). With the OFF setting, /a/1.html and /A/1.HTML are switched to the same target.<br>Default value: ON<br>Possible values = ON, OFF</td></tr><tr><td>somethod</td><td>&lt;String></td><td>Read-write</td><td>Type of spillover used to divert traffic to the backup virtual server when the primary virtual server reaches the spillover threshold. Connection spillover is based on the number of connections. Bandwidth spillover is based on the total Kbps of incoming and outgoing traffic.<br>Possible values = CONNECTION, DYNAMICCONNECTION, BANDWIDTH, HEALTH, NONE</td></tr><tr><td>sopersistence</td><td>&lt;String></td><td>Read-write</td><td>Maintain source-IP based persistence on primary and backup virtual servers.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>sopersistencetimeout</td><td>&lt;Double></td><td>Read-write</td><td>Time-out value, in minutes, for spillover persistence.<br>Default value: 2<br>Minimum value = 2<br>Maximum value = 1440</td></tr><tr><td>sothreshold</td><td>&lt;Double></td><td>Read-write</td><td>Depending on the spillover method, the maximum number of connections or the maximum total bandwidth (Kbps) that a virtual server can handle before spillover occurs.<br>Minimum value = 1<br>Maximum value = 4294967287</td></tr><tr><td>sobackupaction</td><td>&lt;String></td><td>Read-write</td><td>Action to be performed if spillover is to take effect, but no backup chain to spillover is usable or exists.<br>Possible values = DROP, ACCEPT, REDIRECT</td></tr><tr><td>redirectportrewrite</td><td>&lt;String></td><td>Read-write</td><td>State of port rewrite while performing HTTP redirect.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>downstateflush</td><td>&lt;String></td><td>Read-write</td><td>Flush all active transactions associated with a virtual server whose state transitions from UP to DOWN. Do not enable this option for applications that must complete their transactions.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>backupvserver</td><td>&lt;String></td><td>Read-write</td><td>Name of the backup virtual server that you are configuring. Must begin with an ASCII alphanumeric or underscore (_) character, and must contain only ASCII alphanumeric, underscore, hash (#), period (.), space, colon (:), at sign (@), equal sign (=), and hyphen (-) characters. Can be changed after the backup virtual server is created. You can assign a different backup virtual server or rename the existing virtual server.<br>The following requirement applies only to the NetScaler CLI:<br>If the name includes one or more spaces, enclose the name in double or single quotation marks.<br>Minimum length = 1</td></tr><tr><td>disableprimaryondown</td><td>&lt;String></td><td>Read-write</td><td>Continue forwarding the traffic to backup virtual server even after the primary server comes UP from the DOWN state.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>insertvserveripport</td><td>&lt;String></td><td>Read-write</td><td>Insert the virtual server's VIP address and port number in the request header. Available values function as follows:<br>VIPADDR - Header contains the vserver's IP address and port number without any translation.<br>OFF - The virtual IP and port header insertion option is disabled.<br>V6TOV4MAPPING - Header contains the mapped IPv4 address corresponding to the IPv6 address of the vserver and the port number. An IPv6 address can be mapped to a user-specified IPv4 address using the set ns ip6 command.<br>Possible values = OFF, VIPADDR, V6TOV4MAPPING</td></tr><tr><td>vipheader</td><td>&lt;String></td><td>Read-write</td><td>Name of virtual server IP and port header, for use with the VServer IP Port Insertion parameter.<br>Minimum length = 1</td></tr><tr><td>rtspnat</td><td>&lt;String></td><td>Read-write</td><td>Enable network address translation (NAT) for real-time streaming protocol (RTSP) connections.<br>Default value: OFF<br>Possible values = ON, OFF</td></tr><tr><td>authenticationhost</td><td>&lt;String></td><td>Read-write</td><td>FQDN of the authentication virtual server. The service type of the virtual server should be either HTTP or SSL.<br>Minimum length = 3<br>Maximum length = 252</td></tr><tr><td>authentication</td><td>&lt;String></td><td>Read-write</td><td>Authenticate users who request a connection to the content switching virtual server.<br>Default value: OFF<br>Possible values = ON, OFF</td></tr><tr><td>listenpolicy</td><td>&lt;String></td><td>Read-write</td><td>String specifying the listen policy for the content switching virtual server. Can be either the name of an existing expression or an in-line expression.<br>Default value: "NONE"</td></tr><tr><td>listenpriority</td><td>&lt;Double></td><td>Read-write</td><td>Integer specifying the priority of the listen policy. A higher number specifies a lower priority. If a request matches the listen policies of more than one virtual server the virtual server whose listen policy has the highest priority (the lowest priority number) accepts the request.<br>Default value: 101<br>Minimum value = 0<br>Maximum value = 100</td></tr><tr><td>authn401</td><td>&lt;String></td><td>Read-write</td><td>Enable HTTP 401-response based authentication.<br>Default value: OFF<br>Possible values = ON, OFF</td></tr><tr><td>authnvsname</td><td>&lt;String></td><td>Read-write</td><td>Name of authentication virtual server that authenticates the incoming user requests to this content switching virtual server. .<br>Minimum length = 1<br>Maximum length = 252</td></tr><tr><td>push</td><td>&lt;String></td><td>Read-write</td><td>Process traffic with the push virtual server that is bound to this content switching virtual server (specified by the Push VServer parameter). The service type of the push virtual server should be either HTTP or SSL.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>pushvserver</td><td>&lt;String></td><td>Read-write</td><td>Name of the load balancing virtual server, of type PUSH or SSL_PUSH, to which the server pushes updates received on the client-facing load balancing virtual server.<br>Minimum length = 1</td></tr><tr><td>pushlabel</td><td>&lt;String></td><td>Read-write</td><td>Expression for extracting the label from the response received from server. This string can be either an existing rule name or an inline expression. The service type of the virtual server should be either HTTP or SSL.<br>Default value: "none"</td></tr><tr><td>pushmulticlients</td><td>&lt;String></td><td>Read-write</td><td>Allow multiple Web 2.0 connections from the same client to connect to the virtual server and expect updates.<br>Default value: NO<br>Possible values = YES, NO</td></tr><tr><td>tcpprofilename</td><td>&lt;String></td><td>Read-write</td><td>Name of the TCP profile containing TCP configuration settings for the virtual server.<br>Minimum length = 1<br>Maximum length = 127</td></tr><tr><td>httpprofilename</td><td>&lt;String></td><td>Read-write</td><td>Name of the HTTP profile containing HTTP configuration settings for the virtual server. The service type of the virtual server should be either HTTP or SSL.<br>Minimum length = 1<br>Maximum length = 127</td></tr><tr><td>dbprofilename</td><td>&lt;String></td><td>Read-write</td><td>Name of the DB profile.<br>Minimum length = 1<br>Maximum length = 127</td></tr><tr><td>oracleserverversion</td><td>&lt;String></td><td>Read-write</td><td>Oracle server version.<br>Default value: 10G<br>Possible values = 10G, 11G</td></tr><tr><td>comment</td><td>&lt;String></td><td>Read-write</td><td>Information about this virtual server.</td></tr><tr><td>mssqlserverversion</td><td>&lt;String></td><td>Read-write</td><td>The version of the MSSQL server.<br>Default value: 2008R2<br>Possible values = 70, 2000, 2000SP1, 2005, 2008, 2008R2, 2012, 2014</td></tr><tr><td>l2conn</td><td>&lt;String></td><td>Read-write</td><td>Use L2 Parameters to identify a connection.<br>Possible values = ON, OFF</td></tr><tr><td>mysqlprotocolversion</td><td>&lt;Double></td><td>Read-write</td><td>The protocol version returned by the mysql vserver.<br>Default value: 10</td></tr><tr><td>mysqlserverversion</td><td>&lt;String></td><td>Read-write</td><td>The server version string returned by the mysql vserver.<br>Minimum length = 1<br>Maximum length = 31</td></tr><tr><td>mysqlcharacterset</td><td>&lt;Double></td><td>Read-write</td><td>The character set returned by the mysql vserver.<br>Default value: 8</td></tr><tr><td>mysqlservercapabilities</td><td>&lt;Double></td><td>Read-write</td><td>The server capabilities returned by the mysql vserver.<br>Default value: 41613</td></tr><tr><td>appflowlog</td><td>&lt;String></td><td>Read-write</td><td>Enable logging appflow flow information.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>netprofile</td><td>&lt;String></td><td>Read-write</td><td>The name of the network profile.<br>Minimum length = 1<br>Maximum length = 127</td></tr><tr><td>icmpvsrresponse</td><td>&lt;String></td><td>Read-write</td><td>Can be active or passive.<br>Default value: PASSIVE<br>Possible values = PASSIVE, ACTIVE</td></tr><tr><td>rhistate</td><td>&lt;String></td><td>Read-write</td><td>A host route is injected according to the setting on the virtual servers<br>* If set to PASSIVE on all the virtual servers that share the IP address, the appliance always injects the hostroute.<br>* If set to ACTIVE on all the virtual servers that share the IP address, the appliance injects even if one virtual server is UP.<br>* If set to ACTIVE on some virtual servers and PASSIVE on the others, the appliance, injects even if one virtual server set to ACTIVE is UP.<br>Default value: PASSIVE<br>Possible values = PASSIVE, ACTIVE</td></tr><tr><td>authnprofile</td><td>&lt;String></td><td>Read-write</td><td>Name of the authentication profile to be used when authentication is turned on.</td></tr><tr><td>dnsprofilename</td><td>&lt;String></td><td>Read-write</td><td>Name of the DNS profile to be associated with the VServer. DNS profile properties will applied to the transactions processed by a VServer. This parameter is valid only for DNS and DNS-TCP VServers.<br>Minimum length = 1<br>Maximum length = 127</td></tr><tr><td>domainname</td><td>&lt;String></td><td>Read-write</td><td>Domain name for which to change the time to live (TTL) and/or backup service IP address.<br>Minimum length = 1</td></tr><tr><td>ttl</td><td>&lt;Double></td><td>Read-write</td><td>.<br>Minimum value = 1</td></tr><tr><td>backupip</td><td>&lt;String></td><td>Read-write</td><td>.<br>Minimum length = 1</td></tr><tr><td>cookiedomain</td><td>&lt;String></td><td>Read-write</td><td>.<br>Minimum length = 1</td></tr><tr><td>cookietimeout</td><td>&lt;Double></td><td>Read-write</td><td>.<br>Minimum value = 0<br>Maximum value = 1440</td></tr><tr><td>sitedomainttl</td><td>&lt;Double></td><td>Read-write</td><td>.<br>Minimum value = 1</td></tr><tr><td>newname</td><td>&lt;String></td><td>Read-write</td><td>New name for the virtual server. Must begin with an ASCII alphanumeric or underscore (_) character, and must contain only ASCII alphanumeric, underscore, hash (#), period (.), space, colon (:), at sign (@), equal sign (=), and hyphen (-) characters. <br>The following requirement applies only to the NetScaler CLI:<br>If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my name" or 'my name').<br>Minimum length = 1</td></tr><tr><td>ip</td><td>&lt;String></td><td>Read-only</td><td>The IP address of the virtual server.</td></tr><tr><td>value</td><td>&lt;String></td><td>Read-only</td><td>The ssl card status for the transparent ssl cs vserver.<br>Possible values = Certkey not bound, SSL feature disabled</td></tr><tr><td>ngname</td><td>&lt;String></td><td>Read-only</td><td>Nodegroup devno to which this csvserver belongs to.</td></tr><tr><td>type</td><td>&lt;String></td><td>Read-only</td><td>Virtual server type.<br>Possible values = CONTENT, ADDRESS</td></tr><tr><td>curstate</td><td>&lt;String></td><td>Read-only</td><td>The state of the cs vserver.<br>Possible values = UP, DOWN, UNKNOWN, BUSY, OUT OF SERVICE, GOING OUT OF SERVICE, DOWN WHEN GOING OUT OF SERVICE, NS_EMPTY_STR, Unknown, DISABLED</td></tr><tr><td>sc</td><td>&lt;String></td><td>Read-only</td><td>The state of SureConnect the specified virtual server.<br>Possible values = ON, OFF</td></tr><tr><td>status</td><td>&lt;Integer></td><td>Read-only</td><td>Status.</td></tr><tr><td>cachetype</td><td>&lt;String></td><td>Read-only</td><td>Cache type.<br>Possible values = TRANSPARENT, REVERSE, FORWARD</td></tr><tr><td>redirect</td><td>&lt;String></td><td>Read-only</td><td>Redirect URL string.<br>Possible values = CACHE, POLICY, ORIGIN</td></tr><tr><td>homepage</td><td>&lt;String></td><td>Read-only</td><td>Home page.</td></tr><tr><td>dnsvservername</td><td>&lt;String></td><td>Read-only</td><td>DNS vserver name.</td></tr><tr><td>domain</td><td>&lt;String></td><td>Read-only</td><td>Domain.</td></tr><tr><td>policyname</td><td>&lt;String></td><td>Read-only</td><td>Policies bound to this vserver.</td></tr><tr><td>servicename</td><td>&lt;String></td><td>Read-only</td><td>Service name.</td></tr><tr><td>weight</td><td>&lt;Double></td><td>Read-only</td><td>Weight for this service.</td></tr><tr><td>cachevserver</td><td>&lt;String></td><td>Read-only</td><td>Cache vserver name.</td></tr><tr><td>targetvserver</td><td>&lt;String></td><td>Read-only</td><td>target vserver name.</td></tr><tr><td>priority</td><td>&lt;Double></td><td>Read-only</td><td>Priority for the policy.</td></tr><tr><td>url</td><td>&lt;String></td><td>Read-only</td><td>URL string.</td></tr><tr><td>gotopriorityexpression</td><td>&lt;String></td><td>Read-only</td><td>Expression specifying the priority of the next policy which will get evaluated if the current policy rule evaluates to TRUE.</td></tr><tr><td>bindpoint</td><td>&lt;String></td><td>Read-only</td><td>The bindpoint to which the policy is bound.<br>Possible values = REQUEST, RESPONSE</td></tr><tr><td>invoke</td><td>&lt;Boolean></td><td>Read-only</td><td>Invoke flag.</td></tr><tr><td>labeltype</td><td>&lt;String></td><td>Read-only</td><td>The invocation type.<br>Possible values = reqvserver, resvserver, policylabel</td></tr><tr><td>labelname</td><td>&lt;String></td><td>Read-only</td><td>Name of the label invoked.</td></tr><tr><td>gt2gb</td><td>&lt;String></td><td>Read-only</td><td>This argument has no effect.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>statechangetimesec</td><td>&lt;String></td><td>Read-only</td><td>Time when last state change happened. Seconds part.</td></tr><tr><td>statechangetimemsec</td><td>&lt;Double></td><td>Read-only</td><td>Time at which last state change happened. Milliseconds part.</td></tr><tr><td>tickssincelaststatechange</td><td>&lt;Double></td><td>Read-only</td><td>Time in 10 millisecond ticks since the last state change.</td></tr><tr><td>ruletype</td><td>&lt;Double></td><td>Read-only</td><td>Rule type.</td></tr><tr><td>lbvserver</td><td>&lt;String></td><td>Read-only</td><td>Name of the default lb vserver bound. Use this param for Default binding only. For Example: bind cs vserver cs1 -lbvserver lb1.<br>Minimum length = 1</td></tr><tr><td>targetlbvserver</td><td>&lt;String></td><td>Read-only</td><td>target vserver name.</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD]()| [DELETE](#d)| [UPDATE](#u)| [UNSET](#)| [ENABLE](#e)| [DISABLE](#di)| [RENAME](#r)| [GET (ALL)](#get-)| [GET]()| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/csvserver
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"csvserver":{<b>"name":<String_value>,</b>"td":<Double_value>,<b>"servicetype":<String_value>,</b>"ipv46":<String_value>,"targettype":<String_value>,"dnsrecordtype":<String_value>,"persistenceid":<Double_value>,"ippattern":<String_value>,"ipmask":<String_value>,"range":<Double_value>,"port":<Integer_value>,"state":<String_value>,"stateupdate":<String_value>,"cacheable":<String_value>,"redirecturl":<String_value>,"clttimeout":<Double_value>,"precedence":<String_value>,"casesensitive":<String_value>,"somethod":<String_value>,"sopersistence":<String_value>,"sopersistencetimeout":<Double_value>,"sothreshold":<Double_value>,"sobackupaction":<String_value>,"redirectportrewrite":<String_value>,"downstateflush":<String_value>,"backupvserver":<String_value>,"disableprimaryondown":<String_value>,"insertvserveripport":<String_value>,"vipheader":<String_value>,"rtspnat":<String_value>,"authenticationhost":<String_value>,"authentication":<String_value>,"listenpolicy":<String_value>,"listenpriority":<Double_value>,"authn401":<String_value>,"authnvsname":<String_value>,"push":<String_value>,"pushvserver":<String_value>,"pushlabel":<String_value>,"pushmulticlients":<String_value>,"tcpprofilename":<String_value>,"httpprofilename":<String_value>,"dbprofilename":<String_value>,"oracleserverversion":<String_value>,"comment":<String_value>,"mssqlserverversion":<String_value>,"l2conn":<String_value>,"mysqlprotocolversion":<Double_value>,"mysqlserverversion":<String_value>,"mysqlcharacterset":<Double_value>,"mysqlservercapabilities":<Double_value>,"appflowlog":<String_value>,"netprofile":<String_value>,"icmpvsrresponse":<String_value>,"rhistate":<String_value>,"authnprofile":<String_value>,"dnsprofilename":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/csvserver/name_value&lt;String&gt;
<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/csvserver
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"csvserver":{<b>"name":<String_value>,</b>"ipv46":<String_value>,"ippattern":<String_value>,"ipmask":<String_value>,"stateupdate":<String_value>,"precedence":<String_value>,"casesensitive":<String_value>,"backupvserver":<String_value>,"redirecturl":<String_value>,"cacheable":<String_value>,"clttimeout":<Double_value>,"somethod":<String_value>,"sopersistence":<String_value>,"sopersistencetimeout":<Double_value>,"sothreshold":<Double_value>,"sobackupaction":<String_value>,"redirectportrewrite":<String_value>,"downstateflush":<String_value>,"disableprimaryondown":<String_value>,"insertvserveripport":<String_value>,"vipheader":<String_value>,"rtspnat":<String_value>,"authenticationhost":<String_value>,"authentication":<String_value>,"listenpolicy":<String_value>,"listenpriority":<Double_value>,"authn401":<String_value>,"authnvsname":<String_value>,"push":<String_value>,"pushvserver":<String_value>,"pushlabel":<String_value>,"pushmulticlients":<String_value>,"tcpprofilename":<String_value>,"httpprofilename":<String_value>,"dbprofilename":<String_value>,"comment":<String_value>,"l2conn":<String_value>,"mssqlserverversion":<String_value>,"mysqlprotocolversion":<Double_value>,"oracleserverversion":<String_value>,"mysqlserverversion":<String_value>,"mysqlcharacterset":<Double_value>,"mysqlservercapabilities":<Double_value>,"appflowlog":<String_value>,"netprofile":<String_value>,"authnprofile":<String_value>,"icmpvsrresponse":<String_value>,"rhistate":<String_value>,"dnsprofilename":<String_value>,"dnsrecordtype":<String_value>,"persistenceid":<Double_value>,"domainname":<String_value>,"ttl":<Double_value>,"backupip":<String_value>,"cookiedomain":<String_value>,"cookietimeout":<Double_value>,"sitedomainttl":<Double_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/csvserver?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"csvserver":{<b>"name":<String_value>,</b>"casesensitive":true,"backupvserver":true,"clttimeout":true,"redirecturl":true,"authn401":true,"authentication":true,"authenticationhost":true,"authnvsname":true,"pushvserver":true,"pushlabel":true,"tcpprofilename":true,"httpprofilename":true,"dbprofilename":true,"l2conn":true,"mysqlprotocolversion":true,"mysqlserverversion":true,"mysqlcharacterset":true,"mysqlservercapabilities":true,"appflowlog":true,"netprofile":true,"icmpvsrresponse":true,"authnprofile":true,"sothreshold":true,"dnsprofilename":true,"stateupdate":true,"precedence":true,"cacheable":true,"somethod":true,"sopersistence":true,"sopersistencetimeout":true,"sobackupaction":true,"redirectportrewrite":true,"downstateflush":true,"disableprimaryondown":true,"insertvserveripport":true,"vipheader":true,"rtspnat":true,"listenpolicy":true,"listenpriority":true,"push":true,"pushmulticlients":true,"comment":true,"mssqlserverversion":true,"oracleserverversion":true,"rhistate":true,"dnsrecordtype":true,"persistenceid":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###enable



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/csvserver?<b>action=enable</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"csvserver":{<b>"name":<String_value></b>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###disable



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/csvserver?<b>action=disable</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"csvserver":{<b>"name":<String_value></b>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###rename



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/csvserver?<b>action=rename</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"csvserver":{<b>"name":<String_value>,</b><b>"newname":<String_value></b>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/csvserver
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/csvserver?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/csvserver?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of csvserver resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/csvserver?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/csvserver?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the csvserver resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "csvserver": [ {"name":<String_value>,"insertvserveripport":<String_value>,"vipheader":<String_value>,"ip":<String_value>,"td":<Double_value>,"ipv46":<String_value>,"ippattern":<String_value>,"ipmask":<String_value>,"value":<String_value>,"port":<Integer_value>,"range":<Double_value>,"servicetype":<String_value>,"ngname":<String_value>,"type":<String_value>,"curstate":<String_value>,"sc":<String_value>,"stateupdate":<String_value>,"status":<Integer_value>,"cachetype":<String_value>,"redirect":<String_value>,"precedence":<String_value>,"redirecturl":<String_value>,"authentication":<String_value>,"authn401":<String_value>,"authnvsname":<String_value>,"casesensitive":<String_value>,"homepage":<String_value>,"dnsvservername":<String_value>,"domain":<String_value>,"policyname":<String_value>,"servicename":<String_value>,"weight":<Double_value>,"cachevserver":<String_value>,"targetvserver":<String_value>,"backupvserver":<String_value>,"priority":<Double_value>,"clttimeout":<Double_value>,"listenpolicy":<String_value>,"listenpriority":<Double_value>,"somethod":<String_value>,"sopersistence":<String_value>,"sopersistencetimeout":<Double_value>,"sothreshold":<Double_value>,"sobackupaction":<String_value>,"cacheable":<String_value>,"url":<String_value>,"gotopriorityexpression":<String_value>,"redirectportrewrite":<String_value>,"downstateflush":<String_value>,"disableprimaryondown":<String_value>,"bindpoint":<String_value>,"invoke":<Boolean_value>,"labeltype":<String_value>,"labelname":<String_value>,"gt2gb":<String_value>,"statechangetimesec":<String_value>,"statechangetimemsec":<Double_value>,"tickssincelaststatechange":<Double_value>,"rtspnat":<String_value>,"authenticationhost":<String_value>,"push":<String_value>,"pushvserver":<String_value>,"pushlabel":<String_value>,"pushmulticlients":<String_value>,"tcpprofilename":<String_value>,"httpprofilename":<String_value>,"dbprofilename":<String_value>,"comment":<String_value>,"oracleserverversion":<String_value>,"mssqlserverversion":<String_value>,"l2conn":<String_value>,"ruletype":<Double_value>,"mysqlprotocolversion":<Double_value>,"mysqlserverversion":<String_value>,"mysqlcharacterset":<Double_value>,"mysqlservercapabilities":<Double_value>,"appflowlog":<String_value>,"netprofile":<String_value>,"icmpvsrresponse":<String_value>,"rhistate":<String_value>,"lbvserver":<String_value>,"targetlbvserver":<String_value>,"authnprofile":<String_value>,"dnsprofilename":<String_value>,"targettype":<String_value>,"domainname":<String_value>,"ttl":<Double_value>,"backupip":<String_value>,"cookiedomain":<String_value>,"cookietimeout":<Double_value>,"sitedomainttl":<Double_value>,"dnsrecordtype":<String_value>,"persistenceid":<Double_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/csvserver/name_value&lt;String&gt;
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/csvserver/name_value&lt;String&gt;?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/csvserver/name_value&lt;String&gt;?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "csvserver": [ {"name":<String_value>,"insertvserveripport":<String_value>,"vipheader":<String_value>,"ip":<String_value>,"td":<Double_value>,"ipv46":<String_value>,"ippattern":<String_value>,"ipmask":<String_value>,"value":<String_value>,"port":<Integer_value>,"range":<Double_value>,"servicetype":<String_value>,"ngname":<String_value>,"type":<String_value>,"curstate":<String_value>,"sc":<String_value>,"stateupdate":<String_value>,"status":<Integer_value>,"cachetype":<String_value>,"redirect":<String_value>,"precedence":<String_value>,"redirecturl":<String_value>,"authentication":<String_value>,"authn401":<String_value>,"authnvsname":<String_value>,"casesensitive":<String_value>,"homepage":<String_value>,"dnsvservername":<String_value>,"domain":<String_value>,"policyname":<String_value>,"servicename":<String_value>,"weight":<Double_value>,"cachevserver":<String_value>,"targetvserver":<String_value>,"backupvserver":<String_value>,"priority":<Double_value>,"clttimeout":<Double_value>,"listenpolicy":<String_value>,"listenpriority":<Double_value>,"somethod":<String_value>,"sopersistence":<String_value>,"sopersistencetimeout":<Double_value>,"sothreshold":<Double_value>,"sobackupaction":<String_value>,"cacheable":<String_value>,"url":<String_value>,"gotopriorityexpression":<String_value>,"redirectportrewrite":<String_value>,"downstateflush":<String_value>,"disableprimaryondown":<String_value>,"bindpoint":<String_value>,"invoke":<Boolean_value>,"labeltype":<String_value>,"labelname":<String_value>,"gt2gb":<String_value>,"statechangetimesec":<String_value>,"statechangetimemsec":<Double_value>,"tickssincelaststatechange":<Double_value>,"rtspnat":<String_value>,"authenticationhost":<String_value>,"push":<String_value>,"pushvserver":<String_value>,"pushlabel":<String_value>,"pushmulticlients":<String_value>,"tcpprofilename":<String_value>,"httpprofilename":<String_value>,"dbprofilename":<String_value>,"comment":<String_value>,"oracleserverversion":<String_value>,"mssqlserverversion":<String_value>,"l2conn":<String_value>,"ruletype":<Double_value>,"mysqlprotocolversion":<Double_value>,"mysqlserverversion":<String_value>,"mysqlcharacterset":<Double_value>,"mysqlservercapabilities":<Double_value>,"appflowlog":<String_value>,"netprofile":<String_value>,"icmpvsrresponse":<String_value>,"rhistate":<String_value>,"lbvserver":<String_value>,"targetlbvserver":<String_value>,"authnprofile":<String_value>,"dnsprofilename":<String_value>,"targettype":<String_value>,"domainname":<String_value>,"ttl":<Double_value>,"backupip":<String_value>,"cookiedomain":<String_value>,"cookietimeout":<Double_value>,"sitedomainttl":<Double_value>,"dnsrecordtype":<String_value>,"persistenceid":<Double_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/csvserver?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "csvserver": [ { "__count": "#no"} ] }```



