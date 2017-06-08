#wisite_farmname_binding

Binding object showing the farmname that can be bound to wisite.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>sitepath</td><td>&lt;String></td><td>Read-write</td><td>Path to the Web Interface site.&lt;br>Minimum length = 1&lt;br>Maximum length = 250</td><tr><tr><td>groups</td><td>&lt;String></td><td>Read-write</td><td>Active Directory groups that are permitted to enumerate resources from server farms. Including a setting for this parameter activates the user roaming feature. A maximum of 512 user groups can be specified for each farm defined with the Farm;lt;n;gt; parameter. The groups must be comma separated.</td><tr><tr><td>xmlport</td><td>&lt;Double></td><td>Read-write</td><td>Port number at which to contact the XML service.</td><tr><tr><td>transport</td><td>&lt;String></td><td>Read-write</td><td>Transport protocol to use for transferring data, related to the Web Interface site, between the NetScaler appliance and the XML service.&lt;br>Possible values = HTTP, HTTPS, SSLRELAY</td><tr><tr><td>sslrelayport</td><td>&lt;Double></td><td>Read-write</td><td>TCP port at which the XenApp or XenDesktop servers listenfor SSL Relay traffic from the NetScaler appliance. This parameter is required if you have set SSL Relay as the transport protocol. Web Interface uses root certificates when authenticating a server running SSL Relay. Make sure that all the servers running SSL Relay are configured to listen on the same port.</td><tr><tr><td>farmname</td><td>&lt;String></td><td>Read-write</td><td>Name for the logical representation of a XenApp or XenDesktop farm to be bound to the Web Interface site. Must begin with an ASCII alphabetic or underscore (_) character, and must contain only ASCII alphanumeric, underscore, hash (#), period (.), space, colon (:), at (@), equals (=), and hyphen (-) characters.</td><tr><tr><td>loadbalance</td><td>&lt;String></td><td>Read-write</td><td>Use all the XML servers (load balancing mode) or only one server (failover mode).&lt;br>Possible values = ON, OFF</td><tr><tr><td>recoveryfarm</td><td>&lt;String></td><td>Read-write</td><td>Binded farm is set as a recovery farm.&lt;br>Default value: OFF&lt;br>Possible values = ON, OFF</td><tr><tr><td>xmlserveraddresses</td><td>&lt;String></td><td>Read-write</td><td>Comma-separated IP addresses or host names of XenApp or XenDesktop servers providing XML services.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-write</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD:](#add:) | [DELETE:](#delete:) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add:



URL: http://NS_IP/nitro/v1/config
HTTP Method: PUT
Request Payload: ```{"params":{      "warning":<String_value>,      "onerror":<String_value>},sessionid":"##sessionid","wisite_farmname_binding":{      "sitepath":<String_value>,      "farmname":<String_value>,                  "xmlserveraddresses":<String_value>,                  "groups":<String_value>,                  "recoveryfarm":<String_value>,                  "xmlport":<Double_value>,                  "transport":<String_value>,                  "sslrelayport":<Double_value>,                  "loadbalance":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete:



URL: http://&lt;NS_IP&gt;/nitro/v1/config/wisite_farmname_binding/sitepath_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/wisite_farmname_binding/sitepath_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/wisite_farmname_binding/sitepath_value&lt;String&gt;
Query-parameters:
filter
http://&lt;NS_IP&gt;/nitro/v1/config/wisite_farmname_binding/sitepath_value&lt;String&gt;?filter=property-name1:property-value1,property-name2:property-value2
Use this query-parameter to get the filtered set of wisite_farmname_binding resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/wisite_farmname_binding/sitepath_value&lt;String&gt;?pagesize=#no;pageno=#no
Use this query-parameter to get the wisite_farmname_binding resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/wisite_farmname_binding?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "wisite_farmname_binding": [ {      "sitepath":<String_value>,      "groups":<String_value>,      "xmlport":<Double_value>,      "transport":<String_value>,      "sslrelayport":<Double_value>,      "farmname":<String_value>,      "loadbalance":<String_value>,      "recoveryfarm":<String_value>,      "xmlserveraddresses":<String_value>,}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/wisite_farmname_binding/sitepath_value&lt;String&gt;?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",wisite_farmname_binding: [ { "__count": "#no"} ] }


