#pqbinding

Configuration for PQ bindings resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>vservername</td><td>&lt;String></td><td>Read-write</td><td>Name of the load balancing virtual server for which to display the priority queuing policy.&lt;br>Minimum length = 1</td><tr><tr><td>policyname</td><td>&lt;String></td><td>Read-only</td><td>The name of the priority queuing policy.</td><tr><tr><td>rule</td><td>&lt;String></td><td>Read-only</td><td>The condition for applying the policy.</td><tr><tr><td>priority</td><td>&lt;Double></td><td>Read-only</td><td>The priority of queuing the request.</td><tr><tr><td>weight</td><td>&lt;Double></td><td>Read-only</td><td>Weight.</td><tr><tr><td>qdepth</td><td>&lt;Double></td><td>Read-only</td><td>Queue Depth.</td><tr><tr><td>polqdepth</td><td>&lt;Double></td><td>Read-only</td><td>Policy Queue Depth.</td><tr><tr><td>hits</td><td>&lt;Double></td><td>Read-only</td><td>Total number of hits.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[GET (ALL)](#get-(all)) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/pqbinding
Query-parameters:
args
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/pqbinding?args=vservername:&lt;String_value&gt;,
Use this query-parameter to get pqbinding resources based on additional properties.


attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/pqbinding?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


filter
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/pqbinding?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of pqbinding resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/pqbinding?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).


pagination
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/pqbinding?pagesize=#no;pageno=#no
Use this query-parameter to get the pqbinding resources in chunks.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "pqbinding": [ {vservername:<String_value>,      "policyname":<String_value>,      "rule":<String_value>,      "priority":<Double_value>,      "weight":<Double_value>,      "qdepth":<Double_value>,      "polqdepth":<Double_value>,      "hits":<Double_value>}]}```



###count



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/pqbinding?args=vservername:&lt;String_value&gt;,;count=yes
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: 
{ "pqbinding": [ { "__count": "#no"} ] }


