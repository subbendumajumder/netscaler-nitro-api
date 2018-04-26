#authenticationwebauthaction

Configuration for Web authentication action resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the Web Authentication action. <br>Must begin with a letter, number, or the underscore character (_), and must contain only letters, numbers, and the hyphen (-), period (.) pound (#), space ( ), at (@), equals (=), colon (:), and underscore characters. Cannot be changed after the profile is created.<br><br>The following requirement applies only to the NetScaler CLI:<br>If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my authentication action" or 'my authentication action').<br>Minimum length = 1</td></tr><tr><td>serverip</td><td>&lt;String></td><td>Read-write</td><td>IP address of the web server to be used for authentication.<br>Minimum length = 1</td></tr><tr><td>serverport</td><td>&lt;Integer></td><td>Read-write</td><td>Port on which the web server accepts connections.<br>Minimum value = 1<br>Range 1 - 65535<br>* in CLI is represented as 65535 in NITRO API</td></tr><tr><td>fullreqexpr</td><td>&lt;String></td><td>Read-write</td><td>Exact HTTP request, in the form of a default syntax expression, which the NetScaler appliance sends to the authentication server.<br>The NetScaler appliance does not check the validity of this request. One must manually validate the request.</td></tr><tr><td>scheme</td><td>&lt;String></td><td>Read-write</td><td>Type of scheme for the web server.<br>Possible values = http, https</td></tr><tr><td>successrule</td><td>&lt;String></td><td>Read-write</td><td>Expression, that checks to see if authentication is successful.</td></tr><tr><td>defaultauthenticationgroup</td><td>&lt;String></td><td>Read-write</td><td>This is the default group that is chosen when the authentication succeeds in addition to extracted groups.</td></tr><tr><td>attribute1</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute1 from the webauth response.<br>Maximum length = 128</td></tr><tr><td>attribute2</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute2 from the webauth response.<br>Maximum length = 128</td></tr><tr><td>attribute3</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute3 from the webauth response.<br>Maximum length = 128</td></tr><tr><td>attribute4</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute4 from the webauth response.<br>Maximum length = 128</td></tr><tr><td>attribute5</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute5 from the webauth response.<br>Maximum length = 128</td></tr><tr><td>attribute6</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute6 from the webauth response.<br>Maximum length = 128</td></tr><tr><td>attribute7</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute7 from the webauth response.<br>Maximum length = 128</td></tr><tr><td>attribute8</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute8 from the webauth response.<br>Maximum length = 128</td></tr><tr><td>attribute9</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute9 from the webauth response.<br>Maximum length = 128</td></tr><tr><td>attribute10</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute10 from the webauth response.<br>Maximum length = 128</td></tr><tr><td>attribute11</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute11 from the webauth response.<br>Maximum length = 128</td></tr><tr><td>attribute12</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute12 from the webauth response.<br>Maximum length = 128</td></tr><tr><td>attribute13</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute13 from the webauth response.<br>Maximum length = 128</td></tr><tr><td>attribute14</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute14 from the webauth response.<br>Maximum length = 128</td></tr><tr><td>attribute15</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute15 from the webauth response.<br>Maximum length = 128</td></tr><tr><td>attribute16</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute16 from the webauth response.<br>Maximum length = 128</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD]()| [DELETE](#d)| [UPDATE](#u)| [UNSET](#)| [GET (ALL)](#get-)| [GET]()| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationwebauthaction
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"authenticationwebauthaction":{<b>"name":<String_value>,</b><b>"serverip":<String_value>,</b><b>"serverport":<Integer_value>,</b>"fullreqexpr":<String_value>,<b>"scheme":<String_value>,</b><b>"successrule":<String_value>,</b>"defaultauthenticationgroup":<String_value>,"attribute1":<String_value>,"attribute2":<String_value>,"attribute3":<String_value>,"attribute4":<String_value>,"attribute5":<String_value>,"attribute6":<String_value>,"attribute7":<String_value>,"attribute8":<String_value>,"attribute9":<String_value>,"attribute10":<String_value>,"attribute11":<String_value>,"attribute12":<String_value>,"attribute13":<String_value>,"attribute14":<String_value>,"attribute15":<String_value>,"attribute16":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationwebauthaction/name_value&lt;String&gt;
<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationwebauthaction
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"authenticationwebauthaction":{<b>"name":<String_value>,</b>"serverip":<String_value>,"serverport":<Integer_value>,"fullreqexpr":<String_value>,"scheme":<String_value>,"successrule":<String_value>,"defaultauthenticationgroup":<String_value>,"attribute1":<String_value>,"attribute2":<String_value>,"attribute3":<String_value>,"attribute4":<String_value>,"attribute5":<String_value>,"attribute6":<String_value>,"attribute7":<String_value>,"attribute8":<String_value>,"attribute9":<String_value>,"attribute10":<String_value>,"attribute11":<String_value>,"attribute12":<String_value>,"attribute13":<String_value>,"attribute14":<String_value>,"attribute15":<String_value>,"attribute16":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationwebauthaction?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"authenticationwebauthaction":{<b>"name":<String_value>,</b>"serverip":true,"serverport":true,"fullreqexpr":true,"defaultauthenticationgroup":true,"attribute1":true,"attribute2":true,"attribute3":true,"attribute4":true,"attribute5":true,"attribute6":true,"attribute7":true,"attribute8":true,"attribute9":true,"attribute10":true,"attribute11":true,"attribute12":true,"attribute13":true,"attribute14":true,"attribute15":true,"attribute16":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationwebauthaction
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationwebauthaction?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationwebauthaction?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of authenticationwebauthaction resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationwebauthaction?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationwebauthaction?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the authenticationwebauthaction resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "authenticationwebauthaction": [ {"name":<String_value>,"serverip":<String_value>,"serverport":<Integer_value>,"fullreqexpr":<String_value>,"scheme":<String_value>,"successrule":<String_value>,"defaultauthenticationgroup":<String_value>,"attribute1":<String_value>,"attribute2":<String_value>,"attribute3":<String_value>,"attribute4":<String_value>,"attribute5":<String_value>,"attribute6":<String_value>,"attribute7":<String_value>,"attribute8":<String_value>,"attribute9":<String_value>,"attribute10":<String_value>,"attribute11":<String_value>,"attribute12":<String_value>,"attribute13":<String_value>,"attribute14":<String_value>,"attribute15":<String_value>,"attribute16":<String_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationwebauthaction/name_value&lt;String&gt;
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationwebauthaction/name_value&lt;String&gt;?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationwebauthaction/name_value&lt;String&gt;?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "authenticationwebauthaction": [ {"name":<String_value>,"serverip":<String_value>,"serverport":<Integer_value>,"fullreqexpr":<String_value>,"scheme":<String_value>,"successrule":<String_value>,"defaultauthenticationgroup":<String_value>,"attribute1":<String_value>,"attribute2":<String_value>,"attribute3":<String_value>,"attribute4":<String_value>,"attribute5":<String_value>,"attribute6":<String_value>,"attribute7":<String_value>,"attribute8":<String_value>,"attribute9":<String_value>,"attribute10":<String_value>,"attribute11":<String_value>,"attribute12":<String_value>,"attribute13":<String_value>,"attribute14":<String_value>,"attribute15":<String_value>,"attribute16":<String_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationwebauthaction?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "authenticationwebauthaction": [ { "__count": "#no"} ] }```



