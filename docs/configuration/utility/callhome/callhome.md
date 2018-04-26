#callhome

Configuration for callhome resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>mode</td><td>&lt;String></td><td>Read-write</td><td>CallHome mode of operation.<br>Default value: Default<br>Possible values = Default, CSP</td></tr><tr><td>emailaddress</td><td>&lt;String></td><td>Read-write</td><td>Email address of the contact administrator.<br>Maximum length = 78</td></tr><tr><td>hbcustominterval</td><td>&lt;Double></td><td>Read-write</td><td>Interval (in days) between CallHome heartbeats.<br>Default value: 30<br>Minimum value = 1<br>Maximum value = 30</td></tr><tr><td>proxymode</td><td>&lt;String></td><td>Read-write</td><td>Enables or disables the proxy mode. The proxy server can be set by either specifying the IP address of the server or the name of the service representing the proxy server.<br>Default value: NO<br>Possible values = YES, NO</td></tr><tr><td>ipaddress</td><td>&lt;String></td><td>Read-write</td><td>IP address of the proxy server.<br>Minimum length = 1</td></tr><tr><td>proxyauthservice</td><td>&lt;String></td><td>Read-write</td><td>Name of the service that represents the proxy server.<br>Maximum length = 128</td></tr><tr><td>port</td><td>&lt;Integer></td><td>Read-write</td><td>HTTP port on the Proxy server. This is a mandatory parameter for both IP address and service name based configuration.<br>Minimum value = 1<br>Range 1 - 65535<br>* in CLI is represented as 65535 in NITRO API</td></tr><tr><td>sslcardfirstfailure</td><td>&lt;String></td><td>Read-only</td><td>First occurrence SSL card failure.</td></tr><tr><td>sslcardlatestfailure</td><td>&lt;String></td><td>Read-only</td><td>Latest occurrence SSL card failure.</td></tr><tr><td>powfirstfail</td><td>&lt;String></td><td>Read-only</td><td>First occurrence power supply unit failure.</td></tr><tr><td>powlatestfailure</td><td>&lt;String></td><td>Read-only</td><td>Latest occurrence power supply unit failure.</td></tr><tr><td>hddfirstfail</td><td>&lt;String></td><td>Read-only</td><td>First occurrence hard disk drive failure.</td></tr><tr><td>hddlatestfailure</td><td>&lt;String></td><td>Read-only</td><td>Latest occurrence hard disk drive failure.</td></tr><tr><td>flashfirstfail</td><td>&lt;String></td><td>Read-only</td><td>First occurrence compact flash failure.</td></tr><tr><td>flashlatestfailure</td><td>&lt;String></td><td>Read-only</td><td>Latest occurrence compact flush failure.</td></tr><tr><td>rlfirsthighdrop</td><td>&lt;String></td><td>Read-only</td><td>First occurence of high rate limit drops.</td></tr><tr><td>rllatesthighdrop</td><td>&lt;String></td><td>Read-only</td><td>Latest occurence of high rate limit drops.</td></tr><tr><td>restartlatestfail</td><td>&lt;String></td><td>Read-only</td><td>Latest occurrence warm restart failure.</td></tr><tr><td>memthrefirstanomaly</td><td>&lt;String></td><td>Read-only</td><td>First occurrence of memory anomaly.</td></tr><tr><td>memthrelatestanomaly</td><td>&lt;String></td><td>Read-only</td><td>Latest occurrence of memory anomaly.</td></tr><tr><td>callhomestatus</td><td>&lt;String[]></td><td>Read-only</td><td>Callhome feature enabled/disable, register with upload server successful/failed.<br>Possible values = ENABLED, DISABLED, SUCCESSFUL, FAILED, INVALID HOSTNAME, NO DNSSERVER, HOSTNAME RESOLUTION FAILED</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[UPDATE](#u)| [UNSET](#)| [GET (ALL)](#get-)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/callhome
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"callhome":{"mode":<String_value>,"emailaddress":<String_value>,"hbcustominterval":<Double_value>,"proxymode":<String_value>,"ipaddress":<String_value>,"proxyauthservice":<String_value>,"port":<Integer_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/callhome?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"callhome":{"mode":true,"emailaddress":true,"hbcustominterval":true,"proxymode":true,"ipaddress":true,"proxyauthservice":true,"port":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/callhome
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "callhome": [ {"mode":<String_value>,"emailaddress":<String_value>,"hbcustominterval":<Double_value>,"proxymode":<String_value>,"ipaddress":<String_value>,"port":<Integer_value>,"proxyauthservice":<String_value>,"sslcardfirstfailure":<String_value>,"sslcardlatestfailure":<String_value>,"powfirstfail":<String_value>,"powlatestfailure":<String_value>,"hddfirstfail":<String_value>,"hddlatestfailure":<String_value>,"flashfirstfail":<String_value>,"flashlatestfailure":<String_value>,"rlfirsthighdrop":<String_value>,"rllatesthighdrop":<String_value>,"restartlatestfail":<String_value>,"memthrefirstanomaly":<String_value>,"memthrelatestanomaly":<String_value>,"callhomestatus":<String[]_value>}]}```



