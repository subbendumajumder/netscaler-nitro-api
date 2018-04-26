#sslocspresponder

Configuration for OCSP responser resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the OCSP responder. Cannot begin with a hash (#) or space character and must contain only ASCII alphanumeric, underscore (_), hash (#), period (.), space, colon (:), at (@), equals (=), and hyphen (-) characters. Cannot be changed after the responder is created.<br><br>The following requirement applies only to the NetScaler CLI:<br>If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my responder" or 'my responder').<br>Minimum length = 1</td></tr><tr><td>url</td><td>&lt;String></td><td>Read-write</td><td>URL of the OCSP responder.<br>Minimum length = 1</td></tr><tr><td>cache</td><td>&lt;String></td><td>Read-write</td><td>Enable caching of responses. Caching of responses received from the OCSP responder enables faster responses to the clients and reduces the load on the OCSP responder.<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>cachetimeout</td><td>&lt;Double></td><td>Read-write</td><td>Timeout for caching the OCSP response. After the timeout, the NetScaler sends a fresh request to the OCSP responder for the certificate status. If a timeout is not specified, the timeout provided in the OCSP response applies.<br>Default value: 1<br>Minimum value = 1<br>Maximum value = 1440</td></tr><tr><td>batchingdepth</td><td>&lt;Double></td><td>Read-write</td><td>Number of client certificates to batch together into one OCSP request. Batching avoids overloading the OCSP responder. A value of 1 signifies that each request is queried independently. For a value greater than 1, specify a timeout (batching delay) to avoid inordinately delaying the processing of a single certificate.<br>Minimum value = 1<br>Maximum value = 8</td></tr><tr><td>batchingdelay</td><td>&lt;Double></td><td>Read-write</td><td>Maximum time, in milliseconds, to wait to accumulate OCSP requests to batch. Does not apply if the Batching Depth is 1.<br>Minimum value = 0<br>Maximum value = 10000</td></tr><tr><td>resptimeout</td><td>&lt;Double></td><td>Read-write</td><td>Time, in milliseconds, to wait for an OCSP response. When this time elapses, an error message appears or the transaction is forwarded, depending on the settings on the virtual server. Includes Batching Delay time.<br>Minimum value = 0<br>Maximum value = 120000</td></tr><tr><td>ocspurlresolvetimeout</td><td>&lt;Double></td><td>Read-write</td><td>Time, in milliseconds, to wait for an OCSP URL Resolution. When this time elapses, an error message appears or the transaction is forwarded, depending on the settings on the virtual server.<br>Minimum value = 100<br>Maximum value = 2000</td></tr><tr><td>respondercert</td><td>&lt;String></td><td>Read-write</td><td>.<br>Minimum length = 1</td></tr><tr><td>trustresponder</td><td>&lt;Boolean></td><td>Read-write</td><td>A certificate to use to validate OCSP responses. Alternatively, if -trustResponder is specified, no verification will be done on the reponse. If both are omitted, only the response times (producedAt, lastUpdate, nextUpdate) will be verified.</td></tr><tr><td>producedattimeskew</td><td>&lt;Double></td><td>Read-write</td><td>Time, in seconds, for which the NetScaler waits before considering the response as invalid. The response is considered invalid if the Produced At time stamp in the OCSP response exceeds or precedes the current NetScaler clock time by the amount of time specified.<br>Default value: 300<br>Minimum value = 0<br>Maximum value = 86400</td></tr><tr><td>signingcert</td><td>&lt;String></td><td>Read-write</td><td>Certificate-key pair that is used to sign OCSP requests. If this parameter is not set, the requests are not signed.<br>Minimum length = 1</td></tr><tr><td>usenonce</td><td>&lt;String></td><td>Read-write</td><td>Enable the OCSP nonce extension, which is designed to prevent replay attacks.<br>Possible values = YES, NO</td></tr><tr><td>insertclientcert</td><td>&lt;String></td><td>Read-write</td><td>Include the complete client certificate in the OCSP request.<br>Possible values = YES, NO</td></tr><tr><td>httpmethod</td><td>&lt;String></td><td>Read-write</td><td>HTTP method used to send ocsp request. POST is the default httpmethod. If request length is &gt; 255, POST wil be used even if GET is set as httpMethod.<br>Default value: POST<br>Possible values = GET, POST</td></tr><tr><td>ocspaiarefcount</td><td>&lt;Double></td><td>Read-only</td><td>No of CA certs referencing this AIA responder.</td></tr><tr><td>ocspipaddrstr</td><td>&lt;String></td><td>Read-only</td><td>DNS resolved IP address.</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD]()| [DELETE](#d)| [UPDATE](#u)| [UNSET](#)| [GET (ALL)](#get-)| [GET]()| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslocspresponder
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"sslocspresponder":{<b>"name":<String_value>,</b><b>"url":<String_value>,</b>"cache":<String_value>,"cachetimeout":<Double_value>,"batchingdepth":<Double_value>,"batchingdelay":<Double_value>,"resptimeout":<Double_value>,"ocspurlresolvetimeout":<Double_value>,"respondercert":<String_value>,"trustresponder":<Boolean_value>,"producedattimeskew":<Double_value>,"signingcert":<String_value>,"usenonce":<String_value>,"insertclientcert":<String_value>,"httpmethod":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslocspresponder/name_value&lt;String&gt;
<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslocspresponder
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"sslocspresponder":{<b>"name":<String_value>,</b>"url":<String_value>,"cache":<String_value>,"cachetimeout":<Double_value>,"batchingdepth":<Double_value>,"batchingdelay":<Double_value>,"resptimeout":<Double_value>,"ocspurlresolvetimeout":<Double_value>,"respondercert":<String_value>,"trustresponder":<Boolean_value>,"producedattimeskew":<Double_value>,"signingcert":<String_value>,"usenonce":<String_value>,"insertclientcert":<String_value>,"httpmethod":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslocspresponder?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"sslocspresponder":{<b>"name":<String_value>,</b>"trustresponder":true,"insertclientcert":true,"cache":true,"cachetimeout":true,"batchingdepth":true,"batchingdelay":true,"resptimeout":true,"ocspurlresolvetimeout":true,"respondercert":true,"producedattimeskew":true,"signingcert":true,"usenonce":true,"httpmethod":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslocspresponder
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslocspresponder?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslocspresponder?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of sslocspresponder resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslocspresponder?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslocspresponder?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the sslocspresponder resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "sslocspresponder": [ {"name":<String_value>,"url":<String_value>,"cache":<String_value>,"cachetimeout":<Double_value>,"batchingdepth":<Double_value>,"batchingdelay":<Double_value>,"ocspurlresolvetimeout":<Double_value>,"resptimeout":<Double_value>,"producedattimeskew":<Double_value>,"respondercert":<String_value>,"trustresponder":<Boolean_value>,"signingcert":<String_value>,"usenonce":<String_value>,"insertclientcert":<String_value>,"ocspaiarefcount":<Double_value>,"httpmethod":<String_value>,"ocspipaddrstr":<String_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslocspresponder/name_value&lt;String&gt;
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslocspresponder/name_value&lt;String&gt;?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslocspresponder/name_value&lt;String&gt;?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "sslocspresponder": [ {"name":<String_value>,"url":<String_value>,"cache":<String_value>,"cachetimeout":<Double_value>,"batchingdepth":<Double_value>,"batchingdelay":<Double_value>,"ocspurlresolvetimeout":<Double_value>,"resptimeout":<Double_value>,"producedattimeskew":<Double_value>,"respondercert":<String_value>,"trustresponder":<Boolean_value>,"signingcert":<String_value>,"usenonce":<String_value>,"insertclientcert":<String_value>,"ocspaiarefcount":<Double_value>,"httpmethod":<String_value>,"ocspipaddrstr":<String_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslocspresponder?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "sslocspresponder": [ { "__count": "#no"} ] }```



