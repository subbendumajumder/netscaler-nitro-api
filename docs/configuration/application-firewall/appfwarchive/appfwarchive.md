#appfwarchive

Configuration for archive resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name of tar archive.&lt;br>Minimum length = 1&lt;br>Maximum length = 31</td><tr><tr><td>target</td><td>&lt;String></td><td>Read-write</td><td>Path to the file to be exported.&lt;br>Minimum length = 1&lt;br>Maximum length = 2047</td><tr><tr><td>src</td><td>&lt;String></td><td>Read-write</td><td>Indicates the source of the tar archive file as a URL of the form ;lt;protocol;gt;://;lt;host;gt;[:;lt;port;gt;][/;lt;path;gt;] ;lt;protocol;gt; is http or https. ;lt;host;gt; is the DNS name or IP address of the http or https server. ;lt;port;gt; is the port number of the server. If omitted, the default port for http or https will be used. ;lt;path;gt; is the path of the file on the server. Import will fail if an https server requires client certificate authentication. .&lt;br>Minimum length = 1&lt;br>Maximum length = 2047</td><tr><tr><td>comment</td><td>&lt;String></td><td>Read-write</td><td>Comments associated with this archive.&lt;br>Maximum length = 128</td><tr><tr><td>response</td><td>&lt;String></td><td>Read-only</td><td>.</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[EXPORT](#export) | [IMPORT](#import) | [DELETE](#delete) | [GET (ALL)](#get-(all))


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###export



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"export"},"sessionid":"##sessionid","appfwarchive":{      "name":<String_value>,      "target":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###Import



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"Import"},"sessionid":"##sessionid","appfwarchive":{      "src":<String_value>,      "name":<String_value>,      "comment":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/appfwarchive/name_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/appfwarchive/name_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/appfwarchive
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "appfwarchive": [ {      "response":<String_value>}]}```



