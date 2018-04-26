#contentinspectionaction

Configuration for Content Inspection action resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name of the remote service action. Must begin with an ASCII alphabetic or underscore (_) character, and must contain only ASCII alphanumeric, underscore, hash (#), period (.), space, colon (:), at (@), equals (=), and hyphen (-) characters.</td></tr><tr><td>type</td><td>&lt;String></td><td>Read-write</td><td>Type of operation this action is going to perform. following actions are available to configure:<br>* ICAP - forward the incoming request or response to an ICAP server for modification.<br>* NSTRACE - capture current and further incoming packets on this transaction.<br>Possible values = ICAP, NSTRACE</td></tr><tr><td>servername</td><td>&lt;String></td><td>Read-write</td><td>Name of the LB vserver or service.<br>Minimum length = 1<br>Maximum length = 127</td></tr><tr><td>serverip</td><td>&lt;String></td><td>Read-write</td><td>IP address of remoteService.<br>Minimum length = 1</td></tr><tr><td>serverport</td><td>&lt;Double></td><td>Read-write</td><td>Port of remoteService.<br>Default value: 1344<br>Minimum value = 1<br>Maximum value = 65535</td></tr><tr><td>icapprofilename</td><td>&lt;String></td><td>Read-write</td><td>Name of the ICAP profile to be attached to the contentInspection action.<br>Minimum length = 1<br>Maximum length = 127</td></tr><tr><td>ifserverdown</td><td>&lt;String></td><td>Read-write</td><td>Name of the action to perform if the Vserver representing the remote service is not UP. There are also some built-in actions which can be used. These are:<br>* RESET - Reset the client connection by closing it. The client program, such as a browser, will handle this and may inform the user. The client may then resend the request if desired.<br>* DROP - Drop the request without sending a response to the user.<br>Default value: CONTINUE<br>Possible values = CONTINUE, DROP, RESET</td></tr><tr><td>reqtimeout</td><td>&lt;Double></td><td>Read-write</td><td>Time, in seconds, within which the remote service request must complete. If the request does not complete within this time, the specified request timeout action is executed. Zero disables the timeout.<br>Default value: 0<br>Minimum value = 0<br>Maximum value = 86400</td></tr><tr><td>reqtimeoutaction</td><td>&lt;String></td><td>Read-write</td><td>Name of the action to perform if the Vserver representing the remote service does not respond. There are also some built-in actions which can be used. These are:<br>* RESET - Reset the client connection by closing it. The client program, such as a browser, will handle this and may inform the user. The client may then resend the request if desired.<br>* DROP - Drop the request without sending a response to the user.<br>Default value: BYPASS<br>Possible values = BYPASS, DROP, RESET</td></tr><tr><td>hits</td><td>&lt;Double></td><td>Read-only</td><td>The number of times the action has been taken.</td></tr><tr><td>referencecount</td><td>&lt;Double></td><td>Read-only</td><td>The number of references to the action.</td></tr><tr><td>undefhits</td><td>&lt;Double></td><td>Read-only</td><td>The number of times the action resulted in UNDEF.</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD]()| [UPDATE](#u)| [UNSET](#)| [DELETE](#d)| [GET (ALL)](#get-)| [GET]()| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/contentinspectionaction
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"contentinspectionaction":{<b>"name":<String_value>,</b><b>"type":<String_value>,</b>"servername":<String_value>,"serverip":<String_value>,"serverport":<Double_value>,"icapprofilename":<String_value>,"ifserverdown":<String_value>,"reqtimeout":<Double_value>,"reqtimeoutaction":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/contentinspectionaction
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"contentinspectionaction":{<b>"name":<String_value>,</b>"servername":<String_value>,"serverip":<String_value>,"serverport":<Double_value>,"icapprofilename":<String_value>,"ifserverdown":<String_value>,"reqtimeout":<Double_value>,"reqtimeoutaction":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/contentinspectionaction?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"contentinspectionaction":{<b>"name":<String_value>,</b>"servername":true,"serverip":true,"serverport":true,"icapprofilename":true,"ifserverdown":true,"reqtimeout":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/contentinspectionaction/name_value&lt;String&gt;
<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/contentinspectionaction
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/contentinspectionaction?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/contentinspectionaction?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of contentinspectionaction resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/contentinspectionaction?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/contentinspectionaction?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the contentinspectionaction resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "contentinspectionaction": [ {"name":<String_value>,"type":<String_value>,"servername":<String_value>,"serverip":<String_value>,"serverport":<Double_value>,"icapprofilename":<String_value>,"ifserverdown":<String_value>,"reqtimeout":<Double_value>,"reqtimeoutaction":<String_value>,"hits":<Double_value>,"referencecount":<Double_value>,"undefhits":<Double_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/contentinspectionaction/name_value&lt;String&gt;
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/contentinspectionaction/name_value&lt;String&gt;?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/contentinspectionaction/name_value&lt;String&gt;?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "contentinspectionaction": [ {"name":<String_value>,"type":<String_value>,"servername":<String_value>,"serverip":<String_value>,"serverport":<Double_value>,"icapprofilename":<String_value>,"ifserverdown":<String_value>,"reqtimeout":<Double_value>,"reqtimeoutaction":<String_value>,"hits":<Double_value>,"referencecount":<Double_value>,"undefhits":<Double_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/contentinspectionaction?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "contentinspectionaction": [ { "__count": "#no"} ] }```



