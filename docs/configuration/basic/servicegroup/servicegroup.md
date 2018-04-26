#servicegroup

Configuration for service group resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>servicegroupname</td><td>&lt;String></td><td>Read-write</td><td>Name of the service group. Must begin with an ASCII alphabetic or underscore (_) character, and must contain only ASCII alphanumeric, underscore, hash (#), period (.), space, colon (:), at (@), equals (=), and hyphen (-) characters. Can be changed after the name is created.<br>Minimum length = 1</td></tr><tr><td>servicetype</td><td>&lt;String></td><td>Read-write</td><td>Protocol used to exchange data with the service.<br>Possible values = HTTP, FTP, TCP, UDP, SSL, SSL_BRIDGE, SSL_TCP, DTLS, NNTP, RPCSVR, DNS, ADNS, SNMP, RTSP, DHCPRA, ANY, SIP_UDP, SIP_TCP, SIP_SSL, DNS_TCP, ADNS_TCP, MYSQL, MSSQL, ORACLE, RADIUS, RADIUSListener, RDP, DIAMETER, SSL_DIAMETER, TFTP, SMPP, PPTP, GRE, SYSLOGTCP, SYSLOGUDP, FIX, SSL_FIX, USER_TCP, USER_SSL_TCP, QUIC</td></tr><tr><td>cachetype</td><td>&lt;String></td><td>Read-write</td><td>Cache type supported by the cache server.<br>Possible values = TRANSPARENT, REVERSE, FORWARD</td></tr><tr><td>td</td><td>&lt;Double></td><td>Read-write</td><td>Integer value that uniquely identifies the traffic domain in which you want to configure the entity. If you do not specify an ID, the entity becomes part of the default traffic domain, which has an ID of 0.<br>Minimum value = 0<br>Maximum value = 4094</td></tr><tr><td>maxclient</td><td>&lt;Double></td><td>Read-write</td><td>Maximum number of simultaneous open connections for the service group.<br>Minimum value = 0<br>Maximum value = 4294967294</td></tr><tr><td>maxreq</td><td>&lt;Double></td><td>Read-write</td><td>Maximum number of requests that can be sent on a persistent connection to the service group. <br>Note: Connection requests beyond this value are rejected.<br>Minimum value = 0<br>Maximum value = 65535</td></tr><tr><td>cacheable</td><td>&lt;String></td><td>Read-write</td><td>Use the transparent cache redirection virtual server to forward the request to the cache server.<br>Note: Do not set this parameter if you set the Cache Type.<br>Default value: NO<br>Possible values = YES, NO</td></tr><tr><td>cip</td><td>&lt;String></td><td>Read-write</td><td>Insert the Client IP header in requests forwarded to the service.<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>cipheader</td><td>&lt;String></td><td>Read-write</td><td>Name of the HTTP header whose value must be set to the IP address of the client. Used with the Client IP parameter. If client IP insertion is enabled, and the client IP header is not specified, the value of Client IP Header parameter or the value set by the set ns config command is used as client's IP header name.<br>Minimum length = 1</td></tr><tr><td>usip</td><td>&lt;String></td><td>Read-write</td><td>Use client's IP address as the source IP address when initiating connection to the server. With the NO setting, which is the default, a mapped IP (MIP) address or subnet IP (SNIP) address is used as the source IP address to initiate server side connections.<br>Possible values = YES, NO</td></tr><tr><td>pathmonitor</td><td>&lt;String></td><td>Read-write</td><td>Path monitoring for clustering.<br>Possible values = YES, NO</td></tr><tr><td>pathmonitorindv</td><td>&lt;String></td><td>Read-write</td><td>Individual Path monitoring decisions.<br>Possible values = YES, NO</td></tr><tr><td>useproxyport</td><td>&lt;String></td><td>Read-write</td><td>Use the proxy port as the source port when initiating connections with the server. With the NO setting, the client-side connection port is used as the source port for the server-side connection. <br>Note: This parameter is available only when the Use Source IP (USIP) parameter is set to YES.<br>Possible values = YES, NO</td></tr><tr><td>healthmonitor</td><td>&lt;String></td><td>Read-write</td><td>Monitor the health of this service. Available settings function as follows:<br>YES - Send probes to check the health of the service.<br>NO - Do not send probes to check the health of the service. With the NO option, the appliance shows the service as UP at all times.<br>Default value: YES<br>Possible values = YES, NO</td></tr><tr><td>sc</td><td>&lt;String></td><td>Read-write</td><td>State of the SureConnect feature for the service group.<br>Default value: OFF<br>Possible values = ON, OFF</td></tr><tr><td>sp</td><td>&lt;String></td><td>Read-write</td><td>Enable surge protection for the service group.<br>Default value: OFF<br>Possible values = ON, OFF</td></tr><tr><td>rtspsessionidremap</td><td>&lt;String></td><td>Read-write</td><td>Enable RTSP session ID mapping for the service group.<br>Default value: OFF<br>Possible values = ON, OFF</td></tr><tr><td>clttimeout</td><td>&lt;Double></td><td>Read-write</td><td>Time, in seconds, after which to terminate an idle client connection.<br>Minimum value = 0<br>Maximum value = 31536000</td></tr><tr><td>svrtimeout</td><td>&lt;Double></td><td>Read-write</td><td>Time, in seconds, after which to terminate an idle server connection.<br>Minimum value = 0<br>Maximum value = 31536000</td></tr><tr><td>cka</td><td>&lt;String></td><td>Read-write</td><td>Enable client keep-alive for the service group.<br>Possible values = YES, NO</td></tr><tr><td>tcpb</td><td>&lt;String></td><td>Read-write</td><td>Enable TCP buffering for the service group.<br>Possible values = YES, NO</td></tr><tr><td>cmp</td><td>&lt;String></td><td>Read-write</td><td>Enable compression for the specified service.<br>Possible values = YES, NO</td></tr><tr><td>maxbandwidth</td><td>&lt;Double></td><td>Read-write</td><td>Maximum bandwidth, in Kbps, allocated for all the services in the service group.<br>Minimum value = 0<br>Maximum value = 4294967287</td></tr><tr><td>monthreshold</td><td>&lt;Double></td><td>Read-write</td><td>Minimum sum of weights of the monitors that are bound to this service. Used to determine whether to mark a service as UP or DOWN.<br>Minimum value = 0<br>Maximum value = 65535</td></tr><tr><td>state</td><td>&lt;String></td><td>Read-write</td><td>Initial state of the service group.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>downstateflush</td><td>&lt;String></td><td>Read-write</td><td>Flush all active transactions associated with all the services in the service group whose state transitions from UP to DOWN. Do not enable this option for applications that must complete their transactions.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>tcpprofilename</td><td>&lt;String></td><td>Read-write</td><td>Name of the TCP profile that contains TCP configuration settings for the service group.<br>Minimum length = 1<br>Maximum length = 127</td></tr><tr><td>httpprofilename</td><td>&lt;String></td><td>Read-write</td><td>Name of the HTTP profile that contains HTTP configuration settings for the service group.<br>Minimum length = 1<br>Maximum length = 127</td></tr><tr><td>comment</td><td>&lt;String></td><td>Read-write</td><td>Any information about the service group.</td></tr><tr><td>appflowlog</td><td>&lt;String></td><td>Read-write</td><td>Enable logging of AppFlow information for the specified service group.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>netprofile</td><td>&lt;String></td><td>Read-write</td><td>Network profile for the service group.<br>Minimum length = 1<br>Maximum length = 127</td></tr><tr><td>autoscale</td><td>&lt;String></td><td>Read-write</td><td>Auto scale option for a servicegroup.<br>Default value: DISABLED<br>Possible values = DISABLED, DNS, POLICY</td></tr><tr><td>memberport</td><td>&lt;Integer></td><td>Read-write</td><td>member port.</td></tr><tr><td>monconnectionclose</td><td>&lt;String></td><td>Read-write</td><td>Close monitoring connections by sending the service a connection termination message with the specified bit set.<br>Default value: NONE<br>Possible values = RESET, FIN</td></tr><tr><td>servername</td><td>&lt;String></td><td>Read-write</td><td>Name of the server to which to bind the service group.<br>Minimum length = 1</td></tr><tr><td>port</td><td>&lt;Integer></td><td>Read-write</td><td>Server port number.<br>Range 1 - 65535<br>* in CLI is represented as 65535 in NITRO API</td></tr><tr><td>weight</td><td>&lt;Double></td><td>Read-write</td><td>Weight to assign to the servers in the service group. Specifies the capacity of the servers relative to the other servers in the load balancing configuration. The higher the weight, the higher the percentage of requests sent to the service.<br>Minimum value = 1<br>Maximum value = 100</td></tr><tr><td>customserverid</td><td>&lt;String></td><td>Read-write</td><td>The identifier for this IP:Port pair. Used when the persistency type is set to Custom Server ID.<br>Default value: "None"</td></tr><tr><td>serverid</td><td>&lt;Double></td><td>Read-write</td><td>The identifier for the service. This is used when the persistency type is set to Custom Server ID.</td></tr><tr><td>hashid</td><td>&lt;Double></td><td>Read-write</td><td>The hash identifier for the service. This must be unique for each service. This parameter is used by hash based load balancing methods.<br>Minimum value = 1</td></tr><tr><td>monitor_name_svc</td><td>&lt;String></td><td>Read-write</td><td>Name of the monitor bound to the service group. Used to assign a weight to the monitor.<br>Minimum length = 1</td></tr><tr><td>dup_weight</td><td>&lt;Double></td><td>Read-write</td><td>weight of the monitor that is bound to servicegroup.<br>Minimum value = 1</td></tr><tr><td>riseapbrstatsmsgcode</td><td>&lt;Integer></td><td>Read-write</td><td>The code indicating the rise apbr status.</td></tr><tr><td>delay</td><td>&lt;Double></td><td>Read-write</td><td>Time, in seconds, allocated for a shutdown of the services in the service group. During this period, new requests are sent to the service only for clients who already have persistent sessions on the appliance. Requests from new clients are load balanced among other available services. After the delay time expires, no requests are sent to the service, and the service is marked as unavailable (OUT OF SERVICE).</td></tr><tr><td>graceful</td><td>&lt;String></td><td>Read-write</td><td>Wait for all existing connections to the service to terminate before shutting down the service.<br>Default value: NO<br>Possible values = YES, NO</td></tr><tr><td>includemembers</td><td>&lt;Boolean></td><td>Read-write</td><td>Display the members of the listed service groups in addition to their settings. Can be specified when no service group name is provided in the command. In that case, the details displayed for each service group are identical to the details displayed when a service group name is provided, except that bound monitors are not displayed.</td></tr><tr><td>newname</td><td>&lt;String></td><td>Read-write</td><td>New name for the service group.<br>Minimum length = 1</td></tr><tr><td>numofconnections</td><td>&lt;Integer></td><td>Read-only</td><td>This will tell the number of client side connections are still open.</td></tr><tr><td>serviceconftype</td><td>&lt;Boolean></td><td>Read-only</td><td>The configuration type of the service group.</td></tr><tr><td>value</td><td>&lt;String></td><td>Read-only</td><td>SSL Status.<br>Possible values = Certkey not bound, SSL feature disabled</td></tr><tr><td>svrstate</td><td>&lt;String></td><td>Read-only</td><td>The state of the service.<br>Possible values = UP, DOWN, UNKNOWN, BUSY, OUT OF SERVICE, GOING OUT OF SERVICE, DOWN WHEN GOING OUT OF SERVICE, NS_EMPTY_STR, Unknown, DISABLED</td></tr><tr><td>ip</td><td>&lt;String></td><td>Read-only</td><td>IP Address.</td></tr><tr><td>monstatcode</td><td>&lt;Integer></td><td>Read-only</td><td>The code indicating the monitor response.</td></tr><tr><td>monstatparam1</td><td>&lt;Integer></td><td>Read-only</td><td>First parameter for use with message code.</td></tr><tr><td>monstatparam2</td><td>&lt;Integer></td><td>Read-only</td><td>Second parameter for use with message code.</td></tr><tr><td>monstatparam3</td><td>&lt;Integer></td><td>Read-only</td><td>Third parameter for use with message code.</td></tr><tr><td>statechangetimemsec</td><td>&lt;Double></td><td>Read-only</td><td>Time when last state change occurred. Milliseconds part.</td></tr><tr><td>stateupdatereason</td><td>&lt;Double></td><td>Read-only</td><td>Checks state update reason on the secondary node.</td></tr><tr><td>clmonowner</td><td>&lt;Double></td><td>Read-only</td><td>Tells the mon owner of the service.</td></tr><tr><td>clmonview</td><td>&lt;Double></td><td>Read-only</td><td>Tells the view id of the monitoring owner.</td></tr><tr><td>groupcount</td><td>&lt;Double></td><td>Read-only</td><td>Servicegroup Count.</td></tr><tr><td>riseapbrstatsmsgcode2</td><td>&lt;Integer></td><td>Read-only</td><td>The code indicating other rise stats.</td></tr><tr><td>serviceipstr</td><td>&lt;String></td><td>Read-only</td><td>This field has been intorduced to show the dbs services ip.</td></tr><tr><td>servicegroupeffectivestate</td><td>&lt;String></td><td>Read-only</td><td>Indicates the effective servicegroup state based on the state of the bound service items.If all services are UP the effective state is UP, if all are DOWN its DOWN,if all are OFS its OFS.If atleast one serviceis UP and rest are either DOWN or OFS, the effective state is PARTIAL-UP.If atleast one bound service is DOWN and rest are OFS the effective state is PARTIAL DOWN.<br>Possible values = UP, DOWN, OUT OF SERVICE, PARTIAL-UP, PARTIAL-DOWN</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD]()| [DELETE](#d)| [UPDATE](#u)| [UNSET](#)| [ENABLE](#e)| [DISABLE](#di)| [RENAME](#r)| [GET (ALL)](#get-)| [GET]()| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/servicegroup
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"servicegroup":{<b>"servicegroupname":<String_value>,</b><b>"servicetype":<String_value>,</b>"cachetype":<String_value>,"td":<Double_value>,"maxclient":<Double_value>,"maxreq":<Double_value>,"cacheable":<String_value>,"cip":<String_value>,"cipheader":<String_value>,"usip":<String_value>,"pathmonitor":<String_value>,"pathmonitorindv":<String_value>,"useproxyport":<String_value>,"healthmonitor":<String_value>,"sc":<String_value>,"sp":<String_value>,"rtspsessionidremap":<String_value>,"clttimeout":<Double_value>,"svrtimeout":<Double_value>,"cka":<String_value>,"tcpb":<String_value>,"cmp":<String_value>,"maxbandwidth":<Double_value>,"monthreshold":<Double_value>,"state":<String_value>,"downstateflush":<String_value>,"tcpprofilename":<String_value>,"httpprofilename":<String_value>,"comment":<String_value>,"appflowlog":<String_value>,"netprofile":<String_value>,"autoscale":<String_value>,"memberport":<Integer_value>,"monconnectionclose":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/servicegroup/servicegroupname_value&lt;String&gt;
<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/servicegroup
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"servicegroup":{<b>"servicegroupname":<String_value>,</b>"servername":<String_value>,"port":<Integer_value>,"weight":<Double_value>,"customserverid":<String_value>,"serverid":<Double_value>,"hashid":<Double_value>,"monitor_name_svc":<String_value>,"dup_weight":<Double_value>,"maxclient":<Double_value>,"maxreq":<Double_value>,"healthmonitor":<String_value>,"cacheable":<String_value>,"cip":<String_value>,"cipheader":<String_value>,"usip":<String_value>,"pathmonitor":<String_value>,"pathmonitorindv":<String_value>,"useproxyport":<String_value>,"sc":<String_value>,"sp":<String_value>,"rtspsessionidremap":<String_value>,"clttimeout":<Double_value>,"svrtimeout":<Double_value>,"cka":<String_value>,"tcpb":<String_value>,"cmp":<String_value>,"maxbandwidth":<Double_value>,"monthreshold":<Double_value>,"downstateflush":<String_value>,"tcpprofilename":<String_value>,"httpprofilename":<String_value>,"comment":<String_value>,"appflowlog":<String_value>,"netprofile":<String_value>,"monconnectionclose":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/servicegroup?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"servicegroup":{<b>"servicegroupname":<String_value>,</b>"servername":true,"port":true,"weight":true,"customserverid":true,"serverid":true,"hashid":true,"riseapbrstatsmsgcode":true,"maxclient":true,"maxreq":true,"cacheable":true,"cip":true,"usip":true,"useproxyport":true,"sc":true,"sp":true,"rtspsessionidremap":true,"clttimeout":true,"svrtimeout":true,"cka":true,"tcpb":true,"cmp":true,"maxbandwidth":true,"monthreshold":true,"tcpprofilename":true,"httpprofilename":true,"appflowlog":true,"netprofile":true,"monitor_name_svc":true,"dup_weight":true,"healthmonitor":true,"cipheader":true,"pathmonitor":true,"pathmonitorindv":true,"downstateflush":true,"comment":true,"monconnectionclose":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###enable



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/servicegroup?<b>action=enable</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"servicegroup":{<b>"servicegroupname":<String_value>,</b>"servername":<String_value>,"port":<Integer_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###disable



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/servicegroup?<b>action=disable</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"servicegroup":{<b>"servicegroupname":<String_value>,</b>"servername":<String_value>,"port":<Integer_value>,"delay":<Double_value>,"graceful":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###rename



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/servicegroup?<b>action=rename</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"servicegroup":{<b>"servicegroupname":<String_value>,</b><b>"newname":<String_value></b>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/servicegroup
<b>Query-parameters:</b>
<b>args</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/servicegroup?<b>args=servicegroupname:&lt;String_value&gt;,includemembers:&lt;Boolean_value&gt;</b>
Use this query-parameter to get servicegroup resources based on additional properties.


<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/servicegroup?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/servicegroup?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of servicegroup resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/servicegroup?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/servicegroup?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the servicegroup resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "servicegroup": [ {servicegroupname:<String_value>,includemembers:<Boolean_value>"numofconnections":<Integer_value>,"servicetype":<String_value>,"port":<Integer_value>,"td":<Double_value>,"serviceconftpye":<Boolean_value>,"serviceconftype":<Boolean_value>,"value":<String_value>,"cachetype":<String_value>,"maxclient":<Double_value>,"maxreq":<Double_value>,"cacheable":<String_value>,"cip":<String_value>,"cipheader":<String_value>,"usip":<String_value>,"pathmonitor":<String_value>,"pathmonitorindv":<String_value>,"useproxyport":<String_value>,"sc":<String_value>,"sp":<String_value>,"rtspsessionidremap":<String_value>,"clttimeout":<Double_value>,"svrtimeout":<Double_value>,"cka":<String_value>,"tcpb":<String_value>,"cmp":<String_value>,"maxbandwidth":<Double_value>,"state":<String_value>,"svrstate":<String_value>,"delay":<Double_value>,"ip":<String_value>,"servername":<String_value>,"monthreshold":<Double_value>,"weight":<Double_value>,"customserverid":<String_value>,"serverid":<Double_value>,"monstatcode":<Integer_value>,"monstatparam1":<Integer_value>,"monstatparam2":<Integer_value>,"monstatparam3":<Integer_value>,"downstateflush":<String_value>,"statechangetimemsec":<Double_value>,"timesincelaststatechange":<Double_value>,"stateupdatereason":<Double_value>,"clmonowner":<Double_value>,"clmonview":<Double_value>,"groupcount":<Double_value>,"comment":<String_value>,"tcpprofilename":<String_value>,"httpprofilename":<String_value>,"hashid":<Double_value>,"riseapbrstatsmsgcode":<Integer_value>,"riseapbrstatsmsgcode2":<Integer_value>,"graceful":<String_value>,"healthmonitor":<String_value>,"appflowlog":<String_value>,"netprofile":<String_value>,"autoscale":<String_value>,"memberport":<Integer_value>,"serviceipstr":<String_value>,"servicegroupeffectivestate":<String_value>,"monconnectionclose":<String_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/servicegroup/servicegroupname_value&lt;String&gt;
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/servicegroup/servicegroupname_value&lt;String&gt;?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/servicegroup/servicegroupname_value&lt;String&gt;?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "servicegroup": [ {servicegroupname:<String_value>,includemembers:<Boolean_value>"numofconnections":<Integer_value>,"servicetype":<String_value>,"port":<Integer_value>,"td":<Double_value>,"serviceconftpye":<Boolean_value>,"serviceconftype":<Boolean_value>,"value":<String_value>,"cachetype":<String_value>,"maxclient":<Double_value>,"maxreq":<Double_value>,"cacheable":<String_value>,"cip":<String_value>,"cipheader":<String_value>,"usip":<String_value>,"pathmonitor":<String_value>,"pathmonitorindv":<String_value>,"useproxyport":<String_value>,"sc":<String_value>,"sp":<String_value>,"rtspsessionidremap":<String_value>,"clttimeout":<Double_value>,"svrtimeout":<Double_value>,"cka":<String_value>,"tcpb":<String_value>,"cmp":<String_value>,"maxbandwidth":<Double_value>,"state":<String_value>,"svrstate":<String_value>,"delay":<Double_value>,"ip":<String_value>,"servername":<String_value>,"monthreshold":<Double_value>,"weight":<Double_value>,"customserverid":<String_value>,"serverid":<Double_value>,"monstatcode":<Integer_value>,"monstatparam1":<Integer_value>,"monstatparam2":<Integer_value>,"monstatparam3":<Integer_value>,"downstateflush":<String_value>,"statechangetimemsec":<Double_value>,"timesincelaststatechange":<Double_value>,"stateupdatereason":<Double_value>,"clmonowner":<Double_value>,"clmonview":<Double_value>,"groupcount":<Double_value>,"comment":<String_value>,"tcpprofilename":<String_value>,"httpprofilename":<String_value>,"hashid":<Double_value>,"riseapbrstatsmsgcode":<Integer_value>,"riseapbrstatsmsgcode2":<Integer_value>,"graceful":<String_value>,"healthmonitor":<String_value>,"appflowlog":<String_value>,"netprofile":<String_value>,"autoscale":<String_value>,"memberport":<Integer_value>,"serviceipstr":<String_value>,"servicegroupeffectivestate":<String_value>,"monconnectionclose":<String_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/servicegroup?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "servicegroup": [ { "__count": "#no"} ] }```



