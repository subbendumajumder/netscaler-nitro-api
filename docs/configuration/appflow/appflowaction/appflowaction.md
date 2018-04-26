#appflowaction

Configuration for AppFlow action resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the action. Must begin with an ASCII alphabetic or underscore (_) character, and must contain only ASCII alphanumeric, underscore, hash (#), period (.), space, colon (:), at (@), equals (=), and hyphen (-) characters.<br><br>The following requirement applies only to the NetScaler CLI:<br>If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my appflow action" or 'my appflow action').</td></tr><tr><td>collectors</td><td>&lt;String[]></td><td>Read-write</td><td>Name(s) of collector(s) to be associated with the AppFlow action.<br>Minimum length = 1</td></tr><tr><td>clientsidemeasurements</td><td>&lt;String></td><td>Read-write</td><td>On enabling this option, the NetScaler will collect the time required to load and render the mainpage on the client.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>pagetracking</td><td>&lt;String></td><td>Read-write</td><td>On enabling this option, the NetScaler will start tracking the page for waterfall chart by inserting a NS_ESNS cookie in the response.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>webinsight</td><td>&lt;String></td><td>Read-write</td><td>On enabling this option, the netscaler will send the webinsight records to the configured collectors.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>securityinsight</td><td>&lt;String></td><td>Read-write</td><td>On enabling this option, the netscaler will send the security insight records to the configured collectors.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>videoanalytics</td><td>&lt;String></td><td>Read-write</td><td>On enabling this option, the netscaler will send the videoinsight records to the configured collectors.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>distributionalgorithm</td><td>&lt;String></td><td>Read-write</td><td>On enabling this option, the netscaler will distribute records among the collectors. Else, all records will be sent to all the collectors.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>metricslog</td><td>&lt;Boolean></td><td>Read-write</td><td>If only the stats records are to be exported, turn on this option.</td></tr><tr><td>transactionlog</td><td>&lt;String></td><td>Read-write</td><td>If over stats channel, transactions logs also need to be sent, set this option appropriately. By default netscaler sends anomalous transaction logs over metrics channel. This can be changed to ALL or NONE transactions.<br>Default value: ANOMALOUS<br>Possible values = ANOMALOUS, NONE, ALL</td></tr><tr><td>comment</td><td>&lt;String></td><td>Read-write</td><td>Any comments about this action. In the CLI, if including spaces between words, enclose the comment in quotation marks. (The quotation marks are not required in the configuration utility.).<br>Maximum length = 256</td></tr><tr><td>newname</td><td>&lt;String></td><td>Read-write</td><td>New name for the AppFlow action. Must begin with an ASCII alphabetic or underscore (_) character, and must contain only ASCII alphanumeric, underscore, hash (#), period (.), space, colon (:), at<br>(@), equals (=), and hyphen (-) characters. <br><br>The following requirement applies only to the NetScaler CLI:<br>If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my appflow action" or 'my appflow action').<br>Minimum length = 1</td></tr><tr><td>hits</td><td>&lt;Double></td><td>Read-only</td><td>The number of times the action has been taken.</td></tr><tr><td>referencecount</td><td>&lt;Double></td><td>Read-only</td><td>The number of references to the action.</td></tr><tr><td>description</td><td>&lt;String></td><td>Read-only</td><td>Description of the action.</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD]()| [DELETE](#d)| [UPDATE](#u)| [UNSET](#)| [RENAME](#r)| [GET (ALL)](#get-)| [GET]()| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appflowaction
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"appflowaction":{<b>"name":<String_value>,</b><b>"collectors":<String[]_value>,</b>"clientsidemeasurements":<String_value>,"pagetracking":<String_value>,"webinsight":<String_value>,"securityinsight":<String_value>,"videoanalytics":<String_value>,"distributionalgorithm":<String_value>,"metricslog":<Boolean_value>,"transactionlog":<String_value>,"comment":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appflowaction/name_value&lt;String&gt;
<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appflowaction
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"appflowaction":{<b>"name":<String_value>,</b>"collectors":<String[]_value>,"clientsidemeasurements":<String_value>,"comment":<String_value>,"pagetracking":<String_value>,"webinsight":<String_value>,"securityinsight":<String_value>,"videoanalytics":<String_value>,"distributionalgorithm":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appflowaction?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"appflowaction":{<b>"name":<String_value>,</b>"clientsidemeasurements":true,"comment":true,"pagetracking":true,"webinsight":true,"securityinsight":true,"videoanalytics":true,"distributionalgorithm":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###rename



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appflowaction?<b>action=rename</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"appflowaction":{<b>"name":<String_value>,</b><b>"newname":<String_value></b>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appflowaction
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appflowaction?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appflowaction?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of appflowaction resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appflowaction?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appflowaction?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the appflowaction resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "appflowaction": [ {"name":<String_value>,"hits":<Double_value>,"collectors":<String[]_value>,"clientsidemeasurements":<String_value>,"pagetracking":<String_value>,"webinsight":<String_value>,"securityinsight":<String_value>,"videoanalytics":<String_value>,"distributionalgorithm":<String_value>,"metricslog":<Boolean_value>,"transactionlog":<String_value>,"referencecount":<Double_value>,"description":<String_value>,"comment":<String_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appflowaction/name_value&lt;String&gt;
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appflowaction/name_value&lt;String&gt;?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appflowaction/name_value&lt;String&gt;?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "appflowaction": [ {"name":<String_value>,"hits":<Double_value>,"collectors":<String[]_value>,"clientsidemeasurements":<String_value>,"pagetracking":<String_value>,"webinsight":<String_value>,"securityinsight":<String_value>,"videoanalytics":<String_value>,"distributionalgorithm":<String_value>,"metricslog":<Boolean_value>,"transactionlog":<String_value>,"referencecount":<Double_value>,"description":<String_value>,"comment":<String_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appflowaction?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "appflowaction": [ { "__count": "#no"} ] }```



