#nscapacity

Configuration for capacity resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>bandwidth</td><td>&lt;Double></td><td>Read-write</td><td>System bandwidth limit.</td><tr><tr><td>edition</td><td>&lt;String></td><td>Read-write</td><td>Product edition.&lt;br>Possible values = Standard, Enterprise, Platinum</td><tr><tr><td>unit</td><td>&lt;String></td><td>Read-write</td><td>Bandwidth unit.&lt;br>Possible values = Gbps, Mbps</td><tr><tr><td>actualbandwidth</td><td>&lt;Double></td><td>Read-only</td><td>Bandwith in MBPS.</td><tr><tr><td>maxbandwidth</td><td>&lt;Double></td><td>Read-only</td><td>Maximum Bandwidth.</td><tr><tr><td>minbandwidth</td><td>&lt;Double></td><td>Read-only</td><td>Minimum Bandwidth.</td><tr><tr><td>instancecount</td><td>&lt;Double></td><td>Read-only</td><td>VPX will consume one instance and MPX will consume zero instance.</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[UPDATE](#update) | [UNSET](#unset) | [GET (ALL)](#get-(all))


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###update



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nscapacity
HTTP Method: PUT
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Request Payload: 
Response:
HTTP Status Code on Success: 200 OK


###unset



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nscapacity?action=unset
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Request Payload: 
Response:
HTTP Status Code on Success: 200 OK


###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nscapacity
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Response:
HTTP Status Code on Success: 200 OK

Content-Type:application/json

Response Payload: 


