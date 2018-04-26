#feoaction

Configuration for Front end optimization action resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>The name of the front end optimization action.<br>Minimum length = 1</td></tr><tr><td>pageextendcache</td><td>&lt;Boolean></td><td>Read-write</td><td>Extend the time period during which the browser can use the cached resource.</td></tr><tr><td>cachemaxage</td><td>&lt;Double></td><td>Read-write</td><td>Maxage for cache extension.<br>Default value: 30<br>Minimum value = 0<br>Maximum value = 360</td></tr><tr><td>imgshrinktoattrib</td><td>&lt;Boolean></td><td>Read-write</td><td>Shrink image dimensions as per the height and width attributes specified in the &lt;img&gt; tag.</td></tr><tr><td>imggiftopng</td><td>&lt;Boolean></td><td>Read-write</td><td>Convert GIF image formats to PNG formats.</td></tr><tr><td>imgtowebp</td><td>&lt;Boolean></td><td>Read-write</td><td>Convert JPEG, GIF, PNG image formats to WEBP format.</td></tr><tr><td>imgtojpegxr</td><td>&lt;Boolean></td><td>Read-write</td><td>Convert JPEG, GIF, PNG image formats to JXR format.</td></tr><tr><td>imginline</td><td>&lt;Boolean></td><td>Read-write</td><td>Inline images whose size is less than 2KB.</td></tr><tr><td>cssimginline</td><td>&lt;Boolean></td><td>Read-write</td><td>Inline small images (less than 2KB) referred within CSS files as background-URLs.</td></tr><tr><td>jpgoptimize</td><td>&lt;Boolean></td><td>Read-write</td><td>Remove non-image data such as comments from JPEG images.</td></tr><tr><td>imglazyload</td><td>&lt;Boolean></td><td>Read-write</td><td>Download images, only when the user scrolls the page to view them.</td></tr><tr><td>cssminify</td><td>&lt;Boolean></td><td>Read-write</td><td>Remove comments and whitespaces from CSSs.</td></tr><tr><td>cssinline</td><td>&lt;Boolean></td><td>Read-write</td><td>Inline CSS files, whose size is less than 2KB, within the main page.</td></tr><tr><td>csscombine</td><td>&lt;Boolean></td><td>Read-write</td><td>Combine one or more CSS files into one file.</td></tr><tr><td>convertimporttolink</td><td>&lt;Boolean></td><td>Read-write</td><td>Convert CSS import statements to HTML link tags.</td></tr><tr><td>jsminify</td><td>&lt;Boolean></td><td>Read-write</td><td>Remove comments and whitespaces from JavaScript.</td></tr><tr><td>jsinline</td><td>&lt;Boolean></td><td>Read-write</td><td>Convert linked JavaScript files (less than 2KB) to inline JavaScript files.</td></tr><tr><td>htmlminify</td><td>&lt;Boolean></td><td>Read-write</td><td>Remove comments and whitespaces from an HTML page.</td></tr><tr><td>cssmovetohead</td><td>&lt;Boolean></td><td>Read-write</td><td>Move any CSS file present within the body tag of an HTML page to the head tag.</td></tr><tr><td>jsmovetoend</td><td>&lt;Boolean></td><td>Read-write</td><td>Move any JavaScript present in the body tag to the end of the body tag.</td></tr><tr><td>domainsharding</td><td>&lt;String></td><td>Read-write</td><td>Domain name of the server.</td></tr><tr><td>dnsshards</td><td>&lt;String[]></td><td>Read-write</td><td>Set of domain names that replaces the parent domain.</td></tr><tr><td>clientsidemeasurements</td><td>&lt;Boolean></td><td>Read-write</td><td>Send AppFlow records about the web pages optimized by this action. The records provide FEO statistics, such as the number of HTTP requests that have been reduced for this page. You must enable the Appflow feature before enabling this parameter.</td></tr><tr><td>imgadddimensions</td><td>&lt;Boolean></td><td>Read-only</td><td>Add dimension attributes to images, if not specified within the &lt;img&gt; tag.</td></tr><tr><td>imgshrinkformobile</td><td>&lt;Boolean></td><td>Read-only</td><td>Serve smaller images for mobile users.</td></tr><tr><td>imgweaken</td><td>&lt;Boolean></td><td>Read-only</td><td>Reduce the image quality.</td></tr><tr><td>jpgprogressive</td><td>&lt;Boolean></td><td>Read-only</td><td>Convert JPEG image formats to progressive formats.</td></tr><tr><td>cssflattenimports</td><td>&lt;Boolean></td><td>Read-only</td><td>Replace CSS import statements with the file content.</td></tr><tr><td>jscombine</td><td>&lt;Boolean></td><td>Read-only</td><td>Combine one or more JavaScript files into one file.</td></tr><tr><td>htmlrmdefaultattribs</td><td>&lt;Boolean></td><td>Read-only</td><td>Remove default redundant attributes from an HTML file.</td></tr><tr><td>htmlrmattribquotes</td><td>&lt;Boolean></td><td>Read-only</td><td>Remove unnecessary quotes present within the HTML attributes.</td></tr><tr><td>htmltrimurls</td><td>&lt;Boolean></td><td>Read-only</td><td>Trim URLs.</td></tr><tr><td>hits</td><td>&lt;Double></td><td>Read-only</td><td>The number of times the action has been taken.</td></tr><tr><td>undefhits</td><td>&lt;Double></td><td>Read-only</td><td>Total number of undefined policy hits.</td></tr><tr><td>builtin</td><td>&lt;String[]></td><td>Read-only</td><td>Flag to determine if front end optimization action is built-in or not.<br>Possible values = MODIFIABLE, DELETABLE, IMMUTABLE, PARTITION_ALL</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD]()| [UPDATE](#u)| [UNSET](#)| [DELETE](#d)| [GET (ALL)](#get-)| [GET]()| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/feoaction
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"feoaction":{<b>"name":<String_value>,</b>"pageextendcache":<Boolean_value>,"cachemaxage":<Double_value>,"imgshrinktoattrib":<Boolean_value>,"imggiftopng":<Boolean_value>,"imgtowebp":<Boolean_value>,"imgtojpegxr":<Boolean_value>,"imginline":<Boolean_value>,"cssimginline":<Boolean_value>,"jpgoptimize":<Boolean_value>,"imglazyload":<Boolean_value>,"cssminify":<Boolean_value>,"cssinline":<Boolean_value>,"csscombine":<Boolean_value>,"convertimporttolink":<Boolean_value>,"jsminify":<Boolean_value>,"jsinline":<Boolean_value>,"htmlminify":<Boolean_value>,"cssmovetohead":<Boolean_value>,"jsmovetoend":<Boolean_value>,"domainsharding":<String_value>,"dnsshards":<String[]_value>,"clientsidemeasurements":<Boolean_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/feoaction
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"feoaction":{<b>"name":<String_value>,</b>"pageextendcache":<Boolean_value>,"cachemaxage":<Double_value>,"imgshrinktoattrib":<Boolean_value>,"imggiftopng":<Boolean_value>,"imgtowebp":<Boolean_value>,"imgtojpegxr":<Boolean_value>,"imginline":<Boolean_value>,"cssimginline":<Boolean_value>,"jpgoptimize":<Boolean_value>,"imglazyload":<Boolean_value>,"cssminify":<Boolean_value>,"cssinline":<Boolean_value>,"csscombine":<Boolean_value>,"convertimporttolink":<Boolean_value>,"jsminify":<Boolean_value>,"jsinline":<Boolean_value>,"htmlminify":<Boolean_value>,"cssmovetohead":<Boolean_value>,"jsmovetoend":<Boolean_value>,"domainsharding":<String_value>,"dnsshards":<String[]_value>,"clientsidemeasurements":<Boolean_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/feoaction?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"feoaction":{<b>"name":<String_value>,</b>"pageextendcache":true,"imgshrinktoattrib":true,"imggiftopng":true,"imgtowebp":true,"imgtojpegxr":true,"imginline":true,"cssimginline":true,"jpgoptimize":true,"imglazyload":true,"cssminify":true,"cssinline":true,"csscombine":true,"convertimporttolink":true,"jsminify":true,"jsinline":true,"htmlminify":true,"cssmovetohead":true,"jsmovetoend":true,"clientsidemeasurements":true,"domainsharding":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/feoaction/name_value&lt;String&gt;
<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/feoaction
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/feoaction?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/feoaction?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of feoaction resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/feoaction?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/feoaction?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the feoaction resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "feoaction": [ {"name":<String_value>,"pageextendcache":<Boolean_value>,"cachemaxage":<Double_value>,"imgshrinktoattrib":<Boolean_value>,"imggiftopng":<Boolean_value>,"imgtowebp":<Boolean_value>,"imgtojpegxr":<Boolean_value>,"imgadddimensions":<Boolean_value>,"imgshrinkformobile":<Boolean_value>,"imgweaken":<Boolean_value>,"imginline":<Boolean_value>,"cssimginline":<Boolean_value>,"jpgoptimize":<Boolean_value>,"jpgprogressive":<Boolean_value>,"imglazyload":<Boolean_value>,"cssminify":<Boolean_value>,"cssinline":<Boolean_value>,"csscombine":<Boolean_value>,"cssflattenimports":<Boolean_value>,"convertimporttolink":<Boolean_value>,"jsminify":<Boolean_value>,"jsinline":<Boolean_value>,"jscombine":<Boolean_value>,"htmlminify":<Boolean_value>,"htmlrmdefaultattribs":<Boolean_value>,"htmlrmattribquotes":<Boolean_value>,"htmltrimurls":<Boolean_value>,"cssmovetohead":<Boolean_value>,"jsmovetoend":<Boolean_value>,"domainsharding":<String_value>,"dnsshards":<String[]_value>,"clientsidemeasurements":<Boolean_value>,"hits":<Double_value>,"undefhits":<Double_value>,"builtin":<String[]_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/feoaction/name_value&lt;String&gt;
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/feoaction/name_value&lt;String&gt;?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/feoaction/name_value&lt;String&gt;?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "feoaction": [ {"name":<String_value>,"pageextendcache":<Boolean_value>,"cachemaxage":<Double_value>,"imgshrinktoattrib":<Boolean_value>,"imggiftopng":<Boolean_value>,"imgtowebp":<Boolean_value>,"imgtojpegxr":<Boolean_value>,"imgadddimensions":<Boolean_value>,"imgshrinkformobile":<Boolean_value>,"imgweaken":<Boolean_value>,"imginline":<Boolean_value>,"cssimginline":<Boolean_value>,"jpgoptimize":<Boolean_value>,"jpgprogressive":<Boolean_value>,"imglazyload":<Boolean_value>,"cssminify":<Boolean_value>,"cssinline":<Boolean_value>,"csscombine":<Boolean_value>,"cssflattenimports":<Boolean_value>,"convertimporttolink":<Boolean_value>,"jsminify":<Boolean_value>,"jsinline":<Boolean_value>,"jscombine":<Boolean_value>,"htmlminify":<Boolean_value>,"htmlrmdefaultattribs":<Boolean_value>,"htmlrmattribquotes":<Boolean_value>,"htmltrimurls":<Boolean_value>,"cssmovetohead":<Boolean_value>,"jsmovetoend":<Boolean_value>,"domainsharding":<String_value>,"dnsshards":<String[]_value>,"clientsidemeasurements":<Boolean_value>,"hits":<Double_value>,"undefhits":<Double_value>,"builtin":<String[]_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/feoaction?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "feoaction": [ { "__count": "#no"} ] }```



