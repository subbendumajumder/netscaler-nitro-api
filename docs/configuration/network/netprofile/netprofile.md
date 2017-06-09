#netprofile

Configuration for Network profile resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the net profile. Must begin with a letter, number, or the underscore character (_), and can consist of letters, numbers, and the hyphen (-), period (.) pound (#), space ( ), at sign (@), equals (=), colon (:), and underscore characters. Cannot be changed after the profile is created. Choose a name that helps identify the net profile.&lt;br>Minimum length = 1</td><tr><tr><td>td</td><td>&lt;Double></td><td>Read-write</td><td>Integer value that uniquely identifies the traffic domain in which you want to configure the entity. If you do not specify an ID, the entity becomes part of the default traffic domain, which has an ID of 0.&lt;br>Minimum value = 0&lt;br>Maximum value = 4094</td><tr><tr><td>srcip</td><td>&lt;String></td><td>Read-write</td><td>IP address or the name of an IP set.</td><tr><tr><td>srcippersistency</td><td>&lt;String></td><td>Read-write</td><td>When the net profile is associated with a virtual server or its bound services, this option enables the NetScaler appliance to use the same address, specified in the net profile, to communicate to servers for all sessions initiated from a particular client to the virtual server.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>overridelsn</td><td>&lt;String></td><td>Read-write</td><td>USNIP/USIP settings override LSN settings for configured service/virtual server traffic.. .&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
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
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>},"sessionid":"##sessionid","netprofile":{      "name":<String_value>,      "td":<Double_value>,      "srcip":<String_value>,      "srcippersistency":<String_value>,      "overridelsn":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/netprofile/name_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/netprofile/name_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","netprofile":{      "name":<String_value>,      "srcip":<String_value>,      "srcippersistency":<String_value>,      "overridelsn":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","netprofile":{      "name":<String_value>,      "srcip":true,      "srcippersistency":true,      "overridelsn":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/netprofile
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/netprofile?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of netprofile resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/netprofile?view=summary
Use this query-parameter to get the summary output of netprofile resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/netprofile?pagesize=#no;pageno=#no
Use this query-parameter to get the netprofile resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/netprofile?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "netprofile": [ {      "name":<String_value>,      "srcip":<String_value>,      "td":<Double_value>,      "srcippersistency":<String_value>,      "overridelsn":<String_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/netprofile/name_value&lt;String&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "netprofile": [ {      "name":<String_value>,      "srcip":<String_value>,      "td":<Double_value>,      "srcippersistency":<String_value>,      "overridelsn":<String_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/netprofile?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",netprofile: [ { "__count": "#no"} ] }


