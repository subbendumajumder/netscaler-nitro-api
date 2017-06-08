#ssldtlsprofile

Configuration for DTLS profile resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the DTLS profile. Must begin with an ASCII alphanumeric or underscore (_) character, and must contain only ASCII alphanumeric, underscore, hash (#), period (.), space, colon (:), at (@),equals sign (=), and hyphen (-) characters. Cannot be changed after the profile is created.&lt;br>Minimum length = 1&lt;br>Maximum length = 127</td><tr><tr><td>pmtudiscovery</td><td>&lt;String></td><td>Read-write</td><td>Source for the maximum record size value. If ENABLED, the value is taken from the PMTU table. If DISABLED, the value is taken from the profile.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>maxrecordsize</td><td>&lt;Double></td><td>Read-write</td><td>Maximum size of records that can be sent if PMTU is disabled.&lt;br>Default value: 1459&lt;br>Minimum value = 250&lt;br>Maximum value = 1459</td><tr><tr><td>maxretrytime</td><td>&lt;Double></td><td>Read-write</td><td>Wait for the specified time, in seconds, before resending the request.&lt;br>Default value: 3</td><tr><tr><td>helloverifyrequest</td><td>&lt;String></td><td>Read-write</td><td>Send a Hello Verify request to validate the client.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>terminatesession</td><td>&lt;String></td><td>Read-write</td><td>Terminate the session if the message authentication code (MAC) of the client and server do not match.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>maxpacketsize</td><td>&lt;Double></td><td>Read-write</td><td>Maximum number of packets to reassemble. This value helps protect against a fragmented packet attack.&lt;br>Default value: 120&lt;br>Minimum value = 0&lt;br>Maximum value = 86400</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
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
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>},"sessionid":"##sessionid","ssldtlsprofile":{      "name":<String_value>,      "pmtudiscovery":<String_value>,      "maxrecordsize":<Double_value>,      "maxretrytime":<Double_value>,      "helloverifyrequest":<String_value>,      "terminatesession":<String_value>,      "maxpacketsize":<Double_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/ssldtlsprofile/name_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/ssldtlsprofile/name_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","ssldtlsprofile":{      "name":<String_value>,      "pmtudiscovery":<String_value>,      "maxrecordsize":<Double_value>,      "maxretrytime":<Double_value>,      "helloverifyrequest":<String_value>,      "terminatesession":<String_value>,      "maxpacketsize":<Double_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","ssldtlsprofile":{      "name":<String_value>,      "pmtudiscovery":true,      "maxrecordsize":true,      "maxretrytime":true,      "helloverifyrequest":true,      "terminatesession":true,      "maxpacketsize":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/ssldtlsprofile
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/ssldtlsprofile?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of ssldtlsprofile resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/ssldtlsprofile?view=summary
Use this query-parameter to get the summary output of ssldtlsprofile resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/ssldtlsprofile?pagesize=#no;pageno=#no
Use this query-parameter to get the ssldtlsprofile resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/ssldtlsprofile?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "ssldtlsprofile": [ {      "name":<String_value>,      "pmtudiscovery":<String_value>,      "maxrecordsize":<Double_value>,      "maxretrytime":<Double_value>,      "helloverifyrequest":<String_value>,      "terminatesession":<String_value>,      "maxpacketsize":<Double_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/ssldtlsprofile/name_value&lt;String&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "ssldtlsprofile": [ {      "name":<String_value>,      "pmtudiscovery":<String_value>,      "maxrecordsize":<Double_value>,      "maxretrytime":<Double_value>,      "helloverifyrequest":<String_value>,      "terminatesession":<String_value>,      "maxpacketsize":<Double_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/ssldtlsprofile?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",ssldtlsprofile: [ { "__count": "#no"} ] }


