#ipsecalgsession

Configuration for IPSEC ALG session resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>sourceip_alg</td><td>&lt;String></td><td>Read-write</td><td>Original Source IP address.<br>Minimum length = 1</td></tr><tr><td>natip_alg</td><td>&lt;String></td><td>Read-write</td><td>Natted Source IP address.<br>Minimum length = 1</td></tr><tr><td>destip_alg</td><td>&lt;String></td><td>Read-write</td><td>Destination IP address.<br>Minimum length = 1</td></tr><tr><td>sourceip</td><td>&lt;String></td><td>Read-write</td><td>Original Source IP address.<br>Minimum length = 1</td></tr><tr><td>natip</td><td>&lt;String></td><td>Read-write</td><td>Natted Source IP address.<br>Minimum length = 1</td></tr><tr><td>destip</td><td>&lt;String></td><td>Read-write</td><td>Destination IP address.<br>Minimum length = 1</td></tr><tr><td>spiin</td><td>&lt;Double></td><td>Read-only</td><td>Client SPI for ESP.</td></tr><tr><td>spiout</td><td>&lt;Double></td><td>Read-only</td><td>Server SPI for ESP.</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[FLUSH](#)| [GET (ALL)](#get-)| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###flush



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/ipsecalgsession?<b>action=flush</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"ipsecalgsession":{"sourceip":<String_value>,"natip":<String_value>,"destip":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/ipsecalgsession
<b>Query-parameters:</b>
<b>args</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/ipsecalgsession?<b>args=sourceip_alg:&lt;String_value&gt;,natip_alg:&lt;String_value&gt;,destip_alg:&lt;String_value&gt;</b>
Use this query-parameter to get ipsecalgsession resources based on additional properties.


<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/ipsecalgsession?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/ipsecalgsession?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of ipsecalgsession resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/ipsecalgsession?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/ipsecalgsession?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the ipsecalgsession resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "ipsecalgsession": [ {sourceip_alg:<String_value>,natip_alg:<String_value>,destip_alg:<String_value>"sourceip":<String_value>,"natip":<String_value>,"destip":<String_value>,"spiin":<Double_value>,"spiout":<Double_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/ipsecalgsession?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "ipsecalgsession": [ { "__count": "#no"} ] }```



