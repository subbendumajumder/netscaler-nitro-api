#aaakcdaccount

Configuration for Kerberos constrained delegation account resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>kcdaccount</td><td>&lt;String></td><td>Read-write</td><td>The name of the KCD account.<br>Minimum length = 1</td></tr><tr><td>keytab</td><td>&lt;String></td><td>Read-write</td><td>The path to the keytab file. If specified other parameters in this command need not be given.</td></tr><tr><td>realmstr</td><td>&lt;String></td><td>Read-write</td><td>Kerberos Realm.</td></tr><tr><td>delegateduser</td><td>&lt;String></td><td>Read-write</td><td>Username that can perform kerberos constrained delegation.</td></tr><tr><td>kcdpassword</td><td>&lt;String></td><td>Read-write</td><td>Password for Delegated User.</td></tr><tr><td>usercert</td><td>&lt;String></td><td>Read-write</td><td>SSL Cert (including private key) for Delegated User.</td></tr><tr><td>cacert</td><td>&lt;String></td><td>Read-write</td><td>CA Cert for UserCert or when doing PKINIT backchannel.</td></tr><tr><td>userrealm</td><td>&lt;String></td><td>Read-write</td><td>Realm of the user.</td></tr><tr><td>enterpriserealm</td><td>&lt;String></td><td>Read-write</td><td>Enterprise Realm of the user. This should be given only in certain KDC deployments where KDC expects Enterprise username instead of Principal Name.</td></tr><tr><td>servicespn</td><td>&lt;String></td><td>Read-write</td><td>Service SPN. When specified, this will be used to fetch kerberos tickets. If not specified, Netscaler will construct SPN using service fqdn.</td></tr><tr><td>principle</td><td>&lt;String></td><td>Read-only</td><td>SPN extracted from keytab file.</td></tr><tr><td>kcdspn</td><td>&lt;String></td><td>Read-only</td><td>Host SPN extracted from keytab file.</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD]()| [DELETE](#d)| [UPDATE](#u)| [UNSET](#)| [GET (ALL)](#get-)| [GET]()| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/aaakcdaccount
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"aaakcdaccount":{<b>"kcdaccount":<String_value>,</b>"keytab":<String_value>,"realmstr":<String_value>,"delegateduser":<String_value>,"kcdpassword":<String_value>,"usercert":<String_value>,"cacert":<String_value>,"userrealm":<String_value>,"enterpriserealm":<String_value>,"servicespn":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/aaakcdaccount/kcdaccount_value&lt;String&gt;
<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/aaakcdaccount
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"aaakcdaccount":{<b>"kcdaccount":<String_value>,</b>"keytab":<String_value>,"realmstr":<String_value>,"delegateduser":<String_value>,"kcdpassword":<String_value>,"usercert":<String_value>,"cacert":<String_value>,"userrealm":<String_value>,"enterpriserealm":<String_value>,"servicespn":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/aaakcdaccount?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"aaakcdaccount":{<b>"kcdaccount":<String_value>,</b>"keytab":true,"usercert":true,"cacert":true,"userrealm":true,"enterpriserealm":true,"servicespn":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/aaakcdaccount
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/aaakcdaccount?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/aaakcdaccount?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of aaakcdaccount resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/aaakcdaccount?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/aaakcdaccount?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the aaakcdaccount resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "aaakcdaccount": [ {"kcdaccount":<String_value>,"keytab":<String_value>,"principle":<String_value>,"kcdspn":<String_value>,"realmstr":<String_value>,"delegateduser":<String_value>,"kcdpassword":<String_value>,"usercert":<String_value>,"cacert":<String_value>,"userrealm":<String_value>,"enterpriserealm":<String_value>,"servicespn":<String_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/aaakcdaccount/kcdaccount_value&lt;String&gt;
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/aaakcdaccount/kcdaccount_value&lt;String&gt;?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/aaakcdaccount/kcdaccount_value&lt;String&gt;?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "aaakcdaccount": [ {"kcdaccount":<String_value>,"keytab":<String_value>,"principle":<String_value>,"kcdspn":<String_value>,"realmstr":<String_value>,"delegateduser":<String_value>,"kcdpassword":<String_value>,"usercert":<String_value>,"cacert":<String_value>,"userrealm":<String_value>,"enterpriserealm":<String_value>,"servicespn":<String_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/aaakcdaccount?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "aaakcdaccount": [ { "__count": "#no"} ] }```



