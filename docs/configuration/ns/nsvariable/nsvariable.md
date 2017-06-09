#nsvariable

Configuration for variable resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Variable name. This follows the same syntax rules as other default syntax expression entity names:&lt;br> It must begin with an alpha character (A-Z or a-z) or an underscore (_).&lt;br> The rest of the characters must be alpha, numeric (0-9) or underscores.&lt;br> It cannot be re or xp (reserved for regular and XPath expressions).&lt;br> It cannot be a default syntax expression reserved word (e.g. SYS or HTTP).&lt;br> It cannot be used for an existing default syntax expression object (HTTP callout, patset, dataset, stringmap, or named expression).&lt;br>Minimum length = 1</td><tr><tr><td>type</td><td>&lt;String></td><td>Read-write</td><td>Specification of the variable type; one of the following:&lt;br> ulong - singleton variable with an unsigned 64-bit value.&lt;br> text(value-max-size) - singleton variable with a text string value.&lt;br> map(text(key-max-size),ulong,max-entries) - map of text string keys to unsigned 64-bit values.&lt;br> map(text(key-max-size),text(value-max-size),max-entries) - map of text string keys to text string values.&lt;br>where&lt;br> value-max-size is a positive integer that is the maximum number of bytes in a text string value.&lt;br> key-max-size is a positive integer that is the maximum number of bytes in a text string key.&lt;br> max-entries is a positive integer that is the maximum number of entries in a map variable.&lt;br> For a global singleton text variable, value-max-size ;lt;= 64000.&lt;br> For a global map with ulong values, key-max-size ;lt;= 64000.&lt;br> For a global map with text values, key-max-size + value-max-size ;lt;= 64000.&lt;br> max-entries is a positive integer that is the maximum number of entries in a map variable. This has a theoretical maximum of 2^64-1, but in actual use will be much smaller, considering the memory available for use by the map.&lt;br>Example:&lt;br> map(text(10),text(20),100) specifies a map of text string keys (max size 10 bytes) to text string values (max size 20 bytes), with 100 max entries.&lt;br>Minimum length = 1</td><tr><tr><td>scope</td><td>&lt;String></td><td>Read-write</td><td>Scope of the variable:&lt;br> global - (default) one set of values visible across all Packet Engines and, in a cluster, all nodes&lt;br> transaction - one value for each request-response transaction (singleton variables only; no expiration).&lt;br>Default value: global&lt;br>Possible values = global, transaction</td><tr><tr><td>iffull</td><td>&lt;String></td><td>Read-write</td><td>Action to perform if an assignment to a map exceeds its configured max-entries:&lt;br> lru - (default) reuse the least recently used entry in the map.&lt;br> undef - force the assignment to return an undefined (Undef) result to the policy executing the assignment.&lt;br>Default value: lru&lt;br>Possible values = undef, lru</td><tr><tr><td>ifvaluetoobig</td><td>&lt;String></td><td>Read-write</td><td>Action to perform if an value is assigned to a text variable that exceeds its configured max-size,&lt;br>or if a key is used that exceeds its configured max-size:&lt;br> truncate - (default) truncate the text string to the first max-size bytes and proceed.&lt;br> undef - force the assignment or expression evaluation to return an undefined (Undef) result to the policy executing the assignment or expression.&lt;br>Default value: truncate&lt;br>Possible values = undef, truncate</td><tr><tr><td>ifnovalue</td><td>&lt;String></td><td>Read-write</td><td>Action to perform if on a variable reference in an expression if the variable is single-valued and uninitialized&lt;br>or if the variable is a map and there is no value for the specified key:&lt;br> init - (default) initialize the single-value variable, or create a map entry for the key and the initial value,&lt;br>using the -init value or its default.&lt;br> undef - force the expression evaluation to return an undefined (Undef) result to the policy executing the expression.&lt;br>Default value: init&lt;br>Possible values = undef, init</td><tr><tr><td>init</td><td>&lt;String></td><td>Read-write</td><td>Initialization value for values in this variable. Default: 0 for ulong, NULL for text.</td><tr><tr><td>expires</td><td>&lt;Double></td><td>Read-write</td><td>Value expiration in seconds. If the value is not referenced within the expiration period it will be deleted. 0 (the default) means no expiration.&lt;br>Minimum value = 0&lt;br>Maximum value = 31622400</td><tr><tr><td>comment</td><td>&lt;String></td><td>Read-write</td><td>Comments associated with this variable.</td><tr><tr><td>referencecount</td><td>&lt;Double></td><td>Read-only</td><td>The number of references to the variable in expressions and assignments.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [UPDATE](#update) | [UNSET](#unset) | [DELETE](#delete) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsvariable
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"nsvariable":{      "name":<String_value>,      "type":<String_value>,      "scope":<String_value>,      "iffull":<String_value>,      "ifvaluetoobig":<String_value>,      "ifnovalue":<String_value>,      "init":<String_value>,      "expires":<Double_value>,      "comment":<String_value>}}```
Response:
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsvariable
HTTP Method: PUT
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"nsvariable":{      "name":<String_value>,      "type":<String_value>,      "iffull":<String_value>,      "ifvaluetoobig":<String_value>,      "ifnovalue":<String_value>,      "init":<String_value>,      "expires":<Double_value>,      "comment":<String_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsvariable?action=unset
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"nsvariable":{      "name":<String_value>,      "iffull":true,      "ifvaluetoobig":true,      "ifnovalue":true,      "init":true,      "expires":true,      "comment":true}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsvariable/name_value&lt;String&gt;
HTTP Method: DELETE
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsvariable
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsvariable?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


filter
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsvariable?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of nsvariable resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsvariable?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).


pagination
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsvariable?pagesize=#no;pageno=#no
Use this query-parameter to get the nsvariable resources in chunks.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "nsvariable": [ {      "name":<String_value>,      "type":<String_value>,      "scope":<String_value>,      "iffull":<String_value>,      "ifvaluetoobig":<String_value>,      "ifnovalue":<String_value>,      "expires":<Double_value>,      "init":<String_value>,      "comment":<String_value>,      "referencecount":<Double_value>}]}```



###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsvariable/name_value&lt;String&gt;
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsvariable/name_value&lt;String&gt;?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsvariable/name_value&lt;String&gt;?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "nsvariable": [ {      "name":<String_value>,      "type":<String_value>,      "scope":<String_value>,      "iffull":<String_value>,      "ifvaluetoobig":<String_value>,      "ifnovalue":<String_value>,      "expires":<Double_value>,      "init":<String_value>,      "comment":<String_value>,      "referencecount":<Double_value>}]}```



###count



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsvariable?count=yes
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: 
{ "nsvariable": [ { "__count": "#no"} ] }


