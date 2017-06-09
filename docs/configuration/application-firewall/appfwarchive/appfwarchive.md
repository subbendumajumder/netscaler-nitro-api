#appfwarchive

Configuration for archive resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name of tar archive.&lt;br>Minimum length = 1&lt;br>Maximum length = 31</td><tr><tr><td>target</td><td>&lt;String></td><td>Read-write</td><td>Path to the file to be exported.&lt;br>Minimum length = 1&lt;br>Maximum length = 2047</td><tr><tr><td>src</td><td>&lt;String></td><td>Read-write</td><td>Indicates the source of the tar archive file as a URL&lt;br>of the form&lt;br>&lt;br> ;lt;protocol;gt;://;lt;host;gt;[:;lt;port;gt;][/;lt;path;gt;]&lt;br>&lt;br>;lt;protocol;gt; is http or https.&lt;br>;lt;host;gt; is the DNS name or IP address of the http or https server.&lt;br>;lt;port;gt; is the port number of the server. If omitted, the&lt;br>default port for http or https will be used.&lt;br>;lt;path;gt; is the path of the file on the server.&lt;br>&lt;br>Import will fail if an https server requires client&lt;br>certificate authentication.&lt;br>&lt;br>&lt;br>.&lt;br>Minimum length = 1&lt;br>Maximum length = 2047</td><tr><tr><td>comment</td><td>&lt;String></td><td>Read-write</td><td>Comments associated with this archive.&lt;br>Maximum length = 128</td><tr><tr><td>response</td><td>&lt;String></td><td>Read-only</td><td>.</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[EXPORT](#export) | [IMPORT](#import) | [DELETE](#delete) | [GET (ALL)](#get-(all))


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###export



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appfwarchive?action=export
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"appfwarchive":{      "name":<String_value>,      "target":<String_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###Import



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appfwarchive?action=Import
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"appfwarchive":{      "src":<String_value>,      "name":<String_value>,      "comment":<String_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appfwarchive/name_value&lt;String&gt;
HTTP Method: DELETE
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appfwarchive
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "appfwarchive": [ {      "response":<String_value>}]}```



