#aaatacacsparams

Configuration for tacacs parameters resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>serverip</td><td>&lt;String></td><td>Read-write</td><td>IP address of your TACACS+ server.&lt;br>Minimum length = 1</td><tr><tr><td>serverport</td><td>&lt;Integer></td><td>Read-write</td><td>Port number on which the TACACS+ server listens for connections.&lt;br>Default value: 49&lt;br>Minimum value = 1</td><tr><tr><td>authtimeout</td><td>&lt;Double></td><td>Read-write</td><td>Maximum number of seconds that the NetScaler appliance waits for a response from the TACACS+ server.&lt;br>Default value: 3&lt;br>Minimum value = 1</td><tr><tr><td>tacacssecret</td><td>&lt;String></td><td>Read-write</td><td>Key shared between the TACACS+ server and clients. Required for allowing the NetScaler appliance to communicate with the TACACS+ server.&lt;br>Minimum length = 1</td><tr><tr><td>authorization</td><td>&lt;String></td><td>Read-write</td><td>Use streaming authorization on the TACACS+ server.&lt;br>Possible values = ON, OFF</td><tr><tr><td>accounting</td><td>&lt;String></td><td>Read-write</td><td>Send accounting messages to the TACACS+ server.&lt;br>Possible values = ON, OFF</td><tr><tr><td>auditfailedcmds</td><td>&lt;String></td><td>Read-write</td><td>The option for sending accounting messages to the TACACS+ server.&lt;br>Possible values = ON, OFF</td><tr><tr><td>defaultauthenticationgroup</td><td>&lt;String></td><td>Read-write</td><td>This is the default group that is chosen when the authentication succeeds in addition to extracted groups.&lt;br>Maximum length = 64</td><tr></tbody></table>
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
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","aaatacacsparams":{      "serverip":<String_value>,      "serverport":<Integer_value>,      "authtimeout":<Double_value>,      "tacacssecret":<String_value>,      "authorization":<String_value>,      "accounting":<String_value>,      "auditfailedcmds":<String_value>,      "defaultauthenticationgroup":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","aaatacacsparams":{      "serverip":true,      "serverport":true,      "authtimeout":true,      "tacacssecret":true,      "authorization":true,      "accounting":true,      "auditfailedcmds":true,      "defaultauthenticationgroup":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/aaatacacsparams
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "aaatacacsparams": [ {      "serverip":<String_value>,      "serverport":<Integer_value>,      "authtimeout":<Double_value>,      "tacacssecret":<String_value>,      "authorization":<String_value>,      "accounting":<String_value>,      "auditfailedcmds":<String_value>,      "defaultauthenticationgroup":<String_value>}]}```



