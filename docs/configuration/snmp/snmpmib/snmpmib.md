#snmpmib

Configuration for SNMP mib resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>contact</td><td>&lt;String></td><td>Read-write</td><td>Name of the administrator for this NetScaler appliance. Along with the name, you can include information on how to contact this person, such as a phone number or an email address. Can consist of 1 to 127 characters that include uppercase and lowercase letters, numbers, and the hyphen (-), period (.) pound (#), space ( ), at sign (@), equals (=), colon (:), and underscore (_) characters. The following requirement applies only to the NetScaler CLI: If the information includes one or more spaces, enclose it in double or single quotation marks (for example, "my contact" or my contact).&lt;br>Default value: "WebMaster (default)"&lt;br>Minimum length = 1</td><tr><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for this NetScaler appliance. Can consist of 1 to 127 characters that include uppercase and lowercase letters, numbers, and the hyphen (-), period (.) pound (#), space ( ), at sign (@), equals (=), colon (:), and underscore (_) characters. You should choose a name that helps identify the NetScaler appliance. The following requirement applies only to the NetScaler CLI: If the name includes one or more spaces, enclose it in double or single quotation marks (for example, "my name" or my name).&lt;br>Default value: "NetScaler"&lt;br>Minimum length = 1</td><tr><tr><td>location</td><td>&lt;String></td><td>Read-write</td><td>Physical location of the NetScaler appliance. For example, you can specify building name, lab number, and rack number. Can consist of 1 to 127 characters that include uppercase and lowercase letters, numbers, and the hyphen (-), period (.) pound (#), space ( ), at sign (@), equals (=), colon (:), and underscore (_) characters. The following requirement applies only to the NetScaler CLI: If the location includes one or more spaces, enclose it in double or single quotation marks (for example, "my location" or my location).&lt;br>Default value: "POP (default)"&lt;br>Minimum length = 1</td><tr><tr><td>customid</td><td>&lt;String></td><td>Read-write</td><td>Custom identification number for the NetScaler appliance. Can consist of 1 to 127 characters that include uppercase and lowercase letters, numbers, and the hyphen (-), period (.) pound (#), space ( ), at sign (@), equals (=), colon (:), and underscore (_) characters. You should choose a custom identification that helps identify the NetScaler appliance. The following requirement applies only to the NetScaler CLI: If the ID includes one or more spaces, enclose it in double or single quotation marks (for example, "my ID" or my ID).&lt;br>Default value: "Default"&lt;br>Minimum length = 1</td><tr><tr><td>sysdesc</td><td>&lt;String></td><td>Read-only</td><td>The description of the system.</td><tr><tr><td>sysuptime</td><td>&lt;Double></td><td>Read-only</td><td>The UP time of the system in 100th of a second.</td><tr><tr><td>sysservices</td><td>&lt;Double></td><td>Read-only</td><td>The services offered by the system.</td><tr><tr><td>sysoid</td><td>&lt;String></td><td>Read-only</td><td>The OID of the systems management system.</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[UPDATE](#update) | [UNSET](#unset) | [GET (ALL)](#get-(all))


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","snmpmib":{      "contact":<String_value>,      "name":<String_value>,      "location":<String_value>,      "customid":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","snmpmib":{      "contact":true,      "name":true,      "location":true,      "customid":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/snmpmib
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "snmpmib": [ {      "contact":<String_value>,      "name":<String_value>,      "location":<String_value>,      "sysdesc":<String_value>,      "sysuptime":<Double_value>,      "sysservices":<Double_value>,      "sysoid":<String_value>,      "customid":<String_value>}]}```



