#systemparameter

Configuration for system parameter resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>rbaonresponse</td><td>&lt;String></td><td>Read-write</td><td>Enable or disable Role-Based Authentication (RBA) on responses.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>promptstring</td><td>&lt;String></td><td>Read-write</td><td>String to display at the command-line prompt. Can consist of letters, numbers, hyphen (-), period (.), hash (#), space ( ), at (@), equal (=), colon (:), underscore (_), and the following variables: <br>* %u - Will be replaced by the user name.<br>* %h - Will be replaced by the hostname of the NetScaler appliance.<br>* %t - Will be replaced by the current time in 12-hour format.<br>* %T - Will be replaced by the current time in 24-hour format.<br>* %d - Will be replaced by the current date.<br>* %s - Will be replaced by the state of the NetScaler appliance.<br><br>Note: The 63-character limit for the length of the string does not apply to the characters that replace the variables.<br>Minimum length = 1</td></tr><tr><td>natpcbforceflushlimit</td><td>&lt;Double></td><td>Read-write</td><td>Flush the system if the number of Network Address Translation Protocol Control Blocks (NATPCBs) exceeds this value.<br>Default value: 2147483647<br>Minimum value = 1000</td></tr><tr><td>natpcbrstontimeout</td><td>&lt;String></td><td>Read-write</td><td>Send a reset signal to client and server connections when their NATPCBs time out. Avoids the buildup of idle TCP connections on both the sides.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>timeout</td><td>&lt;Double></td><td>Read-write</td><td>CLI session inactivity timeout, in seconds. If Restrictedtimeout argument is enabled, Timeout can have values in the range [300-86400] seconds.<br>If Restrictedtimeout argument is disabled, Timeout can have values in the range [0, 10-100000000] seconds. Default value is 900 seconds.</td></tr><tr><td>localauth</td><td>&lt;String></td><td>Read-write</td><td>When enabled, local users can access NetScaler even when external authentication is configured. When disabled, local users are not allowed to access the NetScaler, Local users can access the NetScaler only when the configured external authentication servers are unavailable.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>minpasswordlen</td><td>&lt;Double></td><td>Read-write</td><td>Minimum length of system user password. When strong password is enabled default minimum length is 4. User entered value can be greater than or equal to 4. Default mininum value is 1 when strong password is disabled. Maximum value is 127 in both cases.<br>Minimum value = 1<br>Maximum value = 127</td></tr><tr><td>strongpassword</td><td>&lt;String></td><td>Read-write</td><td>After enabling strong password (enableall / enablelocal - not included in exclude list), all the passwords / sensitive information must have - Atleast 1 Lower case character, Atleast 1 Upper case character, Atleast 1 numeric character, Atleast 1 special character ( ~, `, !, @, #, $, %, ^, ;, *, -, _, =, +, {, }, [, ], |, \, :, &lt;, &gt;, /, ., ,, " "). Exclude list in case of enablelocal is - NS_FIPS, NS_CRL, NS_RSAKEY, NS_PKCS12, NS_PKCS8, NS_LDAP, NS_TACACS, NS_TACACSACTION, NS_RADIUS, NS_RADIUSACTION, NS_ENCRYPTION_PARAMS. So no Strong Password checks will be performed on these ObjectType commands for enablelocal case.<br>Default value: disabled<br>Possible values = enableall, enablelocal, disabled</td></tr><tr><td>restrictedtimeout</td><td>&lt;String></td><td>Read-write</td><td>Enable/Disable the restricted timeout behaviour. When enabled, timeout cannot be configured beyond admin configured timeout and also it will have the [minimum - maximum] range check. When disabled, timeout will have the old behaviour. By default the value is disabled.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>fipsusermode</td><td>&lt;String></td><td>Read-write</td><td>Use this option to set the FIPS mode for key user-land processes. When enabled, these user-land processes will operate in FIPS mode. In this mode, theses processes will use FIPS 140-2 Level-1 certified crypto algorithms. Default is disabled, wherein, these user-land processes will not operate in FIPS mode.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>doppler</td><td>&lt;String></td><td>Read-write</td><td>Enable or disable Doppler.<br>Default value: 0<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>googleanalytics</td><td>&lt;String></td><td>Read-write</td><td>Enable or disable Google analytics.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>totalauthtimeout</td><td>&lt;Double></td><td>Read-write</td><td>Total time a request can take for authentication/authorization.<br>Default value: 20<br>Minimum value = 5<br>Maximum value = 120</td></tr><tr><td>cliloglevel</td><td>&lt;String></td><td>Read-write</td><td>Audit log level, which specifies the types of events to log for cli executed commands.<br>Available values function as follows:<br>* EMERGENCY - Events that indicate an immediate crisis on the server.<br>* ALERT - Events that might require action.<br>* CRITICAL - Events that indicate an imminent server crisis.<br>* ERROR - Events that indicate some type of error.<br>* WARNING - Events that require action in the near future.<br>* NOTICE - Events that the administrator should know about.<br>* INFORMATIONAL - All but low-level events.<br>* DEBUG - All events, in extreme detail.<br>Default value: INFORMATIONAL<br>Possible values = EMERGENCY, ALERT, CRITICAL, ERROR, WARNING, NOTICE, INFORMATIONAL, DEBUG</td></tr><tr><td>forcepasswordchange</td><td>&lt;String></td><td>Read-write</td><td>Enable or disable force password change for nsroot user.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>basicauth</td><td>&lt;String></td><td>Read-write</td><td>Enable or disable basic authentication for Nitro API.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>reauthonauthparamchange</td><td>&lt;String></td><td>Read-write</td><td>Enable or disable External user reauthentication when authentication parameter changes.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>maxclient</td><td>&lt;Double></td><td>Read-only</td><td>Maximum number of client connection allowed by the system.<br>Minimum value = 20<br>Maximum value = 40</td></tr><tr><td>allowdefaultpartition</td><td>&lt;String></td><td>Read-only</td><td>Enable/Disable the allowing partition users to access default partition.<br>Default value: NO<br>Possible values = YES, NO</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[UPDATE](#u)| [UNSET](#)| [GET (ALL)](#get-)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/systemparameter
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"systemparameter":{"rbaonresponse":<String_value>,"promptstring":<String_value>,"natpcbforceflushlimit":<Double_value>,"natpcbrstontimeout":<String_value>,"timeout":<Double_value>,"localauth":<String_value>,"minpasswordlen":<Double_value>,"strongpassword":<String_value>,"restrictedtimeout":<String_value>,"fipsusermode":<String_value>,"doppler":<String_value>,"googleanalytics":<String_value>,"totalauthtimeout":<Double_value>,"cliloglevel":<String_value>,"forcepasswordchange":<String_value>,"basicauth":<String_value>,"reauthonauthparamchange":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/systemparameter?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"systemparameter":{"minpasswordlen":true,"rbaonresponse":true,"promptstring":true,"natpcbforceflushlimit":true,"natpcbrstontimeout":true,"timeout":true,"localauth":true,"strongpassword":true,"restrictedtimeout":true,"fipsusermode":true,"doppler":true,"googleanalytics":true,"totalauthtimeout":true,"cliloglevel":true,"forcepasswordchange":true,"basicauth":true,"reauthonauthparamchange":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/systemparameter
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "systemparameter": [ {"rbaonresponse":<String_value>,"promptstring":<String_value>,"natpcbforceflushlimit":<Double_value>,"natpcbrstontimeout":<String_value>,"timeout":<Double_value>,"maxclient":<Double_value>,"localauth":<String_value>,"minpasswordlen":<Double_value>,"strongpassword":<String_value>,"restrictedtimeout":<String_value>,"fipsusermode":<String_value>,"doppler":<String_value>,"googleanalytics":<String_value>,"cliloglevel":<String_value>,"forcepasswordchange":<String_value>,"totalauthtimeout":<Double_value>,"basicauth":<String_value>,"allowdefaultpartition":<String_value>,"reauthonauthparamchange":<String_value>}]}```



