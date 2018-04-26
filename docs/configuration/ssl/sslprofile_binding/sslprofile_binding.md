#sslprofile_binding

Binding object which returns the resources bound to sslprofile.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name of the SSL profile for which to show detailed information.<br>Minimum length = 1<br>Maximum length = 127</td></tr><tr><td>sslprofile_sslcipher_binding</td><td>&lt;sslprofile_sslcipher_binding[]></td><td>Read-only</td><td>sslcipher that can be bound to sslprofile.</td></tr><tr><td>sslprofile_ecccurve_binding</td><td>&lt;sslprofile_ecccurve_binding[]></td><td>Read-only</td><td>ecccurve that can be bound to sslprofile.</td></tr><tr><td>sslprofile_sslvserver_binding</td><td>&lt;sslprofile_sslvserver_binding[]></td><td>Read-only</td><td>sslvserver that can be bound to sslprofile.</td></tr><tr><td>sslprofile_sslciphersuite_binding</td><td>&lt;sslprofile_sslciphersuite_binding[]></td><td>Read-only</td><td>sslciphersuite that can be bound to sslprofile.</td></tr><tr><td>sslprofile_sslcertkey_binding</td><td>&lt;sslprofile_sslcertkey_binding[]></td><td>Read-only</td><td>sslcertkey that can be bound to sslprofile.</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[GET]()| [GET (ALL)](#get-)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslprofile_binding/name_value&lt;String&gt;
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "sslprofile_binding": [ {"name":<String_value>,"sslprofile_ecccurve_binding":<sslprofile_ecccurve_binding[]_value>,"sslprofile_sslcertkey_binding":<sslprofile_sslcertkey_binding[]_value>,"sslprofile_sslciphersuite_binding":<sslprofile_sslciphersuite_binding[]_value>,"sslprofile_sslvserver_binding":<sslprofile_sslvserver_binding[]_value>,"sslprofile_sslcipher_binding":<sslprofile_sslcipher_binding[]_value>}]}```



###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslprofile_binding
<b>Query-parameters:</b>
<b>bulkbindings</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslprofile_binding?<b>bulkbindings=yes</b>
NITRO allows you to fetch bindings in bulk.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "sslprofile_binding": [ {"name":<String_value>,"sslprofile_ecccurve_binding":<sslprofile_ecccurve_binding[]_value>,"sslprofile_sslcertkey_binding":<sslprofile_sslcertkey_binding[]_value>,"sslprofile_sslciphersuite_binding":<sslprofile_sslciphersuite_binding[]_value>,"sslprofile_sslvserver_binding":<sslprofile_sslvserver_binding[]_value>,"sslprofile_sslcipher_binding":<sslprofile_sslcipher_binding[]_value>}]}```



