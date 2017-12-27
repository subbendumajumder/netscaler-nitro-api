#vpnalwaysonprofile

Configuration for AlwyasON profile resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>name of AlwaysON profile.&lt;br>Minimum length = 1</td><tr><tr><td>networkaccessonvpnfailure</td><td>&lt;String></td><td>Read-write</td><td>Option to block network traffic when tunnel is not established(and the config requires that tunnel be established). When set to onlyToGateway, the network traffic to and from the client (except Gateway IP) is blocked. When set to fullAccess, the network traffic is not blocked.&lt;br>Default value: fullAccess,&lt;br>Possible values = onlyToGateway, fullAccess</td><tr><tr><td>clientcontrol</td><td>&lt;String></td><td>Read-write</td><td>Allow/Deny user to log off and connect to another Gateway.&lt;br>Default value: DENY&lt;br>Possible values = ALLOW, DENY</td><tr><tr><td>locationbasedvpn</td><td>&lt;String></td><td>Read-write</td><td>Option to decide if tunnel should be established when in enterprise network. When locationBasedVPN is remote, client tries to detect if it is located in enterprise network or not and establishes the tunnel if not in enterprise network. Dns suffixes configured using -add dns suffix- are used to decide if the client is in the enterprise network or not. If the resolution of the DNS suffix results in private IP, client is said to be in enterprise network. When set to EveryWhere, the client skips the check to detect if it is on the enterprise network and tries to establish the tunnel.&lt;br>Default value: Remote&lt;br>Possible values = Remote, Everywhere</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [DELETE](#delete) | [UPDATE](#update) | [UNSET](#unset) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnalwaysonprofile
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Request Payload: 
Response:
HTTP Status Code on Success: 201 Created


###delete



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnalwaysonprofile/name_value&lt;String&gt;
HTTP Method: DELETE
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Response:
HTTP Status Code on Success: 200 OK


###update



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnalwaysonprofile
HTTP Method: PUT
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Request Payload: 
Response:
HTTP Status Code on Success: 200 OK


###unset



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnalwaysonprofile?action=unset
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Request Payload: 
Response:
HTTP Status Code on Success: 200 OK


###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnalwaysonprofile
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnalwaysonprofile?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


filter
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnalwaysonprofile?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of vpnalwaysonprofile resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnalwaysonprofile?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).


pagination
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnalwaysonprofile?pagesize=#no;pageno=#no
Use this query-parameter to get the vpnalwaysonprofile resources in chunks.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Response:
HTTP Status Code on Success: 200 OK

Content-Type:application/json

Response Payload: 



###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnalwaysonprofile/name_value&lt;String&gt;
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnalwaysonprofile/name_value&lt;String&gt;?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnalwaysonprofile/name_value&lt;String&gt;?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Response:
HTTP Status Code on Success: 200 OK

Content-Type:application/json

Response Payload: 



###count



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnalwaysonprofile?count=yes
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Response:
HTTP Status Code on Success: 200 OK

Content-Type:application/json

Response Payload: 


