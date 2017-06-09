#nsmode

Configuration for ns mode resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>mode</td><td>&lt;String[]></td><td>Read-write</td><td>Mode to be enabled. Multiple modes can be specified by providing a blank space between each mode.&lt;br>Possible values = FR, FastRamp, L2, L2mode, L3, L3mode, USIP, UseSourceIP, CKA, ClientKeepAlive, TCPB, TCPBuffering, MBF, MACbasedforwarding, Edge, USNIP, SRADV, DRADV, IRADV, SRADV6, DRADV6, PMTUD, RISE_APBR, RISE_RHI, BridgeBPDUs, Mediaclassification, ULFD</td><tr><tr><td>fr</td><td>&lt;Boolean></td><td>Read-only</td><td>Fast Ramp.</td><tr><tr><td>l2</td><td>&lt;Boolean></td><td>Read-only</td><td>Layer 2 mode.</td><tr><tr><td>usip</td><td>&lt;Boolean></td><td>Read-only</td><td>Use Source IP.</td><tr><tr><td>cka</td><td>&lt;Boolean></td><td>Read-only</td><td>Client Keep-alive.</td><tr><tr><td>tcpb</td><td>&lt;Boolean></td><td>Read-only</td><td>TCP Buffering.</td><tr><tr><td>mbf</td><td>&lt;Boolean></td><td>Read-only</td><td>MAC-based forwarding.</td><tr><tr><td>edge</td><td>&lt;Boolean></td><td>Read-only</td><td>Edge configuration.</td><tr><tr><td>usnip</td><td>&lt;Boolean></td><td>Read-only</td><td>Use Subnet IP.</td><tr><tr><td>l3</td><td>&lt;Boolean></td><td>Read-only</td><td>Layer 3 mode (ip forwarding).</td><tr><tr><td>pmtud</td><td>&lt;Boolean></td><td>Read-only</td><td>Path MTU Discovery.</td><tr><tr><td>mediaclassification</td><td>&lt;Boolean></td><td>Read-only</td><td>mediaclassification.</td><tr><tr><td>sradv</td><td>&lt;Boolean></td><td>Read-only</td><td>Static Route Advertisement.</td><tr><tr><td>dradv</td><td>&lt;Boolean></td><td>Read-only</td><td>Direct Route Advertisement.</td><tr><tr><td>iradv</td><td>&lt;Boolean></td><td>Read-only</td><td>Intranet Route Advertisement.</td><tr><tr><td>sradv6</td><td>&lt;Boolean></td><td>Read-only</td><td>Ipv6 Static Route Advertisement.</td><tr><tr><td>dradv6</td><td>&lt;Boolean></td><td>Read-only</td><td>Ipv6 Direct Route Advertisement.</td><tr><tr><td>bridgebpdus</td><td>&lt;Boolean></td><td>Read-only</td><td>BPDU Bridging Mode.</td><tr><tr><td>rise_apbr</td><td>&lt;Boolean></td><td>Read-only</td><td>APBR Publishing Mode.</td><tr><tr><td>rise_rhi</td><td>&lt;Boolean></td><td>Read-only</td><td>RHI Publishing Mode.</td><tr><tr><td>ulfd</td><td>&lt;Boolean></td><td>Read-only</td><td>Unified Logging Framework Mode for adding/removing ULF services.</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ENABLE](#enable) | [DISABLE](#disable) | [GET (ALL)](#get-(all))


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###enable



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsmode?action=enable
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"nsmode":{      "mode":<String[]_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###disable



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsmode?action=disable
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"nsmode":{      "mode":<String[]_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsmode
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "nsmode": [ {      "mode":<String[]_value>,      "fr":<Boolean_value>,      "l2":<Boolean_value>,      "usip":<Boolean_value>,      "cka":<Boolean_value>,      "tcpb":<Boolean_value>,      "mbf":<Boolean_value>,      "edge":<Boolean_value>,      "usnip":<Boolean_value>,      "l3":<Boolean_value>,      "pmtud":<Boolean_value>,      "mediaclassification":<Boolean_value>,      "sradv":<Boolean_value>,      "dradv":<Boolean_value>,      "iradv":<Boolean_value>,      "sradv6":<Boolean_value>,      "dradv6":<Boolean_value>,      "bridgebpdus":<Boolean_value>,      "rise_apbr":<Boolean_value>,      "rise_rhi":<Boolean_value>,      "ulfd":<Boolean_value>}]}```



