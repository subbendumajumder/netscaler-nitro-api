#autoscaleaction

Configuration for autoscale action resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>ActionScale action name.&lt;br>Minimum length = 1</td><tr><tr><td>type</td><td>&lt;String></td><td>Read-write</td><td>The type of action.&lt;br>Possible values = SCALE_UP, SCALE_DOWN</td><tr><tr><td>profilename</td><td>&lt;String></td><td>Read-write</td><td>AutoScale profile name.&lt;br>Minimum length = 1</td><tr><tr><td>parameters</td><td>&lt;String></td><td>Read-write</td><td>Parameters to use in the action.&lt;br>Minimum length = 1</td><tr><tr><td>vmdestroygraceperiod</td><td>&lt;Double></td><td>Read-write</td><td>Time in minutes a VM is kept in inactive state before destroying.&lt;br>Default value: 10</td><tr><tr><td>quiettime</td><td>&lt;Double></td><td>Read-write</td><td>Time in seconds no other policy is evaluated or action is taken.&lt;br>Default value: 300</td><tr><tr><td>vserver</td><td>&lt;String></td><td>Read-write</td><td>Name of the vserver on which autoscale action has to be taken.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
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
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>},"sessionid":"##sessionid","autoscaleaction":{      "name":<String_value>,      "type":<String_value>,      "profilename":<String_value>,      "parameters":<String_value>,      "vmdestroygraceperiod":<Double_value>,      "quiettime":<Double_value>,      "vserver":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/autoscaleaction/name_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/autoscaleaction/name_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","autoscaleaction":{      "name":<String_value>,      "profilename":<String_value>,      "parameters":<String_value>,      "vmdestroygraceperiod":<Double_value>,      "quiettime":<Double_value>,      "vserver":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","autoscaleaction":{      "name":<String_value>,      "vmdestroygraceperiod":true,      "quiettime":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/autoscaleaction
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/autoscaleaction?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of autoscaleaction resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/autoscaleaction?view=summary
Use this query-parameter to get the summary output of autoscaleaction resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/autoscaleaction?pagesize=#no;pageno=#no
Use this query-parameter to get the autoscaleaction resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/autoscaleaction?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "autoscaleaction": [ {      "name":<String_value>,      "type":<String_value>,      "profilename":<String_value>,      "parameters":<String_value>,      "vmdestroygraceperiod":<Double_value>,      "quiettime":<Double_value>,      "vserver":<String_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/autoscaleaction/name_value&lt;String&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "autoscaleaction": [ {      "name":<String_value>,      "type":<String_value>,      "profilename":<String_value>,      "parameters":<String_value>,      "vmdestroygraceperiod":<Double_value>,      "quiettime":<Double_value>,      "vserver":<String_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/autoscaleaction?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",autoscaleaction: [ { "__count": "#no"} ] }


