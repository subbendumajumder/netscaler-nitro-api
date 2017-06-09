#responderaction

Configuration for responder action resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the responder action. Must begin with a letter, number, or the underscore character (_), and must contain only letters, numbers, and the hyphen (-), period (.) hash (#), space ( ), at (@), equals (=), colon (:), and underscore characters. Can be changed after the responder policy is added.&lt;br>&lt;br>The following requirement applies only to the NetScaler CLI:&lt;br>If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my responder action" or my responder action).</td><tr><tr><td>type</td><td>&lt;String></td><td>Read-write</td><td>Type of responder action. Available settings function as follows:&lt;br>* respondwith ;lt;target;gt; - Respond to the request with the expression specified as the target.&lt;br>* respondwithhtmlpage - Respond to the request with the uploaded HTML page object specified as the target.&lt;br>* redirect - Redirect the request to the URL specified as the target.&lt;br>* sqlresponse_ok - Send an SQL OK response.&lt;br>* sqlresponse_error - Send an SQL ERROR response.&lt;br>Possible values = noop, respondwith, redirect, respondwithhtmlpage, sqlresponse_ok, sqlresponse_error</td><tr><tr><td>target</td><td>&lt;String></td><td>Read-write</td><td>Expression specifying what to respond with. Typically a URL for redirect policies or a default-syntax expression. In addition to NetScaler default-syntax expressions that refer to information in the request, a stringbuilder expression can contain text and HTML, and simple escape codes that define new lines and paragraphs. Enclose each stringbuilder expression element (either a NetScaler default-syntax expression or a string) in double quotation marks. Use the plus (+) character to join the elements. &lt;br>&lt;br>Examples:&lt;br>1) Respondwith expression that sends an HTTP 1.1 200 OK response:&lt;br>"HTTP/1.1 200 OK\\r\\n\\r\\n"&lt;br>&lt;br>2) Redirect expression that redirects user to the specified web host and appends the request URL to the redirect.&lt;br>"http://backupsite2.com" + HTTP.REQ.URL&lt;br>&lt;br>3) Respondwith expression that sends an HTTP 1.1 404 Not Found response with the request URL included in the response:&lt;br>"HTTP/1.1 404 Not Found\\r\\n\\r\\n"+ "HTTP.REQ.URL.HTTP_URL_SAFE" + "does not exist on the web server."&lt;br>&lt;br>The following requirement applies only to the NetScaler CLI:&lt;br>Enclose the entire expression in single quotation marks. (NetScaler default expression elements should be included inside the single quotation marks for the entire expression, but do not need to be enclosed in double quotation marks.).</td><tr><tr><td>htmlpage</td><td>&lt;String></td><td>Read-write</td><td>For respondwithhtmlpage policies, name of the HTML page object to use as the response. You must first import the page object.&lt;br>Minimum length = 1</td><tr><tr><td>bypasssafetycheck</td><td>&lt;String></td><td>Read-write</td><td>Bypass the safety check, allowing potentially unsafe expressions. An unsafe expression in a response is one that contains references to request elements that might not be present in all requests. If a response refers to a missing request element, an empty string is used instead.&lt;br>Default value: NO&lt;br>Possible values = YES, NO</td><tr><tr><td>comment</td><td>&lt;String></td><td>Read-write</td><td>Comment. Any type of information about this responder action.</td><tr><tr><td>responsestatuscode</td><td>&lt;Double></td><td>Read-write</td><td>HTTP response status code, for example 200, 302, 404, etc. The default value for the redirect action type is 302 and for respondwithhtmlpage is 200.&lt;br>Minimum value = 100&lt;br>Maximum value = 599</td><tr><tr><td>reasonphrase</td><td>&lt;String></td><td>Read-write</td><td>Expression specifying the reason phrase of the HTTP response. The reason phrase may be a string literal with quotes or a PI expression. For example: "Invalid URL: " + HTTP.REQ.URL.&lt;br>Minimum length = 1</td><tr><tr><td>newname</td><td>&lt;String></td><td>Read-write</td><td>New name for the responder action.&lt;br>Must begin with a letter, number, or the underscore character (_), and must contain only letters, numbers, and the hyphen (-), period (.) hash (#), space ( ), at (@), equals (=), colon (:), and underscore characters.&lt;br>&lt;br>The following requirement applies only to the NetScaler CLI:&lt;br>If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my responder action" or my responder action).&lt;br>Minimum length = 1</td><tr><tr><td>hits</td><td>&lt;Double></td><td>Read-only</td><td>The number of times the action has been taken.</td><tr><tr><td>referencecount</td><td>&lt;Double></td><td>Read-only</td><td>The number of references to the action.</td><tr><tr><td>undefhits</td><td>&lt;Double></td><td>Read-only</td><td>The number of times the action resulted in UNDEF.</td><tr><tr><td>builtin</td><td>&lt;String[]></td><td>Read-only</td><td>Flag to determine whether responder action is built-in or not.&lt;br>Possible values = MODIFIABLE, DELETABLE, IMMUTABLE, PARTITION_ALL</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [DELETE](#delete) | [UPDATE](#update) | [UNSET](#unset) | [RENAME](#rename) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/responderaction
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"responderaction":{      "name":<String_value>,      "type":<String_value>,      "target":<String_value>,      "htmlpage":<String_value>,      "bypasssafetycheck":<String_value>,      "comment":<String_value>,      "responsestatuscode":<Double_value>,      "reasonphrase":<String_value>}}```
Response:
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/responderaction/name_value&lt;String&gt;
HTTP Method: DELETE
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/responderaction
HTTP Method: PUT
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"responderaction":{      "name":<String_value>,      "target":<String_value>,      "bypasssafetycheck":<String_value>,      "htmlpage":<String_value>,      "responsestatuscode":<Double_value>,      "reasonphrase":<String_value>,      "comment":<String_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/responderaction?action=unset
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"responderaction":{      "name":<String_value>,      "responsestatuscode":true,      "reasonphrase":true,      "comment":true}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###rename



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/responderaction?action=rename
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"responderaction":{      "name":<String_value>,      "newname":<String_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/responderaction
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/responderaction?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


filter
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/responderaction?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of responderaction resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/responderaction?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).


pagination
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/responderaction?pagesize=#no;pageno=#no
Use this query-parameter to get the responderaction resources in chunks.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "responderaction": [ {      "name":<String_value>,      "type":<String_value>,      "target":<String_value>,      "htmlpage":<String_value>,      "bypasssafetycheck":<String_value>,      "hits":<Double_value>,      "referencecount":<Double_value>,      "undefhits":<Double_value>,      "comment":<String_value>,      "builtin":<String[]_value>,      "responsestatuscode":<Double_value>,      "reasonphrase":<String_value>}]}```



###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/responderaction/name_value&lt;String&gt;
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/responderaction/name_value&lt;String&gt;?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/responderaction/name_value&lt;String&gt;?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "responderaction": [ {      "name":<String_value>,      "type":<String_value>,      "target":<String_value>,      "htmlpage":<String_value>,      "bypasssafetycheck":<String_value>,      "hits":<Double_value>,      "referencecount":<Double_value>,      "undefhits":<Double_value>,      "comment":<String_value>,      "builtin":<String[]_value>,      "responsestatuscode":<Double_value>,      "reasonphrase":<String_value>}]}```



###count



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/responderaction?count=yes
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: 
{ "responderaction": [ { "__count": "#no"} ] }


