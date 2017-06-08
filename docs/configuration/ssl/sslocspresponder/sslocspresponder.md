#sslocspresponder

Configuration for OCSP responser resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the OCSP responder. Cannot begin with a hash (#) or space character and must contain only ASCII alphanumeric, underscore (_), hash (#), period (.), space, colon (:), at (@), equals (=), and hyphen (-) characters. Cannot be changed after the responder is created. The following requirement applies only to the NetScaler CLI: If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my responder" or my responder).&lt;br>Minimum length = 1</td><tr><tr><td>url</td><td>&lt;String></td><td>Read-write</td><td>URL of the OCSP responder.&lt;br>Minimum length = 1</td><tr><tr><td>cache</td><td>&lt;String></td><td>Read-write</td><td>Enable caching of responses. Caching of responses received from the OCSP responder enables faster responses to the clients and reduces the load on the OCSP responder.&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>cachetimeout</td><td>&lt;Double></td><td>Read-write</td><td>Timeout for caching the OCSP response. After the timeout, the NetScaler sends a fresh request to the OCSP responder for the certificate status. If a timeout is not specified, the timeout provided in the OCSP response applies.&lt;br>Default value: 1&lt;br>Minimum value = 1&lt;br>Maximum value = 1440</td><tr><tr><td>batchingdepth</td><td>&lt;Double></td><td>Read-write</td><td>Number of client certificates to batch together into one OCSP request. Batching avoids overloading the OCSP responder. A value of 1 signifies that each request is queried independently. For a value greater than 1, specify a timeout (batching delay) to avoid inordinately delaying the processing of a single certificate.&lt;br>Minimum value = 1&lt;br>Maximum value = 8</td><tr><tr><td>batchingdelay</td><td>&lt;Double></td><td>Read-write</td><td>Maximum time, in milliseconds, to wait to accumulate OCSP requests to batch. Does not apply if the Batching Depth is 1.&lt;br>Minimum value = 0&lt;br>Maximum value = 10000</td><tr><tr><td>resptimeout</td><td>&lt;Double></td><td>Read-write</td><td>Time, in milliseconds, to wait for an OCSP response. When this time elapses, an error message appears or the transaction is forwarded, depending on the settings on the virtual server. Includes Batching Delay time.&lt;br>Minimum value = 0&lt;br>Maximum value = 120000</td><tr><tr><td>respondercert</td><td>&lt;String></td><td>Read-write</td><td>.&lt;br>Minimum length = 1</td><tr><tr><td>trustresponder</td><td>&lt;Boolean></td><td>Read-write</td><td>A certificate to use to validate OCSP responses. Alternatively, if -trustResponder is specified, no verification will be done on the reponse. If both are omitted, only the response times (producedAt, lastUpdate, nextUpdate) will be verified.</td><tr><tr><td>producedattimeskew</td><td>&lt;Double></td><td>Read-write</td><td>Time, in seconds, for which the NetScaler waits before considering the response as invalid. The response is considered invalid if the Produced At time stamp in the OCSP response exceeds or precedes the current NetScaler clock time by the amount of time specified.&lt;br>Default value: 300&lt;br>Minimum value = 0&lt;br>Maximum value = 86400</td><tr><tr><td>signingcert</td><td>&lt;String></td><td>Read-write</td><td>Certificate-key pair that is used to sign OCSP requests. If this parameter is not set, the requests are not signed.&lt;br>Minimum length = 1</td><tr><tr><td>usenonce</td><td>&lt;String></td><td>Read-write</td><td>Enable the OCSP nonce extension, which is designed to prevent replay attacks.&lt;br>Possible values = YES, NO</td><tr><tr><td>insertclientcert</td><td>&lt;String></td><td>Read-write</td><td>Include the complete client certificate in the OCSP request.&lt;br>Possible values = YES, NO</td><tr><tr><td>useaia</td><td>&lt;Boolean></td><td>Read-only</td><td>Only use the URL present in the certificate.</td><tr><tr><td>dns</td><td>&lt;String></td><td>Read-only</td><td>Was DNS resolution successful for a domain-based OCSP responder.</td><tr><tr><td>ipaddress</td><td>&lt;String></td><td>Read-only</td><td>The IPv6 address of the ocsp responder.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [DELETE](#delete) | [UPDATE](#update) | [UNSET](#unset) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>},"sessionid":"##sessionid","sslocspresponder":{      "name":<String_value>,      "url":<String_value>,      "cache":<String_value>,      "cachetimeout":<Double_value>,      "batchingdepth":<Double_value>,      "batchingdelay":<Double_value>,      "resptimeout":<Double_value>,      "respondercert":<String_value>,                  "trustresponder":<Boolean_value>,      "producedattimeskew":<Double_value>,      "signingcert":<String_value>,      "usenonce":<String_value>,      "insertclientcert":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/sslocspresponder/name_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/sslocspresponder/name_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","sslocspresponder":{      "name":<String_value>,      "url":<String_value>,      "cache":<String_value>,      "cachetimeout":<Double_value>,      "batchingdepth":<Double_value>,      "batchingdelay":<Double_value>,      "resptimeout":<Double_value>,      "respondercert":<String_value>,                  "trustresponder":<Boolean_value>,      "producedattimeskew":<Double_value>,      "signingcert":<String_value>,      "usenonce":<String_value>,      "insertclientcert":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","sslocspresponder":{      "name":<String_value>,      "trustresponder":true,      "insertclientcert":true,      "cache":true,      "cachetimeout":true,      "batchingdepth":true,      "batchingdelay":true,      "resptimeout":true,      "respondercert":true,      "producedattimeskew":true,      "signingcert":true,      "usenonce":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/sslocspresponder
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/sslocspresponder?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of sslocspresponder resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/sslocspresponder?view=summary
Use this query-parameter to get the summary output of sslocspresponder resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/sslocspresponder?pagesize=#no;pageno=#no
Use this query-parameter to get the sslocspresponder resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/sslocspresponder?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "sslocspresponder": [ {      "name":<String_value>,      "url":<String_value>,      "useaia":<Boolean_value>,      "cache":<String_value>,      "cachetimeout":<Double_value>,      "batchingdepth":<Double_value>,      "batchingdelay":<Double_value>,      "resptimeout":<Double_value>,      "producedattimeskew":<Double_value>,      "respondercert":<String_value>,      "trustresponder":<Boolean_value>,      "signingcert":<String_value>,      "usenonce":<String_value>,      "dns":<String_value>,      "insertclientcert":<String_value>,      "ipaddress":<String_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/sslocspresponder/name_value&lt;String&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "sslocspresponder": [ {      "name":<String_value>,      "url":<String_value>,      "useaia":<Boolean_value>,      "cache":<String_value>,      "cachetimeout":<Double_value>,      "batchingdepth":<Double_value>,      "batchingdelay":<Double_value>,      "resptimeout":<Double_value>,      "producedattimeskew":<Double_value>,      "respondercert":<String_value>,      "trustresponder":<Boolean_value>,      "signingcert":<String_value>,      "usenonce":<String_value>,      "dns":<String_value>,      "insertclientcert":<String_value>,      "ipaddress":<String_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/sslocspresponder?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",sslocspresponder: [ { "__count": "#no"} ] }


