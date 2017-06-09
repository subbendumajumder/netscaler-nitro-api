#cachecontentgroup

Configuration for Integrated Cache content group resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the content group. Must begin with an ASCII alphabetic or underscore (_) character, and must contain only ASCII alphanumeric, underscore, hash (#), period (.), space, colon (:), at (@), equals (=), and hyphen (-) characters. Cannot be changed after the content group is created.&lt;br>Minimum length = 1</td><tr><tr><td>weakposrelexpiry</td><td>&lt;Double></td><td>Read-write</td><td>Relative expiry time, in seconds, for expiring positive responses with response codes between 200 and 399. Cannot be used in combination with other Expiry attributes. Similar to -relExpiry but has lower precedence.&lt;br>Minimum value = 0&lt;br>Maximum value = 31536000</td><tr><tr><td>heurexpiryparam</td><td>&lt;Double></td><td>Read-write</td><td>Heuristic expiry time, in percent of the duration, since the object was last modified.&lt;br>Minimum value = 0&lt;br>Maximum value = 100</td><tr><tr><td>relexpiry</td><td>&lt;Double></td><td>Read-write</td><td>Relative expiry time, in seconds, after which to expire an object cached in this content group.&lt;br>Minimum value = 0&lt;br>Maximum value = 31536000</td><tr><tr><td>relexpirymillisec</td><td>&lt;Double></td><td>Read-write</td><td>Relative expiry time, in milliseconds, after which to expire an object cached in this content group.&lt;br>Minimum value = 0&lt;br>Maximum value = 86400000</td><tr><tr><td>absexpiry</td><td>&lt;String[]></td><td>Read-write</td><td>Local time, up to 4 times a day, at which all objects in the content group must expire. &lt;br>&lt;br>CLI Users:&lt;br>For example, to specify that the objects in the content group should expire by 11:00 PM, type the following command: add cache contentgroup ;lt;contentgroup name;gt; -absexpiry 23:00 &lt;br>To specify that the objects in the content group should expire at 10:00 AM, 3 PM, 6 PM, and 11:00 PM, type: add cache contentgroup ;lt;contentgroup name;gt; -absexpiry 10:00 15:00 18:00 23:00.</td><tr><tr><td>absexpirygmt</td><td>&lt;String[]></td><td>Read-write</td><td>Coordinated Universal Time (GMT), up to 4 times a day, when all objects in the content group must expire.</td><tr><tr><td>weaknegrelexpiry</td><td>&lt;Double></td><td>Read-write</td><td>Relative expiry time, in seconds, for expiring negative responses. This value is used only if the expiry time cannot be determined from any other source. It is applicable only to the following status codes: 307, 403, 404, and 410.&lt;br>Minimum value = 0&lt;br>Maximum value = 31536000</td><tr><tr><td>hitparams</td><td>&lt;String[]></td><td>Read-write</td><td>Parameters to use for parameterized hit evaluation of an object. Up to 128 parameters can be specified. Mutually exclusive with the Hit Selector parameter.&lt;br>Minimum length = 1</td><tr><tr><td>invalparams</td><td>&lt;String[]></td><td>Read-write</td><td>Parameters for parameterized invalidation of an object. You can specify up to 8 parameters. Mutually exclusive with invalSelector.&lt;br>Minimum length = 1</td><tr><tr><td>ignoreparamvaluecase</td><td>&lt;String></td><td>Read-write</td><td>Ignore case when comparing parameter values during parameterized hit evaluation. (Parameter value case is ignored by default during parameterized invalidation.).&lt;br>Possible values = YES, NO</td><tr><tr><td>matchcookies</td><td>&lt;String></td><td>Read-write</td><td>Evaluate for parameters in the cookie header also.&lt;br>Possible values = YES, NO</td><tr><tr><td>invalrestrictedtohost</td><td>&lt;String></td><td>Read-write</td><td>Take the host header into account during parameterized invalidation.&lt;br>Possible values = YES, NO</td><tr><tr><td>polleverytime</td><td>&lt;String></td><td>Read-write</td><td>Always poll for the objects in this content group. That is, retrieve the objects from the origin server whenever they are requested.&lt;br>Default value: NO&lt;br>Possible values = YES, NO</td><tr><tr><td>ignorereloadreq</td><td>&lt;String></td><td>Read-write</td><td>Ignore any request to reload a cached object from the origin server.&lt;br>To guard against Denial of Service attacks, set this parameter to YES. For RFC-compliant behavior, set it to NO.&lt;br>Default value: YES&lt;br>Possible values = YES, NO</td><tr><tr><td>removecookies</td><td>&lt;String></td><td>Read-write</td><td>Remove cookies from responses.&lt;br>Default value: YES&lt;br>Possible values = YES, NO</td><tr><tr><td>prefetch</td><td>&lt;String></td><td>Read-write</td><td>Attempt to refresh objects that are about to go stale.&lt;br>Default value: YES&lt;br>Possible values = YES, NO</td><tr><tr><td>prefetchperiod</td><td>&lt;Double></td><td>Read-write</td><td>Time period, in seconds before an objects calculated expiry time, during which to attempt prefetch.&lt;br>Minimum value = 0&lt;br>Maximum value = 4294967294</td><tr><tr><td>prefetchperiodmillisec</td><td>&lt;Double></td><td>Read-write</td><td>Time period, in milliseconds before an objects calculated expiry time, during which to attempt prefetch.&lt;br>Minimum value = 0&lt;br>Maximum value = 4294967290</td><tr><tr><td>prefetchmaxpending</td><td>&lt;Double></td><td>Read-write</td><td>Maximum number of outstanding prefetches that can be queued for the content group.&lt;br>Minimum value = 0&lt;br>Maximum value = 4294967294</td><tr><tr><td>flashcache</td><td>&lt;String></td><td>Read-write</td><td>Perform flash cache. Mutually exclusive with Poll Every Time (PET) on the same content group.&lt;br>Default value: NO&lt;br>Possible values = YES, NO</td><tr><tr><td>expireatlastbyte</td><td>&lt;String></td><td>Read-write</td><td>Force expiration of the content immediately after the response is downloaded (upon receipt of the last byte of the response body). Applicable only to positive responses.&lt;br>Default value: NO&lt;br>Possible values = YES, NO</td><tr><tr><td>insertvia</td><td>&lt;String></td><td>Read-write</td><td>Insert a Via header into the response.&lt;br>Default value: YES&lt;br>Possible values = YES, NO</td><tr><tr><td>insertage</td><td>&lt;String></td><td>Read-write</td><td>Insert an Age header into the response. An Age header contains information about the age of the object, in seconds, as calculated by the integrated cache.&lt;br>Default value: YES&lt;br>Possible values = YES, NO</td><tr><tr><td>insertetag</td><td>&lt;String></td><td>Read-write</td><td>Insert an ETag header in the response. With ETag header insertion, the integrated cache does not serve full responses on repeat requests.&lt;br>Default value: YES&lt;br>Possible values = YES, NO</td><tr><tr><td>cachecontrol</td><td>&lt;String></td><td>Read-write</td><td>Insert a Cache-Control header into the response.&lt;br>Minimum length = 1</td><tr><tr><td>quickabortsize</td><td>&lt;Double></td><td>Read-write</td><td>If the size of an object that is being downloaded is less than or equal to the quick abort value, and a client aborts during the download, the cache stops downloading the response. If the object is larger than the quick abort size, the cache continues to download the response.&lt;br>Default value: 4194303&lt;br>Minimum value = 0&lt;br>Maximum value = 4194303</td><tr><tr><td>minressize</td><td>&lt;Double></td><td>Read-write</td><td>Minimum size of a response that can be cached in this content group.&lt;br> Default minimum response size is 0.&lt;br>Minimum value = 0&lt;br>Maximum value = 2097151</td><tr><tr><td>maxressize</td><td>&lt;Double></td><td>Read-write</td><td>Maximum size of a response that can be cached in this content group.&lt;br>Default value: 80&lt;br>Minimum value = 0&lt;br>Maximum value = 2097151</td><tr><tr><td>memlimit</td><td>&lt;Double></td><td>Read-write</td><td>Maximum amount of memory that the cache can use. The effective limit is based on the available memory of the NetScaler appliance.&lt;br>Default value: 65536</td><tr><tr><td>ignorereqcachinghdrs</td><td>&lt;String></td><td>Read-write</td><td>Ignore Cache-Control and Pragma headers in the incoming request.&lt;br>Default value: YES&lt;br>Possible values = YES, NO</td><tr><tr><td>minhits</td><td>&lt;Integer></td><td>Read-write</td><td>Number of hits that qualifies a response for storage in this content group.&lt;br>Default value: 0</td><tr><tr><td>alwaysevalpolicies</td><td>&lt;String></td><td>Read-write</td><td>Force policy evaluation for each response arriving from the origin server. Cannot be set to YES if the Prefetch parameter is also set to YES.&lt;br>Default value: NO&lt;br>Possible values = YES, NO</td><tr><tr><td>persistha</td><td>&lt;String></td><td>Read-write</td><td>Setting persistHA to YES causes IC to save objects in contentgroup to Secondary node in HA deployment.&lt;br>Default value: NO&lt;br>Possible values = YES, NO</td><tr><tr><td>pinned</td><td>&lt;String></td><td>Read-write</td><td>Do not flush objects from this content group under memory pressure.&lt;br>Default value: NO&lt;br>Possible values = YES, NO</td><tr><tr><td>lazydnsresolve</td><td>&lt;String></td><td>Read-write</td><td>Perform DNS resolution for responses only if the destination IP address in the request does not match the destination IP address of the cached response.&lt;br>Default value: YES&lt;br>Possible values = YES, NO</td><tr><tr><td>hitselector</td><td>&lt;String></td><td>Read-write</td><td>Selector for evaluating whether an object gets stored in a particular content group. A selector is an abstraction for a collection of PIXL expressions.</td><tr><tr><td>invalselector</td><td>&lt;String></td><td>Read-write</td><td>Selector for invalidating objects in the content group. A selector is an abstraction for a collection of PIXL expressions.</td><tr><tr><td>type</td><td>&lt;String></td><td>Read-write</td><td>The type of the content group.&lt;br>Default value: HTTP&lt;br>Possible values = HTTP, MYSQL, MSSQL</td><tr><tr><td>query</td><td>&lt;String></td><td>Read-write</td><td>Query string specifying individual objects to flush from this group by using parameterized invalidation. If this parameter is not set, all objects are flushed from the group.&lt;br>Minimum length = 1</td><tr><tr><td>host</td><td>&lt;String></td><td>Read-write</td><td>Flush only objects that belong to the specified host. Do not use except with parameterized invalidation. Also, the Invalidation Restricted to Host parameter for the group must be set to YES.&lt;br>Minimum length = 1</td><tr><tr><td>selectorvalue</td><td>&lt;String></td><td>Read-write</td><td>Value of the selector to be used for flushing objects from the content group. Requires that an invalidation selector be configured for the content group.&lt;br>Minimum length = 1</td><tr><tr><td>tosecondary</td><td>&lt;String></td><td>Read-write</td><td>content group whose objects are to be sent to secondary.&lt;br>Default value: NO&lt;br>Possible values = YES, NO</td><tr><tr><td>flags</td><td>&lt;Double></td><td>Read-only</td><td>Flags.</td><tr><tr><td>prefetchcur</td><td>&lt;Double></td><td>Read-only</td><td>Current outstanding prefetches.</td><tr><tr><td>memusage</td><td>&lt;Double></td><td>Read-only</td><td>Current memory usage.</td><tr><tr><td>memdusage</td><td>&lt;Double></td><td>Read-only</td><td>Current disk memory usage.</td><tr><tr><td>disklimit</td><td>&lt;Double></td><td>Read-only</td><td>Maximum amount of disk that the cache can use. The effective limit is based on the available memory of the NetScaler appliance.&lt;br>Default value: 0</td><tr><tr><td>cachenon304hits</td><td>&lt;Double></td><td>Read-only</td><td>Cache non 304 hits.</td><tr><tr><td>cache304hits</td><td>&lt;Double></td><td>Read-only</td><td>Cache 304 hits.</td><tr><tr><td>cachecells</td><td>&lt;Double></td><td>Read-only</td><td>Number of cells.</td><tr><tr><td>cachegroupincarnation</td><td>&lt;Double></td><td>Read-only</td><td>Cache group incarnation.</td><tr><tr><td>persist</td><td>&lt;String></td><td>Read-only</td><td>Setting persist to YES causes IC to save objects in contentgroup to disk.&lt;br>Default value: NO&lt;br>Possible values = YES, NO</td><tr><tr><td>policyname</td><td>&lt;String[]></td><td>Read-only</td><td>Active cache policies refering to this group.</td><tr><tr><td>cachenuminvalpolicy</td><td>&lt;Double></td><td>Read-only</td><td>Number of active Invalidation policies refering to this group.</td><tr><tr><td>markercells</td><td>&lt;Double></td><td>Read-only</td><td>Numbers of marker cells in this group.</td><tr><tr><td>builtin</td><td>&lt;String[]></td><td>Read-only</td><td>.&lt;br>Possible values = MODIFIABLE, DELETABLE, IMMUTABLE, PARTITION_ALL</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [DELETE](#delete) | [UPDATE](#update) | [UNSET](#unset) | [EXPIRE](#expire) | [FLUSH](#flush) | [SAVE](#save) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/cachecontentgroup
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"cachecontentgroup":{      "name":<String_value>,      "weakposrelexpiry":<Double_value>,      "heurexpiryparam":<Double_value>,      "relexpiry":<Double_value>,      "relexpirymillisec":<Double_value>,      "absexpiry":<String[]_value>,      "absexpirygmt":<String[]_value>,      "weaknegrelexpiry":<Double_value>,      "hitparams":<String[]_value>,      "invalparams":<String[]_value>,      "ignoreparamvaluecase":<String_value>,      "matchcookies":<String_value>,      "invalrestrictedtohost":<String_value>,      "polleverytime":<String_value>,      "ignorereloadreq":<String_value>,      "removecookies":<String_value>,      "prefetch":<String_value>,      "prefetchperiod":<Double_value>,      "prefetchperiodmillisec":<Double_value>,      "prefetchmaxpending":<Double_value>,      "flashcache":<String_value>,      "expireatlastbyte":<String_value>,      "insertvia":<String_value>,      "insertage":<String_value>,      "insertetag":<String_value>,      "cachecontrol":<String_value>,      "quickabortsize":<Double_value>,      "minressize":<Double_value>,      "maxressize":<Double_value>,      "memlimit":<Double_value>,      "ignorereqcachinghdrs":<String_value>,      "minhits":<Integer_value>,      "alwaysevalpolicies":<String_value>,      "persistha":<String_value>,      "pinned":<String_value>,      "lazydnsresolve":<String_value>,      "hitselector":<String_value>,      "invalselector":<String_value>,      "type":<String_value>}}```
Response:
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/cachecontentgroup/name_value&lt;String&gt;
HTTP Method: DELETE
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/cachecontentgroup
HTTP Method: PUT
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"cachecontentgroup":{      "name":<String_value>,      "weakposrelexpiry":<Double_value>,      "heurexpiryparam":<Double_value>,      "relexpiry":<Double_value>,      "relexpirymillisec":<Double_value>,      "absexpiry":<String[]_value>,      "absexpirygmt":<String[]_value>,      "weaknegrelexpiry":<Double_value>,      "hitparams":<String[]_value>,      "invalparams":<String[]_value>,      "ignoreparamvaluecase":<String_value>,      "matchcookies":<String_value>,      "invalrestrictedtohost":<String_value>,      "polleverytime":<String_value>,      "ignorereloadreq":<String_value>,      "removecookies":<String_value>,      "prefetch":<String_value>,      "prefetchperiod":<Double_value>,      "prefetchperiodmillisec":<Double_value>,      "prefetchmaxpending":<Double_value>,      "flashcache":<String_value>,      "expireatlastbyte":<String_value>,      "insertvia":<String_value>,      "insertage":<String_value>,      "insertetag":<String_value>,      "cachecontrol":<String_value>,      "quickabortsize":<Double_value>,      "minressize":<Double_value>,      "maxressize":<Double_value>,      "memlimit":<Double_value>,      "ignorereqcachinghdrs":<String_value>,      "minhits":<Integer_value>,      "alwaysevalpolicies":<String_value>,      "persistha":<String_value>,      "pinned":<String_value>,      "lazydnsresolve":<String_value>,      "hitselector":<String_value>,      "invalselector":<String_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/cachecontentgroup?action=unset
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"cachecontentgroup":{      "name":<String_value>,      "weakposrelexpiry":true,      "heurexpiryparam":true,      "relexpiry":true,      "relexpirymillisec":true,      "absexpiry":true,      "absexpirygmt":true,      "weaknegrelexpiry":true,      "hitparams":true,      "invalparams":true,      "ignoreparamvaluecase":true,      "matchcookies":true,      "invalrestrictedtohost":true,      "polleverytime":true,      "ignorereloadreq":true,      "removecookies":true,      "prefetch":true,      "prefetchperiod":true,      "prefetchperiodmillisec":true,      "prefetchmaxpending":true,      "flashcache":true,      "expireatlastbyte":true,      "insertvia":true,      "insertage":true,      "insertetag":true,      "cachecontrol":true,      "quickabortsize":true,      "minressize":true,      "maxressize":true,      "memlimit":true,      "ignorereqcachinghdrs":true,      "minhits":true,      "alwaysevalpolicies":true,      "persistha":true,      "pinned":true,      "lazydnsresolve":true,      "hitselector":true,      "invalselector":true}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###expire



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/cachecontentgroup?action=expire
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"cachecontentgroup":{      "name":<String_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###flush



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/cachecontentgroup?action=flush
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"cachecontentgroup":{      "name":<String_value>,      "query":<String_value>,      "host":<String_value>,      "selectorvalue":<String_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###save



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/cachecontentgroup?action=save
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"cachecontentgroup":{      "name":<String_value>,      "tosecondary":<String_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/cachecontentgroup
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/cachecontentgroup?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


filter
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/cachecontentgroup?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of cachecontentgroup resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/cachecontentgroup?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).


pagination
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/cachecontentgroup?pagesize=#no;pageno=#no
Use this query-parameter to get the cachecontentgroup resources in chunks.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "cachecontentgroup": [ {      "name":<String_value>,      "flags":<Double_value>,      "type":<String_value>,      "relexpiry":<Double_value>,      "relexpirymillisec":<Double_value>,      "absexpiry":<String[]_value>,      "absexpirygmt":<String[]_value>,      "heurexpiryparam":<Double_value>,      "weakposrelexpiry":<Double_value>,      "weaknegrelexpiry":<Double_value>,      "hitparams":<String[]_value>,      "invalparams":<String[]_value>,      "ignoreparamvaluecase":<String_value>,      "matchcookies":<String_value>,      "invalrestrictedtohost":<String_value>,      "polleverytime":<String_value>,      "ignorereloadreq":<String_value>,      "removecookies":<String_value>,      "prefetch":<String_value>,      "prefetchperiod":<Double_value>,      "prefetchperiodmillisec":<Double_value>,      "prefetchcur":<Double_value>,      "prefetchmaxpending":<Double_value>,      "flashcache":<String_value>,      "expireatlastbyte":<String_value>,      "insertvia":<String_value>,      "insertage":<String_value>,      "insertetag":<String_value>,      "cachecontrol":<String_value>,      "quickabortsize":<Double_value>,      "minressize":<Double_value>,      "maxressize":<Double_value>,      "memusage":<Double_value>,      "memdusage":<Double_value>,      "disklimit":<Double_value>,      "memlimit":<Double_value>,      "ignorereqcachinghdrs":<String_value>,      "cachenon304hits":<Double_value>,      "cache304hits":<Double_value>,      "cachecells":<Double_value>,      "cachegroupincarnation":<Double_value>,      "minhits":<Integer_value>,      "alwaysevalpolicies":<String_value>,      "persist":<String_value>,      "persistha":<String_value>,      "pinned":<String_value>,      "lazydnsresolve":<String_value>,      "hitselector":<String_value>,      "invalselector":<String_value>,      "policyname":<String[]_value>,      "cachenuminvalpolicy":<Double_value>,      "markercells":<Double_value>,      "builtin":<String[]_value>}]}```



