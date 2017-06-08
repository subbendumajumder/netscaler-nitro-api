#appflowparam

Configuration for AppFlow parameter resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>templaterefresh</td><td>&lt;Double></td><td>Read-write</td><td>Refresh interval, in seconds, at which to export the template data. Because data transmission is in UDP, the templates must be resent at regular intervals.&lt;br>Default value: 600&lt;br>Minimum value = 60&lt;br>Maximum value = 3600</td><tr><tr><td>appnamerefresh</td><td>&lt;Double></td><td>Read-write</td><td>Interval, in seconds, at which to send Appnames to the configured collectors. Appname refers to the name of an entity (virtual server, service, or service group) in the NetScaler appliance.&lt;br>Default value: 600&lt;br>Minimum value = 60&lt;br>Maximum value = 3600</td><tr><tr><td>flowrecordinterval</td><td>&lt;Double></td><td>Read-write</td><td>Interval, in seconds, at which to send flow records to the configured collectors.&lt;br>Default value: 60&lt;br>Minimum value = 60&lt;br>Maximum value = 3600</td><tr><tr><td>udppmtu</td><td>&lt;Double></td><td>Read-write</td><td>MTU, in bytes, for IPFIX UDP packets.&lt;br>Default value: 1472&lt;br>Minimum value = 128&lt;br>Maximum value = 1472</td><tr><tr><td>httpurl</td><td>&lt;String></td><td>Read-write</td><td>Include the http URL that the NetScaler appliance received from the client.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>aaausername</td><td>&lt;String></td><td>Read-write</td><td>Enable AppFlow AAA Username logging.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>httpcookie</td><td>&lt;String></td><td>Read-write</td><td>Include the cookie that was in the HTTP request the appliance received from the client.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>httpreferer</td><td>&lt;String></td><td>Read-write</td><td>Include the web page that was last visited by the client.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>httpmethod</td><td>&lt;String></td><td>Read-write</td><td>Include the method that was specified in the HTTP request that the appliance received from the client.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>httphost</td><td>&lt;String></td><td>Read-write</td><td>Include the host identified in the HTTP request that the appliance received from the client.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>httpuseragent</td><td>&lt;String></td><td>Read-write</td><td>Include the client application through which the HTTP request was received by the NetScaler appliance.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>clienttrafficonly</td><td>&lt;String></td><td>Read-write</td><td>Generate AppFlow records for only the traffic from the client.&lt;br>Default value: NO&lt;br>Possible values = YES, NO</td><tr><tr><td>httpcontenttype</td><td>&lt;String></td><td>Read-write</td><td>Include the HTTP Content-Type header sent from the server to the client to determine the type of the content sent.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>httpauthorization</td><td>&lt;String></td><td>Read-write</td><td>Include the HTTP Authorization header information.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>httpvia</td><td>&lt;String></td><td>Read-write</td><td>Include the httpVia header which contains the IP address of proxy server through which the client accessed the server.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>httpxforwardedfor</td><td>&lt;String></td><td>Read-write</td><td>Include the httpXForwardedFor header, which contains the original IP Address of the client using a proxy server to access the server.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>httplocation</td><td>&lt;String></td><td>Read-write</td><td>Include the HTTP location headers returned from the HTTP responses.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>httpsetcookie</td><td>&lt;String></td><td>Read-write</td><td>Include the Set-cookie header sent from the server to the client in response to a HTTP request.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>httpsetcookie2</td><td>&lt;String></td><td>Read-write</td><td>Include the Set-cookie header sent from the server to the client in response to a HTTP request.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>connectionchaining</td><td>&lt;String></td><td>Read-write</td><td>Enable connection chaining so that the client server flows of a connection are linked. Also the connection chain ID is propagated across NetScalers, so that in a multi-hop environment the flows belonging to the same logical connection are linked. This id is also logged as part of appflow record.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>httpdomain</td><td>&lt;String></td><td>Read-write</td><td>Include the http domain request to be exported.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>skipcacheredirectionhttptransaction</td><td>&lt;String></td><td>Read-write</td><td>Skip Cache http transaction. This HTTP transaction is specific to Cache Redirection module. In Case of Cache Miss there will be another HTTP transaction initiated by the cache server.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>builtin</td><td>&lt;String[]></td><td>Read-only</td><td>Flag to determine if the appflow param is built-in or not.&lt;br>Possible values = MODIFIABLE, DELETABLE, IMMUTABLE</td><tr></tbody></table>
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
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","appflowparam":{      "templaterefresh":<Double_value>,      "appnamerefresh":<Double_value>,      "flowrecordinterval":<Double_value>,      "udppmtu":<Double_value>,      "httpurl":<String_value>,      "aaausername":<String_value>,      "httpcookie":<String_value>,      "httpreferer":<String_value>,      "httpmethod":<String_value>,      "httphost":<String_value>,      "httpuseragent":<String_value>,      "clienttrafficonly":<String_value>,      "httpcontenttype":<String_value>,      "httpauthorization":<String_value>,      "httpvia":<String_value>,      "httpxforwardedfor":<String_value>,      "httplocation":<String_value>,      "httpsetcookie":<String_value>,      "httpsetcookie2":<String_value>,      "connectionchaining":<String_value>,      "httpdomain":<String_value>,      "skipcacheredirectionhttptransaction":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","appflowparam":{      "templaterefresh":true,      "appnamerefresh":true,      "flowrecordinterval":true,      "udppmtu":true,      "httpurl":true,      "aaausername":true,      "httpcookie":true,      "httpreferer":true,      "httpmethod":true,      "httphost":true,      "httpuseragent":true,      "clienttrafficonly":true,      "httpcontenttype":true,      "httpauthorization":true,      "httpvia":true,      "httpxforwardedfor":true,      "httplocation":true,      "httpsetcookie":true,      "httpsetcookie2":true,      "connectionchaining":true,      "httpdomain":true,      "skipcacheredirectionhttptransaction":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/appflowparam
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "appflowparam": [ {      "templaterefresh":<Double_value>,      "appnamerefresh":<Double_value>,      "flowrecordinterval":<Double_value>,      "udppmtu":<Double_value>,      "httpurl":<String_value>,      "aaausername":<String_value>,      "httpcookie":<String_value>,      "httpreferer":<String_value>,      "httpmethod":<String_value>,      "httphost":<String_value>,      "httpuseragent":<String_value>,      "clienttrafficonly":<String_value>,      "httpcontenttype":<String_value>,      "httpauthorization":<String_value>,      "httpvia":<String_value>,      "httpxforwardedfor":<String_value>,      "httplocation":<String_value>,      "httpsetcookie":<String_value>,      "httpsetcookie2":<String_value>,      "connectionchaining":<String_value>,      "httpdomain":<String_value>,      "skipcacheredirectionhttptransaction":<String_value>,      "builtin":<String[]_value>}]}```



