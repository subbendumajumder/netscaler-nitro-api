#dnspolicy

Configuration for DNS policy resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the DNS policy.</td><tr><tr><td>rule</td><td>&lt;String></td><td>Read-write</td><td>Expression against which DNS traffic is evaluated. Written in the default syntax.&lt;br>Note:&lt;br>* On the command line interface, if the expression includes blank spaces, the entire expression must be enclosed in double quotation marks.&lt;br>* If the expression itself includes double quotation marks, you must escape the quotations by using the character. &lt;br>* Alternatively, you can use single quotation marks to enclose the rule, in which case you do not have to escape the double quotation marks. &lt;br>Maximum length of a string literal in the expression is 255 characters. A longer string can be split into smaller strings of up to 255 characters each, and the smaller strings concatenated with the + operator. For example, you can create a 500-character string as follows: ";lt;string of 255 characters;gt;" + ";lt;string of 245 characters;gt;"&lt;br>Example: CLIENT.UDP.DNS.DOMAIN.EQ("domainname").</td><tr><tr><td>viewname</td><td>&lt;String></td><td>Read-write</td><td>The view name that must be used for the given policy.</td><tr><tr><td>preferredlocation</td><td>&lt;String></td><td>Read-write</td><td>The location used for the given policy. This is deprecated attribute. Please use -prefLocList.</td><tr><tr><td>preferredloclist</td><td>&lt;String[]></td><td>Read-write</td><td>The location list in priority order used for the given policy.&lt;br>Minimum length = 1</td><tr><tr><td>drop</td><td>&lt;String></td><td>Read-write</td><td>The dns packet must be dropped.&lt;br>Possible values = YES, NO</td><tr><tr><td>cachebypass</td><td>&lt;String></td><td>Read-write</td><td>By pass dns cache for this.&lt;br>Possible values = YES, NO</td><tr><tr><td>actionname</td><td>&lt;String></td><td>Read-write</td><td>Name of the DNS action to perform when the rule evaluates to TRUE. The built in actions function as follows:&lt;br>* dns_default_act_Drop. Drop the DNS request.&lt;br>* dns_default_act_Cachebypass. Bypass the DNS cache and forward the request to the name server.&lt;br>You can create custom actions by using the add dns action command in the CLI or the DNS ;gt; Actions ;gt; Create DNS Action dialog box in the NetScaler configuration utility.</td><tr><tr><td>logaction</td><td>&lt;String></td><td>Read-write</td><td>Name of the messagelog action to use for requests that match this policy.</td><tr><tr><td>hits</td><td>&lt;Double></td><td>Read-only</td><td>The number of times the policy has been hit.</td><tr><tr><td>undefhits</td><td>&lt;Double></td><td>Read-only</td><td>Number of Undef hits.</td><tr><tr><td>description</td><td>&lt;String></td><td>Read-only</td><td>Description of the policy.</td><tr><tr><td>builtin</td><td>&lt;String[]></td><td>Read-only</td><td>Flag to determine whether DNS policy is default or not.&lt;br>Possible values = MODIFIABLE, DELETABLE, IMMUTABLE, PARTITION_ALL</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [DELETE](#delete) | [UPDATE](#update) | [UNSET](#unset) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnspolicy
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"dnspolicy":{      "name":<String_value>,      "rule":<String_value>,      "viewname":<String_value>,      "preferredlocation":<String_value>,      "preferredloclist":<String[]_value>,      "drop":<String_value>,      "cachebypass":<String_value>,      "actionname":<String_value>,      "logaction":<String_value>}}```
Response:
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnspolicy/name_value&lt;String&gt;
HTTP Method: DELETE
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnspolicy
HTTP Method: PUT
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"dnspolicy":{      "name":<String_value>,      "rule":<String_value>,      "viewname":<String_value>,      "preferredlocation":<String_value>,      "preferredloclist":<String[]_value>,      "drop":<String_value>,      "cachebypass":<String_value>,      "actionname":<String_value>,      "logaction":<String_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnspolicy?action=unset
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"dnspolicy":{      "name":<String_value>,      "logaction":true}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnspolicy
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnspolicy?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


filter
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnspolicy?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of dnspolicy resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnspolicy?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).


pagination
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnspolicy?pagesize=#no;pageno=#no
Use this query-parameter to get the dnspolicy resources in chunks.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "dnspolicy": [ {      "name":<String_value>,      "rule":<String_value>,      "viewname":<String_value>,      "preferredlocation":<String_value>,      "preferredloclist":<String[]_value>,      "hits":<Double_value>,      "undefhits":<Double_value>,      "drop":<String_value>,      "actionname":<String_value>,      "cachebypass":<String_value>,      "description":<String_value>,      "logaction":<String_value>,      "builtin":<String[]_value>}]}```



###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnspolicy/name_value&lt;String&gt;
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnspolicy/name_value&lt;String&gt;?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnspolicy/name_value&lt;String&gt;?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "dnspolicy": [ {      "name":<String_value>,      "rule":<String_value>,      "viewname":<String_value>,      "preferredlocation":<String_value>,      "preferredloclist":<String[]_value>,      "hits":<Double_value>,      "undefhits":<Double_value>,      "drop":<String_value>,      "actionname":<String_value>,      "cachebypass":<String_value>,      "description":<String_value>,      "logaction":<String_value>,      "builtin":<String[]_value>}]}```



###count



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnspolicy?count=yes
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: 
{ "dnspolicy": [ { "__count": "#no"} ] }


