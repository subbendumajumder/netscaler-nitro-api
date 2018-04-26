#pcpmap

Configuration for server resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>nattype</td><td>&lt;String></td><td>Read-write</td><td>Type of sessions to be displayed.<br>Default value: NAT44<br>Possible values = NAT44, DS-Lite, NAT64</td></tr><tr><td>pcpsrcip</td><td>&lt;String></td><td>Read-only</td><td>Internal IP address.</td></tr><tr><td>subscrip</td><td>&lt;String></td><td>Read-only</td><td>IPV4 src address of Client in DS-Lite.</td></tr><tr><td>pcpsrcport</td><td>&lt;Integer></td><td>Read-only</td><td>Internal Port.<br>Range 1 - 65535<br>* in CLI is represented as 65535 in NITRO API</td></tr><tr><td>pcpdstip</td><td>&lt;String></td><td>Read-only</td><td>Remote PEER IP address.</td></tr><tr><td>pcpdstport</td><td>&lt;Integer></td><td>Read-only</td><td>Remote PEER Port.<br>Range 1 - 65535<br>* in CLI is represented as 65535 in NITRO API</td></tr><tr><td>pcpnatip</td><td>&lt;String></td><td>Read-only</td><td>External IP address.</td></tr><tr><td>pcpnatport</td><td>&lt;Integer></td><td>Read-only</td><td>External Port Number.<br>Range 1 - 65535<br>* in CLI is represented as 65535 in NITRO API</td></tr><tr><td>pcpprotocol</td><td>&lt;String></td><td>Read-only</td><td>Protocol of the PCP mapping.<br>Possible values = HopOpt, icmp, igmp, ggp, ipv4, st, tcp, udp</td></tr><tr><td>pcpaddr</td><td>&lt;Double></td><td>Read-only</td><td>Address of PCP Map entity.</td></tr><tr><td>pcpnounce</td><td>&lt;Double></td><td>Read-only</td><td>PCP Mapping Nounce.</td></tr><tr><td>pcprefcnt</td><td>&lt;Double></td><td>Read-only</td><td>Refcount, which indicates how many session is active.</td></tr><tr><td>pcplifetime</td><td>&lt;Double></td><td>Read-only</td><td>Integer value that shows the requested lifetime.</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[GET (ALL)](#get-)| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/pcpmap
<b>Query-parameters:</b>
<b>args</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/pcpmap?<b>args=nattype:&lt;String_value&gt;</b>
Use this query-parameter to get pcpmap resources based on additional properties.


<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/pcpmap?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/pcpmap?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of pcpmap resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/pcpmap?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/pcpmap?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the pcpmap resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "pcpmap": [ {nattype:<String_value>"pcpsrcip":<String_value>,"subscrip":<String_value>,"pcpsrcport":<Integer_value>,"pcpdstip":<String_value>,"pcpdstport":<Integer_value>,"pcpnatip":<String_value>,"pcpnatport":<Integer_value>,"pcpprotocol":<String_value>,"pcpaddr":<Double_value>,"pcpnounce":<Double_value>,"pcprefcnt":<Double_value>,"pcplifetime":<Double_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/pcpmap?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "pcpmap": [ { "__count": "#no"} ] }```



