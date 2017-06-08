#vpntrafficaction

Configuration for VPN traffic action resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the traffic action. Must begin with an ASCII alphabetic or underscore (_) character, and must contain only ASCII alphanumeric, underscore, hash (#), period (.), space, colon (:), at (@), equals (=), and hyphen (-) characters. Cannot be changed after a traffic action is created. The following requirement applies only to the NetScaler CLI: If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my action" or my action).&lt;br>Minimum length = 1</td><tr><tr><td>qual</td><td>&lt;String></td><td>Read-write</td><td>Protocol, either HTTP or TCP, to be used with the action.&lt;br>Possible values = http, tcp</td><tr><tr><td>apptimeout</td><td>&lt;Double></td><td>Read-write</td><td>Maximum amount of time, in minutes, a user can stay logged on to the web application.&lt;br>Minimum value = 1&lt;br>Maximum value = 715827</td><tr><tr><td>sso</td><td>&lt;String></td><td>Read-write</td><td>Provide single sign-on to the web application.&lt;br>Possible values = ON, OFF</td><tr><tr><td>hdx</td><td>&lt;String></td><td>Read-write</td><td>Provide hdx proxy to the ICA traffic.&lt;br>Possible values = ON, OFF</td><tr><tr><td>formssoaction</td><td>&lt;String></td><td>Read-write</td><td>Name of the form-based single sign-on profile. Form-based single sign-on allows users to log on one time to all protected applications in your network, instead of requiring them to log on separately to access each one.</td><tr><tr><td>fta</td><td>&lt;String></td><td>Read-write</td><td>Specify file type association, which is a list of file extensions that users are allowed to open.&lt;br>Possible values = ON, OFF</td><tr><tr><td>wanscaler</td><td>&lt;String></td><td>Read-write</td><td>Use the Repeater Plug-in to optimize network traffic.&lt;br>Possible values = ON, OFF</td><tr><tr><td>kcdaccount</td><td>&lt;String></td><td>Read-write</td><td>Kerberos constrained delegation account name.&lt;br>Default value: "Default"&lt;br>Minimum length = 1&lt;br>Maximum length = 32</td><tr><tr><td>samlssoprofile</td><td>&lt;String></td><td>Read-write</td><td>Profile to be used for doing SAML SSO to remote relying party.&lt;br>Minimum length = 1</td><tr><tr><td>proxy</td><td>&lt;String></td><td>Read-write</td><td>IP address and Port of the proxy server to be used for HTTP access for this request.&lt;br>Minimum length = 1</td><tr><tr><td>userexpression</td><td>&lt;String></td><td>Read-write</td><td>expression that will be evaluated to obtain username for SingleSignOn.&lt;br>Maximum length = 256</td><tr><tr><td>passwdexpression</td><td>&lt;String></td><td>Read-write</td><td>expression that will be evaluated to obtain password for SingleSignOn.&lt;br>Maximum length = 256</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [DELETE](#delete) | [UPDATE](#update) | [UNSET](#unset) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>},"sessionid":"##sessionid","vpntrafficaction":{      "name":<String_value>,      "qual":<String_value>,      "apptimeout":<Double_value>,      "sso":<String_value>,      "hdx":<String_value>,      "formssoaction":<String_value>,      "fta":<String_value>,      "wanscaler":<String_value>,      "kcdaccount":<String_value>,      "samlssoprofile":<String_value>,      "proxy":<String_value>,      "userexpression":<String_value>,      "passwdexpression":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/vpntrafficaction/name_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/vpntrafficaction/name_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","vpntrafficaction":{      "name":<String_value>,      "apptimeout":<Double_value>,      "sso":<String_value>,      "hdx":<String_value>,      "formssoaction":<String_value>,      "fta":<String_value>,      "wanscaler":<String_value>,      "kcdaccount":<String_value>,      "samlssoprofile":<String_value>,      "proxy":<String_value>,      "userexpression":<String_value>,      "passwdexpression":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","vpntrafficaction":{      "name":<String_value>,      "wanscaler":true,      "kcdaccount":true,      "proxy":true,      "userexpression":true,      "passwdexpression":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/vpntrafficaction
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/vpntrafficaction?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of vpntrafficaction resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/vpntrafficaction?view=summary
Use this query-parameter to get the summary output of vpntrafficaction resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/vpntrafficaction?pagesize=#no;pageno=#no
Use this query-parameter to get the vpntrafficaction resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/vpntrafficaction?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "vpntrafficaction": [ {      "name":<String_value>,      "qual":<String_value>,      "apptimeout":<Double_value>,      "sso":<String_value>,      "formssoaction":<String_value>,      "hdx":<String_value>,      "fta":<String_value>,      "wanscaler":<String_value>,      "kcdaccount":<String_value>,      "samlssoprofile":<String_value>,      "proxy":<String_value>,      "userexpression":<String_value>,      "passwdexpression":<String_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/vpntrafficaction/name_value&lt;String&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "vpntrafficaction": [ {      "name":<String_value>,      "qual":<String_value>,      "apptimeout":<Double_value>,      "sso":<String_value>,      "formssoaction":<String_value>,      "hdx":<String_value>,      "fta":<String_value>,      "wanscaler":<String_value>,      "kcdaccount":<String_value>,      "samlssoprofile":<String_value>,      "proxy":<String_value>,      "userexpression":<String_value>,      "passwdexpression":<String_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/vpntrafficaction?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",vpntrafficaction: [ { "__count": "#no"} ] }


