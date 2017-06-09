#systemfile

Configuration for file resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>filename</td><td>&lt;String></td><td>Read-write</td><td>Name of the file. It should not include filepath.&lt;br>Maximum length = 63</td><tr><tr><td>filecontent</td><td>&lt;String></td><td>Read-write</td><td>file content in Base64 format.</td><tr><tr><td>filelocation</td><td>&lt;String></td><td>Read-write</td><td>location of the file on NetScaler.&lt;br>Maximum length = 127</td><tr><tr><td>fileencoding</td><td>&lt;String></td><td>Read-write</td><td>encoding type of the file content.&lt;br>Default value: "BASE64"</td><tr><tr><td>fileaccesstime</td><td>&lt;String></td><td>Read-only</td><td>Last access time of the file.</td><tr><tr><td>filemodifiedtime</td><td>&lt;String></td><td>Read-only</td><td>last modified time of the file.</td><tr><tr><td>filemode</td><td>&lt;String[]></td><td>Read-only</td><td>file mode.&lt;br>Possible values = DIRECTORY</td><tr><tr><td>filesize</td><td>&lt;Double></td><td>Read-only</td><td>Size of the file in BYTES.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [DELETE](#delete) | [GET (ALL)](#get-(all)) | [GET](#get)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/systemfile
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"systemfile":{      "filename":<String_value>,      "filecontent":<String_value>,      "filelocation":<String_value>,      "fileencoding":<String_value>}}```
Response:
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/systemfile/filename_value&lt;String&gt;
HTTP Method: DELETE
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/systemfile
Query-parameters:
args
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/systemfile?args=filename:&lt;String_value&gt;,filelocation:&lt;String_value&gt;
Use this query-parameter to get systemfile resources based on additional properties.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "systemfile": [ {filename:<String_value>,filelocation:<String_value>      "filecontent":<String_value>,      "fileencoding":<String_value>,      "fileaccesstime":<String_value>,      "filemodifiedtime":<String_value>,      "filemode":<String[]_value>,      "filesize":<Double_value>}]}```



###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/systemfile/filename_value&lt;String&gt;
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "systemfile": [ {filename:<String_value>,filelocation:<String_value>      "filecontent":<String_value>,      "fileencoding":<String_value>,      "fileaccesstime":<String_value>,      "filemodifiedtime":<String_value>,      "filemode":<String[]_value>,      "filesize":<Double_value>}]}```



