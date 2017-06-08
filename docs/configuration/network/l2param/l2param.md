#l2param

Configuration for Layer 2 related parameter resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>mbfpeermacupdate</td><td>&lt;Double></td><td>Read-write</td><td>When mbf_instant_learning is enabled, learn any changes in peers MAC after this time interval, which is in 10ms ticks.&lt;br>Default value: 10</td><tr><tr><td>maxbridgecollision</td><td>&lt;Double></td><td>Read-write</td><td>Maximum bridge collision for loop detection .&lt;br>Default value: 20</td><tr><tr><td>bdggrpproxyarp</td><td>&lt;String></td><td>Read-write</td><td>Set/reset proxy ARP in bridge group deployment.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>bdgsetting</td><td>&lt;String></td><td>Read-write</td><td>Bridging settings for C2C behavior.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>garponvridintf</td><td>&lt;String></td><td>Read-write</td><td>Send GARP messagess on VRID-configured interfaces upon failover .&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>macmodefwdmypkt</td><td>&lt;String></td><td>Read-write</td><td>MAC mode vserver forward packets destined to VIPs.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>usemymac</td><td>&lt;String></td><td>Read-write</td><td>Set/reset cfg_use_my_mac .&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>proxyarp</td><td>&lt;String></td><td>Read-write</td><td>Set/reset cfg_proxy_arp_dr .&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>garpreply</td><td>&lt;String></td><td>Read-write</td><td>Set/reset REPLY form of GARP .&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>mbfinstlearning</td><td>&lt;String></td><td>Read-write</td><td>Enable instant learning of MAC changes in MBF mode.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>rstintfonhafo</td><td>&lt;String></td><td>Read-write</td><td>Enable the reset interface upon HA failover.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>skipproxyingbsdtraffic</td><td>&lt;String></td><td>Read-write</td><td>Enable the proxying of FreeBSD traffic.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>returntoethernetsender</td><td>&lt;String></td><td>Read-write</td><td>Return to ethernet sender.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>stopmacmoveupdate</td><td>&lt;String></td><td>Read-write</td><td>Stop propagation of server mac change to natpcbs.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[UPDATE](#update) | [UNSET](#unset) | [GET (ALL)](#get-(all))


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","l2param":{      "mbfpeermacupdate":<Double_value>,      "maxbridgecollision":<Double_value>,      "bdggrpproxyarp":<String_value>,      "bdgsetting":<String_value>,      "garponvridintf":<String_value>,      "macmodefwdmypkt":<String_value>,      "usemymac":<String_value>,      "proxyarp":<String_value>,      "garpreply":<String_value>,      "mbfinstlearning":<String_value>,      "rstintfonhafo":<String_value>,      "skipproxyingbsdtraffic":<String_value>,      "returntoethernetsender":<String_value>,      "stopmacmoveupdate":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","l2param":{      "mbfpeermacupdate":true,      "maxbridgecollision":true,      "bdggrpproxyarp":true,      "bdgsetting":true,      "garponvridintf":true,      "macmodefwdmypkt":true,      "usemymac":true,      "proxyarp":true,      "garpreply":true,      "mbfinstlearning":true,      "rstintfonhafo":true,      "skipproxyingbsdtraffic":true,      "returntoethernetsender":true,      "stopmacmoveupdate":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/l2param
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "l2param": [ {      "maxbridgecollision":<Double_value>,      "mbfpeermacupdate":<Double_value>,      "bdggrpproxyarp":<String_value>,      "bdgsetting":<String_value>,      "garponvridintf":<String_value>,      "macmodefwdmypkt":<String_value>,      "usemymac":<String_value>,      "proxyarp":<String_value>,      "garpreply":<String_value>,      "mbfinstlearning":<String_value>,      "rstintfonhafo":<String_value>,      "skipproxyingbsdtraffic":<String_value>,      "returntoethernetsender":<String_value>,      "stopmacmoveupdate":<String_value>}]}```



