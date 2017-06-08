#feoaction

Configuration for Front end optimization action resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>The name of the front end optimization action.&lt;br>Minimum length = 1</td><tr><tr><td>pageextendcache</td><td>&lt;Boolean></td><td>Read-write</td><td>Extend the time period during which the browser can use the cached resource.</td><tr><tr><td>imgshrinktoattrib</td><td>&lt;Boolean></td><td>Read-write</td><td>Shrink image dimensions as per the height and width attributes specified in the ;lt;img;gt; tag.</td><tr><tr><td>imggiftopng</td><td>&lt;Boolean></td><td>Read-write</td><td>Convert GIF image formats to PNG formats.</td><tr><tr><td>imginline</td><td>&lt;Boolean></td><td>Read-write</td><td>Inline images whose size is less than 2KB.</td><tr><tr><td>cssimginline</td><td>&lt;Boolean></td><td>Read-write</td><td>Inline small images (less than 2KB) referred within CSS files as background-URLs.</td><tr><tr><td>jpgoptimize</td><td>&lt;Boolean></td><td>Read-write</td><td>Remove non-image data such as comments from JPEG images.</td><tr><tr><td>imglazyload</td><td>&lt;Boolean></td><td>Read-write</td><td>Download images, only when the user scrolls the page to view them.</td><tr><tr><td>cssminify</td><td>&lt;Boolean></td><td>Read-write</td><td>Remove comments and whitespaces from CSSs.</td><tr><tr><td>cssinline</td><td>&lt;Boolean></td><td>Read-write</td><td>Inline CSS files, whose size is less than 2KB, within the main page.</td><tr><tr><td>csscombine</td><td>&lt;Boolean></td><td>Read-write</td><td>Combine one or more CSS files into one file.</td><tr><tr><td>convertimporttolink</td><td>&lt;Boolean></td><td>Read-write</td><td>Convert CSS import statements to HTML link tags.</td><tr><tr><td>jsminify</td><td>&lt;Boolean></td><td>Read-write</td><td>Remove comments and whitespaces from JavaScript.</td><tr><tr><td>jsinline</td><td>&lt;Boolean></td><td>Read-write</td><td>Convert linked JavaScript files (less than 2KB) to inline JavaScript files.</td><tr><tr><td>htmlminify</td><td>&lt;Boolean></td><td>Read-write</td><td>Remove comments and whitespaces from an HTML page.</td><tr><tr><td>cssmovetohead</td><td>&lt;Boolean></td><td>Read-write</td><td>Move any CSS file present within the body tag of an HTML page to the head tag.</td><tr><tr><td>jsmovetoend</td><td>&lt;Boolean></td><td>Read-write</td><td>Move any JavaScript present in the body tag to the end of the body tag.</td><tr><tr><td>domainsharding</td><td>&lt;String></td><td>Read-write</td><td>Domain name of the server.</td><tr><tr><td>dnsshards</td><td>&lt;String[]></td><td>Read-write</td><td>Set of domain names that replaces the parent domain.</td><tr><tr><td>clientsidemeasurements</td><td>&lt;Boolean></td><td>Read-write</td><td>Collect the amount of time required for the client to load and render the web page.</td><tr><tr><td>imgadddimensions</td><td>&lt;Boolean></td><td>Read-only</td><td>Add dimension attributes to images, if not specified within the ;lt;img;gt; tag.</td><tr><tr><td>imgshrinkformobile</td><td>&lt;Boolean></td><td>Read-only</td><td>Serve smaller images for mobile users.</td><tr><tr><td>imgweaken</td><td>&lt;Boolean></td><td>Read-only</td><td>Reduce the image quality.</td><tr><tr><td>jpgprogressive</td><td>&lt;Boolean></td><td>Read-only</td><td>Convert JPEG image formats to progressive formats.</td><tr><tr><td>cssflattenimports</td><td>&lt;Boolean></td><td>Read-only</td><td>Replace CSS import statements with the file content.</td><tr><tr><td>jscombine</td><td>&lt;Boolean></td><td>Read-only</td><td>Combine one or more JavaScript files into one file.</td><tr><tr><td>htmlrmdefaultattribs</td><td>&lt;Boolean></td><td>Read-only</td><td>Remove default redundant attributes from an HTML file.</td><tr><tr><td>htmlrmattribquotes</td><td>&lt;Boolean></td><td>Read-only</td><td>Remove unnecessary quotes present within the HTML attributes.</td><tr><tr><td>htmltrimurls</td><td>&lt;Boolean></td><td>Read-only</td><td>Trim URLs.</td><tr><tr><td>hits</td><td>&lt;Double></td><td>Read-only</td><td>The number of times the action has been taken.</td><tr><tr><td>undefhits</td><td>&lt;Double></td><td>Read-only</td><td>Total number of undefined policy hits.</td><tr><tr><td>builtin</td><td>&lt;String[]></td><td>Read-only</td><td>Flag to determine if front end optimization action is built-in or not.&lt;br>Possible values = MODIFIABLE, DELETABLE, IMMUTABLE</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [UPDATE](#update) | [UNSET](#unset) | [DELETE](#delete) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>},"sessionid":"##sessionid","feoaction":{      "name":<String_value>,      "pageextendcache":<Boolean_value>,      "imgshrinktoattrib":<Boolean_value>,      "imggiftopng":<Boolean_value>,      "imginline":<Boolean_value>,      "cssimginline":<Boolean_value>,      "jpgoptimize":<Boolean_value>,      "imglazyload":<Boolean_value>,      "cssminify":<Boolean_value>,      "cssinline":<Boolean_value>,      "csscombine":<Boolean_value>,      "convertimporttolink":<Boolean_value>,      "jsminify":<Boolean_value>,      "jsinline":<Boolean_value>,      "htmlminify":<Boolean_value>,      "cssmovetohead":<Boolean_value>,      "jsmovetoend":<Boolean_value>,      "domainsharding":<String_value>,                  "dnsshards":<String[]_value>,      "clientsidemeasurements":<Boolean_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","feoaction":{      "name":<String_value>,      "pageextendcache":<Boolean_value>,      "imgshrinktoattrib":<Boolean_value>,      "imggiftopng":<Boolean_value>,      "imginline":<Boolean_value>,      "cssimginline":<Boolean_value>,      "jpgoptimize":<Boolean_value>,      "imglazyload":<Boolean_value>,      "cssminify":<Boolean_value>,      "cssinline":<Boolean_value>,      "csscombine":<Boolean_value>,      "convertimporttolink":<Boolean_value>,      "jsminify":<Boolean_value>,      "jsinline":<Boolean_value>,      "htmlminify":<Boolean_value>,      "cssmovetohead":<Boolean_value>,      "jsmovetoend":<Boolean_value>,      "domainsharding":<String_value>,                  "dnsshards":<String[]_value>,      "clientsidemeasurements":<Boolean_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","feoaction":{      "name":<String_value>,      "pageextendcache":true,      "imgshrinktoattrib":true,      "imggiftopng":true,      "imginline":true,      "cssimginline":true,      "jpgoptimize":true,      "imglazyload":true,      "cssminify":true,      "cssinline":true,      "csscombine":true,      "convertimporttolink":true,      "jsminify":true,      "jsinline":true,      "htmlminify":true,      "cssmovetohead":true,      "jsmovetoend":true,      "clientsidemeasurements":true,      "domainsharding":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/feoaction/name_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/feoaction/name_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/feoaction
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/feoaction?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of feoaction resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/feoaction?view=summary
Use this query-parameter to get the summary output of feoaction resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/feoaction?pagesize=#no;pageno=#no
Use this query-parameter to get the feoaction resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/feoaction?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "feoaction": [ {      "name":<String_value>,      "pageextendcache":<Boolean_value>,      "imgshrinktoattrib":<Boolean_value>,      "imggiftopng":<Boolean_value>,      "imgadddimensions":<Boolean_value>,      "imgshrinkformobile":<Boolean_value>,      "imgweaken":<Boolean_value>,      "imginline":<Boolean_value>,      "cssimginline":<Boolean_value>,      "jpgoptimize":<Boolean_value>,      "jpgprogressive":<Boolean_value>,      "imglazyload":<Boolean_value>,      "cssminify":<Boolean_value>,      "cssinline":<Boolean_value>,      "csscombine":<Boolean_value>,      "cssflattenimports":<Boolean_value>,      "convertimporttolink":<Boolean_value>,      "jsminify":<Boolean_value>,      "jsinline":<Boolean_value>,      "jscombine":<Boolean_value>,      "htmlminify":<Boolean_value>,      "htmlrmdefaultattribs":<Boolean_value>,      "htmlrmattribquotes":<Boolean_value>,      "htmltrimurls":<Boolean_value>,      "cssmovetohead":<Boolean_value>,      "jsmovetoend":<Boolean_value>,      "domainsharding":<String_value>,      "dnsshards":<String[]_value>,      "clientsidemeasurements":<Boolean_value>,      "hits":<Double_value>,      "undefhits":<Double_value>,      "builtin":<String[]_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/feoaction/name_value&lt;String&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "feoaction": [ {      "name":<String_value>,      "pageextendcache":<Boolean_value>,      "imgshrinktoattrib":<Boolean_value>,      "imggiftopng":<Boolean_value>,      "imgadddimensions":<Boolean_value>,      "imgshrinkformobile":<Boolean_value>,      "imgweaken":<Boolean_value>,      "imginline":<Boolean_value>,      "cssimginline":<Boolean_value>,      "jpgoptimize":<Boolean_value>,      "jpgprogressive":<Boolean_value>,      "imglazyload":<Boolean_value>,      "cssminify":<Boolean_value>,      "cssinline":<Boolean_value>,      "csscombine":<Boolean_value>,      "cssflattenimports":<Boolean_value>,      "convertimporttolink":<Boolean_value>,      "jsminify":<Boolean_value>,      "jsinline":<Boolean_value>,      "jscombine":<Boolean_value>,      "htmlminify":<Boolean_value>,      "htmlrmdefaultattribs":<Boolean_value>,      "htmlrmattribquotes":<Boolean_value>,      "htmltrimurls":<Boolean_value>,      "cssmovetohead":<Boolean_value>,      "jsmovetoend":<Boolean_value>,      "domainsharding":<String_value>,      "dnsshards":<String[]_value>,      "clientsidemeasurements":<Boolean_value>,      "hits":<Double_value>,      "undefhits":<Double_value>,      "builtin":<String[]_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/feoaction?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",feoaction: [ { "__count": "#no"} ] }


