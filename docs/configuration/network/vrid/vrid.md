#vrid

Configuration for Virtual Router ID resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>&lt;Double></td><td>Read-write</td><td>Integer that uniquely identifies the VMAC address. The generic VMAC address is in the form of 00:00:5e:00:01:&lt;VRID&gt;. For example, if you add a VRID with a value of 60 and bind it to an interface, the resulting VMAC address is 00:00:5e:00:01:3c, where 3c is the hexadecimal representation of 60.<br>Minimum value = 1<br>Maximum value = 255</td></tr><tr><td>priority</td><td>&lt;Double></td><td>Read-write</td><td>Base priority (BP), in an active-active mode configuration, which ordinarily determines the master VIP address.<br>Default value: 255<br>Minimum value = 0<br>Maximum value = 255</td></tr><tr><td>preemption</td><td>&lt;String></td><td>Read-write</td><td>In an active-active mode configuration, make a backup VIP address the master if its priority becomes higher than that of a master VIP address bound to this VMAC address. <br>If you disable pre-emption while a backup VIP address is the master, the backup VIP address remains master until the original master VIP's priority becomes higher than that of the current master.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>sharing</td><td>&lt;String></td><td>Read-write</td><td>In an active-active mode configuration, enable the backup VIP address to process any traffic instead of dropping it.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>tracking</td><td>&lt;String></td><td>Read-write</td><td>The effective priority (EP) value, relative to the base priority (BP) value in an active-active mode configuration. When EP is set to a value other than None, it is EP, not BP, which determines the master VIP address.<br>Available settings function as follows:<br>* NONE - No tracking. EP = BP<br>* ALL - If the status of all virtual servers is UP, EP = BP. Otherwise, EP = 0.<br>* ONE - If the status of at least one virtual server is UP, EP = BP. Otherwise, EP = 0.<br>* PROGRESSIVE - If the status of all virtual servers is UP, EP = BP. If the status of all virtual servers is DOWN, EP = 0. Otherwise EP = BP (1 - K/N), where N is the total number of virtual servers associated with the VIP address and K is the number of virtual servers for which the status is DOWN.<br>Default: NONE.<br>Default value: NONE<br>Possible values = NONE, ONE, ALL, PROGRESSIVE</td></tr><tr><td>ownernode</td><td>&lt;Double></td><td>Read-write</td><td>In a cluster setup, assign a cluster node as the owner of this VMAC address for IP based VRRP configuration. If no owner is configured, owner node is displayed as ALL and one node is dynamically elected as the owner.<br>Minimum value = 0<br>Maximum value = 31</td></tr><tr><td>trackifnumpriority</td><td>&lt;Double></td><td>Read-write</td><td>Priority by which the Effective priority will be reduced if any of the tracked interfaces goes down in an active-active configuration.<br>Default value: 0<br>Minimum value = 1<br>Maximum value = 255</td></tr><tr><td>preemptiondelaytimer</td><td>&lt;Double></td><td>Read-write</td><td>Preemption delay time, in seconds, in an active-active configuration. If any high priority node will come in network, it will wait for these many seconds before becoming master.<br>Default value: 0<br>Minimum value = 1<br>Maximum value = 36000</td></tr><tr><td>all</td><td>&lt;Boolean></td><td>Read-write</td><td>Remove all the configured VMAC addresses from the NetScaler appliance.</td></tr><tr><td>ifaces</td><td>&lt;String></td><td>Read-only</td><td>Interfaces bound to this VRID.</td></tr><tr><td>type</td><td>&lt;String></td><td>Read-only</td><td>Indicates whether this VRID entry was added manually or dynamically. When you manually add a VRID entry, the value for this parameter is STATIC. Otherwise, it is DYNAMIC.<br>Possible values = STATIC, DYNAMIC</td></tr><tr><td>effectivepriority</td><td>&lt;Double></td><td>Read-only</td><td>The effective priority of this VRID.</td></tr><tr><td>flags</td><td>&lt;Double></td><td>Read-only</td><td>Flags.</td></tr><tr><td>ipaddress</td><td>&lt;String></td><td>Read-only</td><td>The IP address bound to the VRID.</td></tr><tr><td>state</td><td>&lt;Double></td><td>Read-only</td><td>State of this VRID.</td></tr><tr><td>operationalownernode</td><td>&lt;Double></td><td>Read-only</td><td>Run time owner node of the vrid.<br>Minimum value = 0<br>Maximum value = 31</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD]()| [DELETE](#d)| [UPDATE](#u)| [UNSET](#)| [GET (ALL)](#get-)| [GET]()| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vrid
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"vrid":{<b>"id":<Double_value>,</b>"priority":<Double_value>,"preemption":<String_value>,"sharing":<String_value>,"tracking":<String_value>,"ownernode":<Double_value>,"trackifnumpriority":<Double_value>,"preemptiondelaytimer":<Double_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vrid/id_value&lt;Double&gt;
<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vrid
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"vrid":{<b>"id":<Double_value>,</b>"priority":<Double_value>,"preemption":<String_value>,"sharing":<String_value>,"tracking":<String_value>,"ownernode":<Double_value>,"trackifnumpriority":<Double_value>,"preemptiondelaytimer":<Double_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vrid?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"vrid":{<b>"id":<Double_value>,</b>"priority":true,"preemption":true,"sharing":true,"tracking":true,"ownernode":true,"trackifnumpriority":true,"preemptiondelaytimer":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vrid
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vrid?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vrid?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of vrid resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vrid?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vrid?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the vrid resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "vrid": [ {"id":<Double_value>,"ifaces":<String_value>,"type":<String_value>,"priority":<Double_value>,"effectivepriority":<Double_value>,"preemption":<String_value>,"sharing":<String_value>,"tracking":<String_value>,"flags":<Double_value>,"ipaddress":<String_value>,"state":<Double_value>,"operationalownernode":<Double_value>,"ownernode":<Double_value>,"trackifnumpriority":<Double_value>,"preemptiondelaytimer":<Double_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vrid/id_value&lt;Double&gt;
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vrid/id_value&lt;Double&gt;?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vrid/id_value&lt;Double&gt;?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "vrid": [ {"id":<Double_value>,"ifaces":<String_value>,"type":<String_value>,"priority":<Double_value>,"effectivepriority":<Double_value>,"preemption":<String_value>,"sharing":<String_value>,"tracking":<String_value>,"flags":<Double_value>,"ipaddress":<String_value>,"state":<Double_value>,"operationalownernode":<Double_value>,"ownernode":<Double_value>,"trackifnumpriority":<Double_value>,"preemptiondelaytimer":<Double_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vrid?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "vrid": [ { "__count": "#no"} ] }```



