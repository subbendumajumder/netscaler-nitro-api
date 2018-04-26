#rnat

Configuration for RNAT configured route resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>network</td><td>&lt;String></td><td>Read-write</td><td>The network address defined for the RNAT entry.<br>Minimum length = 1</td></tr><tr><td>netmask</td><td>&lt;String></td><td>Read-write</td><td>The subnet mask for the network address.<br>Minimum length = 1</td></tr><tr><td>aclname</td><td>&lt;String></td><td>Read-write</td><td>An extended ACL defined for the RNAT entry.<br>Minimum length = 1</td></tr><tr><td>redirectport</td><td>&lt;Boolean></td><td>Read-write</td><td>The port number to which the packets are redirected.</td></tr><tr><td>natip</td><td>&lt;String></td><td>Read-write</td><td>The NAT IP address defined for the RNAT entry. .<br>Minimum length = 1</td></tr><tr><td>td</td><td>&lt;Double></td><td>Read-write</td><td>Integer value that uniquely identifies the traffic domain in which you want to configure the entity. If you do not specify an ID, the entity becomes part of the default traffic domain, which has an ID of 0.<br>Minimum value = 0<br>Maximum value = 4094</td></tr><tr><td>ownergroup</td><td>&lt;String></td><td>Read-write</td><td>The owner node group in a Cluster for this rnat rule.<br>Default value: DEFAULT_NG<br>Minimum length = 1</td></tr><tr><td>natip2</td><td>&lt;String></td><td>Read-write</td><td>The NAT IP(s) assigned to the RNAT.<br>Minimum length = 1</td></tr><tr><td>srcippersistency</td><td>&lt;String></td><td>Read-write</td><td>Enables the NetScaler appliance to use the same NAT IP address for all RNAT sessions initiated from a particular server.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>useproxyport</td><td>&lt;String></td><td>Read-write</td><td>Enable source port proxying, which enables the NetScaler appliance to use the RNAT ips using proxied source port.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>connfailover</td><td>&lt;String></td><td>Read-write</td><td>Synchronize connection information with the secondary appliance in a high availability (HA) pair. That is, synchronize all connection-related information for the RNAT session. In order for this to work, tcpproxy should be DISABLED. To disable tcpproxy use "set rnatparam tcpproxy DISABLED".<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[CLEAR](#)| [UPDATE](#u)| [UNSET](#)| [GET (ALL)](#get-)| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###clear



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/rnat?<b>action=clear</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"rnat":{"network":<String_value>,"netmask":<String_value>,"aclname":<String_value>,"redirectport":<Boolean_value>,"natip":<String_value>,"td":<Double_value>,"ownergroup":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/rnat
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"rnat":{"network":<String_value>,"netmask":<String_value>,"natip":<String_value>,"td":<Double_value>,"aclname":<String_value>,"redirectport":<Boolean_value>,"natip2":<String_value>,"srcippersistency":<String_value>,"useproxyport":<String_value>,"ownergroup":<String_value>,"connfailover":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/rnat?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"rnat":{"network":true,"netmask":true,"td":true,"aclname":true,"redirectport":true,"natip":true,"srcippersistency":true,"ownergroup":true,"useproxyport":true,"connfailover":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/rnat
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/rnat?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/rnat?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of rnat resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/rnat?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/rnat?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the rnat resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "rnat": [ {"network":<String_value>,"netmask":<String_value>,"td":<Double_value>,"natip":<String_value>,"aclname":<String_value>,"redirectport":<Boolean_value>,"srcippersistency":<String_value>,"useproxyport":<String_value>,"ownergroup":<String_value>,"connfailover":<String_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/rnat?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "rnat": [ { "__count": "#no"} ] }```



