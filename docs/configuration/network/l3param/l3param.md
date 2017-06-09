#l3param

Configuration for Layer 3 related parameter resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>srcnat</td><td>&lt;String></td><td>Read-write</td><td>Perform NAT if only the source is in the private network.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>icmpgenratethreshold</td><td>&lt;Double></td><td>Read-write</td><td>NS generated ICMP pkts per 10ms rate threshold.&lt;br>Default value: 100</td><tr><tr><td>overridernat</td><td>&lt;String></td><td>Read-write</td><td>USNIP/USIP settings override RNAT settings for configured service/virtual server traffic.. .&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>dropdfflag</td><td>&lt;String></td><td>Read-write</td><td>Enable dropping the IP DF flag.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>miproundrobin</td><td>&lt;String></td><td>Read-write</td><td>Enable round robin usage of mapped IPs.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>externalloopback</td><td>&lt;String></td><td>Read-write</td><td>Enable external loopback.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>tnlpmtuwoconn</td><td>&lt;String></td><td>Read-write</td><td>Enable external loopback.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>usipserverstraypkt</td><td>&lt;String></td><td>Read-write</td><td>Enable detection of stray server side pkts in USIP mode.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>forwardicmpfragments</td><td>&lt;String></td><td>Read-write</td><td>Enable forwarding of ICMP fragments.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>dropipfragments</td><td>&lt;String></td><td>Read-write</td><td>Enable dropping of IP fragments.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>acllogtime</td><td>&lt;Double></td><td>Read-write</td><td>Parameter to tune acl logging time.&lt;br>Default value: 5000</td><tr><tr><td>icmperrgenerate</td><td>&lt;String></td><td>Read-write</td><td>Enable/Disable fragmentation required icmp error generation, before encapsulating a packet with vPath header. This knob is only functional for vPath Environment.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>overridelsn</td><td>&lt;String></td><td>Read-write</td><td>USNIP/USIP settings override LSN settings for configured service/virtual server traffic.. .&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>implicitaclallow</td><td>&lt;String></td><td>Read-write</td><td>Do not apply ACLs for internal ports.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>dynamicrouting</td><td>&lt;String></td><td>Read-write</td><td>Enable/Disable Dynamic routing on partition.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[UPDATE](#update) | [UNSET](#unset) | [GET (ALL)](#get-(all))


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","l3param":{      "srcnat":<String_value>,      "icmpgenratethreshold":<Double_value>,      "overridernat":<String_value>,      "dropdfflag":<String_value>,      "miproundrobin":<String_value>,      "externalloopback":<String_value>,      "tnlpmtuwoconn":<String_value>,      "usipserverstraypkt":<String_value>,      "forwardicmpfragments":<String_value>,      "dropipfragments":<String_value>,      "acllogtime":<Double_value>,      "icmperrgenerate":<String_value>,      "overridelsn":<String_value>,      "implicitaclallow":<String_value>,      "dynamicrouting":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","l3param":{      "srcnat":true,      "icmpgenratethreshold":true,      "overridernat":true,      "dropdfflag":true,      "miproundrobin":true,      "externalloopback":true,      "tnlpmtuwoconn":true,      "usipserverstraypkt":true,      "forwardicmpfragments":true,      "dropipfragments":true,      "acllogtime":true,      "icmperrgenerate":true,      "overridelsn":true,      "implicitaclallow":true,      "dynamicrouting":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/l3param
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "l3param": [ {      "srcnat":<String_value>,      "icmpgenratethreshold":<Double_value>,      "overridernat":<String_value>,      "dropdfflag":<String_value>,      "miproundrobin":<String_value>,      "externalloopback":<String_value>,      "tnlpmtuwoconn":<String_value>,      "usipserverstraypkt":<String_value>,      "forwardicmpfragments":<String_value>,      "dropipfragments":<String_value>,      "acllogtime":<Double_value>,      "icmperrgenerate":<String_value>,      "overridelsn":<String_value>,      "implicitaclallow":<String_value>,      "dynamicrouting":<String_value>}]}```



