#vpnclientlessaccessprofile

Configuration for Clientless VPN rewrite profile resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>profilename</td><td>&lt;String></td><td>Read-write</td><td>Name for the NetScaler Gateway clientless access profile. Must begin with an ASCII alphabetic or underscore (_) character, and must consist only of ASCII alphanumeric, underscore, hash (#), period (.), space, colon (:), at (@), equals (=), and hyphen (-) characters. Cannot be changed after the profile is created.<br><br>The following requirement applies only to the NetScaler CLI:<br>If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my profile" or 'my profile').<br>Minimum length = 1</td></tr><tr><td>urlrewritepolicylabel</td><td>&lt;String></td><td>Read-write</td><td>Name of the configured URL rewrite policy label. If you do not specify a policy label name, then URLs are not rewritten.<br>Minimum length = 1</td></tr><tr><td>javascriptrewritepolicylabel</td><td>&lt;String></td><td>Read-write</td><td>Name of the configured JavaScript rewrite policy label. If you do not specify a policy label name, then JAVA scripts are not rewritten.<br>Minimum length = 1</td></tr><tr><td>reqhdrrewritepolicylabel</td><td>&lt;String></td><td>Read-write</td><td>Name of the configured Request rewrite policy label. If you do not specify a policy label name, then requests are not rewritten.<br>Minimum length = 1</td></tr><tr><td>reshdrrewritepolicylabel</td><td>&lt;String></td><td>Read-write</td><td>Name of the configured Response rewrite policy label.<br>Minimum length = 1</td></tr><tr><td>regexforfindingurlinjavascript</td><td>&lt;String></td><td>Read-write</td><td>Name of the pattern set that contains the regular expressions, which match the URL in Java script.<br>Minimum length = 1</td></tr><tr><td>regexforfindingurlincss</td><td>&lt;String></td><td>Read-write</td><td>Name of the pattern set that contains the regular expressions, which match the URL in the CSS.<br>Minimum length = 1</td></tr><tr><td>regexforfindingurlinxcomponent</td><td>&lt;String></td><td>Read-write</td><td>Name of the pattern set that contains the regular expressions, which match the URL in X Component.<br>Minimum length = 1</td></tr><tr><td>regexforfindingurlinxml</td><td>&lt;String></td><td>Read-write</td><td>Name of the pattern set that contains the regular expressions, which match the URL in XML.<br>Minimum length = 1</td></tr><tr><td>regexforfindingcustomurls</td><td>&lt;String></td><td>Read-write</td><td>Name of the pattern set that contains the regular expressions, which match the URLs in the custom content type other than HTML, CSS, XML, XCOMP, and JavaScript. The custom content type should be included in the patset ns_cvpn_custom_content_types.<br>Minimum length = 1</td></tr><tr><td>clientconsumedcookies</td><td>&lt;String></td><td>Read-write</td><td>Specify the name of the pattern set containing the names of the cookies, which are allowed between the client and the server. If a pattern set is not specified, NetSCaler Gateway does not allow any cookies between the client and the server. A cookie that is not specified in the pattern set is handled by NetScaler Gateway on behalf of the client.<br>Minimum length = 1</td></tr><tr><td>requirepersistentcookie</td><td>&lt;String></td><td>Read-write</td><td>Specify whether a persistent session cookie is set and accepted for clientless access. If this parameter is set to ON, COM objects, such as MSOffice, which are invoked by the browser can access the files using clientless access. Use caution because the persistent cookie is stored on the disk.<br>Default value: OFF<br>Possible values = ON, OFF</td></tr><tr><td>cssrewritepolicylabel</td><td>&lt;String></td><td>Read-only</td><td>The configured CSS rewrite policylabel.<br>Minimum length = 1</td></tr><tr><td>xmlrewritepolicylabel</td><td>&lt;String></td><td>Read-only</td><td>The configured XML rewrite policylabel.<br>Minimum length = 1</td></tr><tr><td>xcomponentrewritepolicylabel</td><td>&lt;String></td><td>Read-only</td><td>The configured X-Component rewrite policylabel.<br>Minimum length = 1</td></tr><tr><td>isdefault</td><td>&lt;Boolean></td><td>Read-only</td><td>A value of true is returned if it is a default vpnclientlessrwprofile.</td></tr><tr><td>description</td><td>&lt;String></td><td>Read-only</td><td>Description of the clientless access profile.</td></tr><tr><td>builtin</td><td>&lt;String[]></td><td>Read-only</td><td>Flag to determine if vpn clientless rewrite profile is built-in or not.<br>Possible values = MODIFIABLE, DELETABLE, IMMUTABLE, PARTITION_ALL</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD]()| [DELETE](#d)| [UPDATE](#u)| [UNSET](#)| [GET (ALL)](#get-)| [GET]()| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnclientlessaccessprofile
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"vpnclientlessaccessprofile":{<b>"profilename":<String_value></b>}}```
<b>Response:</b>
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnclientlessaccessprofile/profilename_value&lt;String&gt;
<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnclientlessaccessprofile
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"vpnclientlessaccessprofile":{<b>"profilename":<String_value>,</b>"urlrewritepolicylabel":<String_value>,"javascriptrewritepolicylabel":<String_value>,"reqhdrrewritepolicylabel":<String_value>,"reshdrrewritepolicylabel":<String_value>,"regexforfindingurlinjavascript":<String_value>,"regexforfindingurlincss":<String_value>,"regexforfindingurlinxcomponent":<String_value>,"regexforfindingurlinxml":<String_value>,"regexforfindingcustomurls":<String_value>,"clientconsumedcookies":<String_value>,"requirepersistentcookie":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnclientlessaccessprofile?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"vpnclientlessaccessprofile":{<b>"profilename":<String_value>,</b>"urlrewritepolicylabel":true,"javascriptrewritepolicylabel":true,"reqhdrrewritepolicylabel":true,"reshdrrewritepolicylabel":true,"regexforfindingurlinjavascript":true,"regexforfindingurlincss":true,"regexforfindingurlinxcomponent":true,"regexforfindingurlinxml":true,"regexforfindingcustomurls":true,"clientconsumedcookies":true,"requirepersistentcookie":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnclientlessaccessprofile
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnclientlessaccessprofile?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnclientlessaccessprofile?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of vpnclientlessaccessprofile resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnclientlessaccessprofile?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnclientlessaccessprofile?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the vpnclientlessaccessprofile resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "vpnclientlessaccessprofile": [ {"profilename":<String_value>,"urlrewritepolicylabel":<String_value>,"javascriptrewritepolicylabel":<String_value>,"cssrewritepolicylabel":<String_value>,"xmlrewritepolicylabel":<String_value>,"xcomponentrewritepolicylabel":<String_value>,"reqhdrrewritepolicylabel":<String_value>,"reshdrrewritepolicylabel":<String_value>,"regexforfindingurlinjavascript":<String_value>,"regexforfindingurlincss":<String_value>,"regexforfindingurlinxcomponent":<String_value>,"regexforfindingurlinxml":<String_value>,"regexforfindingcustomurls":<String_value>,"clientconsumedcookies":<String_value>,"requirepersistentcookie":<String_value>,"isdefault":<Boolean_value>,"description":<String_value>,"builtin":<String[]_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnclientlessaccessprofile/profilename_value&lt;String&gt;
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnclientlessaccessprofile/profilename_value&lt;String&gt;?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnclientlessaccessprofile/profilename_value&lt;String&gt;?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "vpnclientlessaccessprofile": [ {"profilename":<String_value>,"urlrewritepolicylabel":<String_value>,"javascriptrewritepolicylabel":<String_value>,"cssrewritepolicylabel":<String_value>,"xmlrewritepolicylabel":<String_value>,"xcomponentrewritepolicylabel":<String_value>,"reqhdrrewritepolicylabel":<String_value>,"reshdrrewritepolicylabel":<String_value>,"regexforfindingurlinjavascript":<String_value>,"regexforfindingurlincss":<String_value>,"regexforfindingurlinxcomponent":<String_value>,"regexforfindingurlinxml":<String_value>,"regexforfindingcustomurls":<String_value>,"clientconsumedcookies":<String_value>,"requirepersistentcookie":<String_value>,"isdefault":<Boolean_value>,"description":<String_value>,"builtin":<String[]_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnclientlessaccessprofile?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "vpnclientlessaccessprofile": [ { "__count": "#no"} ] }```



