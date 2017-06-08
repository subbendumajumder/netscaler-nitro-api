#responderpolicylabel

Configuration for responder policy label resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>labelname</td><td>&lt;String></td><td>Read-write</td><td>Name for the responder policy label. Must begin with a letter, number, or the underscore character (_), and must contain only letters, numbers, and the hyphen (-), period (.) hash (#), space ( ), at (@), equals (=), colon (:), and underscore characters. Cannot be changed after the responder policy label is added. The following requirement applies only to the NetScaler CLI: If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my responder policy label" or my responder policy label).</td><tr><tr><td>policylabeltype</td><td>&lt;String></td><td>Read-write</td><td>Type of responses sent by the policies bound to this policy label. Types are: * HTTP - HTTP responses. * OTHERTCP - NON-HTTP TCP responses. * SIP_UDP - SIP responses. * MYSQL - SQL responses in MySQL format. * MSSQL - SQL responses in Microsoft SQL format. * NAT - NAT response.&lt;br>Default value: HTTP&lt;br>Possible values = HTTP, OTHERTCP, SIP_UDP, MYSQL, MSSQL, NAT, DIAMETER</td><tr><tr><td>comment</td><td>&lt;String></td><td>Read-write</td><td>Any comments to preserve information about this responder policy label.</td><tr><tr><td>newname</td><td>&lt;String></td><td>Read-write</td><td>New name for the responder policy label. Must begin with a letter, number, or the underscore character (_), and must contain only letters, numbers, and the hyphen (-), period (.) hash (#), space ( ), at (@), equals (=), colon (:), and underscore characters.&lt;br>Minimum length = 1</td><tr><tr><td>numpol</td><td>&lt;Double></td><td>Read-only</td><td>number of polices bound to label.</td><tr><tr><td>hits</td><td>&lt;Double></td><td>Read-only</td><td>Number of times policy label was invoked.</td><tr><tr><td>priority</td><td>&lt;Double></td><td>Read-only</td><td>Specifies the priority of the policy.</td><tr><tr><td>gotopriorityexpression</td><td>&lt;String></td><td>Read-only</td><td>Expression specifying the priority of the next policy which will get evaluated if the current policy rule evaluates to TRUE.</td><tr><tr><td>labeltype</td><td>&lt;String></td><td>Read-only</td><td>Type of policy label to invoke. Available settings function as follows: * vserver - Invoke an unnamed policy label associated with a virtual server. * policylabel - Invoke a user-defined policy label.&lt;br>Possible values = vserver, policylabel</td><tr><tr><td>invoke_labelname</td><td>&lt;String></td><td>Read-only</td><td>* If labelType is policylabel, name of the policy label to invoke. * If labelType is reqvserver or resvserver, name of the virtual server.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
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
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>},"sessionid":"##sessionid","responderpolicylabel":{      "labelname":<String_value>,      "policylabeltype":<String_value>,      "comment":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/responderpolicylabel/labelname_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/responderpolicylabel/labelname_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###rename



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"rename"},"sessionid":"##sessionid","responderpolicylabel":{      "labelname":<String_value>,      "newname":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/responderpolicylabel
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/responderpolicylabel?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of responderpolicylabel resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/responderpolicylabel?view=summary
Use this query-parameter to get the summary output of responderpolicylabel resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/responderpolicylabel?pagesize=#no;pageno=#no
Use this query-parameter to get the responderpolicylabel resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/responderpolicylabel?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "responderpolicylabel": [ {      "labelname":<String_value>,      "policylabeltype":<String_value>,      "numpol":<Double_value>,      "hits":<Double_value>,      "priority":<Double_value>,      "gotopriorityexpression":<String_value>,      "labeltype":<String_value>,      "invoke_labelname":<String_value>,      "comment":<String_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/responderpolicylabel/labelname_value&lt;String&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "responderpolicylabel": [ {      "labelname":<String_value>,      "policylabeltype":<String_value>,      "numpol":<Double_value>,      "hits":<Double_value>,      "priority":<Double_value>,      "gotopriorityexpression":<String_value>,      "labeltype":<String_value>,      "invoke_labelname":<String_value>,      "comment":<String_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/responderpolicylabel?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",responderpolicylabel: [ { "__count": "#no"} ] }


