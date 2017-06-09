#nspartition

Configuration for admin partition resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>partitionname</td><td>&lt;String></td><td>Read-write</td><td>Name of the Partition. Must begin with an ASCII alphanumeric or underscore (_) character, and must contain only ASCII alphanumeric, underscore, hash (#), period (.), space, colon (:), at (@), equals (=), and hyphen (-) characters.&lt;br>Minimum length = 1</td><tr><tr><td>maxbandwidth</td><td>&lt;Double></td><td>Read-write</td><td>Maximum bandwidth in Kbps, permitted on this partition.&lt;br>Default value: 10240</td><tr><tr><td>minbandwidth</td><td>&lt;Double></td><td>Read-write</td><td>Minimum bandwidth in Kbps, permitted on this partition.&lt;br>Default value: 10240</td><tr><tr><td>maxconn</td><td>&lt;Double></td><td>Read-write</td><td>Maximum number of connections permitted on this partition.&lt;br>Default value: 1024</td><tr><tr><td>maxmemlimit</td><td>&lt;Double></td><td>Read-write</td><td>Maximum memory allowed for this partition in megabytes.&lt;br>Default value: 10</td><tr><tr><td>partitionid</td><td>&lt;Double></td><td>Read-only</td><td>Partition Id.&lt;br>Minimum value = 1</td><tr><tr><td>partitiontype</td><td>&lt;String></td><td>Read-only</td><td>Type of the Partition.&lt;br>Possible values = Default Partition, Current Partition</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [DELETE](#delete) | [UPDATE](#update) | [UNSET](#unset) | [SWITCH](#switch) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>},"sessionid":"##sessionid","nspartition":{      "partitionname":<String_value>,      "maxbandwidth":<Double_value>,      "minbandwidth":<Double_value>,      "maxconn":<Double_value>,      "maxmemlimit":<Double_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/nspartition/partitionname_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/nspartition/partitionname_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","nspartition":{      "partitionname":<String_value>,      "maxbandwidth":<Double_value>,      "minbandwidth":<Double_value>,      "maxconn":<Double_value>,      "maxmemlimit":<Double_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","nspartition":{      "partitionname":<String_value>,      "maxbandwidth":true,      "minbandwidth":true,      "maxconn":true,      "maxmemlimit":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###Switch



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"Switch"},"sessionid":"##sessionid","nspartition":{      "partitionname":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/nspartition
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/nspartition?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of nspartition resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/nspartition?view=summary
Use this query-parameter to get the summary output of nspartition resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/nspartition?pagesize=#no;pageno=#no
Use this query-parameter to get the nspartition resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/nspartition?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "nspartition": [ {      "partitionname":<String_value>,      "partitionid":<Double_value>,      "partitiontype":<String_value>,      "maxbandwidth":<Double_value>,      "minbandwidth":<Double_value>,      "maxconn":<Double_value>,      "maxmemlimit":<Double_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/nspartition/partitionname_value&lt;String&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "nspartition": [ {      "partitionname":<String_value>,      "partitionid":<Double_value>,      "partitiontype":<String_value>,      "maxbandwidth":<Double_value>,      "minbandwidth":<Double_value>,      "maxconn":<Double_value>,      "maxmemlimit":<Double_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/nspartition?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",nspartition: [ { "__count": "#no"} ] }


