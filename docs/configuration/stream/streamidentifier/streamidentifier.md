#streamidentifier

Configuration for identifier resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>The name of stream identifier.</td><tr><tr><td>selectorname</td><td>&lt;String></td><td>Read-write</td><td>Name of the selector to use with the stream identifier.&lt;br>Minimum length = 1</td><tr><tr><td>interval</td><td>&lt;Double></td><td>Read-write</td><td>Number of minutes of data to use when calculating session statistics (number of requests, bandwidth, and response times). The interval is a moving window that keeps the most recently collected data. Older data is discarded at regular intervals.&lt;br>Default value: 1&lt;br>Minimum value = 1</td><tr><tr><td>samplecount</td><td>&lt;Double></td><td>Read-write</td><td>Size of the sample from which to select a request for evaluation. The smaller the sample count, the more accurate is the statistical data. To evaluate all requests, set the sample count to 1. However, such a low setting can result in excessive consumption of memory and processing resources.&lt;br>Default value: 1&lt;br>Minimum value = 1&lt;br>Maximum value = 65535</td><tr><tr><td>sort</td><td>&lt;String></td><td>Read-write</td><td>Sort stored records by the specified statistics column, in descending order. Performed during data collection, the sorting enables real-time data evaluation through NetScaler policies (for example, compression and caching policies) that use functions such as IS_TOP(n).&lt;br>Default value: REQUESTS&lt;br>Possible values = REQUESTS, CONNECTIONS, RESPTIME, BANDWIDTH, RESPTIME_BREACHES, NONE</td><tr><tr><td>snmptrap</td><td>&lt;String></td><td>Read-write</td><td>Enable/disable SNMP trap for stream identifier.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>appflowlog</td><td>&lt;String></td><td>Read-write</td><td>Enable/disable Appflow logging for stream identifier.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>tracktransactions</td><td>&lt;String></td><td>Read-write</td><td>Track transactions exceeding configured threshold. Transaction tracking can be enabled for following metric: ResponseTime. By default transaction tracking is disabled.&lt;br>Default value: NONE&lt;br>Possible values = RESPTIME, NONE</td><tr><tr><td>maxtransactionthreshold</td><td>&lt;Double></td><td>Read-write</td><td>Maximum per transcation value of metric. Metric to be tracked is specified by tracktransactions attribute.&lt;br>Default value: 0</td><tr><tr><td>mintransactionthreshold</td><td>&lt;Double></td><td>Read-write</td><td>Minimum per transcation value of metric. Metric to be tracked is specified by tracktransactions attribute.&lt;br>Default value: 0</td><tr><tr><td>acceptancethreshold</td><td>&lt;String></td><td>Read-write</td><td>Non-Breaching transactions to Total transactions threshold expressed in percent. Maximum of 6 decimal places is supported.&lt;br>Default value: 0.000000&lt;br>Maximum length = 10</td><tr><tr><td>breachthreshold</td><td>&lt;Double></td><td>Read-write</td><td>Breaching transactions threshold calculated over interval.&lt;br>Default value: 0</td><tr><tr><td>rule</td><td>&lt;String[]></td><td>Read-only</td><td>Rule.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
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
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>},"sessionid":"##sessionid","streamidentifier":{      "name":<String_value>,      "selectorname":<String_value>,      "interval":<Double_value>,      "samplecount":<Double_value>,      "sort":<String_value>,      "snmptrap":<String_value>,      "appflowlog":<String_value>,      "tracktransactions":<String_value>,                  "maxtransactionthreshold":<Double_value>,                  "mintransactionthreshold":<Double_value>,                  "acceptancethreshold":<String_value>,                  "breachthreshold":<Double_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","streamidentifier":{      "name":<String_value>,      "selectorname":<String_value>,      "interval":<Double_value>,      "samplecount":<Double_value>,      "sort":<String_value>,      "snmptrap":<String_value>,      "appflowlog":<String_value>,      "tracktransactions":<String_value>,      "maxtransactionthreshold":<Double_value>,      "mintransactionthreshold":<Double_value>,      "acceptancethreshold":<String_value>,      "breachthreshold":<Double_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","streamidentifier":{      "name":<String_value>,      "selectorname":true,      "interval":true,      "samplecount":true,      "sort":true,      "snmptrap":true,      "appflowlog":true,      "tracktransactions":true,      "maxtransactionthreshold":true,      "mintransactionthreshold":true,      "acceptancethreshold":true,      "breachthreshold":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/streamidentifier/name_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/streamidentifier/name_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/streamidentifier
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/streamidentifier?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of streamidentifier resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/streamidentifier?view=summary
Use this query-parameter to get the summary output of streamidentifier resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/streamidentifier?pagesize=#no;pageno=#no
Use this query-parameter to get the streamidentifier resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/streamidentifier?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "streamidentifier": [ {      "name":<String_value>,      "selectorname":<String_value>,      "rule":<String[]_value>,      "interval":<Double_value>,      "samplecount":<Double_value>,      "sort":<String_value>,      "snmptrap":<String_value>,      "appflowlog":<String_value>,      "tracktransactions":<String_value>,      "maxtransactionthreshold":<Double_value>,      "mintransactionthreshold":<Double_value>,      "acceptancethreshold":<String_value>,      "breachthreshold":<Double_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/streamidentifier/name_value&lt;String&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "streamidentifier": [ {      "name":<String_value>,      "selectorname":<String_value>,      "rule":<String[]_value>,      "interval":<Double_value>,      "samplecount":<Double_value>,      "sort":<String_value>,      "snmptrap":<String_value>,      "appflowlog":<String_value>,      "tracktransactions":<String_value>,      "maxtransactionthreshold":<Double_value>,      "mintransactionthreshold":<Double_value>,      "acceptancethreshold":<String_value>,      "breachthreshold":<Double_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/streamidentifier?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",streamidentifier: [ { "__count": "#no"} ] }


