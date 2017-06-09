#policyevaluation

Configuration for expr evaluation resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>expression</td><td>&lt;String></td><td>Read-write</td><td>Expression string. For example: http.req.body(100).contains("this").</td><tr><tr><td>action</td><td>&lt;String></td><td>Read-write</td><td>Rewrite action name. Supported rewrite action types are:&lt;br>-delete&lt;br>-delete_all&lt;br>-delete_http_header&lt;br>-insert_after&lt;br>-insert_after_all&lt;br>-insert_before&lt;br>-insert_before_all&lt;br>-insert_http_header&lt;br>-replace&lt;br>-replace_all&lt;br>.&lt;br>Minimum length = 1</td><tr><tr><td>type</td><td>&lt;String></td><td>Read-write</td><td>Indicates request or response input packet.&lt;br>Possible values = HTTP_REQ, HTTP_RES, TEXT</td><tr><tr><td>input</td><td>&lt;String></td><td>Read-write</td><td>Text representation of input packet.</td><tr><tr><td>pitmodifiedinputdata</td><td>&lt;String></td><td>Read-only</td><td>Text representation of packet after evaluating expression or rewrite action.</td><tr><tr><td>pitboolresult</td><td>&lt;Boolean></td><td>Read-only</td><td>Result of the expression in bool format.</td><tr><tr><td>pitnumresult</td><td>&lt;Double></td><td>Read-only</td><td>Result of the expression in num format.</td><tr><tr><td>pitdoubleresult</td><td>&lt;Double></td><td>Read-only</td><td>Result of the expression in double format.</td><tr><tr><td>pitulongresult</td><td>&lt;Double></td><td>Read-only</td><td>Result of the expression in unsigned long format.</td><tr><tr><td>pitrefresult</td><td>&lt;String></td><td>Read-only</td><td>Result of the expression in string format.</td><tr><tr><td>pitoffsetresult</td><td>&lt;Double></td><td>Read-only</td><td>Offset of the resultant sting.</td><tr><tr><td>pitoffsetresultlen</td><td>&lt;Double></td><td>Read-only</td><td>Offset length of the resultant sting.</td><tr><tr><td>istruncatedrefresult</td><td>&lt;Boolean></td><td>Read-only</td><td>Identify whether ref result is truncated result.</td><tr><tr><td>pitboolevaltime</td><td>&lt;Double></td><td>Read-only</td><td>Average evaluation time of bool type expression in nanoseconds.</td><tr><tr><td>pitnumevaltime</td><td>&lt;Double></td><td>Read-only</td><td>Average evaluation time of num type expression in nanoseconds.</td><tr><tr><td>pitdoubleevaltime</td><td>&lt;Double></td><td>Read-only</td><td>Average evaluation time of double type expression in nanoseconds.</td><tr><tr><td>pitulongevaltime</td><td>&lt;Double></td><td>Read-only</td><td>Average evaluation time of unsigned long type expression in nanoseconds.</td><tr><tr><td>pitrefevaltime</td><td>&lt;Double></td><td>Read-only</td><td>Average evaluation time of string type expression in nanoseconds.</td><tr><tr><td>pitoffsetevaltime</td><td>&lt;Double></td><td>Read-only</td><td>Average evaluation time in finding offset of the resultant string in the input. Time is in nanoseconds.</td><tr><tr><td>pitactionevaltime</td><td>&lt;Double></td><td>Read-only</td><td>Average evaluation time of rewrite action in nanoseconds.</td><tr><tr><td>pitoperationperformerarray</td><td>&lt;String[]></td><td>Read-only</td><td>Details of the operation NS performed at various offsets during applying of rewrite action on input data. Operation can be insertion, modfication or deletion.&lt;br>Possible values = INSERT, MODIFY, DELETE</td><tr><tr><td>pitoldoffsetarray</td><td>&lt;Double[]></td><td>Read-only</td><td>Details of the offsets in the input data at which NS either inserted or modified or deleted data during applying of rewrite action.</td><tr><tr><td>pitnewoffsetarray</td><td>&lt;Double[]></td><td>Read-only</td><td>Details of the offsets in the output data at which NS either inserted or modified or deleted data during applying of rewrite action.</td><tr><tr><td>pitoffsetlengtharray</td><td>&lt;Integer[]></td><td>Read-only</td><td>Details of the lengths of the data which NS either inserted or modified or deleted during applying of rewrite action.</td><tr><tr><td>pitboolerrorresult</td><td>&lt;String></td><td>Read-only</td><td>Result of the bool type expression if any error occurs during evaluation. Result will be in string format.</td><tr><tr><td>pitnumerrorresult</td><td>&lt;String></td><td>Read-only</td><td>Result of the num type expression if any error occurs during evaluation. Result will be in string format.</td><tr><tr><td>pitdoubleerrorresult</td><td>&lt;String></td><td>Read-only</td><td>Result of the double type expression if any error occurs during evaluation. Result will be in string format.</td><tr><tr><td>pitulongerrorresult</td><td>&lt;String></td><td>Read-only</td><td>Result of the unsigned long type expression if any error occurs during evaluation. Result will be in string format.</td><tr><tr><td>pitreferrorresult</td><td>&lt;String></td><td>Read-only</td><td>Result of the ref type expression if any error occurs during evaluation. Result will be in string format.</td><tr><tr><td>pitoffseterrorresult</td><td>&lt;String></td><td>Read-only</td><td>Result of the expression if any error occurs in calculating offset. Result will be in string format.</td><tr><tr><td>pitactionerrorresult</td><td>&lt;String></td><td>Read-only</td><td>Result of the action if any error occurs in evaluation. Result will be in string format.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[GET (ALL)](#get-(all)) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/policyevaluation
Query-parameters:
args
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/policyevaluation?args=expression:&lt;String_value&gt;,action:&lt;String_value&gt;,type:&lt;String_value&gt;,input:&lt;String_value&gt;,
Use this query-parameter to get policyevaluation resources based on additional properties.


attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/policyevaluation?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


filter
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/policyevaluation?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of policyevaluation resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/policyevaluation?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).


