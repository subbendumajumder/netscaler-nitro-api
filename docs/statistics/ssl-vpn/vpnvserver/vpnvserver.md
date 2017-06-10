#vpnvserver

Statistics for VPN virtual server resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name of the virtual server for which to show detailed statistics.&lt;br>Minimum length = 1</td><tr><tr><td>clearstats</td><td>&lt;String></td><td>Read-write</td><td>Clear the statsistics / counters.&lt;br>Possible values = basic, full</td><tr><tr><td>primaryipaddress</td><td>&lt;String></td><td>Read-only</td><td>The IP address on which the service is running.</td><tr><tr><td>primaryport</td><td>&lt;Integer></td><td>Read-only</td><td>The port on which the service is running.</td><tr><tr><td>type</td><td>&lt;String></td><td>Read-only</td><td>Protocol associated with the vserver</td><tr><tr><td>state</td><td>&lt;String></td><td>Read-only</td><td>Current state of the server. Possible values are UP, DOWN, UNKNOWN, OFS(Out of Service), TROFS(Transition Out of Service), TROFS_DOWN(Down When going Out of Service)</td><tr><tr><td>totalrequests</td><td>&lt;Double></td><td>Read-only</td><td>Total number of requests received on this service or virtual server. (This applies to HTTP/SSL services and servers.)</td><tr><tr><td>requestsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for totalrequests</td><tr><tr><td>totalresponses</td><td>&lt;Double></td><td>Read-only</td><td>Number of responses received on this service or virtual server. (This applies to HTTP/SSL services and servers.)</td><tr><tr><td>responsesrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for totalresponses</td><tr><tr><td>totalrequestbytes</td><td>&lt;Double></td><td>Read-only</td><td>Total number of request bytes received on this service or virtual server.</td><tr><tr><td>requestbytesrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for totalrequestbytes</td><tr><tr><td>totalresponsebytes</td><td>&lt;Double></td><td>Read-only</td><td>Number of response bytes received by this service or virtual server.</td><tr><tr><td>responsebytesrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for totalresponsebytes</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[GET (ALL)](#get-(all)) | [GET](#get)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/vpnvserver
Query-parameters:
args
http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/vpnvserver?args=name:&lt;String_value&gt;,detail:&lt;Boolean_value&gt;,fullvalues:&lt;Boolean_value&gt;,ntimes:&lt;Double_value&gt;,logfile:&lt;String_value&gt;,clearstats:&lt;String_value&gt;
Use this query-parameter to get vpnvserver resources based on additional properties.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "vpnvserver": [ {      "name":<String_value>,      "totalrequests":<Double_value>,      "responsebytesrate":<Double_value>,      "totalresponses":<Double_value>,      "requestbytesrate":<Double_value>,      "type":<String_value>,      "primaryipaddress":<String_value>,      "responsesrate":<Double_value>,      "totalrequestbytes":<Double_value>,      "state":<String_value>,      "totalresponsebytes":<Double_value>,      "primaryport":<Integer_value>,      "requestsrate":<Double_value>}]}```



###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/vpnvserver/name_value&gt;&lt;String&gt;
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "vpnvserver": [ {      "name":<String_value>,      "totalrequests":<Double_value>,      "responsebytesrate":<Double_value>,      "totalresponses":<Double_value>,      "requestbytesrate":<Double_value>,      "type":<String_value>,      "primaryipaddress":<String_value>,      "responsesrate":<Double_value>,      "totalrequestbytes":<Double_value>,      "state":<String_value>,      "totalresponsebytes":<Double_value>,      "primaryport":<Integer_value>,      "requestsrate":<Double_value>}]}```



