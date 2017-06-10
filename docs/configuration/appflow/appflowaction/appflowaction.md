#appflowaction

Configuration for AppFlow action resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the action. Must begin with an ASCII alphabetic or underscore (_) character, and must contain only ASCII alphanumeric, underscore, hash (#), period (.), space, colon (:), at (@), equals (=), and hyphen (-) characters.&lt;br>&lt;br>The following requirement applies only to the NetScaler CLI:&lt;br>If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my appflow action" or my appflow action).</td><tr><tr><td>collectors</td><td>&lt;String[]></td><td>Read-write</td><td>Name(s) of collector(s) to be associated with the AppFlow action.&lt;br>Minimum length = 1</td><tr><tr><td>clientsidemeasurements</td><td>&lt;String></td><td>Read-write</td><td>On enabling this option, the NetScaler will collect the time required to load and render the mainpage on the client.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>pagetracking</td><td>&lt;String></td><td>Read-write</td><td>On enabling this option, the NetScaler will start tracking the page for waterfall chart by inserting a NS_ESNS cookie in the response.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>webinsight</td><td>&lt;String></td><td>Read-write</td><td>On enabling this option, the netscaler will send the webinsight records to the configured collectors.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>securityinsight</td><td>&lt;String></td><td>Read-write</td><td>On enabling this option, the netscaler will send the security insight records to the configured collectors.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>videoanalytics</td><td>&lt;String></td><td>Read-write</td><td>On enabling this option, the netscaler will send the videoinsight records to the configured collectors.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>distributionalgorithm</td><td>&lt;String></td><td>Read-write</td><td>On enabling this option, the netscaler will distribute records among the collectors. Else, all records will be sent to all the collectors.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>metricslog</td><td>&lt;Boolean></td><td>Read-write</td><td>If only the stats records are to be exported, turn on this option.</td><tr><tr><td>transactionlog</td><td>&lt;String></td><td>Read-write</td><td>If over stats channel, transactions logs also need to be sent, set this option appropriately. By default netscaler sends anomalous transaction logs over metrics channel. This can be changed to ALL or NONE transactions.&lt;br>Default value: ANOMALOUS&lt;br>Possible values = ANOMALOUS, NONE, ALL</td><tr><tr><td>comment</td><td>&lt;String></td><td>Read-write</td><td>Any comments about this action. In the CLI, if including spaces between words, enclose the comment in quotation marks. (The quotation marks are not required in the configuration utility.).&lt;br>Maximum length = 256</td><tr><tr><td>newname</td><td>&lt;String></td><td>Read-write</td><td>New name for the AppFlow action. Must begin with an ASCII alphabetic or underscore (_) character, and must contain only ASCII alphanumeric, underscore, hash (#), period (.), space, colon (:), at&lt;br>(@), equals (=), and hyphen (-) characters. &lt;br>&lt;br>The following requirement applies only to the NetScaler CLI:&lt;br>If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my appflow action" or my appflow action).&lt;br>Minimum length = 1</td><tr><tr><td>hits</td><td>&lt;Double></td><td>Read-only</td><td>The number of times the action has been taken.</td><tr><tr><td>referencecount</td><td>&lt;Double></td><td>Read-only</td><td>The number of references to the action.</td><tr><tr><td>description</td><td>&lt;String></td><td>Read-only</td><td>Description of the action.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [DELETE](#delete) | [UPDATE](#update) | [UNSET](#unset) | [RENAME](#rename) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appflowaction
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"appflowaction":{      "name":<String_value>,      "collectors":<String[]_value>,      "clientsidemeasurements":<String_value>,      "pagetracking":<String_value>,      "webinsight":<String_value>,      "securityinsight":<String_value>,      "videoanalytics":<String_value>,      "distributionalgorithm":<String_value>,      "metricslog":<Boolean_value>,      "transactionlog":<String_value>,      "comment":<String_value>}}```
Response:
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appflowaction/name_value&lt;String&gt;
HTTP Method: DELETE
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appflowaction
HTTP Method: PUT
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"appflowaction":{      "name":<String_value>,      "collectors":<String[]_value>,      "clientsidemeasurements":<String_value>,      "comment":<String_value>,      "pagetracking":<String_value>,      "webinsight":<String_value>,      "securityinsight":<String_value>,      "videoanalytics":<String_value>,      "distributionalgorithm":<String_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appflowaction?action=unset
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"appflowaction":{      "name":<String_value>,      "clientsidemeasurements":true,      "comment":true,      "pagetracking":true,      "webinsight":true,      "securityinsight":true,      "videoanalytics":true,      "distributionalgorithm":true}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###rename



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appflowaction?action=rename
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"appflowaction":{      "name":<String_value>,      "newname":<String_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appflowaction
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appflowaction?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


filter
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appflowaction?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of appflowaction resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appflowaction?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).


pagination
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appflowaction?pagesize=#no;pageno=#no
Use this query-parameter to get the appflowaction resources in chunks.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "appflowaction": [ {      "name":<String_value>,      "hits":<Double_value>,      "collectors":<String[]_value>,      "clientsidemeasurements":<String_value>,      "pagetracking":<String_value>,      "webinsight":<String_value>,      "securityinsight":<String_value>,      "videoanalytics":<String_value>,      "distributionalgorithm":<String_value>,      "metricslog":<Boolean_value>,      "transactionlog":<String_value>,      "referencecount":<Double_value>,      "description":<String_value>,      "comment":<String_value>}]}```



###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appflowaction/name_value&lt;String&gt;
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appflowaction/name_value&lt;String&gt;?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appflowaction/name_value&lt;String&gt;?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "appflowaction": [ {      "name":<String_value>,      "hits":<Double_value>,      "collectors":<String[]_value>,      "clientsidemeasurements":<String_value>,      "pagetracking":<String_value>,      "webinsight":<String_value>,      "securityinsight":<String_value>,      "videoanalytics":<String_value>,      "distributionalgorithm":<String_value>,      "metricslog":<Boolean_value>,      "transactionlog":<String_value>,      "referencecount":<Double_value>,      "description":<String_value>,      "comment":<String_value>}]}```



###count



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appflowaction?count=yes
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: 
{ "appflowaction": [ { "__count": "#no"} ] }


