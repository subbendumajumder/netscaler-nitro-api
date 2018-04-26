#sslparameter

Configuration for SSL parameter resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>quantumsize</td><td>&lt;String></td><td>Read-write</td><td>Amount of data to collect before the data is pushed to the crypto hardware for encryption. For large downloads, a larger quantum size better utilizes the crypto resources.<br>Default value: 8192<br>Possible values = 4096, 8192, 16384</td></tr><tr><td>crlmemorysizemb</td><td>&lt;Double></td><td>Read-write</td><td>Maximum memory size to use for certificate revocation lists (CRLs). This parameter reserves memory for a CRL but sets a limit to the maximum memory that the CRLs loaded on the appliance can consume.<br>Default value: 256<br>Minimum value = 10<br>Maximum value = 1024</td></tr><tr><td>strictcachecks</td><td>&lt;String></td><td>Read-write</td><td>Enable strict CA certificate checks on the appliance.<br>Default value: NO<br>Possible values = YES, NO</td></tr><tr><td>ssltriggertimeout</td><td>&lt;Double></td><td>Read-write</td><td>Time, in milliseconds, after which encryption is triggered for transactions that are not tracked on the NetScaler appliance because their length is not known. There can be a delay of up to 10ms from the specified timeout value before the packet is pushed into the queue.<br>Default value: 100<br>Minimum value = 1<br>Maximum value = 200</td></tr><tr><td>sendclosenotify</td><td>&lt;String></td><td>Read-write</td><td>Send an SSL Close-Notify message to the client at the end of a transaction.<br>Default value: YES<br>Possible values = YES, NO</td></tr><tr><td>encrypttriggerpktcount</td><td>&lt;Double></td><td>Read-write</td><td>Maximum number of queued packets after which encryption is triggered. Use this setting for SSL transactions that send small packets from server to NetScaler.<br>Default value: 45<br>Minimum value = 10<br>Maximum value = 50</td></tr><tr><td>denysslreneg</td><td>&lt;String></td><td>Read-write</td><td>Deny renegotiation in specified circumstances. Available settings function as follows:<br>* NO - Allow SSL renegotiation.<br>* FRONTEND_CLIENT - Deny secure and nonsecure SSL renegotiation initiated by the client.<br>* FRONTEND_CLIENTSERVER - Deny secure and nonsecure SSL renegotiation initiated by the client or the NetScaler during policy-based client authentication. <br>* ALL - Deny all secure and nonsecure SSL renegotiation.<br>* NONSECURE - Deny nonsecure SSL renegotiation. Allows only clients that support RFC 5746.<br>Default value: ALL<br>Possible values = NO, FRONTEND_CLIENT, FRONTEND_CLIENTSERVER, ALL, NONSECURE</td></tr><tr><td>insertionencoding</td><td>&lt;String></td><td>Read-write</td><td>Encoding method used to insert the subject or issuer's name in HTTP requests to servers.<br>Default value: Unicode<br>Possible values = Unicode, UTF-8</td></tr><tr><td>ocspcachesize</td><td>&lt;Double></td><td>Read-write</td><td>Size, per packet engine, in megabytes, of the OCSP cache. A maximum of 10% of the packet engine memory can be assigned. Because the maximum allowed packet engine memory is 4GB, the maximum value that can be assigned to the OCSP cache is approximately 410 MB.<br>Default value: 10<br>Minimum value = 0<br>Maximum value = 512</td></tr><tr><td>pushflag</td><td>&lt;Double></td><td>Read-write</td><td>Insert PUSH flag into decrypted, encrypted, or all records. If the PUSH flag is set to a value other than 0, the buffered records are forwarded on the basis of the value of the PUSH flag. Available settings function as follows:<br>0 - Auto (PUSH flag is not set.)<br>1 - Insert PUSH flag into every decrypted record.<br>2 -Insert PUSH flag into every encrypted record.<br>3 - Insert PUSH flag into every decrypted and encrypted record.<br>Minimum value = 0<br>Maximum value = 3</td></tr><tr><td>dropreqwithnohostheader</td><td>&lt;String></td><td>Read-write</td><td>Host header check for SNI enabled sessions. If this check is enabled and the HTTP request does not contain the host header for SNI enabled sessions, the request is dropped.<br>Default value: NO<br>Possible values = YES, NO</td></tr><tr><td>pushenctriggertimeout</td><td>&lt;Double></td><td>Read-write</td><td>PUSH encryption trigger timeout value. The timeout value is applied only if you set the Push Encryption Trigger parameter to Timer in the SSL virtual server settings.<br>Default value: 1<br>Minimum value = 1<br>Maximum value = 200</td></tr><tr><td>cryptodevdisablelimit</td><td>&lt;Double></td><td>Read-write</td><td>Limit to the number of disabled SSL chips after which the ADC restarts. A value of zero implies that the ADC does not automatically restart.<br>Default value: 0</td></tr><tr><td>undefactioncontrol</td><td>&lt;String></td><td>Read-write</td><td>Name of the undefined built-in control action: CLIENTAUTH, NOCLIENTAUTH, NOOP, RESET, or DROP.<br>Default value: "CLIENTAUTH"</td></tr><tr><td>undefactiondata</td><td>&lt;String></td><td>Read-write</td><td>Name of the undefined built-in data action: NOOP, RESET or DROP.<br>Default value: "NOOP"</td></tr><tr><td>defaultprofile</td><td>&lt;String></td><td>Read-write</td><td>Global parameter used to enable default profile feature.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>softwarecryptothreshold</td><td>&lt;Double></td><td>Read-write</td><td>Netscaler CPU utilization threshold (in percentage) beyond which crypto operations are not done in software.<br>A value of zero implies that CPU is not utilized for doing crypto in software.<br>Default value: 0<br>Minimum value = 0<br>Maximum value = 100</td></tr><tr><td>hybridfipsmode</td><td>&lt;String></td><td>Read-write</td><td>When this mode is enabled, system will use additional crypto hardware to accelerate symmetric crypto operations.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>sigdigesttype</td><td>&lt;String[]></td><td>Read-write</td><td>Signature Digest Algorithms that are supported by appliance. Default value is "ALL" and it will enable the following algorithms depending on the platform.<br>On VPX: RSA-MD5 RSA-SHA1 RSA-SHA224 RSA-SHA256 RSA-SHA384 RSA-SHA512 DSA-SHA1 DSA-SHA224 DSA-SHA256 DSA-SHA384 DSA-SHA512<br>On MPX with Nitrox-III Cards: RSA-MD5 RSA-SHA1 RSA-SHA224 RSA-SHA256 RSA-SHA384 RSA-SHA512 ECDSA-SHA1 ECDSA-SHA224 ECDSA-SHA256 ECDSA-SHA384 ECDSA-SHA512<br>Others: RSA-MD5 RSA-SHA1 RSA-SHA224 RSA-SHA256 RSA-SHA384 RSA-SHA512.<br><br>Default value: ALL<br>Possible values = ALL, RSA-MD5, RSA-SHA1, RSA-SHA224, RSA-SHA256, RSA-SHA384, RSA-SHA512, DSA-SHA1, DSA-SHA224, DSA-SHA256, DSA-SHA384, DSA-SHA512, ECDSA-SHA1, ECDSA-SHA224, ECDSA-SHA256, ECDSA-SHA384, ECDSA-SHA512</td></tr><tr><td>sslierrorcache</td><td>&lt;String></td><td>Read-write</td><td>Enable or disable dynamically learning and caching the learned information to make the subsequent interception or bypass decision. When enabled, NS does the lookup of this cached data to do early bypass.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>sslimaxerrorcachemem</td><td>&lt;Double></td><td>Read-write</td><td>Specify the maximum memory that can be used for caching the learned data. This memory is used as a LRU cache so that the old entries gets replaced with new entry once the set memory limit is fully utilised. A value of 0 decides the limit automatically.<br>Default value: 0<br>Minimum value = 0<br>Maximum value = 4294967294</td></tr><tr><td>insertcertspace</td><td>&lt;String></td><td>Read-write</td><td>To insert space between lines in the certificate header of request.<br>Default value: YES<br>Possible values = YES, NO</td></tr><tr><td>svctls1112disable</td><td>&lt;String></td><td>Read-only</td><td>Disable TLS 1.1 and 1.2 for dynamic and VPN created services.<br>Default value: NO<br>Possible values = YES, NO</td></tr><tr><td>montls1112disable</td><td>&lt;String></td><td>Read-only</td><td>Disable TLS 1.1 and 1.2 for secure (https) monitors bound to SSL_BRIDGE services.<br>Default value: NO<br>Possible values = YES, NO</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[UPDATE](#u)| [UNSET](#)| [GET (ALL)](#get-)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslparameter
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"sslparameter":{"quantumsize":<String_value>,"crlmemorysizemb":<Double_value>,"strictcachecks":<String_value>,"ssltriggertimeout":<Double_value>,"sendclosenotify":<String_value>,"encrypttriggerpktcount":<Double_value>,"denysslreneg":<String_value>,"insertionencoding":<String_value>,"ocspcachesize":<Double_value>,"pushflag":<Double_value>,"dropreqwithnohostheader":<String_value>,"pushenctriggertimeout":<Double_value>,"cryptodevdisablelimit":<Double_value>,"undefactioncontrol":<String_value>,"undefactiondata":<String_value>,"defaultprofile":<String_value>,"softwarecryptothreshold":<Double_value>,"hybridfipsmode":<String_value>,"sigdigesttype":<String[]_value>,"sslierrorcache":<String_value>,"sslimaxerrorcachemem":<Double_value>,"insertcertspace":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslparameter?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"sslparameter":{"quantumsize":true,"crlmemorysizemb":true,"strictcachecks":true,"ssltriggertimeout":true,"sendclosenotify":true,"encrypttriggerpktcount":true,"denysslreneg":true,"insertionencoding":true,"ocspcachesize":true,"pushflag":true,"dropreqwithnohostheader":true,"pushenctriggertimeout":true,"cryptodevdisablelimit":true,"undefactioncontrol":true,"undefactiondata":true,"defaultprofile":true,"softwarecryptothreshold":true,"hybridfipsmode":true,"sigdigesttype":true,"sslierrorcache":true,"sslimaxerrorcachemem":true,"insertcertspace":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslparameter
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "sslparameter": [ {"quantumsize":<String_value>,"crlmemorysizemb":<Double_value>,"strictcachecks":<String_value>,"ssltriggertimeout":<Double_value>,"sendclosenotify":<String_value>,"encrypttriggerpktcount":<Double_value>,"denysslreneg":<String_value>,"insertionencoding":<String_value>,"ocspcachesize":<Double_value>,"pushflag":<Double_value>,"dropreqwithnohostheader":<String_value>,"pushenctriggertimeout":<Double_value>,"cryptodevdisablelimit":<Double_value>,"undefactioncontrol":<String_value>,"undefactiondata":<String_value>,"defaultprofile":<String_value>,"svctls1112disable":<String_value>,"montls1112disable":<String_value>,"softwarecryptothreshold":<Double_value>,"hybridfipsmode":<String_value>,"sigdigesttype":<String[]_value>,"sslierrorcache":<String_value>,"sslimaxerrorcachemem":<Double_value>,"insertcertspace":<String_value>}]}```



