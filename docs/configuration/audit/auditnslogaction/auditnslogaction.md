#auditnslogaction

Configuration for ns log action resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name of the nslog action. Must begin with a letter, number, or the underscore character (_), and must contain only letters, numbers, and the hyphen (-), period (.) pound (#), space ( ), at (@), equals (=), colon (:), and underscore characters. Cannot be changed after the nslog action is added. The following requirement applies only to the NetScaler CLI: If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, ?my nslog action? or ?my nslog action).&lt;br>Minimum length = 1</td><tr><tr><td>serverip</td><td>&lt;String></td><td>Read-write</td><td>IP address of the nslog server.&lt;br>Minimum length = 1</td><tr><tr><td>serverport</td><td>&lt;Integer></td><td>Read-write</td><td>Port on which the nslog server accepts connections.&lt;br>Minimum value = 1</td><tr><tr><td>loglevel</td><td>&lt;String[]></td><td>Read-write</td><td>Audit log level, which specifies the types of events to log. Available settings function as follows: * ALL - All events. * EMERGENCY - Events that indicate an immediate crisis on the server. * ALERT - Events that might require action. * CRITICAL - Events that indicate an imminent server crisis. * ERROR - Events that indicate some type of error. * WARNING - Events that require action in the near future. * NOTICE - Events that the administrator should know about. * INFORMATIONAL - All but low-level events. * DEBUG - All events, in extreme detail. * NONE - No events.&lt;br>Possible values = ALL, EMERGENCY, ALERT, CRITICAL, ERROR, WARNING, NOTICE, INFORMATIONAL, DEBUG, NONE</td><tr><tr><td>dateformat</td><td>&lt;String></td><td>Read-write</td><td>Format of dates in the logs. Supported formats are: * MMDDYYYY - U.S. style month/date/year format. * DDMMYYYY - European style date/month/year format. * YYYYMMDD - ISO style year/month/date format.&lt;br>Possible values = MMDDYYYY, DDMMYYYY, YYYYMMDD</td><tr><tr><td>logfacility</td><td>&lt;String></td><td>Read-write</td><td>Facility value, as defined in RFC 3164, assigned to the log message. Log facility values are numbers 0 to 7 (LOCAL0 through LOCAL7). Each number indicates where a specific message originated from, such as the NetScaler appliance itself, the VPN, or external.&lt;br>Possible values = LOCAL0, LOCAL1, LOCAL2, LOCAL3, LOCAL4, LOCAL5, LOCAL6, LOCAL7</td><tr><tr><td>tcp</td><td>&lt;String></td><td>Read-write</td><td>Log TCP messages.&lt;br>Possible values = NONE, ALL</td><tr><tr><td>acl</td><td>&lt;String></td><td>Read-write</td><td>Log access control list (ACL) messages.&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>timezone</td><td>&lt;String></td><td>Read-write</td><td>Time zone used for date and timestamps in the logs. Available settings function as follows: * GMT_TIME. Coordinated Universal Time. * LOCAL_TIME. The server?s timezone setting.&lt;br>Possible values = GMT_TIME, LOCAL_TIME</td><tr><tr><td>userdefinedauditlog</td><td>&lt;String></td><td>Read-write</td><td>Log user-configurable log messages to nslog. Setting this parameter to NO causes auditing to ignore all user-configured message actions. Setting this parameter to YES causes auditing to log user-configured message actions that meet the other logging criteria.&lt;br>Possible values = YES, NO</td><tr><tr><td>appflowexport</td><td>&lt;String></td><td>Read-write</td><td>Export log messages to AppFlow collectors. Appflow collectors are entities to which log messages can be sent so that some action can be performed on them.&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>lsn</td><td>&lt;String></td><td>Read-write</td><td>Log the LSN messages.&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>alg</td><td>&lt;String></td><td>Read-write</td><td>Log the ALG messages.&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>builtin</td><td>&lt;String[]></td><td>Read-only</td><td>Indicates that a variable is a built-in (SYSTEM INTERNAL) type.&lt;br>Possible values = MODIFIABLE, DELETABLE, IMMUTABLE, PARTITION_ALL</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [DELETE](#delete) | [UPDATE](#update) | [UNSET](#unset) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>},"sessionid":"##sessionid","auditnslogaction":{      "name":<String_value>,      "serverip":<String_value>,      "serverport":<Integer_value>,      "loglevel":<String[]_value>,      "dateformat":<String_value>,      "logfacility":<String_value>,      "tcp":<String_value>,      "acl":<String_value>,      "timezone":<String_value>,      "userdefinedauditlog":<String_value>,      "appflowexport":<String_value>,      "lsn":<String_value>,      "alg":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/auditnslogaction/name_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/auditnslogaction/name_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","auditnslogaction":{      "name":<String_value>,      "serverip":<String_value>,      "serverport":<Integer_value>,      "loglevel":<String[]_value>,      "dateformat":<String_value>,      "logfacility":<String_value>,      "tcp":<String_value>,      "acl":<String_value>,      "timezone":<String_value>,      "userdefinedauditlog":<String_value>,      "appflowexport":<String_value>,      "lsn":<String_value>,      "alg":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","auditnslogaction":{      "name":<String_value>,      "serverport":true,      "loglevel":true,      "dateformat":true,      "logfacility":true,      "tcp":true,      "acl":true,      "timezone":true,      "userdefinedauditlog":true,      "appflowexport":true,      "lsn":true,      "alg":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/auditnslogaction
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/auditnslogaction?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of auditnslogaction resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/auditnslogaction?view=summary
Use this query-parameter to get the summary output of auditnslogaction resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/auditnslogaction?pagesize=#no;pageno=#no
Use this query-parameter to get the auditnslogaction resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/auditnslogaction?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "auditnslogaction": [ {      "name":<String_value>,      "serverip":<String_value>,      "serverport":<Integer_value>,      "loglevel":<String[]_value>,      "dateformat":<String_value>,      "logfacility":<String_value>,      "tcp":<String_value>,      "acl":<String_value>,      "timezone":<String_value>,      "userdefinedauditlog":<String_value>,      "appflowexport":<String_value>,      "builtin":<String[]_value>,      "lsn":<String_value>,      "alg":<String_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/auditnslogaction/name_value&lt;String&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "auditnslogaction": [ {      "name":<String_value>,      "serverip":<String_value>,      "serverport":<Integer_value>,      "loglevel":<String[]_value>,      "dateformat":<String_value>,      "logfacility":<String_value>,      "tcp":<String_value>,      "acl":<String_value>,      "timezone":<String_value>,      "userdefinedauditlog":<String_value>,      "appflowexport":<String_value>,      "builtin":<String[]_value>,      "lsn":<String_value>,      "alg":<String_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/auditnslogaction?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",auditnslogaction: [ { "__count": "#no"} ] }


