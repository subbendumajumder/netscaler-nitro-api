#l2param

Configuration for Layer 2 related parameter resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>mbfpeermacupdate</td><td>&lt;Double></td><td>Read-write</td><td>When mbf_instant_learning is enabled, learn any changes in peers MAC after this time interval, which is in 10ms ticks.&lt;br>Default value: 10</td><tr><tr><td>maxbridgecollision</td><td>&lt;Double></td><td>Read-write</td><td>Maximum bridge collision for loop detection .&lt;br>Default value: 20</td><tr><tr><td>bdggrpproxyarp</td><td>&lt;String></td><td>Read-write</td><td>Set/reset proxy ARP in bridge group deployment.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>bdgsetting</td><td>&lt;String></td><td>Read-write</td><td>Bridging settings for C2C behavior. If enabled, each PE will learn MAC entries independently. Otherwise, when L2 mode is ON, learned MAC entries on a PE will be broadcasted to all other PEs.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>garponvridintf</td><td>&lt;String></td><td>Read-write</td><td>Send GARP messagess on VRID-configured interfaces upon failover .&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>macmodefwdmypkt</td><td>&lt;String></td><td>Read-write</td><td>Allows MAC mode vserver to pick and forward the packets even if it is destined to NetScaler owned VIP.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>usemymac</td><td>&lt;String></td><td>Read-write</td><td>Use Netscaler MAC for all outgoing packets.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>proxyarp</td><td>&lt;String></td><td>Read-write</td><td>Proxies the ARP as Netscaler MAC for FreeBSD.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>garpreply</td><td>&lt;String></td><td>Read-write</td><td>Set/reset REPLY form of GARP .&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>mbfinstlearning</td><td>&lt;String></td><td>Read-write</td><td>Enable instant learning of MAC changes in MBF mode.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>rstintfonhafo</td><td>&lt;String></td><td>Read-write</td><td>Enable the reset interface upon HA failover.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>skipproxyingbsdtraffic</td><td>&lt;String></td><td>Read-write</td><td>Control source parameters (IP and Port) for FreeBSD initiated traffic. If Enabled, source parameters are retained. Else proxy the source parameters based on next hop.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>returntoethernetsender</td><td>&lt;String></td><td>Read-write</td><td>Return to ethernet sender.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>stopmacmoveupdate</td><td>&lt;String></td><td>Read-write</td><td>Stop Update of server mac change to NAT sessions.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>bridgeagetimeout</td><td>&lt;Double></td><td>Read-write</td><td>Time-out value for the bridge table entries, in seconds. The new value applies only to the entries that are dynamically learned after the new value is set. Previously existing bridge table entries expire after the previously configured time-out value.&lt;br>Default value: 300&lt;br>Minimum value = 60&lt;br>Maximum value = 300</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[UPDATE](#update) | [UNSET](#unset) | [GET (ALL)](#get-(all))


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###update



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/l2param
HTTP Method: PUT
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"l2param":{      "mbfpeermacupdate":<Double_value>,      "maxbridgecollision":<Double_value>,      "bdggrpproxyarp":<String_value>,      "bdgsetting":<String_value>,      "garponvridintf":<String_value>,      "macmodefwdmypkt":<String_value>,      "usemymac":<String_value>,      "proxyarp":<String_value>,      "garpreply":<String_value>,      "mbfinstlearning":<String_value>,      "rstintfonhafo":<String_value>,      "skipproxyingbsdtraffic":<String_value>,      "returntoethernetsender":<String_value>,      "stopmacmoveupdate":<String_value>,      "bridgeagetimeout":<Double_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/l2param?action=unset
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"l2param":{      "mbfpeermacupdate":true,      "maxbridgecollision":true,      "bdggrpproxyarp":true,      "bdgsetting":true,      "garponvridintf":true,      "macmodefwdmypkt":true,      "usemymac":true,      "proxyarp":true,      "garpreply":true,      "mbfinstlearning":true,      "rstintfonhafo":true,      "skipproxyingbsdtraffic":true,      "returntoethernetsender":true,      "stopmacmoveupdate":true,      "bridgeagetimeout":true}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/l2param
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "l2param": [ {      "maxbridgecollision":<Double_value>,      "mbfpeermacupdate":<Double_value>,      "bdggrpproxyarp":<String_value>,      "bdgsetting":<String_value>,      "garponvridintf":<String_value>,      "macmodefwdmypkt":<String_value>,      "usemymac":<String_value>,      "proxyarp":<String_value>,      "garpreply":<String_value>,      "mbfinstlearning":<String_value>,      "rstintfonhafo":<String_value>,      "skipproxyingbsdtraffic":<String_value>,      "returntoethernetsender":<String_value>,      "stopmacmoveupdate":<String_value>,      "bridgeagetimeout":<Double_value>}]}```



