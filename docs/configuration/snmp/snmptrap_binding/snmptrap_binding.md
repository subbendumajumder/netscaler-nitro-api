#snmptrap_binding

Binding object which returns the resources bound to snmptrap.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>trapclass</td><td>&lt;String></td><td>Read-write</td><td>Trap type specified in the trap listener entry.&lt;br>Possible values = generic, specific</td><tr><tr><td>trapdestination</td><td>&lt;String></td><td>Read-write</td><td>IP address specified in the trap listener entry.&lt;br>Minimum length = 1</td><tr><tr><td>version</td><td>&lt;String></td><td>Read-write</td><td>The SNMP version of the trap specified in the trap listener entry.&lt;br>Possible values = V1, V2, V3</td><tr><tr><td>td</td><td>&lt;Double></td><td>Read-write</td><td>Integer value that uniquely identifies the traffic domain in which you want to configure the entity. If you do not specify an ID, the entity becomes part of the default traffic domain, which has an ID of 0.&lt;br>Minimum value = 0&lt;br>Maximum value = 4094</td><tr><tr><td>snmptrap_snmpuser_binding</td><td>&lt;snmptrap_snmpuser_binding[]></td><td>Read-only</td><td>snmpuser that can be bound to snmptrap.</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[GET](#get) | [GET (ALL)](#get-(all))


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/snmptrap_binding
Query-parameters:
args
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/snmptrap_binding?args=trapdestination:&lt;String_value&gt;,version:&lt;String_value&gt;,td:&lt;Double_value&gt;,trapclass:&lt;String_value&gt;
Use this query-parameter to get snmptrap_binding resources based on additional properties.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "snmptrap_binding": [ {      "trapdestination":<String_value>,      "version":<String_value>,      "td":<Double_value>,      "trapclass":<String_value>,      "snmptrap_snmpuser_binding":<snmptrap_snmpuser_binding[]_value>}]}```



###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/snmptrap_binding
Query-parameters:
bulkbindings
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/snmptrap_binding?bulkbindings=yes
NITRO allows you to fetch bindings in bulk.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "snmptrap_binding": [ {      "trapdestination":<String_value>,      "version":<String_value>,      "td":<Double_value>,      "trapclass":<String_value>,      "snmptrap_snmpuser_binding":<snmptrap_snmpuser_binding[]_value>}]}```



