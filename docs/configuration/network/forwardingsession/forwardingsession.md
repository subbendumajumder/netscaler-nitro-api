#forwardingsession

Configuration for session forward resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the forwarding session rule. Can begin with a letter, number, or the underscore character (_), and can consist of letters, numbers, and the hyphen (-), period (.) pound (#), space ( ), at (@), equals (=), colon (:), and underscore characters. Cannot be changed after the rule is created.&lt;br>The following requirement applies only to the NetScaler CLI:&lt;br>If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my rule" or my rule).&lt;br>Minimum length = 1</td><tr><tr><td>network</td><td>&lt;String></td><td>Read-write</td><td>An IPv4 network address or IPv6 prefix of a network from which the forwarded traffic originates or to which it is destined.&lt;br>Minimum length = 1</td><tr><tr><td>netmask</td><td>&lt;String></td><td>Read-write</td><td>Subnet mask associated with the network.&lt;br>Minimum length = 1</td><tr><tr><td>acl6name</td><td>&lt;String></td><td>Read-write</td><td>Name of any configured ACL6 whose action is ALLOW. The rule of the ACL6 is used as a forwarding session rule.&lt;br>Minimum length = 1</td><tr><tr><td>aclname</td><td>&lt;String></td><td>Read-write</td><td>Name of any configured ACL whose action is ALLOW. The rule of the ACL is used as a forwarding session rule.&lt;br>Minimum length = 1</td><tr><tr><td>td</td><td>&lt;Double></td><td>Read-write</td><td>Integer value that uniquely identifies the traffic domain in which you want to configure the entity. If you do not specify an ID, the entity becomes part of the default traffic domain, which has an ID of 0.&lt;br>Minimum value = 0&lt;br>Maximum value = 4094</td><tr><tr><td>connfailover</td><td>&lt;String></td><td>Read-write</td><td>Synchronize connection information with the secondary appliance in a high availability (HA) pair. That is, synchronize all connection-related information for the forwarding session.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>sourceroutecache</td><td>&lt;String></td><td>Read-write</td><td>Cache the source ip address and mac address of the DA servers.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [UPDATE](#update) | [DELETE](#delete) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/forwardingsession
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"forwardingsession":{      "name":<String_value>,      "network":<String_value>,      "netmask":<String_value>,      "acl6name":<String_value>,      "aclname":<String_value>,      "td":<Double_value>,      "connfailover":<String_value>,      "sourceroutecache":<String_value>}}```
Response:
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/forwardingsession
HTTP Method: PUT
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"forwardingsession":{      "name":<String_value>,      "connfailover":<String_value>,      "sourceroutecache":<String_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/forwardingsession/name_value&lt;String&gt;
HTTP Method: DELETE
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/forwardingsession
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/forwardingsession?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


filter
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/forwardingsession?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of forwardingsession resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/forwardingsession?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).


pagination
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/forwardingsession?pagesize=#no;pageno=#no
Use this query-parameter to get the forwardingsession resources in chunks.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "forwardingsession": [ {      "name":<String_value>,      "network":<String_value>,      "netmask":<String_value>,      "td":<Double_value>,      "aclname":<String_value>,      "acl6name":<String_value>,      "connfailover":<String_value>,      "sourceroutecache":<String_value>}]}```



###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/forwardingsession/name_value&lt;String&gt;
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/forwardingsession/name_value&lt;String&gt;?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/forwardingsession/name_value&lt;String&gt;?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "forwardingsession": [ {      "name":<String_value>,      "network":<String_value>,      "netmask":<String_value>,      "td":<Double_value>,      "aclname":<String_value>,      "acl6name":<String_value>,      "connfailover":<String_value>,      "sourceroutecache":<String_value>}]}```



###count



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/forwardingsession?count=yes
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: 
{ "forwardingsession": [ { "__count": "#no"} ] }


