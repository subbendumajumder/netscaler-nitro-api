#nsappflowparam

Configuration for appflowParam resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>templaterefresh</td><td>&lt;Double></td><td>Read-write</td><td>IPFIX template refresh interval (in seconds).<br>Default value: 600<br>Minimum value = 60<br>Maximum value = 3600</td></tr><tr><td>udppmtu</td><td>&lt;Double></td><td>Read-write</td><td>MTU to be used for IPFIX UDP packets.<br>Default value: 1472<br>Minimum value = 128<br>Maximum value = 1472</td></tr><tr><td>httpurl</td><td>&lt;String></td><td>Read-write</td><td>Enable AppFlow HTTP URL logging.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>httpcookie</td><td>&lt;String></td><td>Read-write</td><td>Enable AppFlow HTTP cookie logging.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>httpreferer</td><td>&lt;String></td><td>Read-write</td><td>Enable AppFlow HTTP referer logging.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>httpmethod</td><td>&lt;String></td><td>Read-write</td><td>Enable AppFlow HTTP method logging.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>httphost</td><td>&lt;String></td><td>Read-write</td><td>Enable AppFlow HTTP host logging.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>httpuseragent</td><td>&lt;String></td><td>Read-write</td><td>Enable AppFlow HTTP user-agent logging.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>clienttrafficonly</td><td>&lt;String></td><td>Read-write</td><td>Control whether AppFlow records should be generated only for client-side traffic.<br>Default value: NO<br>Possible values = YES, NO</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[UPDATE](#u)| [UNSET](#)| [GET (ALL)](#get-)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsappflowparam
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"nsappflowparam":{"templaterefresh":<Double_value>,"udppmtu":<Double_value>,"httpurl":<String_value>,"httpcookie":<String_value>,"httpreferer":<String_value>,"httpmethod":<String_value>,"httphost":<String_value>,"httpuseragent":<String_value>,"clienttrafficonly":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsappflowparam?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"nsappflowparam":{"templaterefresh":true,"udppmtu":true,"httpurl":true,"httpcookie":true,"httpreferer":true,"httpmethod":true,"httphost":true,"httpuseragent":true,"clienttrafficonly":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsappflowparam
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "nsappflowparam": [ {"templaterefresh":<Double_value>,"udppmtu":<Double_value>,"httpurl":<String_value>,"httpcookie":<String_value>,"httpreferer":<String_value>,"httpmethod":<String_value>,"httphost":<String_value>,"httpuseragent":<String_value>,"clienttrafficonly":<String_value>}]}```



