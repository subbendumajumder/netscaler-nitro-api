#nd6ravariables

Configuration for nd6 Router Advertisment configuration variables resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>vlan</td><td>&lt;Double></td><td>Read-write</td><td>The VLAN number.&lt;br>Minimum value = 0&lt;br>Maximum value = 4094</td><tr><tr><td>ceaserouteradv</td><td>&lt;String></td><td>Read-write</td><td>Cease router advertisements on this vlan.&lt;br>Default value: NO&lt;br>Possible values = YES, NO</td><tr><tr><td>sendrouteradv</td><td>&lt;String></td><td>Read-write</td><td>whether the router sends periodic RAs and responds to Router Solicitations.&lt;br>Default value: NO&lt;br>Possible values = YES, NO</td><tr><tr><td>srclinklayeraddroption</td><td>&lt;String></td><td>Read-write</td><td>Include source link layer address option in RA messages.&lt;br>Default value: YES&lt;br>Possible values = YES, NO</td><tr><tr><td>onlyunicastrtadvresponse</td><td>&lt;String></td><td>Read-write</td><td>Send only Unicast Router Advertisements in respond to Router Solicitations.&lt;br>Default value: NO&lt;br>Possible values = YES, NO</td><tr><tr><td>managedaddrconfig</td><td>&lt;String></td><td>Read-write</td><td>Value to be placed in the Managed address configuration flag field.&lt;br>Default value: NO&lt;br>Possible values = YES, NO</td><tr><tr><td>otheraddrconfig</td><td>&lt;String></td><td>Read-write</td><td>Value to be placed in the Other configuration flag field.&lt;br>Default value: NO&lt;br>Possible values = YES, NO</td><tr><tr><td>currhoplimit</td><td>&lt;Double></td><td>Read-write</td><td>Current Hop limit.&lt;br>Default value: 64&lt;br>Minimum value = 0&lt;br>Maximum value = 255</td><tr><tr><td>maxrtadvinterval</td><td>&lt;Double></td><td>Read-write</td><td>Maximum time allowed between unsolicited multicast RAs, in seconds.&lt;br>Default value: 600&lt;br>Minimum value = 4&lt;br>Maximum value = 1800</td><tr><tr><td>minrtadvinterval</td><td>&lt;Double></td><td>Read-write</td><td>Minimum time interval between RA messages, in seconds.&lt;br>Default value: 198&lt;br>Minimum value = 3&lt;br>Maximum value = 1350</td><tr><tr><td>linkmtu</td><td>&lt;Double></td><td>Read-write</td><td>The Link MTU.&lt;br>Default value: 0&lt;br>Minimum value = 0&lt;br>Maximum value = 1500</td><tr><tr><td>reachabletime</td><td>&lt;Double></td><td>Read-write</td><td>Reachable time, in milliseconds.&lt;br>Default value: 0&lt;br>Minimum value = 0&lt;br>Maximum value = 3600000</td><tr><tr><td>retranstime</td><td>&lt;Double></td><td>Read-write</td><td>Retransmission time, in milliseconds.&lt;br>Default value: 0</td><tr><tr><td>defaultlifetime</td><td>&lt;Integer></td><td>Read-write</td><td>Default life time, in seconds.&lt;br>Default value: 1800&lt;br>Minimum value = 0&lt;br>Maximum value = 9000</td><tr><tr><td>lastrtadvtime</td><td>&lt;Double></td><td>Read-only</td><td>Last RA sent timestamp.</td><tr><tr><td>nextrtadvdelay</td><td>&lt;Double></td><td>Read-only</td><td>Next RA delay.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
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
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","nd6ravariables":{      "vlan":<Double_value>,      "ceaserouteradv":<String_value>,      "sendrouteradv":<String_value>,      "srclinklayeraddroption":<String_value>,      "onlyunicastrtadvresponse":<String_value>,      "managedaddrconfig":<String_value>,      "otheraddrconfig":<String_value>,      "currhoplimit":<Double_value>,      "maxrtadvinterval":<Double_value>,      "minrtadvinterval":<Double_value>,      "linkmtu":<Double_value>,      "reachabletime":<Double_value>,      "retranstime":<Double_value>,      "defaultlifetime":<Integer_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","nd6ravariables":{      "vlan":<Double_value>,      "ceaserouteradv":true,      "sendrouteradv":true,      "srclinklayeraddroption":true,      "onlyunicastrtadvresponse":true,      "managedaddrconfig":true,      "otheraddrconfig":true,      "currhoplimit":true,      "maxrtadvinterval":true,      "minrtadvinterval":true,      "linkmtu":true,      "reachabletime":true,      "retranstime":true,      "defaultlifetime":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/nd6ravariables
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/nd6ravariables?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of nd6ravariables resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/nd6ravariables?view=summary
Use this query-parameter to get the summary output of nd6ravariables resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/nd6ravariables?pagesize=#no;pageno=#no
Use this query-parameter to get the nd6ravariables resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/nd6ravariables?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "nd6ravariables": [ {      "vlan":<Double_value>,      "ceaserouteradv":<String_value>,      "sendrouteradv":<String_value>,      "srclinklayeraddroption":<String_value>,      "onlyunicastrtadvresponse":<String_value>,      "managedaddrconfig":<String_value>,      "otheraddrconfig":<String_value>,      "currhoplimit":<Double_value>,      "maxrtadvinterval":<Double_value>,      "minrtadvinterval":<Double_value>,      "linkmtu":<Double_value>,      "reachabletime":<Double_value>,      "retranstime":<Double_value>,      "defaultlifetime":<Integer_value>,      "lastrtadvtime":<Double_value>,      "nextrtadvdelay":<Double_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/nd6ravariables/vlan_value&lt;Double&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "nd6ravariables": [ {      "vlan":<Double_value>,      "ceaserouteradv":<String_value>,      "sendrouteradv":<String_value>,      "srclinklayeraddroption":<String_value>,      "onlyunicastrtadvresponse":<String_value>,      "managedaddrconfig":<String_value>,      "otheraddrconfig":<String_value>,      "currhoplimit":<Double_value>,      "maxrtadvinterval":<Double_value>,      "minrtadvinterval":<Double_value>,      "linkmtu":<Double_value>,      "reachabletime":<Double_value>,      "retranstime":<Double_value>,      "defaultlifetime":<Integer_value>,      "lastrtadvtime":<Double_value>,      "nextrtadvdelay":<Double_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/nd6ravariables?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",nd6ravariables: [ { "__count": "#no"} ] }


