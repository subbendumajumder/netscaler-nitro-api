#nshttpparam

Configuration for HTTP parameter resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>dropinvalreqs</td><td>&lt;String></td><td>Read-write</td><td>Drop invalid HTTP requests or responses.&lt;br>Default value: OFF&lt;br>Possible values = ON, OFF</td><tr><tr><td>markhttp09inval</td><td>&lt;String></td><td>Read-write</td><td>Mark HTTP/0.9 requests as invalid.&lt;br>Default value: OFF&lt;br>Possible values = ON, OFF</td><tr><tr><td>markconnreqinval</td><td>&lt;String></td><td>Read-write</td><td>Mark CONNECT requests as invalid.&lt;br>Default value: OFF&lt;br>Possible values = ON, OFF</td><tr><tr><td>insnssrvrhdr</td><td>&lt;String></td><td>Read-write</td><td>Enable or disable NetScaler server header insertion for NetScaler generated HTTP responses.&lt;br>Default value: OFF&lt;br>Possible values = ON, OFF</td><tr><tr><td>nssrvrhdr</td><td>&lt;String></td><td>Read-write</td><td>The server header value to be inserted. If no explicit header is specified then NSBUILD.RELEASE is used as default server header.&lt;br>Minimum length = 1</td><tr><tr><td>logerrresp</td><td>&lt;String></td><td>Read-write</td><td>Server header value to be inserted.&lt;br>Default value: ON&lt;br>Possible values = ON, OFF</td><tr><tr><td>conmultiplex</td><td>&lt;String></td><td>Read-write</td><td>Reuse server connections for requests from more than one client connections.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>maxreusepool</td><td>&lt;Double></td><td>Read-write</td><td>Maximum limit on the number of connections, from the NetScaler to a particular server that are kept in the reuse pool. This setting is helpful for optimal memory utilization and for reducing the idle connections to the server just after the peak time.&lt;br>Minimum value = 0&lt;br>Maximum value = 360000</td><tr><tr><td>builtin</td><td>&lt;String[]></td><td>Read-only</td><td>Flag to determine if the http param is built-in or not.&lt;br>Possible values = MODIFIABLE, DELETABLE, IMMUTABLE, PARTITION_ALL</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[UPDATE](#update) | [UNSET](#unset) | [GET (ALL)](#get-(all))


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","nshttpparam":{      "dropinvalreqs":<String_value>,      "markhttp09inval":<String_value>,      "markconnreqinval":<String_value>,      "insnssrvrhdr":<String_value>,                  "nssrvrhdr":<String_value>,      "logerrresp":<String_value>,      "conmultiplex":<String_value>,      "maxreusepool":<Double_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","nshttpparam":{      "dropinvalreqs":true,      "markhttp09inval":true,      "markconnreqinval":true,      "insnssrvrhdr":true,      "nssrvrhdr":true,      "logerrresp":true,      "conmultiplex":true,      "maxreusepool":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/nshttpparam
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "nshttpparam": [ {      "dropinvalreqs":<String_value>,      "markhttp09inval":<String_value>,      "markconnreqinval":<String_value>,      "insnssrvrhdr":<String_value>,      "nssrvrhdr":<String_value>,      "logerrresp":<String_value>,      "conmultiplex":<String_value>,      "maxreusepool":<Double_value>,      "builtin":<String[]_value>}]}```



