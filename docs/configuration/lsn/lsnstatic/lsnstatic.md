#lsnstatic

Configuration for static mapping resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the LSN static mapping entry. Must begin with an ASCII alphanumeric or underscore (_) character, and must contain only ASCII alphanumeric, underscore, hash (#), period (.), space, colon (:), at (@), equals (=), and hyphen (-) characters. Cannot be changed after the LSN group is created. The following requirement applies only to the NetScaler CLI: If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "lsn static1" or 'lsn static1').<br>Minimum length = 1<br>Maximum length = 127</td></tr><tr><td>transportprotocol</td><td>&lt;String></td><td>Read-write</td><td>Protocol for the LSN mapping entry.<br>Possible values = TCP, UDP, ICMP, ALL</td></tr><tr><td>subscrip</td><td>&lt;String></td><td>Read-write</td><td>IPv4(NAT44 ; DS-Lite)/IPv6(NAT64) address of an LSN subscriber for the LSN static mapping entry.</td></tr><tr><td>subscrport</td><td>&lt;Integer></td><td>Read-write</td><td>Port of the LSN subscriber for the LSN mapping entry. * represents all ports being used. Used in case of static wildcard.<br>Minimum value = 0<br>Maximum value = 65535<br>Range 1 - 65535<br>* in CLI is represented as 65535 in NITRO API</td></tr><tr><td>network6</td><td>&lt;String></td><td>Read-write</td><td>B4 address in DS-Lite setup.<br>Minimum length = 1</td></tr><tr><td>td</td><td>&lt;Double></td><td>Read-write</td><td>ID of the traffic domain to which the subscriber belongs. <br><br>If you do not specify an ID, the subscriber is assumed to be a part of the default traffic domain.<br>Default value: 0<br>Minimum value = 0<br>Maximum value = 4094</td></tr><tr><td>natip</td><td>&lt;String></td><td>Read-write</td><td>IPv4 address, already existing on the NetScaler ADC as type LSN, to be used as NAT IP address for this mapping entry.</td></tr><tr><td>natport</td><td>&lt;Integer></td><td>Read-write</td><td>NAT port for this LSN mapping entry. * represents all ports being used. Used in case of static wildcard.<br>Minimum value = 0<br>Maximum value = 65535<br>Range 1 - 65535<br>* in CLI is represented as 65535 in NITRO API</td></tr><tr><td>destip</td><td>&lt;String></td><td>Read-write</td><td>Destination IP address for the LSN mapping entry.</td></tr><tr><td>dsttd</td><td>&lt;Double></td><td>Read-write</td><td>ID of the traffic domain through which the destination IP address for this LSN mapping entry is reachable from the NetScaler ADC.<br><br>If you do not specify an ID, the destination IP address is assumed to be reachable through the default traffic domain, which has an ID of 0.<br>Default value: 0<br>Minimum value = 0<br>Maximum value = 4094</td></tr><tr><td>nattype</td><td>&lt;String></td><td>Read-write</td><td>Type of sessions to be displayed.<br>Possible values = NAT44, DS-Lite, NAT64</td></tr><tr><td>status</td><td>&lt;String></td><td>Read-only</td><td>The status of the Mapping. Status could be Inactive, if mapping addition failed due to already existing dynamic/static mapping, port allocation failure.<br>Possible values = ACTIVE, INACTIVE</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD]()| [DELETE](#d)| [GET (ALL)](#get-)| [GET]()| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsnstatic
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"lsnstatic":{<b>"name":<String_value>,</b><b>"transportprotocol":<String_value>,</b><b>"subscrip":<String_value>,</b><b>"subscrport":<Integer_value>,</b>"network6":<String_value>,"td":<Double_value>,"natip":<String_value>,"natport":<Integer_value>,"destip":<String_value>,"dsttd":<Double_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsnstatic/name_value&lt;String&gt;
<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsnstatic
<b>Query-parameters:</b>
<b>args</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsnstatic?<b>args=name:&lt;String_value&gt;,nattype:&lt;String_value&gt;</b>
Use this query-parameter to get lsnstatic resources based on additional properties.


<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsnstatic?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsnstatic?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of lsnstatic resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsnstatic?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsnstatic?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the lsnstatic resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "lsnstatic": [ {name:<String_value>,nattype:<String_value>"transportprotocol":<String_value>,"subscrip":<String_value>,"subscrport":<Integer_value>,"network6":<String_value>,"natip":<String_value>,"natport":<Integer_value>,"td":<Double_value>,"destip":<String_value>,"dsttd":<Double_value>,"status":<String_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsnstatic/name_value&lt;String&gt;
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsnstatic/name_value&lt;String&gt;?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsnstatic/name_value&lt;String&gt;?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "lsnstatic": [ {name:<String_value>,nattype:<String_value>"transportprotocol":<String_value>,"subscrip":<String_value>,"subscrport":<Integer_value>,"network6":<String_value>,"natip":<String_value>,"natport":<Integer_value>,"td":<Double_value>,"destip":<String_value>,"dsttd":<Double_value>,"status":<String_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsnstatic?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "lsnstatic": [ { "__count": "#no"} ] }```



