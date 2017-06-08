#nslimitsessions

Configuration for limit sessions resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>limitidentifier</td><td>&lt;String></td><td>Read-write</td><td>Name of the rate limit identifier for which to display the sessions.&lt;br>Minimum length = 1</td><tr><tr><td>detail</td><td>&lt;Boolean></td><td>Read-write</td><td>Show the individual hash values.</td><tr><tr><td>timeout</td><td>&lt;Double></td><td>Read-only</td><td>The time remaining on the session before a flush can be attempted. If active transactions are present the session will not be flushed.</td><tr><tr><td>hits</td><td>&lt;Double></td><td>Read-only</td><td>The number of times this entry was hit.</td><tr><tr><td>drop</td><td>&lt;Double></td><td>Read-only</td><td>The number of times action was taken.</td><tr><tr><td>number</td><td>&lt;Double[]></td><td>Read-only</td><td>The hash of the matched selectlets.</td><tr><tr><td>name</td><td>&lt;String></td><td>Read-only</td><td>The string formed by gathering selectlet values.</td><tr><tr><td>unit</td><td>&lt;Double></td><td>Read-only</td><td>Total computed hash of the matched selectlets.</td><tr><tr><td>flags</td><td>&lt;Double></td><td>Read-only</td><td>Used internally to identify ip addresses.</td><tr><tr><td>referencecount</td><td>&lt;Double></td><td>Read-only</td><td>Total number of transactions pointing to this entry. Its the sum total of the connection and bandwidth references.</td><tr><tr><td>maxbandwidth</td><td>&lt;Double></td><td>Read-only</td><td>The current bandwidth.</td><tr><tr><td>selectoripv61</td><td>&lt;String></td><td>Read-only</td><td>First IPV6 address gathered.</td><tr><tr><td>selectoripv62</td><td>&lt;String></td><td>Read-only</td><td>Second IPV6 address gathered.</td><tr><tr><td>flag</td><td>&lt;Double></td><td>Read-only</td><td>Used internally to identify ipv6 addresses.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[CLEAR](#clear) | [GET (ALL)](#get-(all)) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###clear



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"clear"},"sessionid":"##sessionid","nslimitsessions":{      "limitidentifier":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/nslimitsessions
Query-parameters:
args
http://&lt;NSIP&gt;/nitro/v1/config/nslimitsessions?args=      "limitidentifier":&lt;String_value&gt;,      "detail":&lt;Boolean_value&gt;,
Use this query-parameter to get nslimitsessions resources based on additional properties.


filter
http://&lt;NSIP&gt;/nitro/v1/config/nslimitsessions?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of nslimitsessions resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/nslimitsessions?view=summary
Use this query-parameter to get the summary output of nslimitsessions resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/nslimitsessions?pagesize=#no;pageno=#no
Use this query-parameter to get the nslimitsessions resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/nslimitsessions?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "nslimitsessions": [ {      "limitidentifier":<String_value>,      "detail":<Boolean_value>,      "timeout":<Double_value>,      "hits":<Double_value>,      "drop":<Double_value>,      "number":<Double[]_value>,      "name":<String_value>,      "unit":<Double_value>,      "flags":<Double_value>,      "referencecount":<Double_value>,      "maxbandwidth":<Double_value>,      "selectoripv61":<String_value>,      "selectoripv62":<String_value>,      "flag":<Double_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/nslimitsessions?args=     "limitidentifier":&lt;String_value&gt;,      "detail":&lt;Boolean_value&gt;;count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",nslimitsessions: [ { "__count": "#no"} ] }


