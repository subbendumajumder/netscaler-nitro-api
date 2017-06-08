#dnskey

Configuration for 0 resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>keyname</td><td>&lt;String></td><td>Read-write</td><td>Name of the public-private key pair to publish in the zone.&lt;br>Minimum length = 1</td><tr><tr><td>publickey</td><td>&lt;String></td><td>Read-write</td><td>File name of the public key.</td><tr><tr><td>privatekey</td><td>&lt;String></td><td>Read-write</td><td>File name of the private key.</td><tr><tr><td>expires</td><td>&lt;Double></td><td>Read-write</td><td>Time period for which to consider the key valid, after the key is used to sign a zone.&lt;br>Default value: 120&lt;br>Minimum value = 1&lt;br>Maximum value = 32767</td><tr><tr><td>units1</td><td>&lt;String></td><td>Read-write</td><td>Units for the expiry period.&lt;br>Default value: DAYS&lt;br>Possible values = MINUTES, HOURS, DAYS</td><tr><tr><td>notificationperiod</td><td>&lt;Double></td><td>Read-write</td><td>Time at which to generate notification of key expiration, specified as number of days, hours, or minutes before expiry. Must be less than the expiry period. The notification is an SNMP trap sent to an SNMP manager. To enable the appliance to send the trap, enable the DNSKEY-EXPIRY SNMP alarm.&lt;br>Default value: 7&lt;br>Minimum value = 1&lt;br>Maximum value = 32767</td><tr><tr><td>units2</td><td>&lt;String></td><td>Read-write</td><td>Units for the notification period.&lt;br>Default value: DAYS&lt;br>Possible values = MINUTES, HOURS, DAYS</td><tr><tr><td>ttl</td><td>&lt;Double></td><td>Read-write</td><td>Time to Live (TTL), in seconds, for the DNSKEY resource record created in the zone. TTL is the time for which the record must be cached by the DNS proxies. If the TTL is not specified, either the DNS zones minimum TTL or the default value of 3600 is used.&lt;br>Default value: 3600&lt;br>Minimum value = 0&lt;br>Maximum value = 2147483647</td><tr><tr><td>zonename</td><td>&lt;String></td><td>Read-write</td><td>Name of the zone for which to create a key.&lt;br>Minimum length = 1</td><tr><tr><td>keytype</td><td>&lt;String></td><td>Read-write</td><td>Type of key to create.&lt;br>Default value: NS_DNSKEY_ZSK&lt;br>Possible values = KSK, KeySigningKey, ZSK, ZoneSigningKey</td><tr><tr><td>algorithm</td><td>&lt;String></td><td>Read-write</td><td>Algorithm to generate for zone signing.&lt;br>Default value: NS_DNSKEYALGO_RSASHA1&lt;br>Possible values = RSASHA1</td><tr><tr><td>keysize</td><td>&lt;Double></td><td>Read-write</td><td>Size of the key, in bits.&lt;br>Default value: 512</td><tr><tr><td>filenameprefix</td><td>&lt;String></td><td>Read-write</td><td>Common prefix for the names of the generated public and private key files and the Delegation Signer (DS) resource record. During key generation, the .key, .private, and .ds suffixes are appended automatically to the file name prefix to produce the names of the public key, the private key, and the DS record, respectively.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [CREATE](#create) | [UPDATE](#update) | [UNSET](#unset) | [DELETE](#delete) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>},"sessionid":"##sessionid","dnskey":{      "keyname":<String_value>,      "publickey":<String_value>,      "privatekey":<String_value>,      "expires":<Double_value>,                  "units1":<String_value>,      "notificationperiod":<Double_value>,                  "units2":<String_value>,      "ttl":<Double_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###create



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"create"},"sessionid":"##sessionid","dnskey":{      "zonename":<String_value>,      "keytype":<String_value>,      "algorithm":<String_value>,      "keysize":<Double_value>,      "filenameprefix":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","dnskey":{      "keyname":<String_value>,      "expires":<Double_value>,                  "units1":<String_value>,      "notificationperiod":<Double_value>,                  "units2":<String_value>,      "ttl":<Double_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","dnskey":{      "keyname":<String_value>,      "expires":true,      "units1":true,      "notificationperiod":true,      "units2":true,      "ttl":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/dnskey/keyname_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/dnskey/keyname_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/dnskey
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/dnskey?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of dnskey resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/dnskey?view=summary
Use this query-parameter to get the summary output of dnskey resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/dnskey?pagesize=#no;pageno=#no
Use this query-parameter to get the dnskey resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/dnskey?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "dnskey": [ {      "keyname":<String_value>,      "publickey":<String_value>,      "privatekey":<String_value>,      "expires":<Double_value>,      "units1":<String_value>,      "notificationperiod":<Double_value>,      "units2":<String_value>,      "ttl":<Double_value>,      "zonename":<String_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/dnskey/keyname_value&lt;String&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "dnskey": [ {      "keyname":<String_value>,      "publickey":<String_value>,      "privatekey":<String_value>,      "expires":<Double_value>,      "units1":<String_value>,      "notificationperiod":<Double_value>,      "units2":<String_value>,      "ttl":<Double_value>,      "zonename":<String_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/dnskey?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",dnskey: [ { "__count": "#no"} ] }


