#lsnrtspalgsession_datachannel_binding

Binding object showing the datachannel that can be bound to lsnrtspalgsession.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>channelip</td><td>&lt;String></td><td>Read-write</td><td>IP address of the channel.</td><tr><tr><td>sessionid</td><td>&lt;String></td><td>Read-write</td><td>Session ID for the RTSP call.</td><tr><tr><td>channelnatip</td><td>&lt;String></td><td>Read-only</td><td>Natted IP address of the channel.</td><tr><tr><td>channelport</td><td>&lt;Integer></td><td>Read-only</td><td>port for the channel.</td><tr><tr><td>channelflags</td><td>&lt;Double></td><td>Read-only</td><td>Flags for the call entry.</td><tr><tr><td>channeltimeout</td><td>&lt;Double></td><td>Read-only</td><td>Timeout for the channel.</td><tr><tr><td>channelnatport</td><td>&lt;Integer></td><td>Read-only</td><td>Natted port for the channel.</td><tr><tr><td>channelprotocol</td><td>&lt;String></td><td>Read-only</td><td>Channel transport protocol.&lt;br>Possible values = HTTP, FTP, TCP, UDP, SSL, SSL_BRIDGE, SSL_TCP, NNTP, RPCSVR, DNS, ADNS, SNMP, RTSP, DHCPRA, ANY, SIP_UDP, SIP_TCP, SIP_SSL, DNS_TCP, ADNS_TCP, HTTPSVR, HTTPCLIENT, NAT, HA, AAA, SINCTCP, VPN AFTP, MONITORS, SSLVPN UDP, SINCUDP, RIP, UDP CLNT, SASP, RPCCLNTS, ROUTE, AUDIT, STA HTTP, STA SSL, DNS RESOLVE, RDP, MYSQL, MSSQL, DIAMETER, SSL_DIAMETER, TFTP, ORACLE, ICA, RADIUS, RADIUSListener, SMPP, PPTP, GRE, SYSLOGTCP, SYSLOGUDP, FIX, SSL_FIX, TFTP_DATA, USER_TCP, USER_SSL_TCP</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[GET](#get) | [GET (ALL)](#get-(all)) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsnrtspalgsession_datachannel_binding/sessionid_value&lt;String&gt;
Query-parameters:
filter
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsnrtspalgsession_datachannel_binding/sessionid_value&lt;String&gt;?filter=property-name1:property-value1,property-name2:property-value2
Use this query-parameter to get the filtered set of lsnrtspalgsession_datachannel_binding resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


pagination
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsnrtspalgsession_datachannel_binding/sessionid_value&lt;String&gt;?pagesize=#no;pageno=#no
Use this query-parameter to get the lsnrtspalgsession_datachannel_binding resources in chunks.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "lsnrtspalgsession_datachannel_binding": [ {      "channelip":<String_value>,      "sessionid":<String_value>,      "channelnatip":<String_value>,      "channelport":<Integer_value>,      "channelflags":<Double_value>,      "channeltimeout":<Double_value>,      "channelnatport":<Integer_value>,      "channelprotocol":<String_value>}]}```



###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsnrtspalgsession_datachannel_binding
Query-parameters:
bulkbindings
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsnrtspalgsession_datachannel_binding?bulkbindings=yes
NITRO allows you to fetch bindings in bulk.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "lsnrtspalgsession_datachannel_binding": [ {      "channelip":<String_value>,      "sessionid":<String_value>,      "channelnatip":<String_value>,      "channelport":<Integer_value>,      "channelflags":<Double_value>,      "channeltimeout":<Double_value>,      "channelnatport":<Integer_value>,      "channelprotocol":<String_value>}]}```



###count



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsnrtspalgsession_datachannel_binding/sessionid_value&lt;String&gt;?count=yes
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: 
{"lsnrtspalgsession_datachannel_binding": [ { "__count": "#no"} ] }


