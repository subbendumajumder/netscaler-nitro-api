#subscriberparam

Configuration for Subscriber Params resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>keytype</td><td>&lt;String></td><td>Read-write</td><td>Type of subscriber key type IP or IPANDVLAN.<br>Default value: IP<br>Possible values = IP</td></tr><tr><td>interfacetype</td><td>&lt;String></td><td>Read-write</td><td>Subscriber Interface refers to Netscaler interaction with control plane protocols, RADIUS and GX.<br>Types of subscriber interface: NONE, RadiusOnly, RadiusAndGx, GxOnly.<br>NONE: Only static subscribers can be configured.<br>RadiusOnly: GX interface is absent. Subscriber information is obtained through RADIUS Accounting messages.<br>RadiusAndGx: Subscriber ID obtained through RADIUS Accounting is used to query PCRF. Subscriber information is obtained from both RADIUS and PCRF.<br>GxOnly: RADIUS interface is absent. Subscriber information is queried using Subscriber IP.<br><br>Default value: None<br>Possible values = None, RadiusOnly, RadiusAndGx, GxOnly</td></tr><tr><td>idlettl</td><td>&lt;Double></td><td>Read-write</td><td>q!Idle Timeout, in seconds, after which Netscaler will take an idleAction on a subscriber session (refer to 'idleAction' arguement in 'set subscriber param' for more details on idleAction). Any data-plane or control plane activity updates the idleTimeout on subscriber session. idleAction could be to 'just delete the session' or 'delete and CCR-T' (if PCRF is configured) or 'do not delete but send a CCR-U'. <br>Zero value disables the idle timeout. !.<br>Default value: 0<br>Minimum value = 0<br>Maximum value = 172800</td></tr><tr><td>idleaction</td><td>&lt;String></td><td>Read-write</td><td>q!Once idleTTL exprires on a subscriber session, Netscaler will take an idle action on that session. idleAction could be chosen from one of these ==&gt;<br>1. ccrTerminate: (default) send CCR-T to inform PCRF about session termination and delete the session. <br>2. delete: Just delete the subscriber session without informing PCRF.<br>3. ccrUpdate: Do not delete the session and instead send a CCR-U to PCRF requesting for an updated session. !.<br>Default value: ccrTerminate<br>Possible values = ccrTerminate, delete, ccrUpdate</td></tr><tr><td>ipv6prefixlookuplist</td><td>&lt;Double[]></td><td>Read-write</td><td>The ipv6PrefixLookupList should consist of all the ipv6 prefix lengths assigned to the UE's'.<br>Minimum value = 1<br>Maximum value = 128</td></tr><tr><td>builtin</td><td>&lt;String[]></td><td>Read-only</td><td>.<br>Possible values = MODIFIABLE, DELETABLE, IMMUTABLE, PARTITION_ALL</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[UPDATE](#u)| [UNSET](#)| [GET (ALL)](#get-)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/subscriberparam
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"subscriberparam":{"keytype":<String_value>,"interfacetype":<String_value>,"idlettl":<Double_value>,"idleaction":<String_value>,"ipv6prefixlookuplist":<Double[]_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/subscriberparam?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"subscriberparam":{"keytype":true,"interfacetype":true,"idlettl":true,"idleaction":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/subscriberparam
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "subscriberparam": [ {"keytype":<String_value>,"interfacetype":<String_value>,"idlettl":<Double_value>,"idleaction":<String_value>,"ipv6prefixlookuplist":<Double[]_value>,"builtin":<String[]_value>}]}```



