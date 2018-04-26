#server

Configuration for server resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the server. <br>Must begin with an ASCII alphabetic or underscore (_) character, and must contain only ASCII alphanumeric, underscore, hash (#), period (.), space, colon (:), at (@), equals (=), and hyphen (-) characters.<br>Can be changed after the name is created.<br>Minimum length = 1</td></tr><tr><td>ipaddress</td><td>&lt;String></td><td>Read-write</td><td>IPv4 or IPv6 address of the server. If you create an IP address based server, you can specify the name of the server, instead of its IP address, when creating a service. Note: If you do not create a server entry, the server IP address that you enter when you create a service becomes the name of the server.</td></tr><tr><td>domain</td><td>&lt;String></td><td>Read-write</td><td>Domain name of the server. For a domain based configuration, you must create the server first.<br>Minimum length = 1</td></tr><tr><td>translationip</td><td>&lt;String></td><td>Read-write</td><td>IP address used to transform the server's DNS-resolved IP address.</td></tr><tr><td>translationmask</td><td>&lt;String></td><td>Read-write</td><td>The netmask of the translation ip.</td></tr><tr><td>domainresolveretry</td><td>&lt;Integer></td><td>Read-write</td><td>Time, in seconds, for which the NetScaler appliance must wait, after DNS resolution fails, before sending the next DNS query to resolve the domain name.<br>Default value: 5<br>Minimum value = 5<br>Maximum value = 20939</td></tr><tr><td>state</td><td>&lt;String></td><td>Read-write</td><td>Initial state of the server.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>ipv6address</td><td>&lt;String></td><td>Read-write</td><td>Support IPv6 addressing mode. If you configure a server with the IPv6 addressing mode, you cannot use the server in the IPv4 addressing mode.<br>Default value: NO<br>Possible values = YES, NO</td></tr><tr><td>comment</td><td>&lt;String></td><td>Read-write</td><td>Any information about the server.</td></tr><tr><td>td</td><td>&lt;Double></td><td>Read-write</td><td>Integer value that uniquely identifies the traffic domain in which you want to configure the entity. If you do not specify an ID, the entity becomes part of the default traffic domain, which has an ID of 0.<br>Minimum value = 0<br>Maximum value = 4094</td></tr><tr><td>domainresolvenow</td><td>&lt;Boolean></td><td>Read-write</td><td>Immediately send a DNS query to resolve the server's domain name.</td></tr><tr><td>delay</td><td>&lt;Double></td><td>Read-write</td><td>Time, in seconds, after which all the services configured on the server are disabled.</td></tr><tr><td>graceful</td><td>&lt;String></td><td>Read-write</td><td>Shut down gracefully, without accepting any new connections, and disabling each service when all of its connections are closed.<br>Default value: NO<br>Possible values = YES, NO</td></tr><tr><td>Internal</td><td>&lt;Boolean></td><td>Read-write</td><td>Display names of the servers that have been created for internal use.</td></tr><tr><td>newname</td><td>&lt;String></td><td>Read-write</td><td>New name for the server. Must begin with an ASCII alphabetic or underscore (_) character, and must contain only ASCII alphanumeric, underscore, hash (#), period (.), space, colon (:), at (@), equals (=), and hyphen (-) characters.<br>Minimum length = 1</td></tr><tr><td>statechangetimesec</td><td>&lt;String></td><td>Read-only</td><td>Time when last state change happened. Seconds part.</td></tr><tr><td>tickssincelaststatechange</td><td>&lt;Double></td><td>Read-only</td><td>Time in 10 millisecond ticks since the last state change.</td></tr><tr><td>autoscale</td><td>&lt;String></td><td>Read-only</td><td>Auto scale option for a servicegroup.<br>Default value: DISABLED<br>Possible values = DISABLED, DNS, POLICY</td></tr><tr><td>usip</td><td>&lt;String></td><td>Read-only</td><td>Use the client's IP address as the source IP address when initiating a connection to the server. When creating a service, if you do not set this parameter, the service inherits the global Use Source IP setting (available in the enable ns mode and disable ns mode CLI commands, or in the System &gt; Settings &gt; Configure modes &gt; Configure Modes dialog box). However, you can override this setting after you create the service.<br>Possible values = YES, NO</td></tr><tr><td>cka</td><td>&lt;String></td><td>Read-only</td><td>Enable client keep-alive for the service group.<br>Possible values = YES, NO</td></tr><tr><td>tcpb</td><td>&lt;String></td><td>Read-only</td><td>Enable TCP buffering for the service group.<br>Possible values = YES, NO</td></tr><tr><td>cmp</td><td>&lt;String></td><td>Read-only</td><td>Enable compression for the specified service.<br>Possible values = YES, NO</td></tr><tr><td>cacheable</td><td>&lt;String></td><td>Read-only</td><td>Use the transparent cache redirection virtual server to forward the request to the cache server.<br>Default value: NO<br>Possible values = YES, NO</td></tr><tr><td>sc</td><td>&lt;String></td><td>Read-only</td><td>State of the SureConnect feature for the service group.<br>Default value: OFF<br>Possible values = ON, OFF</td></tr><tr><td>sp</td><td>&lt;String></td><td>Read-only</td><td>Enable surge protection for the service group.<br>Default value: OFF<br>Possible values = ON, OFF</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD]()| [DELETE](#d)| [UPDATE](#u)| [UNSET](#)| [ENABLE](#e)| [DISABLE](#di)| [RENAME](#r)| [GET (ALL)](#get-)| [GET]()| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/server
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"server":{<b>"name":<String_value>,</b>"ipaddress":<String_value>,"domain":<String_value>,"translationip":<String_value>,"translationmask":<String_value>,"domainresolveretry":<Integer_value>,"state":<String_value>,"ipv6address":<String_value>,"comment":<String_value>,"td":<Double_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/server/name_value&lt;String&gt;
<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/server
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"server":{<b>"name":<String_value>,</b>"ipaddress":<String_value>,"domainresolveretry":<Integer_value>,"translationip":<String_value>,"translationmask":<String_value>,"domainresolvenow":<Boolean_value>,"comment":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/server?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"server":{<b>"name":<String_value>,</b>"comment":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###enable



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/server?<b>action=enable</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"server":{<b>"name":<String_value></b>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###disable



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/server?<b>action=disable</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"server":{<b>"name":<String_value>,</b>"delay":<Double_value>,"graceful":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###rename



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/server?<b>action=rename</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"server":{<b>"name":<String_value>,</b><b>"newname":<String_value></b>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/server
<b>Query-parameters:</b>
<b>args</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/server?<b>args=name:&lt;String_value&gt;,Internal:&lt;Boolean_value&gt;</b>
Use this query-parameter to get server resources based on additional properties.


<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/server?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/server?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of server resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/server?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/server?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the server resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "server": [ {name:<String_value>,Internal:<Boolean_value>"ipaddress":<String_value>,"state":<String_value>,"domain":<String_value>,"domainresolveretry":<Integer_value>,"translationip":<String_value>,"translationmask":<String_value>,"comment":<String_value>,"statechangetimesec":<String_value>,"tickssincelaststatechange":<Double_value>,"ipv6address":<String_value>,"td":<Double_value>,"autoscale":<String_value>,"usip":<String_value>,"cka":<String_value>,"tcpb":<String_value>,"cmp":<String_value>,"cacheable":<String_value>,"sc":<String_value>,"sp":<String_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/server/name_value&lt;String&gt;
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/server/name_value&lt;String&gt;?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/server/name_value&lt;String&gt;?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "server": [ {name:<String_value>,Internal:<Boolean_value>"ipaddress":<String_value>,"state":<String_value>,"domain":<String_value>,"domainresolveretry":<Integer_value>,"translationip":<String_value>,"translationmask":<String_value>,"comment":<String_value>,"statechangetimesec":<String_value>,"tickssincelaststatechange":<Double_value>,"ipv6address":<String_value>,"td":<Double_value>,"autoscale":<String_value>,"usip":<String_value>,"cka":<String_value>,"tcpb":<String_value>,"cmp":<String_value>,"cacheable":<String_value>,"sc":<String_value>,"sp":<String_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/server?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "server": [ { "__count": "#no"} ] }```



