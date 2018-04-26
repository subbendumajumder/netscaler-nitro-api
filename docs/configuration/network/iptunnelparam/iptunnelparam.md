#iptunnelparam

Configuration for ip tunnel parameter resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>srcip</td><td>&lt;String></td><td>Read-write</td><td>Common source-IP address for all tunnels. For a specific tunnel, this global setting is overridden if you have specified another source IP address. Must be a MIP or SNIP address.<br>Minimum length = 1</td></tr><tr><td>dropfrag</td><td>&lt;String></td><td>Read-write</td><td>Drop any IP packet that requires fragmentation before it is sent through the tunnel.<br>Default value: NO<br>Possible values = YES, NO</td></tr><tr><td>dropfragcputhreshold</td><td>&lt;Double></td><td>Read-write</td><td>Threshold value, as a percentage of CPU usage, at which to drop packets that require fragmentation to use the IP tunnel. Applies only if dropFragparameter is set to NO. The default value, 0, specifies that this parameter is not set.<br>Minimum value = 1<br>Maximum value = 100</td></tr><tr><td>srciproundrobin</td><td>&lt;String></td><td>Read-write</td><td>Use a different source IP address for each new session through a particular IP tunnel, as determined by round robin selection of one of the SNIP addresses. This setting is ignored if a common global source IP address has been specified for all the IP tunnels. This setting does not apply to a tunnel for which a source IP address has been specified.<br>Default value: NO<br>Possible values = YES, NO</td></tr><tr><td>enablestrictrx</td><td>&lt;String></td><td>Read-write</td><td>Strict PBR check for IPSec packets received through tunnel.<br>Default value: NO<br>Possible values = YES, NO</td></tr><tr><td>enablestricttx</td><td>&lt;String></td><td>Read-write</td><td>Strict PBR check for packets to be sent IPSec protected.<br>Default value: NO<br>Possible values = YES, NO</td></tr><tr><td>mac</td><td>&lt;String></td><td>Read-write</td><td>The shared MAC used for shared IP between cluster nodes/HA peers.</td></tr><tr><td>useclientsourceip</td><td>&lt;String></td><td>Read-write</td><td>Use client source IP as source IP for outer tunnel IP header.<br>Default value: NO<br>Possible values = YES, NO</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[UPDATE](#u)| [UNSET](#)| [GET (ALL)](#get-)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/iptunnelparam
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"iptunnelparam":{"srcip":<String_value>,"dropfrag":<String_value>,"dropfragcputhreshold":<Double_value>,"srciproundrobin":<String_value>,"enablestrictrx":<String_value>,"enablestricttx":<String_value>,"mac":<String_value>,"useclientsourceip":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/iptunnelparam?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"iptunnelparam":{"srcip":true,"dropfrag":true,"dropfragcputhreshold":true,"srciproundrobin":true,"enablestrictrx":true,"enablestricttx":true,"mac":true,"useclientsourceip":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/iptunnelparam
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "iptunnelparam": [ {"srcip":<String_value>,"dropfrag":<String_value>,"dropfragcputhreshold":<Double_value>,"srciproundrobin":<String_value>,"enablestrictrx":<String_value>,"enablestricttx":<String_value>,"mac":<String_value>,"useclientsourceip":<String_value>}]}```



