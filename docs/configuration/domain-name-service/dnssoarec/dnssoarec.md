#dnssoarec

Configuration for SOA record resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>domain</td><td>&lt;String></td><td>Read-write</td><td>Domain name for which to add the SOA record.&lt;br>Minimum length = 1</td><tr><tr><td>originserver</td><td>&lt;String></td><td>Read-write</td><td>Domain name of the name server that responds authoritatively for the domain.&lt;br>Minimum length = 1</td><tr><tr><td>contact</td><td>&lt;String></td><td>Read-write</td><td>Email address of the contact to whom domain issues can be addressed. In the email address, replace the @ sign with a period (.). For example, enter domainadmin.example.com instead of domainadmin@example.com.&lt;br>Minimum length = 1</td><tr><tr><td>serial</td><td>&lt;Double></td><td>Read-write</td><td>The secondary server uses this parameter to determine whether it requires a zone transfer from the primary server.&lt;br>Default value: 100&lt;br>Minimum value = 0&lt;br>Maximum value = 4294967294</td><tr><tr><td>refresh</td><td>&lt;Double></td><td>Read-write</td><td>Time, in seconds, for which a secondary server must wait between successive checks on the value of the serial number.&lt;br>Default value: 3600&lt;br>Minimum value = 0&lt;br>Maximum value = 4294967294</td><tr><tr><td>retry</td><td>&lt;Double></td><td>Read-write</td><td>Time, in seconds, between retries if a secondary servers attempt to contact the primary server for a zone refresh fails.&lt;br>Default value: 3&lt;br>Minimum value = 0&lt;br>Maximum value = 4294967294</td><tr><tr><td>expire</td><td>&lt;Double></td><td>Read-write</td><td>Time, in seconds, after which the zone data on a secondary name server can no longer be considered authoritative because all refresh and retry attempts made during the period have failed. After the expiry period, the secondary server stops serving the zone. Typically one week. Not used by the primary server.&lt;br>Default value: 3600&lt;br>Minimum value = 0&lt;br>Maximum value = 4294967294</td><tr><tr><td>minimum</td><td>&lt;Double></td><td>Read-write</td><td>Default time to live (TTL) for all records in the zone. Can be overridden for individual records.&lt;br>Default value: 5&lt;br>Minimum value = 0&lt;br>Maximum value = 2147483647</td><tr><tr><td>ttl</td><td>&lt;Double></td><td>Read-write</td><td>Time to Live (TTL), in seconds, for the record. TTL is the time for which the record must be cached by DNS proxies. The specified TTL is applied to all the resource records that are of the same record type and belong to the specified domain name. For example, if you add an address record, with a TTL of 36000, to the domain name example.com, the TTLs of all the address records of example.com are changed to 36000. If the TTL is not specified, the NetScaler appliance uses either the DNS zones minimum TTL or, if the SOA record is not available on the appliance, the default value of 3600.&lt;br>Default value: 3600&lt;br>Minimum value = 0&lt;br>Maximum value = 2147483647</td><tr><tr><td>type</td><td>&lt;String></td><td>Read-write</td><td>Type of records to display. Available settings function as follows:&lt;br>* ADNS - Display all authoritative address records.&lt;br>* PROXY - Display all proxy address records.&lt;br>* ALL - Display all address records.&lt;br>Possible values = ALL, ADNS, PROXY</td><tr><tr><td>nodeid</td><td>&lt;Double></td><td>Read-write</td><td>Unique number that identifies the cluster node.&lt;br>Minimum value = 0&lt;br>Maximum value = 31</td><tr><tr><td>authtype</td><td>&lt;String></td><td>Read-only</td><td>Record type.&lt;br>Possible values = ALL, ADNS, PROXY</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [DELETE](#delete) | [UPDATE](#update) | [UNSET](#unset) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnssoarec
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"dnssoarec":{      "domain":<String_value>,      "originserver":<String_value>,      "contact":<String_value>,      "serial":<Double_value>,      "refresh":<Double_value>,      "retry":<Double_value>,      "expire":<Double_value>,      "minimum":<Double_value>,      "ttl":<Double_value>}}```
Response:
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnssoarec/domain_value&lt;String&gt;
HTTP Method: DELETE
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnssoarec
HTTP Method: PUT
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"dnssoarec":{      "domain":<String_value>,      "originserver":<String_value>,      "contact":<String_value>,      "serial":<Double_value>,      "refresh":<Double_value>,      "retry":<Double_value>,      "expire":<Double_value>,      "minimum":<Double_value>,      "ttl":<Double_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnssoarec?action=unset
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"dnssoarec":{      "domain":<String_value>,      "serial":true,      "refresh":true,      "retry":true,      "expire":true,      "minimum":true,      "ttl":true}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnssoarec
Query-parameters:
args
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnssoarec?args=domain:&lt;String_value&gt;,type:&lt;String_value&gt;,nodeid:&lt;Double_value&gt;
Use this query-parameter to get dnssoarec resources based on additional properties.


attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnssoarec?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


filter
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnssoarec?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of dnssoarec resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnssoarec?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).


pagination
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnssoarec?pagesize=#no;pageno=#no
Use this query-parameter to get the dnssoarec resources in chunks.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "dnssoarec": [ {domain:<String_value>,type:<String_value>,nodeid:<Double_value>      "originserver":<String_value>,      "contact":<String_value>,      "serial":<Double_value>,      "refresh":<Double_value>,      "retry":<Double_value>,      "expire":<Double_value>,      "minimum":<Double_value>,      "ttl":<Double_value>,      "authtype":<String_value>}]}```



###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnssoarec/domain_value&lt;String&gt;
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnssoarec/domain_value&lt;String&gt;?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnssoarec/domain_value&lt;String&gt;?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "dnssoarec": [ {domain:<String_value>,type:<String_value>,nodeid:<Double_value>      "originserver":<String_value>,      "contact":<String_value>,      "serial":<Double_value>,      "refresh":<Double_value>,      "retry":<Double_value>,      "expire":<Double_value>,      "minimum":<Double_value>,      "ttl":<Double_value>,      "authtype":<String_value>}]}```



###count



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnssoarec?count=yes
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: 
{ "dnssoarec": [ { "__count": "#no"} ] }


