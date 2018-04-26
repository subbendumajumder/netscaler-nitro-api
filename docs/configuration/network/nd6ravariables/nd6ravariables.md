#nd6ravariables

Configuration for nd6 Router Advertisment configuration variables resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>vlan</td><td>&lt;Double></td><td>Read-write</td><td>The VLAN number.<br>Minimum value = 1<br>Maximum value = 4094</td></tr><tr><td>ceaserouteradv</td><td>&lt;String></td><td>Read-write</td><td>Cease router advertisements on this vlan.<br>Default value: NO<br>Possible values = YES, NO</td></tr><tr><td>sendrouteradv</td><td>&lt;String></td><td>Read-write</td><td>whether the router sends periodic RAs and responds to Router Solicitations.<br>Default value: NO<br>Possible values = YES, NO</td></tr><tr><td>srclinklayeraddroption</td><td>&lt;String></td><td>Read-write</td><td>Include source link layer address option in RA messages.<br>Default value: YES<br>Possible values = YES, NO</td></tr><tr><td>onlyunicastrtadvresponse</td><td>&lt;String></td><td>Read-write</td><td>Send only Unicast Router Advertisements in respond to Router Solicitations.<br>Default value: NO<br>Possible values = YES, NO</td></tr><tr><td>managedaddrconfig</td><td>&lt;String></td><td>Read-write</td><td>Value to be placed in the Managed address configuration flag field.<br>Default value: NO<br>Possible values = YES, NO</td></tr><tr><td>otheraddrconfig</td><td>&lt;String></td><td>Read-write</td><td>Value to be placed in the Other configuration flag field.<br>Default value: NO<br>Possible values = YES, NO</td></tr><tr><td>currhoplimit</td><td>&lt;Double></td><td>Read-write</td><td>Current Hop limit.<br>Default value: 64<br>Minimum value = 0<br>Maximum value = 255</td></tr><tr><td>maxrtadvinterval</td><td>&lt;Double></td><td>Read-write</td><td>Maximum time allowed between unsolicited multicast RAs, in seconds.<br>Default value: 600<br>Minimum value = 4<br>Maximum value = 1800</td></tr><tr><td>minrtadvinterval</td><td>&lt;Double></td><td>Read-write</td><td>Minimum time interval between RA messages, in seconds.<br>Default value: 198<br>Minimum value = 3<br>Maximum value = 1350</td></tr><tr><td>linkmtu</td><td>&lt;Double></td><td>Read-write</td><td>The Link MTU.<br>Default value: 0<br>Minimum value = 0<br>Maximum value = 1500</td></tr><tr><td>reachabletime</td><td>&lt;Double></td><td>Read-write</td><td>Reachable time, in milliseconds.<br>Default value: 0<br>Minimum value = 0<br>Maximum value = 3600000</td></tr><tr><td>retranstime</td><td>&lt;Double></td><td>Read-write</td><td>Retransmission time, in milliseconds.<br>Default value: 0</td></tr><tr><td>defaultlifetime</td><td>&lt;Integer></td><td>Read-write</td><td>Default life time, in seconds.<br>Default value: 1800<br>Minimum value = 0<br>Maximum value = 9000</td></tr><tr><td>lastrtadvtime</td><td>&lt;Double></td><td>Read-only</td><td>Last RA sent timestamp.</td></tr><tr><td>nextrtadvdelay</td><td>&lt;Double></td><td>Read-only</td><td>Next RA delay.</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[UPDATE](#u)| [UNSET](#)| [GET (ALL)](#get-)| [GET]()| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nd6ravariables
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"nd6ravariables":{<b>"vlan":<Double_value>,</b>"ceaserouteradv":<String_value>,"sendrouteradv":<String_value>,"srclinklayeraddroption":<String_value>,"onlyunicastrtadvresponse":<String_value>,"managedaddrconfig":<String_value>,"otheraddrconfig":<String_value>,"currhoplimit":<Double_value>,"maxrtadvinterval":<Double_value>,"minrtadvinterval":<Double_value>,"linkmtu":<Double_value>,"reachabletime":<Double_value>,"retranstime":<Double_value>,"defaultlifetime":<Integer_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nd6ravariables?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"nd6ravariables":{<b>"vlan":<Double_value>,</b>"ceaserouteradv":true,"sendrouteradv":true,"srclinklayeraddroption":true,"onlyunicastrtadvresponse":true,"managedaddrconfig":true,"otheraddrconfig":true,"currhoplimit":true,"maxrtadvinterval":true,"minrtadvinterval":true,"linkmtu":true,"reachabletime":true,"retranstime":true,"defaultlifetime":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nd6ravariables
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nd6ravariables?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nd6ravariables?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of nd6ravariables resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nd6ravariables?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nd6ravariables?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the nd6ravariables resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "nd6ravariables": [ {"vlan":<Double_value>,"ceaserouteradv":<String_value>,"sendrouteradv":<String_value>,"srclinklayeraddroption":<String_value>,"onlyunicastrtadvresponse":<String_value>,"managedaddrconfig":<String_value>,"otheraddrconfig":<String_value>,"currhoplimit":<Double_value>,"maxrtadvinterval":<Double_value>,"minrtadvinterval":<Double_value>,"linkmtu":<Double_value>,"reachabletime":<Double_value>,"retranstime":<Double_value>,"defaultlifetime":<Integer_value>,"lastrtadvtime":<Double_value>,"nextrtadvdelay":<Double_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nd6ravariables/vlan_value&lt;Double&gt;
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nd6ravariables/vlan_value&lt;Double&gt;?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nd6ravariables/vlan_value&lt;Double&gt;?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "nd6ravariables": [ {"vlan":<Double_value>,"ceaserouteradv":<String_value>,"sendrouteradv":<String_value>,"srclinklayeraddroption":<String_value>,"onlyunicastrtadvresponse":<String_value>,"managedaddrconfig":<String_value>,"otheraddrconfig":<String_value>,"currhoplimit":<Double_value>,"maxrtadvinterval":<Double_value>,"minrtadvinterval":<Double_value>,"linkmtu":<Double_value>,"reachabletime":<Double_value>,"retranstime":<Double_value>,"defaultlifetime":<Integer_value>,"lastrtadvtime":<Double_value>,"nextrtadvdelay":<Double_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nd6ravariables?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "nd6ravariables": [ { "__count": "#no"} ] }```



