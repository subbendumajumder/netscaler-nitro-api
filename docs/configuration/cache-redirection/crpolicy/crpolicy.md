#crpolicy

Configuration for cache redirection policy resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>policyname</td><td>&lt;String></td><td>Read-write</td><td>Name for the cache redirection policy. Must begin with an ASCII alphanumeric or underscore (_) character, and must contain only ASCII alphanumeric, underscore, hash (#), period (.), space, colon (:), at sign (@), equal sign (=), and hyphen (-) characters. Cannot be changed after the policy is created. The following requirement applies only to the NetScaler CLI: If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, ?my policy? or ?my policy?).&lt;br>Minimum length = 1</td><tr><tr><td>rule</td><td>&lt;String></td><td>Read-write</td><td>Expression, or name of a named expression, against which traffic is evaluated. Written in the classic syntax. Note:Maximum length of a string literal in the expression is 255 characters. A longer string can be split into smaller strings of up to 255 characters each, and the smaller strings concatenated with the + operator. For example, you can create a 500-character string as follows: ";lt;string of 255 characters;gt;" + ";lt;string of 245 characters;gt;" The following requirements apply only to the NetScaler CLI: * If the expression includes one or more spaces, enclose the entire expression in double quotation marks. * If the expression itself includes double quotation marks, escape the quotations by using the \\ character. * Alternatively, you can use single quotation marks to enclose the rule, in which case you do not have to escape the double quotation marks.</td><tr><tr><td>action</td><td>&lt;String></td><td>Read-write</td><td>Name of the built-in cache redirection action: CACHE/ORIGIN.</td><tr><tr><td>logaction</td><td>&lt;String></td><td>Read-write</td><td>The log action associated with the cache redirection policy.</td><tr><tr><td>newname</td><td>&lt;String></td><td>Read-write</td><td>The new name of the content switching policy.&lt;br>Minimum length = 1</td><tr><tr><td>domain</td><td>&lt;String></td><td>Read-only</td><td>Domain name.</td><tr><tr><td>vstype</td><td>&lt;Double></td><td>Read-only</td><td>Virtual server type.</td><tr><tr><td>hits</td><td>&lt;Double></td><td>Read-only</td><td>Total number of hits.</td><tr><tr><td>bindhits</td><td>&lt;Double></td><td>Read-only</td><td>Total number of hits.</td><tr><tr><td>priority</td><td>&lt;Double></td><td>Read-only</td><td>priority of bound policy.</td><tr><tr><td>activepolicy</td><td>&lt;Boolean></td><td>Read-only</td><td>Indicates whether policy is bound or not.</td><tr><tr><td>cspolicytype</td><td>&lt;String></td><td>Read-only</td><td>Indicates whether policy is PI or not.(used only during display).&lt;br>Possible values = Classic Policy, Advanced Policy</td><tr><tr><td>labelname</td><td>&lt;String></td><td>Read-only</td><td>Name of the label invoked.</td><tr><tr><td>labeltype</td><td>&lt;String></td><td>Read-only</td><td>The invocation type.&lt;br>Possible values = reqvserver, resvserver, policylabel</td><tr><tr><td>builtin</td><td>&lt;String[]></td><td>Read-only</td><td>.&lt;br>Possible values = MODIFIABLE, DELETABLE, IMMUTABLE, PARTITION_ALL</td><tr><tr><td>isdefault</td><td>&lt;Boolean></td><td>Read-only</td><td>A value of true is returned if it is a default cr policy.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
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
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>},"sessionid":"##sessionid","crpolicy":{      "policyname":<String_value>,      "rule":<String_value>,      "action":<String_value>,      "logaction":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/crpolicy/policyname_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/crpolicy/policyname_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","crpolicy":{      "policyname":<String_value>,      "rule":<String_value>,      "action":<String_value>,      "logaction":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","crpolicy":{      "policyname":<String_value>,      "logaction":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###rename



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"rename"},"sessionid":"##sessionid","crpolicy":{      "policyname":<String_value>,      "newname":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/crpolicy
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/crpolicy?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of crpolicy resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/crpolicy?view=summary
Use this query-parameter to get the summary output of crpolicy resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/crpolicy?pagesize=#no;pageno=#no
Use this query-parameter to get the crpolicy resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/crpolicy?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "crpolicy": [ {      "policyname":<String_value>,      "rule":<String_value>,      "domain":<String_value>,      "action":<String_value>,      "vstype":<Double_value>,      "hits":<Double_value>,      "bindhits":<Double_value>,      "priority":<Double_value>,      "activepolicy":<Boolean_value>,      "cspolicytype":<String_value>,      "logaction":<String_value>,      "labelname":<String_value>,      "labeltype":<String_value>,      "builtin":<String[]_value>,      "isdefault":<Boolean_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/crpolicy/policyname_value&lt;String&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "crpolicy": [ {      "policyname":<String_value>,      "rule":<String_value>,      "domain":<String_value>,      "action":<String_value>,      "vstype":<Double_value>,      "hits":<Double_value>,      "bindhits":<Double_value>,      "priority":<Double_value>,      "activepolicy":<Boolean_value>,      "cspolicytype":<String_value>,      "logaction":<String_value>,      "labelname":<String_value>,      "labeltype":<String_value>,      "builtin":<String[]_value>,      "isdefault":<Boolean_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/crpolicy?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",crpolicy: [ { "__count": "#no"} ] }


