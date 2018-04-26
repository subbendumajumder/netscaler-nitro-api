#authenticationradiusaction

Configuration for RADIUS action resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the RADIUS action. <br>Must begin with a letter, number, or the underscore character (_), and must contain only letters, numbers, and the hyphen (-), period (.) pound (#), space ( ), at (@), equals (=), colon (:), and underscore characters. Cannot be changed after the RADIUS action is added.<br>Minimum length = 1</td></tr><tr><td>serverip</td><td>&lt;String></td><td>Read-write</td><td>IP address assigned to the RADIUS server.<br>Minimum length = 1</td></tr><tr><td>servername</td><td>&lt;String></td><td>Read-write</td><td>RADIUS server name as a FQDN. Mutually exclusive with RADIUS IP address.<br>Minimum length = 1</td></tr><tr><td>serverport</td><td>&lt;Integer></td><td>Read-write</td><td>Port number on which the RADIUS server listens for connections.<br>Minimum value = 1</td></tr><tr><td>authtimeout</td><td>&lt;Double></td><td>Read-write</td><td>Number of seconds the NetScaler appliance waits for a response from the RADIUS server.<br>Default value: 3<br>Minimum value = 1</td></tr><tr><td>radkey</td><td>&lt;String></td><td>Read-write</td><td>Key shared between the RADIUS server and the NetScaler appliance. <br>Required to allow the NetScaler appliance to communicate with the RADIUS server.<br>Minimum length = 1</td></tr><tr><td>radnasip</td><td>&lt;String></td><td>Read-write</td><td>If enabled, the NetScaler appliance IP address (NSIP) is sent to the RADIUS server as the Network Access Server IP (NASIP) address. <br>The RADIUS protocol defines the meaning and use of the NASIP address.<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>radnasid</td><td>&lt;String></td><td>Read-write</td><td>If configured, this string is sent to the RADIUS server as the Network Access Server ID (NASID).</td></tr><tr><td>radvendorid</td><td>&lt;Double></td><td>Read-write</td><td>RADIUS vendor ID attribute, used for RADIUS group extraction.<br>Minimum value = 1</td></tr><tr><td>radattributetype</td><td>&lt;Double></td><td>Read-write</td><td>RADIUS attribute type, used for RADIUS group extraction.<br>Minimum value = 1</td></tr><tr><td>radgroupsprefix</td><td>&lt;String></td><td>Read-write</td><td>RADIUS groups prefix string. <br>This groups prefix precedes the group names within a RADIUS attribute for RADIUS group extraction.</td></tr><tr><td>radgroupseparator</td><td>&lt;String></td><td>Read-write</td><td>RADIUS group separator string<br>The group separator delimits group names within a RADIUS attribute for RADIUS group extraction.</td></tr><tr><td>passencoding</td><td>&lt;String></td><td>Read-write</td><td>Encoding type for passwords in RADIUS packets that the NetScaler appliance sends to the RADIUS server.<br>Default value: pap<br>Possible values = pap, chap, mschapv1, mschapv2</td></tr><tr><td>ipvendorid</td><td>&lt;Double></td><td>Read-write</td><td>Vendor ID of the intranet IP attribute in the RADIUS response.<br>NOTE: A value of 0 indicates that the attribute is not vendor encoded.</td></tr><tr><td>ipattributetype</td><td>&lt;Double></td><td>Read-write</td><td>Remote IP address attribute type in a RADIUS response.<br>Minimum value = 1</td></tr><tr><td>accounting</td><td>&lt;String></td><td>Read-write</td><td>Whether the RADIUS server is currently accepting accounting messages.<br>Possible values = ON, OFF</td></tr><tr><td>pwdvendorid</td><td>&lt;Double></td><td>Read-write</td><td>Vendor ID of the attribute, in the RADIUS response, used to extract the user password.<br>Minimum value = 1</td></tr><tr><td>pwdattributetype</td><td>&lt;Double></td><td>Read-write</td><td>Vendor-specific password attribute type in a RADIUS response.<br>Minimum value = 1</td></tr><tr><td>defaultauthenticationgroup</td><td>&lt;String></td><td>Read-write</td><td>This is the default group that is chosen when the authentication succeeds in addition to extracted groups.</td></tr><tr><td>callingstationid</td><td>&lt;String></td><td>Read-write</td><td>Send Calling-Station-ID of the client to the RADIUS server. IP Address of the client is sent as its Calling-Station-ID.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>authservretry</td><td>&lt;Double></td><td>Read-write</td><td>Number of retry by the NetScaler appliance before getting response from the RADIUS server.<br>Default value: 3<br>Minimum value = 1<br>Maximum value = 10</td></tr><tr><td>authentication</td><td>&lt;String></td><td>Read-write</td><td>Configure the RADIUS server state to accept or refuse authentication messages.<br>Default value: ON<br>Possible values = ON, OFF</td></tr><tr><td>ipaddress</td><td>&lt;String></td><td>Read-only</td><td>IP address.</td></tr><tr><td>success</td><td>&lt;Double></td><td>Read-only</td><td>.</td></tr><tr><td>failure</td><td>&lt;Double></td><td>Read-only</td><td>.</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD]()| [DELETE](#d)| [UPDATE](#u)| [UNSET](#)| [GET (ALL)](#get-)| [GET]()| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationradiusaction
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"authenticationradiusaction":{<b>"name":<String_value>,</b>"serverip":<String_value>,"servername":<String_value>,"serverport":<Integer_value>,"authtimeout":<Double_value>,<b>"radkey":<String_value>,</b>"radnasip":<String_value>,"radnasid":<String_value>,"radvendorid":<Double_value>,"radattributetype":<Double_value>,"radgroupsprefix":<String_value>,"radgroupseparator":<String_value>,"passencoding":<String_value>,"ipvendorid":<Double_value>,"ipattributetype":<Double_value>,"accounting":<String_value>,"pwdvendorid":<Double_value>,"pwdattributetype":<Double_value>,"defaultauthenticationgroup":<String_value>,"callingstationid":<String_value>,"authservretry":<Double_value>,"authentication":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationradiusaction/name_value&lt;String&gt;
<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationradiusaction
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"authenticationradiusaction":{<b>"name":<String_value>,</b>"serverip":<String_value>,"servername":<String_value>,"serverport":<Integer_value>,"authtimeout":<Double_value>,"radkey":<String_value>,"radnasip":<String_value>,"radnasid":<String_value>,"radvendorid":<Double_value>,"radattributetype":<Double_value>,"radgroupsprefix":<String_value>,"radgroupseparator":<String_value>,"passencoding":<String_value>,"ipvendorid":<Double_value>,"ipattributetype":<Double_value>,"accounting":<String_value>,"pwdvendorid":<Double_value>,"pwdattributetype":<Double_value>,"defaultauthenticationgroup":<String_value>,"callingstationid":<String_value>,"authservretry":<Double_value>,"authentication":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationradiusaction?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"authenticationradiusaction":{<b>"name":<String_value>,</b>"serverport":true,"authtimeout":true,"radnasip":true,"radnasid":true,"radvendorid":true,"radattributetype":true,"radgroupsprefix":true,"radgroupseparator":true,"passencoding":true,"ipvendorid":true,"ipattributetype":true,"accounting":true,"pwdvendorid":true,"pwdattributetype":true,"defaultauthenticationgroup":true,"callingstationid":true,"authservretry":true,"authentication":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationradiusaction
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationradiusaction?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationradiusaction?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of authenticationradiusaction resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationradiusaction?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationradiusaction?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the authenticationradiusaction resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "authenticationradiusaction": [ {"name":<String_value>,"serverip":<String_value>,"servername":<String_value>,"serverport":<Integer_value>,"authtimeout":<Double_value>,"radkey":<String_value>,"radnasip":<String_value>,"ipaddress":<String_value>,"radnasid":<String_value>,"radvendorid":<Double_value>,"radattributetype":<Double_value>,"radgroupsprefix":<String_value>,"radgroupseparator":<String_value>,"passencoding":<String_value>,"ipvendorid":<Double_value>,"ipattributetype":<Double_value>,"accounting":<String_value>,"success":<Double_value>,"failure":<Double_value>,"pwdvendorid":<Double_value>,"pwdattributetype":<Double_value>,"defaultauthenticationgroup":<String_value>,"callingstationid":<String_value>,"authservretry":<Double_value>,"authentication":<String_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationradiusaction/name_value&lt;String&gt;
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationradiusaction/name_value&lt;String&gt;?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationradiusaction/name_value&lt;String&gt;?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "authenticationradiusaction": [ {"name":<String_value>,"serverip":<String_value>,"servername":<String_value>,"serverport":<Integer_value>,"authtimeout":<Double_value>,"radkey":<String_value>,"radnasip":<String_value>,"ipaddress":<String_value>,"radnasid":<String_value>,"radvendorid":<Double_value>,"radattributetype":<Double_value>,"radgroupsprefix":<String_value>,"radgroupseparator":<String_value>,"passencoding":<String_value>,"ipvendorid":<Double_value>,"ipattributetype":<Double_value>,"accounting":<String_value>,"success":<Double_value>,"failure":<Double_value>,"pwdvendorid":<Double_value>,"pwdattributetype":<Double_value>,"defaultauthenticationgroup":<String_value>,"callingstationid":<String_value>,"authservretry":<Double_value>,"authentication":<String_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationradiusaction?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "authenticationradiusaction": [ { "__count": "#no"} ] }```



