#gslbservice

Configuration for GSLB service resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>servicename</td><td>&lt;String></td><td>Read-write</td><td>Name for the GSLB service. Must begin with an ASCII alphanumeric or underscore (_) character, and must contain only ASCII alphanumeric, underscore, hash (#), period (.), space, colon (:), at (@), equals (=), and hyphen (-) characters. Can be changed after the GSLB service is created. CLI Users: If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my gslbsvc" or my gslbsvc).&lt;br>Minimum length = 1</td><tr><tr><td>cnameentry</td><td>&lt;String></td><td>Read-write</td><td>Canonical name of the GSLB service. Used in CNAME-based GSLB.&lt;br>Minimum length = 1</td><tr><tr><td>ip</td><td>&lt;String></td><td>Read-write</td><td>IP address for the GSLB service. Should represent a load balancing, content switching, or VPN virtual server on the NetScaler appliance, or the IP address of another load balancing device.&lt;br>Minimum length = 1</td><tr><tr><td>servername</td><td>&lt;String></td><td>Read-write</td><td>Name of the server hosting the GSLB service.&lt;br>Minimum length = 1</td><tr><tr><td>servicetype</td><td>&lt;String></td><td>Read-write</td><td>Type of service to create.&lt;br>Default value: NSSVC_SERVICE_UNKNOWN&lt;br>Possible values = HTTP, FTP, TCP, UDP, SSL, SSL_BRIDGE, SSL_TCP, NNTP, ANY, SIP_UDP, RADIUS, RDP, RTSP, MYSQL, MSSQL, ORACLE</td><tr><tr><td>port</td><td>&lt;Integer></td><td>Read-write</td><td>Port on which the load balancing entity represented by this GSLB service listens.&lt;br>Minimum value = 1&lt;br>Range 1 - 65535</td><tr><tr><td>publicip</td><td>&lt;String></td><td>Read-write</td><td>The public IP address that a NAT device translates to the GSLB services private IP address. Optional.</td><tr><tr><td>publicport</td><td>&lt;Integer></td><td>Read-write</td><td>The public port associated with the GSLB services public IP address. The port is mapped to the services private port number. Applicable to the local GSLB service. Optional.</td><tr><tr><td>maxclient</td><td>&lt;Double></td><td>Read-write</td><td>The maximum number of open connections that the service can support at any given time. A GSLB service whose connection count reaches the maximum is not considered when a GSLB decision is made, until the connection count drops below the maximum.&lt;br>Minimum value = 0&lt;br>Maximum value = 4294967294</td><tr><tr><td>healthmonitor</td><td>&lt;String></td><td>Read-write</td><td>Monitor the health of the GSLB service.&lt;br>Default value: YES&lt;br>Possible values = YES, NO</td><tr><tr><td>sitename</td><td>&lt;String></td><td>Read-write</td><td>Name of the GSLB site to which the service belongs.&lt;br>Minimum length = 1</td><tr><tr><td>state</td><td>&lt;String></td><td>Read-write</td><td>Enable or disable the service.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>cip</td><td>&lt;String></td><td>Read-write</td><td>In the request that is forwarded to the GSLB service, insert a header that stores the clients IP address. Client IP header insertion is used in connection-proxy based site persistence.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>cipheader</td><td>&lt;String></td><td>Read-write</td><td>Name for the HTTP header that stores the clients IP address. Used with the Client IP option. If client IP header insertion is enabled on the service and a name is not specified for the header, the NetScaler appliance uses the name specified by the cipHeader parameter in the set ns param command or, in the GUI, the Client IP Header parameter in the Configure HTTP Parameters dialog box.&lt;br>Minimum length = 1</td><tr><tr><td>sitepersistence</td><td>&lt;String></td><td>Read-write</td><td>Use cookie-based site persistence. Applicable only to HTTP and SSL GSLB services.&lt;br>Possible values = ConnectionProxy, HTTPRedirect, NONE</td><tr><tr><td>cookietimeout</td><td>&lt;Double></td><td>Read-write</td><td>Timeout value, in minutes, for the cookie, when cookie based site persistence is enabled.&lt;br>Minimum value = 0&lt;br>Maximum value = 1440</td><tr><tr><td>siteprefix</td><td>&lt;String></td><td>Read-write</td><td>The sites prefix string. When the service is bound to a GSLB virtual server, a GSLB site domain is generated internally for each bound service-domain pair by concatenating the site prefix of the service and the name of the domain. If the special string NONE is specified, the site-prefix string is unset. When implementing HTTP redirect site persistence, the NetScaler appliance redirects GSLB requests to GSLB services by using their site domains.</td><tr><tr><td>clttimeout</td><td>&lt;Double></td><td>Read-write</td><td>Idle time, in seconds, after which a client connection is terminated. Applicable if connection proxy based site persistence is used.&lt;br>Minimum value = 0&lt;br>Maximum value = 31536000</td><tr><tr><td>svrtimeout</td><td>&lt;Double></td><td>Read-write</td><td>Idle time, in seconds, after which a server connection is terminated. Applicable if connection proxy based site persistence is used.&lt;br>Minimum value = 0&lt;br>Maximum value = 31536000</td><tr><tr><td>maxbandwidth</td><td>&lt;Double></td><td>Read-write</td><td>Integer specifying the maximum bandwidth allowed for the service. A GSLB service whose bandwidth reaches the maximum is not considered when a GSLB decision is made, until its bandwidth consumption drops below the maximum.</td><tr><tr><td>downstateflush</td><td>&lt;String></td><td>Read-write</td><td>Flush all active transactions associated with the GSLB service when its state transitions from UP to DOWN. Do not enable this option for services that must complete their transactions. Applicable if connection proxy based site persistence is used.&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>maxaaausers</td><td>&lt;Double></td><td>Read-write</td><td>Maximum number of SSL VPN users that can be logged on concurrently to the VPN virtual server that is represented by this GSLB service. A GSLB service whose user count reaches the maximum is not considered when a GSLB decision is made, until the count drops below the maximum.&lt;br>Minimum value = 0&lt;br>Maximum value = 65535</td><tr><tr><td>monthreshold</td><td>&lt;Double></td><td>Read-write</td><td>Monitoring threshold value for the GSLB service. If the sum of the weights of the monitors that are bound to this GSLB service and are in the UP state is not equal to or greater than this threshold value, the service is marked as DOWN.&lt;br>Minimum value = 0&lt;br>Maximum value = 65535</td><tr><tr><td>hashid</td><td>&lt;Double></td><td>Read-write</td><td>Unique hash identifier for the GSLB service, used by hash based load balancing methods.&lt;br>Minimum value = 1</td><tr><tr><td>comment</td><td>&lt;String></td><td>Read-write</td><td>Any comments that you might want to associate with the GSLB service.</td><tr><tr><td>appflowlog</td><td>&lt;String></td><td>Read-write</td><td>Enable logging appflow flow information.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>ipaddress</td><td>&lt;String></td><td>Read-write</td><td>The new IP address of the service.</td><tr><tr><td>viewname</td><td>&lt;String></td><td>Read-write</td><td>Name of the DNS view of the service. A DNS view is used in global server load balancing (GSLB) to return a predetermined IP address to a specific group of clients, which are identified by using a DNS policy.&lt;br>Minimum length = 1</td><tr><tr><td>viewip</td><td>&lt;String></td><td>Read-write</td><td>IP address to be used for the given view.</td><tr><tr><td>weight</td><td>&lt;Double></td><td>Read-write</td><td>Weight to assign to the monitor-service binding. A larger number specifies a greater weight. Contributes to the monitoring threshold, which determines the state of the service.&lt;br>Minimum value = 1&lt;br>Maximum value = 100</td><tr><tr><td>monitor_name_svc</td><td>&lt;String></td><td>Read-write</td><td>Name of the monitor to bind to the service.&lt;br>Minimum length = 1</td><tr><tr><td>newname</td><td>&lt;String></td><td>Read-write</td><td>New name for the GSLB service.&lt;br>Minimum length = 1</td><tr><tr><td>gslb</td><td>&lt;String></td><td>Read-only</td><td>.&lt;br>Default value: GSLB&lt;br>Possible values = REMOTE, LOCAL</td><tr><tr><td>svrstate</td><td>&lt;String></td><td>Read-only</td><td>Server state.&lt;br>Possible values = UP, DOWN, UNKNOWN, BUSY, OUT OF SERVICE, GOING OUT OF SERVICE, DOWN WHEN GOING OUT OF SERVICE, NS_EMPTY_STR, Unknown, DISABLED</td><tr><tr><td>svreffgslbstate</td><td>&lt;String></td><td>Read-only</td><td>Effective state of the gslb svc.&lt;br>Possible values = UP, DOWN, UNKNOWN, BUSY, OUT OF SERVICE, GOING OUT OF SERVICE, DOWN WHEN GOING OUT OF SERVICE, NS_EMPTY_STR, Unknown, DISABLED</td><tr><tr><td>gslbthreshold</td><td>&lt;Integer></td><td>Read-only</td><td>Indicates if gslb svc has reached threshold.</td><tr><tr><td>gslbsvcstats</td><td>&lt;Integer></td><td>Read-only</td><td>Indicates if gslb svc has stats of the primary or the whole chain.</td><tr><tr><td>monstate</td><td>&lt;String></td><td>Read-only</td><td>State of the monitor bound to gslb service.&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>preferredlocation</td><td>&lt;String></td><td>Read-only</td><td>Prefered location.</td><tr><tr><td>monitor_state</td><td>&lt;String></td><td>Read-only</td><td>The running state of the monitor on this service.&lt;br>Possible values = UP, DOWN, UNKNOWN, BUSY, OUT OF SERVICE, GOING OUT OF SERVICE, DOWN WHEN GOING OUT OF SERVICE, NS_EMPTY_STR, Unknown, DISABLED</td><tr><tr><td>statechangetimesec</td><td>&lt;String></td><td>Read-only</td><td>Time when last state change happened. Seconds part.</td><tr><tr><td>tickssincelaststatechange</td><td>&lt;Double></td><td>Read-only</td><td>Time in 10 millisecond ticks since the last state change.</td><tr><tr><td>threshold</td><td>&lt;String></td><td>Read-only</td><td>.&lt;br>Possible values = ABOVE, BELOW</td><tr><tr><td>clmonowner</td><td>&lt;Double></td><td>Read-only</td><td>Tells the mon owner of the gslb service.&lt;br>Minimum value = 0&lt;br>Maximum value = 32</td><tr><tr><td>clmonview</td><td>&lt;Double></td><td>Read-only</td><td>Tells the view id of the monitoring owner.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [DELETE](#delete) | [UPDATE](#update) | [UNSET](#unset) | [RENAME](#rename) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>},"sessionid":"##sessionid","gslbservice":{      "servicename":<String_value>,      "cnameentry":<String_value>,      "ip":<String_value>,      "servername":<String_value>,      "servicetype":<String_value>,      "port":<Integer_value>,      "publicip":<String_value>,      "publicport":<Integer_value>,      "maxclient":<Double_value>,      "healthmonitor":<String_value>,      "sitename":<String_value>,      "state":<String_value>,      "cip":<String_value>,      "cipheader":<String_value>,      "sitepersistence":<String_value>,      "cookietimeout":<Double_value>,      "siteprefix":<String_value>,      "clttimeout":<Double_value>,      "svrtimeout":<Double_value>,      "maxbandwidth":<Double_value>,      "downstateflush":<String_value>,      "maxaaausers":<Double_value>,      "monthreshold":<Double_value>,      "hashid":<Double_value>,      "comment":<String_value>,      "appflowlog":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/gslbservice/servicename_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/gslbservice/servicename_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","gslbservice":{      "servicename":<String_value>,      "ipaddress":<String_value>,      "publicip":<String_value>,      "publicport":<Integer_value>,      "cip":<String_value>,                  "cipheader":<String_value>,      "sitepersistence":<String_value>,      "siteprefix":<String_value>,      "maxclient":<Double_value>,      "healthmonitor":<String_value>,      "maxbandwidth":<Double_value>,      "downstateflush":<String_value>,      "maxaaausers":<Double_value>,      "viewname":<String_value>,                  "viewip":<String_value>,      "monthreshold":<Double_value>,      "weight":<Double_value>,                  "monitor_name_svc":<String_value>,      "hashid":<Double_value>,      "comment":<String_value>,      "appflowlog":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","gslbservice":{      "servicename":<String_value>,      "publicip":true,      "publicport":true,      "cip":true,      "cipheader":true,      "sitepersistence":true,      "siteprefix":true,      "maxclient":true,      "healthmonitor":true,      "maxbandwidth":true,      "downstateflush":true,      "maxaaausers":true,      "monthreshold":true,      "hashid":true,      "comment":true,      "appflowlog":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###rename



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"rename"},"sessionid":"##sessionid","gslbservice":{      "servicename":<String_value>,      "newname":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/gslbservice
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/gslbservice?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of gslbservice resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/gslbservice?view=summary
Use this query-parameter to get the summary output of gslbservice resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/gslbservice?pagesize=#no;pageno=#no
Use this query-parameter to get the gslbservice resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/gslbservice?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "gslbservice": [ {      "servicename":<String_value>,      "gslb":<String_value>,      "ipaddress":<String_value>,      "ip":<String_value>,      "servername":<String_value>,      "servicetype":<String_value>,      "port":<Integer_value>,      "publicip":<String_value>,      "publicport":<Integer_value>,      "maxclient":<Double_value>,      "maxaaausers":<Double_value>,      "sitename":<String_value>,      "svrstate":<String_value>,      "svreffgslbstate":<String_value>,      "gslbthreshold":<Integer_value>,      "gslbsvcstats":<Integer_value>,      "state":<String_value>,      "monstate":<String_value>,      "cip":<String_value>,      "cipheader":<String_value>,      "sitepersistence":<String_value>,      "siteprefix":<String_value>,      "clttimeout":<Double_value>,      "svrtimeout":<Double_value>,      "preferredlocation":<String_value>,      "maxbandwidth":<Double_value>,      "downstateflush":<String_value>,      "cnameentry":<String_value>,      "viewname":<String_value>,      "viewip":<String_value>,      "weight":<Double_value>,      "monthreshold":<Double_value>,      "monitor_state":<String_value>,      "hashid":<Double_value>,      "comment":<String_value>,      "healthmonitor":<String_value>,      "appflowlog":<String_value>,      "statechangetimesec":<String_value>,      "tickssincelaststatechange":<Double_value>,      "threshold":<String_value>,      "clmonowner":<Double_value>,      "clmonview":<Double_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/gslbservice/servicename_value&lt;String&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "gslbservice": [ {      "servicename":<String_value>,      "gslb":<String_value>,      "ipaddress":<String_value>,      "ip":<String_value>,      "servername":<String_value>,      "servicetype":<String_value>,      "port":<Integer_value>,      "publicip":<String_value>,      "publicport":<Integer_value>,      "maxclient":<Double_value>,      "maxaaausers":<Double_value>,      "sitename":<String_value>,      "svrstate":<String_value>,      "svreffgslbstate":<String_value>,      "gslbthreshold":<Integer_value>,      "gslbsvcstats":<Integer_value>,      "state":<String_value>,      "monstate":<String_value>,      "cip":<String_value>,      "cipheader":<String_value>,      "sitepersistence":<String_value>,      "siteprefix":<String_value>,      "clttimeout":<Double_value>,      "svrtimeout":<Double_value>,      "preferredlocation":<String_value>,      "maxbandwidth":<Double_value>,      "downstateflush":<String_value>,      "cnameentry":<String_value>,      "viewname":<String_value>,      "viewip":<String_value>,      "weight":<Double_value>,      "monthreshold":<Double_value>,      "monitor_state":<String_value>,      "hashid":<Double_value>,      "comment":<String_value>,      "healthmonitor":<String_value>,      "appflowlog":<String_value>,      "statechangetimesec":<String_value>,      "tickssincelaststatechange":<Double_value>,      "threshold":<String_value>,      "clmonowner":<Double_value>,      "clmonview":<Double_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/gslbservice?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",gslbservice: [ { "__count": "#no"} ] }


