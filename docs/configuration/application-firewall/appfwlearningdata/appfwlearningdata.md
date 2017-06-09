#appfwlearningdata

Configuration for learning data resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>profilename</td><td>&lt;String></td><td>Read-write</td><td>Name of the profile.</td><tr><tr><td>starturl</td><td>&lt;String></td><td>Read-write</td><td>Start URL configuration.&lt;br>Minimum length = 1</td><tr><tr><td>cookieconsistency</td><td>&lt;String></td><td>Read-write</td><td>Cookie Name.&lt;br>Minimum length = 1</td><tr><tr><td>fieldconsistency</td><td>&lt;String></td><td>Read-write</td><td>Form field name.&lt;br>Minimum length = 1</td><tr><tr><td>formactionurl_ffc</td><td>&lt;String></td><td>Read-write</td><td>Form action URL.</td><tr><tr><td>contenttype</td><td>&lt;String></td><td>Read-write</td><td>Content Type Name.&lt;br>Minimum length = 1</td><tr><tr><td>crosssitescripting</td><td>&lt;String></td><td>Read-write</td><td>Cross-site scripting.&lt;br>Minimum length = 1</td><tr><tr><td>formactionurl_xss</td><td>&lt;String></td><td>Read-write</td><td>Form action URL.&lt;br>Minimum length = 1</td><tr><tr><td>as_scan_location_xss</td><td>&lt;String></td><td>Read-write</td><td>Location of cross-site scripting exception - form field, header or cookie.&lt;br>Possible values = FORMFIELD, HEADER, COOKIE</td><tr><tr><td>as_value_type_xss</td><td>&lt;String></td><td>Read-write</td><td>XSS value type. (Tag | Attribute | Pattern).&lt;br>Possible values = Tag, Attribute, Pattern</td><tr><tr><td>as_value_expr_xss</td><td>&lt;String></td><td>Read-write</td><td>XSS value expressions consistituting expressions for Tag, Attribute or Pattern.</td><tr><tr><td>sqlinjection</td><td>&lt;String></td><td>Read-write</td><td>Form field name.&lt;br>Minimum length = 1</td><tr><tr><td>formactionurl_sql</td><td>&lt;String></td><td>Read-write</td><td>Form action URL.&lt;br>Minimum length = 1</td><tr><tr><td>as_scan_location_sql</td><td>&lt;String></td><td>Read-write</td><td>Location of sql injection exception - form field, header or cookie.&lt;br>Possible values = FORMFIELD, HEADER, COOKIE</td><tr><tr><td>as_value_type_sql</td><td>&lt;String></td><td>Read-write</td><td>SQL value type. Keyword, SpecialString or Wildchar.&lt;br>Possible values = Keyword, SpecialString, Wildchar</td><tr><tr><td>as_value_expr_sql</td><td>&lt;String></td><td>Read-write</td><td>SQL value expressions consistituting expressions for Keyword, SpecialString or Wildchar.</td><tr><tr><td>fieldformat</td><td>&lt;String></td><td>Read-write</td><td>Field format name.&lt;br>Minimum length = 1</td><tr><tr><td>formactionurl_ff</td><td>&lt;String></td><td>Read-write</td><td>Form action URL.&lt;br>Minimum length = 1</td><tr><tr><td>csrftag</td><td>&lt;String></td><td>Read-write</td><td>CSRF Form Action URL.&lt;br>Minimum length = 1</td><tr><tr><td>csrfformoriginurl</td><td>&lt;String></td><td>Read-write</td><td>CSRF Form Origin URL.&lt;br>Minimum length = 1</td><tr><tr><td>creditcardnumber</td><td>&lt;String></td><td>Read-write</td><td>The object expression that is to be excluded from safe commerce check.&lt;br>Minimum length = 1</td><tr><tr><td>creditcardnumberurl</td><td>&lt;String></td><td>Read-write</td><td>The url for which the list of credit card numbers are needed to be bypassed from inspection.&lt;br>Minimum length = 1</td><tr><tr><td>xmldoscheck</td><td>&lt;String></td><td>Read-write</td><td>XML Denial of Service check, one of MaxAttributes MaxAttributeNameLength MaxAttributeValueLength MaxElementNameLength MaxFileSize MinFileSize MaxCDATALength MaxElements MaxElementDepth MaxElementChildren NumDTDs NumProcessingInstructions NumExternalEntities MaxEntityExpansions MaxEntityExpansionDepth MaxNamespaces MaxNamespaceUriLength MaxSOAPArraySize MaxSOAPArrayRank .&lt;br>Minimum length = 1</td><tr><tr><td>xmlwsicheck</td><td>&lt;String></td><td>Read-write</td><td>Web Services Interoperability Rule ID.&lt;br>Minimum length = 1</td><tr><tr><td>xmlattachmentcheck</td><td>&lt;String></td><td>Read-write</td><td>XML Attachment Content-Type.&lt;br>Minimum length = 1</td><tr><tr><td>totalxmlrequests</td><td>&lt;Boolean></td><td>Read-write</td><td>Total XML requests.</td><tr><tr><td>securitycheck</td><td>&lt;String></td><td>Read-write</td><td>Name of the security check.&lt;br>Possible values = startURL, cookieConsistency, fieldConsistency, crossSiteScripting, SQLInjection, fieldFormat, CSRFtag, XMLDoSCheck, XMLWSICheck, XMLAttachmentCheck, TotalXMLRequests, creditCardNumber, ContentType</td><tr><tr><td>target</td><td>&lt;String></td><td>Read-write</td><td>Target filename for data to be exported.&lt;br>Minimum length = 1&lt;br>Maximum length = 127</td><tr><tr><td>url</td><td>&lt;String></td><td>Read-only</td><td>Learnt url.</td><tr><tr><td>name</td><td>&lt;String></td><td>Read-only</td><td>Learnt field name.</td><tr><tr><td>fieldtype</td><td>&lt;String></td><td>Read-only</td><td>Learnt field type.</td><tr><tr><td>fieldformatminlength</td><td>&lt;Double></td><td>Read-only</td><td>The minimum allowed length for data in this form field.</td><tr><tr><td>fieldformatmaxlength</td><td>&lt;Double></td><td>Read-only</td><td>The maximum allowed length for data in this form field.</td><tr><tr><td>fieldformatcharmappcre</td><td>&lt;String></td><td>Read-only</td><td>Form field value allowed character map.</td><tr><tr><td>value_type</td><td>&lt;String></td><td>Read-only</td><td>Learnt field value type.</td><tr><tr><td>value</td><td>&lt;String></td><td>Read-only</td><td>Learnt field value.</td><tr><tr><td>hits</td><td>&lt;Double></td><td>Read-only</td><td>Learnt entity hit count.</td><tr><tr><td>data</td><td>&lt;String></td><td>Read-only</td><td>Learned data.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[DELETE](#delete) | [RESET](#reset) | [EXPORT](#export) | [GET (ALL)](#get-(all)) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/appfwlearningdata
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/appfwlearningdata/_value&lt;&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###reset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"reset"},"sessionid":"##sessionid","appfwlearningdata":{}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###export



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"export"},"sessionid":"##sessionid","appfwlearningdata":{      "profilename":<String_value>,      "securitycheck":<String_value>,      "target":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/appfwlearningdata
Query-parameters:
args
http://&lt;NSIP&gt;/nitro/v1/config/appfwlearningdata?args=      "profilename":&lt;String_value&gt;,      "securitycheck":&lt;String_value&gt;,
Use this query-parameter to get appfwlearningdata resources based on additional properties.


filter
http://&lt;NSIP&gt;/nitro/v1/config/appfwlearningdata?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of appfwlearningdata resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/appfwlearningdata?view=summary
Use this query-parameter to get the summary output of appfwlearningdata resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/appfwlearningdata?pagesize=#no;pageno=#no
Use this query-parameter to get the appfwlearningdata resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/appfwlearningdata?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "appfwlearningdata": [ {      "profilename":<String_value>,      "securitycheck":<String_value>,      "url":<String_value>,      "name":<String_value>,      "fieldtype":<String_value>,      "fieldformatminlength":<Double_value>,      "fieldformatmaxlength":<Double_value>,      "fieldformatcharmappcre":<String_value>,      "value_type":<String_value>,      "value":<String_value>,      "hits":<Double_value>,      "data":<String_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/appfwlearningdata?args=     "profilename":&lt;String_value&gt;,      "securitycheck":&lt;String_value&gt;,;count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",appfwlearningdata: [ { "__count": "#no"} ] }


