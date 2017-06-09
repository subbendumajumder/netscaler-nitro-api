#aaaradiusparams

Configuration for RADIUS parameter resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>serverip</td><td>&lt;String></td><td>Read-write</td><td>IP address of your RADIUS server.&lt;br>Minimum length = 1</td><tr><tr><td>serverport</td><td>&lt;Integer></td><td>Read-write</td><td>Port number on which the RADIUS server listens for connections.&lt;br>Default value: 1812&lt;br>Minimum value = 1</td><tr><tr><td>authtimeout</td><td>&lt;Double></td><td>Read-write</td><td>Maximum number of seconds that the NetScaler appliance waits for a response from the RADIUS server.&lt;br>Default value: 3&lt;br>Minimum value = 1</td><tr><tr><td>radkey</td><td>&lt;String></td><td>Read-write</td><td>The key shared between the RADIUS server and clients. &lt;br>Required for allowing the NetScaler appliance to communicate with the RADIUS server.&lt;br>Minimum length = 1</td><tr><tr><td>radnasip</td><td>&lt;String></td><td>Read-write</td><td>Send the NetScaler IP (NSIP) address to the RADIUS server as the Network Access Server IP (NASIP) part of the Radius protocol.&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>radnasid</td><td>&lt;String></td><td>Read-write</td><td>Send the Network Access Server ID (NASID) for your NetScaler appliance to the RADIUS server as the nasid part of the Radius protocol.</td><tr><tr><td>radvendorid</td><td>&lt;Double></td><td>Read-write</td><td>Vendor ID for RADIUS group extraction.&lt;br>Minimum value = 1</td><tr><tr><td>radattributetype</td><td>&lt;Double></td><td>Read-write</td><td>Attribute type for RADIUS group extraction.&lt;br>Minimum value = 1</td><tr><tr><td>radgroupsprefix</td><td>&lt;String></td><td>Read-write</td><td>Prefix string that precedes group names within a RADIUS attribute for RADIUS group extraction.</td><tr><tr><td>radgroupseparator</td><td>&lt;String></td><td>Read-write</td><td>Group separator string that delimits group names within a RADIUS attribute for RADIUS group extraction.</td><tr><tr><td>passencoding</td><td>&lt;String></td><td>Read-write</td><td>Enable password encoding in RADIUS packets that the NetScaler appliance sends to the RADIUS server.&lt;br>Default value: pap&lt;br>Possible values = pap, chap, mschapv1, mschapv2</td><tr><tr><td>ipvendorid</td><td>&lt;Double></td><td>Read-write</td><td>Vendor ID attribute in the RADIUS response. &lt;br>If the attribute is not vendor-encoded, it is set to 0.</td><tr><tr><td>ipattributetype</td><td>&lt;Double></td><td>Read-write</td><td>IP attribute type in the RADIUS response.&lt;br>Minimum value = 1</td><tr><tr><td>accounting</td><td>&lt;String></td><td>Read-write</td><td>Configure the RADIUS server state to accept or refuse accounting messages.&lt;br>Possible values = ON, OFF</td><tr><tr><td>pwdvendorid</td><td>&lt;Double></td><td>Read-write</td><td>Vendor ID of the password in the RADIUS response. Used to extract the user password.&lt;br>Minimum value = 1</td><tr><tr><td>pwdattributetype</td><td>&lt;Double></td><td>Read-write</td><td>Attribute type of the Vendor ID in the RADIUS response.&lt;br>Minimum value = 1</td><tr><tr><td>defaultauthenticationgroup</td><td>&lt;String></td><td>Read-write</td><td>This is the default group that is chosen when the authentication succeeds in addition to extracted groups.&lt;br>Maximum length = 64</td><tr><tr><td>callingstationid</td><td>&lt;String></td><td>Read-write</td><td>Send Calling-Station-ID of the client to the RADIUS server. IP Address of the client is sent as its Calling-Station-ID.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>authservretry</td><td>&lt;Double></td><td>Read-write</td><td>Number of retry by the NetScaler appliance before getting response from the RADIUS server.&lt;br>Default value: 3&lt;br>Minimum value = 1&lt;br>Maximum value = 10</td><tr><tr><td>groupauthname</td><td>&lt;String></td><td>Read-only</td><td>To associate AAA users with an AAA group, use the command&lt;br>&lt;br> "bind AAA group ... -username ...".&lt;br>&lt;br>You can bind different policies to each AAA group. Use the command&lt;br>&lt;br> "bind AAA group ... -policy ...".</td><tr><tr><td>ipaddress</td><td>&lt;String></td><td>Read-only</td><td>IP Address.</td><tr><tr><td>builtin</td><td>&lt;String[]></td><td>Read-only</td><td>Indicates that a variable is a built-in (SYSTEM INTERNAL) type.&lt;br>Possible values = MODIFIABLE, DELETABLE, IMMUTABLE, PARTITION_ALL</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[UPDATE](#update) | [UNSET](#unset) | [GET (ALL)](#get-(all))


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###update



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/aaaradiusparams
HTTP Method: PUT
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"aaaradiusparams":{      "serverip":<String_value>,      "serverport":<Integer_value>,      "authtimeout":<Double_value>,      "radkey":<String_value>,      "radnasip":<String_value>,      "radnasid":<String_value>,      "radvendorid":<Double_value>,      "radattributetype":<Double_value>,      "radgroupsprefix":<String_value>,      "radgroupseparator":<String_value>,      "passencoding":<String_value>,      "ipvendorid":<Double_value>,      "ipattributetype":<Double_value>,      "accounting":<String_value>,      "pwdvendorid":<Double_value>,      "pwdattributetype":<Double_value>,      "defaultauthenticationgroup":<String_value>,      "callingstationid":<String_value>,      "authservretry":<Double_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/aaaradiusparams?action=unset
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"aaaradiusparams":{      "serverip":true,      "serverport":true,      "authtimeout":true,      "radnasip":true,      "radnasid":true,      "radvendorid":true,      "radattributetype":true,      "radgroupsprefix":true,      "radgroupseparator":true,      "passencoding":true,      "ipvendorid":true,      "ipattributetype":true,      "accounting":true,      "pwdvendorid":true,      "pwdattributetype":true,      "defaultauthenticationgroup":true,      "callingstationid":true,      "authservretry":true}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/aaaradiusparams
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "aaaradiusparams": [ {      "serverip":<String_value>,      "serverport":<Integer_value>,      "radkey":<String_value>,      "groupauthname":<String_value>,      "authtimeout":<Double_value>,      "radnasip":<String_value>,      "radnasid":<String_value>,      "ipaddress":<String_value>,      "radvendorid":<Double_value>,      "radattributetype":<Double_value>,      "radgroupsprefix":<String_value>,      "radgroupseparator":<String_value>,      "passencoding":<String_value>,      "ipvendorid":<Double_value>,      "ipattributetype":<Double_value>,      "accounting":<String_value>,      "pwdvendorid":<Double_value>,      "pwdattributetype":<Double_value>,      "defaultauthenticationgroup":<String_value>,      "callingstationid":<String_value>,      "authservretry":<Double_value>,      "builtin":<String[]_value>}]}```