pagination
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/policyevaluation?pagesize=#no;pageno=#no
Use this query-parameter to get the policyevaluation resources in chunks.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "policyevaluation": [ {expression:<String_value>,action:<String_value>,type:<String_value>,input:<String_value>,      "pitmodifiedinputdata":<String_value>,      "pitboolresult":<Boolean_value>,      "pitnumresult":<Double_value>,      "pitdoubleresult":<Double_value>,      "pitulongresult":<Double_value>,      "pitrefresult":<String_value>,      "pitoffsetresult":<Double_value>,      "pitoffsetresultlen":<Double_value>,      "istruncatedrefresult":<Boolean_value>,      "pitboolevaltime":<Double_value>,      "pitnumevaltime":<Double_value>,      "pitdoubleevaltime":<Double_value>,      "pitulongevaltime":<Double_value>,      "pitrefevaltime":<Double_value>,      "pitoffsetevaltime":<Double_value>,      "pitactionevaltime":<Double_value>,      "pitoperationperformerarray":<String[]_value>,      "pitoldoffsetarray":<Double[]_value>,      "pitnewoffsetarray":<Double[]_value>,      "pitoffsetlengtharray":<Integer[]_value>,      "pitboolerrorresult":<String_value>,      "pitnumerrorresult":<String_value>,      "pitdoubleerrorresult":<String_value>,      "pitulongerrorresult":<String_value>,      "pitreferrorresult":<String_value>,      "pitoffseterrorresult":<String_value>,      "pitactionerrorresult":<String_value>}]}```



###count



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/policyevaluation?args=expression:&lt;String_value&gt;,action:&lt;String_value&gt;,type:&lt;String_value&gt;,input:&lt;String_value&gt;,;count=yes
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: 
{ "policyevaluation": [ { "__count": "#no"} ] }


