#vpnintranetapplication

Configuration for SSLVPN intranet application resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>intranetapplication</td><td>&lt;String></td><td>Read-write</td><td>Name of the intranet application.<br>Minimum length = 1<br>Maximum length = 31</td></tr><tr><td>protocol</td><td>&lt;String></td><td>Read-write</td><td>Protocol used by the intranet application. If protocol is set to BOTH, TCP and UDP traffic is allowed.<br>Possible values = TCP, UDP, ANY</td></tr><tr><td>destip</td><td>&lt;String></td><td>Read-write</td><td>Destination IP address, IP range, or host name of the intranet application. This address is the server IP address.<br>Minimum length = 1</td></tr><tr><td>netmask</td><td>&lt;String></td><td>Read-write</td><td>Destination subnet mask for the intranet application.</td></tr><tr><td>iprange</td><td>&lt;String></td><td>Read-write</td><td>If you have multiple servers in your network, such as web, email, and file shares, configure an intranet application that includes the IP range for all the network applications. This allows users to access all the intranet applications contained in the IP address range.<br>Minimum length = 1</td></tr><tr><td>hostname</td><td>&lt;String></td><td>Read-write</td><td>Name of the host for which to configure interception. The names are resolved during interception when users log on with the NetScaler Gateway Plug-in.<br>Minimum length = 1</td></tr><tr><td>clientapplication</td><td>&lt;String[]></td><td>Read-write</td><td>Names of the client applications, such as PuTTY and Xshell.<br>Minimum length = 1</td></tr><tr><td>spoofiip</td><td>&lt;String></td><td>Read-write</td><td>IP address that the intranet application will use to route the connection through the virtual adapter.<br>Default value: ON<br>Possible values = ON, OFF</td></tr><tr><td>destport</td><td>&lt;String></td><td>Read-write</td><td>Destination TCP or UDP port number for the intranet application. Use a hyphen to specify a range of port numbers, for example 90-95.<br>Minimum length = 1</td></tr><tr><td>interception</td><td>&lt;String></td><td>Read-write</td><td>Interception mode for the intranet application or resource. Correct value depends on the type of client software used to make connections. If the interception mode is set to TRANSPARENT, users connect with the NetScaler Gateway Plug-in for Windows. With the PROXY setting, users connect with the NetScaler Gateway Plug-in for Java.<br>Possible values = PROXY, TRANSPARENT</td></tr><tr><td>srcip</td><td>&lt;String></td><td>Read-write</td><td>Source IP address. Required if interception mode is set to PROXY. Default is the loopback address, 127.0.0.1.<br>Minimum length = 1</td></tr><tr><td>srcport</td><td>&lt;Integer></td><td>Read-write</td><td>Source port for the application for which the NetScaler Gateway virtual server proxies the traffic. If users are connecting from a device that uses the NetScaler Gateway Plug-in for Java, applications must be configured manually by using the source IP address and TCP port values specified in the intranet application profile. If a port value is not set, the destination port value is used.<br>Minimum value = 1</td></tr><tr><td>ipaddress</td><td>&lt;String></td><td>Read-only</td><td>The IP address for the application. This address is the real application server IP address.</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD]()| [DELETE](#d)| [GET (ALL)](#get-)| [GET]()| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnintranetapplication
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"vpnintranetapplication":{<b>"intranetapplication":<String_value>,</b>"protocol":<String_value>,"destip":<String_value>,"netmask":<String_value>,"iprange":<String_value>,"hostname":<String_value>,"clientapplication":<String[]_value>,"spoofiip":<String_value>,"destport":<String_value>,"interception":<String_value>,"srcip":<String_value>,"srcport":<Integer_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnintranetapplication/intranetapplication_value&lt;String&gt;
<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnintranetapplication
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnintranetapplication?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnintranetapplication?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of vpnintranetapplication resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnintranetapplication?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnintranetapplication?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the vpnintranetapplication resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "vpnintranetapplication": [ {"intranetapplication":<String_value>,"protocol":<String_value>,"destip":<String_value>,"netmask":<String_value>,"ipaddress":<String_value>,"hostname":<String_value>,"destport":<String_value>,"clientapplication":<String[]_value>,"spoofiip":<String_value>,"interception":<String_value>,"srcip":<String_value>,"srcport":<Integer_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnintranetapplication/intranetapplication_value&lt;String&gt;
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnintranetapplication/intranetapplication_value&lt;String&gt;?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnintranetapplication/intranetapplication_value&lt;String&gt;?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "vpnintranetapplication": [ {"intranetapplication":<String_value>,"protocol":<String_value>,"destip":<String_value>,"netmask":<String_value>,"ipaddress":<String_value>,"hostname":<String_value>,"destport":<String_value>,"clientapplication":<String[]_value>,"spoofiip":<String_value>,"interception":<String_value>,"srcip":<String_value>,"srcport":<Integer_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnintranetapplication?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "vpnintranetapplication": [ { "__count": "#no"} ] }```



