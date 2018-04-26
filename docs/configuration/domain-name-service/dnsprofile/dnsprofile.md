#dnsprofile

Configuration for DNS profile resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>dnsprofilename</td><td>&lt;String></td><td>Read-write</td><td>Name of the DNS profile.<br>Minimum length = 1<br>Maximum length = 127</td></tr><tr><td>dnsquerylogging</td><td>&lt;String></td><td>Read-write</td><td>DNS query logging; if enabled, DNS query information such as DNS query id, DNS query flags , DNS domain name and DNS query type will be logged.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>dnsanswerseclogging</td><td>&lt;String></td><td>Read-write</td><td>DNS answer section; if enabled, answer section in the response will be logged.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>dnsextendedlogging</td><td>&lt;String></td><td>Read-write</td><td>DNS extended logging; if enabled, authority and additional section in the response will be logged.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>dnserrorlogging</td><td>&lt;String></td><td>Read-write</td><td>DNS error logging; if enabled, whenever error is encountered in DNS module reason for the error will be logged.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>cacherecords</td><td>&lt;String></td><td>Read-write</td><td>Cache resource records in the DNS cache. Applies to resource records obtained through proxy configurations only. End resolver and forwarder configurations always cache records in the DNS cache, and you cannot disable this behavior. When you disable record caching, the appliance stops caching server responses. However, cached records are not flushed. The appliance does not serve requests from the cache until record caching is enabled again.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>cachenegativeresponses</td><td>&lt;String></td><td>Read-write</td><td>Cache negative responses in the DNS cache. When disabled, the appliance stops caching negative responses except referral records. This applies to all configurations - proxy, end resolver, and forwarder. However, cached responses are not flushed. The appliance does not serve negative responses from the cache until this parameter is enabled again.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>dropmultiqueryrequest</td><td>&lt;String></td><td>Read-write</td><td>Drop the DNS requests containing multiple queries. When enabled, DNS requests containing multiple queries will be dropped. In case of proxy configuration by default the DNS request containing multiple queries is forwarded to the backend and in case of ADNS and Resolver configuration NOCODE error response will be sent to the client.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>cacheecsresponses</td><td>&lt;String></td><td>Read-write</td><td>Cache DNS responses with EDNS Client Subnet(ECS) option in the DNS cache. When disabled, the appliance stops caching responses with ECS option. This is relevant to proxy configuration. Enabling/disabling support of ECS option when NetScaler is authoritative for a GSLB domain is supported using a knob in GSLB vserver. In all other modes, ECS option is ignored.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>referencecount</td><td>&lt;Double></td><td>Read-only</td><td>Number of entities using this profile.</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD]()| [UPDATE](#u)| [UNSET](#)| [DELETE](#d)| [GET (ALL)](#get-)| [GET]()| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnsprofile
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"dnsprofile":{<b>"dnsprofilename":<String_value>,</b>"dnsquerylogging":<String_value>,"dnsanswerseclogging":<String_value>,"dnsextendedlogging":<String_value>,"dnserrorlogging":<String_value>,"cacherecords":<String_value>,"cachenegativeresponses":<String_value>,"dropmultiqueryrequest":<String_value>,"cacheecsresponses":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnsprofile
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"dnsprofile":{<b>"dnsprofilename":<String_value>,</b>"dnsquerylogging":<String_value>,"dnsanswerseclogging":<String_value>,"dnsextendedlogging":<String_value>,"dnserrorlogging":<String_value>,"cacherecords":<String_value>,"cachenegativeresponses":<String_value>,"dropmultiqueryrequest":<String_value>,"cacheecsresponses":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnsprofile?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"dnsprofile":{<b>"dnsprofilename":<String_value>,</b>"dnsquerylogging":true,"dnsanswerseclogging":true,"dnsextendedlogging":true,"dnserrorlogging":true,"cacherecords":true,"cachenegativeresponses":true,"dropmultiqueryrequest":true,"cacheecsresponses":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnsprofile/dnsprofilename_value&lt;String&gt;
<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnsprofile
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnsprofile?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnsprofile?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of dnsprofile resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnsprofile?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnsprofile?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the dnsprofile resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "dnsprofile": [ {"dnsprofilename":<String_value>,"dnsquerylogging":<String_value>,"dnsanswerseclogging":<String_value>,"dnsextendedlogging":<String_value>,"dnserrorlogging":<String_value>,"cacherecords":<String_value>,"cachenegativeresponses":<String_value>,"dropmultiqueryrequest":<String_value>,"cacheecsresponses":<String_value>,"referencecount":<Double_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnsprofile/dnsprofilename_value&lt;String&gt;
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnsprofile/dnsprofilename_value&lt;String&gt;?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnsprofile/dnsprofilename_value&lt;String&gt;?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "dnsprofile": [ {"dnsprofilename":<String_value>,"dnsquerylogging":<String_value>,"dnsanswerseclogging":<String_value>,"dnsextendedlogging":<String_value>,"dnserrorlogging":<String_value>,"cacherecords":<String_value>,"cachenegativeresponses":<String_value>,"dropmultiqueryrequest":<String_value>,"cacheecsresponses":<String_value>,"referencecount":<Double_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnsprofile?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "dnsprofile": [ { "__count": "#no"} ] }```



