#nsextension

Configuration for Extension resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>src</td><td>&lt;String></td><td>Read-write</td><td>Local path to and name of, or URL (protocol, host, path, and file name) for, the file in which to store the imported extension. NOTE: The import fails if the object to be imported is on an HTTPS server that requires client certificate authentication for access.&lt;br>Minimum length = 1&lt;br>Maximum length = 2047</td><tr><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name to assign to the extension object on the NetScaler appliance.&lt;br>Minimum length = 1&lt;br>Maximum length = 31</td><tr><tr><td>comment</td><td>&lt;String></td><td>Read-write</td><td>Any comments to preserve information about the extension object.&lt;br>Maximum length = 128</td><tr><tr><td>overwrite</td><td>&lt;Boolean></td><td>Read-write</td><td>Overwrites the existing file.</td><tr><tr><td>trace</td><td>&lt;String></td><td>Read-write</td><td>Enables tracing to the NS log file of extension execution: off - turns off tracing (equivalent to unset ns extension ;lt;extension-name;gt; -trace) calls - traces extension function calls with arguments and function returns with the first return value lines - traces the above plus line numbers for executed extension lines all - traces the above plus local variables changed by executed extension lines Note that the DEBUG log level must be enabled to see extension tracing. This can be done by set audit syslogParams -loglevel ALL or -loglevel DEBUG.&lt;br>Default value: off&lt;br>Possible values = off, calls, lines, all</td><tr><tr><td>tracefunctions</td><td>&lt;String></td><td>Read-write</td><td>Comma-separated list of extension functions to trace. By default, all extension functions are traced.&lt;br>Maximum length = 256</td><tr><tr><td>tracevariables</td><td>&lt;String></td><td>Read-write</td><td>Comma-separated list of variables (in traced extension functions) to trace. By default, all variables are traced.&lt;br>Maximum length = 256</td><tr><tr><td>detail</td><td>&lt;String></td><td>Read-write</td><td>Show detail for extension function.&lt;br>Possible values = brief, all</td><tr><tr><td>type</td><td>&lt;String></td><td>Read-only</td><td>.&lt;br>Possible values = WSDL, CustomSettings, XMLSchema, XMLErrorPage, htmlpage, CustomResp, Extension</td><tr><tr><td>functionhits</td><td>&lt;Double></td><td>Read-only</td><td>Number of time function evaluates successfully.</td><tr><tr><td>functionundefhits</td><td>&lt;Double></td><td>Read-only</td><td>Number of times error occured in evaluating extension function.</td><tr><tr><td>functionhaltcount</td><td>&lt;Double></td><td>Read-only</td><td>Number of time function evaluation is halted.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[IMPORT](#import) | [DELETE](#delete) | [ADD](#add) | [CHANGE](#change) | [UPDATE](#update) | [UNSET](#unset) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###Import



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"Import"},"sessionid":"##sessionid","nsextension":{      "src":<String_value>,      "name":<String_value>,      "comment":<String_value>,      "overwrite":<Boolean_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/nsextension/name_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/nsextension/name_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###add



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>},"sessionid":"##sessionid","nsextension":{      "name":<String_value>,      "comment":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###change



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"update"},"sessionid":"##sessionid","nsextension":{      "name":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","nsextension":{      "name":<String_value>,      "trace":<String_value>,      "tracefunctions":<String_value>,      "tracevariables":<String_value>,      "comment":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","nsextension":{      "name":<String_value>,      "trace":true,      "tracefunctions":true,      "tracevariables":true,      "comment":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/nsextension
Query-parameters:
args
http://&lt;NSIP&gt;/nitro/v1/config/nsextension?args=      "name":&lt;String_value&gt;,      "detail":&lt;String_value&gt;,
Use this query-parameter to get nsextension resources based on additional properties.


filter
http://&lt;NSIP&gt;/nitro/v1/config/nsextension?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of nsextension resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/nsextension?view=summary
Use this query-parameter to get the summary output of nsextension resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/nsextension?pagesize=#no;pageno=#no
Use this query-parameter to get the nsextension resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/nsextension?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "nsextension": [ {      "name":<String_value>,      "detail":<String_value>,      "src":<String_value>,      "type":<String_value>,      "comment":<String_value>,      "functionhits":<Double_value>,      "functionundefhits":<Double_value>,      "functionhaltcount":<Double_value>,      "trace":<String_value>,      "tracefunctions":<String_value>,      "tracevariables":<String_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/nsextension/name_value&lt;String&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "nsextension": [ {      "name":<String_value>,      "detail":<String_value>,      "src":<String_value>,      "type":<String_value>,      "comment":<String_value>,      "functionhits":<Double_value>,      "functionundefhits":<Double_value>,      "functionhaltcount":<Double_value>,      "trace":<String_value>,      "tracefunctions":<String_value>,      "tracevariables":<String_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/nsextension?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",nsextension: [ { "__count": "#no"} ] }


