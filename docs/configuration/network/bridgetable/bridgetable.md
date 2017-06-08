#bridgetable

Configuration for bridge table entry resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>bridgeage</td><td>&lt;Double></td><td>Read-write</td><td>Time-out value for the bridge table entries, in seconds. The new value applies only to the entries that are dynamically learned after the new value is set. Previously existing bridge table entries expire after the previously configured time-out value.&lt;br>Default value: 300&lt;br>Minimum value = 60&lt;br>Maximum value = 300</td><tr><tr><td>vlan</td><td>&lt;Double></td><td>Read-write</td><td>VLAN whose entries are to be removed.&lt;br>Minimum value = 1&lt;br>Maximum value = 4094</td><tr><tr><td>ifnum</td><td>&lt;String></td><td>Read-write</td><td>INTERFACE whose entries are to be removed.</td><tr><tr><td>vxlan</td><td>&lt;Double></td><td>Read-write</td><td>VXLAN whose entries are to be removed.&lt;br>Minimum value = 1&lt;br>Maximum value = 16777215</td><tr><tr><td>mac</td><td>&lt;String></td><td>Read-only</td><td>The MAC address of the target.</td><tr><tr><td>vtep</td><td>&lt;String></td><td>Read-only</td><td>The IP address of the VTEP.</td><tr><tr><td>flags</td><td>&lt;Double></td><td>Read-only</td><td>Display flags,.</td><tr><tr><td>channel</td><td>&lt;Double></td><td>Read-only</td><td>The Tunnel through which bridge entry is learned.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[UPDATE](#update) | [UNSET](#unset) | [CLEAR](#clear) | [GET (ALL)](#get-(all)) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","bridgetable":{      "bridgeage":<Double_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","bridgetable":{      "bridgeage":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###clear



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"clear"},"sessionid":"##sessionid","bridgetable":{      "vlan":<Double_value>,      "ifnum":<String_value>,      "vxlan":<Double_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/bridgetable
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/bridgetable?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of bridgetable resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/bridgetable?view=summary
Use this query-parameter to get the summary output of bridgetable resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/bridgetable?pagesize=#no;pageno=#no
Use this query-parameter to get the bridgetable resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/bridgetable?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "bridgetable": [ {      "bridgeage":<Double_value>,      "mac":<String_value>,      "ifnum":<String_value>,      "vlan":<Double_value>,      "vxlan":<Double_value>,      "vtep":<String_value>,      "flags":<Double_value>,      "channel":<Double_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/bridgetable?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",bridgetable: [ { "__count": "#no"} ] }


