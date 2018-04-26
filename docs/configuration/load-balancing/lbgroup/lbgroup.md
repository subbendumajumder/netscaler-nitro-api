#lbgroup

Configuration for LB group resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name of the load balancing virtual server group.<br>Minimum length = 1</td></tr><tr><td>persistencetype</td><td>&lt;String></td><td>Read-write</td><td>Type of persistence for the group. Available settings function as follows:<br>* SOURCEIP - Create persistence sessions based on the client IP.<br>* COOKIEINSERT - Create persistence sessions based on a cookie in client requests. The cookie is inserted by a Set-Cookie directive from the server, in its first response to a client.<br>* RULE - Create persistence sessions based on a user defined rule.<br>* NONE - Disable persistence for the group.<br>Possible values = SOURCEIP, COOKIEINSERT, RULE, NONE</td></tr><tr><td>persistencebackup</td><td>&lt;String></td><td>Read-write</td><td>Type of backup persistence for the group.<br>Possible values = SOURCEIP, NONE</td></tr><tr><td>backuppersistencetimeout</td><td>&lt;Double></td><td>Read-write</td><td>Time period, in minutes, for which backup persistence is in effect.<br>Default value: 2<br>Minimum value = 2<br>Maximum value = 1440</td></tr><tr><td>persistmask</td><td>&lt;String></td><td>Read-write</td><td>Persistence mask to apply to source IPv4 addresses when creating source IP based persistence sessions.<br>Minimum length = 1</td></tr><tr><td>cookiename</td><td>&lt;String></td><td>Read-write</td><td>Use this parameter to specify the cookie name for COOKIE peristence type. It specifies the name of cookie with a maximum of 32 characters. If not specified, cookie name is internally generated.</td></tr><tr><td>v6persistmasklen</td><td>&lt;Double></td><td>Read-write</td><td>Persistence mask to apply to source IPv6 addresses when creating source IP based persistence sessions.<br>Default value: 128<br>Minimum value = 1<br>Maximum value = 128</td></tr><tr><td>cookiedomain</td><td>&lt;String></td><td>Read-write</td><td>Domain attribute for the HTTP cookie.<br>Minimum length = 1</td></tr><tr><td>timeout</td><td>&lt;Double></td><td>Read-write</td><td>Time period for which a persistence session is in effect.<br>Default value: 2<br>Minimum value = 0<br>Maximum value = 1440</td></tr><tr><td>rule</td><td>&lt;String></td><td>Read-write</td><td>Expression, or name of a named expression, against which traffic is evaluated. Written in the classic or default syntax.<br>Note:<br>Maximum length of a string literal in the expression is 255 characters. A longer string can be split into smaller strings of up to 255 characters each, and the smaller strings concatenated with the + operator. For example, you can create a 500-character string as follows: '"&lt;string of 255 characters&gt;" + "&lt;string of 245 characters&gt;"'<br><br>The following requirements apply only to the NetScaler CLI:<br>* If the expression includes one or more spaces, enclose the entire expression in double quotation marks.<br>* If the expression itself includes double quotation marks, escape the quotations by using the \ character. <br>* Alternatively, you can use single quotation marks to enclose the rule, in which case you do not have to escape the double quotation marks.<br>Default value: "None"</td></tr><tr><td>usevserverpersistency</td><td>&lt;String></td><td>Read-write</td><td>.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>mastervserver</td><td>&lt;String></td><td>Read-write</td><td>.</td></tr><tr><td>newname</td><td>&lt;String></td><td>Read-write</td><td>New name for the load balancing virtual server group.<br>Minimum length = 1</td></tr><tr><td>td</td><td>&lt;Double></td><td>Read-only</td><td>Integer value that uniquely identifies the traffic domain in which you want to configure the entity. If you do not specify an ID, the entity becomes part of the default traffic domain, which has an ID of 0.<br>Minimum value = 0<br>Maximum value = 4094</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD]()| [UPDATE](#u)| [UNSET](#)| [DELETE](#d)| [RENAME](#r)| [GET (ALL)](#get-)| [GET]()| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lbgroup
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"lbgroup":{<b>"name":<String_value>,</b>"persistencetype":<String_value>,"persistencebackup":<String_value>,"backuppersistencetimeout":<Double_value>,"persistmask":<String_value>,"cookiename":<String_value>,"v6persistmasklen":<Double_value>,"cookiedomain":<String_value>,"timeout":<Double_value>,"rule":<String_value>,"usevserverpersistency":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lbgroup
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"lbgroup":{<b>"name":<String_value>,</b>"persistencetype":<String_value>,"persistencebackup":<String_value>,"backuppersistencetimeout":<Double_value>,"persistmask":<String_value>,"cookiename":<String_value>,"v6persistmasklen":<Double_value>,"cookiedomain":<String_value>,"timeout":<Double_value>,"rule":<String_value>,"usevserverpersistency":<String_value>,"mastervserver":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lbgroup?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"lbgroup":{<b>"name":<String_value>,</b>"persistencetype":true,"persistencebackup":true,"backuppersistencetimeout":true,"persistmask":true,"cookiename":true,"v6persistmasklen":true,"cookiedomain":true,"timeout":true,"rule":true,"usevserverpersistency":true,"mastervserver":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lbgroup/name_value&lt;String&gt;
<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###rename



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lbgroup?<b>action=rename</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"lbgroup":{<b>"name":<String_value>,</b><b>"newname":<String_value></b>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lbgroup
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lbgroup?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lbgroup?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of lbgroup resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lbgroup?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lbgroup?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the lbgroup resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "lbgroup": [ {"name":<String_value>,"persistencetype":<String_value>,"persistencebackup":<String_value>,"backuppersistencetimeout":<Double_value>,"persistmask":<String_value>,"v6persistmasklen":<Double_value>,"cookiename":<String_value>,"cookiedomain":<String_value>,"timeout":<Double_value>,"rule":<String_value>,"td":<Double_value>,"usevserverpersistency":<String_value>,"mastervserver":<String_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lbgroup/name_value&lt;String&gt;
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lbgroup/name_value&lt;String&gt;?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lbgroup/name_value&lt;String&gt;?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "lbgroup": [ {"name":<String_value>,"persistencetype":<String_value>,"persistencebackup":<String_value>,"backuppersistencetimeout":<Double_value>,"persistmask":<String_value>,"v6persistmasklen":<Double_value>,"cookiename":<String_value>,"cookiedomain":<String_value>,"timeout":<Double_value>,"rule":<String_value>,"td":<Double_value>,"usevserverpersistency":<String_value>,"mastervserver":<String_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lbgroup?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "lbgroup": [ { "__count": "#no"} ] }```



