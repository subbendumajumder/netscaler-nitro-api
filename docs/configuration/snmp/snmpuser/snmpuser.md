#snmpuser

Configuration for SNMP user resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the SNMPv3 user. Can consist of 1 to 31 characters that include uppercase and lowercase letters, numbers, and the hyphen (-), period (.) pound (#), space ( ), at sign (@), equals (=), colon (:), and underscore (_) characters. The following requirement applies only to the NetScaler CLI: If the name includes one or more spaces, enclose it in double or single quotation marks (for example, "my user" or my user).&lt;br>Minimum length = 1</td><tr><tr><td>group</td><td>&lt;String></td><td>Read-write</td><td>Name of the configured SNMPv3 group to which to bind this SNMPv3 user. The access rights (bound SNMPv3 views) and security level set for this group are assigned to this user.&lt;br>Minimum length = 1</td><tr><tr><td>authtype</td><td>&lt;String></td><td>Read-write</td><td>Authentication algorithm used by the NetScaler appliance and the SNMPv3 user for authenticating the communication between them. You must specify the same authentication algorithm when you configure the SNMPv3 user in the SNMP manager.&lt;br>Possible values = MD5, SHA</td><tr><tr><td>authpasswd</td><td>&lt;String></td><td>Read-write</td><td>Plain-text pass phrase to be used by the authentication algorithm specified by the authType (Authentication Type) parameter. Can consist of 1 to 31 characters that include uppercase and lowercase letters, numbers, and the hyphen (-), period (.) pound (#), space ( ), at sign (@), equals (=), colon (:), and underscore (_) characters. The following requirement applies only to the NetScaler CLI: If the pass phrase includes one or more spaces, enclose it in double or single quotation marks (for example, "my phrase" or my phrase).&lt;br>Minimum length = 8</td><tr><tr><td>privtype</td><td>&lt;String></td><td>Read-write</td><td>Encryption algorithm used by the NetScaler appliance and the SNMPv3 user for encrypting the communication between them. You must specify the same encryption algorithm when you configure the SNMPv3 user in the SNMP manager.&lt;br>Possible values = DES, AES</td><tr><tr><td>privpasswd</td><td>&lt;String></td><td>Read-write</td><td>Encryption key to be used by the encryption algorithm specified by the privType (Encryption Type) parameter. Can consist of 1 to 31 characters that include uppercase and lowercase letters, numbers, and the hyphen (-), period (.) pound (#), space ( ), at sign (@), equals (=), colon (:), and underscore (_) characters. The following requirement applies only to the NetScaler CLI: If the key includes one or more spaces, enclose it in double or single quotation marks (for example, "my key" or my key).&lt;br>Minimum length = 8</td><tr><tr><td>engineid</td><td>&lt;String></td><td>Read-only</td><td>The context engine ID of the user.</td><tr><tr><td>storagetype</td><td>&lt;String></td><td>Read-only</td><td>The storage type for this user.&lt;br>Possible values = volatile, nonVolatile</td><tr><tr><td>status</td><td>&lt;String></td><td>Read-only</td><td>The status of this user.&lt;br>Possible values = active</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
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
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>},"sessionid":"##sessionid","snmpuser":{      "name":<String_value>,      "group":<String_value>,      "authtype":<String_value>,                  "authpasswd":<String_value>,      "privtype":<String_value>,                  "privpasswd":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/snmpuser/name_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/snmpuser/name_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","snmpuser":{      "name":<String_value>,      "group":<String_value>,      "authtype":<String_value>,                  "authpasswd":<String_value>,      "privtype":<String_value>,                  "privpasswd":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","snmpuser":{      "name":<String_value>,      "authtype":true,      "privtype":true,      "authpasswd":true,      "privpasswd":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/snmpuser
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/snmpuser?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of snmpuser resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/snmpuser?view=summary
Use this query-parameter to get the summary output of snmpuser resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/snmpuser?pagesize=#no;pageno=#no
Use this query-parameter to get the snmpuser resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/snmpuser?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "snmpuser": [ {      "name":<String_value>,      "group":<String_value>,      "authtype":<String_value>,      "privtype":<String_value>,      "engineid":<String_value>,      "storagetype":<String_value>,      "status":<String_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/snmpuser/name_value&lt;String&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "snmpuser": [ {      "name":<String_value>,      "group":<String_value>,      "authtype":<String_value>,      "privtype":<String_value>,      "engineid":<String_value>,      "storagetype":<String_value>,      "status":<String_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/snmpuser?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",snmpuser: [ { "__count": "#no"} ] }


