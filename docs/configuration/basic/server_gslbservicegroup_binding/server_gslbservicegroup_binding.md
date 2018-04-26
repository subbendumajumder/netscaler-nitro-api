#server_gslbservicegroup_binding

Binding object showing the gslbservicegroup that can be bound to server.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name of the server for which to display parameters.<br>Minimum length = 1</td></tr><tr><td>servicegroupname</td><td>&lt;String></td><td>Read-write</td><td>servicegroups bind to this server.</td></tr><tr><td>svrtimeout</td><td>&lt;Double></td><td>Read-only</td><td>Time, in seconds, after which to terminate an idle server connection.<br>Minimum value = 0<br>Maximum value = 31536000</td></tr><tr><td>serviceipstr</td><td>&lt;String></td><td>Read-only</td><td>This field has been intorduced to show the dbs services ip.</td></tr><tr><td>cip</td><td>&lt;String></td><td>Read-only</td><td>Before forwarding a request to the service, insert an HTTP header with the client's IPv4 or IPv6 address as its value. Used if the server needs the client's IP address for security, accounting, or other purposes, and setting the Use Source IP parameter is not a viable option.<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>dup_port</td><td>&lt;Integer></td><td>Read-only</td><td>port of the service.<br>Range 1 - 65535<br>* in CLI is represented as 65535 in NITRO API</td></tr><tr><td>customserverid</td><td>&lt;String></td><td>Read-only</td><td>A positive integer to identify the service. Used when the persistency type is set to Custom Server ID.<br>Default value: "None"</td></tr><tr><td>boundtd</td><td>&lt;Double></td><td>Read-only</td><td>Integer value that uniquely identifies the traffic domain in which you want to configure the entity. If you do not specify an ID, the entity becomes part of the default traffic domain, which has an ID of 0.<br>Minimum value = 0<br>Maximum value = 4094</td></tr><tr><td>downstateflush</td><td>&lt;String></td><td>Read-only</td><td>Perform delayed clean-up of connections to all services in the service group.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>svctype</td><td>&lt;String></td><td>Read-only</td><td>The type of bound service.<br>Possible values = HTTP, FTP, TCP, UDP, SSL, SSL_BRIDGE, SSL_TCP, DTLS, NNTP, RPCSVR, DNS, ADNS, SNMP, RTSP, DHCPRA, ANY, SIP_UDP, SIP_TCP, SIP_SSL, DNS_TCP, ADNS_TCP, MYSQL, MSSQL, ORACLE, RADIUS, RADIUSListener, RDP, DIAMETER, SSL_DIAMETER, TFTP, SMPP, PPTP, GRE, SYSLOGTCP, SYSLOGUDP, FIX, SSL_FIX, USER_TCP, USER_SSL_TCP, QUIC</td></tr><tr><td>svrstate</td><td>&lt;String></td><td>Read-only</td><td>The state of the bound service.<br>Possible values = UP, DOWN, UNKNOWN, BUSY, OUT OF SERVICE, GOING OUT OF SERVICE, DOWN WHEN GOING OUT OF SERVICE, NS_EMPTY_STR, Unknown, DISABLED</td></tr><tr><td>appflowlog</td><td>&lt;String></td><td>Read-only</td><td>Enable logging of AppFlow information for the specified service group.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>cipheader</td><td>&lt;String></td><td>Read-only</td><td>Name of the HTTP header whose value must be set to the IP address of the client. Used with the Client IP parameter. If client IP insertion is enabled, and the client IP header is not specified, the value of Client IP Header parameter or the value set by the set ns config command is used as client's IP header name.<br>Minimum length = 1</td></tr><tr><td>maxclient</td><td>&lt;Double></td><td>Read-only</td><td>Maximum number of simultaneous open connections for the service group.<br>Minimum value = 0<br>Maximum value = 4294967294</td></tr><tr><td>clttimeout</td><td>&lt;Double></td><td>Read-only</td><td>Time, in seconds, after which to terminate an idle client connection.<br>Minimum value = 0<br>Maximum value = 31536000</td></tr><tr><td>port</td><td>&lt;Integer></td><td>Read-only</td><td>The port number to be used for the bound service.<br>Range 1 - 65535<br>* in CLI is represented as 65535 in NITRO API</td></tr><tr><td>dup_svctype</td><td>&lt;String></td><td>Read-only</td><td>service type of the service.<br>Possible values = HTTP, FTP, TCP, UDP, SSL, SSL_BRIDGE, SSL_TCP, DTLS, NNTP, RPCSVR, DNS, ADNS, SNMP, RTSP, DHCPRA, ANY, SIP_UDP, SIP_TCP, SIP_SSL, DNS_TCP, ADNS_TCP, MYSQL, MSSQL, ORACLE, RADIUS, RADIUSListener, RDP, DIAMETER, SSL_DIAMETER, TFTP, SMPP, PPTP, GRE, SYSLOGTCP, SYSLOGUDP, FIX, SSL_FIX, USER_TCP, USER_SSL_TCP, QUIC</td></tr><tr><td>monthreshold</td><td>&lt;Double></td><td>Read-only</td><td>Minimum sum of weights of the monitors that are bound to this service. Used to determine whether to mark a service as UP or DOWN.<br>Minimum value = 0<br>Maximum value = 65535</td></tr><tr><td>maxreq</td><td>&lt;Double></td><td>Read-only</td><td>Maximum number of requests that can be sent on a persistent connection to the service group. Note: Connection requests beyond this value are rejected.<br>Minimum value = 0<br>Maximum value = 65535</td></tr><tr><td>serviceipaddress</td><td>&lt;String></td><td>Read-only</td><td>The IP address of the bound service.</td></tr><tr><td>maxbandwidth</td><td>&lt;Double></td><td>Read-only</td><td>Maximum bandwidth, in Kbps, allocated for all the services in the service group.<br>Minimum value = 0<br>Maximum value = 4294967287</td></tr><tr><td>svrcfgflags</td><td>&lt;Double></td><td>Read-only</td><td>service flags to denote its a db enabled.</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[GET]()| [GET (ALL)](#get-)| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/server_gslbservicegroup_binding/name_value&lt;String&gt;
<b>Query-parameters:</b>
<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/server_gslbservicegroup_binding/name_value&lt;String&gt;?<b>filter=property-name1:property-value1,property-name2:property-value2</b>
Use this query-parameter to get the filtered set of server_gslbservicegroup_binding resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/server_gslbservicegroup_binding/name_value&lt;String&gt;?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the server_gslbservicegroup_binding resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "server_gslbservicegroup_binding": [ {"name":<String_value>,"servicegroupname":<String_value>,"svrtimeout":<Double_value>,"serviceipstr":<String_value>,"cip":<String_value>,"dup_port":<Integer_value>,"customserverid":<String_value>,"boundtd":<Double_value>,"downstateflush":<String_value>,"svctype":<String_value>,"svrstate":<String_value>,"appflowlog":<String_value>,"cipheader":<String_value>,"maxclient":<Double_value>,"clttimeout":<Double_value>,"port":<Integer_value>,"dup_svctype":<String_value>,"monthreshold":<Double_value>,"maxreq":<Double_value>,"serviceipaddress":<String_value>,"maxbandwidth":<Double_value>,"svrcfgflags":<Double_value>}]}```



###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/server_gslbservicegroup_binding
<b>Query-parameters:</b>
<b>bulkbindings</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/server_gslbservicegroup_binding?<b>bulkbindings=yes</b>
NITRO allows you to fetch bindings in bulk.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "server_gslbservicegroup_binding": [ {"name":<String_value>,"servicegroupname":<String_value>,"svrtimeout":<Double_value>,"serviceipstr":<String_value>,"cip":<String_value>,"dup_port":<Integer_value>,"customserverid":<String_value>,"boundtd":<Double_value>,"downstateflush":<String_value>,"svctype":<String_value>,"svrstate":<String_value>,"appflowlog":<String_value>,"cipheader":<String_value>,"maxclient":<Double_value>,"clttimeout":<Double_value>,"port":<Integer_value>,"dup_svctype":<String_value>,"monthreshold":<Double_value>,"maxreq":<Double_value>,"serviceipaddress":<String_value>,"maxbandwidth":<Double_value>,"svrcfgflags":<Double_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/server_gslbservicegroup_binding/name_value&lt;String&gt;?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{"server_gslbservicegroup_binding": [ { "__count": "#no"} ] }```



