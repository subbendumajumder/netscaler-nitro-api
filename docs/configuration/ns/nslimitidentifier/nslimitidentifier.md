#nslimitidentifier

Configuration for limit Indetifier resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>limitidentifier</td><td>&lt;String></td><td>Read-write</td><td>Name for a rate limit identifier. Must begin with an ASCII letter or underscore (_) character, and must consist only of ASCII alphanumeric or underscore characters. Reserved words must not be used.</td><tr><tr><td>threshold</td><td>&lt;Double></td><td>Read-write</td><td>Maximum number of requests that are allowed in the given timeslice when requests (mode is set as REQUEST_RATE) are tracked per timeslice.&lt;br>When connections (mode is set as CONNECTION) are tracked, it is the total number of connections that would be let through.&lt;br>Default value: 1&lt;br>Minimum value = 1</td><tr><tr><td>timeslice</td><td>&lt;Double></td><td>Read-write</td><td>Time interval, in milliseconds, specified in multiples of 10, during which requests are tracked to check if they cross the threshold. This argument is needed only when the mode is set to REQUEST_RATE.&lt;br>Default value: 1000&lt;br>Minimum value = 10</td><tr><tr><td>mode</td><td>&lt;String></td><td>Read-write</td><td>Defines the type of traffic to be tracked.&lt;br>* REQUEST_RATE - Tracks requests/timeslice.&lt;br>* CONNECTION - Tracks active transactions.&lt;br>&lt;br>Examples&lt;br>&lt;br>1. To permit 20 requests in 10 ms and 2 traps in 10 ms:&lt;br>add limitidentifier limit_req -mode request_rate -limitType smooth -timeslice 1000 -Threshold 2000 -trapsInTimeSlice 200&lt;br>&lt;br>2. To permit 50 requests in 10 ms:&lt;br>set limitidentifier limit_req -mode request_rate -timeslice 1000 -Threshold 5000 -limitType smooth&lt;br>&lt;br>3. To permit 1 request in 40 ms:&lt;br>set limitidentifier limit_req -mode request_rate -timeslice 2000 -Threshold 50 -limitType smooth&lt;br>&lt;br>4. To permit 1 request in 200 ms and 1 trap in 130 ms:&lt;br>set limitidentifier limit_req -mode request_rate -timeslice 1000 -Threshold 5 -limitType smooth -trapsInTimeSlice 8&lt;br>&lt;br>5. To permit 5000 requests in 1000 ms and 200 traps in 1000 ms:&lt;br>set limitidentifier limit_req -mode request_rate -timeslice 1000 -Threshold 5000 -limitType BURSTY.&lt;br>Default value: REQUEST_RATE&lt;br>Possible values = CONNECTION, REQUEST_RATE, NONE</td><tr><tr><td>limittype</td><td>&lt;String></td><td>Read-write</td><td>Smooth or bursty request type.&lt;br>* SMOOTH - When you want the permitted number of requests in a given interval of time to be spread evenly across the timeslice&lt;br>* BURSTY - When you want the permitted number of requests to exhaust the quota anytime within the timeslice.&lt;br>This argument is needed only when the mode is set to REQUEST_RATE.&lt;br>Default value: BURSTY&lt;br>Possible values = BURSTY, SMOOTH</td><tr><tr><td>selectorname</td><td>&lt;String></td><td>Read-write</td><td>Name of the rate limit selector. If this argument is NULL, rate limiting will be applied on all traffic received by the virtual server or the NetScaler (depending on whether the limit identifier is bound to a virtual server or globally) without any filtering.&lt;br>Minimum length = 1</td><tr><tr><td>maxbandwidth</td><td>&lt;Double></td><td>Read-write</td><td>Maximum bandwidth permitted, in kbps.&lt;br>Minimum value = 0&lt;br>Maximum value = 4294967287</td><tr><tr><td>trapsintimeslice</td><td>&lt;Double></td><td>Read-write</td><td>Number of traps to be sent in the timeslice configured. A value of 0 indicates that traps are disabled.&lt;br>Minimum value = 0&lt;br>Maximum value = 65535</td><tr><tr><td>ngname</td><td>&lt;String></td><td>Read-only</td><td>Nodegroup name to which this identifier belongs to.</td><tr><tr><td>hits</td><td>&lt;Double></td><td>Read-only</td><td>The number of times this identifier was evaluated.</td><tr><tr><td>drop</td><td>&lt;Double></td><td>Read-only</td><td>The number of times action was taken.</td><tr><tr><td>rule</td><td>&lt;String[]></td><td>Read-only</td><td>Rule.</td><tr><tr><td>time</td><td>&lt;Double></td><td>Read-only</td><td>Time interval considered for rate limiting.</td><tr><tr><td>total</td><td>&lt;Double></td><td>Read-only</td><td>Maximum number of requests permitted in the computed timeslice.</td><tr><tr><td>trapscomputedintimeslice</td><td>&lt;Double></td><td>Read-only</td><td>The number of traps that would be sent in the timeslice configured. .</td><tr><tr><td>computedtraptimeslice</td><td>&lt;Double></td><td>Read-only</td><td>The time interval computed for sending traps.</td><tr><tr><td>referencecount</td><td>&lt;Double></td><td>Read-only</td><td>Total number of transactions pointing to this entry.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [DELETE](#delete) | [UPDATE](#update) | [UNSET](#unset) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nslimitidentifier
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"nslimitidentifier":{      "limitidentifier":<String_value>,      "threshold":<Double_value>,      "timeslice":<Double_value>,      "mode":<String_value>,      "limittype":<String_value>,      "selectorname":<String_value>,      "maxbandwidth":<Double_value>,      "trapsintimeslice":<Double_value>}}```
Response:
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nslimitidentifier/limitidentifier_value&lt;String&gt;
HTTP Method: DELETE
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nslimitidentifier
HTTP Method: PUT
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"nslimitidentifier":{      "limitidentifier":<String_value>,      "threshold":<Double_value>,      "timeslice":<Double_value>,      "mode":<String_value>,      "limittype":<String_value>,      "selectorname":<String_value>,      "maxbandwidth":<Double_value>,      "trapsintimeslice":<Double_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nslimitidentifier?action=unset
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"nslimitidentifier":{      "limitidentifier":<String_value>,      "selectorname":true,      "threshold":true,      "timeslice":true,      "mode":true,      "limittype":true,      "maxbandwidth":true,      "trapsintimeslice":true}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nslimitidentifier
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nslimitidentifier?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


filter
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nslimitidentifier?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of nslimitidentifier resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nslimitidentifier?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).


pagination
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nslimitidentifier?pagesize=#no;pageno=#no
Use this query-parameter to get the nslimitidentifier resources in chunks.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "nslimitidentifier": [ {      "limitidentifier":<String_value>,      "ngname":<String_value>,      "threshold":<Double_value>,      "timeslice":<Double_value>,      "mode":<String_value>,      "limittype":<String_value>,      "selectorname":<String_value>,      "hits":<Double_value>,      "drop":<Double_value>,      "rule":<String[]_value>,      "time":<Double_value>,      "total":<Double_value>,      "maxbandwidth":<Double_value>,      "trapsintimeslice":<Double_value>,      "trapscomputedintimeslice":<Double_value>,      "computedtraptimeslice":<Double_value>,      "referencecount":<Double_value>}]}```



###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nslimitidentifier/limitidentifier_value&lt;String&gt;
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nslimitidentifier/limitidentifier_value&lt;String&gt;?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nslimitidentifier/limitidentifier_value&lt;String&gt;?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "nslimitidentifier": [ {      "limitidentifier":<String_value>,      "ngname":<String_value>,      "threshold":<Double_value>,      "timeslice":<Double_value>,      "mode":<String_value>,      "limittype":<String_value>,      "selectorname":<String_value>,      "hits":<Double_value>,      "drop":<Double_value>,      "rule":<String[]_value>,      "time":<Double_value>,      "total":<Double_value>,      "maxbandwidth":<Double_value>,      "trapsintimeslice":<Double_value>,      "trapscomputedintimeslice":<Double_value>,      "computedtraptimeslice":<Double_value>,      "referencecount":<Double_value>}]}```



###count



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nslimitidentifier?count=yes
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: 
{ "nslimitidentifier": [ { "__count": "#no"} ] }


