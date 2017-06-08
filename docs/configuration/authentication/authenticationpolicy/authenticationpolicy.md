#authenticationpolicy

Configuration for Authentication Policy resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the advance AUTHENTICATION policy. Must begin with a letter, number, or the underscore character (_), and must contain only letters, numbers, and the hyphen (-), period (.) pound (#), space ( ), at (@), equals (=), colon (:), and underscore characters. Cannot be changed after AUTHENTICATION policy is created. The following requirement applies only to the NetScaler CLI: If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my authentication policy" or my authentication policy).&lt;br>Minimum length = 1</td><tr><tr><td>rule</td><td>&lt;String></td><td>Read-write</td><td>Name of the NetScaler named rule, or a default syntax expression, that the policy uses to determine whether to attempt to authenticate the user with the AUTHENTICATION server.</td><tr><tr><td>action</td><td>&lt;String></td><td>Read-write</td><td>Name of the authentication action to be performed if the policy matches.</td><tr><tr><td>undefaction</td><td>&lt;String></td><td>Read-write</td><td>Action to perform if the result of policy evaluation is undefined (UNDEF). An UNDEF event indicates an internal error condition. Only the above built-in actions can be used.</td><tr><tr><td>comment</td><td>&lt;String></td><td>Read-write</td><td>Any comments to preserve information about this policy.</td><tr><tr><td>logaction</td><td>&lt;String></td><td>Read-write</td><td>Name of messagelog action to use when a request matches this policy.</td><tr><tr><td>newname</td><td>&lt;String></td><td>Read-write</td><td>New name for the authentication policy. Must begin with a letter, number, or the underscore character (_), and must contain only letters, numbers, and the hyphen (-), period (.) hash (#), space ( ), at (@), equals (=), colon (:), and underscore characters. The following requirement applies only to the NetScaler CLI: If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my authentication policy" or my authentication policy).&lt;br>Minimum length = 1</td><tr><tr><td>hits</td><td>&lt;Double></td><td>Read-only</td><td>Number of hits.</td><tr><tr><td>boundto</td><td>&lt;String></td><td>Read-only</td><td>The entity name to which policy is bound.</td><tr><tr><td>activepolicy</td><td>&lt;Double></td><td>Read-only</td><td>.</td><tr><tr><td>priority</td><td>&lt;Double></td><td>Read-only</td><td>.</td><tr><tr><td>nextfactor</td><td>&lt;String></td><td>Read-only</td><td>On success invoke label.</td><tr><tr><td>gotopriorityexpression</td><td>&lt;String></td><td>Read-only</td><td>Expression specifying the priority of the next policy which will get evaluated if the current policy rule evaluates to TRUE.</td><tr><tr><td>description</td><td>&lt;String></td><td>Read-only</td><td>Description of the policy.</td><tr><tr><td>policysubtype</td><td>&lt;String></td><td>Read-only</td><td>.&lt;br>Possible values = LOCAL, RADIUS, LDAP, TACACS, CERT, NEGOTIATE, SAML, PROFILE, SAMLIDP, WEBAUTH</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
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
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>},"sessionid":"##sessionid","authenticationpolicy":{      "name":<String_value>,      "rule":<String_value>,      "action":<String_value>,      "undefaction":<String_value>,      "comment":<String_value>,      "logaction":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/authenticationpolicy/name_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/authenticationpolicy/name_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","authenticationpolicy":{      "name":<String_value>,      "rule":<String_value>,      "action":<String_value>,      "undefaction":<String_value>,      "comment":<String_value>,      "logaction":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","authenticationpolicy":{      "name":<String_value>,      "undefaction":true,      "comment":true,      "logaction":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###rename



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"rename"},"sessionid":"##sessionid","authenticationpolicy":{      "name":<String_value>,      "newname":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/authenticationpolicy
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/authenticationpolicy?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of authenticationpolicy resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/authenticationpolicy?view=summary
Use this query-parameter to get the summary output of authenticationpolicy resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/authenticationpolicy?pagesize=#no;pageno=#no
Use this query-parameter to get the authenticationpolicy resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/authenticationpolicy?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "authenticationpolicy": [ {      "name":<String_value>,      "rule":<String_value>,      "action":<String_value>,      "undefaction":<String_value>,      "comment":<String_value>,      "logaction":<String_value>,      "hits":<Double_value>,      "boundto":<String_value>,      "activepolicy":<Double_value>,      "priority":<Double_value>,      "nextfactor":<String_value>,      "gotopriorityexpression":<String_value>,      "description":<String_value>,      "policysubtype":<String_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/authenticationpolicy/name_value&lt;String&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "authenticationpolicy": [ {      "name":<String_value>,      "rule":<String_value>,      "action":<String_value>,      "undefaction":<String_value>,      "comment":<String_value>,      "logaction":<String_value>,      "hits":<Double_value>,      "boundto":<String_value>,      "activepolicy":<Double_value>,      "priority":<Double_value>,      "nextfactor":<String_value>,      "gotopriorityexpression":<String_value>,      "description":<String_value>,      "policysubtype":<String_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/authenticationpolicy?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",authenticationpolicy: [ { "__count": "#no"} ] }


