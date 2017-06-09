#nspartition

Configuration for admin partition resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>partitionname</td><td>&lt;String></td><td>Read-write</td><td>Name of the Partition. Must begin with an ASCII alphanumeric or underscore (_) character, and must contain only ASCII alphanumeric, underscore, hash (#), period (.), space, colon (:), at (@), equals (=), and hyphen (-) characters.&lt;br>Minimum length = 1</td><tr><tr><td>maxbandwidth</td><td>&lt;Double></td><td>Read-write</td><td>Maximum bandwidth in Kbps, permitted on this partition.&lt;br>Default value: 10240</td><tr><tr><td>minbandwidth</td><td>&lt;Double></td><td>Read-write</td><td>Minimum bandwidth in Kbps, permitted on this partition.&lt;br>Default value: 10240</td><tr><tr><td>maxconn</td><td>&lt;Double></td><td>Read-write</td><td>Maximum number of connections permitted on this partition.&lt;br>Default value: 1024</td><tr><tr><td>maxmemlimit</td><td>&lt;Double></td><td>Read-write</td><td>Maximum memory allowed for this partition in megabytes.&lt;br>Default value: 10&lt;br>Minimum value = 5</td><tr><tr><td>partitionmac</td><td>&lt;String></td><td>Read-write</td><td>Special MAC address for the partition which is used for communication over shared vlans in this partition. If not specified, the MAC address is auto-generated.</td><tr><tr><td>partitionid</td><td>&lt;Double></td><td>Read-only</td><td>Partition Id.&lt;br>Minimum value = 1</td><tr><tr><td>partitiontype</td><td>&lt;String></td><td>Read-only</td><td>Type of the Partition.&lt;br>Possible values = Default Partition, Current Partition</td><tr><tr><td>pmacinternal</td><td>&lt;Boolean></td><td>Read-only</td><td>Partition MAC is generated internally.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [DELETE](#delete) | [UPDATE](#update) | [UNSET](#unset) | [SWITCH](#switch) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nspartition
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"nspartition":{      "partitionname":<String_value>,      "maxbandwidth":<Double_value>,      "minbandwidth":<Double_value>,      "maxconn":<Double_value>,      "maxmemlimit":<Double_value>,      "partitionmac":<String_value>}}```
Response:
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nspartition/partitionname_value&lt;String&gt;
HTTP Method: DELETE
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nspartition
HTTP Method: PUT
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"nspartition":{      "partitionname":<String_value>,      "maxbandwidth":<Double_value>,      "minbandwidth":<Double_value>,      "maxconn":<Double_value>,      "maxmemlimit":<Double_value>,      "partitionmac":<String_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nspartition?action=unset
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"nspartition":{      "partitionname":<String_value>,      "maxbandwidth":true,      "minbandwidth":true,      "maxconn":true,      "maxmemlimit":true,      "partitionmac":true}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###Switch



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nspartition?action=Switch
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"nspartition":{      "partitionname":<String_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nspartition
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nspartition?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


filter
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nspartition?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of nspartition resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nspartition?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).


pagination
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nspartition?pagesize=#no;pageno=#no
Use this query-parameter to get the nspartition resources in chunks.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "nspartition": [ {      "partitionname":<String_value>,      "partitionid":<Double_value>,      "partitiontype":<String_value>,      "maxbandwidth":<Double_value>,      "minbandwidth":<Double_value>,      "maxconn":<Double_value>,      "maxmemlimit":<Double_value>,      "partitionmac":<String_value>,      "pmacinternal":<Boolean_value>}]}```



###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nspartition/partitionname_value&lt;String&gt;
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nspartition/partitionname_value&lt;String&gt;?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nspartition/partitionname_value&lt;String&gt;?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "nspartition": [ {      "partitionname":<String_value>,      "partitionid":<Double_value>,      "partitiontype":<String_value>,      "maxbandwidth":<Double_value>,      "minbandwidth":<Double_value>,      "maxconn":<Double_value>,      "maxmemlimit":<Double_value>,      "partitionmac":<String_value>,      "pmacinternal":<Boolean_value>}]}```



###count



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nspartition?count=yes
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: 
{ "nspartition": [ { "__count": "#no"} ] }


