#cachepolicy

Configuration for Integrated Cache policy resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>policyname</td><td>&lt;String></td><td>Read-write</td><td>Name for the policy. Must begin with an ASCII alphabetic or underscore (_) character, and must contain only ASCII alphanumeric, underscore, hash (#), period (.), space, colon (:), at (@), equals (=), and hyphen (-) characters. Can be changed after the policy is created.&lt;br>Minimum length = 1</td><tr><tr><td>rule</td><td>&lt;String></td><td>Read-write</td><td>Expression against which the traffic is evaluated. Note: Maximum length of a string literal in the expression is 255 characters. A longer string can be split into smaller strings of up to 255 characters each, and the smaller strings concatenated with the + operator. For example, you can create a 500-character string as follows: ";lt;string of 255 characters;gt;" + ";lt;string of 245 characters;gt;" The following requirements apply only to the NetScaler CLI: * If the expression includes one or more spaces, enclose the entire expression in double quotation marks. * If the expression itself includes double quotation marks, escape the quotations by using the \\ character. * Alternatively, you can use single quotation marks to enclose the rule, in which case you do not have to escape the double quotation marks.</td><tr><tr><td>action</td><td>&lt;String></td><td>Read-write</td><td>Action to apply to content that matches the policy. * CACHE or MAY_CACHE action - positive cachability policy * NOCACHE or MAY_NOCACHE action - negative cachability policy * INVAL action - Dynamic Invalidation Policy.&lt;br>Possible values = CACHE, NOCACHE, MAY_CACHE, MAY_NOCACHE, INVAL</td><tr><tr><td>storeingroup</td><td>&lt;String></td><td>Read-write</td><td>Name of the content group in which to store the object when the final result of policy evaluation is CACHE. The content group must exist before being mentioned here. Use the "show cache contentgroup" command to view the list of existing content groups.&lt;br>Minimum length = 1</td><tr><tr><td>invalgroups</td><td>&lt;String[]></td><td>Read-write</td><td>Content group(s) to be invalidated when the INVAL action is applied. Maximum number of content groups that can be specified is 16.&lt;br>Minimum length = 1</td><tr><tr><td>invalobjects</td><td>&lt;String[]></td><td>Read-write</td><td>Content groups(s) in which the objects will be invalidated if the action is INVAL.&lt;br>Minimum length = 1</td><tr><tr><td>undefaction</td><td>&lt;String></td><td>Read-write</td><td>Action to be performed when the result of rule evaluation is undefined.&lt;br>Possible values = NOCACHE, RESET</td><tr><tr><td>newname</td><td>&lt;String></td><td>Read-write</td><td>New name for the cache policy. Must begin with an ASCII alphabetic or underscore (_) character, and must contain only ASCII alphanumeric, underscore, hash (#), period (.), space, colon (:), at (@), equals (=), and hyphen (-) characters.&lt;br>Minimum length = 1</td><tr><tr><td>hits</td><td>&lt;Double></td><td>Read-only</td><td>Hits.</td><tr><tr><td>undefhits</td><td>&lt;Double></td><td>Read-only</td><td>Number of Undef hits.</td><tr><tr><td>flags</td><td>&lt;Double></td><td>Read-only</td><td>Flag.</td><tr><tr><td>builtin</td><td>&lt;String[]></td><td>Read-only</td><td>.&lt;br>Possible values = MODIFIABLE, DELETABLE, IMMUTABLE, PARTITION_ALL</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
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
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>},"sessionid":"##sessionid","cachepolicy":{      "policyname":<String_value>,      "rule":<String_value>,      "action":<String_value>,      "storeingroup":<String_value>,      "invalgroups":<String[]_value>,      "invalobjects":<String[]_value>,      "undefaction":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/cachepolicy/policyname_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/cachepolicy/policyname_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","cachepolicy":{      "policyname":<String_value>,      "rule":<String_value>,      "action":<String_value>,      "storeingroup":<String_value>,      "invalgroups":<String[]_value>,      "invalobjects":<String[]_value>,      "undefaction":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","cachepolicy":{      "policyname":<String_value>,      "storeingroup":true,      "invalgroups":true,      "invalobjects":true,      "undefaction":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###rename



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"rename"},"sessionid":"##sessionid","cachepolicy":{      "policyname":<String_value>,      "newname":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/cachepolicy
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/cachepolicy?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of cachepolicy resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/cachepolicy?view=summary
Use this query-parameter to get the summary output of cachepolicy resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/cachepolicy?pagesize=#no;pageno=#no
Use this query-parameter to get the cachepolicy resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/cachepolicy?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "cachepolicy": [ {      "policyname":<String_value>,      "rule":<String_value>,      "action":<String_value>,      "storeingroup":<String_value>,      "invalgroups":<String[]_value>,      "invalobjects":<String[]_value>,      "hits":<Double_value>,      "undefaction":<String_value>,      "undefhits":<Double_value>,      "flags":<Double_value>,      "precededefrules":<String_value>,      "builtin":<String[]_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/cachepolicy/policyname_value&lt;String&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "cachepolicy": [ {      "policyname":<String_value>,      "rule":<String_value>,      "action":<String_value>,      "storeingroup":<String_value>,      "invalgroups":<String[]_value>,      "invalobjects":<String[]_value>,      "hits":<Double_value>,      "undefaction":<String_value>,      "undefhits":<Double_value>,      "flags":<Double_value>,      "precededefrules":<String_value>,      "builtin":<String[]_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/cachepolicy?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",cachepolicy: [ { "__count": "#no"} ] }


