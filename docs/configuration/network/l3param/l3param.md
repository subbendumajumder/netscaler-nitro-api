#l3param

Configuration for Layer 3 related parameter resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>srcnat</td><td>&lt;String></td><td>Read-write</td><td>Perform NAT if only the source is in the private network.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>icmpgenratethreshold</td><td>&lt;Double></td><td>Read-write</td><td>NS generated ICMP pkts per 10ms rate threshold.<br>Default value: 100</td></tr><tr><td>overridernat</td><td>&lt;String></td><td>Read-write</td><td>USNIP/USIP settings override RNAT settings for configured<br>service/virtual server traffic.. .<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>dropdfflag</td><td>&lt;String></td><td>Read-write</td><td>Enable dropping the IP DF flag.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>miproundrobin</td><td>&lt;String></td><td>Read-write</td><td>Enable round robin usage of mapped IPs.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>externalloopback</td><td>&lt;String></td><td>Read-write</td><td>Enable external loopback.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>tnlpmtuwoconn</td><td>&lt;String></td><td>Read-write</td><td>Enable/Disable learning PMTU of IP tunnel when ICMP error does not contain connection information.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>usipserverstraypkt</td><td>&lt;String></td><td>Read-write</td><td>Enable detection of stray server side pkts in USIP mode.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>forwardicmpfragments</td><td>&lt;String></td><td>Read-write</td><td>Enable forwarding of ICMP fragments.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>dropipfragments</td><td>&lt;String></td><td>Read-write</td><td>Enable dropping of IP fragments.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>acllogtime</td><td>&lt;Double></td><td>Read-write</td><td>Parameter to tune acl logging time.<br>Default value: 5000</td></tr><tr><td>implicitaclallow</td><td>&lt;String></td><td>Read-write</td><td>Do not apply ACLs for internal ports.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>dynamicrouting</td><td>&lt;String></td><td>Read-write</td><td>Enable/Disable Dynamic routing on partition.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>ipv6dynamicrouting</td><td>&lt;String></td><td>Read-write</td><td>Enable/Disable IPv6 Dynamic routing on partition.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[UPDATE](#u)| [UNSET](#)| [GET (ALL)](#get-)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/l3param
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"l3param":{"srcnat":<String_value>,"icmpgenratethreshold":<Double_value>,"overridernat":<String_value>,"dropdfflag":<String_value>,"miproundrobin":<String_value>,"externalloopback":<String_value>,"tnlpmtuwoconn":<String_value>,"usipserverstraypkt":<String_value>,"forwardicmpfragments":<String_value>,"dropipfragments":<String_value>,"acllogtime":<Double_value>,"implicitaclallow":<String_value>,"dynamicrouting":<String_value>,"ipv6dynamicrouting":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/l3param?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"l3param":{"srcnat":true,"icmpgenratethreshold":true,"overridernat":true,"dropdfflag":true,"miproundrobin":true,"externalloopback":true,"tnlpmtuwoconn":true,"usipserverstraypkt":true,"forwardicmpfragments":true,"dropipfragments":true,"acllogtime":true,"implicitaclallow":true,"dynamicrouting":true,"ipv6dynamicrouting":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/l3param
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "l3param": [ {"srcnat":<String_value>,"icmpgenratethreshold":<Double_value>,"overridernat":<String_value>,"dropdfflag":<String_value>,"miproundrobin":<String_value>,"externalloopback":<String_value>,"tnlpmtuwoconn":<String_value>,"usipserverstraypkt":<String_value>,"forwardicmpfragments":<String_value>,"dropipfragments":<String_value>,"acllogtime":<Double_value>,"implicitaclallow":<String_value>,"dynamicrouting":<String_value>,"ipv6dynamicrouting":<String_value>}]}```



