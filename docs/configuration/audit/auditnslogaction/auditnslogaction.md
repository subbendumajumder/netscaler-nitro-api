#auditnslogaction

Configuration for ns log action resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name of the nslog action. Must begin with a letter, number, or the underscore character (_), and must contain only letters, numbers, and the hyphen (-), period (.) pound (#), space ( ), at (@), equals (=), colon (:), and underscore characters. Cannot be changed after the nslog action is added.<br><br>The following requirement applies only to the NetScaler CLI:<br>If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my nslog action" or 'my nslog action').<br>Minimum length = 1</td></tr><tr><td>serverip</td><td>&lt;String></td><td>Read-write</td><td>IP address of the nslog server.<br>Minimum length = 1</td></tr><tr><td>serverdomainname</td><td>&lt;String></td><td>Read-write</td><td>Auditserver name as a FQDN. Mutually exclusive with serverIP.<br>Minimum length = 1<br>Maximum length = 255</td></tr><tr><td>domainresolveretry</td><td>&lt;Integer></td><td>Read-write</td><td>Time, in seconds, for which the NetScaler appliance waits before sending another DNS query to resolve the host name of the audit server if the last query failed.<br>Default value: 5<br>Minimum value = 5<br>Maximum value = 20939</td></tr><tr><td>serverport</td><td>&lt;Integer></td><td>Read-write</td><td>Port on which the nslog server accepts connections.<br>Minimum value = 1</td></tr><tr><td>loglevel</td><td>&lt;String[]></td><td>Read-write</td><td>Audit log level, which specifies the types of events to log. <br>Available settings function as follows: <br>* ALL - All events.<br>* EMERGENCY - Events that indicate an immediate crisis on the server.<br>* ALERT - Events that might require action.<br>* CRITICAL - Events that indicate an imminent server crisis.<br>* ERROR - Events that indicate some type of error.<br>* WARNING - Events that require action in the near future.<br>* NOTICE - Events that the administrator should know about.<br>* INFORMATIONAL - All but low-level events.<br>* DEBUG - All events, in extreme detail.<br>* NONE - No events.<br>Possible values = ALL, EMERGENCY, ALERT, CRITICAL, ERROR, WARNING, NOTICE, INFORMATIONAL, DEBUG, NONE</td></tr><tr><td>dateformat</td><td>&lt;String></td><td>Read-write</td><td>Format of dates in the logs.<br>Supported formats are: <br>* MMDDYYYY - U.S. style month/date/year format.<br>* DDMMYYYY - European style date/month/year format.<br>* YYYYMMDD - ISO style year/month/date format.<br>Possible values = MMDDYYYY, DDMMYYYY, YYYYMMDD</td></tr><tr><td>logfacility</td><td>&lt;String></td><td>Read-write</td><td>Facility value, as defined in RFC 3164, assigned to the log message. <br>Log facility values are numbers 0 to 7 (LOCAL0 through LOCAL7). Each number indicates where a specific message originated from, such as the NetScaler appliance itself, the VPN, or external.<br>Possible values = LOCAL0, LOCAL1, LOCAL2, LOCAL3, LOCAL4, LOCAL5, LOCAL6, LOCAL7</td></tr><tr><td>tcp</td><td>&lt;String></td><td>Read-write</td><td>Log TCP messages.<br>Possible values = NONE, ALL</td></tr><tr><td>acl</td><td>&lt;String></td><td>Read-write</td><td>Log access control list (ACL) messages.<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>timezone</td><td>&lt;String></td><td>Read-write</td><td>Time zone used for date and timestamps in the logs. <br>Available settings function as follows: <br>* GMT_TIME. Coordinated Universal Time.<br>* LOCAL_TIME. The server's timezone setting.<br>Possible values = GMT_TIME, LOCAL_TIME</td></tr><tr><td>userdefinedauditlog</td><td>&lt;String></td><td>Read-write</td><td>Log user-configurable log messages to nslog.<br>Setting this parameter to NO causes auditing to ignore all user-configured message actions. Setting this parameter to YES causes auditing to log user-configured message actions that meet the other logging criteria.<br>Possible values = YES, NO</td></tr><tr><td>appflowexport</td><td>&lt;String></td><td>Read-write</td><td>Export log messages to AppFlow collectors.<br>Appflow collectors are entities to which log messages can be sent so that some action can be performed on them.<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>lsn</td><td>&lt;String></td><td>Read-write</td><td>Log the LSN messages.<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>alg</td><td>&lt;String></td><td>Read-write</td><td>Log the ALG messages.<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>subscriberlog</td><td>&lt;String></td><td>Read-write</td><td>Log subscriber session event information.<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>sslinterception</td><td>&lt;String></td><td>Read-write</td><td>Log SSL Interception event information.<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>urlfiltering</td><td>&lt;String></td><td>Read-write</td><td>Log URL filtering event information.<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>domainresolvenow</td><td>&lt;Boolean></td><td>Read-write</td><td>Immediately send a DNS query to resolve the server's domain name.</td></tr><tr><td>ip</td><td>&lt;String></td><td>Read-only</td><td>The resolved IP address of the auditserver.</td></tr><tr><td>builtin</td><td>&lt;String[]></td><td>Read-only</td><td>Indicates that a variable is a built-in (SYSTEM INTERNAL) type.<br>Possible values = MODIFIABLE, DELETABLE, IMMUTABLE, PARTITION_ALL</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD]()| [DELETE](#d)| [UPDATE](#u)| [UNSET](#)| [GET (ALL)](#get-)| [GET]()| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/auditnslogaction
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"auditnslogaction":{<b>"name":<String_value>,</b>"serverip":<String_value>,"serverdomainname":<String_value>,"domainresolveretry":<Integer_value>,"serverport":<Integer_value>,<b>"loglevel":<String[]_value>,</b>"dateformat":<String_value>,"logfacility":<String_value>,"tcp":<String_value>,"acl":<String_value>,"timezone":<String_value>,"userdefinedauditlog":<String_value>,"appflowexport":<String_value>,"lsn":<String_value>,"alg":<String_value>,"subscriberlog":<String_value>,"sslinterception":<String_value>,"urlfiltering":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/auditnslogaction/name_value&lt;String&gt;
<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/auditnslogaction
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"auditnslogaction":{<b>"name":<String_value>,</b>"serverip":<String_value>,"serverdomainname":<String_value>,"domainresolveretry":<Integer_value>,"domainresolvenow":<Boolean_value>,"serverport":<Integer_value>,"loglevel":<String[]_value>,"dateformat":<String_value>,"logfacility":<String_value>,"tcp":<String_value>,"acl":<String_value>,"timezone":<String_value>,"userdefinedauditlog":<String_value>,"appflowexport":<String_value>,"lsn":<String_value>,"alg":<String_value>,"subscriberlog":<String_value>,"sslinterception":<String_value>,"urlfiltering":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/auditnslogaction?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"auditnslogaction":{<b>"name":<String_value>,</b>"serverport":true,"loglevel":true,"dateformat":true,"logfacility":true,"tcp":true,"acl":true,"timezone":true,"userdefinedauditlog":true,"appflowexport":true,"lsn":true,"alg":true,"subscriberlog":true,"sslinterception":true,"urlfiltering":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/auditnslogaction
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/auditnslogaction?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/auditnslogaction?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of auditnslogaction resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/auditnslogaction?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/auditnslogaction?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the auditnslogaction resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "auditnslogaction": [ {"name":<String_value>,"serverip":<String_value>,"serverdomainname":<String_value>,"domainresolveretry":<Integer_value>,"domainresolvenow":<Boolean_value>,"ip":<String_value>,"serverport":<Integer_value>,"loglevel":<String[]_value>,"dateformat":<String_value>,"logfacility":<String_value>,"tcp":<String_value>,"acl":<String_value>,"timezone":<String_value>,"userdefinedauditlog":<String_value>,"appflowexport":<String_value>,"builtin":<String[]_value>,"lsn":<String_value>,"alg":<String_value>,"subscriberlog":<String_value>,"sslinterception":<String_value>,"urlfiltering":<String_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/auditnslogaction/name_value&lt;String&gt;
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/auditnslogaction/name_value&lt;String&gt;?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/auditnslogaction/name_value&lt;String&gt;?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "auditnslogaction": [ {"name":<String_value>,"serverip":<String_value>,"serverdomainname":<String_value>,"domainresolveretry":<Integer_value>,"domainresolvenow":<Boolean_value>,"ip":<String_value>,"serverport":<Integer_value>,"loglevel":<String[]_value>,"dateformat":<String_value>,"logfacility":<String_value>,"tcp":<String_value>,"acl":<String_value>,"timezone":<String_value>,"userdefinedauditlog":<String_value>,"appflowexport":<String_value>,"builtin":<String[]_value>,"lsn":<String_value>,"alg":<String_value>,"subscriberlog":<String_value>,"sslinterception":<String_value>,"urlfiltering":<String_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/auditnslogaction?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "auditnslogaction": [ { "__count": "#no"} ] }```



