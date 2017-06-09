#subscribersessions

Configuration for subscriber sesions resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>ip</td><td>&lt;String></td><td>Read-write</td><td>Subscriber IP Address.</td><tr><tr><td>subscriptionidtype</td><td>&lt;String></td><td>Read-only</td><td>Subscription-Id type.&lt;br>Possible values = E164, IMSI, SIP_URI, NAI, PRIVATE</td><tr><tr><td>subscriptionidvalue</td><td>&lt;String></td><td>Read-only</td><td>Subscription-Id value.</td><tr><tr><td>subscriberrules</td><td>&lt;String[]></td><td>Read-only</td><td>Rules stored in this session for this subscriber. When PCRF sends Charging-Rule-Name or Charging-Rule-Base-Name AVP for a subscriber, Netscaler stores these AVPs in the subscriber session. These Rules can be retreived using Subscriber.Rule_Active(;lt;rule name;gt;) expression. For static subscriber profiles, these rules are configured using -subscriberRules ;lt;list of rules;gt;.</td><tr><tr><td>flags</td><td>&lt;Double></td><td>Read-only</td><td>Subscriber Session flags.</td><tr><tr><td>ttl</td><td>&lt;Double></td><td>Read-only</td><td>Subscriber Session revalidation Timeout remaining. This TTL gets refreshed when a radius or CCA or RAR message is received for this subscriber session.&lt;br>Netscaler will send a CCR-U after revalidation timer expires.&lt;br>If subscriber sessions is a negative session, then Netscaler will send a CCR-I after TTL expires. Negative Sessions are sessions which have not been resolved by PCRF and instead of polling PCRF continously, Netscaler has installed a negative session. If default subscriber is configued, then Negative Sessions inherits default subscriber profile. .</td><tr><tr><td>idlettl</td><td>&lt;Double></td><td>Read-only</td><td>Subscriber Session Activity Timeout remaining. Netscaler will take an idleAction after ttl expires. idleaction could be --;gt;&lt;br>1. ccrTerminate: (default) send CCR-T to inform PCRF about session termination and delete the session. &lt;br>2. delete: Just delete the subscriber session without informing PCRF.&lt;br>3. ccrUpdate: Do not delete the session and instead send a CCR-U to PCRF requesting for an updated session.&lt;br> But if this is a negative session and idleaction is ccrUpdate then NS wont take any action. Also on negative sessions ccrTerminate translates to delete.</td><tr><tr><td>avpdisplaybuffer</td><td>&lt;String></td><td>Read-only</td><td>Subscriber Attributes Display.</td><tr><tr><td>servicepath</td><td>&lt;String></td><td>Read-only</td><td>Name of the servicepath to be taken for this subscriber.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[CLEAR](#clear) | [GET (ALL)](#get-(all)) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###clear



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/subscribersessions?action=clear
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"subscribersessions":{      "ip":<String_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/subscribersessions
Query-parameters:
args
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/subscribersessions?args=ip:&lt;String_value&gt;
Use this query-parameter to get subscribersessions resources based on additional properties.


attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/subscribersessions?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


filter
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/subscribersessions?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of subscribersessions resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/subscribersessions?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).


pagination
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/subscribersessions?pagesize=#no;pageno=#no
Use this query-parameter to get the subscribersessions resources in chunks.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "subscribersessions": [ {ip:<String_value>      "subscriptionidtype":<String_value>,      "subscriptionidvalue":<String_value>,      "subscriberrules":<String[]_value>,      "flags":<Double_value>,      "ttl":<Double_value>,      "idlettl":<Double_value>,      "avpdisplaybuffer":<String_value>,      "servicepath":<String_value>}]}```



###count



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/subscribersessions?count=yes
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: 
{ "subscribersessions": [ { "__count": "#no"} ] }


