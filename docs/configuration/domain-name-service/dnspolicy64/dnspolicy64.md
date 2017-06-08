#dnspolicy64

Configuration for dns64 policy resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the DNS64 policy.</td><tr><tr><td>rule</td><td>&lt;String></td><td>Read-write</td><td>Expression against which DNS traffic is evaluated. Written in the default syntax. Note: * On the command line interface, if the expression includes blank spaces, the entire expression must be enclosed in double quotation marks. * If the expression itself includes double quotation marks, you must escape the quotations by using the character. * Alternatively, you can use single quotation marks to enclose the rule, in which case you do not have to escape the double quotation marks. Maximum length of a string literal in the expression is 255 characters. A longer string can be split into smaller strings of up to 255 characters each, and the smaller strings concatenated with the + operator. For example, you can create a 500-character string as follows: ";lt;string of 255 characters;gt;" + ";lt;string of 245 characters;gt;" Example: CLIENT.IP.SRC.IN_SUBENT(23.34.0.0/16).</td><tr><tr><td>action</td><td>&lt;String></td><td>Read-write</td><td>Name of the DNS64 action to perform when the rule evaluates to TRUE. The built in actions function as follows: * A default dns64 action with prefix ;lt;default prefix;gt; and mapped and exclude are any You can create custom actions by using the add dns action command in the CLI or the DNS64 ;gt; Actions ;gt; Create DNS64 Action dialog box in the NetScaler configuration utility.</td><tr><tr><td>hits</td><td>&lt;Double></td><td>Read-only</td><td>The number of times the policy has been hit.</td><tr><tr><td>labeltype</td><td>&lt;String></td><td>Read-only</td><td>Type of policy label invocation.&lt;br>Possible values = reqvserver, resvserver, policylabel</td><tr><tr><td>labelname</td><td>&lt;String></td><td>Read-only</td><td>Name of the label to invoke if the current policy rule evaluates to TRUE.</td><tr><tr><td>undefhits</td><td>&lt;Double></td><td>Read-only</td><td>Number of Undef hits.</td><tr><tr><td>description</td><td>&lt;String></td><td>Read-only</td><td>Description of the policy.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [DELETE](#delete) | [UPDATE](#update) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>},"sessionid":"##sessionid","dnspolicy64":{      "name":<String_value>,      "rule":<String_value>,      "action":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/dnspolicy64/name_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/dnspolicy64/name_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","dnspolicy64":{      "name":<String_value>,      "rule":<String_value>,      "action":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/dnspolicy64
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/dnspolicy64?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of dnspolicy64 resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/dnspolicy64?view=summary
Use this query-parameter to get the summary output of dnspolicy64 resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/dnspolicy64?pagesize=#no;pageno=#no
Use this query-parameter to get the dnspolicy64 resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/dnspolicy64?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "dnspolicy64": [ {      "name":<String_value>,      "rule":<String_value>,      "hits":<Double_value>,      "action":<String_value>,      "labeltype":<String_value>,      "labelname":<String_value>,      "undefhits":<Double_value>,      "description":<String_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/dnspolicy64/name_value&lt;String&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "dnspolicy64": [ {      "name":<String_value>,      "rule":<String_value>,      "hits":<Double_value>,      "action":<String_value>,      "labeltype":<String_value>,      "labelname":<String_value>,      "undefhits":<Double_value>,      "description":<String_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/dnspolicy64?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",dnspolicy64: [ { "__count": "#no"} ] }


