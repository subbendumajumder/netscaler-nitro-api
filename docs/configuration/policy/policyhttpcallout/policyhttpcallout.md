#policyhttpcallout

Configuration for HTTP callout resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the HTTP callout. Not case sensitive. Must begin with an ASCII letter or underscore (_) character, and must consist only of ASCII alphanumeric or underscore characters. Must not begin with 're' or 'xp' or be a word reserved for use as a default syntax expression qualifier prefix (such as HTTP) or enumeration value (such as ASCII). Must not be the name of an existing named expression, pattern set, dataset, stringmap, or HTTP callout.<br>Minimum length = 1</td></tr><tr><td>ipaddress</td><td>&lt;String></td><td>Read-write</td><td>IP Address of the server (callout agent) to which the callout is sent. Can be an IPv4 or IPv6 address.<br>Mutually exclusive with the Virtual Server parameter. Therefore, you cannot set the &lt;IP Address, Port&gt; and the Virtual Server in the same HTTP callout.</td></tr><tr><td>port</td><td>&lt;Integer></td><td>Read-write</td><td>Server port to which the HTTP callout agent is mapped. Mutually exclusive with the Virtual Server parameter. Therefore, you cannot set the &lt;IP Address, Port&gt; and the Virtual Server in the same HTTP callout.<br>Minimum value = 1</td></tr><tr><td>vserver</td><td>&lt;String></td><td>Read-write</td><td>Name of the load balancing, content switching, or cache redirection virtual server (the callout agent) to which the HTTP callout is sent. The service type of the virtual server must be HTTP. Mutually exclusive with the IP address and port parameters. Therefore, you cannot set the &lt;IP Address, Port&gt; and the Virtual Server in the same HTTP callout.<br>Minimum length = 1</td></tr><tr><td>returntype</td><td>&lt;String></td><td>Read-write</td><td>Type of data that the target callout agent returns in response to the callout. <br>Available settings function as follows:<br>* TEXT - Treat the returned value as a text string. <br>* NUM - Treat the returned value as a number.<br>* BOOL - Treat the returned value as a Boolean value. <br>Note: You cannot change the return type after it is set.<br>Possible values = BOOL, NUM, TEXT</td></tr><tr><td>httpmethod</td><td>&lt;String></td><td>Read-write</td><td>Method used in the HTTP request that this callout sends. Mutually exclusive with the full HTTP request expression.<br>Possible values = GET, POST</td></tr><tr><td>hostexpr</td><td>&lt;String></td><td>Read-write</td><td>Default Syntax string expression to configure the Host header. Can contain a literal value (for example, 10.101.10.11) or a derived value (for example, http.req.header("Host")). The literal value can be an IP address or a fully qualified domain name. Mutually exclusive with the full HTTP request expression.<br>Minimum length = 1</td></tr><tr><td>urlstemexpr</td><td>&lt;String></td><td>Read-write</td><td>Default Syntax string expression for generating the URL stem. Can contain a literal string (for example, "/mysite/index.html") or an expression that derives the value (for example, http.req.url). Mutually exclusive with the full HTTP request expression.<br>Minimum length = 1</td></tr><tr><td>headers</td><td>&lt;String[]></td><td>Read-write</td><td>One or more headers to insert into the HTTP request. Each header is specified as "name(expr)", where expr is a default syntax expression that is evaluated at runtime to provide the value for the named header. You can configure a maximum of eight headers for an HTTP callout. Mutually exclusive with the full HTTP request expression.</td></tr><tr><td>parameters</td><td>&lt;String[]></td><td>Read-write</td><td>One or more query parameters to insert into the HTTP request URL (for a GET request) or into the request body (for a POST request). Each parameter is specified as "name(expr)", where expr is an default syntax expression that is evaluated at run time to provide the value for the named parameter (name=value). The parameter values are URL encoded. Mutually exclusive with the full HTTP request expression.</td></tr><tr><td>bodyexpr</td><td>&lt;String></td><td>Read-write</td><td>An advanced string expression for generating the body of the request. The expression can contain a literal string or an expression that derives the value (for example, client.ip.src). Mutually exclusive with -fullReqExpr.<br>Minimum length = 1</td></tr><tr><td>fullreqexpr</td><td>&lt;String></td><td>Read-write</td><td>Exact HTTP request, in the form of a default syntax expression, which the NetScaler appliance sends to the callout agent. If you set this parameter, you must not include HTTP method, host expression, URL stem expression, headers, or parameters.<br>The request expression is constrained by the feature for which the callout is used. For example, an HTTP.RES expression cannot be used in a request-time policy bank or in a TCP content switching policy bank.<br>The NetScaler appliance does not check the validity of this request. You must manually validate the request.<br>Minimum length = 1</td></tr><tr><td>scheme</td><td>&lt;String></td><td>Read-write</td><td>Type of scheme for the callout server.<br>Possible values = http, https</td></tr><tr><td>resultexpr</td><td>&lt;String></td><td>Read-write</td><td>Expression that extracts the callout results from the response sent by the HTTP callout agent. Must be a response based expression, that is, it must begin with HTTP.RES. The operations in this expression must match the return type. For example, if you configure a return type of TEXT, the result expression must be a text based expression. If the return type is NUM, the result expression (resultExpr) must return a numeric value, as in the following example: http.res.body(10000).length.<br>Minimum length = 1</td></tr><tr><td>cacheforsecs</td><td>&lt;Double></td><td>Read-write</td><td>Duration, in seconds, for which the callout response is cached. The cached responses are stored in an integrated caching content group named "calloutContentGroup". If no duration is configured, the callout responses will not be cached unless normal caching configuration is used to cache them. This parameter takes precedence over any normal caching configuration that would otherwise apply to these responses.<br>Note that the calloutContentGroup definition may not be modified or removed nor may it be used with other cache policies.<br>Minimum value = 1<br>Maximum value = 31536000</td></tr><tr><td>comment</td><td>&lt;String></td><td>Read-write</td><td>Any comments to preserve information about this HTTP callout.</td></tr><tr><td>hits</td><td>&lt;Double></td><td>Read-only</td><td>Total hits.</td></tr><tr><td>undefhits</td><td>&lt;Double></td><td>Read-only</td><td>Total undefs.</td></tr><tr><td>svrstate</td><td>&lt;String></td><td>Read-only</td><td>The state of the service.<br>Possible values = UP, DOWN, UNKNOWN, BUSY, OUT OF SERVICE, GOING OUT OF SERVICE, DOWN WHEN GOING OUT OF SERVICE, NS_EMPTY_STR, Unknown, DISABLED</td></tr><tr><td>effectivestate</td><td>&lt;String></td><td>Read-only</td><td>The effective state of the service.<br>Possible values = UP, DOWN, UNKNOWN, BUSY, OUT OF SERVICE, GOING OUT OF SERVICE, DOWN WHEN GOING OUT OF SERVICE, NS_EMPTY_STR, Unknown, DISABLED</td></tr><tr><td>undefreason</td><td>&lt;String></td><td>Read-only</td><td>Reason for last undef.<br>Possible values = Failed to add service, Vserver not found, Not a HTTP or SSL vserver, Generated callout request is invalid, Content-Length header not found in callout request, Not enough space to put Content-Length value, Config incomplete, Server is DOWN, Creating callout connection failed, No memory to generate callout request packets, No memory to create callout task, No memory to create callout async, Callout request expression undef, No callout response expression, Skipped callout response eval, Callout response pixl init undef, Callout response expression undef</td></tr><tr><td>recursivecallout</td><td>&lt;Double></td><td>Read-only</td><td>Number of recursive callouts.</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD]()| [DELETE](#d)| [UPDATE](#u)| [UNSET](#)| [GET (ALL)](#get-)| [GET]()| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/policyhttpcallout
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"policyhttpcallout":{<b>"name":<String_value>,</b>"ipaddress":<String_value>,"port":<Integer_value>,"vserver":<String_value>,"returntype":<String_value>,"httpmethod":<String_value>,"hostexpr":<String_value>,"urlstemexpr":<String_value>,"headers":<String[]_value>,"parameters":<String[]_value>,"bodyexpr":<String_value>,"fullreqexpr":<String_value>,"scheme":<String_value>,"resultexpr":<String_value>,"cacheforsecs":<Double_value>,"comment":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/policyhttpcallout/name_value&lt;String&gt;
<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/policyhttpcallout
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"policyhttpcallout":{<b>"name":<String_value>,</b>"ipaddress":<String_value>,"port":<Integer_value>,"vserver":<String_value>,"returntype":<String_value>,"httpmethod":<String_value>,"hostexpr":<String_value>,"urlstemexpr":<String_value>,"headers":<String[]_value>,"parameters":<String[]_value>,"bodyexpr":<String_value>,"fullreqexpr":<String_value>,"scheme":<String_value>,"resultexpr":<String_value>,"cacheforsecs":<Double_value>,"comment":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/policyhttpcallout?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"policyhttpcallout":{<b>"name":<String_value>,</b>"ipaddress":true,"port":true,"vserver":true,"httpmethod":true,"hostexpr":true,"urlstemexpr":true,"headers":true,"parameters":true,"bodyexpr":true,"fullreqexpr":true,"resultexpr":true,"cacheforsecs":true,"comment":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/policyhttpcallout
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/policyhttpcallout?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/policyhttpcallout?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of policyhttpcallout resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/policyhttpcallout?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/policyhttpcallout?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the policyhttpcallout resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "policyhttpcallout": [ {"name":<String_value>,"ipaddress":<String_value>,"port":<Integer_value>,"vserver":<String_value>,"returntype":<String_value>,"scheme":<String_value>,"httpmethod":<String_value>,"hostexpr":<String_value>,"urlstemexpr":<String_value>,"headers":<String[]_value>,"parameters":<String[]_value>,"fullreqexpr":<String_value>,"resultexpr":<String_value>,"hits":<Double_value>,"undefhits":<Double_value>,"svrstate":<String_value>,"effectivestate":<String_value>,"undefreason":<String_value>,"recursivecallout":<Double_value>,"bodyexpr":<String_value>,"cacheforsecs":<Double_value>,"comment":<String_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/policyhttpcallout/name_value&lt;String&gt;
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/policyhttpcallout/name_value&lt;String&gt;?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/policyhttpcallout/name_value&lt;String&gt;?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "policyhttpcallout": [ {"name":<String_value>,"ipaddress":<String_value>,"port":<Integer_value>,"vserver":<String_value>,"returntype":<String_value>,"scheme":<String_value>,"httpmethod":<String_value>,"hostexpr":<String_value>,"urlstemexpr":<String_value>,"headers":<String[]_value>,"parameters":<String[]_value>,"fullreqexpr":<String_value>,"resultexpr":<String_value>,"hits":<Double_value>,"undefhits":<Double_value>,"svrstate":<String_value>,"effectivestate":<String_value>,"undefreason":<String_value>,"recursivecallout":<Double_value>,"bodyexpr":<String_value>,"cacheforsecs":<Double_value>,"comment":<String_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/policyhttpcallout?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "policyhttpcallout": [ { "__count": "#no"} ] }```



