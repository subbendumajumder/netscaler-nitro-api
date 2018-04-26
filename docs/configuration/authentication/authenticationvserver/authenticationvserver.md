#authenticationvserver

Configuration for authentication virtual server resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the new authentication virtual server. <br>Must begin with a letter, number, or the underscore character (_), and must contain only letters, numbers, and the hyphen (-), period (.) pound (#), space ( ), at (@), equals (=), colon (:), and underscore characters. Can be changed after the authentication virtual server is added by using the rename authentication vserver command.<br><br>The following requirement applies only to the NetScaler CLI:<br>If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my authentication policy" or 'my authentication policy').<br>Minimum length = 1</td></tr><tr><td>servicetype</td><td>&lt;String></td><td>Read-write</td><td>Protocol type of the authentication virtual server. Always SSL.<br>Default value: SSL<br>Possible values = SSL</td></tr><tr><td>ipv46</td><td>&lt;String></td><td>Read-write</td><td>IP address of the authentication virtual server, if a single IP address is assigned to the virtual server.<br>Minimum length = 1</td></tr><tr><td>range</td><td>&lt;Double></td><td>Read-write</td><td>If you are creating a series of virtual servers with a range of IP addresses assigned to them, the length of the range. <br>The new range of authentication virtual servers will have IP addresses consecutively numbered, starting with the primary address specified with the IP Address parameter.<br>Default value: 1<br>Minimum value = 1</td></tr><tr><td>port</td><td>&lt;Integer></td><td>Read-write</td><td>TCP port on which the virtual server accepts connections.<br>Range 1 - 65535<br>* in CLI is represented as 65535 in NITRO API</td></tr><tr><td>state</td><td>&lt;String></td><td>Read-write</td><td>Initial state of the new virtual server.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>authentication</td><td>&lt;String></td><td>Read-write</td><td>Require users to be authenticated before sending traffic through this virtual server.<br>Default value: ON<br>Possible values = ON, OFF</td></tr><tr><td>authenticationdomain</td><td>&lt;String></td><td>Read-write</td><td>The domain of the authentication cookie set by Authentication vserver.<br>Minimum length = 3<br>Maximum length = 252</td></tr><tr><td>comment</td><td>&lt;String></td><td>Read-write</td><td>Any comments associated with this virtual server.</td></tr><tr><td>td</td><td>&lt;Double></td><td>Read-write</td><td>Integer value that uniquely identifies the traffic domain in which you want to configure the entity. If you do not specify an ID, the entity becomes part of the default traffic domain, which has an ID of 0.<br>Minimum value = 0<br>Maximum value = 4094</td></tr><tr><td>appflowlog</td><td>&lt;String></td><td>Read-write</td><td>Log AppFlow flow information.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>maxloginattempts</td><td>&lt;Double></td><td>Read-write</td><td>Maximum Number of login Attempts.<br>Minimum value = 1<br>Maximum value = 255</td></tr><tr><td>failedlogintimeout</td><td>&lt;Double></td><td>Read-write</td><td>Number of minutes an account will be locked if user exceeds maximum permissible attempts.<br>Minimum value = 1</td></tr><tr><td>newname</td><td>&lt;String></td><td>Read-write</td><td>New name of the authentication virtual server. <br>Must begin with a letter, number, or the underscore character (_), and must contain only letters, numbers, and the hyphen (-), period (.) pound (#), space ( ), at (@), equals (=), colon (:), and underscore characters.<br><br>The following requirement applies only to the NetScaler CLI:<br>If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, 'my authentication policy' or "my authentication policy").<br>Minimum length = 1</td></tr><tr><td>ip</td><td>&lt;String></td><td>Read-only</td><td>The Virtual IP address of the authentication vserver.</td></tr><tr><td>value</td><td>&lt;String></td><td>Read-only</td><td>Indicates whether or not the certificate is bound or if SSL offload is disabled.<br>Possible values = Certkey not bound, SSL feature disabled</td></tr><tr><td>type</td><td>&lt;String></td><td>Read-only</td><td>The type of Virtual Server, e.g. CONTENT based or ADDRESS based.<br>Possible values = CONTENT, ADDRESS</td></tr><tr><td>curstate</td><td>&lt;String></td><td>Read-only</td><td>The current state of the Virtual server, e.g. UP, DOWN, BUSY, etc.<br>Possible values = UP, DOWN, UNKNOWN, BUSY, OUT OF SERVICE, GOING OUT OF SERVICE, DOWN WHEN GOING OUT OF SERVICE, NS_EMPTY_STR, Unknown, DISABLED</td></tr><tr><td>status</td><td>&lt;Integer></td><td>Read-only</td><td>Whether or not this vserver responds to ARPs and whether or not round-robin selection is temporarily in effect.</td></tr><tr><td>cachetype</td><td>&lt;String></td><td>Read-only</td><td>Virtual server's cache type. The options are: TRANSPARENT, REVERSE and FORWARD.<br>Possible values = TRANSPARENT, REVERSE, FORWARD</td></tr><tr><td>redirect</td><td>&lt;String></td><td>Read-only</td><td>The cache redirect policy.<br>The valid redirect policies are:<br>l. CACHE - Directs all requests to the cache.<br>2. POLICY - Applies cache redirection policy to determine whether the request should be directed to the cache or origin. This is the default setting.<br>3. ORIGIN - Directs all requests to the origin server.<br>Possible values = CACHE, POLICY, ORIGIN</td></tr><tr><td>precedence</td><td>&lt;String></td><td>Read-only</td><td>This argument is used only when configuring content switching on the specified virtual server. This is applicable only<br>if both the URL and RULE-based policies have been configured on the same virtual server.<br>It specifies the type of policy (URL or RULE) that takes precedence on the content switching virtual server. The default setting is RULE.<br>l URL - In this case, the incoming request is matched against the URL-based policies before the rule-based policies.<br>l RULE - In this case, the incoming request is matched against the rule-based policies before the URL-based policies.<br>For all URL-based policies, the precedence hierarchy is:<br>1. Domain and exact URL<br>2. Domain, prefix and suffix<br>3. Domain and suffix<br>4. Domain and prefix<br>5. Domain only<br>6. Exact URL<br>7. Prefix and suffix<br>8. Suffix only<br>9. Prefix only<br>10. Default.<br>Possible values = RULE, URL</td></tr><tr><td>redirecturl</td><td>&lt;String></td><td>Read-only</td><td>The URL where traffic is redirected if the virtual server in system becomes unavailable. WARNING! Make sure that the domain you specify in the URL does not match the domain specified in the -d domainName argument of the ###add cs policy### command. If the same domain is specified in both arguments, the request will be continuously redirected to the same unavailable virtual server in the system. If so, the user may not get the requested content.</td></tr><tr><td>curaaausers</td><td>&lt;Double></td><td>Read-only</td><td>The number of current users logged in to this vserver.</td></tr><tr><td>policy</td><td>&lt;String></td><td>Read-only</td><td>The name of the policy, if any, bound to the authentication vserver.</td></tr><tr><td>servicename</td><td>&lt;String></td><td>Read-only</td><td>The name of the service, if any, to which the vserver policy is bound.</td></tr><tr><td>weight</td><td>&lt;Double></td><td>Read-only</td><td>Weight for this service, if any. This weight is used when the system performs load balancing, giving greater priority to a specific service. It is useful when the services bound to a virtual server are of different capacity.</td></tr><tr><td>cachevserver</td><td>&lt;String></td><td>Read-only</td><td>The name of the default target cache virtual server, if any, to which requests are redirected.</td></tr><tr><td>backupvserver</td><td>&lt;String></td><td>Read-only</td><td>The name of the backup vpn virtual server for this vpn virtual server.</td></tr><tr><td>clttimeout</td><td>&lt;Double></td><td>Read-only</td><td>The idle time, if any, in seconds after which the client connection is terminated.</td></tr><tr><td>somethod</td><td>&lt;String></td><td>Read-only</td><td>VPN client applications are allocated from a block of Intranet IP addresses.<br>That block may be exhausted after a certain number of connections. This switch specifies the<br>method used to determine whether or not a new connection will spillover, or exhaust, the allocated block of<br>Intranet IP addresses for that application. Possible values are CONNECTION or DYNAMICCONNECTION.<br>CONNECTION means that a static integer value is the hard limit for the spillover threshold. The spillover<br>threshold is described below. DYNAMICCONNECTION means that the spillover threshold is set according to<br>the maximum number of connections defined for the vpn vserver.<br>Possible values = CONNECTION, DYNAMICCONNECTION, BANDWIDTH, HEALTH, NONE</td></tr><tr><td>sothreshold</td><td>&lt;Double></td><td>Read-only</td><td>VPN client applications are allocated from a block of Intranet IP addresses.<br>That block may be exhausted after a certain number of connections.<br>The value of this option is number of client connections after which the Mapped IP address is used<br>as the client source IP address instead of an address from the allocated block of Intranet IP addresses.</td></tr><tr><td>sopersistence</td><td>&lt;String></td><td>Read-only</td><td>Whether or not cookie-based site persistance is enabled for this VPN vserver. Possible values are 'ConnectionProxy', HTTPRedirect, or NONE.<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>sopersistencetimeout</td><td>&lt;Double></td><td>Read-only</td><td>The timeout, if any, for cookie-based site persistance of this VPN vserver.</td></tr><tr><td>priority</td><td>&lt;Double></td><td>Read-only</td><td>The priority, if any, of the vpn vserver policy.</td></tr><tr><td>downstateflush</td><td>&lt;String></td><td>Read-only</td><td>Perform delayed clean up of connections on this vserver.<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>disableprimaryondown</td><td>&lt;String></td><td>Read-only</td><td>Tells whether traffic will continue reaching backup vservers even after primary comes UP from DOWN state.<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>listenpolicy</td><td>&lt;String></td><td>Read-only</td><td>Listenpolicy configured for authentication vserver.</td></tr><tr><td>listenpriority</td><td>&lt;Double></td><td>Read-only</td><td>Priority of listen policy for authentication vserver.</td></tr><tr><td>tcpprofilename</td><td>&lt;String></td><td>Read-only</td><td>The name of the TCP profile.</td></tr><tr><td>httpprofilename</td><td>&lt;String></td><td>Read-only</td><td>Name of the HTTP profile.</td></tr><tr><td>vstype</td><td>&lt;Double></td><td>Read-only</td><td>Virtual Server Type, e.g. Load Balancing, Content Switch, Cache Redirection.</td></tr><tr><td>ngname</td><td>&lt;String></td><td>Read-only</td><td>Nodegroup devno to which this authentication vsever belongs to.</td></tr><tr><td>secondary</td><td>&lt;Boolean></td><td>Read-only</td><td>Bind the authentication policy to the secondary chain.<br>Provides for multifactor authentication in which a user must authenticate via both a primary authentication method and, afterward, via a secondary authentication method.<br>Because user groups are aggregated across authentication systems, usernames must be the same on all authentication servers. Passwords can be different.</td></tr><tr><td>groupextraction</td><td>&lt;Boolean></td><td>Read-only</td><td>Bind the Authentication policy to a tertiary chain which will be used only for group extraction. The user will not authenticate against this server, and this will only be called if primary and/or secondary authentication has succeeded.</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD]()| [DELETE](#d)| [UPDATE](#u)| [UNSET](#)| [ENABLE](#e)| [DISABLE](#di)| [RENAME](#r)| [GET (ALL)](#get-)| [GET]()| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationvserver
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"authenticationvserver":{<b>"name":<String_value>,</b><b>"servicetype":<String_value>,</b>"ipv46":<String_value>,"range":<Double_value>,"port":<Integer_value>,"state":<String_value>,"authentication":<String_value>,"authenticationdomain":<String_value>,"comment":<String_value>,"td":<Double_value>,"appflowlog":<String_value>,"maxloginattempts":<Double_value>,"failedlogintimeout":<Double_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationvserver/name_value&lt;String&gt;
<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationvserver
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"authenticationvserver":{<b>"name":<String_value>,</b>"ipv46":<String_value>,"authentication":<String_value>,"authenticationdomain":<String_value>,"comment":<String_value>,"appflowlog":<String_value>,"maxloginattempts":<Double_value>,"failedlogintimeout":<Double_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationvserver?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"authenticationvserver":{<b>"name":<String_value>,</b>"authenticationdomain":true,"maxloginattempts":true,"authentication":true,"comment":true,"appflowlog":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###enable



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationvserver?<b>action=enable</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"authenticationvserver":{<b>"name":<String_value></b>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###disable



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationvserver?<b>action=disable</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"authenticationvserver":{<b>"name":<String_value></b>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###rename



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationvserver?<b>action=rename</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"authenticationvserver":{<b>"name":<String_value>,</b><b>"newname":<String_value></b>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationvserver
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationvserver?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationvserver?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of authenticationvserver resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationvserver?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationvserver?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the authenticationvserver resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "authenticationvserver": [ {"name":<String_value>,"ip":<String_value>,"td":<Double_value>,"ipv46":<String_value>,"value":<String_value>,"port":<Integer_value>,"range":<Double_value>,"servicetype":<String_value>,"type":<String_value>,"curstate":<String_value>,"status":<Integer_value>,"cachetype":<String_value>,"redirect":<String_value>,"precedence":<String_value>,"redirecturl":<String_value>,"authentication":<String_value>,"curaaausers":<Double_value>,"authenticationdomain":<String_value>,"policyname":<String_value>,"policy":<String_value>,"servicename":<String_value>,"weight":<Double_value>,"cachevserver":<String_value>,"backupvserver":<String_value>,"clttimeout":<Double_value>,"somethod":<String_value>,"sothreshold":<Double_value>,"sopersistence":<String_value>,"sopersistencetimeout":<Double_value>,"priority":<Double_value>,"downstateflush":<String_value>,"disableprimaryondown":<String_value>,"listenpolicy":<String_value>,"listenpriority":<Double_value>,"tcpprofilename":<String_value>,"httpprofilename":<String_value>,"comment":<String_value>,"appflowlog":<String_value>,"vstype":<Double_value>,"ngname":<String_value>,"maxloginattempts":<Double_value>,"failedlogintimeout":<Double_value>,"secondary":<Boolean_value>,"groupextraction":<Boolean_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationvserver/name_value&lt;String&gt;
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationvserver/name_value&lt;String&gt;?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationvserver/name_value&lt;String&gt;?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "authenticationvserver": [ {"name":<String_value>,"ip":<String_value>,"td":<Double_value>,"ipv46":<String_value>,"value":<String_value>,"port":<Integer_value>,"range":<Double_value>,"servicetype":<String_value>,"type":<String_value>,"curstate":<String_value>,"status":<Integer_value>,"cachetype":<String_value>,"redirect":<String_value>,"precedence":<String_value>,"redirecturl":<String_value>,"authentication":<String_value>,"curaaausers":<Double_value>,"authenticationdomain":<String_value>,"policyname":<String_value>,"policy":<String_value>,"servicename":<String_value>,"weight":<Double_value>,"cachevserver":<String_value>,"backupvserver":<String_value>,"clttimeout":<Double_value>,"somethod":<String_value>,"sothreshold":<Double_value>,"sopersistence":<String_value>,"sopersistencetimeout":<Double_value>,"priority":<Double_value>,"downstateflush":<String_value>,"disableprimaryondown":<String_value>,"listenpolicy":<String_value>,"listenpriority":<Double_value>,"tcpprofilename":<String_value>,"httpprofilename":<String_value>,"comment":<String_value>,"appflowlog":<String_value>,"vstype":<Double_value>,"ngname":<String_value>,"maxloginattempts":<Double_value>,"failedlogintimeout":<Double_value>,"secondary":<Boolean_value>,"groupextraction":<Boolean_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationvserver?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "authenticationvserver": [ { "__count": "#no"} ] }```



