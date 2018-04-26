#nsaptlicense

Configuration for aptlicense resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>serialno</td><td>&lt;String></td><td>Read-write</td><td>Hardware Serial Number/License Activation Code(LAC).</td></tr><tr><td>useproxy</td><td>&lt;String></td><td>Read-write</td><td>Specifies whether to use the licenseproxyserver to reach the internet. Make sure to configure licenseproxyserver to use this option.<br>Default value: NO<br>Possible values = YES, NO</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>License ID.</td></tr><tr><td>sessionid</td><td>&lt;String></td><td>Read-write</td><td>Session ID.</td></tr><tr><td>bindtype</td><td>&lt;String></td><td>Read-write</td><td>Bind type.</td></tr><tr><td>countavailable</td><td>&lt;String></td><td>Read-write</td><td>The user can allocate one or more licenses. Ensure the value is less than (for partial allocation) or equal to the total number of available licenses.</td></tr><tr><td>licensedir</td><td>&lt;String></td><td>Read-write</td><td>License Directory.</td></tr><tr><td>response</td><td>&lt;String></td><td>Read-only</td><td>Response data as text blob.</td></tr><tr><td>counttotal</td><td>&lt;String></td><td>Read-only</td><td>Count.</td></tr><tr><td>name</td><td>&lt;String></td><td>Read-only</td><td>License name.</td></tr><tr><td>relevance</td><td>&lt;String></td><td>Read-only</td><td>License relevance.</td></tr><tr><td>datepurchased</td><td>&lt;String></td><td>Read-only</td><td>License purchase date.</td></tr><tr><td>datesa</td><td>&lt;String></td><td>Read-only</td><td>License SA date.</td></tr><tr><td>dateexp</td><td>&lt;String></td><td>Read-only</td><td>License expiry date.</td></tr><tr><td>features</td><td>&lt;String[]></td><td>Read-only</td><td>Features.</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[CHANGE](#c)| [GET (ALL)](#get-)| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###change



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsaptlicense?<b>action=update</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"nsaptlicense":{<b>"id":<String_value>,</b><b>"sessionid":<String_value>,</b><b>"bindtype":<String_value>,</b><b>"countavailable":<String_value>,</b>"licensedir":<String_value>,"useproxy":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsaptlicense
<b>Query-parameters:</b>
<b>args</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsaptlicense?<b>args=<b>serialno:&lt;String_value&gt;,</b>useproxy:&lt;String_value&gt;</b>
Use this query-parameter to get nsaptlicense resources based on additional properties.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "nsaptlicense": [ {<b>serialno:<String_value>,</b>useproxy:<String_value>"response":<String_value>,"id":<String_value>,"sessionid":<String_value>,"bindtype":<String_value>,"countavailable":<String_value>,"counttotal":<String_value>,"name":<String_value>,"relevance":<String_value>,"datepurchased":<String_value>,"datesa":<String_value>,"dateexp":<String_value>,"features":<String[]_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsaptlicense?<b>args=<b>serialno:&lt;String_value&gt;,</b>useproxy:&lt;String_value&gt;;count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "nsaptlicense": [ { "__count": "#no"} ] }```



