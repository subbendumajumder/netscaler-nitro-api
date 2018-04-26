#inat

Configuration for inbound nat resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the Inbound NAT (INAT) entry. Leading character must be a number or letter. Other characters allowed, after the first character, are @ _ - . (period) : (colon) # and space ( ).<br>Minimum length = 1</td></tr><tr><td>publicip</td><td>&lt;String></td><td>Read-write</td><td>Public IP address of packets received on the NetScaler appliance. Can be aNetScaler-owned VIP or VIP6 address.<br>Minimum length = 1</td></tr><tr><td>privateip</td><td>&lt;String></td><td>Read-write</td><td>IP address of the server to which the packet is sent by the NetScaler. Can be an IPv4 or IPv6 address.<br>Minimum length = 1</td></tr><tr><td>mode</td><td>&lt;String></td><td>Read-write</td><td>Stateless translation.<br>Possible values = STATELESS</td></tr><tr><td>tcpproxy</td><td>&lt;String></td><td>Read-write</td><td>Enable TCP proxy, which enables the NetScaler appliance to optimize the RNAT TCP traffic by using Layer 4 features.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>ftp</td><td>&lt;String></td><td>Read-write</td><td>Enable the FTP protocol on the server for transferring files between the client and the server.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>tftp</td><td>&lt;String></td><td>Read-write</td><td>To enable/disable TFTP (Default DISABLED).<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>usip</td><td>&lt;String></td><td>Read-write</td><td>Enable the NetScaler appliance to retain the source IP address of packets before sending the packets to the server.<br>Possible values = ON, OFF</td></tr><tr><td>usnip</td><td>&lt;String></td><td>Read-write</td><td>Enable the NetScaler appliance to use a SNIP address as the source IP address of packets before sending the packets to the server.<br>Possible values = ON, OFF</td></tr><tr><td>proxyip</td><td>&lt;String></td><td>Read-write</td><td>Unique IP address used as the source IP address in packets sent to the server. Must be a MIP or SNIP address.</td></tr><tr><td>useproxyport</td><td>&lt;String></td><td>Read-write</td><td>Enable the NetScaler appliance to proxy the source port of packets before sending the packets to the server.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>td</td><td>&lt;Double></td><td>Read-write</td><td>Integer value that uniquely identifies the traffic domain in which you want to configure the entity. If you do not specify an ID, the entity becomes part of the default traffic domain, which has an ID of 0.<br>Minimum value = 0<br>Maximum value = 4094</td></tr><tr><td>flags</td><td>&lt;Double></td><td>Read-only</td><td>Flags for different modes.</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD]()| [DELETE](#d)| [UPDATE](#u)| [UNSET](#)| [GET (ALL)](#get-)| [GET]()| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/inat
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"inat":{<b>"name":<String_value>,</b><b>"publicip":<String_value>,</b><b>"privateip":<String_value>,</b>"mode":<String_value>,"tcpproxy":<String_value>,"ftp":<String_value>,"tftp":<String_value>,"usip":<String_value>,"usnip":<String_value>,"proxyip":<String_value>,"useproxyport":<String_value>,"td":<Double_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/inat/name_value&lt;String&gt;
<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/inat
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"inat":{<b>"name":<String_value>,</b>"privateip":<String_value>,"tcpproxy":<String_value>,"ftp":<String_value>,"tftp":<String_value>,"usip":<String_value>,"usnip":<String_value>,"proxyip":<String_value>,"useproxyport":<String_value>,"mode":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/inat?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"inat":{<b>"name":<String_value>,</b>"tcpproxy":true,"ftp":true,"tftp":true,"usip":true,"usnip":true,"proxyip":true,"useproxyport":true,"mode":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/inat
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/inat?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/inat?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of inat resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/inat?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/inat?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the inat resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "inat": [ {"name":<String_value>,"publicip":<String_value>,"privateip":<String_value>,"proxyip":<String_value>,"tcpproxy":<String_value>,"ftp":<String_value>,"tftp":<String_value>,"usip":<String_value>,"usnip":<String_value>,"useproxyport":<String_value>,"flags":<Double_value>,"mode":<String_value>,"td":<Double_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/inat/name_value&lt;String&gt;
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/inat/name_value&lt;String&gt;?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/inat/name_value&lt;String&gt;?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "inat": [ {"name":<String_value>,"publicip":<String_value>,"privateip":<String_value>,"proxyip":<String_value>,"tcpproxy":<String_value>,"ftp":<String_value>,"tftp":<String_value>,"usip":<String_value>,"usnip":<String_value>,"useproxyport":<String_value>,"flags":<Double_value>,"mode":<String_value>,"td":<Double_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/inat?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "inat": [ { "__count": "#no"} ] }```



