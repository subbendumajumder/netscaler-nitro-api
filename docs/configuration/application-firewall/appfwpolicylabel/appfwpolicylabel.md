#appfwpolicylabel

Configuration for application firewall policy label resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>labelname</td><td>&lt;String></td><td>Read-write</td><td>Name for the policy label. Must begin with a letter, number, or the underscore character (_), and must contain only letters, numbers, and the hyphen (-), period (.) pound (#), space ( ), at (@), equals (=), colon (:), and underscore characters. Can be changed after the policy label is created. The following requirement applies only to the NetScaler CLI: If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my policy label" or my policy label).</td><tr><tr><td>policylabeltype</td><td>&lt;String></td><td>Read-write</td><td>Type of transformations allowed by the policies bound to the label. Always http_req for application firewall policy labels.&lt;br>Possible values = http_req</td><tr><tr><td>newname</td><td>&lt;String></td><td>Read-write</td><td>The new name of the application firewall policylabel.&lt;br>Minimum length = 1</td><tr><tr><td>numpol</td><td>&lt;Double></td><td>Read-only</td><td>Number of polices bound to label.</td><tr><tr><td>hits</td><td>&lt;Double></td><td>Read-only</td><td>Number of times policy label was invoked.</td><tr><tr><td>priority</td><td>&lt;Double></td><td>Read-only</td><td>Positive integer specifying the priority of the policy. A lower number specifies a higher priority. Must be unique within a group of policies that are bound to the same bind point or label. Policies are evaluated in the order of their priority numbers.</td><tr><tr><td>gotopriorityexpression</td><td>&lt;String></td><td>Read-only</td><td>Expression specifying the priority of the next policy which will get evaluated if the current policy rule evaluates to TRUE.</td><tr><tr><td>labeltype</td><td>&lt;String></td><td>Read-only</td><td>Type of policy label to invoke if the current policy evaluates to TRUE and the invoke parameter is set. Available settings function as follows: * reqvserver. Invoke the unnamed policy label associated with the specified request virtual server. * policylabel. Invoke the specified user-defined policy label.&lt;br>Possible values = reqvserver, policylabel</td><tr><tr><td>invoke_labelname</td><td>&lt;String></td><td>Read-only</td><td>Name of the policy label to invoke if the current policy evaluates to TRUE, the invoke parameter is set, and Label Type is set to Policy Label.</td><tr><tr><td>description</td><td>&lt;String></td><td>Read-only</td><td>Description of the policylabel.</td><tr><tr><td>policytype</td><td>&lt;String></td><td>Read-only</td><td>.&lt;br>Possible values = Classic Policy, Advanced Policy</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
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
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>},"sessionid":"##sessionid","appfwpolicylabel":{      "labelname":<String_value>,      "policylabeltype":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/appfwpolicylabel/labelname_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/appfwpolicylabel/labelname_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###rename



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"rename"},"sessionid":"##sessionid","appfwpolicylabel":{      "labelname":<String_value>,      "newname":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/appfwpolicylabel
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/appfwpolicylabel?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of appfwpolicylabel resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/appfwpolicylabel?view=summary
Use this query-parameter to get the summary output of appfwpolicylabel resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/appfwpolicylabel?pagesize=#no;pageno=#no
Use this query-parameter to get the appfwpolicylabel resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/appfwpolicylabel?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "appfwpolicylabel": [ {      "labelname":<String_value>,      "policylabeltype":<String_value>,      "numpol":<Double_value>,      "hits":<Double_value>,      "priority":<Double_value>,      "gotopriorityexpression":<String_value>,      "labeltype":<String_value>,      "invoke_labelname":<String_value>,      "description":<String_value>,      "policytype":<String_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/appfwpolicylabel/labelname_value&lt;String&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "appfwpolicylabel": [ {      "labelname":<String_value>,      "policylabeltype":<String_value>,      "numpol":<Double_value>,      "hits":<Double_value>,      "priority":<Double_value>,      "gotopriorityexpression":<String_value>,      "labeltype":<String_value>,      "invoke_labelname":<String_value>,      "description":<String_value>,      "policytype":<String_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/appfwpolicylabel?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",appfwpolicylabel: [ { "__count": "#no"} ] }


