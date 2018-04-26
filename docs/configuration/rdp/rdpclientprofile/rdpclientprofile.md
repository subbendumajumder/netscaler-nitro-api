#rdpclientprofile

Configuration for RDP clientprofile resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>The name of the rdp profile.<br>Minimum length = 1</td></tr><tr><td>rdpurloverride</td><td>&lt;String></td><td>Read-write</td><td>This setting determines whether the RDP parameters supplied in the vpn url override those specified in the RDP profile.<br>Default value: ENABLE<br>Possible values = ENABLE, DISABLE</td></tr><tr><td>redirectclipboard</td><td>&lt;String></td><td>Read-write</td><td>This setting corresponds to the Clipboard check box on the Local Resources tab under Options in RDC.<br>Default value: ENABLE<br>Possible values = ENABLE, DISABLE</td></tr><tr><td>redirectdrives</td><td>&lt;String></td><td>Read-write</td><td>This setting corresponds to the selections for Drives under More on the Local Resources tab under Options in RDC.<br>Default value: DISABLE<br>Possible values = ENABLE, DISABLE</td></tr><tr><td>redirectprinters</td><td>&lt;String></td><td>Read-write</td><td>This setting corresponds to the selection in the Printers check box on the Local Resources tab under Options in RDC.<br>Default value: ENABLE<br>Possible values = ENABLE, DISABLE</td></tr><tr><td>redirectcomports</td><td>&lt;String></td><td>Read-write</td><td>This setting corresponds to the selections for comports under More on the Local Resources tab under Options in RDC.<br>Default value: DISABLE<br>Possible values = ENABLE, DISABLE</td></tr><tr><td>redirectpnpdevices</td><td>&lt;String></td><td>Read-write</td><td>This setting corresponds to the selections for pnpdevices under More on the Local Resources tab under Options in RDC.<br>Default value: DISABLE<br>Possible values = ENABLE, DISABLE</td></tr><tr><td>keyboardhook</td><td>&lt;String></td><td>Read-write</td><td>This setting corresponds to the selection in the Keyboard drop-down list on the Local Resources tab under Options in RDC.<br>Default value: InFullScreenMode<br>Possible values = OnLocal, OnRemote, InFullScreenMode</td></tr><tr><td>audiocapturemode</td><td>&lt;String></td><td>Read-write</td><td>This setting corresponds to the selections in the Remote audio area on the Local Resources tab under Options in RDC.<br>Default value: DISABLE<br>Possible values = ENABLE, DISABLE</td></tr><tr><td>videoplaybackmode</td><td>&lt;String></td><td>Read-write</td><td>This setting determines if Remote Desktop Connection (RDC) will use RDP efficient multimedia streaming for video playback.<br>Default value: ENABLE<br>Possible values = ENABLE, DISABLE</td></tr><tr><td>multimonitorsupport</td><td>&lt;String></td><td>Read-write</td><td>Enable/Disable Multiple Monitor Support for Remote Desktop Connection (RDC).<br>Default value: ENABLE<br>Possible values = ENABLE, DISABLE</td></tr><tr><td>rdpcookievalidity</td><td>&lt;Double></td><td>Read-write</td><td>RDP cookie validity period.<br>Default value: 60<br>Minimum value = 1<br>Maximum value = 86400</td></tr><tr><td>addusernameinrdpfile</td><td>&lt;String></td><td>Read-write</td><td>Add username in rdp file.<br>Default value: NO<br>Possible values = YES, NO</td></tr><tr><td>rdpfilename</td><td>&lt;String></td><td>Read-write</td><td>RDP file name to be sent to End User.<br>Minimum length = 1</td></tr><tr><td>rdphost</td><td>&lt;String></td><td>Read-write</td><td>Fully-qualified domain name (FQDN) of the RDP Listener.<br>Maximum length = 252</td></tr><tr><td>rdplistener</td><td>&lt;String></td><td>Read-write</td><td>IP address (or) Fully-qualified domain name(FQDN) of the RDP Listener with the port in the format IP:Port (or) FQDN:Port.<br>Maximum length = 255</td></tr><tr><td>rdpcustomparams</td><td>&lt;String></td><td>Read-write</td><td>Option for RDP custom parameters settings (if any). Custom params needs to be separated by ';'.<br>Default value: 0<br>Minimum length = 1</td></tr><tr><td>psk</td><td>&lt;String></td><td>Read-write</td><td>Pre shared key value.<br>Default value: 0</td></tr><tr><td>builtin</td><td>&lt;String[]></td><td>Read-only</td><td>Indicates that a variable is a built-in (SYSTEM INTERNAL) type.<br>Possible values = MODIFIABLE, DELETABLE, IMMUTABLE, PARTITION_ALL</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD]()| [UPDATE](#u)| [UNSET](#)| [DELETE](#d)| [GET (ALL)](#get-)| [GET]()| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/rdpclientprofile
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"rdpclientprofile":{<b>"name":<String_value>,</b>"rdpurloverride":<String_value>,"redirectclipboard":<String_value>,"redirectdrives":<String_value>,"redirectprinters":<String_value>,"redirectcomports":<String_value>,"redirectpnpdevices":<String_value>,"keyboardhook":<String_value>,"audiocapturemode":<String_value>,"videoplaybackmode":<String_value>,"multimonitorsupport":<String_value>,"rdpcookievalidity":<Double_value>,"addusernameinrdpfile":<String_value>,"rdpfilename":<String_value>,"rdphost":<String_value>,"rdplistener":<String_value>,"rdpcustomparams":<String_value>,"psk":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/rdpclientprofile
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"rdpclientprofile":{<b>"name":<String_value>,</b>"rdpurloverride":<String_value>,"redirectclipboard":<String_value>,"redirectdrives":<String_value>,"redirectprinters":<String_value>,"redirectcomports":<String_value>,"redirectpnpdevices":<String_value>,"keyboardhook":<String_value>,"audiocapturemode":<String_value>,"videoplaybackmode":<String_value>,"multimonitorsupport":<String_value>,"rdpcookievalidity":<Double_value>,"addusernameinrdpfile":<String_value>,"rdpfilename":<String_value>,"rdphost":<String_value>,"rdplistener":<String_value>,"rdpcustomparams":<String_value>,"psk":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/rdpclientprofile?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"rdpclientprofile":{<b>"name":<String_value>,</b>"rdpurloverride":true,"redirectclipboard":true,"redirectdrives":true,"redirectprinters":true,"redirectcomports":true,"redirectpnpdevices":true,"keyboardhook":true,"audiocapturemode":true,"videoplaybackmode":true,"multimonitorsupport":true,"rdpcookievalidity":true,"addusernameinrdpfile":true,"rdpfilename":true,"rdphost":true,"rdplistener":true,"rdpcustomparams":true,"psk":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/rdpclientprofile/name_value&lt;String&gt;
<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/rdpclientprofile
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/rdpclientprofile?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/rdpclientprofile?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of rdpclientprofile resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/rdpclientprofile?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/rdpclientprofile?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the rdpclientprofile resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "rdpclientprofile": [ {"name":<String_value>,"rdpurloverride":<String_value>,"redirectclipboard":<String_value>,"redirectdrives":<String_value>,"redirectprinters":<String_value>,"redirectcomports":<String_value>,"redirectpnpdevices":<String_value>,"keyboardhook":<String_value>,"audiocapturemode":<String_value>,"videoplaybackmode":<String_value>,"multimonitorsupport":<String_value>,"rdpcookievalidity":<Double_value>,"addusernameinrdpfile":<String_value>,"rdpfilename":<String_value>,"rdphost":<String_value>,"rdplistener":<String_value>,"rdpcustomparams":<String_value>,"psk":<String_value>,"builtin":<String[]_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/rdpclientprofile/name_value&lt;String&gt;
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/rdpclientprofile/name_value&lt;String&gt;?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/rdpclientprofile/name_value&lt;String&gt;?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "rdpclientprofile": [ {"name":<String_value>,"rdpurloverride":<String_value>,"redirectclipboard":<String_value>,"redirectdrives":<String_value>,"redirectprinters":<String_value>,"redirectcomports":<String_value>,"redirectpnpdevices":<String_value>,"keyboardhook":<String_value>,"audiocapturemode":<String_value>,"videoplaybackmode":<String_value>,"multimonitorsupport":<String_value>,"rdpcookievalidity":<Double_value>,"addusernameinrdpfile":<String_value>,"rdpfilename":<String_value>,"rdphost":<String_value>,"rdplistener":<String_value>,"rdpcustomparams":<String_value>,"psk":<String_value>,"builtin":<String[]_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/rdpclientprofile?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "rdpclientprofile": [ { "__count": "#no"} ] }```



