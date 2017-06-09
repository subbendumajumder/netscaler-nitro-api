#systemsession

Configuration for system session resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>sid</td><td>&lt;Double></td><td>Read-write</td><td>ID of the system session about which to display information.&lt;br>Minimum value = 1</td><tr><tr><td>all</td><td>&lt;Boolean></td><td>Read-write</td><td>Terminate all the system sessions except the current session.</td><tr><tr><td>username</td><td>&lt;String></td><td>Read-only</td><td>user name of the session.</td><tr><tr><td>logintime</td><td>&lt;String></td><td>Read-only</td><td>logged-in time of this session.</td><tr><tr><td>lastactivitytime</td><td>&lt;String></td><td>Read-only</td><td>last activity time of on this session.</td><tr><tr><td>expirytime</td><td>&lt;Integer></td><td>Read-only</td><td>Time left in expire the session in seconds.</td><tr><tr><td>numofconnections</td><td>&lt;Double></td><td>Read-only</td><td>number of connection using this token.</td><tr><tr><td>currentconn</td><td>&lt;Boolean></td><td>Read-only</td><td>True if the token is used for current session.</td><tr><tr><td>clienttype</td><td>&lt;String></td><td>Read-only</td><td>client type of the session.&lt;br>Possible values = CLI, API, GUI</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[KILL](#kill) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###kill



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"kill"},"sessionid":"##sessionid","systemsession":{      "sid":<Double_value>,      "all":<Boolean_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/systemsession
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/systemsession?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of systemsession resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/systemsession?view=summary
Use this query-parameter to get the summary output of systemsession resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/systemsession?pagesize=#no;pageno=#no
Use this query-parameter to get the systemsession resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/systemsession?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "systemsession": [ {      "sid":<Double_value>,      "username":<String_value>,      "logintime":<String_value>,      "lastactivitytime":<String_value>,      "expirytime":<Integer_value>,      "numofconnections":<Double_value>,      "currentconn":<Boolean_value>,      "clienttype":<String_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/systemsession/sid_value&lt;Double&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "systemsession": [ {      "sid":<Double_value>,      "username":<String_value>,      "logintime":<String_value>,      "lastactivitytime":<String_value>,      "expirytime":<Integer_value>,      "numofconnections":<Double_value>,      "currentconn":<Boolean_value>,      "clienttype":<String_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/systemsession?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",systemsession: [ { "__count": "#no"} ] }


