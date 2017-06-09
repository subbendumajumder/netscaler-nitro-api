#icalatencyprofile

Configuration for Profile for Latency monitoring resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the ICA latencyprofile. Must begin with a letter, number, or the underscore character (_), and must contain only letters, numbers, and&lt;br>the hyphen (-), period (.) pound (#), space ( ), at (@), equals (=), colon (:), and underscore characters. Cannot be changed after the ICA latency profile is added.&lt;br>&lt;br>The following requirement applies only to the NetScaler CLI:&lt;br>If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my ica l7latencyprofile" or my ica l7latencyprofile).&lt;br>Minimum length = 1</td><tr><tr><td>l7latencymonitoring</td><td>&lt;String></td><td>Read-write</td><td>Enable/Disable L7 Latency monitoring for L7 latency notifications.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>l7latencythresholdfactor</td><td>&lt;Double></td><td>Read-write</td><td>L7 Latency threshold factor. This is the factor by which the active latency should be greater than the minimum observed value to determine that the latency is high and may need to be reported.&lt;br>Default value: 4&lt;br>Minimum value = 2&lt;br>Maximum value = 65535</td><tr><tr><td>l7latencywaittime</td><td>&lt;Double></td><td>Read-write</td><td>L7 Latency Wait time. This is the time for which the Netscaler waits after the threshold is exceeded before it sends out a Notification to the Insight Center.&lt;br>Default value: 20&lt;br>Minimum value = 1&lt;br>Maximum value = 65535</td><tr><tr><td>l7latencynotifyinterval</td><td>&lt;Double></td><td>Read-write</td><td>L7 Latency Notify Interval. This is the interval at which the Netscaler sends out notifications to the Insight Center after the wait time has passed.&lt;br>Default value: 20&lt;br>Minimum value = 1&lt;br>Maximum value = 65535</td><tr><tr><td>l7latencymaxnotifycount</td><td>&lt;Double></td><td>Read-write</td><td>L7 Latency Max notify Count. This is the upper limit on the number of notifications sent to the Insight Center within an interval where the Latency is above the threshold.&lt;br>Default value: 5&lt;br>Minimum value = 1&lt;br>Maximum value = 65535</td><tr><tr><td>refcnt</td><td>&lt;Double></td><td>Read-only</td><td>Number of entities using this l7latencyprofile.</td><tr><tr><td>builtin</td><td>&lt;String[]></td><td>Read-only</td><td>Indicates that the ICA latencyprofile is a built-in (SYSTEM INTERNAL) type.&lt;br>Possible values = MODIFIABLE, DELETABLE, IMMUTABLE, PARTITION_ALL</td><tr><tr><td>isdefault</td><td>&lt;Boolean></td><td>Read-only</td><td>A value of true is returned if it is a default l7latencyprofile.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [DELETE](#delete) | [UPDATE](#update) | [UNSET](#unset) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/icalatencyprofile
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"icalatencyprofile":{      "name":<String_value>,      "l7latencymonitoring":<String_value>,      "l7latencythresholdfactor":<Double_value>,      "l7latencywaittime":<Double_value>,      "l7latencynotifyinterval":<Double_value>,      "l7latencymaxnotifycount":<Double_value>}}```
Response:
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx   (for general HTTP errors) or 5xx     (for NetScaler-specific errors). The response payload provides details of the error 


###delete



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/icalatencyprofile/name_value&lt;String&gt;
HTTP Method: DELETE
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx   (for general HTTP errors) or 5xx     (for NetScaler-specific errors). The response payload provides details of the error 


###update



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/icalatencyprofile
HTTP Method: PUT
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"icalatencyprofile":{      "name":<String_value>,      "l7latencymonitoring":<String_value>,      "l7latencythresholdfactor":<Double_value>,      "l7latencywaittime":<Double_value>,      "l7latencynotifyinterval":<Double_value>,      "l7latencymaxnotifycount":<Double_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx   (for general HTTP errors) or 5xx     (for NetScaler-specific errors). The response payload provides details of the error 


###unset



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/icalatencyprofile?action=unset
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"icalatencyprofile":{      "name":<String_value>,      "l7latencymonitoring":true,      "l7latencythresholdfactor":true,      "l7latencywaittime":true,      "l7latencynotifyinterval":true,      "l7latencymaxnotifycount":true}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx   (for general HTTP errors) or 5xx     (for NetScaler-specific errors). The response payload provides details of the error 


###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/icalatencyprofile
Query-parameters:
args
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/icalatencyprofile?args=      "name":&lt;String_value&gt;
Use this query-parameter to get icalatencyprofile resources based on additional properties.


attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/icalatencyprofile?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


filter
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/icalatencyprofile?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of icalatencyprofile resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/icalatencyprofile?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).


pagesize=#no;pageno=#no
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/icalatencyprofile?pagesize=#no;pageno=#no
Use this query-parameter to get the icalatencyprofile resources in chunks.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx   (for general HTTP errors) or 5xx     (for NetScaler-specific errors). The response payload provides details of the error Response Headers:

Content-Type:application/json

Response Payload: ```{ "icalatencyprofile": [ {      "name":<String_value>,      "l7latencymonitoring":<String_value>,      "l7latencythresholdfactor":<Double_value>,      "l7latencywaittime":<Double_value>,      "l7latencynotifyinterval":<Double_value>,      "l7latencymaxnotifycount":<Double_value>,      "refcnt":<Double_value>,      "builtin":<String[]_value>,      "isdefault":<Boolean_value>}]}```



###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/icalatencyprofile/name_value&lt;String&gt;
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/icalatencyprofile/name_value&lt;String&gt;?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/icalatencyprofile/name_value&lt;String&gt;?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx   (for general HTTP errors) or 5xx     (for NetScaler-specific errors). The response payload provides details of the error Response Headers:

Content-Type:application/json

Response Payload: ```{ "icalatencyprofile": [ {      "name":<String_value>,      "l7latencymonitoring":<String_value>,      "l7latencythresholdfactor":<Double_value>,      "l7latencywaittime":<Double_value>,      "l7latencynotifyinterval":<Double_value>,      "l7latencymaxnotifycount":<Double_value>,      "refcnt":<Double_value>,      "builtin":<String[]_value>,      "isdefault":<Boolean_value>}]}```



###count



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/icalatencyprofile?count=yes
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx   (for general HTTP errors) or 5xx     (for NetScaler-specific errors). The response payload provides details of the error Response Headers:

Content-Type:application/json

Response Payload: 
{ "icalatencyprofile": [ { "__count": "#no"} ] }


