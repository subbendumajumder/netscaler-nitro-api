#snmptrap

Configuration for snmp trap resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>trapclass</td><td>&lt;String></td><td>Read-write</td><td>Type of trap messages that the NetScaler appliance sends to the trap listener: Generic or the enterprise-specific messages defined in the MIB file.&lt;br>Possible values = generic, specific</td><tr><tr><td>trapdestination</td><td>&lt;String></td><td>Read-write</td><td>IPv4 or the IPv6 address of the trap listener to which the NetScaler appliance is to send SNMP trap messages.&lt;br>Minimum length = 1</td><tr><tr><td>version</td><td>&lt;String></td><td>Read-write</td><td>SNMP version, which determines the format of trap messages sent to the trap listener. This setting must match the setting on the trap listener. Otherwise, the listener drops the trap messages.&lt;br>Default value: V2&lt;br>Possible values = V1, V2, V3</td><tr><tr><td>td</td><td>&lt;Double></td><td>Read-write</td><td>Integer value that uniquely identifies the traffic domain in which you want to configure the entity. If you do not specify an ID, the entity becomes part of the default traffic domain, which has an ID of 0.&lt;br>Minimum value = 0&lt;br>Maximum value = 4094</td><tr><tr><td>destport</td><td>&lt;Integer></td><td>Read-write</td><td>UDP port at which the trap listener listens for trap messages. This setting must match the setting on the trap listener. Otherwise, the listener drops the trap messages.&lt;br>Default value: 162&lt;br>Minimum value = 1&lt;br>Maximum value = 65534</td><tr><tr><td>communityname</td><td>&lt;String></td><td>Read-write</td><td>Password (string) sent with the trap messages, so that the trap listener can authenticate them. Can include 1 to 31 uppercase or lowercase letters, numbers, and hyphen (-), period (.) pound (#), space ( ), at (@), equals (=), colon (:), and underscore (_) characters. You must specify the same community string on the trap listener device. Otherwise, the trap listener drops the trap messages. The following requirement applies only to the NetScaler CLI: If the string includes one or more spaces, enclose the name in double or single quotation marks (for example, "my string" or my string).</td><tr><tr><td>srcip</td><td>&lt;String></td><td>Read-write</td><td>IPv4 or IPv6 address that the NetScaler appliance inserts as the source IP address in all SNMP trap messages that it sends to this trap listener. By default this is the appliances NSIP or NSIP6 address, but you can specify an IPv4 MIP or SNIP address or a SNIP6 address.&lt;br>Minimum length = 1</td><tr><tr><td>severity</td><td>&lt;String></td><td>Read-write</td><td>Severity level at or above which the NetScaler appliance sends trap messages to this trap listener. The severity levels, in increasing order of severity, are Informational, Warning, Minor, Major, Critical. This parameter can be set for trap listeners of type SPECIFIC only. The default is to send all levels of trap messages. Important: Trap messages are not assigned severity levels unless you specify severity levels when configuring SNMP alarms.&lt;br>Default value: Unknown&lt;br>Possible values = Critical, Major, Minor, Warning, Informational</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [DELETE](#delete) | [UPDATE](#update) | [UNSET](#unset) | [GET (ALL)](#get-(all)) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>},"sessionid":"##sessionid","snmptrap":{      "trapclass":<String_value>,      "trapdestination":<String_value>,      "version":<String_value>,      "td":<Double_value>,      "destport":<Integer_value>,      "communityname":<String_value>,      "srcip":<String_value>,      "severity":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/snmptrap/trapclass_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/snmptrap/trapclass_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","snmptrap":{      "trapclass":<String_value>,      "trapdestination":<String_value>,      "version":<String_value>,      "td":<Double_value>,      "destport":<Integer_value>,      "communityname":<String_value>,      "srcip":<String_value>,      "severity":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","snmptrap":{      "trapclass":<String_value>,      "trapdestination":<String_value>,      "version":<String_value>,      "td":<Double_value>,      "destport":true,      "communityname":true,      "srcip":true,      "severity":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/snmptrap
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/snmptrap?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of snmptrap resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/snmptrap?view=summary
Use this query-parameter to get the summary output of snmptrap resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/snmptrap?pagesize=#no;pageno=#no
Use this query-parameter to get the snmptrap resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/snmptrap?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "snmptrap": [ {      "trapclass":<String_value>,                  "trapdestination":<String_value>,                  "version":<String_value>,                  "td":<Double_value>,      "destport":<Integer_value>,      "communityname":<String_value>,      "srcip":<String_value>,      "severity":<String_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/snmptrap?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",snmptrap: [ { "__count": "#no"} ] }