###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/cachecontentgroup/name_value&lt;String&gt;
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/cachecontentgroup/name_value&lt;String&gt;?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/cachecontentgroup/name_value&lt;String&gt;?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "cachecontentgroup": [ {      "name":<String_value>,      "flags":<Double_value>,      "type":<String_value>,      "relexpiry":<Double_value>,      "relexpirymillisec":<Double_value>,      "absexpiry":<String[]_value>,      "absexpirygmt":<String[]_value>,      "heurexpiryparam":<Double_value>,      "weakposrelexpiry":<Double_value>,      "weaknegrelexpiry":<Double_value>,      "hitparams":<String[]_value>,      "invalparams":<String[]_value>,      "ignoreparamvaluecase":<String_value>,      "matchcookies":<String_value>,      "invalrestrictedtohost":<String_value>,      "polleverytime":<String_value>,      "ignorereloadreq":<String_value>,      "removecookies":<String_value>,      "prefetch":<String_value>,      "prefetchperiod":<Double_value>,      "prefetchperiodmillisec":<Double_value>,      "prefetchcur":<Double_value>,      "prefetchmaxpending":<Double_value>,      "flashcache":<String_value>,      "expireatlastbyte":<String_value>,      "insertvia":<String_value>,      "insertage":<String_value>,      "insertetag":<String_value>,      "cachecontrol":<String_value>,      "quickabortsize":<Double_value>,      "minressize":<Double_value>,      "maxressize":<Double_value>,      "memusage":<Double_value>,      "memdusage":<Double_value>,      "disklimit":<Double_value>,      "memlimit":<Double_value>,      "ignorereqcachinghdrs":<String_value>,      "cachenon304hits":<Double_value>,      "cache304hits":<Double_value>,      "cachecells":<Double_value>,      "cachegroupincarnation":<Double_value>,      "minhits":<Integer_value>,      "alwaysevalpolicies":<String_value>,      "persist":<String_value>,      "persistha":<String_value>,      "pinned":<String_value>,      "lazydnsresolve":<String_value>,      "hitselector":<String_value>,      "invalselector":<String_value>,      "policyname":<String[]_value>,      "cachenuminvalpolicy":<Double_value>,      "markercells":<Double_value>,      "builtin":<String[]_value>}]}```



###count



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/cachecontentgroup?count=yes
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: 
{ "cachecontentgroup": [ { "__count": "#no"} ] }


