#urlfilteringparameter

Configuration for URLFILTERING paramter resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>hoursbetweendbupdates</td><td>&lt;Double></td><td>Read-write</td><td>URL Filtering hours between DB updates.<br>Minimum value = 0<br>Maximum value = 720</td></tr><tr><td>timeofdaytoupdatedb</td><td>&lt;String></td><td>Read-write</td><td>URL Filtering time of day to update DB.</td></tr><tr><td>localdatabasethreads</td><td>&lt;Double></td><td>Read-write</td><td>URL Filtering Local DB number of threads.<br>Minimum value = 1<br>Maximum value = 4</td></tr><tr><td>maxnumberofcloudthreads</td><td>&lt;Double></td><td>Read-only</td><td>URL Filtering hours between DB updates.<br>Minimum value = 1<br>Maximum value = 128</td></tr><tr><td>cloudkeepalivetimeout</td><td>&lt;Double></td><td>Read-only</td><td>URL Filtering Cloud keep alive timeout in msec.<br>Minimum value = 1000<br>Maximum value = 600000</td></tr><tr><td>cloudserverconnecttimeout</td><td>&lt;Double></td><td>Read-only</td><td>URL Filtering Cloud server connect timeout in msec.<br>Minimum value = 1000<br>Maximum value = 600000</td></tr><tr><td>clouddblookuptimeout</td><td>&lt;Double></td><td>Read-only</td><td>URL Filtering CloudDB send/receive timeout in msec.<br>Minimum value = 1000<br>Maximum value = 600000</td></tr><tr><td>proxyhostip</td><td>&lt;String></td><td>Read-only</td><td>URL Filtering Cloud Proxy HostIp.<br>Minimum length = 1</td></tr><tr><td>proxyport</td><td>&lt;Double></td><td>Read-only</td><td>URL Filtering Cloud Proxy Port.</td></tr><tr><td>proxyusername</td><td>&lt;String></td><td>Read-only</td><td>URL Filtering Cloud Proxy Username.<br>Minimum length = 1</td></tr><tr><td>proxypassword</td><td>&lt;String></td><td>Read-only</td><td>URL Filtering Cloud Proxy Password.<br>Minimum length = 1</td></tr><tr><td>seeddbsizelevel</td><td>&lt;Double></td><td>Read-only</td><td>URL Filtering Seed DB Size Level to get downloaded.<br>Minimum value = 1<br>Maximum value = 5</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[UPDATE](#u)| [UNSET](#)| [GET (ALL)](#get-)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/urlfilteringparameter
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Request Payload: </b>
<b>Response:</b>
HTTP Status Code on Success: 200 OK


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/urlfilteringparameter?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Request Payload: </b>
<b>Response:</b>
HTTP Status Code on Success: 200 OK


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/urlfilteringparameter
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OK

Content-Type:application/json

<b>Response Payload: </b>


