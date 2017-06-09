#wfsite

Configuration for WF site resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>sitename</td><td>&lt;String></td><td>Read-write</td><td>Name of the WebFront site being created on the NetScaler appliance.&lt;br>Minimum length = 1&lt;br>Maximum length = 255</td><tr><tr><td>storefronturl</td><td>&lt;String></td><td>Read-write</td><td>FQDN or IP of Windows StoreFront server where the store is configured.&lt;br>Minimum length = 1&lt;br>Maximum length = 255</td><tr><tr><td>storename</td><td>&lt;String></td><td>Read-write</td><td>Name of the store present in StoreFront.&lt;br>Minimum length = 1&lt;br>Maximum length = 255</td><tr><tr><td>html5receiver</td><td>&lt;String></td><td>Read-write</td><td>Specifies whether or not to use HTML5 receiver for launching apps for the WF site.&lt;br>Default value: FALLBACK&lt;br>Possible values = ALWAYS, FALLBACK, OFF</td><tr><tr><td>workspacecontrol</td><td>&lt;String></td><td>Read-write</td><td>Specifies whether of not to use workspace control for the WF site.&lt;br>Default value: ON&lt;br>Possible values = ON, OFF</td><tr><tr><td>displayroamingaccounts</td><td>&lt;String></td><td>Read-write</td><td>Specifies whether or not to display the accounts selection screen during First Time Use of Receiver .&lt;br>Default value: ON&lt;br>Possible values = ON, OFF</td><tr><tr><td>xframeoptions</td><td>&lt;String></td><td>Read-write</td><td>The value to be sent in the X-Frame-Options header. WARNING: Setting this option to ALLOW could leave the end user vulnerable to Click Jacking attacks.&lt;br>Default value: DENY&lt;br>Possible values = ALLOW, DENY</td><tr><tr><td>state</td><td>&lt;String></td><td>Read-only</td><td>State of wf site.&lt;br>Default value: UP&lt;br>Possible values = UP, INITIALIZING, DOWN-HostUnknown, DOWN-ReqTimeout, DOWN-Wrong Store, DOWN-SF Error, DOWN-SSL Error, DOWN-Conn Reset, DOWN</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [DELETE](#delete) | [UPDATE](#update) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>},"sessionid":"##sessionid","wfsite":{      "sitename":<String_value>,      "storefronturl":<String_value>,      "storename":<String_value>,      "html5receiver":<String_value>,      "workspacecontrol":<String_value>,      "displayroamingaccounts":<String_value>,      "xframeoptions":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/wfsite/sitename_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/wfsite/sitename_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","wfsite":{      "sitename":<String_value>,      "storefronturl":<String_value>,      "storename":<String_value>,      "html5receiver":<String_value>,      "workspacecontrol":<String_value>,      "displayroamingaccounts":<String_value>,      "xframeoptions":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/wfsite
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/wfsite?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of wfsite resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/wfsite?view=summary
Use this query-parameter to get the summary output of wfsite resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/wfsite?pagesize=#no;pageno=#no
Use this query-parameter to get the wfsite resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/wfsite?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "wfsite": [ {      "sitename":<String_value>,      "storefronturl":<String_value>,      "storename":<String_value>,      "html5receiver":<String_value>,      "workspacecontrol":<String_value>,      "displayroamingaccounts":<String_value>,      "xframeoptions":<String_value>,      "state":<String_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/wfsite/sitename_value&lt;String&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "wfsite": [ {      "sitename":<String_value>,      "storefronturl":<String_value>,      "storename":<String_value>,      "html5receiver":<String_value>,      "workspacecontrol":<String_value>,      "displayroamingaccounts":<String_value>,      "xframeoptions":<String_value>,      "state":<String_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/wfsite?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",wfsite: [ { "__count": "#no"} ] }


