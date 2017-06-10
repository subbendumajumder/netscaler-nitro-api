#aaaparameter

Configuration for AAA parameter resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>enablestaticpagecaching</td><td>&lt;String></td><td>Read-write</td><td>The default state of VPN Static Page caching. If nothing is specified, the default value is set to YES.&lt;br>Default value: YES&lt;br>Possible values = YES, NO</td><tr><tr><td>enableenhancedauthfeedback</td><td>&lt;String></td><td>Read-write</td><td>Enhanced auth feedback provides more information to the end user about the reason for an authentication failure. The default value is set to NO.&lt;br>Default value: NO&lt;br>Possible values = YES, NO</td><tr><tr><td>defaultauthtype</td><td>&lt;String></td><td>Read-write</td><td>The default authentication server type.&lt;br>Default value: LOCAL&lt;br>Possible values = LOCAL, LDAP, RADIUS, TACACS, CERT</td><tr><tr><td>maxaaausers</td><td>&lt;Double></td><td>Read-write</td><td>Maximum number of concurrent users allowed to log on to VPN simultaneously.&lt;br>Minimum value = 1</td><tr><tr><td>maxloginattempts</td><td>&lt;Double></td><td>Read-write</td><td>Maximum Number of login Attempts.&lt;br>Minimum value = 1</td><tr><tr><td>failedlogintimeout</td><td>&lt;Double></td><td>Read-write</td><td>Number of minutes an account will be locked if user exceeds maximum permissible attempts.&lt;br>Minimum value = 1</td><tr><tr><td>aaadnatip</td><td>&lt;String></td><td>Read-write</td><td>Source IP address to use for traffic that is sent to the authentication server.</td><tr><tr><td>enablesessionstickiness</td><td>&lt;String></td><td>Read-write</td><td>Enables/Disables stickiness to authentication servers.&lt;br>Default value: NO&lt;br>Possible values = YES, NO</td><tr><tr><td>aaasessionloglevel</td><td>&lt;String></td><td>Read-write</td><td>Audit log level, which specifies the types of events to log for cli executed commands. &lt;br>Available values function as follows: &lt;br>* EMERGENCY - Events that indicate an immediate crisis on the server.&lt;br>* ALERT - Events that might require action.&lt;br>* CRITICAL - Events that indicate an imminent server crisis.&lt;br>* ERROR - Events that indicate some type of error.&lt;br>* WARNING - Events that require action in the near future.&lt;br>* NOTICE - Events that the administrator should know about.&lt;br>* INFORMATIONAL - All but low-level events.&lt;br>* DEBUG - All events, in extreme detail.&lt;br>Default value: DEFAULT_LOGLEVEL_AAA&lt;br>Possible values = EMERGENCY, ALERT, CRITICAL, ERROR, WARNING, NOTICE, INFORMATIONAL, DEBUG</td><tr><tr><td>aaadloglevel</td><td>&lt;String></td><td>Read-write</td><td>AAAD log level, which specifies the types of AAAD events to log in nsvpn.log. &lt;br>Available values function as follows: &lt;br>* EMERGENCY - Events that indicate an immediate crisis on the server.&lt;br>* ALERT - Events that might require action.&lt;br>* CRITICAL - Events that indicate an imminent server crisis.&lt;br>* ERROR - Events that indicate some type of error.&lt;br>* WARNING - Events that require action in the near future.&lt;br>* NOTICE - Events that the administrator should know about.&lt;br>* INFORMATIONAL - All but low-level events.&lt;br>* DEBUG - All events, in extreme detail.&lt;br>Default value: INFORMATIONAL&lt;br>Possible values = EMERGENCY, ALERT, CRITICAL, ERROR, WARNING, NOTICE, INFORMATIONAL, DEBUG</td><tr><tr><td>dynaddr</td><td>&lt;String></td><td>Read-write</td><td>Set by the DHCP client when the IP address was fetched dynamically.&lt;br>Default value: OFF&lt;br>Possible values = ON, OFF</td><tr><tr><td>ftmode</td><td>&lt;String></td><td>Read-write</td><td>First time user mode determines which configuration options are shown by default when logging in to the GUI. This setting is controlled by the GUI.&lt;br>Default value: ON&lt;br>Possible values = ON, HA, OFF</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[UPDATE](#update) | [UNSET](#unset) | [GET (ALL)](#get-(all))


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###update



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/aaaparameter
HTTP Method: PUT
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"aaaparameter":{      "enablestaticpagecaching":<String_value>,      "enableenhancedauthfeedback":<String_value>,      "defaultauthtype":<String_value>,      "maxaaausers":<Double_value>,      "maxloginattempts":<Double_value>,      "failedlogintimeout":<Double_value>,      "aaadnatip":<String_value>,      "enablesessionstickiness":<String_value>,      "aaasessionloglevel":<String_value>,      "aaadloglevel":<String_value>,      "dynaddr":<String_value>,      "ftmode":<String_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/aaaparameter?action=unset
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"aaaparameter":{      "enablestaticpagecaching":true,      "enableenhancedauthfeedback":true,      "defaultauthtype":true,      "maxaaausers":true,      "aaadnatip":true,      "maxloginattempts":true,      "enablesessionstickiness":true,      "aaasessionloglevel":true,      "aaadloglevel":true,      "dynaddr":true,      "ftmode":true}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/aaaparameter
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "aaaparameter": [ {      "enablestaticpagecaching":<String_value>,      "enableenhancedauthfeedback":<String_value>,      "defaultauthtype":<String_value>,      "maxaaausers":<Double_value>,      "aaadnatip":<String_value>,      "maxloginattempts":<Double_value>,      "failedlogintimeout":<Double_value>,      "enablesessionstickiness":<String_value>,      "aaasessionloglevel":<String_value>,      "aaadloglevel":<String_value>,      "dynaddr":<String_value>,      "ftmode":<String_value>}]}```



