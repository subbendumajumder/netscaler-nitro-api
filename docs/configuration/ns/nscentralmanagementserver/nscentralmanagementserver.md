#nscentralmanagementserver

Configuration for centralmanagementserver resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>type</td><td>&lt;String></td><td>Read-write</td><td>Type of the central management server. Must be either CLOUD or ONPREM depending on whether the server is on the cloud or on premise.<br>Possible values = CLOUD, ONPREM</td></tr><tr><td>username</td><td>&lt;String></td><td>Read-write</td><td>Username for access to central management server. Must begin with a letter, number, or the underscore character (_), and must contain only letters, numbers, and the hyphen (-), period (.) pound (#), space ( ), at (@), equals (=), colon (:), and underscore characters.<br><br>The following requirement applies only to the NetScaler CLI:<br>If the name includes one or more spaces, enclose the name in double or<br>single quotation marks (for example, "my ns centralmgmtserver" or "my ns centralmgmtserver").<br>Minimum length = 1<br>Maximum length = 127</td></tr><tr><td>password</td><td>&lt;String></td><td>Read-write</td><td>Password for access to central management server. Required for any user account.<br>Minimum length = 1<br>Maximum length = 127</td></tr><tr><td>ipaddress</td><td>&lt;String></td><td>Read-write</td><td>Ip Address of central management server.<br>Minimum length = 1</td></tr><tr><td>servername</td><td>&lt;String></td><td>Read-write</td><td>Fully qualified domain name of the central management server.</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD]()| [DELETE](#d)| [GET (ALL)](#get-)| [GET]()| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nscentralmanagementserver
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"nscentralmanagementserver":{<b>"type":<String_value>,</b><b>"username":<String_value>,</b><b>"password":<String_value>,</b>"ipaddress":<String_value>,"servername":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nscentralmanagementserver/type_value&lt;String&gt;
<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nscentralmanagementserver
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nscentralmanagementserver?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nscentralmanagementserver?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of nscentralmanagementserver resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nscentralmanagementserver?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nscentralmanagementserver?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the nscentralmanagementserver resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "nscentralmanagementserver": [ {"type":<String_value>,"username":<String_value>,"ipaddress":<String_value>,"servername":<String_value>,"password":<String_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nscentralmanagementserver/type_value&lt;String&gt;
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nscentralmanagementserver/type_value&lt;String&gt;?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nscentralmanagementserver/type_value&lt;String&gt;?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "nscentralmanagementserver": [ {"type":<String_value>,"username":<String_value>,"ipaddress":<String_value>,"servername":<String_value>,"password":<String_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nscentralmanagementserver?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "nscentralmanagementserver": [ { "__count": "#no"} ] }```



