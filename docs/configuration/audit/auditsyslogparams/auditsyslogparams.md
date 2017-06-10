#auditsyslogparams

Configuration for system log parameters resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>serverip</td><td>&lt;String></td><td>Read-write</td><td>IP address of the syslog server.&lt;br>Minimum length = 1</td><tr><tr><td>serverport</td><td>&lt;Integer></td><td>Read-write</td><td>Port on which the syslog server accepts connections.&lt;br>Minimum value = 1</td><tr><tr><td>dateformat</td><td>&lt;String></td><td>Read-write</td><td>Format of dates in the logs.&lt;br>Supported formats are: &lt;br>* MMDDYYYY - U.S. style month/date/year format.&lt;br>* DDMMYYYY. European style -date/month/year format.&lt;br>* YYYYMMDD - ISO style year/month/date format.&lt;br>Possible values = MMDDYYYY, DDMMYYYY, YYYYMMDD</td><tr><tr><td>loglevel</td><td>&lt;String[]></td><td>Read-write</td><td>Types of information to be logged. &lt;br>Available settings function as follows: &lt;br>* ALL - All events.&lt;br>* EMERGENCY - Events that indicate an immediate crisis on the server.&lt;br>* ALERT - Events that might require action.&lt;br>* CRITICAL - Events that indicate an imminent server crisis.&lt;br>* ERROR - Events that indicate some type of error.&lt;br>* WARNING - Events that require action in the near future.&lt;br>* NOTICE - Events that the administrator should know about.&lt;br>* INFORMATIONAL - All but low-level events.&lt;br>* DEBUG - All events, in extreme detail.&lt;br>* NONE - No events.&lt;br>Possible values = ALL, EMERGENCY, ALERT, CRITICAL, ERROR, WARNING, NOTICE, INFORMATIONAL, DEBUG, NONE</td><tr><tr><td>logfacility</td><td>&lt;String></td><td>Read-write</td><td>Facility value, as defined in RFC 3164, assigned to the log message. &lt;br>Log facility values are numbers 0 to 7 (LOCAL0 through LOCAL7). Each number indicates where a specific message originated from, such as the NetScaler appliance itself, the VPN, or external.&lt;br>Possible values = LOCAL0, LOCAL1, LOCAL2, LOCAL3, LOCAL4, LOCAL5, LOCAL6, LOCAL7</td><tr><tr><td>tcp</td><td>&lt;String></td><td>Read-write</td><td>Log TCP messages.&lt;br>Possible values = NONE, ALL</td><tr><tr><td>acl</td><td>&lt;String></td><td>Read-write</td><td>Log access control list (ACL) messages.&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>timezone</td><td>&lt;String></td><td>Read-write</td><td>Time zone used for date and timestamps in the logs. &lt;br>Available settings function as follows: &lt;br>* GMT_TIME - Coordinated Universal Time.&lt;br>* LOCAL_TIME Use the servers timezone setting.&lt;br>Possible values = GMT_TIME, LOCAL_TIME</td><tr><tr><td>userdefinedauditlog</td><td>&lt;String></td><td>Read-write</td><td>Log user-configurable log messages to syslog. &lt;br>Setting this parameter to NO causes audit to ignore all user-configured message actions. Setting this parameter to YES causes audit to log user-configured message actions that meet the other logging criteria.&lt;br>Possible values = YES, NO</td><tr><tr><td>appflowexport</td><td>&lt;String></td><td>Read-write</td><td>Export log messages to AppFlow collectors.&lt;br>Appflow collectors are entities to which log messages can be sent so that some action can be performed on them.&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>lsn</td><td>&lt;String></td><td>Read-write</td><td>Log the LSN messages.&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>alg</td><td>&lt;String></td><td>Read-write</td><td>Log the ALG messages.&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>subscriberlog</td><td>&lt;String></td><td>Read-write</td><td>Log subscriber session event information.&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>dns</td><td>&lt;String></td><td>Read-write</td><td>Log DNS related syslog messages.&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>sslinterception</td><td>&lt;String></td><td>Read-write</td><td>Log SSL Interceptionn event information.&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>builtin</td><td>&lt;String[]></td><td>Read-only</td><td>Indicates that a variable is a built-in (SYSTEM INTERNAL) type.&lt;br>Possible values = MODIFIABLE, DELETABLE, IMMUTABLE, PARTITION_ALL</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[UPDATE](#update) | [UNSET](#unset) | [GET (ALL)](#get-(all))


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###update



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/auditsyslogparams
HTTP Method: PUT
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"auditsyslogparams":{      "serverip":<String_value>,      "serverport":<Integer_value>,      "dateformat":<String_value>,      "loglevel":<String[]_value>,      "logfacility":<String_value>,      "tcp":<String_value>,      "acl":<String_value>,      "timezone":<String_value>,      "userdefinedauditlog":<String_value>,      "appflowexport":<String_value>,      "lsn":<String_value>,      "alg":<String_value>,      "subscriberlog":<String_value>,      "dns":<String_value>,      "sslinterception":<String_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/auditsyslogparams?action=unset
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"auditsyslogparams":{      "serverip":true,      "serverport":true,      "loglevel":true,      "dateformat":true,      "logfacility":true,      "tcp":true,      "acl":true,      "timezone":true,      "userdefinedauditlog":true,      "appflowexport":true,      "lsn":true,      "alg":true,      "subscriberlog":true,      "dns":true,      "sslinterception":true}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/auditsyslogparams
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "auditsyslogparams": [ {      "name":<String_value>,      "serverip":<String_value>,      "serverport":<Integer_value>,      "dateformat":<String_value>,      "loglevel":<String[]_value>,      "logfacility":<String_value>,      "tcp":<String_value>,      "acl":<String_value>,      "timezone":<String_value>,      "userdefinedauditlog":<String_value>,      "appflowexport":<String_value>,      "builtin":<String[]_value>,      "lsn":<String_value>,      "alg":<String_value>,      "subscriberlog":<String_value>,      "dns":<String_value>,      "sslinterception":<String_value>}]}```



