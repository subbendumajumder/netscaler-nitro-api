#sslfipssimtarget

Configuration for FIPS SIM Target resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>keyvector</td><td>&lt;String></td><td>Read-write</td><td>Name of and, optionally, path to the target FIPS appliance's key vector. /nsconfig/ssl/ is the default path.<br>Minimum length = 1</td></tr><tr><td>sourcesecret</td><td>&lt;String></td><td>Read-write</td><td>Name of and, optionally, path to the source FIPS appliance's secret data. /nsconfig/ssl/ is the default path.<br>Minimum length = 1</td></tr><tr><td>certfile</td><td>&lt;String></td><td>Read-write</td><td>Name of and, optionally, path to the source FIPS appliance's certificate file. /nsconfig/ssl/ is the default path.<br>Minimum length = 1</td></tr><tr><td>targetsecret</td><td>&lt;String></td><td>Read-write</td><td>Name for and, optionally, path to the target FIPS appliance's secret data. The default input path for the secret data is /nsconfig/ssl/.<br>Minimum length = 1</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ENABLE](#e)| [INIT]()


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###enable



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslfipssimtarget?<b>action=enable</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"sslfipssimtarget":{<b>"keyvector":<String_value>,</b><b>"sourcesecret":<String_value></b>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###init



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslfipssimtarget?<b>action=init</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"sslfipssimtarget":{<b>"certfile":<String_value>,</b><b>"keyvector":<String_value>,</b><b>"targetsecret":<String_value></b>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


