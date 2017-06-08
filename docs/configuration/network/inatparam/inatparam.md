#inatparam

Configuration for INAT parameter resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>nat46v6prefix</td><td>&lt;String></td><td>Read-write</td><td>The prefix used for translating packets received from private IPv6 servers into IPv4 packets. This prefix has a length of 96 bits (128-32 = 96). The IPv6 servers embed the destination IP address of the IPv4 servers or hosts in the last 32 bits of the destination IP address field of the IPv6 packets. The first 96 bits of the destination IP address field are set as the IPv6 NAT prefix. IPv6 packets addressed to this prefix have to be routed to the NetScaler appliance to ensure that the IPv6-IPv4 translation is done by the appliance.</td><tr><tr><td>td</td><td>&lt;Double></td><td>Read-write</td><td>Integer value that uniquely identifies the traffic domain in which you want to configure the entity. If you do not specify an ID, the entity becomes part of the default traffic domain, which has an ID of 0.&lt;br>Minimum value = 0&lt;br>Maximum value = 4094</td><tr><tr><td>nat46ignoretos</td><td>&lt;String></td><td>Read-write</td><td>Ignore TOS.&lt;br>Default value: NO&lt;br>Possible values = YES, NO</td><tr><tr><td>nat46zerochecksum</td><td>&lt;String></td><td>Read-write</td><td>Calculate checksum for UDP packets with zero checksum.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>nat46v6mtu</td><td>&lt;Double></td><td>Read-write</td><td>MTU setting for the IPv6 side. If the incoming IPv4 packet greater than this, either fragment or send icmp need fragmentation error.&lt;br>Default value: 1280&lt;br>Minimum value = 1280&lt;br>Maximum value = 9216</td><tr><tr><td>nat46fragheader</td><td>&lt;String></td><td>Read-write</td><td>When disabled, translator will not insert IPv6 fragmentation header for non fragmented IPv4 packets.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[UPDATE](#update) | [UNSET](#unset) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","inatparam":{      "nat46v6prefix":<String_value>,                  "td":<Double_value>,      "nat46ignoretos":<String_value>,      "nat46zerochecksum":<String_value>,      "nat46v6mtu":<Double_value>,      "nat46fragheader":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","inatparam":{      "nat46v6prefix":true,                  "td":<Double_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/inatparam
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/inatparam?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of inatparam resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/inatparam?view=summary
Use this query-parameter to get the summary output of inatparam resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/inatparam?pagesize=#no;pageno=#no
Use this query-parameter to get the inatparam resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/inatparam?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "inatparam": [ {      "td":<Double_value>,      "nat46v6prefix":<String_value>,      "nat46ignoretos":<String_value>,      "nat46zerochecksum":<String_value>,      "nat46v6mtu":<Double_value>,      "nat46fragheader":<String_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/inatparam/td_value&lt;Double&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "inatparam": [ {      "td":<Double_value>,      "nat46v6prefix":<String_value>,      "nat46ignoretos":<String_value>,      "nat46zerochecksum":<String_value>,      "nat46v6mtu":<Double_value>,      "nat46fragheader":<String_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/inatparam?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",inatparam: [ { "__count": "#no"} ] }


