#riseapbrsvc

Configuration for RISE Apbr services resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-only</td><td>Name for the APBR service.</td><tr><tr><td>risesvctype</td><td>&lt;String></td><td>Read-only</td><td>Service or Service Group.&lt;br>Possible values = Service, ServiceGroup</td><tr><tr><td>serverip</td><td>&lt;String></td><td>Read-only</td><td>Server IP for APBR service.</td><tr><tr><td>nexthopip</td><td>&lt;String></td><td>Read-only</td><td>Nexthop IP for APBR service.</td><tr><tr><td>vlan</td><td>&lt;Double></td><td>Read-only</td><td>Vlan id for APBR service.</td><tr><tr><td>protocol</td><td>&lt;String></td><td>Read-only</td><td>Protocol type for APBR service.&lt;br>Possible values = HTTP, FTP, TCP, UDP, SSL, SSL_BRIDGE, SSL_TCP, DTLS, NNTP, RPCSVR, DNS, ADNS, SNMP, RTSP, DHCPRA, ANY, SIP_UDP, DNS_TCP, ADNS_TCP, MYSQL, MSSQL, ORACLE, RADIUS, RDP, DIAMETER, SSL_DIAMETER, TFTP</td><tr><tr><td>serverport</td><td>&lt;Integer></td><td>Read-only</td><td>Server port for APBR service.&lt;br>Range 1 - 65535</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[GET (ALL)](#get-(all)) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/riseapbrsvc
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/riseapbrsvc?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of riseapbrsvc resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/riseapbrsvc?view=summary
Use this query-parameter to get the summary output of riseapbrsvc resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/riseapbrsvc?pagesize=#no;pageno=#no
Use this query-parameter to get the riseapbrsvc resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/riseapbrsvc?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "riseapbrsvc": [ {      "name":<String_value>,      "risesvctype":<String_value>,      "serverip":<String_value>,      "nexthopip":<String_value>,      "vlan":<Double_value>,      "protocol":<String_value>,      "serverport":<Integer_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/riseapbrsvc?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",riseapbrsvc: [ { "__count": "#no"} ] }


