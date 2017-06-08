#lbparameter

Configuration for LB parameter resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>httponlycookieflag</td><td>&lt;String></td><td>Read-write</td><td>Include the HttpOnly attribute in persistence cookies. The HttpOnly attribute limits the scope of a cookie to HTTP requests and helps mitigate the risk of cross-site scripting attacks.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>usesecuredpersistencecookie</td><td>&lt;String></td><td>Read-write</td><td>Encode persistence cookie values using SHA2 hash.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>cookiepassphrase</td><td>&lt;String></td><td>Read-write</td><td>Use this parameter to specify the passphrase used to generate secured persistence cookie value. It specifies the passphrase with a maximum of 31 characters.</td><tr><tr><td>consolidatedlconn</td><td>&lt;String></td><td>Read-write</td><td>To find the service with the fewest connections, the virtual server uses the consolidated connection statistics from all the packet engines. The NO setting allows consideration of only the number of connections on the packet engine that received the new connection.&lt;br>Default value: YES&lt;br>Possible values = YES, NO</td><tr><tr><td>useportforhashlb</td><td>&lt;String></td><td>Read-write</td><td>Include the port number of the service when creating a hash for hash based load balancing methods. With the NO setting, only the IP address of the service is considered when creating a hash.&lt;br>Default value: YES&lt;br>Possible values = YES, NO</td><tr><tr><td>preferdirectroute</td><td>&lt;String></td><td>Read-write</td><td>Perform route lookup for traffic received by the NetScaler appliance, and forward the traffic according to configured routes. Do not set this parameter if you want a wildcard virtual server to direct packets received by the appliance to an intermediary device, such as a firewall, even if their destination is directly connected to the appliance. Route lookup is performed after the packets have been processed and returned by the intermediary device.&lt;br>Default value: YES&lt;br>Possible values = YES, NO</td><tr><tr><td>startuprrfactor</td><td>&lt;Double></td><td>Read-write</td><td>Number of requests, per service, for which to apply the round robin load balancing method before switching to the configured load balancing method, thus allowing services to ramp up gradually to full load. Until the specified number of requests is distributed, the NetScaler appliance is said to be implementing the slow start mode (or startup round robin). Implemented for a virtual server when one of the following is true: * The virtual server is newly created. * One or more services are newly bound to the virtual server. * One or more services bound to the virtual server are enabled. * The load balancing method is changed. This parameter applies to all the load balancing virtual servers configured on the NetScaler appliance, except for those virtual servers for which the virtual server-level slow start parameters (New Service Startup Request Rate and Increment Interval) are configured. If the global slow start parameter and the slow start parameters for a given virtual server are not set, the appliance implements a default slow start for the virtual server, as follows: * For a newly configured virtual server, the appliance implements slow start for the first 100 requests received by the virtual server. * For an existing virtual server, if one or more services are newly bound or newly enabled, or if the load balancing method is changed, the appliance dynamically computes the number of requests for which to implement startup round robin. It obtains this number by multiplying the request rate by the number of bound services (it includes services that are marked as DOWN). For example, if the current request rate is 20 requests/s and ten services are bound to the virtual server, the appliance performs startup round robin for 200 requests. Not applicable to a virtual server for which a hash based load balancing method is configured.</td><tr><tr><td>monitorskipmaxclient</td><td>&lt;String></td><td>Read-write</td><td>When a monitor initiates a connection to a service, do not check to determine whether the number of connections to the service has reached the limit specified by the services Max Clients setting. Enables monitoring to continue even if the service has reached its connection limit.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>monitorconnectionclose</td><td>&lt;String></td><td>Read-write</td><td>Close monitoring connections by sending the service a connection termination message with the specified bit set.&lt;br>Default value: FIN&lt;br>Possible values = RESET, FIN</td><tr><tr><td>vserverspecificmac</td><td>&lt;String></td><td>Read-write</td><td>Allow a MAC-mode virtual server to accept traffic returned by an intermediary device, such as a firewall, to which the traffic was previously forwarded by another MAC-mode virtual server. The second virtual server can then distribute that traffic across the destination server farm. Also useful when load balancing Branch Repeater appliances. Note: The second virtual server can also send the traffic to another set of intermediary devices, such as another set of firewalls. If necessary, you can configure multiple MAC-mode virtual servers to pass traffic successively through multiple sets of intermediary devices.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>sessionsthreshold</td><td>&lt;Double></td><td>Read-only</td><td>This option is used to get the upper-limit on the number of persistent sessions set by the administrator for this system.&lt;br>Minimum value = 1</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[UPDATE](#update) | [UNSET](#unset) | [GET (ALL)](#get-(all))


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","lbparameter":{      "httponlycookieflag":<String_value>,      "usesecuredpersistencecookie":<String_value>,      "cookiepassphrase":<String_value>,      "consolidatedlconn":<String_value>,      "useportforhashlb":<String_value>,      "preferdirectroute":<String_value>,      "startuprrfactor":<Double_value>,      "monitorskipmaxclient":<String_value>,      "monitorconnectionclose":<String_value>,      "vserverspecificmac":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","lbparameter":{      "httponlycookieflag":true,      "usesecuredpersistencecookie":true,      "cookiepassphrase":true,      "consolidatedlconn":true,      "useportforhashlb":true,      "preferdirectroute":true,      "startuprrfactor":true,      "monitorskipmaxclient":true,      "monitorconnectionclose":true,      "vserverspecificmac":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/lbparameter
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "lbparameter": [ {      "httponlycookieflag":<String_value>,      "usesecuredpersistencecookie":<String_value>,      "cookiepassphrase":<String_value>,      "consolidatedlconn":<String_value>,      "useportforhashlb":<String_value>,      "preferdirectroute":<String_value>,      "startuprrfactor":<Double_value>,      "monitorskipmaxclient":<String_value>,      "monitorconnectionclose":<String_value>,      "vserverspecificmac":<String_value>,      "sessionsthreshold":<Double_value>}]}```



