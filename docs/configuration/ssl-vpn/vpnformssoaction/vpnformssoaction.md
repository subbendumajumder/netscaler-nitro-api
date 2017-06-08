#vpnformssoaction

Configuration for Form sso action resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the form based single sign-on profile.&lt;br>Minimum length = 1</td><tr><tr><td>actionurl</td><td>&lt;String></td><td>Read-write</td><td>Root-relative URL to which the completed form is submitted.&lt;br>Minimum length = 1</td><tr><tr><td>userfield</td><td>&lt;String></td><td>Read-write</td><td>Name of the form field in which the user types in the user ID.&lt;br>Minimum length = 1</td><tr><tr><td>passwdfield</td><td>&lt;String></td><td>Read-write</td><td>Name of the form field in which the user types in the password.&lt;br>Minimum length = 1</td><tr><tr><td>ssosuccessrule</td><td>&lt;String></td><td>Read-write</td><td>Use a frequently used expression or create a custom expression describing the action that the form-based single sign-on profile takes when invoked by a policy. Used for verifying successful single sign-on.</td><tr><tr><td>namevaluepair</td><td>&lt;String></td><td>Read-write</td><td>Other name-value pair attributes to send to the server, in addition to sending the user name and password. Value names are separated by an ampersand (;amp;), such as in name1=value1;amp;name2=value2.</td><tr><tr><td>responsesize</td><td>&lt;Double></td><td>Read-write</td><td>Maximum number of bytes to allow in the response size. Specifies the number of bytes in the response to be parsed for extracting the forms.&lt;br>Default value: 8096</td><tr><tr><td>nvtype</td><td>&lt;String></td><td>Read-write</td><td>How to process the name-value pair. Available settings function as follows: * STATIC - The administrator-configured values are used. * DYNAMIC - The response is parsed, the form is extracted, and then submitted.&lt;br>Default value: DYNAMIC&lt;br>Possible values = STATIC, DYNAMIC</td><tr><tr><td>submitmethod</td><td>&lt;String></td><td>Read-write</td><td>HTTP method (GET or POST) used by the single sign-on form to send the logon credentials to the logon server.&lt;br>Default value: GET&lt;br>Possible values = GET, POST</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
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
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>},"sessionid":"##sessionid","vpnformssoaction":{      "name":<String_value>,      "actionurl":<String_value>,      "userfield":<String_value>,      "passwdfield":<String_value>,      "ssosuccessrule":<String_value>,      "namevaluepair":<String_value>,      "responsesize":<Double_value>,      "nvtype":<String_value>,      "submitmethod":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/vpnformssoaction/name_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/vpnformssoaction/name_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","vpnformssoaction":{      "name":<String_value>,      "actionurl":<String_value>,      "userfield":<String_value>,      "passwdfield":<String_value>,      "ssosuccessrule":<String_value>,      "responsesize":<Double_value>,      "namevaluepair":<String_value>,      "nvtype":<String_value>,      "submitmethod":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","vpnformssoaction":{      "name":<String_value>,      "responsesize":true,      "namevaluepair":true,      "nvtype":true,      "submitmethod":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/vpnformssoaction
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/vpnformssoaction?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of vpnformssoaction resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/vpnformssoaction?view=summary
Use this query-parameter to get the summary output of vpnformssoaction resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/vpnformssoaction?pagesize=#no;pageno=#no
Use this query-parameter to get the vpnformssoaction resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/vpnformssoaction?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "vpnformssoaction": [ {      "name":<String_value>,      "actionurl":<String_value>,      "userfield":<String_value>,      "passwdfield":<String_value>,      "responsesize":<Double_value>,      "namevaluepair":<String_value>,      "nvtype":<String_value>,      "ssosuccessrule":<String_value>,      "submitmethod":<String_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/vpnformssoaction/name_value&lt;String&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "vpnformssoaction": [ {      "name":<String_value>,      "actionurl":<String_value>,      "userfield":<String_value>,      "passwdfield":<String_value>,      "responsesize":<Double_value>,      "namevaluepair":<String_value>,      "nvtype":<String_value>,      "ssosuccessrule":<String_value>,      "submitmethod":<String_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/vpnformssoaction?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",vpnformssoaction: [ { "__count": "#no"} ] }


