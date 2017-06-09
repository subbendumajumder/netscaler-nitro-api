#lsnsipalgprofile

Configuration for LSN SIPALG Profile resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>sipalgprofilename</td><td>&lt;String></td><td>Read-write</td><td>The name of the SIPALG Profile.&lt;br>Minimum length = 1&lt;br>Maximum length = 127</td><tr><tr><td>datasessionidletimeout</td><td>&lt;Double></td><td>Read-write</td><td>Idle timeout for the data channel sessions in seconds.&lt;br>Default value: 120</td><tr><tr><td>sipsessiontimeout</td><td>&lt;Double></td><td>Read-write</td><td>SIP control channel session timeout in seconds.&lt;br>Default value: 600</td><tr><tr><td>registrationtimeout</td><td>&lt;Double></td><td>Read-write</td><td>SIP registration timeout in seconds.&lt;br>Default value: 60</td><tr><tr><td>sipsrcportrange</td><td>&lt;String></td><td>Read-write</td><td>Source port range for SIP_UDP and SIP_TCP.</td><tr><tr><td>sipdstportrange</td><td>&lt;String></td><td>Read-write</td><td>Destination port range for SIP_UDP and SIP_TCP.</td><tr><tr><td>openregisterpinhole</td><td>&lt;String></td><td>Read-write</td><td>ENABLE/DISABLE RegisterPinhole creation.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>opencontactpinhole</td><td>&lt;String></td><td>Read-write</td><td>ENABLE/DISABLE ContactPinhole creation.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>openviapinhole</td><td>&lt;String></td><td>Read-write</td><td>ENABLE/DISABLE ViaPinhole creation.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>openrecordroutepinhole</td><td>&lt;String></td><td>Read-write</td><td>ENABLE/DISABLE RecordRoutePinhole creation.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>siptransportprotocol</td><td>&lt;String></td><td>Read-write</td><td>SIP ALG Profile transport protocol type.&lt;br>Possible values = TCP, UDP</td><tr><tr><td>openroutepinhole</td><td>&lt;String></td><td>Read-write</td><td>ENABLE/DISABLE RoutePinhole creation.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>rport</td><td>&lt;String></td><td>Read-write</td><td>ENABLE/DISABLE rport.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [UPDATE](#update) | [UNSET](#unset) | [DELETE](#delete) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>},"sessionid":"##sessionid","lsnsipalgprofile":{      "sipalgprofilename":<String_value>,      "datasessionidletimeout":<Double_value>,      "sipsessiontimeout":<Double_value>,      "registrationtimeout":<Double_value>,      "sipsrcportrange":<String_value>,      "sipdstportrange":<String_value>,      "openregisterpinhole":<String_value>,      "opencontactpinhole":<String_value>,      "openviapinhole":<String_value>,      "openrecordroutepinhole":<String_value>,      "siptransportprotocol":<String_value>,      "openroutepinhole":<String_value>,      "rport":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","lsnsipalgprofile":{      "sipalgprofilename":<String_value>,      "datasessionidletimeout":<Double_value>,      "sipsessiontimeout":<Double_value>,      "registrationtimeout":<Double_value>,      "sipsrcportrange":<String_value>,      "sipdstportrange":<String_value>,      "openregisterpinhole":<String_value>,      "opencontactpinhole":<String_value>,      "openviapinhole":<String_value>,      "openrecordroutepinhole":<String_value>,      "siptransportprotocol":<String_value>,      "openroutepinhole":<String_value>,      "rport":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","lsnsipalgprofile":{      "sipalgprofilename":<String_value>,      "datasessionidletimeout":true,      "sipsessiontimeout":true,      "registrationtimeout":true,      "sipsrcportrange":true,      "sipdstportrange":true,      "openregisterpinhole":true,      "opencontactpinhole":true,      "openviapinhole":true,      "openrecordroutepinhole":true,      "siptransportprotocol":true,      "openroutepinhole":true,      "rport":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/lsnsipalgprofile/sipalgprofilename_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/lsnsipalgprofile/sipalgprofilename_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/lsnsipalgprofile
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/lsnsipalgprofile?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of lsnsipalgprofile resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/lsnsipalgprofile?view=summary
Use this query-parameter to get the summary output of lsnsipalgprofile resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/lsnsipalgprofile?pagesize=#no;pageno=#no
Use this query-parameter to get the lsnsipalgprofile resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/lsnsipalgprofile?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "lsnsipalgprofile": [ {      "sipalgprofilename":<String_value>,      "datasessionidletimeout":<Double_value>,      "sipsessiontimeout":<Double_value>,      "registrationtimeout":<Double_value>,      "sipsrcportrange":<String_value>,      "sipdstportrange":<String_value>,      "openregisterpinhole":<String_value>,      "opencontactpinhole":<String_value>,      "openviapinhole":<String_value>,      "openrecordroutepinhole":<String_value>,      "siptransportprotocol":<String_value>,      "openroutepinhole":<String_value>,      "rport":<String_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/lsnsipalgprofile/sipalgprofilename_value&lt;String&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "lsnsipalgprofile": [ {      "sipalgprofilename":<String_value>,      "datasessionidletimeout":<Double_value>,      "sipsessiontimeout":<Double_value>,      "registrationtimeout":<Double_value>,      "sipsrcportrange":<String_value>,      "sipdstportrange":<String_value>,      "openregisterpinhole":<String_value>,      "opencontactpinhole":<String_value>,      "openviapinhole":<String_value>,      "openrecordroutepinhole":<String_value>,      "siptransportprotocol":<String_value>,      "openroutepinhole":<String_value>,      "rport":<String_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/lsnsipalgprofile?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",lsnsipalgprofile: [ { "__count": "#no"} ] }


