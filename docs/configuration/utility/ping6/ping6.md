#ping6

Configuration for 0 resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>b</td><td>&lt;Double></td><td>Read-write</td><td>Set socket buffer size. If used, should be used with roughly +100 then the datalen (-s option). The default value is 8192.<br>Minimum value = 132<br>Maximum value = 131071</td></tr><tr><td>c</td><td>&lt;Double></td><td>Read-write</td><td>Number of packets to send. The default value is infinite. For Nitro API, defalut value is taken as 5.<br>Minimum value = 1<br>Maximum value = 65535</td></tr><tr><td>i</td><td>&lt;Double></td><td>Read-write</td><td>Waiting time, in seconds. The default value is 1 second.<br>Minimum value = 0<br>Maximum value = 65535</td></tr><tr><td>I</td><td>&lt;String></td><td>Read-write</td><td>Network interface on which to ping, if you have multiple interfaces.<br>Minimum length = 1<br>Maximum length = 15</td></tr><tr><td>m</td><td>&lt;Boolean></td><td>Read-write</td><td>By default, ping6 asks the kernel to fragment packets to fit into the minimum IPv6 MTU.The -m option will suppress the behavior for unicast packets.</td></tr><tr><td>n</td><td>&lt;Boolean></td><td>Read-write</td><td>Numeric output only. No name resolution.</td></tr><tr><td>p</td><td>&lt;String></td><td>Read-write</td><td>Pattern to fill in packets. Can be up to 16 bytes, useful for diagnosing data-dependent problems.<br>Minimum length = 1<br>Maximum length = 32</td></tr><tr><td>q</td><td>&lt;Boolean></td><td>Read-write</td><td>Quiet output. Only summary is printed. For Nitro API, this flag is set by default.</td></tr><tr><td>s</td><td>&lt;Double></td><td>Read-write</td><td>Data size, in bytes. The default value is 32.<br>Minimum value = 0<br>Maximum value = 65527</td></tr><tr><td>V</td><td>&lt;Double></td><td>Read-write</td><td>VLAN ID for link local address.<br>Minimum value = 1<br>Maximum value = 4094</td></tr><tr><td>S</td><td>&lt;String></td><td>Read-write</td><td>Source IP address to be used in the outgoing query packets.<br>Minimum length = 1</td></tr><tr><td>T</td><td>&lt;Double></td><td>Read-write</td><td>Traffic Domain Id.<br>Minimum value = 1<br>Maximum value = 4094</td></tr><tr><td>t</td><td>&lt;Double></td><td>Read-write</td><td>Timeout in seconds before ping6 exits.</td></tr><tr><td>hostName</td><td>&lt;String></td><td>Read-write</td><td>Address of host to ping.<br>Minimum length = 1<br>Maximum length = 256</td></tr><tr><td>response</td><td>&lt;String></td><td>Read-only</td><td>.</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[PING6](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###Ping6



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/ping6
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"ping6":{"b":<Double_value>,"c":<Double_value>,"i":<Double_value>,"I":<String_value>,"m":<Boolean_value>,"n":<Boolean_value>,"p":<String_value>,"q":<Boolean_value>,"s":<Double_value>,"V":<Double_value>,"S":<String_value>,"T":<Double_value>,"t":<Double_value>,<b>"hostName":<String_value></b>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Payload: </b>```{ "ping6": [ {"response":<String_value>}]}```



