#appfwsettings

Configuration for AS settings resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>defaultprofile</td><td>&lt;String></td><td>Read-write</td><td>Profile to use when a connection does not match any policy. Default setting is APPFW_BYPASS, which sends unmatched connections back to the NetScaler appliance without attempting to filter them further.&lt;br>Default value: APPFW_BYPASS&lt;br>Minimum length = 1</td><tr><tr><td>undefaction</td><td>&lt;String></td><td>Read-write</td><td>Profile to use when an application firewall policy evaluates to undefined (UNDEF). An UNDEF event indicates an internal error condition. The APPFW_BLOCK built-in profile is the default setting. You can specify a different built-in or user-created profile as the UNDEF profile.&lt;br>Default value: APPFW_BLOCK&lt;br>Minimum length = 1</td><tr><tr><td>sessiontimeout</td><td>&lt;Double></td><td>Read-write</td><td>Timeout, in seconds, after which a user session is terminated. Before continuing to use the protected web site, the user must establish a new session by opening a designated start URL.&lt;br>Default value: 900&lt;br>Minimum value = 1&lt;br>Maximum value = 65535</td><tr><tr><td>learnratelimit</td><td>&lt;Double></td><td>Read-write</td><td>Maximum number of connections per second that the application firewall learning engine examines to generate new relaxations for learning-enabled security checks. The application firewall drops any connections above this limit from the list of connections used by the learning engine.&lt;br>Default value: 400&lt;br>Minimum value = 1&lt;br>Maximum value = 1000</td><tr><tr><td>sessionlifetime</td><td>&lt;Double></td><td>Read-write</td><td>Maximum amount of time (in seconds) that the application firewall allows a user session to remain active, regardless of user activity. After this time, the user session is terminated. Before continuing to use the protected web site, the user must establish a new session by opening a designated start URL.&lt;br>Default value: 0&lt;br>Minimum value = 0&lt;br>Maximum value = 2147483647</td><tr><tr><td>sessioncookiename</td><td>&lt;String></td><td>Read-write</td><td>Name of the session cookie that the application firewall uses to track user sessions. Must begin with a letter or number, and can consist of from 1 to 31 letters, numbers, and the hyphen (-) and underscore (_) symbols. The following requirement applies only to the NetScaler CLI: If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my cookie name" or my cookie name).&lt;br>Minimum length = 1</td><tr><tr><td>clientiploggingheader</td><td>&lt;String></td><td>Read-write</td><td>Name of an HTTP header that contains the IP address that the client used to connect to the protected web site or service.</td><tr><tr><td>importsizelimit</td><td>&lt;Double></td><td>Read-write</td><td>Cumulative total maximum number of bytes in web forms imported to a protected web site. If a user attempts to upload files with a total byte count higher than the specified limit, the application firewall blocks the request.&lt;br>Default value: 134217728&lt;br>Minimum value = 1&lt;br>Maximum value = 134217728</td><tr><tr><td>signatureautoupdate</td><td>&lt;String></td><td>Read-write</td><td>Flag used to enable/disable auto update signatures.&lt;br>Default value: OFF&lt;br>Possible values = ON, OFF</td><tr><tr><td>signatureurl</td><td>&lt;String></td><td>Read-write</td><td>URL to download the mapping file from server.&lt;br>Default value: https://s3.amazonaws.com/NSAppFwSignatures/SignaturesMapping.xml</td><tr><tr><td>cookiepostencryptprefix</td><td>&lt;String></td><td>Read-write</td><td>String that is prepended to all encrypted cookie values.&lt;br>Minimum length = 1</td><tr><tr><td>logmalformedreq</td><td>&lt;String></td><td>Read-write</td><td>Log requests that are so malformed that application firewall parsing doesnt occur.&lt;br>Default value: ON&lt;br>Possible values = ON, OFF</td><tr><tr><td>ceflogging</td><td>&lt;String></td><td>Read-write</td><td>Enable CEF format logs.&lt;br>Default value: OFF&lt;br>Possible values = ON, OFF</td><tr><tr><td>entitydecoding</td><td>&lt;String></td><td>Read-write</td><td>Transform multibyte (double- or half-width) characters to single width characters.&lt;br>Default value: OFF&lt;br>Possible values = ON, OFF</td><tr><tr><td>useconfigurablesecretkey</td><td>&lt;String></td><td>Read-write</td><td>Use configurable secret key in AppFw operations.&lt;br>Default value: OFF&lt;br>Possible values = ON, OFF</td><tr></tbody></table>
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
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","appfwsettings":{      "defaultprofile":<String_value>,      "undefaction":<String_value>,      "sessiontimeout":<Double_value>,      "learnratelimit":<Double_value>,      "sessionlifetime":<Double_value>,      "sessioncookiename":<String_value>,      "clientiploggingheader":<String_value>,      "importsizelimit":<Double_value>,      "signatureautoupdate":<String_value>,      "signatureurl":<String_value>,      "cookiepostencryptprefix":<String_value>,      "logmalformedreq":<String_value>,      "ceflogging":<String_value>,      "entitydecoding":<String_value>,      "useconfigurablesecretkey":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","appfwsettings":{      "defaultprofile":true,      "undefaction":true,      "sessiontimeout":true,      "learnratelimit":true,      "sessionlifetime":true,      "sessioncookiename":true,      "clientiploggingheader":true,      "importsizelimit":true,      "signatureautoupdate":true,      "signatureurl":true,      "cookiepostencryptprefix":true,      "logmalformedreq":true,      "ceflogging":true,      "entitydecoding":true,      "useconfigurablesecretkey":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/appfwsettings
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "appfwsettings": [ {      "defaultprofile":<String_value>,      "undefaction":<String_value>,      "sessiontimeout":<Double_value>,      "learnratelimit":<Double_value>,      "sessionlifetime":<Double_value>,      "sessioncookiename":<String_value>,      "clientiploggingheader":<String_value>,      "importsizelimit":<Double_value>,      "signatureautoupdate":<String_value>,      "signatureurl":<String_value>,      "cookiepostencryptprefix":<String_value>,      "logmalformedreq":<String_value>,      "ceflogging":<String_value>,      "entitydecoding":<String_value>,      "useconfigurablesecretkey":<String_value>}]}```



