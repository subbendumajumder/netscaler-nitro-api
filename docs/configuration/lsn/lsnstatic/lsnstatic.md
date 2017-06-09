#lsnstatic

Configuration for static mapping resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the LSN static mapping entry. Must begin with an ASCII alphanumeric or underscore (_) character, and must contain only ASCII alphanumeric, underscore, hash (#), period (.), space, colon (:), at (@), equals (=), and hyphen (-) characters. Cannot be changed after the LSN group is created. The following requirement applies only to the NetScaler CLI: If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "lsn static1" or lsn static1).&lt;br>Minimum length = 1&lt;br>Maximum length = 127</td><tr><tr><td>transportprotocol</td><td>&lt;String></td><td>Read-write</td><td>Protocol for the LSN mapping entry.&lt;br>Possible values = TCP, UDP, ICMP</td><tr><tr><td>subscrip</td><td>&lt;String></td><td>Read-write</td><td>IPv4 address of an LSN subscriber for the LSN mapping entry.</td><tr><tr><td>subscrport</td><td>&lt;Integer></td><td>Read-write</td><td>Port of the LSN subscriber for the LSN mapping entry.&lt;br>Minimum value = 0&lt;br>Maximum value = 65535</td><tr><tr><td>td</td><td>&lt;Double></td><td>Read-write</td><td>ID of the traffic domain to which the subscriber belongs. If you do not specify an ID, the subscriber is assumed to be a part of the default traffic domain.&lt;br>Default value: 0&lt;br>Minimum value = 0&lt;br>Maximum value = 4094</td><tr><tr><td>natip</td><td>&lt;String></td><td>Read-write</td><td>IPv4 address, already existing on the NetScaler ADC as type LSN, to be used as NAT IP address for this mapping entry.</td><tr><tr><td>natport</td><td>&lt;Integer></td><td>Read-write</td><td>NAT port for this LSN mapping entry.</td><tr><tr><td>destip</td><td>&lt;String></td><td>Read-write</td><td>Destination IP address for the LSN mapping entry.</td><tr><tr><td>dsttd</td><td>&lt;Double></td><td>Read-write</td><td>ID of the traffic domain through which the destination IP address for this LSN mapping entry is reachable from the NetScaler ADC. If you do not specify an ID, the destination IP address is assumed to be reachable through the default traffic domain, which has an ID of 0.&lt;br>Default value: 0&lt;br>Minimum value = 0&lt;br>Maximum value = 4094</td><tr><tr><td>status</td><td>&lt;String></td><td>Read-only</td><td>The status of the Mapping. Status could be Inactive, if mapping addition failed due to already existing dynamic/static mapping, port allocation failure.&lt;br>Possible values = ACTIVE, INACTIVE</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [DELETE](#delete) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>},"sessionid":"##sessionid","lsnstatic":{      "name":<String_value>,      "transportprotocol":<String_value>,      "subscrip":<String_value>,      "subscrport":<Integer_value>,      "td":<Double_value>,      "natip":<String_value>,      "natport":<Integer_value>,      "destip":<String_value>,      "dsttd":<Double_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/lsnstatic/name_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/lsnstatic/name_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/lsnstatic
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/lsnstatic?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of lsnstatic resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/lsnstatic?view=summary
Use this query-parameter to get the summary output of lsnstatic resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/lsnstatic?pagesize=#no;pageno=#no
Use this query-parameter to get the lsnstatic resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/lsnstatic?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "lsnstatic": [ {      "name":<String_value>,      "transportprotocol":<String_value>,      "subscrip":<String_value>,      "subscrport":<Integer_value>,      "natip":<String_value>,      "natport":<Integer_value>,      "td":<Double_value>,      "destip":<String_value>,      "dsttd":<Double_value>,      "status":<String_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/lsnstatic/name_value&lt;String&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "lsnstatic": [ {      "name":<String_value>,      "transportprotocol":<String_value>,      "subscrip":<String_value>,      "subscrport":<Integer_value>,      "natip":<String_value>,      "natport":<Integer_value>,      "td":<Double_value>,      "destip":<String_value>,      "dsttd":<Double_value>,      "status":<String_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/lsnstatic?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",lsnstatic: [ { "__count": "#no"} ] }


