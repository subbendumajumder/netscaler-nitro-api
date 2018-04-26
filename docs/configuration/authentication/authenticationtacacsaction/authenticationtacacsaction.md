#authenticationtacacsaction

Configuration for TACACS action resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the TACACS+ profile (action). <br>Must begin with a letter, number, or the underscore character (_), and must contain only letters, numbers, and the hyphen (-), period (.) pound (#), space ( ), at (@), equals (=), colon (:), and underscore characters. Cannot be changed after TACACS profile is created.<br><br>The following requirement applies only to the NetScaler CLI:<br>If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my authentication action" or 'y authentication action').<br>Minimum length = 1</td></tr><tr><td>serverip</td><td>&lt;String></td><td>Read-write</td><td>IP address assigned to the TACACS+ server.<br>Minimum length = 1</td></tr><tr><td>serverport</td><td>&lt;Integer></td><td>Read-write</td><td>Port number on which the TACACS+ server listens for connections.<br>Default value: 49<br>Minimum value = 1</td></tr><tr><td>authtimeout</td><td>&lt;Double></td><td>Read-write</td><td>Number of seconds the NetScaler appliance waits for a response from the TACACS+ server.<br>Default value: 3<br>Minimum value = 1</td></tr><tr><td>tacacssecret</td><td>&lt;String></td><td>Read-write</td><td>Key shared between the TACACS+ server and the NetScaler appliance. <br>Required for allowing the NetScaler appliance to communicate with the TACACS+ server.<br>Minimum length = 1</td></tr><tr><td>authorization</td><td>&lt;String></td><td>Read-write</td><td>Use streaming authorization on the TACACS+ server.<br>Possible values = ON, OFF</td></tr><tr><td>accounting</td><td>&lt;String></td><td>Read-write</td><td>Whether the TACACS+ server is currently accepting accounting messages.<br>Possible values = ON, OFF</td></tr><tr><td>auditfailedcmds</td><td>&lt;String></td><td>Read-write</td><td>The state of the TACACS+ server that will receive accounting messages.<br>Possible values = ON, OFF</td></tr><tr><td>groupattrname</td><td>&lt;String></td><td>Read-write</td><td>TACACS+ group attribute name.<br>Used for group extraction on the TACACS+ server.</td></tr><tr><td>defaultauthenticationgroup</td><td>&lt;String></td><td>Read-write</td><td>This is the default group that is chosen when the authentication succeeds in addition to extracted groups.</td></tr><tr><td>attribute1</td><td>&lt;String></td><td>Read-write</td><td>Name of the custom attribute to be extracted from server and stored at index '1' (where '1' changes for each attribute).</td></tr><tr><td>attribute2</td><td>&lt;String></td><td>Read-write</td><td>Name of the custom attribute to be extracted from server and stored at index '2' (where '2' changes for each attribute).</td></tr><tr><td>attribute3</td><td>&lt;String></td><td>Read-write</td><td>Name of the custom attribute to be extracted from server and stored at index '3' (where '3' changes for each attribute).</td></tr><tr><td>attribute4</td><td>&lt;String></td><td>Read-write</td><td>Name of the custom attribute to be extracted from server and stored at index '4' (where '4' changes for each attribute).</td></tr><tr><td>attribute5</td><td>&lt;String></td><td>Read-write</td><td>Name of the custom attribute to be extracted from server and stored at index '5' (where '5' changes for each attribute).</td></tr><tr><td>attribute6</td><td>&lt;String></td><td>Read-write</td><td>Name of the custom attribute to be extracted from server and stored at index '6' (where '6' changes for each attribute).</td></tr><tr><td>attribute7</td><td>&lt;String></td><td>Read-write</td><td>Name of the custom attribute to be extracted from server and stored at index '7' (where '7' changes for each attribute).</td></tr><tr><td>attribute8</td><td>&lt;String></td><td>Read-write</td><td>Name of the custom attribute to be extracted from server and stored at index '8' (where '8' changes for each attribute).</td></tr><tr><td>attribute9</td><td>&lt;String></td><td>Read-write</td><td>Name of the custom attribute to be extracted from server and stored at index '9' (where '9' changes for each attribute).</td></tr><tr><td>attribute10</td><td>&lt;String></td><td>Read-write</td><td>Name of the custom attribute to be extracted from server and stored at index '10' (where '10' changes for each attribute).</td></tr><tr><td>attribute11</td><td>&lt;String></td><td>Read-write</td><td>Name of the custom attribute to be extracted from server and stored at index '11' (where '11' changes for each attribute).</td></tr><tr><td>attribute12</td><td>&lt;String></td><td>Read-write</td><td>Name of the custom attribute to be extracted from server and stored at index '12' (where '12' changes for each attribute).</td></tr><tr><td>attribute13</td><td>&lt;String></td><td>Read-write</td><td>Name of the custom attribute to be extracted from server and stored at index '13' (where '13' changes for each attribute).</td></tr><tr><td>attribute14</td><td>&lt;String></td><td>Read-write</td><td>Name of the custom attribute to be extracted from server and stored at index '14' (where '14' changes for each attribute).</td></tr><tr><td>attribute15</td><td>&lt;String></td><td>Read-write</td><td>Name of the custom attribute to be extracted from server and stored at index '15' (where '15' changes for each attribute).</td></tr><tr><td>attribute16</td><td>&lt;String></td><td>Read-write</td><td>Name of the custom attribute to be extracted from server and stored at index '16' (where '16' changes for each attribute).</td></tr><tr><td>success</td><td>&lt;Double></td><td>Read-only</td><td>.</td></tr><tr><td>failure</td><td>&lt;Double></td><td>Read-only</td><td>.</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD]()| [DELETE](#d)| [UPDATE](#u)| [UNSET](#)| [GET (ALL)](#get-)| [GET]()| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationtacacsaction
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"authenticationtacacsaction":{<b>"name":<String_value>,</b>"serverip":<String_value>,"serverport":<Integer_value>,"authtimeout":<Double_value>,"tacacssecret":<String_value>,"authorization":<String_value>,"accounting":<String_value>,"auditfailedcmds":<String_value>,"groupattrname":<String_value>,"defaultauthenticationgroup":<String_value>,"attribute1":<String_value>,"attribute2":<String_value>,"attribute3":<String_value>,"attribute4":<String_value>,"attribute5":<String_value>,"attribute6":<String_value>,"attribute7":<String_value>,"attribute8":<String_value>,"attribute9":<String_value>,"attribute10":<String_value>,"attribute11":<String_value>,"attribute12":<String_value>,"attribute13":<String_value>,"attribute14":<String_value>,"attribute15":<String_value>,"attribute16":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationtacacsaction/name_value&lt;String&gt;
<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationtacacsaction
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"authenticationtacacsaction":{<b>"name":<String_value>,</b>"serverip":<String_value>,"serverport":<Integer_value>,"authtimeout":<Double_value>,"tacacssecret":<String_value>,"authorization":<String_value>,"accounting":<String_value>,"auditfailedcmds":<String_value>,"groupattrname":<String_value>,"defaultauthenticationgroup":<String_value>,"attribute1":<String_value>,"attribute2":<String_value>,"attribute3":<String_value>,"attribute4":<String_value>,"attribute5":<String_value>,"attribute6":<String_value>,"attribute7":<String_value>,"attribute8":<String_value>,"attribute9":<String_value>,"attribute10":<String_value>,"attribute11":<String_value>,"attribute12":<String_value>,"attribute13":<String_value>,"attribute14":<String_value>,"attribute15":<String_value>,"attribute16":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationtacacsaction?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"authenticationtacacsaction":{<b>"name":<String_value>,</b>"serverip":true,"serverport":true,"authtimeout":true,"tacacssecret":true,"authorization":true,"accounting":true,"auditfailedcmds":true,"groupattrname":true,"defaultauthenticationgroup":true,"attribute1":true,"attribute2":true,"attribute3":true,"attribute4":true,"attribute5":true,"attribute6":true,"attribute7":true,"attribute8":true,"attribute9":true,"attribute10":true,"attribute11":true,"attribute12":true,"attribute13":true,"attribute14":true,"attribute15":true,"attribute16":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationtacacsaction
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationtacacsaction?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationtacacsaction?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of authenticationtacacsaction resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationtacacsaction?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationtacacsaction?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the authenticationtacacsaction resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "authenticationtacacsaction": [ {"name":<String_value>,"serverip":<String_value>,"serverport":<Integer_value>,"authtimeout":<Double_value>,"tacacssecret":<String_value>,"authorization":<String_value>,"accounting":<String_value>,"auditfailedcmds":<String_value>,"groupattrname":<String_value>,"success":<Double_value>,"failure":<Double_value>,"defaultauthenticationgroup":<String_value>,"attribute1":<String_value>,"attribute2":<String_value>,"attribute3":<String_value>,"attribute4":<String_value>,"attribute5":<String_value>,"attribute6":<String_value>,"attribute7":<String_value>,"attribute8":<String_value>,"attribute9":<String_value>,"attribute10":<String_value>,"attribute11":<String_value>,"attribute12":<String_value>,"attribute13":<String_value>,"attribute14":<String_value>,"attribute15":<String_value>,"attribute16":<String_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationtacacsaction/name_value&lt;String&gt;
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationtacacsaction/name_value&lt;String&gt;?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationtacacsaction/name_value&lt;String&gt;?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "authenticationtacacsaction": [ {"name":<String_value>,"serverip":<String_value>,"serverport":<Integer_value>,"authtimeout":<Double_value>,"tacacssecret":<String_value>,"authorization":<String_value>,"accounting":<String_value>,"auditfailedcmds":<String_value>,"groupattrname":<String_value>,"success":<Double_value>,"failure":<Double_value>,"defaultauthenticationgroup":<String_value>,"attribute1":<String_value>,"attribute2":<String_value>,"attribute3":<String_value>,"attribute4":<String_value>,"attribute5":<String_value>,"attribute6":<String_value>,"attribute7":<String_value>,"attribute8":<String_value>,"attribute9":<String_value>,"attribute10":<String_value>,"attribute11":<String_value>,"attribute12":<String_value>,"attribute13":<String_value>,"attribute14":<String_value>,"attribute15":<String_value>,"attribute16":<String_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationtacacsaction?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "authenticationtacacsaction": [ { "__count": "#no"} ] }```



