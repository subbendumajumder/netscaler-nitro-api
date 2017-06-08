#callhome

Configuration for callhome resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>emailaddress</td><td>&lt;String></td><td>Read-write</td><td>The contact persons E-mail address.&lt;br>Maximum length = 78</td><tr><tr><td>proxymode</td><td>&lt;String></td><td>Read-write</td><td>Deploy the callhome proxy mode.&lt;br>Default value: NO&lt;br>Possible values = YES, NO</td><tr><tr><td>ipaddress</td><td>&lt;String></td><td>Read-write</td><td>Proxy Server IP address.&lt;br>Minimum length = 1</td><tr><tr><td>port</td><td>&lt;Integer></td><td>Read-write</td><td>Proxy Server Port.&lt;br>Minimum value = 1&lt;br>Range 1 - 65535</td><tr><tr><td>sslcardfirstfailure</td><td>&lt;String></td><td>Read-only</td><td>First occurrence SSL card failure.</td><tr><tr><td>sslcardlatestfailure</td><td>&lt;String></td><td>Read-only</td><td>Latest occurrence SSL card failure.</td><tr><tr><td>powfirstfail</td><td>&lt;String></td><td>Read-only</td><td>First occurrence power supply unit failure.</td><tr><tr><td>powlatestfailure</td><td>&lt;String></td><td>Read-only</td><td>Latest occurrence power supply unit failure.</td><tr><tr><td>hddfirstfail</td><td>&lt;String></td><td>Read-only</td><td>First occurrence hard disk drive failure.</td><tr><tr><td>hddlatestfailure</td><td>&lt;String></td><td>Read-only</td><td>Latest occurrence hard disk drive failure.</td><tr><tr><td>flashfirstfail</td><td>&lt;String></td><td>Read-only</td><td>First occurrence compact flash failure.</td><tr><tr><td>flashlatestfailure</td><td>&lt;String></td><td>Read-only</td><td>Latest occurrence compact flush failure.</td><tr><tr><td>restartlatestfail</td><td>&lt;String></td><td>Read-only</td><td>Latest occurrence warm restart failure.</td><tr><tr><td>callhomestatus</td><td>&lt;String[]></td><td>Read-only</td><td>Callhome feature enabled/disable, register with upload server successful/failed.&lt;br>Possible values = ENABLED, DISABLED, SUCCESSFUL, FAILED</td><tr></tbody></table>
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
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","callhome":{      "emailaddress":<String_value>,      "proxymode":<String_value>,                  "ipaddress":<String_value>,                  "port":<Integer_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","callhome":{      "emailaddress":true,      "proxymode":true,      "ipaddress":true,      "port":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/callhome
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "callhome": [ {      "emailaddress":<String_value>,      "proxymode":<String_value>,      "ipaddress":<String_value>,      "port":<Integer_value>,      "sslcardfirstfailure":<String_value>,      "sslcardlatestfailure":<String_value>,      "powfirstfail":<String_value>,      "powlatestfailure":<String_value>,      "hddfirstfail":<String_value>,      "hddlatestfailure":<String_value>,      "flashfirstfail":<String_value>,      "flashlatestfailure":<String_value>,      "restartlatestfail":<String_value>,      "callhomestatus":<String[]_value>}]}```



