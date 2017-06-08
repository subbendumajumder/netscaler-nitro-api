#auditmessages

Configuration for audit message resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>loglevel</td><td>&lt;String[]></td><td>Read-write</td><td>Audit log level filter, which specifies the types of events to display. The following loglevels are valid: * ALL - All events. * EMERGENCY - Events that indicate an immediate crisis on the server. * ALERT - Events that might require action. * CRITICAL - Events that indicate an imminent server crisis. * ERROR - Events that indicate some type of error. * WARNING - Events that require action in the near future. * NOTICE - Events that the administrator should know about. * INFORMATIONAL - All but low-level events. * DEBUG - All events, in extreme detail.&lt;br>Possible values = ALL, EMERGENCY, ALERT, CRITICAL, ERROR, WARNING, NOTICE, INFORMATIONAL, DEBUG</td><tr><tr><td>numofmesgs</td><td>&lt;Double></td><td>Read-write</td><td>Number of log messages to be displayed.&lt;br>Default value: 20&lt;br>Minimum value = 1&lt;br>Maximum value = 256</td><tr><tr><td>value</td><td>&lt;String></td><td>Read-only</td><td>The Audit message.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[GET (ALL)](#get-(all)) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/auditmessages
Query-parameters:
args
http://&lt;NSIP&gt;/nitro/v1/config/auditmessages?args=      "loglevel":&lt;String[]_value&gt;,      "numofmesgs":&lt;Double_value&gt;,
Use this query-parameter to get auditmessages resources based on additional properties.


filter
http://&lt;NSIP&gt;/nitro/v1/config/auditmessages?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of auditmessages resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/auditmessages?view=summary
Use this query-parameter to get the summary output of auditmessages resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/auditmessages?pagesize=#no;pageno=#no
Use this query-parameter to get the auditmessages resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/auditmessages?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "auditmessages": [ {      "loglevel":<String[]_value>,      "numofmesgs":<Double_value>,      "value":<String_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/auditmessages?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",auditmessages: [ { "__count": "#no"} ] }


