#snmptrap_snmpuser_binding

Binding object showing the snmpuser that can be bound to snmptrap.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>trapclass</td><td>&lt;String></td><td>Read-write</td><td>Type of trap messages that the NetScaler appliance sends to the trap listener: Generic or the enterprise-specific messages defined in the MIB file.&lt;br>Possible values = generic, specific</td><tr><tr><td>securitylevel</td><td>&lt;String></td><td>Read-write</td><td>Security level of the SNMPv3 trap.&lt;br>Default value: authNoPriv,&lt;br>Possible values = noAuthNoPriv, authNoPriv, authPriv</td><tr><tr><td>username</td><td>&lt;String></td><td>Read-write</td><td>Name of the SNMP user that will send the SNMPv3 traps.</td><tr><tr><td>td</td><td>&lt;Double></td><td>Read-write</td><td>Integer value that uniquely identifies the traffic domain in which you want to configure the entity. If you do not specify an ID, the entity becomes part of the default traffic domain, which has an ID of 0.&lt;br>Minimum value = 0&lt;br>Maximum value = 4094</td><tr><tr><td>trapdestination</td><td>&lt;String></td><td>Read-write</td><td>IPv4 or the IPv6 address of the trap listener to which the NetScaler appliance is to send SNMP trap messages.&lt;br>Minimum length = 1</td><tr><tr><td>version</td><td>&lt;String></td><td>Read-write</td><td>SNMP version, which determines the format of trap messages sent to the trap listener. This setting must match the setting on the trap listener. Otherwise, the listener drops the trap messages.&lt;br>Default value: V3&lt;br>Possible values = V1, V2, V3</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-write</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD:](#add:) | [DELETE:](#delete:) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add:



URL: http://NS_IP/nitro/v1/config
HTTP Method: PUT
Request Payload: ```{"params":{      "warning":<String_value>,      "onerror":<String_value>},sessionid":"##sessionid","snmptrap_snmpuser_binding":{      "trapclass":<String_value>,      "trapdestination":<String_value>,      "td":<Double_value>,      "version":<String_value>,      "username":<String_value>,                  "securitylevel":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete:



URL: http://&lt;NS_IP&gt;/nitro/v1/config/snmptrap_snmpuser_binding/trapclass_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/snmptrap_snmpuser_binding/trapclass_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/snmptrap_snmpuser_binding
Query-parameters:
args
http://&lt;NSIP&gt;/nitro/v1/config/snmptrap_snmpuser_binding?args=      "trapdestination":&lt;String_value&gt;,      "version":&lt;String_value&gt;,      "td":&lt;Double_value&gt;,      "trapclass":&lt;String_value&gt;,
Use this query-parameter to get snmptrap_snmpuser_binding resources based on additional properties.


filter
http://&lt;NS_IP&gt;/nitro/v1/config/snmptrap_snmpuser_binding?filter=property-name1:property-value1,property-name2:property-value2
Use this query-parameter to get the filtered set of snmptrap_snmpuser_binding resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/snmptrap_snmpuser_binding?pagesize=#no;pageno=#no
Use this query-parameter to get the snmptrap_snmpuser_binding resources in chunks.



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "snmptrap_snmpuser_binding": [ {      "trapclass":<String_value>,      "securitylevel":<String_value>,      "username":<String_value>,      "td":<Double_value>,      "trapdestination":<String_value>,      "version":<String_value>,}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/snmptrap_snmpuser_binding?args=     "trapdestination":&lt;String_value&gt;,      "version":&lt;String_value&gt;,      "td":&lt;Double_value&gt;,      "trapclass":&lt;String_value&gt;;count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",snmptrap_snmpuser_binding: [ { "__count": "#no"} ] }


