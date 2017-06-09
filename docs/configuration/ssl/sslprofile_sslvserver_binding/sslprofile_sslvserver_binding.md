#sslprofile_sslvserver_binding

Binding object showing the sslvserver that can be bound to sslprofile.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>cipherpriority</td><td>&lt;Double></td><td>Read-write</td><td>Priority of the cipher binding.&lt;br>Minimum value = 1&lt;br>Maximum value = 1000</td><tr><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name of the SSL profile.&lt;br>Minimum length = 1&lt;br>Maximum length = 127</td><tr><tr><td>description</td><td>&lt;String></td><td>Read-write</td><td>The cipher suite description.</td><tr><tr><td>servicename</td><td>&lt;String></td><td>Read-write</td><td>Service name.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-write</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslprofile_sslvserver_binding/name_value&lt;String&gt;
Query-parameters:
filter
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslprofile_sslvserver_binding/name_value&lt;String&gt;?filter=property-name1:property-value1,property-name2:property-value2
Use this query-parameter to get the filtered set of sslprofile_sslvserver_binding resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


pagesize=#no;pageno=#no
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslprofile_sslvserver_binding/name_value&lt;String&gt;?pagesize=#no;pageno=#no
Use this query-parameter to get the sslprofile_sslvserver_binding resources in chunks.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx   (for general HTTP errors) or 5xx     (for NetScaler-specific errors). The response payload provides details of the error Response Headers:

Content-Type:application/json

Response Payload: ```{ "sslprofile_sslvserver_binding": [ {      "cipherpriority":<Double_value>,      "name":<String_value>,      "description":<String_value>,      "servicename":<String_value>}]}```



###count



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslprofile_sslvserver_binding/name_value&lt;String&gt;?count=yes
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx   (for general HTTP errors) or 5xx     (for NetScaler-specific errors). The response payload provides details of the error Response Headers:

Content-Type:application/json

Response Payload: 
{"sslprofile_sslvserver_binding": [ { "__count": "#no"} ] }


