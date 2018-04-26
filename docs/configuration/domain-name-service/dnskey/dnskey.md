#dnskey

Configuration for dns key resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>keyname</td><td>&lt;String></td><td>Read-write</td><td>Name of the public-private key pair to publish in the zone.<br>Minimum length = 1</td></tr><tr><td>publickey</td><td>&lt;String></td><td>Read-write</td><td>File name of the public key.</td></tr><tr><td>privatekey</td><td>&lt;String></td><td>Read-write</td><td>File name of the private key.</td></tr><tr><td>expires</td><td>&lt;Double></td><td>Read-write</td><td>Time period for which to consider the key valid, after the key is used to sign a zone.<br>Default value: 120<br>Minimum value = 1<br>Maximum value = 32767</td></tr><tr><td>units1</td><td>&lt;String></td><td>Read-write</td><td>Units for the expiry period.<br>Default value: DAYS<br>Possible values = MINUTES, HOURS, DAYS</td></tr><tr><td>notificationperiod</td><td>&lt;Double></td><td>Read-write</td><td>Time at which to generate notification of key expiration, specified as number of days, hours, or minutes before expiry. Must be less than the expiry period. The notification is an SNMP trap sent to an SNMP manager. To enable the appliance to send the trap, enable the DNSKEY-EXPIRY SNMP alarm.<br>Default value: 7<br>Minimum value = 1<br>Maximum value = 32767</td></tr><tr><td>units2</td><td>&lt;String></td><td>Read-write</td><td>Units for the notification period.<br>Default value: DAYS<br>Possible values = MINUTES, HOURS, DAYS</td></tr><tr><td>ttl</td><td>&lt;Double></td><td>Read-write</td><td>Time to Live (TTL), in seconds, for the DNSKEY resource record created in the zone. TTL is the time for which the record must be cached by the DNS proxies. If the TTL is not specified, either the DNS zone's minimum TTL or the default value of 3600 is used.<br>Default value: 3600<br>Minimum value = 0<br>Maximum value = 2147483647</td></tr><tr><td>password</td><td>&lt;String></td><td>Read-write</td><td>Passphrase for reading the encrypted public/private DNS keys.<br>Minimum length = 1</td></tr><tr><td>zonename</td><td>&lt;String></td><td>Read-write</td><td>Name of the zone for which to create a key.<br>Minimum length = 1</td></tr><tr><td>keytype</td><td>&lt;String></td><td>Read-write</td><td>Type of key to create.<br>Default value: NS_DNSKEY_ZSK<br>Possible values = KSK, KeySigningKey, ZSK, ZoneSigningKey</td></tr><tr><td>algorithm</td><td>&lt;String></td><td>Read-write</td><td>Algorithm to generate for zone signing.<br>Default value: NS_DNSKEYALGO_RSASHA1<br>Possible values = RSASHA1</td></tr><tr><td>keysize</td><td>&lt;Double></td><td>Read-write</td><td>Size of the key, in bits.<br>Default value: 512</td></tr><tr><td>filenameprefix</td><td>&lt;String></td><td>Read-write</td><td>Common prefix for the names of the generated public and private key files and the Delegation Signer (DS) resource record. During key generation, the .key, .private, and .ds suffixes are appended automatically to the file name prefix to produce the names of the public key, the private key, and the DS record, respectively.</td></tr><tr><td>src</td><td>&lt;String></td><td>Read-write</td><td>URL (protocol, host, path, and file name) from where the DNS key file will be imported. NOTE: The import fails if the object to be imported is on an HTTPS server that requires client certificate authentication for access. This is a mandatory argument.<br>Minimum length = 1<br>Maximum length = 2047</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD]()| [CREATE](#c)| [UPDATE](#u)| [UNSET](#)| [DELETE](#d)| [IMPORT](#i)| [GET (ALL)](#get-)| [GET]()| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnskey
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"dnskey":{<b>"keyname":<String_value>,</b><b>"publickey":<String_value>,</b><b>"privatekey":<String_value>,</b>"expires":<Double_value>,"units1":<String_value>,"notificationperiod":<Double_value>,"units2":<String_value>,"ttl":<Double_value>,"password":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###create



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnskey?<b>action=create</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"dnskey":{<b>"zonename":<String_value>,</b><b>"keytype":<String_value>,</b><b>"algorithm":<String_value>,</b><b>"keysize":<Double_value>,</b><b>"filenameprefix":<String_value>,</b>"password":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnskey
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"dnskey":{<b>"keyname":<String_value>,</b>"expires":<Double_value>,"units1":<String_value>,"notificationperiod":<Double_value>,"units2":<String_value>,"ttl":<Double_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnskey?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"dnskey":{<b>"keyname":<String_value>,</b>"expires":true,"units1":true,"notificationperiod":true,"units2":true,"ttl":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnskey/keyname_value&lt;String&gt;
<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###Import



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnskey?<b>action=Import</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"dnskey":{<b>"keyname":<String_value>,</b><b>"src":<String_value></b>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnskey
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnskey?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnskey?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of dnskey resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnskey?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnskey?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the dnskey resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "dnskey": [ {"keyname":<String_value>,"publickey":<String_value>,"privatekey":<String_value>,"expires":<Double_value>,"units1":<String_value>,"notificationperiod":<Double_value>,"units2":<String_value>,"ttl":<Double_value>,"zonename":<String_value>,"password":<String_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnskey/keyname_value&lt;String&gt;
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnskey/keyname_value&lt;String&gt;?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnskey/keyname_value&lt;String&gt;?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "dnskey": [ {"keyname":<String_value>,"publickey":<String_value>,"privatekey":<String_value>,"expires":<Double_value>,"units1":<String_value>,"notificationperiod":<Double_value>,"units2":<String_value>,"ttl":<Double_value>,"zonename":<String_value>,"password":<String_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnskey?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "dnskey": [ { "__count": "#no"} ] }```



