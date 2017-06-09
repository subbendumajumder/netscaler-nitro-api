#systemparameter

Configuration for system parameter resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>rbaonresponse</td><td>&lt;String></td><td>Read-write</td><td>Enable or disable Role-Based Authentication (RBA) on responses.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>promptstring</td><td>&lt;String></td><td>Read-write</td><td>String to display at the command-line prompt. Can consist of letters, numbers, hyphen (-), period (.), hash (#), space ( ), at (@), equal (=), colon (:), underscore (_), and the following variables: * %u - Will be replaced by the user name. * %h - Will be replaced by the hostname of the NetScaler appliance. * %t - Will be replaced by the current time in 12-hour format. * %T - Will be replaced by the current time in 24-hour format. * %d - Will be replaced by the current date. * %s - Will be replaced by the state of the NetScaler appliance. Note: The 63-character limit for the length of the string does not apply to the characters that replace the variables.&lt;br>Minimum length = 1</td><tr><tr><td>natpcbforceflushlimit</td><td>&lt;Double></td><td>Read-write</td><td>Flush the system if the number of Network Address Translation Protocol Control Blocks (NATPCBs) exceeds this value.&lt;br>Default value: 2147483647&lt;br>Minimum value = 1000</td><tr><tr><td>natpcbrstontimeout</td><td>&lt;String></td><td>Read-write</td><td>Send a reset signal to client and server connections when their NATPCBs time out. Avoids the buildup of idle TCP connections on both the sides.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>timeout</td><td>&lt;Double></td><td>Read-write</td><td>CLI session inactivity timeout, in seconds. If Restrictedtimeout argument is enabled, Timeout can have values in the range [300-86400] seconds. If Restrictedtimeout argument is disabled, Timeout can have values in the range [0, 10-100000000] seconds. Default value is 900 seconds.</td><tr><tr><td>localauth</td><td>&lt;String></td><td>Read-write</td><td>When enabled, local users can access NetScaler even when external authentication is configured. When disabled, local users are not allowed to access the NetScaler, Local users can access the NetScaler only when the configured external authentication servers are unavailable.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>minpasswordlen</td><td>&lt;Double></td><td>Read-write</td><td>Minimum length of system user password. When strong password is enabled default minimum length is 4. User entered value can be greater than or equal to 4. Default mininum value is 1 when strong password is disabled. Maximum value is 127 in both cases.&lt;br>Minimum value = 1&lt;br>Maximum value = 127</td><tr><tr><td>strongpassword</td><td>&lt;String></td><td>Read-write</td><td>Option to enable/disable strong password. When this is enabled, system user password should contain atleast one lower case character, one upper case character, one numeric character and one special character from the set (!, @, #, (, ), $, %, ^, ;amp;, *).&lt;br>Default value: disabled&lt;br>Possible values = enableall, enablelocal, disabled</td><tr><tr><td>restrictedtimeout</td><td>&lt;String></td><td>Read-write</td><td>Enable/Disable the restricted timeout behaviour. When enabled, timeout cannot be configured beyond admin configured timeout and also it will have the [minimum - maximum] range check. When disabled, timeout will have the old behaviour. By default the value is disabled.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>fipsusermode</td><td>&lt;String></td><td>Read-write</td><td>Use this option to set the FIPS mode for key user-land processes. When enabled, these user-land processes will operate in FIPS mode. In this mode, theses processes will use FIPS 140-2 Level-1 certified crypto algorithms. Default is disabled, wherein, these user-land processes will not operate in FIPS mode.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>doppler</td><td>&lt;String></td><td>Read-write</td><td>Enable or disable Doppler.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>googleanalytics</td><td>&lt;String></td><td>Read-write</td><td>Enable or disable Google analytics.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>maxclient</td><td>&lt;Double></td><td>Read-only</td><td>Maximum number of client connection allowed by the system.&lt;br>Minimum value = 20&lt;br>Maximum value = 40</td><tr></tbody></table>
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
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","systemparameter":{      "rbaonresponse":<String_value>,      "promptstring":<String_value>,      "natpcbforceflushlimit":<Double_value>,      "natpcbrstontimeout":<String_value>,      "timeout":<Double_value>,      "localauth":<String_value>,      "minpasswordlen":<Double_value>,      "strongpassword":<String_value>,      "restrictedtimeout":<String_value>,      "fipsusermode":<String_value>,      "doppler":<String_value>,      "googleanalytics":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","systemparameter":{      "minpasswordlen":true,      "rbaonresponse":true,      "promptstring":true,      "natpcbforceflushlimit":true,      "natpcbrstontimeout":true,      "timeout":true,      "localauth":true,      "strongpassword":true,      "restrictedtimeout":true,      "fipsusermode":true,      "doppler":true,      "googleanalytics":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/systemparameter
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "systemparameter": [ {      "rbaonresponse":<String_value>,      "promptstring":<String_value>,      "natpcbforceflushlimit":<Double_value>,      "natpcbrstontimeout":<String_value>,      "timeout":<Double_value>,      "maxclient":<Double_value>,      "localauth":<String_value>,      "minpasswordlen":<Double_value>,      "strongpassword":<String_value>,      "restrictedtimeout":<String_value>,      "fipsusermode":<String_value>,      "doppler":<String_value>,      "googleanalytics":<String_value>}]}```



