#systemglobaldata

Configuration for global counter data resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>counters</td><td>&lt;String></td><td>Read-write</td><td>Specify the counters to be collected.</td><tr><tr><td>countergroup</td><td>&lt;String></td><td>Read-write</td><td>Specify the (counter) group name which contains all the counters specific to this particular group.</td><tr><tr><td>starttime</td><td>&lt;String></td><td>Read-write</td><td>Specify start time in mmddyyyyhhmm to start collecting values from that timestamp.</td><tr><tr><td>endtime</td><td>&lt;String></td><td>Read-write</td><td>Specify end time in mmddyyyyhhmm upto which values have to be collected.</td><tr><tr><td>last</td><td>&lt;Integer></td><td>Read-write</td><td>Last is literal way of saying a certain time period from the current moment. Example: -last 1 hour, -last 1 day, et cetera.&lt;br>Default value: 1</td><tr><tr><td>unit</td><td>&lt;String></td><td>Read-write</td><td>Specify the time period from current moment. Example 1 x where x = hours/ days/ years.&lt;br>Possible values = HOURS, DAYS, MONTHS</td><tr><tr><td>datasource</td><td>&lt;String></td><td>Read-write</td><td>Specifies the source which contains all the stored counter values.</td><tr><tr><td>core</td><td>&lt;Integer></td><td>Read-write</td><td>Specify core ID of the PE in nCore.</td><tr><tr><td>response</td><td>&lt;String></td><td>Read-only</td><td>.</td><tr><tr><td>startupdate</td><td>&lt;Double></td><td>Read-only</td><td>.</td><tr><tr><td>lastupdate</td><td>&lt;Double></td><td>Read-only</td><td>.</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[GET (ALL)](#get-(all))


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/systemglobaldata
Query-parameters:
args
http://&lt;NSIP&gt;/nitro/v1/config/systemglobaldata?args=      "counters":&lt;String_value&gt;,      "countergroup":&lt;String_value&gt;,      "starttime":&lt;String_value&gt;,      "endtime":&lt;String_value&gt;,      "last":&lt;Integer_value&gt;,                  "unit":&lt;String_value&gt;,      "datasource":&lt;String_value&gt;,      "core":&lt;Integer_value&gt;,
Use this query-parameter to get systemglobaldata resources based on additional properties.



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "systemglobaldata": [ {      "counters":<String_value>,      "countergroup":<String_value>,      "starttime":<String_value>,      "endtime":<String_value>,      "last":<Integer_value>,                  "unit":<String_value>,      "datasource":<String_value>,      "core":<Integer_value>,      "response":<String_value>,      "startupdate":<Double_value>,      "lastupdate":<Double_value>}]}```



