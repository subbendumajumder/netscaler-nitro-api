#gslbdomain_gslbvserver_binding

Binding object showing the gslbvserver that can be bound to gslbdomain.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name of the Domain.&lt;br>Minimum length = 1</td><tr><tr><td>vservername</td><td>&lt;String></td><td>Read-write</td><td>.</td><tr><tr><td>sitename</td><td>&lt;String></td><td>Read-only</td><td>Name of the site to which the service belongs.</td><tr><tr><td>backuplbmethod</td><td>&lt;String></td><td>Read-only</td><td>Indicates the backup method in case the primary fails.&lt;br>Possible values = ROUNDROBIN, LEASTCONNECTION, LEASTRESPONSETIME, SOURCEIPHASH, LEASTBANDWIDTH, LEASTPACKETS, STATICPROXIMITY, RTT, CUSTOMLOAD</td><tr><tr><td>customheaders</td><td>&lt;String></td><td>Read-only</td><td>The string that is sent to the service. Applicable to HTTP ,HTTP-ECV and RTSP monitor types.</td><tr><tr><td>persistenceid</td><td>&lt;Double></td><td>Read-only</td><td>Persistence id of the gslb vserver.</td><tr><tr><td>state</td><td>&lt;String></td><td>Read-only</td><td>The state of the vserver.&lt;br>Possible values = UP, DOWN, UNKNOWN, BUSY, OUT OF SERVICE, GOING OUT OF SERVICE, DOWN WHEN GOING OUT OF SERVICE, NS_EMPTY_STR, Unknown, DISABLED</td><tr><tr><td>lbmethod</td><td>&lt;String></td><td>Read-only</td><td>The load balancing method set for the virtual server.&lt;br>Possible values = ROUNDROBIN, LEASTCONNECTION, LEASTRESPONSETIME, SOURCEIPHASH, LEASTBANDWIDTH, LEASTPACKETS, STATICPROXIMITY, RTT, CUSTOMLOAD</td><tr><tr><td>edr</td><td>&lt;String></td><td>Read-only</td><td>Send clients an empty DNS response when the GSLB virtual server is DOWN.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>cip</td><td>&lt;String></td><td>Read-only</td><td>Indicates if Client IP option is enabled.&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>statechangetimesec</td><td>&lt;String></td><td>Read-only</td><td>Time since last state change.</td><tr><tr><td>netmask</td><td>&lt;String></td><td>Read-only</td><td>Netmask.&lt;br>Minimum length = 1</td><tr><tr><td>dnsrecordtype</td><td>&lt;String></td><td>Read-only</td><td>The IP type for this GSLB vserver.&lt;br>Possible values = A, AAAA, CNAME, NAPTR</td><tr><tr><td>persistmask</td><td>&lt;String></td><td>Read-only</td><td>The optional IPv4 network mask applied to IPv4 addresses to establish source IP address based persistence.&lt;br>Minimum length = 1</td><tr><tr><td>sitepersistence</td><td>&lt;String></td><td>Read-only</td><td>Indicates the type of cookie persistence set.&lt;br>Possible values = ConnectionProxy, HTTPRedirect, NONE</td><tr><tr><td>servicetype</td><td>&lt;String></td><td>Read-only</td><td>The type GSLB service.&lt;br>Possible values = HTTP, FTP, TCP, UDP, SSL, SSL_BRIDGE, SSL_TCP, NNTP, ANY, SIP_UDP, SIP_TCP, SIP_SSL, RADIUS, RDP, RTSP, MYSQL, MSSQL, ORACLE</td><tr><tr><td>v6persistmasklen</td><td>&lt;Double></td><td>Read-only</td><td>Number of bits to consider in an IPv6 source IP address when creating source IP address based persistence sessions.&lt;br>Default value: 128&lt;br>Minimum value = 1&lt;br>Maximum value = 128</td><tr><tr><td>v6netmasklen</td><td>&lt;Double></td><td>Read-only</td><td>Number of bits to consider, in an IPv6 source IP address, for creating the hash that is required by the SOURCEIPHASH load balancing method.&lt;br>Default value: 128&lt;br>Minimum value = 1&lt;br>Maximum value = 128</td><tr><tr><td>persistencetype</td><td>&lt;String></td><td>Read-only</td><td>Indicates if persistence is set on the gslb vserver.&lt;br>Possible values = SOURCEIP, NONE</td><tr><tr><td>siteprefix</td><td>&lt;String></td><td>Read-only</td><td>The site prefix string.</td><tr><tr><td>dynamicweight</td><td>&lt;String></td><td>Read-only</td><td>Dynamic weight method of the vserver.&lt;br>Default value: DISABLED&lt;br>Possible values = SERVICECOUNT, SERVICEWEIGHT, DISABLED</td><tr><tr><td>mir</td><td>&lt;String></td><td>Read-only</td><td>.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[GET](#get) | [GET (ALL)](#get-(all)) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbdomain_gslbvserver_binding/name_value&lt;String&gt;
Query-parameters:
filter
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbdomain_gslbvserver_binding/name_value&lt;String&gt;?filter=property-name1:property-value1,property-name2:property-value2
Use this query-parameter to get the filtered set of gslbdomain_gslbvserver_binding resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


pagination
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbdomain_gslbvserver_binding/name_value&lt;String&gt;?pagesize=#no;pageno=#no
Use this query-parameter to get the gslbdomain_gslbvserver_binding resources in chunks.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "gslbdomain_gslbvserver_binding": [ {      "name":<String_value>,      "vservername":<String_value>,      "sitename":<String_value>,      "backuplbmethod":<String_value>,      "customheaders":<String_value>,      "persistenceid":<Double_value>,      "state":<String_value>,      "lbmethod":<String_value>,      "edr":<String_value>,      "cip":<String_value>,      "statechangetimesec":<String_value>,      "netmask":<String_value>,      "dnsrecordtype":<String_value>,      "persistmask":<String_value>,      "sitepersistence":<String_value>,      "servicetype":<String_value>,      "v6persistmasklen":<Double_value>,      "v6netmasklen":<Double_value>,      "persistencetype":<String_value>,      "siteprefix":<String_value>,      "dynamicweight":<String_value>,      "mir":<String_value>}]}```



###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbdomain_gslbvserver_binding
Query-parameters:
bulkbindings
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbdomain_gslbvserver_binding?bulkbindings=yes
NITRO allows you to fetch bindings in bulk.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "gslbdomain_gslbvserver_binding": [ {      "name":<String_value>,      "vservername":<String_value>,      "sitename":<String_value>,      "backuplbmethod":<String_value>,      "customheaders":<String_value>,      "persistenceid":<Double_value>,      "state":<String_value>,      "lbmethod":<String_value>,      "edr":<String_value>,      "cip":<String_value>,      "statechangetimesec":<String_value>,      "netmask":<String_value>,      "dnsrecordtype":<String_value>,      "persistmask":<String_value>,      "sitepersistence":<String_value>,      "servicetype":<String_value>,      "v6persistmasklen":<Double_value>,      "v6netmasklen":<Double_value>,      "persistencetype":<String_value>,      "siteprefix":<String_value>,      "dynamicweight":<String_value>,      "mir":<String_value>}]}```



###count



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbdomain_gslbvserver_binding/name_value&lt;String&gt;?count=yes
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: 
{"gslbdomain_gslbvserver_binding": [ { "__count": "#no"} ] }


