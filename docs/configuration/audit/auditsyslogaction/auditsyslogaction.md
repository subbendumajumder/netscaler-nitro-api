#auditsyslogaction

Configuration for system log action resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name of the syslog action. Must begin with a letter, number, or the underscore character (_), and must contain only letters, numbers, and the hyphen (-), period (.) pound (#), space ( ), at (@), equals (=), colon (:), and underscore characters. Cannot be changed after the syslog action is added.&lt;br>&lt;br>The following requirement applies only to the NetScaler CLI:&lt;br>If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, ?my syslog action? or ?my syslog action).&lt;br>Minimum length = 1</td><tr><tr><td>serverip</td><td>&lt;String></td><td>Read-write</td><td>IP address of the syslog server.&lt;br>Minimum length = 1</td><tr><tr><td>serverdomainname</td><td>&lt;String></td><td>Read-write</td><td>SYSLOG server name as a FQDN. Mutually exclusive with serverIP/lbVserverName.&lt;br>Minimum length = 1&lt;br>Maximum length = 255</td><tr><tr><td>domainresolveretry</td><td>&lt;Integer></td><td>Read-write</td><td>Time, in seconds, for which the NetScaler appliance waits before sending another DNS query to resolve the host name of the syslog server if the last query failed.&lt;br>Default value: 5&lt;br>Minimum value = 5&lt;br>Maximum value = 20939</td><tr><tr><td>lbvservername</td><td>&lt;String></td><td>Read-write</td><td>Name of the LB vserver. Mutually exclusive with syslog serverIP/serverName.&lt;br>Minimum length = 1&lt;br>Maximum length = 127</td><tr><tr><td>serverport</td><td>&lt;Integer></td><td>Read-write</td><td>Port on which the syslog server accepts connections.&lt;br>Minimum value = 1</td><tr><tr><td>loglevel</td><td>&lt;String[]></td><td>Read-write</td><td>Audit log level, which specifies the types of events to log. &lt;br>Available values function as follows: &lt;br>* ALL - All events.&lt;br>* EMERGENCY - Events that indicate an immediate crisis on the server.&lt;br>* ALERT - Events that might require action.&lt;br>* CRITICAL - Events that indicate an imminent server crisis.&lt;br>* ERROR - Events that indicate some type of error.&lt;br>* WARNING - Events that require action in the near future.&lt;br>* NOTICE - Events that the administrator should know about.&lt;br>* INFORMATIONAL - All but low-level events.&lt;br>* DEBUG - All events, in extreme detail.&lt;br>* NONE - No events.&lt;br>Possible values = ALL, EMERGENCY, ALERT, CRITICAL, ERROR, WARNING, NOTICE, INFORMATIONAL, DEBUG, NONE</td><tr><tr><td>dateformat</td><td>&lt;String></td><td>Read-write</td><td>Format of dates in the logs.&lt;br>Supported formats are: &lt;br>* MMDDYYYY. -U.S. style month/date/year format.&lt;br>* DDMMYYYY - European style date/month/year format.&lt;br>* YYYYMMDD - ISO style year/month/date format.&lt;br>Possible values = MMDDYYYY, DDMMYYYY, YYYYMMDD</td><tr><tr><td>logfacility</td><td>&lt;String></td><td>Read-write</td><td>Facility value, as defined in RFC 3164, assigned to the log message. &lt;br>Log facility values are numbers 0 to 7 (LOCAL0 through LOCAL7). Each number indicates where a specific message originated from, such as the NetScaler appliance itself, the VPN, or external.&lt;br>Possible values = LOCAL0, LOCAL1, LOCAL2, LOCAL3, LOCAL4, LOCAL5, LOCAL6, LOCAL7</td><tr><tr><td>tcp</td><td>&lt;String></td><td>Read-write</td><td>Log TCP messages.&lt;br>Possible values = NONE, ALL</td><tr><tr><td>acl</td><td>&lt;String></td><td>Read-write</td><td>Log access control list (ACL) messages.&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>timezone</td><td>&lt;String></td><td>Read-write</td><td>Time zone used for date and timestamps in the logs. &lt;br>Supported settings are: &lt;br>* GMT_TIME. Coordinated Universal time.&lt;br>* LOCAL_TIME. Use the server?s timezone setting.&lt;br>Possible values = GMT_TIME, LOCAL_TIME</td><tr><tr><td>userdefinedauditlog</td><td>&lt;String></td><td>Read-write</td><td>Log user-configurable log messages to syslog. &lt;br>Setting this parameter to NO causes auditing to ignore all user-configured message actions. Setting this parameter to YES causes auditing to log user-configured message actions that meet the other logging criteria.&lt;br>Possible values = YES, NO</td><tr><tr><td>appflowexport</td><td>&lt;String></td><td>Read-write</td><td>Export log messages to AppFlow collectors.&lt;br>Appflow collectors are entities to which log messages can be sent so that some action can be performed on them.&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>lsn</td><td>&lt;String></td><td>Read-write</td><td>Log lsn info.&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>alg</td><td>&lt;String></td><td>Read-write</td><td>Log alg info.&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>subscriberlog</td><td>&lt;String></td><td>Read-write</td><td>Log subscriber session event information.&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>transport</td><td>&lt;String></td><td>Read-write</td><td>Transport type used to send auditlogs to syslog server. Default type is UDP.&lt;br>Possible values = TCP, UDP</td><tr><tr><td>tcpprofilename</td><td>&lt;String></td><td>Read-write</td><td>Name of the TCP profile whose settings are to be applied to the audit server info to tune the TCP connection parameters.&lt;br>Minimum length = 1&lt;br>Maximum length = 127</td><tr><tr><td>maxlogdatasizetohold</td><td>&lt;Double></td><td>Read-write</td><td>Max size of log data that can be held in NSB chain of server info.&lt;br>Default value: 500&lt;br>Minimum value = 50&lt;br>Maximum value = 25600</td><tr><tr><td>dns</td><td>&lt;String></td><td>Read-write</td><td>Log DNS related syslog messages.&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>netprofile</td><td>&lt;String></td><td>Read-write</td><td>Name of the network profile.&lt;br>The SNIP configured in the network profile will be used as source IP while sending log messages.&lt;br>Minimum length = 1&lt;br>Maximum length = 127</td><tr><tr><td>domainresolvenow</td><td>&lt;Boolean></td><td>Read-write</td><td>Immediately send a DNS query to resolve the servers domain name.</td><tr><tr><td>ip</td><td>&lt;String></td><td>Read-only</td><td>The resolved IP address of the syslog server.</td><tr><tr><td>builtin</td><td>&lt;String[]></td><td>Read-only</td><td>Indicates that a variable is a built-in (SYSTEM INTERNAL) type.&lt;br>Possible values = MODIFIABLE, DELETABLE, IMMUTABLE, PARTITION_ALL</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [DELETE](#delete) | [UPDATE](#update) | [UNSET](#unset) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/auditsyslogaction
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"auditsyslogaction":{      "name":<String_value>,      "serverip":<String_value>,      "serverdomainname":<String_value>,      "domainresolveretry":<Integer_value>,      "lbvservername":<String_value>,      "serverport":<Integer_value>,      "loglevel":<String[]_value>,      "dateformat":<String_value>,      "logfacility":<String_value>,      "tcp":<String_value>,      "acl":<String_value>,      "timezone":<String_value>,      "userdefinedauditlog":<String_value>,      "appflowexport":<String_value>,      "lsn":<String_value>,      "alg":<String_value>,      "subscriberlog":<String_value>,      "transport":<String_value>,      "tcpprofilename":<String_value>,      "maxlogdatasizetohold":<Double_value>,      "dns":<String_value>,      "netprofile":<String_value>}}```
Response:
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/auditsyslogaction/name_value&lt;String&gt;
HTTP Method: DELETE
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/auditsyslogaction
HTTP Method: PUT
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"auditsyslogaction":{      "name":<String_value>,      "serverip":<String_value>,      "serverdomainname":<String_value>,      "lbvservername":<String_value>,      "domainresolveretry":<Integer_value>,      "domainresolvenow":<Boolean_value>,      "serverport":<Integer_value>,      "loglevel":<String[]_value>,      "dateformat":<String_value>,      "logfacility":<String_value>,      "tcp":<String_value>,      "acl":<String_value>,      "timezone":<String_value>,      "userdefinedauditlog":<String_value>,      "appflowexport":<String_value>,      "lsn":<String_value>,      "alg":<String_value>,      "subscriberlog":<String_value>,      "tcpprofilename":<String_value>,      "maxlogdatasizetohold":<Double_value>,      "dns":<String_value>,      "netprofile":<String_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/auditsyslogaction?action=unset
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"auditsyslogaction":{      "name":<String_value>,      "serverport":true,      "loglevel":true,      "dateformat":true,      "logfacility":true,      "tcp":true,      "acl":true,      "timezone":true,      "userdefinedauditlog":true,      "appflowexport":true,      "lsn":true,      "alg":true,      "subscriberlog":true,      "tcpprofilename":true,      "maxlogdatasizetohold":true,      "dns":true,      "netprofile":true}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/auditsyslogaction
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/auditsyslogaction?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


filter
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/auditsyslogaction?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of auditsyslogaction resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/auditsyslogaction?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).


pagination
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/auditsyslogaction?pagesize=#no;pageno=#no
Use this query-parameter to get the auditsyslogaction resources in chunks.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "auditsyslogaction": [ {      "name":<String_value>,      "serverip":<String_value>,      "serverdomainname":<String_value>,      "ip":<String_value>,      "lbvservername":<String_value>,      "domainresolveretry":<Integer_value>,      "serverport":<Integer_value>,      "loglevel":<String[]_value>,      "dateformat":<String_value>,      "logfacility":<String_value>,      "tcp":<String_value>,      "acl":<String_value>,      "timezone":<String_value>,      "userdefinedauditlog":<String_value>,      "appflowexport":<String_value>,      "builtin":<String[]_value>,      "lsn":<String_value>,      "alg":<String_value>,      "subscriberlog":<String_value>,      "transport":<String_value>,      "tcpprofilename":<String_value>,      "maxlogdatasizetohold":<Double_value>,      "dns":<String_value>,      "netprofile":<String_value>}]}```



###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/auditsyslogaction/name_value&lt;String&gt;
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/auditsyslogaction/name_value&lt;String&gt;?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/auditsyslogaction/name_value&lt;String&gt;?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "auditsyslogaction": [ {      "name":<String_value>,      "serverip":<String_value>,      "serverdomainname":<String_value>,      "ip":<String_value>,      "lbvservername":<String_value>,      "domainresolveretry":<Integer_value>,      "serverport":<Integer_value>,      "loglevel":<String[]_value>,      "dateformat":<String_value>,      "logfacility":<String_value>,      "tcp":<String_value>,      "acl":<String_value>,      "timezone":<String_value>,      "userdefinedauditlog":<String_value>,      "appflowexport":<String_value>,      "builtin":<String[]_value>,      "lsn":<String_value>,      "alg":<String_value>,      "subscriberlog":<String_value>,      "transport":<String_value>,      "tcpprofilename":<String_value>,      "maxlogdatasizetohold":<Double_value>,      "dns":<String_value>,      "netprofile":<String_value>}]}```



###count



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/auditsyslogaction?count=yes
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: 
{ "auditsyslogaction": [ { "__count": "#no"} ] }


