#cmppolicylabel

Configuration for compression policy label resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>labelname</td><td>&lt;String></td><td>Read-write</td><td>Name of the HTTP compression policy label. Must begin with a letter, number, or the underscore character (_). Additional characters allowed, after the first character, are the hyphen (-), period (.) pound sign (#), space ( ), at sign (@), equals (=), and colon (:). The name must be unique within the list of policy labels for compression policies. Can be renamed after the policy label is created. The following requirement applies only to the NetScaler CLI: If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my cmp policylabel" or my cmp policylabel).&lt;br>Minimum length = 1</td><tr><tr><td>type</td><td>&lt;String></td><td>Read-write</td><td>Type of packets (request packets or response) against which to match the policies bound to this policy label.&lt;br>Possible values = REQ, RES</td><tr><tr><td>newname</td><td>&lt;String></td><td>Read-write</td><td>New name for the compression policy label. Must begin with an ASCII alphabetic or underscore (_) character, and must contain only ASCII alphanumeric, underscore, hash (#), period (.), space, colon (:), at (@), equals (=), and hyphen (-) characters. The following requirement applies only to the NetScaler CLI: If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my cmp policylabel" or my cmp policylabel).&lt;br>Minimum length = 1</td><tr><tr><td>numpol</td><td>&lt;Double></td><td>Read-only</td><td>Number of polices bound to label.</td><tr><tr><td>hits</td><td>&lt;Double></td><td>Read-only</td><td>Number of times policy label was invoked.</td><tr><tr><td>priority</td><td>&lt;Double></td><td>Read-only</td><td>Specifies the priority of the policy.</td><tr><tr><td>gotopriorityexpression</td><td>&lt;String></td><td>Read-only</td><td>Expression specifying the priority of the next policy which will get evaluated if the current policy rule evaluates to TRUE.</td><tr><tr><td>labeltype</td><td>&lt;String></td><td>Read-only</td><td>Type of policy label invocation.&lt;br>Possible values = reqvserver, resvserver, policylabel</td><tr><tr><td>invoke_labelname</td><td>&lt;String></td><td>Read-only</td><td>Name of the label to invoke if the current policy evaluates to TRUE.</td><tr><tr><td>flowtype</td><td>&lt;Double></td><td>Read-only</td><td>Flowtype of the bound compression policy.</td><tr><tr><td>description</td><td>&lt;String></td><td>Read-only</td><td>Description of the policylabel.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [DELETE](#delete) | [RENAME](#rename) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>},"sessionid":"##sessionid","cmppolicylabel":{      "labelname":<String_value>,      "type":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/cmppolicylabel/labelname_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/cmppolicylabel/labelname_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###rename



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"rename"},"sessionid":"##sessionid","cmppolicylabel":{      "labelname":<String_value>,      "newname":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/cmppolicylabel
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/cmppolicylabel?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of cmppolicylabel resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/cmppolicylabel?view=summary
Use this query-parameter to get the summary output of cmppolicylabel resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/cmppolicylabel?pagesize=#no;pageno=#no
Use this query-parameter to get the cmppolicylabel resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/cmppolicylabel?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "cmppolicylabel": [ {      "labelname":<String_value>,      "type":<String_value>,      "numpol":<Double_value>,      "hits":<Double_value>,      "priority":<Double_value>,      "gotopriorityexpression":<String_value>,      "labeltype":<String_value>,      "invoke_labelname":<String_value>,      "flowtype":<Double_value>,      "description":<String_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/cmppolicylabel/labelname_value&lt;String&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "cmppolicylabel": [ {      "labelname":<String_value>,      "type":<String_value>,      "numpol":<Double_value>,      "hits":<Double_value>,      "priority":<Double_value>,      "gotopriorityexpression":<String_value>,      "labeltype":<String_value>,      "invoke_labelname":<String_value>,      "flowtype":<Double_value>,      "description":<String_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/cmppolicylabel?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",cmppolicylabel: [ { "__count": "#no"} ] }


