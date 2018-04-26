#subscribergxinterface

Configuration for Gx interface Parameters resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>vserver</td><td>&lt;String></td><td>Read-write</td><td>Name of the load balancing, or content switching vserver to which the Gx connections are established. The service type of the virtual server must be DIAMETER/SSL_DIAMETER. Mutually exclusive with the service parameter. Therefore, you cannot set both service and the Virtual Server in the Gx Interface.<br>Minimum length = 1</td></tr><tr><td>service</td><td>&lt;String></td><td>Read-write</td><td>Name of DIAMETER/SSL_DIAMETER service corresponding to PCRF to which the Gx connection is established. The service type of the service must be DIAMETER/SSL_DIAMETER. Mutually exclusive with vserver parameter. Therefore, you cannot set both Service and the Virtual Server in the Gx Interface.<br>Minimum length = 1</td></tr><tr><td>pcrfrealm</td><td>&lt;String></td><td>Read-write</td><td>PCRF realm is of type DiameterIdentity and contains the realm of PCRF to which the message is to be routed. This is the realm used in Destination-Realm AVP by Netscaler Gx client (as a Diameter node).<br><br>Minimum length = 1</td></tr><tr><td>holdonsubscriberabsence</td><td>&lt;String></td><td>Read-write</td><td>Set this setting to yes if Netscaler needs to Hold pakcets till subscriber session is fetched from PCRF. Else set to NO. By default set to yes. If this setting is set to NO, then till NetScaler fetches subscriber from PCRF, default subscriber profile will be applied to this subscriber if configured. If default subscriber profile is also not configured an undef would be raised to expressions which use Subscriber attributes. .<br>Default value: NO<br>Possible values = YES, NO</td></tr><tr><td>requesttimeout</td><td>&lt;Double></td><td>Read-write</td><td>q!Time, in seconds, within which the Gx CCR request must complete. If the request does not complete within this time, the request is retransmitted for requestRetryAttempts time. If still reuqest is not complete then default subscriber profile will be applied to this subscriber if configured. If default subscriber profile is also not configured an undef would be raised to expressions which use Subscriber attributes.<br>Zero disables the timeout. !.<br>Default value: 10<br>Minimum value = 0<br>Maximum value = 86400</td></tr><tr><td>requestretryattempts</td><td>&lt;Double></td><td>Read-write</td><td>If the request does not complete within requestTimeout time, the request is retransmitted for requestRetryAttempts time.<br>Default value: 3</td></tr><tr><td>idlettl</td><td>&lt;Double></td><td>Read-write</td><td>q!Idle Time, in seconds, after which the Gx CCR-U request will be sent after any PCRF activity on a session. Any RAR or CCA message resets the timer.<br>Zero value disables the idle timeout. !.<br>Default value: 900<br>Minimum value = 0<br>Maximum value = 86400</td></tr><tr><td>revalidationtimeout</td><td>&lt;Double></td><td>Read-write</td><td>q!Revalidation Timeout, in seconds, after which the Gx CCR-U request will be sent after any PCRF activity on a session. Any RAR or CCA message resets the timer.<br>Zero value disables the idle timeout. !.<br>Default value: 0<br>Minimum value = 0<br>Maximum value = 86400</td></tr><tr><td>negativettl</td><td>&lt;Double></td><td>Read-write</td><td>q!Negative TTL, in seconds, after which the Gx CCR-I request will be resent for sessions that have not been resolved by PCRF due to server being down or no response or failed response. Instead of polling the PCRF server constantly, negative-TTL makes NS stick to un-resolved session. Meanwhile Netscaler installs a negative session to avoid going to PCRF.<br>For Negative Sessions, Netcaler inherits the attributes from default subscriber profile if default subscriber is configured. A default subscriber could be configured as 'add subscriber profile *'. Or these attributes can be inherited from Radius as well if Radius is configued.<br>Zero value disables the Negative Sessions. And Netscaler does not install Negative sessions even if subscriber session could not be fetched. !.<br>Default value: 600<br>Minimum value = 0<br>Maximum value = 86400</td></tr><tr><td>servicepathavp</td><td>&lt;Double[]></td><td>Read-write</td><td>The AVP code in which PCRF sends service path applicable for subscriber.<br>Minimum value = 1</td></tr><tr><td>servicepathvendorid</td><td>&lt;Double></td><td>Read-write</td><td>The vendorid of the AVP in which PCRF sends service path for subscriber.</td></tr><tr><td>nodeid</td><td>&lt;Double></td><td>Read-write</td><td>Unique number that identifies the cluster node.<br>Minimum value = 0<br>Maximum value = 31</td></tr><tr><td>svrstate</td><td>&lt;String></td><td>Read-only</td><td>The state of the gx service.<br>Possible values = UP, DOWN, UNKNOWN, BUSY, OUT OF SERVICE, GOING OUT OF SERVICE, DOWN WHEN GOING OUT OF SERVICE, NS_EMPTY_STR, Unknown, DISABLED</td></tr><tr><td>identity</td><td>&lt;String></td><td>Read-only</td><td>DiameterIdentity to be used by NS. DiameterIdentity is used to identify a Diameter node uniquely. Before setting up diameter configuration, Netscaler (as a Diameter node) MUST be assigned a unique DiameterIdentity.<br>example =&gt;<br>set ns diameter -identity netscaler.com<br>Now whenever Netscaler system needs to use identity in diameter messages. It will use 'netscaler.com' as Origin-Host AVP as defined in RFC3588<br>.<br>Minimum length = 1</td></tr><tr><td>realm</td><td>&lt;String></td><td>Read-only</td><td>Diameter Realm to be used by NS.<br>example =&gt;<br>set ns diameter -realm com<br>Now whenever Netscaler system needs to use realm in diameter messages. It will use 'com' as Origin-Realm AVP as defined in RFC3588<br>.<br>Minimum length = 1</td></tr><tr><td>status</td><td>&lt;String></td><td>Read-only</td><td>NetScaler PCRF connection Status. (Gx Protocol State).</td></tr><tr><td>servicepathinfomode</td><td>&lt;String></td><td>Read-only</td><td>The type of info in which service path is passed from PCRF,<br>SERVICE_FUNCTION: Denotes the service chain is passed as servicefunction names in-order in AVPS with code servicepathAVP<br>SERVICE_PATH: Denotes the service path name is passed in AVPS with code servicepathAVP.q.<br>Default value: SERVICEPATH<br>Possible values = SERVICEFUNCTIONS, SERVICEPATH</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[UPDATE](#u)| [UNSET](#)| [GET (ALL)](#get-)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/subscribergxinterface
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"subscribergxinterface":{"vserver":<String_value>,"service":<String_value>,"pcrfrealm":<String_value>,"holdonsubscriberabsence":<String_value>,"requesttimeout":<Double_value>,"requestretryattempts":<Double_value>,"idlettl":<Double_value>,"revalidationtimeout":<Double_value>,"negativettl":<Double_value>,"servicepathavp":<Double[]_value>,"servicepathvendorid":<Double_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/subscribergxinterface?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"subscribergxinterface":{"vserver":true,"service":true,"holdonsubscriberabsence":true,"requesttimeout":true,"requestretryattempts":true,"idlettl":true,"revalidationtimeout":true,"negativettl":true,"servicepathavp":true,"servicepathvendorid":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/subscribergxinterface
<b>Query-parameters:</b>
<b>args</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/subscribergxinterface?<b>args=nodeid:&lt;Double_value&gt;</b>
Use this query-parameter to get subscribergxinterface resources based on additional properties.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "subscribergxinterface": [ {nodeid:<Double_value>"vserver":<String_value>,"service":<String_value>,"svrstate":<String_value>,"pcrfrealm":<String_value>,"holdonsubscriberabsence":<String_value>,"requesttimeout":<Double_value>,"requestretryattempts":<Double_value>,"idlettl":<Double_value>,"revalidationtimeout":<Double_value>,"negativettl":<Double_value>,"identity":<String_value>,"realm":<String_value>,"status":<String_value>,"servicepathavp":<Double[]_value>,"servicepathvendorid":<Double_value>,"servicepathinfomode":<String_value>}]}```



