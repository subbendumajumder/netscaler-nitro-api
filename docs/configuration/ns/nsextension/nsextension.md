#nsextension

Configuration for Extension resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>src</td><td>&lt;String></td><td>Read-write</td><td>Local path to and name of, or URL (protocol, host, path, and file name) for, the file in which to store the imported extension.<br>NOTE: The import fails if the object to be imported is on an HTTPS server that requires client certificate authentication for access.<br>Minimum length = 1<br>Maximum length = 2047</td></tr><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name to assign to the extension object on the NetScaler appliance.<br>Minimum length = 1<br>Maximum length = 31</td></tr><tr><td>comment</td><td>&lt;String></td><td>Read-write</td><td>Any comments to preserve information about the extension object.<br>Maximum length = 128</td></tr><tr><td>overwrite</td><td>&lt;Boolean></td><td>Read-write</td><td>Overwrites the existing file.</td></tr><tr><td>trace</td><td>&lt;String></td><td>Read-write</td><td>Enables tracing to the NS log file of extension execution:<br>off - turns off tracing (equivalent to unset ns extension &lt;extension-name&gt; -trace)<br>calls - traces extension function calls with arguments and function returns with the first return value<br>lines - traces the above plus line numbers for executed extension lines<br>all - traces the above plus local variables changed by executed extension lines<br>Note that the DEBUG log level must be enabled to see extension tracing.<br>This can be done by set audit syslogParams -loglevel ALL or -loglevel DEBUG.<br>Default value: off<br>Possible values = off, calls, lines, all</td></tr><tr><td>tracefunctions</td><td>&lt;String></td><td>Read-write</td><td>Comma-separated list of extension functions to trace. By default, all extension functions are traced.<br>Maximum length = 256</td></tr><tr><td>tracevariables</td><td>&lt;String></td><td>Read-write</td><td>Comma-separated list of variables (in traced extension functions) to trace. By default, all variables are traced.<br>Maximum length = 256</td></tr><tr><td>detail</td><td>&lt;String></td><td>Read-write</td><td>Show detail for extension function.<br>Possible values = brief, all</td></tr><tr><td>type</td><td>&lt;String></td><td>Read-only</td><td>.<br>Possible values = WSDL, CustomSettings, XMLSchema, XMLErrorPage, htmlpage, CustomResp, Extension</td></tr><tr><td>functionhits</td><td>&lt;Double></td><td>Read-only</td><td>Number of time function evaluates successfully.</td></tr><tr><td>functionundefhits</td><td>&lt;Double></td><td>Read-only</td><td>Number of times error occured in evaluating extension function.</td></tr><tr><td>functionhaltcount</td><td>&lt;Double></td><td>Read-only</td><td>Number of time function evaluation is halted.</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[IMPORT](#i)| [DELETE](#d)| [ADD]()| [CHANGE](#c)| [UPDATE](#u)| [UNSET](#)| [GET (ALL)](#get-)| [GET]()| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###Import



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsextension?<b>action=Import</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"nsextension":{<b>"src":<String_value>,</b><b>"name":<String_value>,</b>"comment":<String_value>,"overwrite":<Boolean_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsextension/name_value&lt;String&gt;
<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###add



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsextension
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"nsextension":{<b>"name":<String_value>,</b>"comment":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###change



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsextension?<b>action=update</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"nsextension":{<b>"name":<String_value></b>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsextension
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"nsextension":{<b>"name":<String_value>,</b>"trace":<String_value>,"tracefunctions":<String_value>,"tracevariables":<String_value>,"comment":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsextension?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"nsextension":{<b>"name":<String_value>,</b>"trace":true,"tracefunctions":true,"tracevariables":true,"comment":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsextension
<b>Query-parameters:</b>
<b>args</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsextension?<b>args=name:&lt;String_value&gt;,detail:&lt;String_value&gt;</b>
Use this query-parameter to get nsextension resources based on additional properties.


<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsextension?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsextension?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of nsextension resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsextension?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsextension?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the nsextension resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "nsextension": [ {name:<String_value>,detail:<String_value>"src":<String_value>,"type":<String_value>,"comment":<String_value>,"functionhits":<Double_value>,"functionundefhits":<Double_value>,"functionhaltcount":<Double_value>,"trace":<String_value>,"tracefunctions":<String_value>,"tracevariables":<String_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsextension/name_value&lt;String&gt;
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsextension/name_value&lt;String&gt;?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsextension/name_value&lt;String&gt;?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "nsextension": [ {name:<String_value>,detail:<String_value>"src":<String_value>,"type":<String_value>,"comment":<String_value>,"functionhits":<Double_value>,"functionundefhits":<Double_value>,"functionhaltcount":<Double_value>,"trace":<String_value>,"tracefunctions":<String_value>,"tracevariables":<String_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsextension?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "nsextension": [ { "__count": "#no"} ] }```



