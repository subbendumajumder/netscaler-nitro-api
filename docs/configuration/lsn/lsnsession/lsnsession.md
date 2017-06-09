#lsnsession

Configuration for lsn session resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>nattype</td><td>&lt;String></td><td>Read-write</td><td>Type of sessions to be displayed.&lt;br>Default value: NAT44&lt;br>Possible values = NAT44, DS-Lite</td><tr><tr><td>clientname</td><td>&lt;String></td><td>Read-write</td><td>Name of the LSN Client entity.</td><tr><tr><td>network</td><td>&lt;String></td><td>Read-write</td><td>IP address or network address of subscriber(s).</td><tr><tr><td>netmask</td><td>&lt;String></td><td>Read-write</td><td>Subnet mask for the IP address specified by the network parameter.</td><tr><tr><td>network6</td><td>&lt;String></td><td>Read-write</td><td>IPv6 address of the LSN subscriber or B4 device.</td><tr><tr><td>td</td><td>&lt;Double></td><td>Read-write</td><td>Traffic domain ID of the LSN client entity.&lt;br>Default value: 0&lt;br>Minimum value = 0&lt;br>Maximum value = 4094</td><tr><tr><td>natip</td><td>&lt;String></td><td>Read-write</td><td>Mapped NAT IP address used in LSN sessions.</td><tr><tr><td>natport2</td><td>&lt;Integer></td><td>Read-write</td><td>Mapped NAT port used in the LSN sessions.</td><tr><tr><td>natprefix</td><td>&lt;String></td><td>Read-only</td><td>IPv6 address of the LSN subscriber(s) or subscriber network(B4-Device) on whose traffic the NetScaler ADC perform Large Scale NAT.</td><tr><tr><td>subscrip</td><td>&lt;String></td><td>Read-only</td><td>The Source IP address.</td><tr><tr><td>subscrport</td><td>&lt;Integer></td><td>Read-only</td><td>The Source Port.</td><tr><tr><td>destip</td><td>&lt;String></td><td>Read-only</td><td>The Destination IP address.</td><tr><tr><td>destport</td><td>&lt;Integer></td><td>Read-only</td><td>The Destination Port.</td><tr><tr><td>natport</td><td>&lt;Integer></td><td>Read-only</td><td>The NAT Port.</td><tr><tr><td>transportprotocol</td><td>&lt;String></td><td>Read-only</td><td>The Transport Protocol for the session.&lt;br>Possible values = TCP, UDP, ICMP</td><tr><tr><td>sessionestdir</td><td>&lt;String></td><td>Read-only</td><td>The Session establishment direction, session was established for outbound or inbound packet.&lt;br>Possible values = OUT, IN</td><tr><tr><td>dsttd</td><td>&lt;Double></td><td>Read-only</td><td>.</td><tr><tr><td>srctd</td><td>&lt;Double></td><td>Read-only</td><td>.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[FLUSH](#flush) | [GET (ALL)](#get-(all)) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###flush



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"flush"},"sessionid":"##sessionid","lsnsession":{      "nattype":<String_value>,      "clientname":<String_value>,      "network":<String_value>,                  "netmask":<String_value>,      "network6":<String_value>,      "td":<Double_value>,      "natip":<String_value>,                  "natport2":<Integer_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/lsnsession
Query-parameters:
args
http://&lt;NSIP&gt;/nitro/v1/config/lsnsession?args=      "nattype":&lt;String_value&gt;,      "clientname":&lt;String_value&gt;,      "network":&lt;String_value&gt;,                  "netmask":&lt;String_value&gt;,      "network6":&lt;String_value&gt;,      "td":&lt;Double_value&gt;,      "natip":&lt;String_value&gt;,
Use this query-parameter to get lsnsession resources based on additional properties.


filter
http://&lt;NSIP&gt;/nitro/v1/config/lsnsession?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of lsnsession resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/lsnsession?view=summary
Use this query-parameter to get the summary output of lsnsession resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/lsnsession?pagesize=#no;pageno=#no
Use this query-parameter to get the lsnsession resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/lsnsession?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "lsnsession": [ {      "nattype":<String_value>,      "clientname":<String_value>,      "network":<String_value>,                  "netmask":<String_value>,      "network6":<String_value>,      "td":<Double_value>,      "natip":<String_value>,      "natprefix":<String_value>,      "subscrip":<String_value>,      "subscrport":<Integer_value>,      "destip":<String_value>,      "destport":<Integer_value>,      "natport":<Integer_value>,      "transportprotocol":<String_value>,      "sessionestdir":<String_value>,      "dsttd":<Double_value>,      "srctd":<Double_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/lsnsession?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",lsnsession: [ { "__count": "#no"} ] }


