#lsndeterministicnat

Configuration for deterministic NAT resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>clientname</td><td>&lt;String></td><td>Read-write</td><td>The name of the LSN Client.</td></tr><tr><td>network6</td><td>&lt;String></td><td>Read-write</td><td>IPv6 address of the LSN subscriber or B4 device.</td></tr><tr><td>subscrip</td><td>&lt;String></td><td>Read-write</td><td>The Client IP address.</td></tr><tr><td>td</td><td>&lt;Double></td><td>Read-write</td><td>The LSN client TD.<br>Default value: 0<br>Minimum value = 0<br>Maximum value = 4094</td></tr><tr><td>natip</td><td>&lt;String></td><td>Read-write</td><td>The NAT IP address.<br>Minimum length = 1</td></tr><tr><td>natprefix</td><td>&lt;String></td><td>Read-only</td><td>IPv6 address of the LSN subscriber network(B4-Device) on whose traffic the NetScaler ADC perform Large Scale NAT.</td></tr><tr><td>subscrip2</td><td>&lt;String></td><td>Read-only</td><td>The Subscriber IP address.</td></tr><tr><td>natip2</td><td>&lt;String></td><td>Read-only</td><td>The NAT IP address.</td></tr><tr><td>firstport</td><td>&lt;Integer></td><td>Read-only</td><td>The Application Protocol Port of the Profile.<br>Minimum value = 1<br>Maximum value = 65535</td></tr><tr><td>lastport</td><td>&lt;Integer></td><td>Read-only</td><td>The Application Protocol Ending Port of the Profile.<br>Minimum value = 1<br>Maximum value = 65535</td></tr><tr><td>srctd</td><td>&lt;Double></td><td>Read-only</td><td>The LSN client TD.<br>Minimum value = 0<br>Maximum value = 4094</td></tr><tr><td>nattype</td><td>&lt;String></td><td>Read-only</td><td>Type of subscriber info(ex: nat44 or ds-lite).<br>Default value: NAT44<br>Possible values = NAT44, DS-Lite, NAT64</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[GET (ALL)](#get-)| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsndeterministicnat
<b>Query-parameters:</b>
<b>args</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsndeterministicnat?<b>args=clientname:&lt;String_value&gt;,network6:&lt;String_value&gt;,subscrip:&lt;String_value&gt;,td:&lt;Double_value&gt;,natip:&lt;String_value&gt;</b>
Use this query-parameter to get lsndeterministicnat resources based on additional properties.


<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsndeterministicnat?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsndeterministicnat?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of lsndeterministicnat resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsndeterministicnat?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsndeterministicnat?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the lsndeterministicnat resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "lsndeterministicnat": [ {clientname:<String_value>,network6:<String_value>,subscrip:<String_value>,td:<Double_value>,natip:<String_value>"natprefix":<String_value>,"subscrip2":<String_value>,"natip2":<String_value>,"firstport":<Integer_value>,"lastport":<Integer_value>,"srctd":<Double_value>,"nattype":<String_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsndeterministicnat?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "lsndeterministicnat": [ { "__count": "#no"} ] }```



