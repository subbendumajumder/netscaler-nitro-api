#nsvariable

Configuration for variable resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Variable name. This follows the same syntax rules as other default syntax expression entity names:<br>It must begin with an alpha character (A-Z or a-z) or an underscore (_).<br>The rest of the characters must be alpha, numeric (0-9) or underscores.<br>It cannot be re or xp (reserved for regular and XPath expressions).<br>It cannot be a default syntax expression reserved word (e.g. SYS or HTTP).<br>It cannot be used for an existing default syntax expression object (HTTP callout, patset, dataset, stringmap, or named expression).<br>Minimum length = 1</td></tr><tr><td>type</td><td>&lt;String></td><td>Read-write</td><td>Specification of the variable type; one of the following:<br>ulong - singleton variable with an unsigned 64-bit value.<br>text(value-max-size) - singleton variable with a text string value.<br>map(text(key-max-size),ulong,max-entries) - map of text string keys to unsigned 64-bit values.<br>map(text(key-max-size),text(value-max-size),max-entries) - map of text string keys to text string values.<br>where<br>value-max-size is a positive integer that is the maximum number of bytes in a text string value.<br>key-max-size is a positive integer that is the maximum number of bytes in a text string key.<br>max-entries is a positive integer that is the maximum number of entries in a map variable.<br>For a global singleton text variable, value-max-size &lt;= 64000.<br>For a global map with ulong values, key-max-size &lt;= 64000.<br>For a global map with text values, key-max-size + value-max-size &lt;= 64000.<br>max-entries is a positive integer that is the maximum number of entries in a map variable. This has a theoretical maximum of 2^64-1, but in actual use will be much smaller, considering the memory available for use by the map.<br>Example:<br>map(text(10),text(20),100) specifies a map of text string keys (max size 10 bytes) to text string values (max size 20 bytes), with 100 max entries.<br>Minimum length = 1</td></tr><tr><td>scope</td><td>&lt;String></td><td>Read-write</td><td>Scope of the variable:<br>global - (default) one set of values visible across all Packet Engines and, in a cluster, all nodes<br>transaction - one value for each request-response transaction (singleton variables only; no expiration).<br>Default value: global<br>Possible values = global, transaction</td></tr><tr><td>iffull</td><td>&lt;String></td><td>Read-write</td><td>Action to perform if an assignment to a map exceeds its configured max-entries:<br>lru - (default) reuse the least recently used entry in the map.<br>undef - force the assignment to return an undefined (Undef) result to the policy executing the assignment.<br>Default value: lru<br>Possible values = undef, lru</td></tr><tr><td>ifvaluetoobig</td><td>&lt;String></td><td>Read-write</td><td>Action to perform if an value is assigned to a text variable that exceeds its configured max-size,<br>or if a key is used that exceeds its configured max-size:<br>truncate - (default) truncate the text string to the first max-size bytes and proceed.<br>undef - force the assignment or expression evaluation to return an undefined (Undef) result to the policy executing the assignment or expression.<br>Default value: truncate<br>Possible values = undef, truncate</td></tr><tr><td>ifnovalue</td><td>&lt;String></td><td>Read-write</td><td>Action to perform if on a variable reference in an expression if the variable is single-valued and uninitialized<br>or if the variable is a map and there is no value for the specified key:<br>init - (default) initialize the single-value variable, or create a map entry for the key and the initial value,<br>using the -init value or its default.<br>undef - force the expression evaluation to return an undefined (Undef) result to the policy executing the expression.<br>Default value: init<br>Possible values = undef, init</td></tr><tr><td>init</td><td>&lt;String></td><td>Read-write</td><td>Initialization value for values in this variable. Default: 0 for ulong, NULL for text.</td></tr><tr><td>expires</td><td>&lt;Double></td><td>Read-write</td><td>Value expiration in seconds. If the value is not referenced within the expiration period it will be deleted. 0 (the default) means no expiration.<br>Minimum value = 0<br>Maximum value = 31622400</td></tr><tr><td>comment</td><td>&lt;String></td><td>Read-write</td><td>Comments associated with this variable.</td></tr><tr><td>referencecount</td><td>&lt;Double></td><td>Read-only</td><td>The number of references to the variable in expressions and assignments.</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD]()| [UPDATE](#u)| [UNSET](#)| [DELETE](#d)| [GET (ALL)](#get-)| [GET]()| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsvariable
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"nsvariable":{<b>"name":<String_value>,</b><b>"type":<String_value>,</b>"scope":<String_value>,"iffull":<String_value>,"ifvaluetoobig":<String_value>,"ifnovalue":<String_value>,"init":<String_value>,"expires":<Double_value>,"comment":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsvariable
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"nsvariable":{<b>"name":<String_value>,</b>"type":<String_value>,"iffull":<String_value>,"ifvaluetoobig":<String_value>,"ifnovalue":<String_value>,"init":<String_value>,"expires":<Double_value>,"comment":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsvariable?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"nsvariable":{<b>"name":<String_value>,</b>"iffull":true,"ifvaluetoobig":true,"ifnovalue":true,"init":true,"expires":true,"comment":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsvariable/name_value&lt;String&gt;
<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsvariable
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsvariable?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsvariable?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of nsvariable resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsvariable?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsvariable?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the nsvariable resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "nsvariable": [ {"name":<String_value>,"type":<String_value>,"scope":<String_value>,"iffull":<String_value>,"ifvaluetoobig":<String_value>,"ifnovalue":<String_value>,"expires":<Double_value>,"init":<String_value>,"comment":<String_value>,"referencecount":<Double_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsvariable/name_value&lt;String&gt;
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsvariable/name_value&lt;String&gt;?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsvariable/name_value&lt;String&gt;?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "nsvariable": [ {"name":<String_value>,"type":<String_value>,"scope":<String_value>,"iffull":<String_value>,"ifvaluetoobig":<String_value>,"ifnovalue":<String_value>,"expires":<Double_value>,"init":<String_value>,"comment":<String_value>,"referencecount":<Double_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsvariable?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "nsvariable": [ { "__count": "#no"} ] }```



