#lbwlm

Configuration for web log manager resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>wlmname</td><td>&lt;String></td><td>Read-write</td><td>The name of the Work Load Manager.&lt;br>Minimum length = 1</td><tr><tr><td>ipaddress</td><td>&lt;String></td><td>Read-write</td><td>The IP address of the WLM.</td><tr><tr><td>port</td><td>&lt;Integer></td><td>Read-write</td><td>The port of the WLM.&lt;br>Range 1 - 65535</td><tr><tr><td>lbuid</td><td>&lt;String></td><td>Read-write</td><td>The LBUID for the Load Balancer to communicate to the Work Load Manager.</td><tr><tr><td>katimeout</td><td>&lt;Double></td><td>Read-write</td><td>The idle time period after which NS would probe the WLM. The value ranges from 1 to 1440 minutes.&lt;br>Default value: 2&lt;br>Minimum value = 0&lt;br>Maximum value = 1440</td><tr><tr><td>secure</td><td>&lt;String></td><td>Read-only</td><td>Use this parameter to enable secure mode of communication with WLM.&lt;br>Possible values = YES, NO</td><tr><tr><td>state</td><td>&lt;String></td><td>Read-only</td><td>State of the WLM.&lt;br>Possible values = ACTIVE, INACTIVE, UNKNOWN</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [DELETE](#delete) | [UPDATE](#update) | [UNSET](#unset) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>},"sessionid":"##sessionid","lbwlm":{      "wlmname":<String_value>,      "ipaddress":<String_value>,                  "port":<Integer_value>,      "lbuid":<String_value>,      "katimeout":<Double_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/lbwlm/wlmname_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/lbwlm/wlmname_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","lbwlm":{      "wlmname":<String_value>,      "katimeout":<Double_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","lbwlm":{      "wlmname":<String_value>,      "katimeout":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/lbwlm
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/lbwlm?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of lbwlm resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/lbwlm?view=summary
Use this query-parameter to get the summary output of lbwlm resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/lbwlm?pagesize=#no;pageno=#no
Use this query-parameter to get the lbwlm resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/lbwlm?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "lbwlm": [ {      "wlmname":<String_value>,      "ipaddress":<String_value>,      "port":<Integer_value>,      "secure":<String_value>,      "katimeout":<Double_value>,      "lbuid":<String_value>,      "state":<String_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/lbwlm/wlmname_value&lt;String&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "lbwlm": [ {      "wlmname":<String_value>,      "ipaddress":<String_value>,      "port":<Integer_value>,      "secure":<String_value>,      "katimeout":<Double_value>,      "lbuid":<String_value>,      "state":<String_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/lbwlm?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",lbwlm: [ { "__count": "#no"} ] }


