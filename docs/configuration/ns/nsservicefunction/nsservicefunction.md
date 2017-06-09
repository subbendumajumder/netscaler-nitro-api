#nsservicefunction

Configuration for service Function resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>servicefunctionname</td><td>&lt;String></td><td>Read-write</td><td>Name of the service function to be created. Leading character must be a number or letter. Other characters allowed, after the first character, are @ _ - . (period) : (colon) # and space ( ).&lt;br>Minimum length = 1</td><tr><tr><td>ingressvlan</td><td>&lt;Double></td><td>Read-write</td><td>VLAN ID on which the traffic from service function reaches Netscaler.&lt;br>Minimum value = 1&lt;br>Maximum value = 4094</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [UPDATE](#update) | [DELETE](#delete) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>},"sessionid":"##sessionid","nsservicefunction":{      "servicefunctionname":<String_value>,      "ingressvlan":<Double_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","nsservicefunction":{      "servicefunctionname":<String_value>,      "ingressvlan":<Double_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/nsservicefunction/servicefunctionname_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/nsservicefunction/servicefunctionname_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/nsservicefunction
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/nsservicefunction?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of nsservicefunction resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/nsservicefunction?view=summary
Use this query-parameter to get the summary output of nsservicefunction resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/nsservicefunction?pagesize=#no;pageno=#no
Use this query-parameter to get the nsservicefunction resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/nsservicefunction?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "nsservicefunction": [ {      "servicefunctionname":<String_value>,      "ingressvlan":<Double_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/nsservicefunction/servicefunctionname_value&lt;String&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "nsservicefunction": [ {      "servicefunctionname":<String_value>,      "ingressvlan":<Double_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/nsservicefunction?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",nsservicefunction: [ { "__count": "#no"} ] }


