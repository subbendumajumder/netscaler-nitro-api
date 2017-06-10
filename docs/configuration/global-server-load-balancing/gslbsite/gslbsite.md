#gslbsite

Configuration for GSLB site resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>sitename</td><td>&lt;String></td><td>Read-write</td><td>Name for the GSLB site. Must begin with an ASCII alphanumeric or underscore (_) character, and must contain only ASCII alphanumeric, underscore, hash (#), period (.), space, colon (:), at (@), equals (=), and hyphen (-) characters. Cannot be changed after the virtual server is created.&lt;br>&lt;br>CLI Users: If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my gslbsite" or my gslbsite).&lt;br>Minimum length = 1</td><tr><tr><td>sitetype</td><td>&lt;String></td><td>Read-write</td><td>Type of site to create. If the type is not specified, the appliance automatically detects and sets the type on the basis of the IP address being assigned to the site. If the specified site IP address is owned by the appliance (for example, a MIP address or SNIP address), the site is a local site. Otherwise, it is a remote site.&lt;br>Default value: NONE&lt;br>Possible values = REMOTE, LOCAL</td><tr><tr><td>siteipaddress</td><td>&lt;String></td><td>Read-write</td><td>IP address for the GSLB site. The GSLB site uses this IP address to communicate with other GSLB sites. For a local site, use any IP address that is owned by the appliance (for example, a SNIP or MIP address, or the IP address of the ADNS service).&lt;br>Minimum length = 1</td><tr><tr><td>publicip</td><td>&lt;String></td><td>Read-write</td><td>Public IP address for the local site. Required only if the appliance is deployed in a private address space and the site has a public IP address hosted on an external firewall or a NAT device.&lt;br>Minimum length = 1</td><tr><tr><td>metricexchange</td><td>&lt;String></td><td>Read-write</td><td>Exchange metrics with other sites. Metrics are exchanged by using Metric Exchange Protocol (MEP). The appliances in the GSLB setup exchange health information once every second. &lt;br>&lt;br>If you disable metrics exchange, you can use only static load balancing methods (such as round robin, static proximity, or the hash-based methods), and if you disable metrics exchange when a dynamic load balancing method (such as least connection) is in operation, the appliance falls back to round robin. Also, if you disable metrics exchange, you must use a monitor to determine the state of GSLB services. Otherwise, the service is marked as DOWN.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>nwmetricexchange</td><td>&lt;String></td><td>Read-write</td><td>Exchange, with other GSLB sites, network metrics such as round-trip time (RTT), learned from communications with various local DNS (LDNS) servers used by clients. RTT information is used in the dynamic RTT load balancing method, and is exchanged every 5 seconds.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>sessionexchange</td><td>&lt;String></td><td>Read-write</td><td>Exchange persistent session entries with other GSLB sites every five seconds.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>triggermonitor</td><td>&lt;String></td><td>Read-write</td><td>Specify the conditions under which the GSLB service must be monitored by a monitor, if one is bound. Available settings function as follows:&lt;br>* ALWAYS - Monitor the GSLB service at all times.&lt;br>* MEPDOWN - Monitor the GSLB service only when the exchange of metrics through the Metrics Exchange Protocol (MEP) is disabled.&lt;br>MEPDOWN_SVCDOWN - Monitor the service in either of the following situations: &lt;br>* The exchange of metrics through MEP is disabled.&lt;br>* The exchange of metrics through MEP is enabled but the status of the service, learned through metrics exchange, is DOWN.&lt;br>Default value: ALWAYS&lt;br>Possible values = ALWAYS, MEPDOWN, MEPDOWN_SVCDOWN</td><tr><tr><td>parentsite</td><td>&lt;String></td><td>Read-write</td><td>Parent site of the GSLB site, in a parent-child topology.</td><tr><tr><td>clip</td><td>&lt;String></td><td>Read-write</td><td>Cluster IP address. Specify this parameter to connect to the remote cluster site for GSLB auto-sync. Note: The cluster IP address is defined when creating the cluster.</td><tr><tr><td>publicclip</td><td>&lt;String></td><td>Read-write</td><td>IP address to be used to globally access the remote cluster when it is deployed behind a NAT. It can be same as the normal cluster IP address.</td><tr><tr><td>naptrreplacementsuffix</td><td>&lt;String></td><td>Read-write</td><td>The naptr replacement suffix configured here will be used to construct the naptr replacement field in NAPTR record.&lt;br>Minimum length = 1</td><tr><tr><td>backupparentlist</td><td>&lt;String[]></td><td>Read-write</td><td>The list of backup gslb sites configured in preferred order. Need to be parent gsb sites.&lt;br>Default value: "None"</td><tr><tr><td>status</td><td>&lt;String></td><td>Read-only</td><td>Current metric exchange status.&lt;br>Possible values = ACTIVE, INACTIVE, DOWN</td><tr><tr><td>persistencemepstatus</td><td>&lt;String></td><td>Read-only</td><td>Network metric and persistence exchange MEP connection status.&lt;br>Possible values = ACTIVE, INACTIVE, DOWN</td><tr><tr><td>version</td><td>&lt;Double></td><td>Read-only</td><td>will be true if the remote sites version is ncore compatible with the local site.(;gt;= 9.2).</td><tr><tr><td>curbackupparentip</td><td>&lt;String></td><td>Read-only</td><td>Current active backup parent IP address since the configured is DOWN.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [DELETE](#delete) | [UPDATE](#update) | [UNSET](#unset) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbsite
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"gslbsite":{      "sitename":<String_value>,      "sitetype":<String_value>,      "siteipaddress":<String_value>,      "publicip":<String_value>,      "metricexchange":<String_value>,      "nwmetricexchange":<String_value>,      "sessionexchange":<String_value>,      "triggermonitor":<String_value>,      "parentsite":<String_value>,      "clip":<String_value>,      "publicclip":<String_value>,      "naptrreplacementsuffix":<String_value>,      "backupparentlist":<String[]_value>}}```
Response:
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbsite/sitename_value&lt;String&gt;
HTTP Method: DELETE
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbsite
HTTP Method: PUT
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"gslbsite":{      "sitename":<String_value>,      "metricexchange":<String_value>,      "nwmetricexchange":<String_value>,      "sessionexchange":<String_value>,      "triggermonitor":<String_value>,      "naptrreplacementsuffix":<String_value>,      "backupparentlist":<String[]_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbsite?action=unset
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"gslbsite":{      "sitename":<String_value>,      "metricexchange":true,      "nwmetricexchange":true,      "sessionexchange":true,      "triggermonitor":true,      "naptrreplacementsuffix":true,      "backupparentlist":true}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbsite
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbsite?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


filter
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbsite?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of gslbsite resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbsite?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).


pagination
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbsite?pagesize=#no;pageno=#no
Use this query-parameter to get the gslbsite resources in chunks.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "gslbsite": [ {      "sitename":<String_value>,      "sitetype":<String_value>,      "siteipaddress":<String_value>,      "publicip":<String_value>,      "metricexchange":<String_value>,      "status":<String_value>,      "persistencemepstatus":<String_value>,      "nwmetricexchange":<String_value>,      "sessionexchange":<String_value>,      "triggermonitor":<String_value>,      "parentsite":<String_value>,      "version":<Double_value>,      "clip":<String_value>,      "publicclip":<String_value>,      "naptrreplacementsuffix":<String_value>,      "backupparentlist":<String[]_value>,      "curbackupparentip":<String_value>}]}```



###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbsite/sitename_value&lt;String&gt;
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbsite/sitename_value&lt;String&gt;?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbsite/sitename_value&lt;String&gt;?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "gslbsite": [ {      "sitename":<String_value>,      "sitetype":<String_value>,      "siteipaddress":<String_value>,      "publicip":<String_value>,      "metricexchange":<String_value>,      "status":<String_value>,      "persistencemepstatus":<String_value>,      "nwmetricexchange":<String_value>,      "sessionexchange":<String_value>,      "triggermonitor":<String_value>,      "parentsite":<String_value>,      "version":<Double_value>,      "clip":<String_value>,      "publicclip":<String_value>,      "naptrreplacementsuffix":<String_value>,      "backupparentlist":<String[]_value>,      "curbackupparentip":<String_value>}]}```



###count



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbsite?count=yes
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: 
{ "gslbsite": [ { "__count": "#no"} ] }


