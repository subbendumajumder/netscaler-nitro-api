#filteraction

Configuration for filter action resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the filtering action. Must begin with a letter, number, or the underscore character (_). Other characters allowed, after the first character, are the hyphen (-), period (.) hash (#), space ( ), at sign (@), equals (=), and colon (:) characters. Choose a name that helps identify the type of action. The name of a filter action cannot be changed after it is created. CLI Users: If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my action" or my action).&lt;br>Minimum length = 1</td><tr><tr><td>qual</td><td>&lt;String></td><td>Read-write</td><td>Qualifier, which is the action to be performed. The qualifier cannot be changed after it is set. The available options function as follows: ADD - Adds the specified HTTP header. RESET - Terminates the connection, sending the appropriate termination notice to the users browser. FORWARD - Redirects the request to the designated service. You must specify either a service name or a page, but not both. DROP - Silently deletes the request, without sending a response to the users browser. CORRUPT - Modifies the designated HTTP header to prevent it from performing the function it was intended to perform, then sends the request/response to the server/browser. ERRORCODE. Returns the designated HTTP error code to the users browser (for example, 404, the standard HTTP code for a non-existent Web page).&lt;br>Possible values = reset, add, corrupt, forward, errorcode, drop</td><tr><tr><td>servicename</td><td>&lt;String></td><td>Read-write</td><td>Service to which to forward HTTP requests. Required if the qualifier is FORWARD.&lt;br>Minimum length = 1</td><tr><tr><td>value</td><td>&lt;String></td><td>Read-write</td><td>String containing the header_name and header_value. If the qualifier is ADD, specify ;lt;header_name;gt;:;lt;header_value;gt;. If the qualifier is CORRUPT, specify only the header_name.&lt;br>Minimum length = 1</td><tr><tr><td>respcode</td><td>&lt;Double></td><td>Read-write</td><td>Response code to be returned for HTTP requests (for use with the ERRORCODE qualifier).&lt;br>Minimum value = 1</td><tr><tr><td>page</td><td>&lt;String></td><td>Read-write</td><td>HTML page to return for HTTP requests (For use with the ERRORCODE qualifier).&lt;br>Minimum length = 1</td><tr><tr><td>isdefault</td><td>&lt;Boolean></td><td>Read-only</td><td>A value of true is returned if it is a default filteraction.</td><tr><tr><td>builtin</td><td>&lt;String[]></td><td>Read-only</td><td>.&lt;br>Possible values = MODIFIABLE, DELETABLE, IMMUTABLE, PARTITION_ALL</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
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
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>},"sessionid":"##sessionid","filteraction":{      "name":<String_value>,      "qual":<String_value>,      "servicename":<String_value>,      "value":<String_value>,      "respcode":<Double_value>,      "page":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/filteraction/name_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/filteraction/name_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","filteraction":{      "name":<String_value>,      "servicename":<String_value>,      "value":<String_value>,      "respcode":<Double_value>,      "page":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","filteraction":{      "name":<String_value>,      "page":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/filteraction
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/filteraction?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of filteraction resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/filteraction?view=summary
Use this query-parameter to get the summary output of filteraction resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/filteraction?pagesize=#no;pageno=#no
Use this query-parameter to get the filteraction resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/filteraction?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "filteraction": [ {      "name":<String_value>,      "qual":<String_value>,      "servicename":<String_value>,      "value":<String_value>,      "respcode":<Double_value>,      "page":<String_value>,      "isdefault":<Boolean_value>,      "builtin":<String[]_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/filteraction/name_value&lt;String&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "filteraction": [ {      "name":<String_value>,      "qual":<String_value>,      "servicename":<String_value>,      "value":<String_value>,      "respcode":<Double_value>,      "page":<String_value>,      "isdefault":<Boolean_value>,      "builtin":<String[]_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/filteraction?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",filteraction: [ { "__count": "#no"} ] }


