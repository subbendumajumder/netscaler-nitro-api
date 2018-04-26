#nstimeout

Configuration for timeout resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>zombie</td><td>&lt;Double></td><td>Read-write</td><td>Interval, in seconds, at which the NetScaler zombie cleanup process must run. This process cleans up inactive TCP connections.<br>Default value: 120<br>Minimum value = 1<br>Maximum value = 600</td></tr><tr><td>client</td><td>&lt;Double></td><td>Read-write</td><td>Client idle timeout (in seconds). If zero, the service-type default value is taken when service is created.<br>Default value: 0<br>Minimum value = 0<br>Maximum value = 18000</td></tr><tr><td>server</td><td>&lt;Double></td><td>Read-write</td><td>Server idle timeout (in seconds). If zero, the service-type default value is taken when service is created.<br>Default value: 0<br>Minimum value = 0<br>Maximum value = 18000</td></tr><tr><td>httpclient</td><td>&lt;Double></td><td>Read-write</td><td>Global idle timeout, in seconds, for client connections of HTTP service type. This value is over ridden by the client timeout that is configured on individual entities.<br>Default value: 0<br>Minimum value = 0<br>Maximum value = 18000</td></tr><tr><td>httpserver</td><td>&lt;Double></td><td>Read-write</td><td>Global idle timeout, in seconds, for server connections of HTTP service type. This value is over ridden by the server timeout that is configured on individual entities.<br>Default value: 0<br>Minimum value = 0<br>Maximum value = 18000</td></tr><tr><td>tcpclient</td><td>&lt;Double></td><td>Read-write</td><td>Global idle timeout, in seconds, for non-HTTP client connections of TCP service type. This value is over ridden by the client timeout that is configured on individual entities.<br>Default value: 0<br>Minimum value = 0<br>Maximum value = 18000</td></tr><tr><td>tcpserver</td><td>&lt;Double></td><td>Read-write</td><td>Global idle timeout, in seconds, for non-HTTP server connections of TCP service type. This value is over ridden by the server timeout that is configured on entities.<br>Default value: 0<br>Minimum value = 0<br>Maximum value = 18000</td></tr><tr><td>anyclient</td><td>&lt;Double></td><td>Read-write</td><td>Global idle timeout, in seconds, for non-TCP client connections. This value is over ridden by the client timeout that is configured on individual entities.<br>Default value: 0<br>Minimum value = 0<br>Maximum value = 31536000</td></tr><tr><td>anyserver</td><td>&lt;Double></td><td>Read-write</td><td>Global idle timeout, in seconds, for non TCP server connections. This value is over ridden by the server timeout that is configured on individual entities.<br>Default value: 0<br>Minimum value = 0<br>Maximum value = 31536000</td></tr><tr><td>anytcpclient</td><td>&lt;Double></td><td>Read-write</td><td>Global idle timeout, in seconds, for TCP client connections. This value takes precedence over entity level timeout settings (vserver/service). This is applicable only to transport protocol TCP.<br>Default value: 0<br>Minimum value = 0<br>Maximum value = 31536000</td></tr><tr><td>anytcpserver</td><td>&lt;Double></td><td>Read-write</td><td>Global idle timeout, in seconds, for TCP server connections. This value takes precedence over entity level timeout settings ( vserver/service). This is applicable only to transport protocol TCP.<br>Default value: 0<br>Minimum value = 0<br>Maximum value = 31536000</td></tr><tr><td>halfclose</td><td>&lt;Double></td><td>Read-write</td><td>Idle timeout, in seconds, for connections that are in TCP half-closed state.<br>Default value: 10<br>Minimum value = 1<br>Maximum value = 600</td></tr><tr><td>nontcpzombie</td><td>&lt;Double></td><td>Read-write</td><td>Interval at which the zombie clean-up process for non-TCP connections should run. Inactive IP NAT connections will be cleaned up.<br>Default value: 60<br>Minimum value = 1<br>Maximum value = 600</td></tr><tr><td>reducedfintimeout</td><td>&lt;Double></td><td>Read-write</td><td>Alternative idle timeout, in seconds, for closed TCP NATPCB connections.<br>Default value: 30<br>Minimum value = 1<br>Maximum value = 300</td></tr><tr><td>reducedrsttimeout</td><td>&lt;Double></td><td>Read-write</td><td>Timer interval, in seconds, for abruptly terminated TCP NATPCB connections.<br>Default value: 0<br>Minimum value = 0<br>Maximum value = 300</td></tr><tr><td>newconnidletimeout</td><td>&lt;Double></td><td>Read-write</td><td>Timer interval, in seconds, for new TCP NATPCB connections on which no data was received.<br>Default value: 4<br>Minimum value = 1<br>Maximum value = 120</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[UPDATE](#u)| [UNSET](#)| [GET (ALL)](#get-)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nstimeout
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"nstimeout":{"zombie":<Double_value>,"client":<Double_value>,"server":<Double_value>,"httpclient":<Double_value>,"httpserver":<Double_value>,"tcpclient":<Double_value>,"tcpserver":<Double_value>,"anyclient":<Double_value>,"anyserver":<Double_value>,"anytcpclient":<Double_value>,"anytcpserver":<Double_value>,"halfclose":<Double_value>,"nontcpzombie":<Double_value>,"reducedfintimeout":<Double_value>,"reducedrsttimeout":<Double_value>,"newconnidletimeout":<Double_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nstimeout?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"nstimeout":{"zombie":true,"client":true,"server":true,"httpclient":true,"httpserver":true,"tcpclient":true,"tcpserver":true,"anyclient":true,"anyserver":true,"anytcpclient":true,"anytcpserver":true,"halfclose":true,"nontcpzombie":true,"reducedfintimeout":true,"reducedrsttimeout":true,"newconnidletimeout":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nstimeout
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "nstimeout": [ {"zombie":<Double_value>,"client":<Double_value>,"server":<Double_value>,"httpclient":<Double_value>,"httpserver":<Double_value>,"tcpclient":<Double_value>,"tcpserver":<Double_value>,"anyclient":<Double_value>,"anyserver":<Double_value>,"halfclose":<Double_value>,"anytcpclient":<Double_value>,"anytcpserver":<Double_value>,"nontcpzombie":<Double_value>,"reducedfintimeout":<Double_value>,"reducedrsttimeout":<Double_value>,"newconnidletimeout":<Double_value>}]}```



