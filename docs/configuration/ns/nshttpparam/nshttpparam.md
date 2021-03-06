#nshttpparam

Configuration for HTTP parameter resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>dropinvalreqs</td><td>&lt;String></td><td>Read-write</td><td>Drop invalid HTTP requests or responses.<br>Default value: OFF<br>Possible values = ON, OFF</td></tr><tr><td>markhttp09inval</td><td>&lt;String></td><td>Read-write</td><td>Mark HTTP/0.9 requests as invalid.<br>Default value: OFF<br>Possible values = ON, OFF</td></tr><tr><td>markconnreqinval</td><td>&lt;String></td><td>Read-write</td><td>Mark CONNECT requests as invalid.<br>Default value: OFF<br>Possible values = ON, OFF</td></tr><tr><td>insnssrvrhdr</td><td>&lt;String></td><td>Read-write</td><td>Enable or disable NetScaler server header insertion for NetScaler generated HTTP responses.<br>Default value: OFF<br>Possible values = ON, OFF</td></tr><tr><td>nssrvrhdr</td><td>&lt;String></td><td>Read-write</td><td>The server header value to be inserted. If no explicit header is specified then NSBUILD.RELEASE is used as default server header.<br>Minimum length = 1</td></tr><tr><td>logerrresp</td><td>&lt;String></td><td>Read-write</td><td>Server header value to be inserted.<br>Default value: ON<br>Possible values = ON, OFF</td></tr><tr><td>conmultiplex</td><td>&lt;String></td><td>Read-write</td><td>Reuse server connections for requests from more than one client connections.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>maxreusepool</td><td>&lt;Double></td><td>Read-write</td><td>Maximum limit on the number of connections, from the NetScaler to a particular server that are kept in the reuse pool. This setting is helpful for optimal memory utilization and for reducing the idle connections to the server just after the peak time.<br>Default value: 0<br>Minimum value = 0<br>Maximum value = 360000</td></tr><tr><td>http2serverside</td><td>&lt;String></td><td>Read-write</td><td>Enable/Disable HTTP/2 on server side.<br>Default value: OFF<br>Possible values = ON, OFF</td></tr><tr><td>builtin</td><td>&lt;String[]></td><td>Read-only</td><td>Flag to determine if the http param is built-in or not.<br>Possible values = MODIFIABLE, DELETABLE, IMMUTABLE, PARTITION_ALL</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[UPDATE](#u)| [UNSET](#)| [GET (ALL)](#get-)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nshttpparam
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"nshttpparam":{"dropinvalreqs":<String_value>,"markhttp09inval":<String_value>,"markconnreqinval":<String_value>,"insnssrvrhdr":<String_value>,"nssrvrhdr":<String_value>,"logerrresp":<String_value>,"conmultiplex":<String_value>,"maxreusepool":<Double_value>,"http2serverside":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nshttpparam?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"nshttpparam":{"dropinvalreqs":true,"markhttp09inval":true,"markconnreqinval":true,"insnssrvrhdr":true,"nssrvrhdr":true,"logerrresp":true,"conmultiplex":true,"maxreusepool":true,"http2serverside":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nshttpparam
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "nshttpparam": [ {"dropinvalreqs":<String_value>,"markhttp09inval":<String_value>,"markconnreqinval":<String_value>,"insnssrvrhdr":<String_value>,"nssrvrhdr":<String_value>,"logerrresp":<String_value>,"conmultiplex":<String_value>,"maxreusepool":<Double_value>,"http2serverside":<String_value>,"builtin":<String[]_value>}]}```



