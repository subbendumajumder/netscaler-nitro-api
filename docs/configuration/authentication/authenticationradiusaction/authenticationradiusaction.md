#authenticationradiusaction

Configuration for RADIUS action resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the RADIUS action. Must begin with a letter, number, or the underscore character (_), and must contain only letters, numbers, and the hyphen (-), period (.) pound (#), space ( ), at (@), equals (=), colon (:), and underscore characters. Cannot be changed after the RADIUS action is added.&lt;br>Minimum length = 1</td><tr><tr><td>serverip</td><td>&lt;String></td><td>Read-write</td><td>IP address assigned to the RADIUS server.&lt;br>Minimum length = 1</td><tr><tr><td>servername</td><td>&lt;String></td><td>Read-write</td><td>RADIUS server name as a FQDN. Mutually exclusive with RADIUS IP address.&lt;br>Minimum length = 1</td><tr><tr><td>serverport</td><td>&lt;Integer></td><td>Read-write</td><td>Port number on which the RADIUS server listens for connections.&lt;br>Minimum value = 1</td><tr><tr><td>authtimeout</td><td>&lt;Double></td><td>Read-write</td><td>Number of seconds the NetScaler appliance waits for a response from the RADIUS server.&lt;br>Default value: 3&lt;br>Minimum value = 1</td><tr><tr><td>radkey</td><td>&lt;String></td><td>Read-write</td><td>Key shared between the RADIUS server and the NetScaler appliance. Required to allow the NetScaler appliance to communicate with the RADIUS server.&lt;br>Minimum length = 1</td><tr><tr><td>radnasip</td><td>&lt;String></td><td>Read-write</td><td>If enabled, the NetScaler appliance IP address (NSIP) is sent to the RADIUS server as the Network Access Server IP (NASIP) address. The RADIUS protocol defines the meaning and use of the NASIP address.&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>radnasid</td><td>&lt;String></td><td>Read-write</td><td>If configured, this string is sent to the RADIUS server as the Network Access Server ID (NASID).</td><tr><tr><td>radvendorid</td><td>&lt;Double></td><td>Read-write</td><td>RADIUS vendor ID attribute, used for RADIUS group extraction.&lt;br>Minimum value = 1</td><tr><tr><td>radattributetype</td><td>&lt;Double></td><td>Read-write</td><td>RADIUS attribute type, used for RADIUS group extraction.&lt;br>Minimum value = 1</td><tr><tr><td>radgroupsprefix</td><td>&lt;String></td><td>Read-write</td><td>RADIUS groups prefix string. This groups prefix precedes the group names within a RADIUS attribute for RADIUS group extraction.</td><tr><tr><td>radgroupseparator</td><td>&lt;String></td><td>Read-write</td><td>RADIUS group separator string The group separator delimits group names within a RADIUS attribute for RADIUS group extraction.</td><tr><tr><td>passencoding</td><td>&lt;String></td><td>Read-write</td><td>Encoding type for passwords in RADIUS packets that the NetScaler appliance sends to the RADIUS server.&lt;br>Default value: pap&lt;br>Possible values = pap, chap, mschapv1, mschapv2</td><tr><tr><td>ipvendorid</td><td>&lt;Double></td><td>Read-write</td><td>Vendor ID of the intranet IP attribute in the RADIUS response. NOTE: A value of 0 indicates that the attribute is not vendor encoded.</td><tr><tr><td>ipattributetype</td><td>&lt;Double></td><td>Read-write</td><td>Remote IP address attribute type in a RADIUS response.&lt;br>Minimum value = 1</td><tr><tr><td>accounting</td><td>&lt;String></td><td>Read-write</td><td>Whether the RADIUS server is currently accepting accounting messages.&lt;br>Possible values = ON, OFF</td><tr><tr><td>pwdvendorid</td><td>&lt;Double></td><td>Read-write</td><td>Vendor ID of the attribute, in the RADIUS response, used to extract the user password.&lt;br>Minimum value = 1</td><tr><tr><td>pwdattributetype</td><td>&lt;Double></td><td>Read-write</td><td>Vendor-specific password attribute type in a RADIUS response.&lt;br>Minimum value = 1</td><tr><tr><td>defaultauthenticationgroup</td><td>&lt;String></td><td>Read-write</td><td>This is the default group that is chosen when the authentication succeeds in addition to extracted groups.&lt;br>Maximum length = 64</td><tr><tr><td>callingstationid</td><td>&lt;String></td><td>Read-write</td><td>Send Calling-Station-ID of the client to the RADIUS server. IP Address of the client is sent as its Calling-Station-ID.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>ipaddress</td><td>&lt;String></td><td>Read-only</td><td>IP address.</td><tr><tr><td>success</td><td>&lt;Double></td><td>Read-only</td><td>.</td><tr><tr><td>failure</td><td>&lt;Double></td><td>Read-only</td><td>.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
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
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>},"sessionid":"##sessionid","authenticationradiusaction":{      "name":<String_value>,      "serverip":<String_value>,      "servername":<String_value>,      "serverport":<Integer_value>,      "authtimeout":<Double_value>,      "radkey":<String_value>,      "radnasip":<String_value>,      "radnasid":<String_value>,      "radvendorid":<Double_value>,      "radattributetype":<Double_value>,      "radgroupsprefix":<String_value>,      "radgroupseparator":<String_value>,      "passencoding":<String_value>,      "ipvendorid":<Double_value>,      "ipattributetype":<Double_value>,      "accounting":<String_value>,      "pwdvendorid":<Double_value>,      "pwdattributetype":<Double_value>,      "defaultauthenticationgroup":<String_value>,      "callingstationid":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/authenticationradiusaction/name_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/authenticationradiusaction/name_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","authenticationradiusaction":{      "name":<String_value>,      "serverip":<String_value>,      "servername":<String_value>,      "serverport":<Integer_value>,      "authtimeout":<Double_value>,      "radkey":<String_value>,      "radnasip":<String_value>,      "radnasid":<String_value>,      "radvendorid":<Double_value>,      "radattributetype":<Double_value>,      "radgroupsprefix":<String_value>,      "radgroupseparator":<String_value>,      "passencoding":<String_value>,      "ipvendorid":<Double_value>,      "ipattributetype":<Double_value>,      "accounting":<String_value>,      "pwdvendorid":<Double_value>,                  "pwdattributetype":<Double_value>,      "defaultauthenticationgroup":<String_value>,      "callingstationid":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","authenticationradiusaction":{      "name":<String_value>,      "serverip":true,      "servername":true,      "serverport":true,      "authtimeout":true,      "radnasip":true,      "radnasid":true,      "radvendorid":true,      "radattributetype":true,      "radgroupsprefix":true,      "radgroupseparator":true,      "passencoding":true,      "ipvendorid":true,      "ipattributetype":true,      "accounting":true,      "pwdvendorid":true,      "pwdattributetype":true,      "defaultauthenticationgroup":true,      "callingstationid":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/authenticationradiusaction
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/authenticationradiusaction?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of authenticationradiusaction resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/authenticationradiusaction?view=summary
Use this query-parameter to get the summary output of authenticationradiusaction resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/authenticationradiusaction?pagesize=#no;pageno=#no
Use this query-parameter to get the authenticationradiusaction resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/authenticationradiusaction?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "authenticationradiusaction": [ {      "name":<String_value>,      "serverip":<String_value>,      "servername":<String_value>,      "serverport":<Integer_value>,      "authtimeout":<Double_value>,      "radkey":<String_value>,      "radnasip":<String_value>,      "ipaddress":<String_value>,      "radnasid":<String_value>,      "radvendorid":<Double_value>,      "radattributetype":<Double_value>,      "radgroupsprefix":<String_value>,      "radgroupseparator":<String_value>,      "passencoding":<String_value>,      "ipvendorid":<Double_value>,      "ipattributetype":<Double_value>,      "accounting":<String_value>,      "success":<Double_value>,      "failure":<Double_value>,      "pwdvendorid":<Double_value>,      "pwdattributetype":<Double_value>,      "defaultauthenticationgroup":<String_value>,      "callingstationid":<String_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/authenticationradiusaction/name_value&lt;String&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "authenticationradiusaction": [ {      "name":<String_value>,      "serverip":<String_value>,      "servername":<String_value>,      "serverport":<Integer_value>,      "authtimeout":<Double_value>,      "radkey":<String_value>,      "radnasip":<String_value>,      "ipaddress":<String_value>,      "radnasid":<String_value>,      "radvendorid":<Double_value>,      "radattributetype":<Double_value>,      "radgroupsprefix":<String_value>,      "radgroupseparator":<String_value>,      "passencoding":<String_value>,      "ipvendorid":<Double_value>,      "ipattributetype":<Double_value>,      "accounting":<String_value>,      "success":<Double_value>,      "failure":<Double_value>,      "pwdvendorid":<Double_value>,      "pwdattributetype":<Double_value>,      "defaultauthenticationgroup":<String_value>,      "callingstationid":<String_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/authenticationradiusaction?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",authenticationradiusaction: [ { "__count": "#no"} ] }


