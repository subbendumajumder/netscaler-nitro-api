#nscqaparam

Configuration for cqaparam resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>harqretxdelay</td><td>&lt;Double></td><td>Read-write</td><td>HARQ retransmission delay (in ms).<br>Default value: 0<br>Minimum value = 1<br>Maximum value = 64000</td></tr><tr><td>net1label</td><td>&lt;String></td><td>Read-write</td><td>Name of the network label.<br>Maximum length = 15</td></tr><tr><td>minrttnet1</td><td>&lt;Double></td><td>Read-write</td><td>MIN RTT (in ms) for the first network.<br>Default value: 0<br>Minimum value = 0<br>Maximum value = 6400</td></tr><tr><td>lr1coeflist</td><td>&lt;String></td><td>Read-write</td><td>coefficients values for Label1.</td></tr><tr><td>lr1probthresh</td><td>&lt;Double></td><td>Read-write</td><td>Probability threshold values for LR model to differentiate between NET1 and reset(NET2 and NET3).<br>Default value: 0<br>Minimum value = 0<br>Maximum value = 1</td></tr><tr><td>net1cclscale</td><td>&lt;String></td><td>Read-write</td><td>Three congestion level scores limits corresponding to None, Low, Medium.</td></tr><tr><td>net1csqscale</td><td>&lt;String></td><td>Read-write</td><td>Three signal quality level scores limits corresponding to Excellent, Good, Fair.</td></tr><tr><td>net1logcoef</td><td>&lt;String></td><td>Read-write</td><td>Connection quality ranking Log coefficients of network 1.</td></tr><tr><td>net2label</td><td>&lt;String></td><td>Read-write</td><td>Name of the network label 2.<br>Maximum length = 15</td></tr><tr><td>minrttnet2</td><td>&lt;Double></td><td>Read-write</td><td>MIN RTT (in ms) for the second network.<br>Default value: 0<br>Minimum value = 0<br>Maximum value = 6400</td></tr><tr><td>lr2coeflist</td><td>&lt;String></td><td>Read-write</td><td>coefficients values for Label 2.</td></tr><tr><td>lr2probthresh</td><td>&lt;Double></td><td>Read-write</td><td>Probability threshold values for LR model to differentiate between NET2 and NET3.<br>Default value: 0<br>Minimum value = 0<br>Maximum value = 1</td></tr><tr><td>net2cclscale</td><td>&lt;String></td><td>Read-write</td><td>Three congestion level scores limits corresponding to None, Low, Medium.</td></tr><tr><td>net2csqscale</td><td>&lt;String></td><td>Read-write</td><td>Three signal quality level scores limits corresponding to Excellent, Good, Fair.</td></tr><tr><td>net2logcoef</td><td>&lt;String></td><td>Read-write</td><td>Connnection quality ranking Log coefficients of network 2.</td></tr><tr><td>net3label</td><td>&lt;String></td><td>Read-write</td><td>Name of the network label 3.<br>Maximum length = 15</td></tr><tr><td>minrttnet3</td><td>&lt;Double></td><td>Read-write</td><td>MIN RTT (in ms) for the third network.<br>Default value: 0<br>Minimum value = 0<br>Maximum value = 6400</td></tr><tr><td>net3cclscale</td><td>&lt;String></td><td>Read-write</td><td>Three congestion level scores limits corresponding to None, Low, Medium.</td></tr><tr><td>net3csqscale</td><td>&lt;String></td><td>Read-write</td><td>Three signal quality level scores limits corresponding to Excellent, Good, Fair.</td></tr><tr><td>net3logcoef</td><td>&lt;String></td><td>Read-write</td><td>Connection quality ranking Log coefficients of network 3.</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[UPDATE](#u)| [UNSET](#)| [GET (ALL)](#get-)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nscqaparam
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"nscqaparam":{"harqretxdelay":<Double_value>,"net1label":<String_value>,"minrttnet1":<Double_value>,"lr1coeflist":<String_value>,"lr1probthresh":<Double_value>,"net1cclscale":<String_value>,"net1csqscale":<String_value>,"net1logcoef":<String_value>,"net2label":<String_value>,"minrttnet2":<Double_value>,"lr2coeflist":<String_value>,"lr2probthresh":<Double_value>,"net2cclscale":<String_value>,"net2csqscale":<String_value>,"net2logcoef":<String_value>,"net3label":<String_value>,"minrttnet3":<Double_value>,"net3cclscale":<String_value>,"net3csqscale":<String_value>,"net3logcoef":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nscqaparam?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"nscqaparam":{"harqretxdelay":true,"net1label":true,"minrttnet1":true,"lr1coeflist":true,"lr1probthresh":true,"net1cclscale":true,"net1csqscale":true,"net1logcoef":true,"net2label":true,"minrttnet2":true,"net2cclscale":true,"net2csqscale":true,"net2logcoef":true,"net3label":true,"minrttnet3":true,"net3cclscale":true,"net3csqscale":true,"net3logcoef":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nscqaparam
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "nscqaparam": [ {"harqretxdelay":<Double_value>,"net1label":<String_value>,"net2label":<String_value>,"minrttnet1":<Double_value>,"lr1coeflist":<String_value>,"lr1probthresh":<Double_value>,"net1cclscale":<String_value>,"net1csqscale":<String_value>,"net1logcoef":<String_value>,"minrttnet2":<Double_value>,"lr2coeflist":<String_value>,"lr2probthresh":<Double_value>,"net2cclscale":<String_value>,"net2csqscale":<String_value>,"net2logcoef":<String_value>,"net3label":<String_value>,"minrttnet3":<Double_value>,"net3cclscale":<String_value>,"net3csqscale":<String_value>,"net3logcoef":<String_value>}]}```



