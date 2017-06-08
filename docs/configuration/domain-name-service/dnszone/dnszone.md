#dnszone

Configuration for DNS zone resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>zonename</td><td>&lt;String></td><td>Read-write</td><td>Name of the zone to create.&lt;br>Minimum length = 1</td><tr><tr><td>proxymode</td><td>&lt;String></td><td>Read-write</td><td>Deploy the zone in proxy mode. Enable in the following scenarios: * The load balanced DNS servers are authoritative for the zone and all resource records that are part of the zone. * The load balanced DNS servers are authoritative for the zone, but the NetScaler appliance owns a subset of the resource records that belong to the zone (partial zone ownership configuration). Typically seen in global server load balancing (GSLB) configurations, in which the appliance responds authoritatively to queries for GSLB domain names but forwards queries for other domain names in the zone to the load balanced servers. In either scenario, do not create the zones Start of Authority (SOA) and name server (NS) resource records on the appliance. Disable if the appliance is authoritative for the zone, but make sure that you have created the SOA and NS records on the appliance before you create the zone.&lt;br>Default value: ENABLED&lt;br>Possible values = YES, NO</td><tr><tr><td>dnssecoffload</td><td>&lt;String></td><td>Read-write</td><td>Enable dnssec offload for this zone.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>nsec</td><td>&lt;String></td><td>Read-write</td><td>Enable nsec generation for dnssec offload.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>keyname</td><td>&lt;String[]></td><td>Read-write</td><td>Name of the public/private DNS key pair with which to sign the zone. You can sign a zone with up to four keys.&lt;br>Minimum length = 1</td><tr><tr><td>type</td><td>&lt;String></td><td>Read-write</td><td>Type of zone to display. Mutually exclusive with the DNS Zone (zoneName) parameter. Available settings function as follows: * ADNS - Display all the zones for which the NetScaler appliance is authoritative. * PROXY - Display all the zones for which the NetScaler appliance is functioning as a proxy server. * ALL - Display all the zones configured on the appliance.&lt;br>Possible values = ALL, ADNS, PROXY</td><tr><tr><td>flags</td><td>&lt;Double></td><td>Read-only</td><td>Flags controlling display.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [UPDATE](#update) | [UNSET](#unset) | [DELETE](#delete) | [SIGN](#sign) | [UNSIGN](#unsign) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>},"sessionid":"##sessionid","dnszone":{      "zonename":<String_value>,      "proxymode":<String_value>,                  "dnssecoffload":<String_value>,                  "nsec":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","dnszone":{      "zonename":<String_value>,      "proxymode":<String_value>,                  "dnssecoffload":<String_value>,                  "nsec":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","dnszone":{      "zonename":<String_value>,      "proxymode":true,      "dnssecoffload":true,      "nsec":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/dnszone/zonename_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/dnszone/zonename_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###sign



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"sign"},"sessionid":"##sessionid","dnszone":{      "zonename":<String_value>,      "keyname":<String[]_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unsign



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unsign"},"sessionid":"##sessionid","dnszone":{      "zonename":<String_value>,      "keyname":<String[]_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/dnszone
Query-parameters:
args
http://&lt;NSIP&gt;/nitro/v1/config/dnszone?args=      "zonename":&lt;String_value&gt;,      "type":&lt;String_value&gt;,
Use this query-parameter to get dnszone resources based on additional properties.


filter
http://&lt;NSIP&gt;/nitro/v1/config/dnszone?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of dnszone resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/dnszone?view=summary
Use this query-parameter to get the summary output of dnszone resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/dnszone?pagesize=#no;pageno=#no
Use this query-parameter to get the dnszone resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/dnszone?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "dnszone": [ {      "zonename":<String_value>,      "type":<String_value>,      "proxymode":<String_value>,      "flags":<Double_value>,      "nsecbitarray":<String[]_value>,      "dnssecoffload":<String_value>,      "nsec":<String_value>,      "keyname":<String[]_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/dnszone/zonename_value&lt;String&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "dnszone": [ {      "zonename":<String_value>,      "type":<String_value>,      "proxymode":<String_value>,      "flags":<Double_value>,      "nsecbitarray":<String[]_value>,      "dnssecoffload":<String_value>,      "nsec":<String_value>,      "keyname":<String[]_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/dnszone?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",dnszone: [ { "__count": "#no"} ] }


