#nslimitsessions

Configuration for limit sessions resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>limitidentifier</td><td>&lt;String></td><td>Read-write</td><td>Name of the rate limit identifier for which to display the sessions.<br>Minimum length = 1</td></tr><tr><td>detail</td><td>&lt;Boolean></td><td>Read-write</td><td>Show the individual hash values.</td></tr><tr><td>timeout</td><td>&lt;Double></td><td>Read-only</td><td>The time remaining on the session before a flush can be attempted. If active transactions are present the session will not be flushed.</td></tr><tr><td>hits</td><td>&lt;Double></td><td>Read-only</td><td>The number of times this entry was hit.</td></tr><tr><td>drop</td><td>&lt;Double></td><td>Read-only</td><td>The number of times action was taken.</td></tr><tr><td>number</td><td>&lt;Double[]></td><td>Read-only</td><td>The hash of the matched selectlets.</td></tr><tr><td>name</td><td>&lt;String></td><td>Read-only</td><td>The string formed by gathering selectlet values.</td></tr><tr><td>unit</td><td>&lt;Double></td><td>Read-only</td><td>Total computed hash of the matched selectlets.</td></tr><tr><td>flags</td><td>&lt;Double></td><td>Read-only</td><td>Used internally to identify ip addresses.</td></tr><tr><td>referencecount</td><td>&lt;Double></td><td>Read-only</td><td>Total number of transactions pointing to this entry. Its the sum total of the connection and bandwidth references.</td></tr><tr><td>maxbandwidth</td><td>&lt;Double></td><td>Read-only</td><td>The current bandwidth.</td></tr><tr><td>selectoripv61</td><td>&lt;String></td><td>Read-only</td><td>First IPV6 address gathered.</td></tr><tr><td>selectoripv62</td><td>&lt;String></td><td>Read-only</td><td>Second IPV6 address gathered.</td></tr><tr><td>flag</td><td>&lt;Double></td><td>Read-only</td><td>Used internally to identify ipv6 addresses.</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[CLEAR](#)| [GET (ALL)](#get-)| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###clear



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nslimitsessions?<b>action=clear</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"nslimitsessions":{<b>"limitidentifier":<String_value></b>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nslimitsessions
<b>Query-parameters:</b>
<b>args</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nslimitsessions?<b>args=<b>limitidentifier:&lt;String_value&gt;,</b>detail:&lt;Boolean_value&gt;</b>
Use this query-parameter to get nslimitsessions resources based on additional properties.


<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nslimitsessions?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nslimitsessions?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of nslimitsessions resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nslimitsessions?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nslimitsessions?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the nslimitsessions resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "nslimitsessions": [ {<b>limitidentifier:<String_value>,</b>detail:<Boolean_value>"timeout":<Double_value>,"hits":<Double_value>,"drop":<Double_value>,"number":<Double[]_value>,"name":<String_value>,"unit":<Double_value>,"flags":<Double_value>,"referencecount":<Double_value>,"maxbandwidth":<Double_value>,"selectoripv61":<String_value>,"selectoripv62":<String_value>,"flag":<Double_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nslimitsessions?<b>args=<b>limitidentifier:&lt;String_value&gt;,</b>detail:&lt;Boolean_value&gt;;count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "nslimitsessions": [ { "__count": "#no"} ] }```



