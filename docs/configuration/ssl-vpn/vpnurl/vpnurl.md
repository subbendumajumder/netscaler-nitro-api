#vpnurl

Configuration for VPN URL resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>urlname</td><td>&lt;String></td><td>Read-write</td><td>Name of the bookmark link.&lt;br>Minimum length = 1</td><tr><tr><td>linkname</td><td>&lt;String></td><td>Read-write</td><td>Description of the bookmark link. The description appears in the Access Interface.&lt;br>Minimum length = 1</td><tr><tr><td>actualurl</td><td>&lt;String></td><td>Read-write</td><td>Web address for the bookmark link.&lt;br>Minimum length = 1</td><tr><tr><td>vservername</td><td>&lt;String></td><td>Read-write</td><td>Name of the associated LB/CS vserver.</td><tr><tr><td>clientlessaccess</td><td>&lt;String></td><td>Read-write</td><td>If clientless access to the resource hosting the link is allowed, also use clientless access for the bookmarked web address in the Secure Client Access based session. Allows single sign-on and other HTTP processing on NetScaler Gateway for HTTPS resources.&lt;br>Default value: OFF&lt;br>Possible values = ON, OFF</td><tr><tr><td>comment</td><td>&lt;String></td><td>Read-write</td><td>Any comments associated with the bookmark link.</td><tr><tr><td>iconurl</td><td>&lt;String></td><td>Read-write</td><td>URL to fetch icon file for displaying this resource.</td><tr><tr><td>ssotype</td><td>&lt;String></td><td>Read-write</td><td>Single sign on type for unified gateway.&lt;br>Possible values = unifiedgateway, selfauth, samlauth</td><tr><tr><td>applicationtype</td><td>&lt;String></td><td>Read-write</td><td>The type of application this VPN URL represents. Possible values are CVPN/SaaS/VPN.&lt;br>Possible values = CVPN, VPN, SaaS</td><tr><tr><td>samlssoprofile</td><td>&lt;String></td><td>Read-write</td><td>Profile to be used for doing SAML SSO.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [DELETE](#delete) | [UPDATE](#update) | [UNSET](#unset) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnurl
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"vpnurl":{      "urlname":<String_value>,      "linkname":<String_value>,      "actualurl":<String_value>,      "vservername":<String_value>,      "clientlessaccess":<String_value>,      "comment":<String_value>,      "iconurl":<String_value>,      "ssotype":<String_value>,      "applicationtype":<String_value>,      "samlssoprofile":<String_value>}}```
Response:
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnurl/urlname_value&lt;String&gt;
HTTP Method: DELETE
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnurl
HTTP Method: PUT
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"vpnurl":{      "urlname":<String_value>,      "linkname":<String_value>,      "actualurl":<String_value>,      "vservername":<String_value>,      "clientlessaccess":<String_value>,      "comment":<String_value>,      "iconurl":<String_value>,      "ssotype":<String_value>,      "applicationtype":<String_value>,      "samlssoprofile":<String_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnurl?action=unset
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"vpnurl":{      "urlname":<String_value>,      "vservername":true,      "clientlessaccess":true,      "comment":true,      "iconurl":true,      "ssotype":true,      "applicationtype":true,      "samlssoprofile":true}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnurl
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnurl?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


filter
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnurl?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of vpnurl resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnurl?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).


pagination
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnurl?pagesize=#no;pageno=#no
Use this query-parameter to get the vpnurl resources in chunks.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "vpnurl": [ {      "urlname":<String_value>,      "linkname":<String_value>,      "vservername":<String_value>,      "actualurl":<String_value>,      "clientlessaccess":<String_value>,      "comment":<String_value>,      "iconurl":<String_value>,      "ssotype":<String_value>,      "applicationtype":<String_value>,      "samlssoprofile":<String_value>}]}```



###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnurl/urlname_value&lt;String&gt;
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnurl/urlname_value&lt;String&gt;?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnurl/urlname_value&lt;String&gt;?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "vpnurl": [ {      "urlname":<String_value>,      "linkname":<String_value>,      "vservername":<String_value>,      "actualurl":<String_value>,      "clientlessaccess":<String_value>,      "comment":<String_value>,      "iconurl":<String_value>,      "ssotype":<String_value>,      "applicationtype":<String_value>,      "samlssoprofile":<String_value>}]}```



###count



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnurl?count=yes
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: 
{ "vpnurl": [ { "__count": "#no"} ] }


