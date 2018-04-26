#gslbservicegroupmember

Statistics for GSLB service group entity resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>servicegroupname</td><td>&lt;String></td><td>Read-write</td><td>Displays statistics for the specified GSLB service group.Name of the GSLB service group. Must begin with an ASCII alphanumeric or underscore (_) character, and must contain only ASCII alphanumeric, underscore, hash (#), period (.), space, colon (:), at sign (@), equal sign (=), and hyphen (-) characters.CLI Users: If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my servicegroup" or 'my servicegroup').<br>Minimum length = 1</td></tr><tr><td>ip</td><td>&lt;String></td><td>Read-write</td><td>IP address of the GSLB service group. Mutually exclusive with the server name parameter.</td></tr><tr><td>servername</td><td>&lt;String></td><td>Read-write</td><td>Name of the server. Mutually exclusive with the IP address parameter.<br>Minimum length = 1</td></tr><tr><td>port</td><td>&lt;Integer></td><td>Read-write</td><td>Port number of the service group member.<br>Range 1 - 65535<br>* in CLI is represented as 65535 in NITRO API</td></tr><tr><td>clearstats</td><td>&lt;String></td><td>Read-write</td><td>Clear the statsistics / counters.<br>Possible values = basic, full</td></tr><tr><td>establishedconn</td><td>&lt;Double></td><td>Read-only</td><td>Number of client connections in ESTABLISHED state.</td></tr><tr><td>primaryipaddress</td><td>&lt;String></td><td>Read-only</td><td>The IP address on which the service is running.</td></tr><tr><td>primaryport</td><td>&lt;Integer></td><td>Read-only</td><td>The port on which the service is running.</td></tr><tr><td>servicetype</td><td>&lt;String></td><td>Read-only</td><td>The service type of this service.Possible values are ADNS, DNS, MYSQL, RTSP, SSL_DIAMETER, ADNS_TCP, DNS_TCP, NNTP, SIP_UDP, SSL_TCP, ANY, FTP, RADIUS, SNMP, TCP, DHCPRA, HTTP, RDP, SSL, TFTP, DIAMETER, MSSQL, RPCSVR, SSL_BRIDGE, UDP</td></tr><tr><td>state</td><td>&lt;String></td><td>Read-only</td><td>Current state of the server. Possible values are UP, DOWN, UNKNOWN, OFS(Out of Service), TROFS(Transition Out of Service), TROFS_DOWN(Down When going Out of Service)</td></tr><tr><td>totalrequestbytes</td><td>&lt;Double></td><td>Read-only</td><td>Total number of request bytes received on this service or virtual server.</td></tr><tr><td>requestbytesrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for totalrequestbytes</td></tr><tr><td>totalresponsebytes</td><td>&lt;Double></td><td>Read-only</td><td>Number of response bytes received by this service or virtual server.</td></tr><tr><td>responsebytesrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for totalresponsebytes</td></tr><tr><td>curload</td><td>&lt;Double></td><td>Read-only</td><td>Load on the service that is calculated from the bound load based monitor.</td></tr><tr><td>totalrequests</td><td>&lt;Double></td><td>Read-only</td><td>Total number of requests received on this service or virtual server. (This applies to HTTP/SSL services and servers.)</td></tr><tr><td>requestsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for totalrequests</td></tr><tr><td>totalresponses</td><td>&lt;Double></td><td>Read-only</td><td>Number of responses received on this service or virtual server. (This applies to HTTP/SSL services and servers.)</td></tr><tr><td>responsesrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for totalresponses</td></tr><tr><td>curclntconnections</td><td>&lt;Double></td><td>Read-only</td><td>Number of current client connections.</td></tr><tr><td>cursrvrconnections</td><td>&lt;Double></td><td>Read-only</td><td>Number of current connections to the actual servers behind the virtual server.</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[GET (ALL)](#get-)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/gslbservicegroupmember
<b>Query-parameters:</b>
<b>args</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/gslbservicegroupmember?<b>args=<b>servicegroupname:&lt;String_value&gt;,</b>ip:&lt;String_value&gt;,servername:&lt;String_value&gt;,<b>port:&lt;Integer_value&gt;,</b>detail:&lt;Boolean_value&gt;,fullvalues:&lt;Boolean_value&gt;,ntimes:&lt;Double_value&gt;,logfile:&lt;String_value&gt;,clearstats:&lt;String_value&gt;</b>
Use this query-parameter to get gslbservicegroupmember resources based on additional properties.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "gslbservicegroupmember": [ {"servicegroupname":<String_value>,"curclntconnections":<Double_value>,"servicetype":<String_value>,"establishedconn":<Double_value>,"totalrequests":<Double_value>,"responsebytesrate":<Double_value>,"totalresponses":<Double_value>,"requestbytesrate":<Double_value>,"cursrvrconnections":<Double_value>,"primaryipaddress":<String_value>,"responsesrate":<Double_value>,"curload":<Double_value>,"totalrequestbytes":<Double_value>,"state":<String_value>,"totalresponsebytes":<Double_value>,"primaryport":<Integer_value>,"requestsrate":<Double_value>}]}```



