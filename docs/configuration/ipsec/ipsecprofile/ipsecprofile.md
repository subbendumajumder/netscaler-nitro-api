#ipsecprofile

Configuration for IPSEC profile resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>The name of the ipsec profile.&lt;br>Minimum length = 1&lt;br>Maximum length = 32</td><tr><tr><td>ikeversion</td><td>&lt;String></td><td>Read-write</td><td>IKE Protocol Version.&lt;br>Possible values = V1, V2</td><tr><tr><td>encalgo</td><td>&lt;String[]></td><td>Read-write</td><td>Type of encryption algorithm.&lt;br>Possible values = AES, 3DES</td><tr><tr><td>hashalgo</td><td>&lt;String[]></td><td>Read-write</td><td>Type of hashing algorithm.&lt;br>Possible values = HMAC_SHA1, HMAC_SHA256, HMAC_SHA384, HMAC_SHA512, HMAC_MD5</td><tr><tr><td>lifetime</td><td>&lt;Double></td><td>Read-write</td><td>Lifetime of IKE SA in seconds. Lifetime of IPSec SA will be (lifetime of IKE SA/8).&lt;br>Minimum value = 480&lt;br>Maximum value = 31536000</td><tr><tr><td>psk</td><td>&lt;String></td><td>Read-write</td><td>Pre shared key value.</td><tr><tr><td>publickey</td><td>&lt;String></td><td>Read-write</td><td>Public key file path.</td><tr><tr><td>privatekey</td><td>&lt;String></td><td>Read-write</td><td>Private key file path.</td><tr><tr><td>peerpublickey</td><td>&lt;String></td><td>Read-write</td><td>Peer public key file path.</td><tr><tr><td>livenesscheckinterval</td><td>&lt;Double></td><td>Read-write</td><td>Number of seconds after which a notify payload is sent to check the liveliness of the peer. Additional retries are done as per retransmit interval setting. Zero value disables liveliness checks.&lt;br>Minimum value = 0&lt;br>Maximum value = 64999</td><tr><tr><td>replaywindowsize</td><td>&lt;Double></td><td>Read-write</td><td>IPSec Replay window size for the data traffic.&lt;br>Minimum value = 0&lt;br>Maximum value = 16384</td><tr><tr><td>ikeretryinterval</td><td>&lt;Double></td><td>Read-write</td><td>IKE retry interval for bringing up the connection.&lt;br>Minimum value = 60&lt;br>Maximum value = 3600</td><tr><tr><td>retransmissiontime</td><td>&lt;Double></td><td>Read-write</td><td>The interval in seconds to retry sending the IKE messages to peer, three consecutive attempts are done with doubled interval after every failure.&lt;br>Minimum value = 1&lt;br>Maximum value = 99</td><tr><tr><td>perfectforwardsecrecy</td><td>&lt;String></td><td>Read-write</td><td>Enable/Disable PFS.&lt;br>Possible values = ENABLE, DISABLE</td><tr><tr><td>builtin</td><td>&lt;String[]></td><td>Read-only</td><td>Indicates that a variable is a built-in (SYSTEM INTERNAL) type.&lt;br>Possible values = MODIFIABLE, DELETABLE, IMMUTABLE</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [DELETE](#delete) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>},"sessionid":"##sessionid","ipsecprofile":{      "name":<String_value>,      "ikeversion":<String_value>,      "encalgo":<String[]_value>,      "hashalgo":<String[]_value>,      "lifetime":<Double_value>,      "psk":<String_value>,      "publickey":<String_value>,                  "privatekey":<String_value>,                  "peerpublickey":<String_value>,      "livenesscheckinterval":<Double_value>,      "replaywindowsize":<Double_value>,      "ikeretryinterval":<Double_value>,      "retransmissiontime":<Double_value>,      "perfectforwardsecrecy":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/ipsecprofile/name_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/ipsecprofile/name_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/ipsecprofile
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/ipsecprofile?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of ipsecprofile resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/ipsecprofile?view=summary
Use this query-parameter to get the summary output of ipsecprofile resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/ipsecprofile?pagesize=#no;pageno=#no
Use this query-parameter to get the ipsecprofile resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/ipsecprofile?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "ipsecprofile": [ {      "name":<String_value>,      "ikeversion":<String_value>,      "encalgo":<String[]_value>,      "hashalgo":<String[]_value>,      "lifetime":<Double_value>,      "livenesscheckinterval":<Double_value>,      "replaywindowsize":<Double_value>,      "retransmissiontime":<Double_value>,      "psk":<String_value>,      "publickey":<String_value>,      "privatekey":<String_value>,      "peerpublickey":<String_value>,      "ikeretryinterval":<Double_value>,      "perfectforwardsecrecy":<String_value>,      "builtin":<String[]_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/ipsecprofile/name_value&lt;String&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "ipsecprofile": [ {      "name":<String_value>,      "ikeversion":<String_value>,      "encalgo":<String[]_value>,      "hashalgo":<String[]_value>,      "lifetime":<Double_value>,      "livenesscheckinterval":<Double_value>,      "replaywindowsize":<Double_value>,      "retransmissiontime":<Double_value>,      "psk":<String_value>,      "publickey":<String_value>,      "privatekey":<String_value>,      "peerpublickey":<String_value>,      "ikeretryinterval":<Double_value>,      "perfectforwardsecrecy":<String_value>,      "builtin":<String[]_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/ipsecprofile?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",ipsecprofile: [ { "__count": "#no"} ] }


