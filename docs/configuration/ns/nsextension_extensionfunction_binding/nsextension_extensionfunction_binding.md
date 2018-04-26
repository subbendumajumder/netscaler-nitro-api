#nsextension_extensionfunction_binding

Binding object showing the extensionfunction that can be bound to nsextension.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name of the extension object.<br>Minimum length = 1<br>Maximum length = 31</td></tr><tr><td>extensionfunctionlinenumber</td><td>&lt;Double></td><td>Read-only</td><td>Line number of the function in file.</td></tr><tr><td>extensionfunctionclasses</td><td>&lt;String[]></td><td>Read-only</td><td>List of classes (including inherited) that the function is present in.</td></tr><tr><td>extensionfunctionargtype</td><td>&lt;String[]></td><td>Read-only</td><td>List of extension function's arguments types.</td></tr><tr><td>activeextensionfunction</td><td>&lt;Integer></td><td>Read-only</td><td>Extension function is in use or not.</td></tr><tr><td>extensionfunctionname</td><td>&lt;String></td><td>Read-only</td><td>Name of extension function given in the extension.<br>Minimum length = 1<br>Maximum length = 31</td></tr><tr><td>extensionfunctionclasstype</td><td>&lt;String></td><td>Read-only</td><td>Extension function class type.<br>Minimum length = 1<br>Maximum length = 31</td></tr><tr><td>extensionfuncdescription</td><td>&lt;String></td><td>Read-only</td><td>Any description to preserve information about the extension function.<br>Maximum length = 1023</td></tr><tr><td>extensionfunctionallparams</td><td>&lt;String[]></td><td>Read-only</td><td>List of parameters (including promotions) that the function can accept.</td></tr><tr><td>extensionfunctionargcount</td><td>&lt;Double></td><td>Read-only</td><td>Number of parameters in the extension function.</td></tr><tr><td>extensionfunctionreturntype</td><td>&lt;String></td><td>Read-only</td><td>Extension function return type.<br>Minimum length = 1<br>Maximum length = 31</td></tr><tr><td>extensionfunctionclassescount</td><td>&lt;Double></td><td>Read-only</td><td>Number of classes the function is present in.</td></tr><tr><td>extensionfunctionallparamscount</td><td>&lt;Double></td><td>Read-only</td><td>Number of parameters (including promotions) that the function can accept.</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[GET]()| [GET (ALL)](#get-)| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsextension_extensionfunction_binding/name_value&lt;String&gt;
<b>Query-parameters:</b>
<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsextension_extensionfunction_binding/name_value&lt;String&gt;?<b>filter=property-name1:property-value1,property-name2:property-value2</b>
Use this query-parameter to get the filtered set of nsextension_extensionfunction_binding resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsextension_extensionfunction_binding/name_value&lt;String&gt;?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the nsextension_extensionfunction_binding resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "nsextension_extensionfunction_binding": [ {"name":<String_value>,"extensionfunctionlinenumber":<Double_value>,"extensionfunctionclasses":<String[]_value>,"extensionfunctionargtype":<String[]_value>,"activeextensionfunction":<Integer_value>,"extensionfunctionname":<String_value>,"extensionfunctionclasstype":<String_value>,"extensionfuncdescription":<String_value>,"extensionfunctionallparams":<String[]_value>,"extensionfunctionargcount":<Double_value>,"extensionfunctionreturntype":<String_value>,"extensionfunctionclassescount":<Double_value>,"extensionfunctionallparamscount":<Double_value>}]}```



###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsextension_extensionfunction_binding
<b>Query-parameters:</b>
<b>bulkbindings</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsextension_extensionfunction_binding?<b>bulkbindings=yes</b>
NITRO allows you to fetch bindings in bulk.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "nsextension_extensionfunction_binding": [ {"name":<String_value>,"extensionfunctionlinenumber":<Double_value>,"extensionfunctionclasses":<String[]_value>,"extensionfunctionargtype":<String[]_value>,"activeextensionfunction":<Integer_value>,"extensionfunctionname":<String_value>,"extensionfunctionclasstype":<String_value>,"extensionfuncdescription":<String_value>,"extensionfunctionallparams":<String[]_value>,"extensionfunctionargcount":<Double_value>,"extensionfunctionreturntype":<String_value>,"extensionfunctionclassescount":<Double_value>,"extensionfunctionallparamscount":<Double_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsextension_extensionfunction_binding/name_value&lt;String&gt;?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{"nsextension_extensionfunction_binding": [ { "__count": "#no"} ] }```



