#autoscalepolicy

Configuration for Autoscale policy resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>The name of the autoscale policy.&lt;br>Minimum length = 1</td><tr><tr><td>rule</td><td>&lt;String></td><td>Read-write</td><td>The rule associated with the policy.</td><tr><tr><td>action</td><td>&lt;String></td><td>Read-write</td><td>The autoscale profile associated with the policy.&lt;br>Minimum length = 1</td><tr><tr><td>comment</td><td>&lt;String></td><td>Read-write</td><td>Comments associated with this autoscale policy.</td><tr><tr><td>logaction</td><td>&lt;String></td><td>Read-write</td><td>The log action associated with the autoscale policy.</td><tr><tr><td>newname</td><td>&lt;String></td><td>Read-write</td><td>The new name of the autoscale policy.&lt;br>Minimum length = 1</td><tr><tr><td>hits</td><td>&lt;Double></td><td>Read-only</td><td>Number of hits.</td><tr><tr><td>undefhits</td><td>&lt;Double></td><td>Read-only</td><td>Number of Undef hits.</td><tr><tr><td>priority</td><td>&lt;Double></td><td>Read-only</td><td>Specifies the priority of the policy.</td><tr><tr><td>activepolicy</td><td>&lt;Integer></td><td>Read-only</td><td>Indicates whether policy is bound or not.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [DELETE](#delete) | [UPDATE](#update) | [UNSET](#unset) | [RENAME](#rename) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>},"sessionid":"##sessionid","autoscalepolicy":{      "name":<String_value>,      "rule":<String_value>,      "action":<String_value>,      "comment":<String_value>,      "logaction":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/autoscalepolicy/name_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/autoscalepolicy/name_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","autoscalepolicy":{      "name":<String_value>,      "rule":<String_value>,      "action":<String_value>,      "comment":<String_value>,      "logaction":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","autoscalepolicy":{      "name":<String_value>,      "rule":true,      "action":true,      "comment":true,      "logaction":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###rename



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"rename"},"sessionid":"##sessionid","autoscalepolicy":{      "name":<String_value>,      "newname":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/autoscalepolicy
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/autoscalepolicy?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of autoscalepolicy resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/autoscalepolicy?view=summary
Use this query-parameter to get the summary output of autoscalepolicy resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/autoscalepolicy?pagesize=#no;pageno=#no
Use this query-parameter to get the autoscalepolicy resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/autoscalepolicy?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "autoscalepolicy": [ {      "name":<String_value>,      "rule":<String_value>,      "action":<String_value>,      "comment":<String_value>,      "logaction":<String_value>,      "hits":<Double_value>,      "undefhits":<Double_value>,      "priority":<Double_value>,      "activepolicy":<Integer_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/autoscalepolicy/name_value&lt;String&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "autoscalepolicy": [ {      "name":<String_value>,      "rule":<String_value>,      "action":<String_value>,      "comment":<String_value>,      "logaction":<String_value>,      "hits":<Double_value>,      "undefhits":<Double_value>,      "priority":<Double_value>,      "activepolicy":<Integer_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/autoscalepolicy?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",autoscalepolicy: [ { "__count": "#no"} ] }


