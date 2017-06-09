#nsassignment

Configuration for assignment resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the assignment. Must begin with a letter, number, or the underscore character (_), and must contain only letters, numbers, and the hyphen (-), period (.) hash (#), space ( ), at (@), equals (=), colon (:), and underscore characters. Can be changed after the assignment is added. The following requirement applies only to the NetScaler CLI: If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my assignment" or ?my assignment?).</td><tr><tr><td>variable</td><td>&lt;String></td><td>Read-write</td><td>Left hand side of the assigment, of the form $variable-name (for a singleton variabled) or $variable-name[key-expression], where key-expression is a default syntax expression that evaluates to a text string and provides the key to select a map entry.</td><tr><tr><td>set</td><td>&lt;String></td><td>Read-write</td><td>Right hand side of the assignment. The default syntax expression is evaluated and assigned to theleft hand variable.</td><tr><tr><td>Add</td><td>&lt;String></td><td>Read-write</td><td>Right hand side of the assignment. The default syntax expression is evaluated and added to the left hand variable.</td><tr><tr><td>sub</td><td>&lt;String></td><td>Read-write</td><td>Right hand side of the assignment. The default syntax expression is evaluated and subtracted from the left hand variable.</td><tr><tr><td>append</td><td>&lt;String></td><td>Read-write</td><td>Right hand side of the assignment. The default syntax expression is evaluated and appended to the left hand variable.</td><tr><tr><td>clear</td><td>&lt;Boolean></td><td>Read-write</td><td>Clear the variable value. Deallocates a text value, and for a map, the text key.</td><tr><tr><td>comment</td><td>&lt;String></td><td>Read-write</td><td>Comment. Can be used to preserve information about this rewrite action.</td><tr><tr><td>newname</td><td>&lt;String></td><td>Read-write</td><td>New name for the assignment. Must begin with a letter, number, or the underscore character (_), and must contain only letters, numbers, and the hyphen (-), period (.) hash (#), space ( ), at (@), equals (=), colon (:), and underscore characters. Can be changed after the rewrite policy is added. The following requirement applies only to the NetScaler CLI: If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my assignment" or ?my assignment?).&lt;br>Minimum length = 1</td><tr><tr><td>hits</td><td>&lt;Double></td><td>Read-only</td><td>The number of times the action has been taken.</td><tr><tr><td>undefhits</td><td>&lt;Double></td><td>Read-only</td><td>The number of times the action resulted in UNDEF.</td><tr><tr><td>referencecount</td><td>&lt;Double></td><td>Read-only</td><td>The number of references to the action.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [UPDATE](#update) | [UNSET](#unset) | [DELETE](#delete) | [RENAME](#rename) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>},"sessionid":"##sessionid","nsassignment":{      "name":<String_value>,      "variable":<String_value>,      "set":<String_value>,      "Add":<String_value>,      "sub":<String_value>,      "append":<String_value>,      "clear":<Boolean_value>,      "comment":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","nsassignment":{      "name":<String_value>,      "variable":<String_value>,      "set":<String_value>,      "Add":<String_value>,      "sub":<String_value>,      "append":<String_value>,      "clear":<Boolean_value>,      "comment":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","nsassignment":{      "name":<String_value>,      "comment":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/nsassignment/name_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/nsassignment/name_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###rename



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"rename"},"sessionid":"##sessionid","nsassignment":{      "name":<String_value>,      "newname":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/nsassignment
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/nsassignment?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of nsassignment resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/nsassignment?view=summary
Use this query-parameter to get the summary output of nsassignment resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/nsassignment?pagesize=#no;pageno=#no
Use this query-parameter to get the nsassignment resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/nsassignment?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "nsassignment": [ {      "name":<String_value>,      "variable":<String_value>,      "set":<String_value>,      "Add":<String_value>,      "sub":<String_value>,      "append":<String_value>,      "clear":<Boolean_value>,      "hits":<Double_value>,      "undefhits":<Double_value>,      "referencecount":<Double_value>,      "comment":<String_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/nsassignment/name_value&lt;String&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "nsassignment": [ {      "name":<String_value>,      "variable":<String_value>,      "set":<String_value>,      "Add":<String_value>,      "sub":<String_value>,      "append":<String_value>,      "clear":<Boolean_value>,      "hits":<Double_value>,      "undefhits":<Double_value>,      "referencecount":<Double_value>,      "comment":<String_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/nsassignment?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",nsassignment: [ { "__count": "#no"} ] }


