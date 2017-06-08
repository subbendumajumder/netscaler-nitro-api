#nshttpprofile

Configuration for HTTP profile resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for an HTTP profile. Must begin with a letter, number, or the underscore \\(_\\) character. Other characters allowed, after the first character, are the hyphen \\(-\\), period \\(.\\), hash \\(\\#\\), space \\( \\), at \\(@\\), and equal \\(=\\) characters. The name of a HTTP profile cannot be changed after it is created. CLI Users: If the name includes one or more spaces, enclose the name in double or single quotation marks \\(for example, "my http profile" or my http profile\\).&lt;br>Minimum length = 1&lt;br>Maximum length = 127</td><tr><tr><td>dropinvalreqs</td><td>&lt;String></td><td>Read-write</td><td>Drop invalid HTTP requests or responses.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>markhttp09inval</td><td>&lt;String></td><td>Read-write</td><td>Mark HTTP/0.9 requests as invalid.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>markconnreqinval</td><td>&lt;String></td><td>Read-write</td><td>Mark CONNECT requests as invalid.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>cmponpush</td><td>&lt;String></td><td>Read-write</td><td>Start data compression on receiving a TCP packet with PUSH flag set.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>conmultiplex</td><td>&lt;String></td><td>Read-write</td><td>Reuse server connections for requests from more than one client connections.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>maxreusepool</td><td>&lt;Double></td><td>Read-write</td><td>Maximum limit on the number of connections, from the NetScaler to a particular server that are kept in the reuse pool. This setting is helpful for optimal memory utilization and for reducing the idle connections to the server just after the peak time.&lt;br>Minimum value = 0&lt;br>Maximum value = 360000</td><tr><tr><td>dropextracrlf</td><td>&lt;String></td><td>Read-write</td><td>Drop any extra CR and LF characters present after the header.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>incomphdrdelay</td><td>&lt;Double></td><td>Read-write</td><td>Maximum time to wait, in milliseconds, between incomplete header packets. If the header packets take longer to arrive at NetScaler, the connection is silently dropped.&lt;br>Default value: 7000&lt;br>Minimum value = 0&lt;br>Maximum value = 360000</td><tr><tr><td>websocket</td><td>&lt;String></td><td>Read-write</td><td>HTTP connection to be upgraded to a web socket connection. Once upgraded, NetScaler does not process Layer 7 traffic on this connection.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>rtsptunnel</td><td>&lt;String></td><td>Read-write</td><td>Allow RTSP tunnel in HTTP. Once application/x-rtsp-tunnelled is seen in Accept or Content-Type header, NetScaler does not process Layer 7 traffic on this connection.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>reqtimeout</td><td>&lt;Double></td><td>Read-write</td><td>Time, in seconds, within which the HTTP request must complete. If the request does not complete within this time, the specified request timeout action is executed.&lt;br>Minimum value = 0&lt;br>Maximum value = 86400</td><tr><tr><td>adpttimeout</td><td>&lt;String></td><td>Read-write</td><td>Adapts the configured request timeout based on flow conditions. The timeout is increased or decreased internally and applied on the flow.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>reqtimeoutaction</td><td>&lt;String></td><td>Read-write</td><td>Action to take when the HTTP request does not complete within the specified request timeout duration. You can configure the following actions: * RESET - Send RST (reset) to client when timeout occurs. * DROP - Drop silently when timeout occurs. * Custom responder action - Name of the responder action to trigger when timeout occurs, used to send custom message.</td><tr><tr><td>dropextradata</td><td>&lt;String></td><td>Read-write</td><td>Drop any extra data when server sends more data than the specified content-length.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>weblog</td><td>&lt;String></td><td>Read-write</td><td>Enable or disable web logging.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>clientiphdrexpr</td><td>&lt;String></td><td>Read-write</td><td>Name of the header that contains the real client IP address.</td><tr><tr><td>maxreq</td><td>&lt;Double></td><td>Read-write</td><td>Maximum requests allowed on a single connection.&lt;br>Default value: 0&lt;br>Minimum value = 0&lt;br>Maximum value = 65534</td><tr><tr><td>persistentetag</td><td>&lt;String></td><td>Read-write</td><td>Generate the persistent NetScaler specific ETag for the HTTP response with ETag header.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>spdy</td><td>&lt;String></td><td>Read-write</td><td>Enable SPDYv2 or SPDYv3 or both over SSL vserver. SSL will advertise SPDY support during NPN Handshake. Both SPDY versions are enabled when this parameter is set to BOTH.&lt;br>Default value: DISABLED&lt;br>Possible values = DISABLED, ENABLED, V2, V3</td><tr><tr><td>reusepooltimeout</td><td>&lt;Double></td><td>Read-write</td><td>Idle timeout (in seconds) for server connections in re-use pool. Connections in the re-use pool are flushed, if they remain idle for the configured timeout.&lt;br>Default value: 0&lt;br>Minimum value = 0&lt;br>Maximum value = 31536000</td><tr><tr><td>maxheaderlen</td><td>&lt;Double></td><td>Read-write</td><td>Number of bytes to be queued to look for complete header before returning error. If complete header is not obtained after queuing these many bytes, request will be marked as invalid and no L7 processing will be done for that TCP connection.&lt;br>Default value: 24820&lt;br>Minimum value = 2048&lt;br>Maximum value = 61440</td><tr><tr><td>refcnt</td><td>&lt;Double></td><td>Read-only</td><td>Number of entities using this profile.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
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
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>},"sessionid":"##sessionid","nshttpprofile":{      "name":<String_value>,      "dropinvalreqs":<String_value>,      "markhttp09inval":<String_value>,      "markconnreqinval":<String_value>,      "cmponpush":<String_value>,      "conmultiplex":<String_value>,      "maxreusepool":<Double_value>,      "dropextracrlf":<String_value>,      "incomphdrdelay":<Double_value>,      "websocket":<String_value>,      "rtsptunnel":<String_value>,      "reqtimeout":<Double_value>,      "adpttimeout":<String_value>,      "reqtimeoutaction":<String_value>,      "dropextradata":<String_value>,      "weblog":<String_value>,      "clientiphdrexpr":<String_value>,      "maxreq":<Double_value>,      "persistentetag":<String_value>,      "spdy":<String_value>,      "reusepooltimeout":<Double_value>,      "maxheaderlen":<Double_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/nshttpprofile/name_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/nshttpprofile/name_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","nshttpprofile":{      "name":<String_value>,      "dropinvalreqs":<String_value>,      "markhttp09inval":<String_value>,      "markconnreqinval":<String_value>,      "cmponpush":<String_value>,      "conmultiplex":<String_value>,      "maxreusepool":<Double_value>,      "dropextracrlf":<String_value>,      "incomphdrdelay":<Double_value>,      "websocket":<String_value>,      "rtsptunnel":<String_value>,      "reqtimeout":<Double_value>,      "adpttimeout":<String_value>,      "reqtimeoutaction":<String_value>,      "dropextradata":<String_value>,      "weblog":<String_value>,      "clientiphdrexpr":<String_value>,      "maxreq":<Double_value>,      "persistentetag":<String_value>,      "spdy":<String_value>,      "reusepooltimeout":<Double_value>,      "maxheaderlen":<Double_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","nshttpprofile":{      "name":<String_value>,      "dropinvalreqs":true,      "markhttp09inval":true,      "markconnreqinval":true,      "cmponpush":true,      "conmultiplex":true,      "maxreusepool":true,      "dropextracrlf":true,      "incomphdrdelay":true,      "websocket":true,      "dropextradata":true,      "clientiphdrexpr":true,      "reqtimeout":true,      "adpttimeout":true,      "reqtimeoutaction":true,      "weblog":true,      "maxreq":true,      "persistentetag":true,      "spdy":true,      "reusepooltimeout":true,      "maxheaderlen":true,      "rtsptunnel":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/nshttpprofile
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/nshttpprofile?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of nshttpprofile resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/nshttpprofile?view=summary
Use this query-parameter to get the summary output of nshttpprofile resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/nshttpprofile?pagesize=#no;pageno=#no
Use this query-parameter to get the nshttpprofile resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/nshttpprofile?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "nshttpprofile": [ {      "name":<String_value>,      "dropinvalreqs":<String_value>,      "markhttp09inval":<String_value>,      "markconnreqinval":<String_value>,      "cmponpush":<String_value>,      "conmultiplex":<String_value>,      "maxreusepool":<Double_value>,      "websocket":<String_value>,      "refcnt":<Double_value>,      "dropextracrlf":<String_value>,      "incomphdrdelay":<Double_value>,      "reqtimeout":<Double_value>,      "adpttimeout":<String_value>,      "reqtimeoutaction":<String_value>,      "dropextradata":<String_value>,      "weblog":<String_value>,      "clientiphdrexpr":<String_value>,      "maxreq":<Double_value>,      "persistentetag":<String_value>,      "spdy":<String_value>,      "reusepooltimeout":<Double_value>,      "maxheaderlen":<Double_value>,      "rtsptunnel":<String_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/nshttpprofile/name_value&lt;String&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "nshttpprofile": [ {      "name":<String_value>,      "dropinvalreqs":<String_value>,      "markhttp09inval":<String_value>,      "markconnreqinval":<String_value>,      "cmponpush":<String_value>,      "conmultiplex":<String_value>,      "maxreusepool":<Double_value>,      "websocket":<String_value>,      "refcnt":<Double_value>,      "dropextracrlf":<String_value>,      "incomphdrdelay":<Double_value>,      "reqtimeout":<Double_value>,      "adpttimeout":<String_value>,      "reqtimeoutaction":<String_value>,      "dropextradata":<String_value>,      "weblog":<String_value>,      "clientiphdrexpr":<String_value>,      "maxreq":<Double_value>,      "persistentetag":<String_value>,      "spdy":<String_value>,      "reusepooltimeout":<Double_value>,      "maxheaderlen":<Double_value>,      "rtsptunnel":<String_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/nshttpprofile?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",nshttpprofile: [ { "__count": "#no"} ] }


