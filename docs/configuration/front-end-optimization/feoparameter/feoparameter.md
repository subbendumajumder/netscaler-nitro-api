#feoparameter

Configuration for FEO parameter resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>jpegqualitypercent</td><td>&lt;Double></td><td>Read-write</td><td>The percentage value of a JPEG image quality to be reduced. Range: 0 - 100.<br>Default value: 75<br>Minimum value = 0<br>Maximum value = 100</td></tr><tr><td>cssinlinethressize</td><td>&lt;Double></td><td>Read-write</td><td>Threshold value of the file size (in bytes) for converting external CSS files to inline CSS files.<br>Default value: 1024<br>Minimum value = 1<br>Maximum value = 2048</td></tr><tr><td>jsinlinethressize</td><td>&lt;Double></td><td>Read-write</td><td>Threshold value of the file size (in bytes), for converting external JavaScript files to inline JavaScript files.<br>Default value: 1024<br>Minimum value = 1<br>Maximum value = 2048</td></tr><tr><td>imginlinethressize</td><td>&lt;Double></td><td>Read-write</td><td>Maximum file size of an image (in bytes), for coverting linked images to inline images.<br>Default value: 1024<br>Minimum value = 1<br>Maximum value = 2048</td></tr><tr><td>builtin</td><td>&lt;String[]></td><td>Read-only</td><td>Specify the builtin flags for - set feo param.<br>Possible values = MODIFIABLE, DELETABLE, IMMUTABLE, PARTITION_ALL</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[UPDATE](#u)| [UNSET](#)| [GET (ALL)](#get-)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/feoparameter
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"feoparameter":{"jpegqualitypercent":<Double_value>,"cssinlinethressize":<Double_value>,"jsinlinethressize":<Double_value>,"imginlinethressize":<Double_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/feoparameter?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"feoparameter":{"jpegqualitypercent":true,"cssinlinethressize":true,"jsinlinethressize":true,"imginlinethressize":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/feoparameter
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "feoparameter": [ {"jpegqualitypercent":<Double_value>,"cssinlinethressize":<Double_value>,"jsinlinethressize":<Double_value>,"imginlinethressize":<Double_value>,"builtin":<String[]_value>}]}```



