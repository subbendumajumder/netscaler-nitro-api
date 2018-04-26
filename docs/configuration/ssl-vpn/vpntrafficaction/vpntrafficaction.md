#vpntrafficaction

Configuration for VPN traffic action resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the traffic action. Must begin with an ASCII alphabetic or underscore (_) character, and must contain only ASCII alphanumeric, underscore, hash (#), period (.), space, colon (:), at (@), equals (=), and hyphen (-) characters. Cannot be changed after a traffic action is created.<br><br>The following requirement applies only to the NetScaler CLI:<br>If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my action" or 'my action').<br>Minimum length = 1</td></tr><tr><td>qual</td><td>&lt;String></td><td>Read-write</td><td>Protocol, either HTTP or TCP, to be used with the action.<br>Possible values = http, tcp</td></tr><tr><td>apptimeout</td><td>&lt;Double></td><td>Read-write</td><td>Maximum amount of time, in minutes, a user can stay logged on to the web application.<br>Minimum value = 1<br>Maximum value = 715827</td></tr><tr><td>sso</td><td>&lt;String></td><td>Read-write</td><td>Provide single sign-on to the web application.<br>Possible values = ON, OFF</td></tr><tr><td>hdx</td><td>&lt;String></td><td>Read-write</td><td>Provide hdx proxy to the ICA traffic.<br>Possible values = ON, OFF</td></tr><tr><td>formssoaction</td><td>&lt;String></td><td>Read-write</td><td>Name of the form-based single sign-on profile. Form-based single sign-on allows users to log on one time to all protected applications in your network, instead of requiring them to log on separately to access each one.</td></tr><tr><td>fta</td><td>&lt;String></td><td>Read-write</td><td>Specify file type association, which is a list of file extensions that users are allowed to open.<br>Possible values = ON, OFF</td></tr><tr><td>wanscaler</td><td>&lt;String></td><td>Read-write</td><td>Use the Repeater Plug-in to optimize network traffic.<br>Possible values = ON, OFF</td></tr><tr><td>kcdaccount</td><td>&lt;String></td><td>Read-write</td><td>Kerberos constrained delegation account name.<br>Default value: "Default"<br>Minimum length = 1<br>Maximum length = 32</td></tr><tr><td>samlssoprofile</td><td>&lt;String></td><td>Read-write</td><td>Profile to be used for doing SAML SSO to remote relying party.<br>Minimum length = 1</td></tr><tr><td>proxy</td><td>&lt;String></td><td>Read-write</td><td>IP address and Port of the proxy server to be used for HTTP access for this request.<br>Minimum length = 1</td></tr><tr><td>userexpression</td><td>&lt;String></td><td>Read-write</td><td>expression that will be evaluated to obtain username for SingleSignOn.<br>Maximum length = 256</td></tr><tr><td>passwdexpression</td><td>&lt;String></td><td>Read-write</td><td>expression that will be evaluated to obtain password for SingleSignOn.<br>Maximum length = 256</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD]()| [DELETE](#d)| [UPDATE](#u)| [UNSET](#)| [GET (ALL)](#get-)| [GET]()| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpntrafficaction
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"vpntrafficaction":{<b>"name":<String_value>,</b><b>"qual":<String_value>,</b>"apptimeout":<Double_value>,"sso":<String_value>,"hdx":<String_value>,"formssoaction":<String_value>,"fta":<String_value>,"wanscaler":<String_value>,"kcdaccount":<String_value>,"samlssoprofile":<String_value>,"proxy":<String_value>,"userexpression":<String_value>,"passwdexpression":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpntrafficaction/name_value&lt;String&gt;
<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpntrafficaction
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"vpntrafficaction":{<b>"name":<String_value>,</b>"apptimeout":<Double_value>,"sso":<String_value>,"hdx":<String_value>,"formssoaction":<String_value>,"fta":<String_value>,"wanscaler":<String_value>,"kcdaccount":<String_value>,"samlssoprofile":<String_value>,"proxy":<String_value>,"userexpression":<String_value>,"passwdexpression":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpntrafficaction?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"vpntrafficaction":{<b>"name":<String_value>,</b>"wanscaler":true,"kcdaccount":true,"proxy":true,"userexpression":true,"passwdexpression":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpntrafficaction
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpntrafficaction?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpntrafficaction?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of vpntrafficaction resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpntrafficaction?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpntrafficaction?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the vpntrafficaction resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "vpntrafficaction": [ {"name":<String_value>,"qual":<String_value>,"apptimeout":<Double_value>,"sso":<String_value>,"formssoaction":<String_value>,"hdx":<String_value>,"fta":<String_value>,"wanscaler":<String_value>,"kcdaccount":<String_value>,"samlssoprofile":<String_value>,"proxy":<String_value>,"userexpression":<String_value>,"passwdexpression":<String_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpntrafficaction/name_value&lt;String&gt;
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpntrafficaction/name_value&lt;String&gt;?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpntrafficaction/name_value&lt;String&gt;?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "vpntrafficaction": [ {"name":<String_value>,"qual":<String_value>,"apptimeout":<Double_value>,"sso":<String_value>,"formssoaction":<String_value>,"hdx":<String_value>,"fta":<String_value>,"wanscaler":<String_value>,"kcdaccount":<String_value>,"samlssoprofile":<String_value>,"proxy":<String_value>,"userexpression":<String_value>,"passwdexpression":<String_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpntrafficaction?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "vpntrafficaction": [ { "__count": "#no"} ] }```



