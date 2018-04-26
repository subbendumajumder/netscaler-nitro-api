#ipsecparameter

Configuration for IPSEC paramter resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>ikeversion</td><td>&lt;String></td><td>Read-write</td><td>IKE Protocol Version.<br>Default value: V2<br>Possible values = V1, V2</td></tr><tr><td>encalgo</td><td>&lt;String[]></td><td>Read-write</td><td>Type of encryption algorithm (Note: Selection of AES enables AES128).<br>Default value: AES<br>Possible values = AES, 3DES, AES192, AES256</td></tr><tr><td>hashalgo</td><td>&lt;String[]></td><td>Read-write</td><td>Type of hashing algorithm.<br>Default value: HMAC_SHA256<br>Possible values = HMAC_SHA1, HMAC_SHA256, HMAC_SHA384, HMAC_SHA512, HMAC_MD5</td></tr><tr><td>lifetime</td><td>&lt;Double></td><td>Read-write</td><td>Lifetime of IKE SA in seconds. Lifetime of IPSec SA will be (lifetime of IKE SA/8).<br>Minimum value = 480<br>Maximum value = 31536000</td></tr><tr><td>livenesscheckinterval</td><td>&lt;Double></td><td>Read-write</td><td>Number of seconds after which a notify payload is sent to check the liveliness of the peer. Additional retries are done as per retransmit interval setting. Zero value disables liveliness checks.<br>Minimum value = 0<br>Maximum value = 64999</td></tr><tr><td>replaywindowsize</td><td>&lt;Double></td><td>Read-write</td><td>IPSec Replay window size for the data traffic.<br>Minimum value = 0<br>Maximum value = 16384</td></tr><tr><td>ikeretryinterval</td><td>&lt;Double></td><td>Read-write</td><td>IKE retry interval for bringing up the connection.<br>Minimum value = 60<br>Maximum value = 3600</td></tr><tr><td>perfectforwardsecrecy</td><td>&lt;String></td><td>Read-write</td><td>Enable/Disable PFS.<br>Default value: DISABLE<br>Possible values = ENABLE, DISABLE</td></tr><tr><td>retransmissiontime</td><td>&lt;Double></td><td>Read-write</td><td>The interval in seconds to retry sending the IKE messages to peer, three consecutive attempts are done with doubled interval after every failure,<br>increases for every retransmit till 6 retransmits.<br>Minimum value = 1<br>Maximum value = 99</td></tr><tr><td>responderonly</td><td>&lt;String></td><td>Read-only</td><td>Responder Only config for IKED.<br>Default value: NO<br>Possible values = YES, NO</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[UPDATE](#u)| [UNSET](#)| [GET (ALL)](#get-)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/ipsecparameter
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"ipsecparameter":{"ikeversion":<String_value>,"encalgo":<String[]_value>,"hashalgo":<String[]_value>,"lifetime":<Double_value>,"livenesscheckinterval":<Double_value>,"replaywindowsize":<Double_value>,"ikeretryinterval":<Double_value>,"perfectforwardsecrecy":<String_value>,"retransmissiontime":<Double_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/ipsecparameter?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"ipsecparameter":{"ikeversion":true,"encalgo":true,"hashalgo":true,"lifetime":true,"livenesscheckinterval":true,"replaywindowsize":true,"ikeretryinterval":true,"perfectforwardsecrecy":true,"retransmissiontime":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/ipsecparameter
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "ipsecparameter": [ {"ikeversion":<String_value>,"encalgo":<String[]_value>,"hashalgo":<String[]_value>,"lifetime":<Double_value>,"livenesscheckinterval":<Double_value>,"replaywindowsize":<Double_value>,"ikeretryinterval":<Double_value>,"perfectforwardsecrecy":<String_value>,"responderonly":<String_value>,"retransmissiontime":<Double_value>}]}```



