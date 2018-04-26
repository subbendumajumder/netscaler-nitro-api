#cacheparameter

Configuration for cache parameter resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>memlimit</td><td>&lt;Double></td><td>Read-write</td><td>Amount of memory available for storing the cache objects. In practice, the amount of memory available for caching can be less than half the total memory of the NetScaler appliance.</td></tr><tr><td>via</td><td>&lt;String></td><td>Read-write</td><td>String to include in the Via header. A Via header is inserted into all responses served from a content group if its Insert Via flag is set.<br>Minimum length = 1</td></tr><tr><td>verifyusing</td><td>&lt;String></td><td>Read-write</td><td>Criteria for deciding whether a cached object can be served for an incoming HTTP request. Available settings function as follows:<br>HOSTNAME - The URL, host name, and host port values in the incoming HTTP request header must match the cache policy. The IP address and the TCP port of the destination host are not evaluated. Do not use the HOSTNAME setting unless you are certain that no rogue client can access a rogue server through the cache. <br>HOSTNAME_AND_IP - The URL, host name, host port in the incoming HTTP request header, and the IP address and TCP port of<br>the destination server, must match the cache policy.<br>DNS - The URL, host name and host port in the incoming HTTP request, and the TCP port must match the cache policy. The host name is used for DNS lookup of the destination server's IP address, and is compared with the set of addresses returned by the DNS lookup.<br>Possible values = HOSTNAME, HOSTNAME_AND_IP, DNS</td></tr><tr><td>maxpostlen</td><td>&lt;Double></td><td>Read-write</td><td>Maximum number of POST body bytes to consider when evaluating parameters for a content group for which you have configured hit parameters and invalidation parameters.<br>Default value: 4096<br>Minimum value = 0<br>Maximum value = 131072</td></tr><tr><td>prefetchmaxpending</td><td>&lt;Double></td><td>Read-write</td><td>Maximum number of outstanding prefetches in the Integrated Cache.</td></tr><tr><td>enablebypass</td><td>&lt;String></td><td>Read-write</td><td>Evaluate the request-time policies before attempting hit selection. If set to NO, an incoming request for which a matching object is found in cache storage results in a response regardless of the policy configuration.<br>If the request matches a policy with a NOCACHE action, the request bypasses all cache processing. <br>This parameter does not affect processing of requests that match any invalidation policy.<br>Possible values = YES, NO</td></tr><tr><td>undefaction</td><td>&lt;String></td><td>Read-write</td><td>Action to take when a policy cannot be evaluated.<br>Possible values = NOCACHE, RESET</td></tr><tr><td>enablehaobjpersist</td><td>&lt;String></td><td>Read-write</td><td>The HA object persisting parameter. When this value is set to YES, cache objects can be synced to Secondary in a HA deployment. If set to NO, objects will never be synced to Secondary node.<br>Default value: NO<br>Possible values = YES, NO</td></tr><tr><td>disklimit</td><td>&lt;Double></td><td>Read-only</td><td>The disk limit for the Integrated Cache.</td></tr><tr><td>maxdisklimit</td><td>&lt;Double></td><td>Read-only</td><td>The maximum value of the memory limit for the Integrated Cache.</td></tr><tr><td>memlimitactive</td><td>&lt;Double></td><td>Read-only</td><td>Active value of the memory limit for the Integrated Cache.</td></tr><tr><td>maxmemlimit</td><td>&lt;Double></td><td>Read-only</td><td>The maximum value of the memory limit for the Integrated Cache.</td></tr><tr><td>prefetchcur</td><td>&lt;Double></td><td>Read-only</td><td>Number of current outstanding prefetches in the IC.</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[UPDATE](#u)| [UNSET](#)| [GET (ALL)](#get-)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/cacheparameter
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"cacheparameter":{"memlimit":<Double_value>,"via":<String_value>,"verifyusing":<String_value>,"maxpostlen":<Double_value>,"prefetchmaxpending":<Double_value>,"enablebypass":<String_value>,"undefaction":<String_value>,"enablehaobjpersist":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/cacheparameter?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"cacheparameter":{"memlimit":true,"via":true,"verifyusing":true,"maxpostlen":true,"prefetchmaxpending":true,"enablebypass":true,"undefaction":true,"enablehaobjpersist":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/cacheparameter
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "cacheparameter": [ {"disklimit":<Double_value>,"maxdisklimit":<Double_value>,"memlimit":<Double_value>,"memlimitactive":<Double_value>,"maxmemlimit":<Double_value>,"via":<String_value>,"verifyusing":<String_value>,"maxpostlen":<Double_value>,"prefetchcur":<Double_value>,"prefetchmaxpending":<Double_value>,"enablebypass":<String_value>,"undefaction":<String_value>,"enablehaobjpersist":<String_value>}]}```



