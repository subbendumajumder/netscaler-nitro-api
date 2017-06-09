#subscribersessions

Configuration for subscriber sesions resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>ip</td><td>&lt;String></td><td>Read-write</td><td>Subscriber IP Address.</td><tr><tr><td>subscriptionidtype</td><td>&lt;String></td><td>Read-only</td><td>Subscription-Id type.&lt;br>Possible values = E164, IMSI, SIP_URI, NAI, PRIVATE</td><tr><tr><td>subscriptionidvalue</td><td>&lt;String></td><td>Read-only</td><td>Subscription-Id value.</td><tr><tr><td>subscriberrules</td><td>&lt;String[]></td><td>Read-only</td><td>Rules stored in this session for this subscriber. When PCRF sends Charging-Rule-Name or Charging-Rule-Base-Name AVP for a subscriber, Netscaler stores these AVPs in the subscriber session. These Rules can be retreived using Subscriber.Rule_Active(;lt;rule name;gt;) expression. For static subscriber profiles, these rules are configured using -subscriberRules ;lt;list of rules;gt;.</td><tr><tr><td>flags</td><td>&lt;Double></td><td>Read-only</td><td>Subscriber Session flags.</td><tr><tr><td>ttl</td><td>&lt;Double></td><td>Read-only</td><td>Subscriber Session Activity Timeout remaining. Netscaler will send a CCR-U after ttl expires. If subscriber sessions is a negative session, then Netscaler will send a CCR-I after TTL expires. Negative Sessions are sessions which have not been resolved by PCRF and instead of polling PCRF continously, Netscaler has installed a negative session. If default subscriber is configued, then Negative Sessions inherits default subscriber profile. .</td><tr><tr><td>avpdisplaybuffer</td><td>&lt;String></td><td>Read-only</td><td>Subscriber Attributes Display.</td><tr><tr><td>servicepath</td><td>&lt;String></td><td>Read-only</td><td>Name of the servicepath to be taken for this subscriber.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[CLEAR](#clear) | [GET (ALL)](#get-(all)) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###clear



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"clear"},"sessionid":"##sessionid","subscribersessions":{      "ip":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/subscribersessions
Query-parameters:
args
http://&lt;NSIP&gt;/nitro/v1/config/subscribersessions?args=      "ip":&lt;String_value&gt;,
Use this query-parameter to get subscribersessions resources based on additional properties.


filter
http://&lt;NSIP&gt;/nitro/v1/config/subscribersessions?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of subscribersessions resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/subscribersessions?view=summary
Use this query-parameter to get the summary output of subscribersessions resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/subscribersessions?pagesize=#no;pageno=#no
Use this query-parameter to get the subscribersessions resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/subscribersessions?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "subscribersessions": [ {      "ip":<String_value>,      "subscriptionidtype":<String_value>,      "subscriptionidvalue":<String_value>,      "subscriberrules":<String[]_value>,      "flags":<Double_value>,      "ttl":<Double_value>,      "avpdisplaybuffer":<String_value>,      "servicepath":<String_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/subscribersessions?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",subscribersessions: [ { "__count": "#no"} ] }


