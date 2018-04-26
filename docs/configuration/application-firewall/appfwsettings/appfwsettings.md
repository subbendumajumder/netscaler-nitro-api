#appfwsettings

Configuration for AS settings resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>defaultprofile</td><td>&lt;String></td><td>Read-write</td><td>Profile to use when a connection does not match any policy. Default setting is APPFW_BYPASS, which sends unmatched connections back to the NetScaler appliance without attempting to filter them further.<br>Default value: APPFW_BYPASS<br>Minimum length = 1</td></tr><tr><td>undefaction</td><td>&lt;String></td><td>Read-write</td><td>Profile to use when an application firewall policy evaluates to undefined (UNDEF). <br>An UNDEF event indicates an internal error condition. The APPFW_BLOCK built-in profile is the default setting. You can specify a different built-in or user-created profile as the UNDEF profile.<br>Default value: APPFW_BLOCK<br>Minimum length = 1</td></tr><tr><td>sessiontimeout</td><td>&lt;Double></td><td>Read-write</td><td>Timeout, in seconds, after which a user session is terminated. Before continuing to use the protected web site, the user must establish a new session by opening a designated start URL.<br>Default value: 900<br>Minimum value = 1<br>Maximum value = 65535</td></tr><tr><td>learnratelimit</td><td>&lt;Double></td><td>Read-write</td><td>Maximum number of connections per second that the application firewall learning engine examines to generate new relaxations for learning-enabled security checks. The application firewall drops any connections above this limit from the list of connections used by the learning engine.<br>Default value: 400<br>Minimum value = 1<br>Maximum value = 1000</td></tr><tr><td>sessionlifetime</td><td>&lt;Double></td><td>Read-write</td><td>Maximum amount of time (in seconds) that the application firewall allows a user session to remain active, regardless of user activity. After this time, the user session is terminated. Before continuing to use the protected web site, the user must establish a new session by opening a designated start URL.<br>Default value: 0<br>Minimum value = 0<br>Maximum value = 2147483647</td></tr><tr><td>sessioncookiename</td><td>&lt;String></td><td>Read-write</td><td>Name of the session cookie that the application firewall uses to track user sessions. <br>Must begin with a letter or number, and can consist of from 1 to 31 letters, numbers, and the hyphen (-) and underscore (_) symbols.<br><br>The following requirement applies only to the NetScaler CLI:<br>If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my cookie name" or 'my cookie name').<br>Minimum length = 1</td></tr><tr><td>clientiploggingheader</td><td>&lt;String></td><td>Read-write</td><td>Name of an HTTP header that contains the IP address that the client used to connect to the protected web site or service.</td></tr><tr><td>importsizelimit</td><td>&lt;Double></td><td>Read-write</td><td>Cumulative total maximum number of bytes in web forms imported to a protected web site. If a user attempts to upload files with a total byte count higher than the specified limit, the application firewall blocks the request.<br>Default value: 134217728<br>Minimum value = 1<br>Maximum value = 268435456</td></tr><tr><td>signatureautoupdate</td><td>&lt;String></td><td>Read-write</td><td>Flag used to enable/disable auto update signatures.<br>Default value: OFF<br>Possible values = ON, OFF</td></tr><tr><td>signatureurl</td><td>&lt;String></td><td>Read-write</td><td>URL to download the mapping file from server.<br>Default value: https://s3.amazonaws.com/NSAppFwSignatures/SignaturesMapping.xml</td></tr><tr><td>cookiepostencryptprefix</td><td>&lt;String></td><td>Read-write</td><td>String that is prepended to all encrypted cookie values.<br>Minimum length = 1</td></tr><tr><td>logmalformedreq</td><td>&lt;String></td><td>Read-write</td><td>Log requests that are so malformed that application firewall parsing doesn't occur.<br>Default value: ON<br>Possible values = ON, OFF</td></tr><tr><td>geolocationlogging</td><td>&lt;String></td><td>Read-write</td><td>Enable Geo-Location Logging in CEF format logs.<br>Default value: OFF<br>Possible values = ON, OFF</td></tr><tr><td>ceflogging</td><td>&lt;String></td><td>Read-write</td><td>Enable CEF format logs.<br>Default value: OFF<br>Possible values = ON, OFF</td></tr><tr><td>entitydecoding</td><td>&lt;String></td><td>Read-write</td><td>Transform multibyte (double- or half-width) characters to single width characters.<br>Default value: OFF<br>Possible values = ON, OFF</td></tr><tr><td>useconfigurablesecretkey</td><td>&lt;String></td><td>Read-write</td><td>Use configurable secret key in AppFw operations.<br>Default value: OFF<br>Possible values = ON, OFF</td></tr><tr><td>sessionlimit</td><td>&lt;Double></td><td>Read-write</td><td>Maximum number of sessions that the application firewall allows to be active, regardless of user activity. After the max_limit reaches, No more user session will be created .<br>Default value: 100000<br>Minimum value = 0<br>Maximum value = 500000</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[UPDATE](#u)| [UNSET](#)| [GET (ALL)](#get-)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appfwsettings
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"appfwsettings":{"defaultprofile":<String_value>,"undefaction":<String_value>,"sessiontimeout":<Double_value>,"learnratelimit":<Double_value>,"sessionlifetime":<Double_value>,"sessioncookiename":<String_value>,"clientiploggingheader":<String_value>,"importsizelimit":<Double_value>,"signatureautoupdate":<String_value>,"signatureurl":<String_value>,"cookiepostencryptprefix":<String_value>,"logmalformedreq":<String_value>,"geolocationlogging":<String_value>,"ceflogging":<String_value>,"entitydecoding":<String_value>,"useconfigurablesecretkey":<String_value>,"sessionlimit":<Double_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appfwsettings?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"appfwsettings":{"defaultprofile":true,"undefaction":true,"sessiontimeout":true,"learnratelimit":true,"sessionlifetime":true,"sessioncookiename":true,"clientiploggingheader":true,"importsizelimit":true,"signatureautoupdate":true,"signatureurl":true,"cookiepostencryptprefix":true,"logmalformedreq":true,"geolocationlogging":true,"ceflogging":true,"entitydecoding":true,"useconfigurablesecretkey":true,"sessionlimit":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appfwsettings
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "appfwsettings": [ {"defaultprofile":<String_value>,"undefaction":<String_value>,"sessiontimeout":<Double_value>,"learnratelimit":<Double_value>,"sessionlifetime":<Double_value>,"sessioncookiename":<String_value>,"clientiploggingheader":<String_value>,"importsizelimit":<Double_value>,"signatureautoupdate":<String_value>,"signatureurl":<String_value>,"cookiepostencryptprefix":<String_value>,"logmalformedreq":<String_value>,"geolocationlogging":<String_value>,"ceflogging":<String_value>,"entitydecoding":<String_value>,"useconfigurablesecretkey":<String_value>,"sessionlimit":<Double_value>}]}```



