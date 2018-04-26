#traceroute

Configuration for 0 resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>S</td><td>&lt;Boolean></td><td>Read-write</td><td>Print a summary of how many probes were not answered for each hop.</td></tr><tr><td>n</td><td>&lt;Boolean></td><td>Read-write</td><td>Print hop addresses numerically instead of symbolically and numerically.</td></tr><tr><td>r</td><td>&lt;Boolean></td><td>Read-write</td><td>Bypass normal routing tables and send directly to a host on an attached network. If the host is not on a directly attached network, an error is returned.</td></tr><tr><td>v</td><td>&lt;Boolean></td><td>Read-write</td><td>Verbose output. List received ICMP packets other than TIME_EXCEEDED and UNREACHABLE.</td></tr><tr><td>M</td><td>&lt;Double></td><td>Read-write</td><td>Minimum TTL value used in outgoing probe packets.<br>Default value: 1<br>Minimum value = 1<br>Maximum value = 255</td></tr><tr><td>m</td><td>&lt;Integer></td><td>Read-write</td><td>Maximum TTL value used in outgoing probe packets. For Nitro API, default value is taken as 10.<br>Default value: 64<br>Minimum value = 1<br>Maximum value = 255</td></tr><tr><td>P</td><td>&lt;String></td><td>Read-write</td><td>Send packets of specified IP protocol. The currently supported protocols are UDP and ICMP.<br>Minimum length = 1<br>Maximum length = 20</td></tr><tr><td>p</td><td>&lt;Integer></td><td>Read-write</td><td>Base port number used in probes.<br>Default value: 33434<br>Minimum value = 1<br>Maximum value = 65535</td></tr><tr><td>q</td><td>&lt;Integer></td><td>Read-write</td><td>Number of queries per hop. For Nitro API, defalut value is taken as 1.<br>Default value: 3<br>Minimum value = 1<br>Maximum value = 65535</td></tr><tr><td>s</td><td>&lt;String></td><td>Read-write</td><td>Source IP address to use in the outgoing query packets. If the IP address does not belong to this appliance, an error is returned and nothing is sent.<br>Minimum length = 1</td></tr><tr><td>T</td><td>&lt;Double></td><td>Read-write</td><td>Traffic Domain Id.<br>Minimum value = 1<br>Maximum value = 4094</td></tr><tr><td>t</td><td>&lt;Integer></td><td>Read-write</td><td>Type-of-service in query packets.<br>Minimum value = 0<br>Maximum value = 255</td></tr><tr><td>w</td><td>&lt;Integer></td><td>Read-write</td><td>Time (in seconds) to wait for a response to a query. For Nitro API, defalut value is set to 3.<br>Default value: 5<br>Minimum value = 2<br>Maximum value = 86399</td></tr><tr><td>host</td><td>&lt;String></td><td>Read-write</td><td>Destination host IP address or name.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>packetlen</td><td>&lt;Integer></td><td>Read-write</td><td>Length (in bytes) of the query packets.<br>Default value: 44<br>Minimum value = 44<br>Maximum value = 32768</td></tr><tr><td>response</td><td>&lt;String></td><td>Read-only</td><td>.</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[TRACEROUTE](#trace)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###Traceroute



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/traceroute
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"traceroute":{"S":<Boolean_value>,"n":<Boolean_value>,"r":<Boolean_value>,"v":<Boolean_value>,"M":<Double_value>,"m":<Integer_value>,"P":<String_value>,"p":<Integer_value>,"q":<Integer_value>,"s":<String_value>,"T":<Double_value>,"t":<Integer_value>,"w":<Integer_value>,<b>"host":<String_value>,</b>"packetlen":<Integer_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Payload: </b>```{ "traceroute": [ {"response":<String_value>}]}```



