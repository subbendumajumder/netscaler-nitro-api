#nsicapprofile

Configuration for ICAP profile resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for an ICAP profile. Must begin with a letter, number, or the underscore \(_\) character. Other characters allowed, after the first character, are the hyphen \(-\), period \(.\), hash \(\#\), space \( \), at \(@\), colon \(:\), and equal \(=\) characters. The name of a ICAP profile cannot be changed after it is created.<br><br>CLI Users: If the name includes one or more spaces, enclose the name in double or single quotation marks \(for example, "my icap profile" or 'my icap profile'\).<br>Minimum length = 1<br>Maximum length = 127</td></tr><tr><td>preview</td><td>&lt;String></td><td>Read-write</td><td>Enable or Disable preview header with ICAP request. This feature allows an ICAP server to see the beginning of a transaction, then decide if it wants to opt-out of the transaction early instead of receiving the remainder of the request message.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>previewlength</td><td>&lt;Double></td><td>Read-write</td><td>Value of Preview Header field.<br>Default value: 4096<br>Minimum value = 0<br>Maximum value = 4294967294</td></tr><tr><td>uri</td><td>&lt;String></td><td>Read-write</td><td>URI representing icap service. It is a mandatory argument while creating an icapprofile.<br>Minimum length = 1</td></tr><tr><td>hostheader</td><td>&lt;String></td><td>Read-write</td><td>ICAP Host Header.<br>Minimum length = 1</td></tr><tr><td>useragent</td><td>&lt;String></td><td>Read-write</td><td>ICAP User Agent Header String.<br>Minimum length = 1</td></tr><tr><td>mode</td><td>&lt;String></td><td>Read-write</td><td>ICAP Mode of operation. It is a mandatory argument while creating an icapprofile.<br>Possible values = REQMOD, RESPMOD</td></tr><tr><td>queryparams</td><td>&lt;String></td><td>Read-write</td><td>Query parameters to be included with ICAP request URI. Entered values should be in arg=value format.For more than one parameters, add ; separated values. e.g.: arg1=val1;arg2=val2.<br>Minimum length = 1</td></tr><tr><td>connectionkeepalive</td><td>&lt;String></td><td>Read-write</td><td>To keep connection alive, enable this option.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>allow204</td><td>&lt;String></td><td>Read-write</td><td>This option allows to include/exclude Allow:204 header while sending request to an ICAP server.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>inserticapheaders</td><td>&lt;String></td><td>Read-write</td><td>Any custom ICAP headers that needs to be inserted while sending request to ICAP server.Follow "X-" convention while adding headers. e.g. : "X-parameter:value, X-parameter2:value2".<br>Minimum length = 1</td></tr><tr><td>reqtimeout</td><td>&lt;Double></td><td>Read-write</td><td>Time, in seconds, within which the remote service request must complete. If the request does not complete within this time, the specified request timeout action is executed. Zero disables the timeout.<br>Default value: 0<br>Minimum value = 0<br>Maximum value = 86400</td></tr><tr><td>reqtimeoutaction</td><td>&lt;String></td><td>Read-write</td><td>Name of the action to perform if the Vserver/Server representing the remote service does not respond. There are also some built-in actions which can be used. These are:<br>* BYPASS - ignore this remote service action and send the request as is.This is done by default.<br>* RESET - Reset the client connection by closing it. The client program, such as a browser, will handle this and may inform the user. The client may then resend the request if desired.<br>* DROP - Drop the request without sending a response to the user.<br>Default value: BYPASS<br>Possible values = BYPASS, DROP, RESET</td></tr><tr><td>sendreqinresmod</td><td>&lt;String></td><td>Read-write</td><td>This option allows NetScaler to encapsulate original HTTP request within RESPMOD requests sent to the ICAP server.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>onservererrorresponse</td><td>&lt;String></td><td>Read-write</td><td>Which action to perform when ICAP server sends error response.<br>Default value: CONTINUE<br>Possible values = CONTINUE, RESPOND</td></tr><tr><td>insertxclientip</td><td>&lt;String></td><td>Read-write</td><td>This option allows NetScaler to insert X-Client-IP: header while sending request to the ICAP server.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>insertxserverip</td><td>&lt;String></td><td>Read-write</td><td>This option allows NetScaler to insert X-Server-IP: header while sending request to the ICAP server.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>insertxauthuseruri</td><td>&lt;String></td><td>Read-write</td><td>This option allows NetScaler to insert Auth-User-URI: header while sending request to the ICAP server.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD]()| [DELETE](#d)| [UPDATE](#u)| [UNSET](#)| [GET (ALL)](#get-)| [GET]()| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsicapprofile
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"nsicapprofile":{<b>"name":<String_value>,</b>"preview":<String_value>,"previewlength":<Double_value>,<b>"uri":<String_value>,</b>"hostheader":<String_value>,"useragent":<String_value>,<b>"mode":<String_value>,</b>"queryparams":<String_value>,"connectionkeepalive":<String_value>,"allow204":<String_value>,"inserticapheaders":<String_value>,"reqtimeout":<Double_value>,"reqtimeoutaction":<String_value>,"sendreqinresmod":<String_value>,"onservererrorresponse":<String_value>,"insertxclientip":<String_value>,"insertxserverip":<String_value>,"insertxauthuseruri":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsicapprofile/name_value&lt;String&gt;
<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsicapprofile
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"nsicapprofile":{<b>"name":<String_value>,</b>"preview":<String_value>,"previewlength":<Double_value>,"uri":<String_value>,"hostheader":<String_value>,"useragent":<String_value>,"mode":<String_value>,"queryparams":<String_value>,"connectionkeepalive":<String_value>,"allow204":<String_value>,"inserticapheaders":<String_value>,"reqtimeout":<Double_value>,"reqtimeoutaction":<String_value>,"sendreqinresmod":<String_value>,"onservererrorresponse":<String_value>,"insertxclientip":<String_value>,"insertxserverip":<String_value>,"insertxauthuseruri":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsicapprofile?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"nsicapprofile":{<b>"name":<String_value>,</b>"preview":true,"previewlength":true,"hostheader":true,"useragent":true,"queryparams":true,"connectionkeepalive":true,"allow204":true,"inserticapheaders":true,"reqtimeout":true,"reqtimeoutaction":true,"sendreqinresmod":true,"onservererrorresponse":true,"insertxclientip":true,"insertxserverip":true,"insertxauthuseruri":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsicapprofile
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsicapprofile?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsicapprofile?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of nsicapprofile resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsicapprofile?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsicapprofile?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the nsicapprofile resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "nsicapprofile": [ {"name":<String_value>,"preview":<String_value>,"previewlength":<Double_value>,"uri":<String_value>,"hostheader":<String_value>,"useragent":<String_value>,"mode":<String_value>,"queryparams":<String_value>,"connectionkeepalive":<String_value>,"allow204":<String_value>,"inserticapheaders":<String_value>,"reqtimeout":<Double_value>,"reqtimeoutaction":<String_value>,"sendreqinresmod":<String_value>,"onservererrorresponse":<String_value>,"insertxclientip":<String_value>,"insertxserverip":<String_value>,"insertxauthuseruri":<String_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsicapprofile/name_value&lt;String&gt;
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsicapprofile/name_value&lt;String&gt;?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsicapprofile/name_value&lt;String&gt;?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "nsicapprofile": [ {"name":<String_value>,"preview":<String_value>,"previewlength":<Double_value>,"uri":<String_value>,"hostheader":<String_value>,"useragent":<String_value>,"mode":<String_value>,"queryparams":<String_value>,"connectionkeepalive":<String_value>,"allow204":<String_value>,"inserticapheaders":<String_value>,"reqtimeout":<Double_value>,"reqtimeoutaction":<String_value>,"sendreqinresmod":<String_value>,"onservererrorresponse":<String_value>,"insertxclientip":<String_value>,"insertxserverip":<String_value>,"insertxauthuseruri":<String_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsicapprofile?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "nsicapprofile": [ { "__count": "#no"} ] }```



