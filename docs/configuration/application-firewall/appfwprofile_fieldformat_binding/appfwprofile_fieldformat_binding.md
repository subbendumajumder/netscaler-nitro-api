#appfwprofile_fieldformat_binding

Binding object showing the fieldformat that can be bound to appfwprofile.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>state</td><td>&lt;String></td><td>Read-write</td><td>Enabled.&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>fieldformatmaxlength</td><td>&lt;Double></td><td>Read-write</td><td>The maximum allowed length for data in this form field.</td><tr><tr><td>isregex_ff</td><td>&lt;String></td><td>Read-write</td><td>Is the form field name a regular expression?.&lt;br>Possible values = REGEX, NOTREGEX</td><tr><tr><td>fieldtype</td><td>&lt;String></td><td>Read-write</td><td>The field type you are assigning to this form field.</td><tr><tr><td>formactionurl_ff</td><td>&lt;String></td><td>Read-write</td><td>Action URL of the form field to which a field format will be assigned.</td><tr><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name of the profile to which to bind an exemption or rule.&lt;br>Minimum length = 1</td><tr><tr><td>fieldformatminlength</td><td>&lt;Double></td><td>Read-write</td><td>The minimum allowed length for data in this form field.</td><tr><tr><td>comment</td><td>&lt;String></td><td>Read-write</td><td>Any comments about the purpose of profile, or other useful information about the profile.</td><tr><tr><td>fieldformat</td><td>&lt;String></td><td>Read-write</td><td>Name of the form field to which a field format will be assigned.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-write</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD:](#add:) | [DELETE:](#delete:) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add:



URL: http://NS_IP/nitro/v1/config
HTTP Method: PUT
Request Payload: ```{"params":{      "warning":<String_value>,      "onerror":<String_value>},sessionid":"##sessionid","appfwprofile_fieldformat_binding":{      "name":<String_value>,      "fieldformat":<String_value>,                  "formactionurl_ff":<String_value>,                  "fieldtype":<String_value>,                  "fieldformatminlength":<Double_value>,                  "fieldformatmaxlength":<Double_value>,                  "isregex_ff":<String_value>,      "comment":<String_value>,      "state":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete:



URL: http://&lt;NS_IP&gt;/nitro/v1/config/appfwprofile_fieldformat_binding/name_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/appfwprofile_fieldformat_binding/name_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/appfwprofile_fieldformat_binding/name_value&lt;String&gt;
Query-parameters:
filter
http://&lt;NS_IP&gt;/nitro/v1/config/appfwprofile_fieldformat_binding/name_value&lt;String&gt;?filter=property-name1:property-value1,property-name2:property-value2
Use this query-parameter to get the filtered set of appfwprofile_fieldformat_binding resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/appfwprofile_fieldformat_binding/name_value&lt;String&gt;?pagesize=#no;pageno=#no
Use this query-parameter to get the appfwprofile_fieldformat_binding resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/appfwprofile_fieldformat_binding?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "appfwprofile_fieldformat_binding": [ {      "state":<String_value>,      "fieldformatmaxlength":<Double_value>,      "isregex_ff":<String_value>,      "fieldtype":<String_value>,      "formactionurl_ff":<String_value>,      "name":<String_value>,      "fieldformatminlength":<Double_value>,      "comment":<String_value>,      "fieldformat":<String_value>,}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/appfwprofile_fieldformat_binding/name_value&lt;String&gt;?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",appfwprofile_fieldformat_binding: [ { "__count": "#no"} ] }


