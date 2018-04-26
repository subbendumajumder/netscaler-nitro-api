#vserver

Configuration for virtual server resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>The name of the virtual server to be removed.<br>Minimum length = 1</td></tr><tr><td>backupvserver</td><td>&lt;String></td><td>Read-write</td><td>The name of the backup virtual server for this virtual server.<br>Minimum length = 1</td></tr><tr><td>redirecturl</td><td>&lt;String></td><td>Read-write</td><td>The URL where traffic is redirected if the virtual server in the system becomes unavailable.<br>Minimum length = 1</td></tr><tr><td>cacheable</td><td>&lt;String></td><td>Read-write</td><td>Use this option to specify whether a virtual server (used for load balancing or content switching) routes requests to the cache redirection virtual server before sending it to the configured servers.<br>Possible values = YES, NO</td></tr><tr><td>clttimeout</td><td>&lt;Double></td><td>Read-write</td><td>The timeout value in seconds for idle client connection.<br>Minimum value = 0<br>Maximum value = 31536000</td></tr><tr><td>somethod</td><td>&lt;String></td><td>Read-write</td><td>The spillover factor. The system will use this value to determine if it should send traffic to the backupvserver when the main virtual server reaches the spillover threshold.<br>Possible values = CONNECTION, DYNAMICCONNECTION, BANDWIDTH, HEALTH, NONE</td></tr><tr><td>sopersistence</td><td>&lt;String></td><td>Read-write</td><td>The state of the spillover persistence.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>sopersistencetimeout</td><td>&lt;Double></td><td>Read-write</td><td>The spillover persistence entry timeout.<br>Default value: 2<br>Minimum value = 2<br>Maximum value = 1440</td></tr><tr><td>sothreshold</td><td>&lt;Double></td><td>Read-write</td><td>The spillver threshold value.<br>Minimum value = 1<br>Maximum value = 4294967294</td></tr><tr><td>pushvserver</td><td>&lt;String></td><td>Read-write</td><td>The lb vserver of type PUSH/SSL_PUSH to which server pushes the updates received on the client facing non-push lb vserver.<br>Minimum length = 1</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[DELETE](#d)| [UPDATE](#u)| [ENABLE](#e)| [DISABLE](#di)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###delete



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vserver/name_value&lt;String&gt;
<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vserver
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"vserver":{<b>"name":<String_value>,</b>"backupvserver":<String_value>,"redirecturl":<String_value>,"cacheable":<String_value>,"clttimeout":<Double_value>,"somethod":<String_value>,"sopersistence":<String_value>,"sopersistencetimeout":<Double_value>,"sothreshold":<Double_value>,"pushvserver":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###enable



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vserver?<b>action=enable</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"vserver":{<b>"name":<String_value></b>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###disable



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vserver?<b>action=disable</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"vserver":{<b>"name":<String_value></b>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


