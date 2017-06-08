#lbpersistentsessions

Configuration for persistence session resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>vserver</td><td>&lt;String></td><td>Read-write</td><td>The name of the virtual server.</td><tr><tr><td>persistenceparameter</td><td>&lt;String></td><td>Read-write</td><td>The persistence parameter whose persistence sessions are to be flushed.</td><tr><tr><td>type</td><td>&lt;Double></td><td>Read-only</td><td>Type of Persistence.</td><tr><tr><td>typestring</td><td>&lt;String></td><td>Read-only</td><td>Type of Persistence as String.</td><tr><tr><td>srcip</td><td>&lt;String></td><td>Read-only</td><td>SOURCE IP.</td><tr><tr><td>srcipv6</td><td>&lt;String></td><td>Read-only</td><td>SOURCE IPv6 ADDRESS.</td><tr><tr><td>destip</td><td>&lt;String></td><td>Read-only</td><td>DESTINATION IP.</td><tr><tr><td>destipv6</td><td>&lt;String></td><td>Read-only</td><td>DESTINATION IPv6 ADDRESS.</td><tr><tr><td>flags</td><td>&lt;Boolean></td><td>Read-only</td><td>IPv6 FLAGS.</td><tr><tr><td>destport</td><td>&lt;Integer></td><td>Read-only</td><td>Destination port.&lt;br>Range 1 - 65535</td><tr><tr><td>vservername</td><td>&lt;String></td><td>Read-only</td><td>Virtual server name.</td><tr><tr><td>timeout</td><td>&lt;Double></td><td>Read-only</td><td>Persistent Session timeout.</td><tr><tr><td>referencecount</td><td>&lt;Double></td><td>Read-only</td><td>Reference Count.</td><tr><tr><td>persistenceparam</td><td>&lt;String></td><td>Read-only</td><td>Specific persistence information . Callid in case of SIP_CALLID persistence entry , RTSP session id in case of RTSP_SESSIONID persistence entry.</td><tr><tr><td>cnamepersparam</td><td>&lt;String></td><td>Read-only</td><td>The cname that is selected incase of gslb service.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[CLEAR](#clear) | [GET (ALL)](#get-(all)) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###clear



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"clear"},"sessionid":"##sessionid","lbpersistentsessions":{      "vserver":<String_value>,      "persistenceparameter":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/lbpersistentsessions
Query-parameters:
args
http://&lt;NSIP&gt;/nitro/v1/config/lbpersistentsessions?args=      "vserver":&lt;String_value&gt;,
Use this query-parameter to get lbpersistentsessions resources based on additional properties.


filter
http://&lt;NSIP&gt;/nitro/v1/config/lbpersistentsessions?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of lbpersistentsessions resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/lbpersistentsessions?view=summary
Use this query-parameter to get the summary output of lbpersistentsessions resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/lbpersistentsessions?pagesize=#no;pageno=#no
Use this query-parameter to get the lbpersistentsessions resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/lbpersistentsessions?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "lbpersistentsessions": [ {      "vserver":<String_value>,      "type":<Double_value>,      "typestring":<String_value>,      "srcip":<String_value>,      "srcipv6":<String_value>,      "destip":<String_value>,      "destipv6":<String_value>,      "flags":<Boolean_value>,      "destport":<Integer_value>,      "vservername":<String_value>,      "timeout":<Double_value>,      "referencecount":<Double_value>,      "sipcallid":<String_value>,      "persistenceparam":<String_value>,      "cnamepersparam":<String_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/lbpersistentsessions?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",lbpersistentsessions: [ { "__count": "#no"} ] }


