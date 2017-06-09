#rewriteaction

Configuration for rewrite action resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the user-defined rewrite action. Must begin with a letter, number, or the underscore character (_), and must contain only letters, numbers, and the hyphen (-), period (.) hash (#), space ( ), at (@), equals (=), colon (:), and underscore characters. Can be changed after the rewrite policy is added. The following requirement applies only to the NetScaler CLI: If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my rewrite action" or ?my rewrite action?).</td><tr><tr><td>type</td><td>&lt;String></td><td>Read-write</td><td>Type of user-defined rewrite action. The information that you provide for, and the effect of, each type are as follows:: * REPLACE ;lt;target;gt; ;lt;string_builder_expr;gt;. Replaces the string with the string-builder expression. * REPLACE_ALL ;lt;target;gt; ;lt;string_builder_expr1;gt; -(pattern|search) ;lt;string_builder_expr2;gt;. In the request or response specified by ;lt;target;gt;, replaces all occurrences of the string defined by ;lt;string_builder_expr1;gt; with the string defined by ;lt;string_builder_expr2;gt;. You can use a PCRE-format pattern or the search facility to find the strings to be replaced. * REPLACE_HTTP_RES ;lt;string_builder_expr;gt;. Replaces the complete HTTP response with the string defined by the string-builder expression. * REPLACE_SIP_RES ;lt;target;gt; - Replaces the complete SIP response with the string specified by ;lt;target;gt;. * INSERT_HTTP_HEADER ;lt;header_string_builder_expr;gt; ;lt;contents_string_builder_expr;gt;. Inserts the HTTP header specified by ;lt;header_string_builder_expr;gt; and header contents specified by ;lt;contents_string_builder_expr;gt;. * DELETE_HTTP_HEADER ;lt;target;gt;. Deletes the HTTP header specified by ;lt;target;gt;. * CORRUPT_HTTP_HEADER ;lt;target;gt;. Replaces the header name of all occurrences of the HTTP header specified by ;lt;target;gt; with a corrupted name, so that it will not be recognized by the receiver Example: MY_HEADER is changed to MHEY_ADER. * INSERT_BEFORE ;lt;string_builder_expr1;gt; ;lt;string_builder_expr1;gt;. Finds the string specified in ;lt;string_builder_expr1;gt; and inserts the string in ;lt;string_builder_expr2;gt; before it. * INSERT_BEFORE_ALL ;lt;target;gt; ;lt;string_builder_expr1;gt; -(pattern|search) ;lt;string_builder_expr2;gt;. In the request or response specified by ;lt;target;gt;, locates all occurrences of the string specified in ;lt;string_builder_expr1;gt; and inserts the string specified in ;lt;string_builder_expr2;gt; before each. You can use a PCRE-format pattern or the search facility to find the strings. * INSERT_AFTER ;lt;string_builder_expr1;gt; ;lt;string_builder_expr2;gt;. Finds the string specified in ;lt;string_builder_expr1;gt;, and inserts the string specified in ;lt;string_builder_expr2;gt; after it. * INSERT_AFTER_ALL ;lt;target;gt; ;lt;string_builder_expr1;gt; -(pattern|search) ;lt;string_builder_expr;gt;. In the request or response specified by ;lt;target;gt;, locates all occurrences of the string specified by ;lt;string_builder_expr1;gt; and inserts the string specified by ;lt;string_builder_expr2;gt; after each. You can use a PCRE-format pattern or the search facility to find the strings. * DELETE ;lt;target;gt;. Finds and deletes the specified target. * DELETE_ALL ;lt;target;gt; -(pattern|search) ;lt;string_builder_expr;gt;. In the request or response specified by ;lt;target;gt;, locates and deletes all occurrences of the string specified by ;lt;string_builder_expr;gt;. You can use a PCRE-format pattern or the search facility to find the strings. * REPLACE_DIAMETER_HEADER_FIELD ;lt;target;gt; ;lt;field value;gt;. In the request or response modify the header field specified by ;lt;target;gt;. Use Diameter.req.flags.SET(;lt;flag;gt;) or Diameter.req.flags.UNSET;lt;flag;gt; as stringbuilderexpression to set or unset flags. * REPLACE_DNS_HEADER_FIELD ;lt;target;gt;. In the request or response modify the header field specified by ;lt;target;gt;. * REPLACE_DNS_ANSWER_SECTION ;lt;target;gt;. Replace the DNS answer section in the response. This is currently applicable for A and AAAA records only. Use DNS.NEW_RRSET_A ;amp; DNS.NEW_RRSET_AAAA expressions to configure the new answer section .&lt;br>Possible values = noop, delete, insert_http_header, delete_http_header, corrupt_http_header, insert_before, insert_after, replace, replace_http_res, delete_all, replace_all, insert_before_all, insert_after_all, clientless_vpn_encode, clientless_vpn_encode_all, clientless_vpn_decode, clientless_vpn_decode_all, insert_sip_header, delete_sip_header, corrupt_sip_header, replace_sip_res, replace_diameter_header_field, replace_dns_header_field, replace_dns_answer_section</td><tr><tr><td>target</td><td>&lt;String></td><td>Read-write</td><td>Default syntax expression that specifies which part of the request or response to rewrite.&lt;br>Minimum length = 1</td><tr><tr><td>stringbuilderexpr</td><td>&lt;String></td><td>Read-write</td><td>Default syntax expression that specifies the content to insert into the request or response at the specified location, or that replaces the specified string.</td><tr><tr><td>pattern</td><td>&lt;String></td><td>Read-write</td><td>Pattern that is used to match multiple strings in the request or response. The pattern may be a string literal (without quotes) or a PCRE-format regular expression with a delimiter that consists of any printable ASCII non-alphanumeric character except for the underscore (_) and space ( ) that is not otherwise used in the expression. Example: re~https?://|HTTPS?://~ The preceding regular expression can use the tilde (~) as the delimiter because that character does not appear in the regular expression itself. Used in the INSERT_BEFORE_ALL, INSERT_AFTER_ALL, REPLACE_ALL, and DELETE_ALL action types.</td><tr><tr><td>search</td><td>&lt;String></td><td>Read-write</td><td>Search facility that is used to match multiple strings in the request or response. Used in the INSERT_BEFORE_ALL, INSERT_AFTER_ALL, REPLACE_ALL, and DELETE_ALL action types. The following search types are supported: * Text ("text(string)") - A literal string. Example: -search text("hello") * Regular expression (?regex(re;lt;delimiter;gt;regular exp;lt;delimiter;gt;)?) - Pattern that is used to match multiple strings in the request or response. The pattern may be a string literal (without quotes) or a PCRE-format regular expression with a delimiter that consists of any printable ASCII non-alphanumeric character except for the underscore (_) and space ( ) that is not otherwise used in the expression. Example: -search regex(re~^hello~) The preceding regular expression can use the tilde (~) as the delimiter because that character does not appear in the regular expression itself. * XPath ("xpath(xp;lt;delimiter;gt;xpath expression;lt;delimiter;gt;)") - An XPath expression. Example: -search xpath(xp%/a/b%) * JSON ("xpath_json(xp;lt;delimiter;gt;xpath expression;lt;delimiter;gt;)") - An XPath JSON expression. Example: -search xpath_json(xp%/a/b%) NOTE: JSON searches use the same syntax as XPath searches, but operate on JSON files instead of standard XML files. * Patset ("patset(patset)") - A predefined pattern set. Example: -search patset("patset1"). * Datset ("dataset(dataset)") - A predefined dataset. Example: -search dataset("dataset1"). * AVP ("avp(avp number)") - AVP number that is used to match multiple AVPs in a Diameter/Radius Message. Example: -search avp(999).</td><tr><tr><td>bypasssafetycheck</td><td>&lt;String></td><td>Read-write</td><td>Bypass the safety check and allow unsafe expressions. An unsafe expression is one that contains references to message elements that might not be present in all messages. If an expression refers to a missing request element, an empty string is used instead.&lt;br>Default value: NO&lt;br>Possible values = YES, NO</td><tr><tr><td>refinesearch</td><td>&lt;String></td><td>Read-write</td><td>Specify additional criteria to refine the results of the search. Always starts with the "extend(m,n)" operation, where m specifies number of bytes to the left of selected data and n specifies number of bytes to the right of selected data. You can use refineSearch only on body expressions, and for the INSERT_BEFORE_ALL, INSERT_AFTER_ALL, REPLACE_ALL, and DELETE_ALL action types.</td><tr><tr><td>comment</td><td>&lt;String></td><td>Read-write</td><td>Comment. Can be used to preserve information about this rewrite action.</td><tr><tr><td>newname</td><td>&lt;String></td><td>Read-write</td><td>New name for the rewrite action. Must begin with a letter, number, or the underscore character (_), and must contain only letters, numbers, and the hyphen (-), period (.) hash (#), space ( ), at (@), equals (=), colon (:), and underscore characters. Can be changed after the rewrite policy is added. The following requirement applies only to the NetScaler CLI: If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my rewrite action" or ?my rewrite action?).&lt;br>Minimum length = 1</td><tr><tr><td>hits</td><td>&lt;Double></td><td>Read-only</td><td>The number of times the action has been taken.</td><tr><tr><td>undefhits</td><td>&lt;Double></td><td>Read-only</td><td>The number of times the action resulted in UNDEF.</td><tr><tr><td>referencecount</td><td>&lt;Double></td><td>Read-only</td><td>The number of references to the action.</td><tr><tr><td>description</td><td>&lt;String></td><td>Read-only</td><td>Description of the action.</td><tr><tr><td>isdefault</td><td>&lt;Boolean></td><td>Read-only</td><td>A value of true is returned if it is a default rewriteaction.</td><tr><tr><td>builtin</td><td>&lt;String[]></td><td>Read-only</td><td>Flag to determine whether rewrite action is built-in or not.&lt;br>Possible values = MODIFIABLE, DELETABLE, IMMUTABLE, PARTITION_ALL</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
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
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>},"sessionid":"##sessionid","rewriteaction":{      "name":<String_value>,      "type":<String_value>,      "target":<String_value>,      "stringbuilderexpr":<String_value>,      "pattern":<String_value>,      "search":<String_value>,      "bypasssafetycheck":<String_value>,      "refinesearch":<String_value>,      "comment":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/rewriteaction/name_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/rewriteaction/name_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","rewriteaction":{      "name":<String_value>,      "target":<String_value>,      "stringbuilderexpr":<String_value>,                  "bypasssafetycheck":<String_value>,      "pattern":<String_value>,      "search":<String_value>,      "bypasssafetycheck":<String_value>,      "refinesearch":<String_value>,      "comment":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","rewriteaction":{      "name":<String_value>,      "stringbuilderexpr":true,      "refinesearch":true,      "comment":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###rename



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"rename"},"sessionid":"##sessionid","rewriteaction":{      "name":<String_value>,      "newname":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/rewriteaction
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/rewriteaction?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of rewriteaction resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/rewriteaction?view=summary
Use this query-parameter to get the summary output of rewriteaction resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/rewriteaction?pagesize=#no;pageno=#no
Use this query-parameter to get the rewriteaction resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/rewriteaction?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "rewriteaction": [ {      "name":<String_value>,      "type":<String_value>,      "target":<String_value>,      "stringbuilderexpr":<String_value>,      "pattern":<String_value>,      "search":<String_value>,      "bypasssafetycheck":<String_value>,      "refinesearch":<String_value>,      "hits":<Double_value>,      "undefhits":<Double_value>,      "referencecount":<Double_value>,      "description":<String_value>,      "isdefault":<Boolean_value>,      "comment":<String_value>,      "builtin":<String[]_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/rewriteaction/name_value&lt;String&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "rewriteaction": [ {      "name":<String_value>,      "type":<String_value>,      "target":<String_value>,      "stringbuilderexpr":<String_value>,      "pattern":<String_value>,      "search":<String_value>,      "bypasssafetycheck":<String_value>,      "refinesearch":<String_value>,      "hits":<Double_value>,      "undefhits":<Double_value>,      "referencecount":<Double_value>,      "description":<String_value>,      "isdefault":<Boolean_value>,      "comment":<String_value>,      "builtin":<String[]_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/rewriteaction?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",rewriteaction: [ { "__count": "#no"} ] }


