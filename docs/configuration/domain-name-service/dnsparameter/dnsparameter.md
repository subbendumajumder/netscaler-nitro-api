#dnsparameter

Configuration for DNS parameter resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>retries</td><td>&lt;Double></td><td>Read-write</td><td>Maximum number of retry attempts when no response is received for a query sent to a name server. Applies to end resolver and forwarder configurations.<br>Default value: 5<br>Minimum value = 1<br>Maximum value = 5</td></tr><tr><td>minttl</td><td>&lt;Double></td><td>Read-write</td><td>Minimum permissible time to live (TTL) for all records cached in the DNS cache by DNS proxy, end resolver, and forwarder configurations. If the TTL of a record that is to be cached is lower than the value configured for minTTL, the TTL of the record is set to the value of minTTL before caching. When you modify this setting, the new value is applied only to those records that are cached after the modification. The TTL values of existing records are not changed.<br>Minimum value = 0<br>Maximum value = 604800</td></tr><tr><td>maxttl</td><td>&lt;Double></td><td>Read-write</td><td>Maximum time to live (TTL) for all records cached in the DNS cache by DNS proxy, end resolver, and forwarder configurations. If the TTL of a record that is to be cached is higher than the value configured for maxTTL, the TTL of the record is set to the value of maxTTL before caching. When you modify this setting, the new value is applied only to those records that are cached after the modification. The TTL values of existing records are not changed.<br>Default value: 604800<br>Minimum value = 1<br>Maximum value = 604800</td></tr><tr><td>cacherecords</td><td>&lt;String></td><td>Read-write</td><td>Cache resource records in the DNS cache. Applies to resource records obtained through proxy configurations only. End resolver and forwarder configurations always cache records in the DNS cache, and you cannot disable this behavior. When you disable record caching, the appliance stops caching server responses. However, cached records are not flushed. The appliance does not serve requests from the cache until record caching is enabled again.<br>Default value: YES<br>Possible values = YES, NO</td></tr><tr><td>namelookuppriority</td><td>&lt;String></td><td>Read-write</td><td>Type of lookup (DNS or WINS) to attempt first. If the first-priority lookup fails, the second-priority lookup is attempted. Used only by the SSL VPN feature.<br>Default value: WINS<br>Possible values = WINS, DNS</td></tr><tr><td>recursion</td><td>&lt;String></td><td>Read-write</td><td>Function as an end resolver and recursively resolve queries for domains that are not hosted on the NetScaler appliance. Also resolve queries recursively when the external name servers configured on the appliance (for a forwarder configuration) are unavailable. When external name servers are unavailable, the appliance queries a root server and resolves the request recursively, as it does for an end resolver configuration.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>resolutionorder</td><td>&lt;String></td><td>Read-write</td><td>Type of DNS queries (A, AAAA, or both) to generate during the routine functioning of certain NetScaler features, such as SSL VPN, cache redirection, and the integrated cache. The queries are sent to the external name servers that are configured for the forwarder function. If you specify both query types, you can also specify the order. Available settings function as follows:<br>* OnlyAQuery. Send queries for IPv4 address records (A records) only. <br>* OnlyAAAAQuery. Send queries for IPv6 address records (AAAA records) instead of queries for IPv4 address records (A records).<br>* AThenAAAAQuery. Send a query for an A record, and then send a query for an AAAA record if the query for the A record results in a NODATA response from the name server.<br>* AAAAThenAQuery. Send a query for an AAAA record, and then send a query for an A record if the query for the AAAA record results in a NODATA response from the name server.<br>Default value: OnlyAQuery<br>Possible values = OnlyAQuery, OnlyAAAAQuery, AThenAAAAQuery, AAAAThenAQuery</td></tr><tr><td>dnssec</td><td>&lt;String></td><td>Read-write</td><td>Enable or disable the Domain Name System Security Extensions (DNSSEC) feature on the appliance. Note: Even when the DNSSEC feature is enabled, forwarder configurations (used by internal NetScaler features such as SSL VPN and Cache Redirection for name resolution) do not support the DNSSEC OK (DO) bit in the EDNS0 OPT header.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>maxpipeline</td><td>&lt;Double></td><td>Read-write</td><td>Maximum number of concurrent DNS requests to allow on a single client connection, which is identified by the &lt;clientip:port&gt;-&lt;vserver ip:port&gt; tuple. A value of 0 (zero) applies no limit to the number of concurrent DNS requests allowed on a single client connection.</td></tr><tr><td>dnsrootreferral</td><td>&lt;String></td><td>Read-write</td><td>Send a root referral if a client queries a domain name that is unrelated to the domains configured/cached on the NetScaler appliance. If the setting is disabled, the appliance sends a blank response instead of a root referral. Applicable to domains for which the appliance is authoritative. Disable the parameter when the appliance is under attack from a client that is sending a flood of queries for unrelated domains.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>dns64timeout</td><td>&lt;Double></td><td>Read-write</td><td>While doing DNS64 resolution, this parameter specifies the time to wait before sending an A query if no response is received from backend DNS server for AAAA query.<br>Minimum value = 0<br>Maximum value = 10000</td></tr><tr><td>ecsmaxsubnets</td><td>&lt;Double></td><td>Read-write</td><td>Maximum number of subnets that can be cached corresponding to a single domain. Subnet caching will occur for responses with EDNS Client Subnet (ECS) option. Caching of such responses can be disabled using DNS profile settings. A value of zero indicates that the number of subnets cached is limited only by existing memory constraints. The default value is zero.<br>Default value: 0<br>Minimum value = 0<br>Maximum value = 1280</td></tr><tr><td>maxnegcachettl</td><td>&lt;Double></td><td>Read-write</td><td>Maximum time to live (TTL) for all negative records ( NXDONAIN and NODATA ) cached in the DNS cache by DNS proxy, end resolver, and forwarder configurations. If the TTL of a record that is to be cached is higher than the value configured for maxnegcacheTTL, the TTL of the record is set to the value of maxnegcacheTTL before caching. When you modify this setting, the new value is applied only to those records that are cached after the modification. The TTL values of existing records are not changed.<br>Default value: 604800<br>Minimum value = 1<br>Maximum value = 604800</td></tr><tr><td>cachehitbypass</td><td>&lt;String></td><td>Read-write</td><td>This parameter is applicable only in proxy mode and if this parameter is enabled we will forward all the client requests to the backend DNS server and the response served will be cached on netscaler.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>maxcachesize</td><td>&lt;Double></td><td>Read-write</td><td>Maximum memory, in megabytes, that can be used for dns caching per Packet Engine.</td></tr><tr><td>maxnegativecachesize</td><td>&lt;Double></td><td>Read-write</td><td>Maximum memory, in megabytes, that can be used for caching of negative DNS responses per packet engine.</td></tr><tr><td>cachenoexpire</td><td>&lt;String></td><td>Read-write</td><td>If this flag is set to YES, the existing entries in cache do not age out. On reaching the max limit the cache records are frozen.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>splitpktqueryprocessing</td><td>&lt;String></td><td>Read-write</td><td>Processing requests split across multiple packets.<br>Default value: ALLOW<br>Possible values = ALLOW, DROP</td></tr><tr><td>cacheecszeroprefix</td><td>&lt;String></td><td>Read-write</td><td>Cache ECS responses with a Scope Prefix length of zero. Such a cached response will be used for all queries with this domain name and any subnet. When disabled, ECS responses with Scope Prefix length of zero will be cached, but not tied to any subnet. This option has no effect if caching of ECS responses is disabled in the corresponding DNS profile.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[UPDATE](#u)| [UNSET](#)| [GET (ALL)](#get-)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnsparameter
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"dnsparameter":{"retries":<Double_value>,"minttl":<Double_value>,"maxttl":<Double_value>,"cacherecords":<String_value>,"namelookuppriority":<String_value>,"recursion":<String_value>,"resolutionorder":<String_value>,"dnssec":<String_value>,"maxpipeline":<Double_value>,"dnsrootreferral":<String_value>,"dns64timeout":<Double_value>,"ecsmaxsubnets":<Double_value>,"maxnegcachettl":<Double_value>,"cachehitbypass":<String_value>,"maxcachesize":<Double_value>,"maxnegativecachesize":<Double_value>,"cachenoexpire":<String_value>,"splitpktqueryprocessing":<String_value>,"cacheecszeroprefix":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnsparameter?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"dnsparameter":{"retries":true,"minttl":true,"maxttl":true,"cacherecords":true,"namelookuppriority":true,"recursion":true,"resolutionorder":true,"dnssec":true,"maxpipeline":true,"dnsrootreferral":true,"dns64timeout":true,"ecsmaxsubnets":true,"maxnegcachettl":true,"cachehitbypass":true,"maxcachesize":true,"maxnegativecachesize":true,"cachenoexpire":true,"splitpktqueryprocessing":true,"cacheecszeroprefix":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnsparameter
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "dnsparameter": [ {"retries":<Double_value>,"minttl":<Double_value>,"maxttl":<Double_value>,"namelookuppriority":<String_value>,"cacherecords":<String_value>,"recursion":<String_value>,"resolutionorder":<String_value>,"dnssec":<String_value>,"maxpipeline":<Double_value>,"dnsrootreferral":<String_value>,"dns64timeout":<Double_value>,"ecsmaxsubnets":<Double_value>,"maxnegcachettl":<Double_value>,"cachehitbypass":<String_value>,"maxcachesize":<Double_value>,"maxnegativecachesize":<Double_value>,"cachenoexpire":<String_value>,"splitpktqueryprocessing":<String_value>,"cacheecszeroprefix":<String_value>}]}```



