#vrid6_binding

Binding object which returns the resources bound to vrid6.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>&lt;Double></td><td>Read-write</td><td>Integer value that uniquely identifies a VMAC6 address.<br>Minimum value = 1<br>Maximum value = 255</td></tr><tr><td>vrid6_interface_binding</td><td>&lt;vrid6_interface_binding[]></td><td>Read-only</td><td>interface that can be bound to vrid6.</td></tr><tr><td>vrid6_trackinterface_binding</td><td>&lt;vrid6_trackinterface_binding[]></td><td>Read-only</td><td>trackinterface that can be bound to vrid6.</td></tr><tr><td>vrid6_channel_binding</td><td>&lt;vrid6_channel_binding[]></td><td>Read-only</td><td>channel that can be bound to vrid6.</td></tr><tr><td>vrid6_nsip_binding</td><td>&lt;vrid6_nsip_binding[]></td><td>Read-only</td><td>nsip that can be bound to vrid6.</td></tr><tr><td>vrid6_nsip6_binding</td><td>&lt;vrid6_nsip6_binding[]></td><td>Read-only</td><td>nsip6 that can be bound to vrid6.</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[GET]()| [GET (ALL)](#get-)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vrid6_binding/id_value&lt;Double&gt;
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "vrid6_binding": [ {"id":<Double_value>,"vrid6_nsip6_binding":<vrid6_nsip6_binding[]_value>,"vrid6_nsip_binding":<vrid6_nsip_binding[]_value>,"vrid6_channel_binding":<vrid6_channel_binding[]_value>,"vrid6_interface_binding":<vrid6_interface_binding[]_value>,"vrid6_trackinterface_binding":<vrid6_trackinterface_binding[]_value>}]}```



###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vrid6_binding
<b>Query-parameters:</b>
<b>bulkbindings</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vrid6_binding?<b>bulkbindings=yes</b>
NITRO allows you to fetch bindings in bulk.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "vrid6_binding": [ {"id":<Double_value>,"vrid6_nsip6_binding":<vrid6_nsip6_binding[]_value>,"vrid6_nsip_binding":<vrid6_nsip_binding[]_value>,"vrid6_channel_binding":<vrid6_channel_binding[]_value>,"vrid6_interface_binding":<vrid6_interface_binding[]_value>,"vrid6_trackinterface_binding":<vrid6_trackinterface_binding[]_value>}]}```



