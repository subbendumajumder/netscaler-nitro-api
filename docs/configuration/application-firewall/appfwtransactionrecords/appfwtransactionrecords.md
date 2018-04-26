#appfwtransactionrecords

Configuration for Application firewall transaction record resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>nodeid</td><td>&lt;Double></td><td>Read-write</td><td>Unique number that identifies the cluster node.<br>Minimum value = 0<br>Maximum value = 31</td></tr><tr><td>httptransactionid</td><td>&lt;Double></td><td>Read-only</td><td>The http transaction identifier.</td></tr><tr><td>packetengineid</td><td>&lt;Integer></td><td>Read-only</td><td>The packet engine identifier.</td></tr><tr><td>appfwsessionid</td><td>&lt;String></td><td>Read-only</td><td>The session identifier set by the Application Firewall to track the user session.</td></tr><tr><td>profilename</td><td>&lt;String></td><td>Read-only</td><td>Application Firewall profile name.</td></tr><tr><td>url</td><td>&lt;String></td><td>Read-only</td><td>Request URL.</td></tr><tr><td>clientip</td><td>&lt;String></td><td>Read-only</td><td>The IP address of client.</td></tr><tr><td>destip</td><td>&lt;String></td><td>Read-only</td><td>The IP address of destination.</td></tr><tr><td>starttime</td><td>&lt;String></td><td>Read-only</td><td>Conveys time at which request processing started.</td></tr><tr><td>endtime</td><td>&lt;String></td><td>Read-only</td><td>Conveys time at which request processing end.</td></tr><tr><td>requestcontentlength</td><td>&lt;Integer></td><td>Read-only</td><td>The content length of request.</td></tr><tr><td>requestyields</td><td>&lt;Double></td><td>Read-only</td><td>The number of times yielded during request processing to send heart beat packets.</td></tr><tr><td>requestmaxprocessingtime</td><td>&lt;Double></td><td>Read-only</td><td>The maximum processing time across yields during request processing.</td></tr><tr><td>responsecontentlength</td><td>&lt;Integer></td><td>Read-only</td><td>The content length of response.</td></tr><tr><td>responseyields</td><td>&lt;Double></td><td>Read-only</td><td>The number of times yielded during response processing to send heart beat packets.</td></tr><tr><td>responsemaxprocessingtime</td><td>&lt;Double></td><td>Read-only</td><td>The maximum processing time across yields during response processing.</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[GET (ALL)](#get-)| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appfwtransactionrecords
<b>Query-parameters:</b>
<b>args</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appfwtransactionrecords?<b>args=nodeid:&lt;Double_value&gt;</b>
Use this query-parameter to get appfwtransactionrecords resources based on additional properties.


<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appfwtransactionrecords?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appfwtransactionrecords?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of appfwtransactionrecords resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appfwtransactionrecords?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appfwtransactionrecords?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the appfwtransactionrecords resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "appfwtransactionrecords": [ {nodeid:<Double_value>"httptransactionid":<Double_value>,"packetengineid":<Integer_value>,"appfwsessionid":<String_value>,"profilename":<String_value>,"url":<String_value>,"clientip":<String_value>,"destip":<String_value>,"starttime":<String_value>,"endtime":<String_value>,"requestcontentlength":<Integer_value>,"requestyields":<Double_value>,"requestmaxprocessingtime":<Double_value>,"responsecontentlength":<Integer_value>,"responseyields":<Double_value>,"responsemaxprocessingtime":<Double_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appfwtransactionrecords?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "appfwtransactionrecords": [ { "__count": "#no"} ] }```



