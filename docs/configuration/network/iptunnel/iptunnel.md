#iptunnel

Configuration for ip Tunnel resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the IP tunnel. Leading character must be a number or letter. Other characters allowed, after the first character, are @ _ - . (period) : (colon) # and space ( ).<br>Minimum length = 1</td></tr><tr><td>remote</td><td>&lt;String></td><td>Read-write</td><td>Public IPv4 address, of the remote device, used to set up the tunnel. For this parameter, you can alternatively specify a network address.<br>Minimum length = 1</td></tr><tr><td>remotesubnetmask</td><td>&lt;String></td><td>Read-write</td><td>Subnet mask of the remote IP address of the tunnel.</td></tr><tr><td>local</td><td>&lt;String></td><td>Read-write</td><td>Type ofNetScaler owned public IPv4 address, configured on the local NetScaler appliance and used to set up the tunnel.</td></tr><tr><td>protocol</td><td>&lt;String></td><td>Read-write</td><td>Name of the protocol to be used on this tunnel.<br>Default value: IPIP<br>Possible values = IPIP, GRE, IPSEC</td></tr><tr><td>grepayload</td><td>&lt;String></td><td>Read-write</td><td>The payload GRE will carry.<br>Default value: ETHERNETwithDOT1Q<br>Possible values = ETHERNETwithDOT1Q, ETHERNET, IP</td></tr><tr><td>ipsecprofilename</td><td>&lt;String></td><td>Read-write</td><td>Name of IPSec profile to be associated.<br>Default value: "ns_ipsec_default_profile"</td></tr><tr><td>vlan</td><td>&lt;Double></td><td>Read-write</td><td>The vlan for mulicast packets.<br>Minimum value = 1<br>Maximum value = 4094</td></tr><tr><td>ownergroup</td><td>&lt;String></td><td>Read-write</td><td>The owner node group in a Cluster for the iptunnel.<br>Default value: DEFAULT_NG<br>Minimum length = 1</td></tr><tr><td>sysname</td><td>&lt;String></td><td>Read-only</td><td>The name of the ip tunnel.</td></tr><tr><td>type</td><td>&lt;Double></td><td>Read-only</td><td>The type of this tunnel.</td></tr><tr><td>encapip</td><td>&lt;String></td><td>Read-only</td><td>The effective local IP address of the tunnel. Used as the source of the encapsulated packets.</td></tr><tr><td>channel</td><td>&lt;Double></td><td>Read-only</td><td>The tunnel that is bound to a netbridge.</td></tr><tr><td>tunneltype</td><td>&lt;String[]></td><td>Read-only</td><td>Indicates that a tunnel is User-Configured, Internal or DELETE-IN-PROGRESS.<br>Possible values = Configured, Delete-In-Progress</td></tr><tr><td>ipsectunnelstatus</td><td>&lt;String></td><td>Read-only</td><td>Whether the ipsec on this tunnel is up or down.<br>Possible values = DOWN, UP, PARTIAL-UP, UNKNOWN</td></tr><tr><td>refcnt</td><td>&lt;Double></td><td>Read-only</td><td>Number of PBRs to bound to this iptunnel.</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD]()| [DELETE](#d)| [GET (ALL)](#get-)| [GET]()| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/iptunnel
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"iptunnel":{<b>"name":<String_value>,</b><b>"remote":<String_value>,</b><b>"remotesubnetmask":<String_value>,</b><b>"local":<String_value>,</b>"protocol":<String_value>,"grepayload":<String_value>,"ipsecprofilename":<String_value>,"vlan":<Double_value>,"ownergroup":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/iptunnel/name_value&lt;String&gt;
<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/iptunnel
<b>Query-parameters:</b>
<b>args</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/iptunnel?<b>args=remote:&lt;String_value&gt;,remotesubnetmask:&lt;String_value&gt;,name:&lt;String_value&gt;</b>
Use this query-parameter to get iptunnel resources based on additional properties.


<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/iptunnel?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/iptunnel?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of iptunnel resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/iptunnel?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/iptunnel?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the iptunnel resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "iptunnel": [ {remote:<String_value>,remotesubnetmask:<String_value>,name:<String_value>"sysname":<String_value>,"local":<String_value>,"protocol":<String_value>,"grepayload":<String_value>,"type":<Double_value>,"encapip":<String_value>,"channel":<Double_value>,"ipsecprofilename":<String_value>,"vlan":<Double_value>,"tunneltype":<String[]_value>,"ipsectunnelstatus":<String_value>,"ownergroup":<String_value>,"refcnt":<Double_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/iptunnel/name_value&lt;String&gt;
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/iptunnel/name_value&lt;String&gt;?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/iptunnel/name_value&lt;String&gt;?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "iptunnel": [ {remote:<String_value>,remotesubnetmask:<String_value>,name:<String_value>"sysname":<String_value>,"local":<String_value>,"protocol":<String_value>,"grepayload":<String_value>,"type":<Double_value>,"encapip":<String_value>,"channel":<Double_value>,"ipsecprofilename":<String_value>,"vlan":<Double_value>,"tunneltype":<String[]_value>,"ipsectunnelstatus":<String_value>,"ownergroup":<String_value>,"refcnt":<Double_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/iptunnel?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "iptunnel": [ { "__count": "#no"} ] }```



