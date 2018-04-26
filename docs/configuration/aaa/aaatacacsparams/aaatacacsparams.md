#aaatacacsparams

Configuration for tacacs parameters resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>serverip</td><td>&lt;String></td><td>Read-write</td><td>IP address of your TACACS+ server.<br>Minimum length = 1</td></tr><tr><td>serverport</td><td>&lt;Integer></td><td>Read-write</td><td>Port number on which the TACACS+ server listens for connections.<br>Default value: 49<br>Minimum value = 1</td></tr><tr><td>authtimeout</td><td>&lt;Double></td><td>Read-write</td><td>Maximum number of seconds that the NetScaler appliance waits for a response from the TACACS+ server.<br>Default value: 3<br>Minimum value = 1</td></tr><tr><td>tacacssecret</td><td>&lt;String></td><td>Read-write</td><td>Key shared between the TACACS+ server and clients. Required for allowing the NetScaler appliance to communicate with the TACACS+ server.<br>Minimum length = 1</td></tr><tr><td>authorization</td><td>&lt;String></td><td>Read-write</td><td>Use streaming authorization on the TACACS+ server.<br>Possible values = ON, OFF</td></tr><tr><td>accounting</td><td>&lt;String></td><td>Read-write</td><td>Send accounting messages to the TACACS+ server.<br>Possible values = ON, OFF</td></tr><tr><td>auditfailedcmds</td><td>&lt;String></td><td>Read-write</td><td>The option for sending accounting messages to the TACACS+ server.<br>Possible values = ON, OFF</td></tr><tr><td>groupattrname</td><td>&lt;String></td><td>Read-write</td><td>TACACS+ group attribute name.Used for group extraction on the TACACS+ server.</td></tr><tr><td>defaultauthenticationgroup</td><td>&lt;String></td><td>Read-write</td><td>This is the default group that is chosen when the authentication succeeds in addition to extracted groups.<br>Maximum length = 64</td></tr><tr><td>builtin</td><td>&lt;String[]></td><td>Read-only</td><td>Indicates that a variable is a built-in (SYSTEM INTERNAL) type.<br>Possible values = MODIFIABLE, DELETABLE, IMMUTABLE, PARTITION_ALL</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[UPDATE](#u)| [UNSET](#)| [GET (ALL)](#get-)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/aaatacacsparams
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"aaatacacsparams":{"serverip":<String_value>,"serverport":<Integer_value>,"authtimeout":<Double_value>,"tacacssecret":<String_value>,"authorization":<String_value>,"accounting":<String_value>,"auditfailedcmds":<String_value>,"groupattrname":<String_value>,"defaultauthenticationgroup":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/aaatacacsparams?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"aaatacacsparams":{"serverip":true,"serverport":true,"authtimeout":true,"tacacssecret":true,"authorization":true,"accounting":true,"auditfailedcmds":true,"groupattrname":true,"defaultauthenticationgroup":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/aaatacacsparams
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "aaatacacsparams": [ {"serverip":<String_value>,"serverport":<Integer_value>,"authtimeout":<Double_value>,"tacacssecret":<String_value>,"authorization":<String_value>,"accounting":<String_value>,"auditfailedcmds":<String_value>,"groupattrname":<String_value>,"defaultauthenticationgroup":<String_value>,"builtin":<String[]_value>}]}```



