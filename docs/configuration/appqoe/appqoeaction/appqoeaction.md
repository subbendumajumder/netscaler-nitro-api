#appqoeaction

Configuration for AppQoS action resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the AppQoE action. Must begin with a letter, number, or the underscore symbol (_). Other characters allowed, after the first character, are the hyphen (-), period (.) hash (#), space ( ), at (@), equals (=), and colon (:) characters. This is a mandatory argument.</td><tr><tr><td>priority</td><td>&lt;String></td><td>Read-write</td><td>Priority for queuing the request. If server resources are not available for a request that matches the configured rule, this option specifies a priority for queuing the request until the server resources are available again. If priority is not configured then Lowest priority will be used to queue the request.&lt;br>Possible values = HIGH, MEDIUM, LOW, LOWEST</td><tr><tr><td>respondwith</td><td>&lt;String></td><td>Read-write</td><td>Responder action to be taken when the threshold is reached. Available settings function as follows: ACS - Serve content from an alternative content service Threshold : maxConn or delay NS - Serve from the NetScaler appliance (built-in response) Threshold : maxConn or delay.&lt;br>Possible values = ACS, NS</td><tr><tr><td>customfile</td><td>&lt;String></td><td>Read-write</td><td>name of the HTML page object to use as the response.&lt;br>Minimum length = 1</td><tr><tr><td>altcontentsvcname</td><td>&lt;String></td><td>Read-write</td><td>Name of the alternative content service to be used in the ACS.&lt;br>Minimum length = 1&lt;br>Maximum length = 127</td><tr><tr><td>altcontentpath</td><td>&lt;String></td><td>Read-write</td><td>Path to the alternative content service to be used in the ACS.&lt;br>Minimum length = 4&lt;br>Maximum length = 127</td><tr><tr><td>polqdepth</td><td>&lt;Double></td><td>Read-write</td><td>Policy queue depth threshold value. When the policy queue size (number of requests queued for the policy binding this action is attached to) increases to the specified polqDepth value, subsequent requests are dropped to the lowest priority level.&lt;br>Minimum value = 0&lt;br>Maximum value = 4294967294</td><tr><tr><td>priqdepth</td><td>&lt;Double></td><td>Read-write</td><td>Queue depth threshold value per priorirty level. If the queue size (number of requests in the queue of that particular priorirty) on the virtual server to which this policy is bound, increases to the specified qDepth value, subsequent requests are dropped to the lowest priority level.&lt;br>Minimum value = 0&lt;br>Maximum value = 4294967294</td><tr><tr><td>maxconn</td><td>&lt;Double></td><td>Read-write</td><td>Maximum number of concurrent connections that can be open for requests that matches with rule.&lt;br>Minimum value = 1&lt;br>Maximum value = 4294967294</td><tr><tr><td>delay</td><td>&lt;Double></td><td>Read-write</td><td>Delay threshold, in microseconds, for requests that match the policys rule. If the delay statistics gathered for the matching request exceed the specified delay, configured action triggered for that request, if there is no action then requests are dropped to the lowest priority level.&lt;br>Minimum value = 1&lt;br>Maximum value = 599999999</td><tr><tr><td>dostrigexpression</td><td>&lt;String></td><td>Read-write</td><td>Optional expression to add second level check to trigger DoS actions. Specifically used for Analytics based DoS response generation.</td><tr><tr><td>dosaction</td><td>&lt;String></td><td>Read-write</td><td>DoS Action to take when vserver will be considered under DoS attack and corresponding rule matches. Mandatory if AppQoE actions are to be used for DoS attack prevention.&lt;br>Possible values = SimpleResponse, HICResponse</td><tr><tr><td>hits</td><td>&lt;Double></td><td>Read-only</td><td>.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
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
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>},"sessionid":"##sessionid","appqoeaction":{      "name":<String_value>,      "priority":<String_value>,      "respondwith":<String_value>,      "customfile":<String_value>,      "altcontentsvcname":<String_value>,      "altcontentpath":<String_value>,      "polqdepth":<Double_value>,      "priqdepth":<Double_value>,      "maxconn":<Double_value>,      "delay":<Double_value>,      "dostrigexpression":<String_value>,      "dosaction":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/appqoeaction/name_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/appqoeaction/name_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","appqoeaction":{      "name":<String_value>,      "priority":<String_value>,      "altcontentsvcname":<String_value>,      "altcontentpath":<String_value>,      "polqdepth":<Double_value>,      "priqdepth":<Double_value>,      "maxconn":<Double_value>,      "delay":<Double_value>,      "dostrigexpression":<String_value>,      "dosaction":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","appqoeaction":{      "name":<String_value>,      "priority":true,      "altcontentsvcname":true,      "altcontentpath":true,      "polqdepth":true,      "priqdepth":true,      "maxconn":true,      "delay":true,      "dosaction":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/appqoeaction
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/appqoeaction?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of appqoeaction resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/appqoeaction?view=summary
Use this query-parameter to get the summary output of appqoeaction resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/appqoeaction?pagesize=#no;pageno=#no
Use this query-parameter to get the appqoeaction resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/appqoeaction?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "appqoeaction": [ {      "name":<String_value>,      "hits":<Double_value>,      "priority":<String_value>,      "respondwith":<String_value>,      "polqdepth":<Double_value>,      "priqdepth":<Double_value>,      "altcontentsvcname":<String_value>,      "altcontentpath":<String_value>,      "maxconn":<Double_value>,      "delay":<Double_value>,      "customfile":<String_value>,      "dostrigexpression":<String_value>,      "dosaction":<String_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/appqoeaction/name_value&lt;String&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "appqoeaction": [ {      "name":<String_value>,      "hits":<Double_value>,      "priority":<String_value>,      "respondwith":<String_value>,      "polqdepth":<Double_value>,      "priqdepth":<Double_value>,      "altcontentsvcname":<String_value>,      "altcontentpath":<String_value>,      "maxconn":<Double_value>,      "delay":<Double_value>,      "customfile":<String_value>,      "dostrigexpression":<String_value>,      "dosaction":<String_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/appqoeaction?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",appqoeaction: [ { "__count": "#no"} ] }


