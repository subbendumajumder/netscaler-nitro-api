#locationparameter

Configuration for location parameter resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>context</td><td>&lt;String></td><td>Read-write</td><td>Context for describing locations. In geographic context, qualifier labels are assigned by default in the following sequence: Continent.Country.Region.City.ISP.Organization. In custom context, the qualifiers labels can have any meaning that you designate.<br>Possible values = geographic, custom</td></tr><tr><td>q1label</td><td>&lt;String></td><td>Read-write</td><td>Label specifying the meaning of the first qualifier. Can be specified for custom context only.<br>Minimum length = 1</td></tr><tr><td>q2label</td><td>&lt;String></td><td>Read-write</td><td>Label specifying the meaning of the second qualifier. Can be specified for custom context only.<br>Minimum length = 1</td></tr><tr><td>q3label</td><td>&lt;String></td><td>Read-write</td><td>Label specifying the meaning of the third qualifier. Can be specified for custom context only.<br>Minimum length = 1</td></tr><tr><td>q4label</td><td>&lt;String></td><td>Read-write</td><td>Label specifying the meaning of the fourth qualifier. Can be specified for custom context only.<br>Minimum length = 1</td></tr><tr><td>q5label</td><td>&lt;String></td><td>Read-write</td><td>Label specifying the meaning of the fifth qualifier. Can be specified for custom context only.<br>Minimum length = 1</td></tr><tr><td>q6label</td><td>&lt;String></td><td>Read-write</td><td>Label specifying the meaning of the sixth qualifier. Can be specified for custom context only.<br>Minimum length = 1</td></tr><tr><td>Locationfile</td><td>&lt;String></td><td>Read-only</td><td>Currently loaded location database file.</td></tr><tr><td>format</td><td>&lt;String></td><td>Read-only</td><td>Location file format.<br>Possible values = netscaler, ip-country, ip-country-isp, ip-country-region-city, ip-country-region-city-isp, geoip-country, geoip-region, geoip-city, geoip-country-org, geoip-country-isp, geoip-city-isp-org</td></tr><tr><td>custom</td><td>&lt;Double></td><td>Read-only</td><td>Number of configured custom locations.</td></tr><tr><td>Static</td><td>&lt;Double></td><td>Read-only</td><td>Number of configured locations in the database file (static locations).</td></tr><tr><td>lines</td><td>&lt;Double></td><td>Read-only</td><td>Number of lines in the databse files.</td></tr><tr><td>errors</td><td>&lt;Double></td><td>Read-only</td><td>Number of errros encountered while reading the database file.</td></tr><tr><td>warnings</td><td>&lt;Double></td><td>Read-only</td><td>Number of warnings encountered while reading the database file.</td></tr><tr><td>entries</td><td>&lt;Double></td><td>Read-only</td><td>Number of successfully added entries.</td></tr><tr><td>locationfile6</td><td>&lt;String></td><td>Read-only</td><td>Currently loaded location database file.</td></tr><tr><td>format6</td><td>&lt;String></td><td>Read-only</td><td>Location file format.<br>Possible values = netscaler6, geoip-country6</td></tr><tr><td>custom6</td><td>&lt;Double></td><td>Read-only</td><td>Number of configured custom locations.</td></tr><tr><td>static6</td><td>&lt;Double></td><td>Read-only</td><td>Number of configured locations in the database file (static locations).</td></tr><tr><td>lines6</td><td>&lt;Double></td><td>Read-only</td><td>Number of lines in the databse files.</td></tr><tr><td>errors6</td><td>&lt;Double></td><td>Read-only</td><td>Number of errros encountered while reading the database file.</td></tr><tr><td>warnings6</td><td>&lt;Double></td><td>Read-only</td><td>Number of warnings encountered while reading the database file.</td></tr><tr><td>entries6</td><td>&lt;Double></td><td>Read-only</td><td>Number of successfully added entries.</td></tr><tr><td>flags</td><td>&lt;Double></td><td>Read-only</td><td>Information needed for display. This argument passes information from the kernel to the user space.</td></tr><tr><td>status</td><td>&lt;Double></td><td>Read-only</td><td>This argument displays when the status (success or failure) of database loading.</td></tr><tr><td>databasemode</td><td>&lt;String></td><td>Read-only</td><td>This argument displays the database mode.<br>Possible values = File, Internal, Not applicable</td></tr><tr><td>flushing</td><td>&lt;String></td><td>Read-only</td><td>This argument displays the state of flushing.<br>Possible values = In progress, Idle</td></tr><tr><td>loading</td><td>&lt;String></td><td>Read-only</td><td>This argument displays the state of loading.<br>Possible values = In progress, Idle</td></tr><tr><td>matchwildcardtoany</td><td>&lt;String></td><td>Read-only</td><td>Indicates whether wildcard qualifiers should match any other qualifier including non-wildcard. Option to fallback after default behavior changes to not match.<br>Default value: NO<br>Possible values = YES, NO</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[UPDATE](#u)| [UNSET](#)| [GET (ALL)](#get-)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/locationparameter
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"locationparameter":{"context":<String_value>,"q1label":<String_value>,"q2label":<String_value>,"q3label":<String_value>,"q4label":<String_value>,"q5label":<String_value>,"q6label":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/locationparameter?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"locationparameter":{"context":true,"q1label":true,"q2label":true,"q3label":true,"q4label":true,"q5label":true,"q6label":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/locationparameter
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "locationparameter": [ {"context":<String_value>,"q1label":<String_value>,"q2label":<String_value>,"q3label":<String_value>,"q4label":<String_value>,"q5label":<String_value>,"q6label":<String_value>,"Locationfile":<String_value>,"format":<String_value>,"custom":<Double_value>,"Static":<Double_value>,"lines":<Double_value>,"errors":<Double_value>,"warnings":<Double_value>,"entries":<Double_value>,"locationfile6":<String_value>,"format6":<String_value>,"custom6":<Double_value>,"static6":<Double_value>,"lines6":<Double_value>,"errors6":<Double_value>,"warnings6":<Double_value>,"entries6":<Double_value>,"flags":<Double_value>,"status":<Double_value>,"databasemode":<String_value>,"flushing":<String_value>,"loading":<String_value>,"matchwildcardtoany":<String_value>}]}```



