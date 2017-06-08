#dnssrvrec

Configuration for server record resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>domain</td><td>&lt;String></td><td>Read-write</td><td>Domain name, which, by convention, is prefixed by the symbolic name of the desired service and the symbolic name of the desired protocol, each with an underscore (_) prepended. For example, if an SRV-aware client wants to discover a SIP service that is provided over UDP, in the domain example.com, the client performs a lookup for _sip._udp.example.com.&lt;br>Minimum length = 1</td><tr><tr><td>target</td><td>&lt;String></td><td>Read-write</td><td>Target host for the specified service.</td><tr><tr><td>priority</td><td>&lt;Double></td><td>Read-write</td><td>Integer specifying the priority of the target host. The lower the number, the higher the priority. If multiple target hosts have the same priority, selection is based on the Weight parameter.&lt;br>Minimum value = 0&lt;br>Maximum value = 65535</td><tr><tr><td>weight</td><td>&lt;Double></td><td>Read-write</td><td>Weight for the target host. Aids host selection when two or more hosts have the same priority. A larger number indicates greater weight.&lt;br>Minimum value = 0&lt;br>Maximum value = 65535</td><tr><tr><td>port</td><td>&lt;Double></td><td>Read-write</td><td>Port on which the target host listens for client requests.&lt;br>Minimum value = 0&lt;br>Maximum value = 65535</td><tr><tr><td>ttl</td><td>&lt;Double></td><td>Read-write</td><td>Time to Live (TTL), in seconds, for the record. TTL is the time for which the record must be cached by DNS proxies. The specified TTL is applied to all the resource records that are of the same record type and belong to the specified domain name. For example, if you add an address record, with a TTL of 36000, to the domain name example.com, the TTLs of all the address records of example.com are changed to 36000. If the TTL is not specified, the NetScaler appliance uses either the DNS zones minimum TTL or, if the SOA record is not available on the appliance, the default value of 3600.&lt;br>Default value: 3600&lt;br>Minimum value = 0&lt;br>Maximum value = 2147483647</td><tr><tr><td>type</td><td>&lt;String></td><td>Read-write</td><td>Type of records to display. Available settings function as follows: * ADNS - Display all authoritative address records. * PROXY - Display all proxy address records. * ALL - Display all address records.&lt;br>Possible values = ALL, ADNS, PROXY</td><tr><tr><td>authtype</td><td>&lt;String></td><td>Read-only</td><td>Record type.&lt;br>Possible values = ALL, ADNS, PROXY</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
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
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>},"sessionid":"##sessionid","dnssrvrec":{      "domain":<String_value>,      "target":<String_value>,      "priority":<Double_value>,      "weight":<Double_value>,      "port":<Double_value>,      "ttl":<Double_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/dnssrvrec/domain_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/dnssrvrec/domain_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","dnssrvrec":{      "domain":<String_value>,      "target":<String_value>,      "priority":<Double_value>,      "weight":<Double_value>,      "port":<Double_value>,      "ttl":<Double_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","dnssrvrec":{      "domain":<String_value>,      "target":<String_value>,      "ttl":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/dnssrvrec
Query-parameters:
args
http://&lt;NSIP&gt;/nitro/v1/config/dnssrvrec?args=      "domain":&lt;String_value&gt;,      "target":&lt;String_value&gt;,      "type":&lt;String_value&gt;,
Use this query-parameter to get dnssrvrec resources based on additional properties.


filter
http://&lt;NSIP&gt;/nitro/v1/config/dnssrvrec?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of dnssrvrec resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/dnssrvrec?view=summary
Use this query-parameter to get the summary output of dnssrvrec resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/dnssrvrec?pagesize=#no;pageno=#no
Use this query-parameter to get the dnssrvrec resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/dnssrvrec?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "dnssrvrec": [ {      "domain":<String_value>,      "target":<String_value>,      "type":<String_value>,      "priority":<Double_value>,      "weight":<Double_value>,      "port":<Double_value>,      "ttl":<Double_value>,      "authtype":<String_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/dnssrvrec?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",dnssrvrec: [ { "__count": "#no"} ] }


