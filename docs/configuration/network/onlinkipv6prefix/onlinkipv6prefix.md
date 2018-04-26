#onlinkipv6prefix

Configuration for on-link IPv6 global prefixes for Router Advertisment resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>ipv6prefix</td><td>&lt;String></td><td>Read-write</td><td>Onlink prefixes for RA messages.</td></tr><tr><td>onlinkprefix</td><td>&lt;String></td><td>Read-write</td><td>RA Prefix onlink flag.<br>Default value: YES<br>Possible values = YES, NO</td></tr><tr><td>autonomusprefix</td><td>&lt;String></td><td>Read-write</td><td>RA Prefix Autonomus flag.<br>Default value: YES<br>Possible values = YES, NO</td></tr><tr><td>depricateprefix</td><td>&lt;String></td><td>Read-write</td><td>Depricate the prefix.<br>Default value: NO<br>Possible values = YES, NO</td></tr><tr><td>decrementprefixlifetimes</td><td>&lt;String></td><td>Read-write</td><td>RA Prefix Autonomus flag.<br>Default value: NO<br>Possible values = YES, NO</td></tr><tr><td>prefixvalidelifetime</td><td>&lt;Double></td><td>Read-write</td><td>Valide life time of the prefix, in seconds.<br>Default value: 2592000</td></tr><tr><td>prefixpreferredlifetime</td><td>&lt;Double></td><td>Read-write</td><td>Preferred life time of the prefix, in seconds.<br>Default value: 604800</td></tr><tr><td>prefixcurrvalidelft</td><td>&lt;Double></td><td>Read-only</td><td>Prefix current valid life time.</td></tr><tr><td>prefixcurrpreferredlft</td><td>&lt;Double></td><td>Read-only</td><td>Prefix current prefered life time.</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD]()| [DELETE](#d)| [UPDATE](#u)| [UNSET](#)| [GET (ALL)](#get-)| [GET]()| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/onlinkipv6prefix
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"onlinkipv6prefix":{<b>"ipv6prefix":<String_value>,</b>"onlinkprefix":<String_value>,"autonomusprefix":<String_value>,"depricateprefix":<String_value>,"decrementprefixlifetimes":<String_value>,"prefixvalidelifetime":<Double_value>,"prefixpreferredlifetime":<Double_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/onlinkipv6prefix/ipv6prefix_value&lt;String&gt;
<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/onlinkipv6prefix
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"onlinkipv6prefix":{<b>"ipv6prefix":<String_value>,</b>"onlinkprefix":<String_value>,"autonomusprefix":<String_value>,"depricateprefix":<String_value>,"decrementprefixlifetimes":<String_value>,"prefixvalidelifetime":<Double_value>,"prefixpreferredlifetime":<Double_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/onlinkipv6prefix?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"onlinkipv6prefix":{<b>"ipv6prefix":<String_value>,</b>"onlinkprefix":true,"autonomusprefix":true,"depricateprefix":true,"decrementprefixlifetimes":true,"prefixvalidelifetime":true,"prefixpreferredlifetime":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/onlinkipv6prefix
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/onlinkipv6prefix?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/onlinkipv6prefix?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of onlinkipv6prefix resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/onlinkipv6prefix?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/onlinkipv6prefix?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the onlinkipv6prefix resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "onlinkipv6prefix": [ {"ipv6prefix":<String_value>,"onlinkprefix":<String_value>,"autonomusprefix":<String_value>,"depricateprefix":<String_value>,"decrementprefixlifetimes":<String_value>,"prefixvalidelifetime":<Double_value>,"prefixpreferredlifetime":<Double_value>,"prefixcurrvalidelft":<Double_value>,"prefixcurrpreferredlft":<Double_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/onlinkipv6prefix/ipv6prefix_value&lt;String&gt;
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/onlinkipv6prefix/ipv6prefix_value&lt;String&gt;?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/onlinkipv6prefix/ipv6prefix_value&lt;String&gt;?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "onlinkipv6prefix": [ {"ipv6prefix":<String_value>,"onlinkprefix":<String_value>,"autonomusprefix":<String_value>,"depricateprefix":<String_value>,"decrementprefixlifetimes":<String_value>,"prefixvalidelifetime":<Double_value>,"prefixpreferredlifetime":<Double_value>,"prefixcurrvalidelft":<Double_value>,"prefixcurrpreferredlft":<Double_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/onlinkipv6prefix?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "onlinkipv6prefix": [ { "__count": "#no"} ] }```



