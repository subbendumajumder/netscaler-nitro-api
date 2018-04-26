#vpnsamlssoprofile

Configuration for SAML sso action resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the new saml single sign-on profile. Must begin with an ASCII alphanumeric or underscore (_) character, and must contain only ASCII alphanumeric, underscore, hash (#), period (.), space, colon (:), at (@), equals (=), and hyphen (-) characters. Cannot be changed after an SSO action is created.<br><br>The following requirement applies only to the NetScaler CLI:<br>If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my action" or 'my action').<br>Minimum length = 1</td></tr><tr><td>samlsigningcertname</td><td>&lt;String></td><td>Read-write</td><td>Name of the signing authority as given in the SAML server's SSL certificate.<br>Minimum length = 1</td></tr><tr><td>assertionconsumerserviceurl</td><td>&lt;String></td><td>Read-write</td><td>URL to which the assertion is to be sent.<br>Minimum length = 1</td></tr><tr><td>relaystaterule</td><td>&lt;String></td><td>Read-write</td><td>Expression to extract relaystate to be sent along with assertion. Evaluation of this expression should return TEXT content. This is typically a target url to which user is redirected after the recipient validates SAML token.</td></tr><tr><td>sendpassword</td><td>&lt;String></td><td>Read-write</td><td>Option to send password in assertion.<br>Default value: OFF<br>Possible values = ON, OFF</td></tr><tr><td>samlissuername</td><td>&lt;String></td><td>Read-write</td><td>The name to be used in requests sent from Netscaler to IdP to uniquely identify Netscaler.<br>Minimum length = 1</td></tr><tr><td>signaturealg</td><td>&lt;String></td><td>Read-write</td><td>Algorithm to be used to sign/verify SAML transactions.<br>Default value: RSA-SHA1<br>Possible values = RSA-SHA1, RSA-SHA256</td></tr><tr><td>digestmethod</td><td>&lt;String></td><td>Read-write</td><td>Algorithm to be used to compute/verify digest for SAML transactions.<br>Default value: SHA1<br>Possible values = SHA1, SHA256</td></tr><tr><td>audience</td><td>&lt;String></td><td>Read-write</td><td>Audience for which assertion sent by IdP is applicable. This is typically entity name or url that represents ServiceProvider.</td></tr><tr><td>nameidformat</td><td>&lt;String></td><td>Read-write</td><td>Format of Name Identifier sent in Assertion.<br>Default value: transient<br>Possible values = Unspecified, emailAddress, X509SubjectName, WindowsDomainQualifiedName, kerberos, entity, persistent, transient</td></tr><tr><td>nameidexpr</td><td>&lt;String></td><td>Read-write</td><td>Expression that will be evaluated to obtain NameIdentifier to be sent in assertion.<br>Maximum length = 128</td></tr><tr><td>attribute1</td><td>&lt;String></td><td>Read-write</td><td>Name of attribute1 that needs to be sent in SAML Assertion.</td></tr><tr><td>attribute1expr</td><td>&lt;String></td><td>Read-write</td><td>Expression that will be evaluated to obtain attribute1's value to be sent in Assertion.<br>Maximum length = 128</td></tr><tr><td>attribute1friendlyname</td><td>&lt;String></td><td>Read-write</td><td>User-Friendly Name of attribute1 that needs to be sent in SAML Assertion.</td></tr><tr><td>attribute1format</td><td>&lt;String></td><td>Read-write</td><td>Format of Attribute1 to be sent in Assertion.<br>Possible values = URI, Basic</td></tr><tr><td>attribute2</td><td>&lt;String></td><td>Read-write</td><td>Name of attribute2 that needs to be sent in SAML Assertion.</td></tr><tr><td>attribute2expr</td><td>&lt;String></td><td>Read-write</td><td>Expression that will be evaluated to obtain attribute2's value to be sent in Assertion.<br>Maximum length = 128</td></tr><tr><td>attribute2friendlyname</td><td>&lt;String></td><td>Read-write</td><td>User-Friendly Name of attribute2 that needs to be sent in SAML Assertion.</td></tr><tr><td>attribute2format</td><td>&lt;String></td><td>Read-write</td><td>Format of Attribute2 to be sent in Assertion.<br>Possible values = URI, Basic</td></tr><tr><td>attribute3</td><td>&lt;String></td><td>Read-write</td><td>Name of attribute3 that needs to be sent in SAML Assertion.</td></tr><tr><td>attribute3expr</td><td>&lt;String></td><td>Read-write</td><td>Expression that will be evaluated to obtain attribute3's value to be sent in Assertion.<br>Maximum length = 128</td></tr><tr><td>attribute3friendlyname</td><td>&lt;String></td><td>Read-write</td><td>User-Friendly Name of attribute3 that needs to be sent in SAML Assertion.</td></tr><tr><td>attribute3format</td><td>&lt;String></td><td>Read-write</td><td>Format of Attribute3 to be sent in Assertion.<br>Possible values = URI, Basic</td></tr><tr><td>attribute4</td><td>&lt;String></td><td>Read-write</td><td>Name of attribute4 that needs to be sent in SAML Assertion.</td></tr><tr><td>attribute4expr</td><td>&lt;String></td><td>Read-write</td><td>Expression that will be evaluated to obtain attribute4's value to be sent in Assertion.<br>Maximum length = 128</td></tr><tr><td>attribute4friendlyname</td><td>&lt;String></td><td>Read-write</td><td>User-Friendly Name of attribute4 that needs to be sent in SAML Assertion.</td></tr><tr><td>attribute4format</td><td>&lt;String></td><td>Read-write</td><td>Format of Attribute4 to be sent in Assertion.<br>Possible values = URI, Basic</td></tr><tr><td>attribute5</td><td>&lt;String></td><td>Read-write</td><td>Name of attribute5 that needs to be sent in SAML Assertion.</td></tr><tr><td>attribute5expr</td><td>&lt;String></td><td>Read-write</td><td>Expression that will be evaluated to obtain attribute5's value to be sent in Assertion.<br>Maximum length = 128</td></tr><tr><td>attribute5friendlyname</td><td>&lt;String></td><td>Read-write</td><td>User-Friendly Name of attribute5 that needs to be sent in SAML Assertion.</td></tr><tr><td>attribute5format</td><td>&lt;String></td><td>Read-write</td><td>Format of Attribute5 to be sent in Assertion.<br>Possible values = URI, Basic</td></tr><tr><td>attribute6</td><td>&lt;String></td><td>Read-write</td><td>Name of attribute6 that needs to be sent in SAML Assertion.</td></tr><tr><td>attribute6expr</td><td>&lt;String></td><td>Read-write</td><td>Expression that will be evaluated to obtain attribute6's value to be sent in Assertion.<br>Maximum length = 128</td></tr><tr><td>attribute6friendlyname</td><td>&lt;String></td><td>Read-write</td><td>User-Friendly Name of attribute6 that needs to be sent in SAML Assertion.</td></tr><tr><td>attribute6format</td><td>&lt;String></td><td>Read-write</td><td>Format of Attribute6 to be sent in Assertion.<br>Possible values = URI, Basic</td></tr><tr><td>attribute7</td><td>&lt;String></td><td>Read-write</td><td>Name of attribute7 that needs to be sent in SAML Assertion.</td></tr><tr><td>attribute7expr</td><td>&lt;String></td><td>Read-write</td><td>Expression that will be evaluated to obtain attribute7's value to be sent in Assertion.<br>Maximum length = 128</td></tr><tr><td>attribute7friendlyname</td><td>&lt;String></td><td>Read-write</td><td>User-Friendly Name of attribute7 that needs to be sent in SAML Assertion.</td></tr><tr><td>attribute7format</td><td>&lt;String></td><td>Read-write</td><td>Format of Attribute7 to be sent in Assertion.<br>Possible values = URI, Basic</td></tr><tr><td>attribute8</td><td>&lt;String></td><td>Read-write</td><td>Name of attribute8 that needs to be sent in SAML Assertion.</td></tr><tr><td>attribute8expr</td><td>&lt;String></td><td>Read-write</td><td>Expression that will be evaluated to obtain attribute8's value to be sent in Assertion.<br>Maximum length = 128</td></tr><tr><td>attribute8friendlyname</td><td>&lt;String></td><td>Read-write</td><td>User-Friendly Name of attribute8 that needs to be sent in SAML Assertion.</td></tr><tr><td>attribute8format</td><td>&lt;String></td><td>Read-write</td><td>Format of Attribute8 to be sent in Assertion.<br>Possible values = URI, Basic</td></tr><tr><td>attribute9</td><td>&lt;String></td><td>Read-write</td><td>Name of attribute9 that needs to be sent in SAML Assertion.</td></tr><tr><td>attribute9expr</td><td>&lt;String></td><td>Read-write</td><td>Expression that will be evaluated to obtain attribute9's value to be sent in Assertion.<br>Maximum length = 128</td></tr><tr><td>attribute9friendlyname</td><td>&lt;String></td><td>Read-write</td><td>User-Friendly Name of attribute9 that needs to be sent in SAML Assertion.</td></tr><tr><td>attribute9format</td><td>&lt;String></td><td>Read-write</td><td>Format of Attribute9 to be sent in Assertion.<br>Possible values = URI, Basic</td></tr><tr><td>attribute10</td><td>&lt;String></td><td>Read-write</td><td>Name of attribute10 that needs to be sent in SAML Assertion.</td></tr><tr><td>attribute10expr</td><td>&lt;String></td><td>Read-write</td><td>Expression that will be evaluated to obtain attribute10's value to be sent in Assertion.<br>Maximum length = 128</td></tr><tr><td>attribute10friendlyname</td><td>&lt;String></td><td>Read-write</td><td>User-Friendly Name of attribute10 that needs to be sent in SAML Assertion.</td></tr><tr><td>attribute10format</td><td>&lt;String></td><td>Read-write</td><td>Format of Attribute10 to be sent in Assertion.<br>Possible values = URI, Basic</td></tr><tr><td>attribute11</td><td>&lt;String></td><td>Read-write</td><td>Name of attribute11 that needs to be sent in SAML Assertion.</td></tr><tr><td>attribute11expr</td><td>&lt;String></td><td>Read-write</td><td>Expression that will be evaluated to obtain attribute11's value to be sent in Assertion.<br>Maximum length = 128</td></tr><tr><td>attribute11friendlyname</td><td>&lt;String></td><td>Read-write</td><td>User-Friendly Name of attribute11 that needs to be sent in SAML Assertion.</td></tr><tr><td>attribute11format</td><td>&lt;String></td><td>Read-write</td><td>Format of Attribute11 to be sent in Assertion.<br>Possible values = URI, Basic</td></tr><tr><td>attribute12</td><td>&lt;String></td><td>Read-write</td><td>Name of attribute12 that needs to be sent in SAML Assertion.</td></tr><tr><td>attribute12expr</td><td>&lt;String></td><td>Read-write</td><td>Expression that will be evaluated to obtain attribute12's value to be sent in Assertion.<br>Maximum length = 128</td></tr><tr><td>attribute12friendlyname</td><td>&lt;String></td><td>Read-write</td><td>User-Friendly Name of attribute12 that needs to be sent in SAML Assertion.</td></tr><tr><td>attribute12format</td><td>&lt;String></td><td>Read-write</td><td>Format of Attribute12 to be sent in Assertion.<br>Possible values = URI, Basic</td></tr><tr><td>attribute13</td><td>&lt;String></td><td>Read-write</td><td>Name of attribute13 that needs to be sent in SAML Assertion.</td></tr><tr><td>attribute13expr</td><td>&lt;String></td><td>Read-write</td><td>Expression that will be evaluated to obtain attribute13's value to be sent in Assertion.<br>Maximum length = 128</td></tr><tr><td>attribute13friendlyname</td><td>&lt;String></td><td>Read-write</td><td>User-Friendly Name of attribute13 that needs to be sent in SAML Assertion.</td></tr><tr><td>attribute13format</td><td>&lt;String></td><td>Read-write</td><td>Format of Attribute13 to be sent in Assertion.<br>Possible values = URI, Basic</td></tr><tr><td>attribute14</td><td>&lt;String></td><td>Read-write</td><td>Name of attribute14 that needs to be sent in SAML Assertion.</td></tr><tr><td>attribute14expr</td><td>&lt;String></td><td>Read-write</td><td>Expression that will be evaluated to obtain attribute14's value to be sent in Assertion.<br>Maximum length = 128</td></tr><tr><td>attribute14friendlyname</td><td>&lt;String></td><td>Read-write</td><td>User-Friendly Name of attribute14 that needs to be sent in SAML Assertion.</td></tr><tr><td>attribute14format</td><td>&lt;String></td><td>Read-write</td><td>Format of Attribute14 to be sent in Assertion.<br>Possible values = URI, Basic</td></tr><tr><td>attribute15</td><td>&lt;String></td><td>Read-write</td><td>Name of attribute15 that needs to be sent in SAML Assertion.</td></tr><tr><td>attribute15expr</td><td>&lt;String></td><td>Read-write</td><td>Expression that will be evaluated to obtain attribute15's value to be sent in Assertion.<br>Maximum length = 128</td></tr><tr><td>attribute15friendlyname</td><td>&lt;String></td><td>Read-write</td><td>User-Friendly Name of attribute15 that needs to be sent in SAML Assertion.</td></tr><tr><td>attribute15format</td><td>&lt;String></td><td>Read-write</td><td>Format of Attribute15 to be sent in Assertion.<br>Possible values = URI, Basic</td></tr><tr><td>attribute16</td><td>&lt;String></td><td>Read-write</td><td>Name of attribute16 that needs to be sent in SAML Assertion.</td></tr><tr><td>attribute16expr</td><td>&lt;String></td><td>Read-write</td><td>Expression that will be evaluated to obtain attribute16's value to be sent in Assertion.<br>Maximum length = 128</td></tr><tr><td>attribute16friendlyname</td><td>&lt;String></td><td>Read-write</td><td>User-Friendly Name of attribute16 that needs to be sent in SAML Assertion.</td></tr><tr><td>attribute16format</td><td>&lt;String></td><td>Read-write</td><td>Format of Attribute16 to be sent in Assertion.<br>Possible values = URI, Basic</td></tr><tr><td>encryptassertion</td><td>&lt;String></td><td>Read-write</td><td>Option to encrypt assertion when Netscaler sends one.<br>Default value: OFF<br>Possible values = ON, OFF</td></tr><tr><td>samlspcertname</td><td>&lt;String></td><td>Read-write</td><td>Name of the SSL certificate of peer/receving party using which Assertion is encrypted.<br>Minimum length = 1</td></tr><tr><td>encryptionalgorithm</td><td>&lt;String></td><td>Read-write</td><td>Algorithm to be used to encrypt SAML assertion.<br>Default value: AES256<br>Possible values = DES3, AES128, AES192, AES256</td></tr><tr><td>skewtime</td><td>&lt;Double></td><td>Read-write</td><td>This option specifies the number of minutes on either side of current time that the assertion would be valid. For example, if skewTime is 10, then assertion would be valid from (current time - 10) min to (current time + 10) min, ie 20min in all.<br>Default value: 5</td></tr><tr><td>signassertion</td><td>&lt;String></td><td>Read-write</td><td>Option to sign portions of assertion when Netscaler IDP sends one. Based on the user selection, either Assertion or Response or Both or none can be signed.<br>Default value: ASSERTION<br>Possible values = NONE, ASSERTION, RESPONSE, BOTH</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD]()| [DELETE](#d)| [UPDATE](#u)| [UNSET](#)| [GET (ALL)](#get-)| [GET]()| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnsamlssoprofile
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"vpnsamlssoprofile":{<b>"name":<String_value>,</b>"samlsigningcertname":<String_value>,<b>"assertionconsumerserviceurl":<String_value>,</b><b>"relaystaterule":<String_value>,</b>"sendpassword":<String_value>,"samlissuername":<String_value>,"signaturealg":<String_value>,"digestmethod":<String_value>,"audience":<String_value>,"nameidformat":<String_value>,"nameidexpr":<String_value>,"attribute1":<String_value>,"attribute1expr":<String_value>,"attribute1friendlyname":<String_value>,"attribute1format":<String_value>,"attribute2":<String_value>,"attribute2expr":<String_value>,"attribute2friendlyname":<String_value>,"attribute2format":<String_value>,"attribute3":<String_value>,"attribute3expr":<String_value>,"attribute3friendlyname":<String_value>,"attribute3format":<String_value>,"attribute4":<String_value>,"attribute4expr":<String_value>,"attribute4friendlyname":<String_value>,"attribute4format":<String_value>,"attribute5":<String_value>,"attribute5expr":<String_value>,"attribute5friendlyname":<String_value>,"attribute5format":<String_value>,"attribute6":<String_value>,"attribute6expr":<String_value>,"attribute6friendlyname":<String_value>,"attribute6format":<String_value>,"attribute7":<String_value>,"attribute7expr":<String_value>,"attribute7friendlyname":<String_value>,"attribute7format":<String_value>,"attribute8":<String_value>,"attribute8expr":<String_value>,"attribute8friendlyname":<String_value>,"attribute8format":<String_value>,"attribute9":<String_value>,"attribute9expr":<String_value>,"attribute9friendlyname":<String_value>,"attribute9format":<String_value>,"attribute10":<String_value>,"attribute10expr":<String_value>,"attribute10friendlyname":<String_value>,"attribute10format":<String_value>,"attribute11":<String_value>,"attribute11expr":<String_value>,"attribute11friendlyname":<String_value>,"attribute11format":<String_value>,"attribute12":<String_value>,"attribute12expr":<String_value>,"attribute12friendlyname":<String_value>,"attribute12format":<String_value>,"attribute13":<String_value>,"attribute13expr":<String_value>,"attribute13friendlyname":<String_value>,"attribute13format":<String_value>,"attribute14":<String_value>,"attribute14expr":<String_value>,"attribute14friendlyname":<String_value>,"attribute14format":<String_value>,"attribute15":<String_value>,"attribute15expr":<String_value>,"attribute15friendlyname":<String_value>,"attribute15format":<String_value>,"attribute16":<String_value>,"attribute16expr":<String_value>,"attribute16friendlyname":<String_value>,"attribute16format":<String_value>,"encryptassertion":<String_value>,"samlspcertname":<String_value>,"encryptionalgorithm":<String_value>,"skewtime":<Double_value>,"signassertion":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnsamlssoprofile/name_value&lt;String&gt;
<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnsamlssoprofile
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"vpnsamlssoprofile":{<b>"name":<String_value>,</b>"samlsigningcertname":<String_value>,"assertionconsumerserviceurl":<String_value>,"sendpassword":<String_value>,"samlissuername":<String_value>,"relaystaterule":<String_value>,"signaturealg":<String_value>,"digestmethod":<String_value>,"audience":<String_value>,"nameidformat":<String_value>,"nameidexpr":<String_value>,"attribute1":<String_value>,"attribute1expr":<String_value>,"attribute1friendlyname":<String_value>,"attribute1format":<String_value>,"attribute2":<String_value>,"attribute2expr":<String_value>,"attribute2friendlyname":<String_value>,"attribute2format":<String_value>,"attribute3":<String_value>,"attribute3expr":<String_value>,"attribute3friendlyname":<String_value>,"attribute3format":<String_value>,"attribute4":<String_value>,"attribute4expr":<String_value>,"attribute4friendlyname":<String_value>,"attribute4format":<String_value>,"attribute5":<String_value>,"attribute5expr":<String_value>,"attribute5friendlyname":<String_value>,"attribute5format":<String_value>,"attribute6":<String_value>,"attribute6expr":<String_value>,"attribute6friendlyname":<String_value>,"attribute6format":<String_value>,"attribute7":<String_value>,"attribute7expr":<String_value>,"attribute7friendlyname":<String_value>,"attribute7format":<String_value>,"attribute8":<String_value>,"attribute8expr":<String_value>,"attribute8friendlyname":<String_value>,"attribute8format":<String_value>,"attribute9":<String_value>,"attribute9expr":<String_value>,"attribute9friendlyname":<String_value>,"attribute9format":<String_value>,"attribute10":<String_value>,"attribute10expr":<String_value>,"attribute10friendlyname":<String_value>,"attribute10format":<String_value>,"attribute11":<String_value>,"attribute11expr":<String_value>,"attribute11friendlyname":<String_value>,"attribute11format":<String_value>,"attribute12":<String_value>,"attribute12expr":<String_value>,"attribute12friendlyname":<String_value>,"attribute12format":<String_value>,"attribute13":<String_value>,"attribute13expr":<String_value>,"attribute13friendlyname":<String_value>,"attribute13format":<String_value>,"attribute14":<String_value>,"attribute14expr":<String_value>,"attribute14friendlyname":<String_value>,"attribute14format":<String_value>,"attribute15":<String_value>,"attribute15expr":<String_value>,"attribute15friendlyname":<String_value>,"attribute15format":<String_value>,"attribute16":<String_value>,"attribute16expr":<String_value>,"attribute16friendlyname":<String_value>,"attribute16format":<String_value>,"encryptassertion":<String_value>,"samlspcertname":<String_value>,"encryptionalgorithm":<String_value>,"skewtime":<Double_value>,"signassertion":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnsamlssoprofile?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"vpnsamlssoprofile":{<b>"name":<String_value>,</b>"samlsigningcertname":true,"sendpassword":true,"samlissuername":true,"signaturealg":true,"digestmethod":true,"audience":true,"nameidformat":true,"nameidexpr":true,"attribute1":true,"attribute1friendlyname":true,"attribute1format":true,"attribute2":true,"attribute2friendlyname":true,"attribute2format":true,"attribute3":true,"attribute3friendlyname":true,"attribute3format":true,"attribute4":true,"attribute4friendlyname":true,"attribute4format":true,"attribute5":true,"attribute5friendlyname":true,"attribute5format":true,"attribute6":true,"attribute6friendlyname":true,"attribute6format":true,"attribute7":true,"attribute7friendlyname":true,"attribute7format":true,"attribute8":true,"attribute8friendlyname":true,"attribute8format":true,"attribute9":true,"attribute9friendlyname":true,"attribute9format":true,"attribute10":true,"attribute10friendlyname":true,"attribute10format":true,"attribute11":true,"attribute11friendlyname":true,"attribute11format":true,"attribute12":true,"attribute12friendlyname":true,"attribute12format":true,"attribute13":true,"attribute13friendlyname":true,"attribute13format":true,"attribute14":true,"attribute14friendlyname":true,"attribute14format":true,"attribute15":true,"attribute15friendlyname":true,"attribute15format":true,"attribute16":true,"attribute16friendlyname":true,"attribute16format":true,"encryptassertion":true,"samlspcertname":true,"encryptionalgorithm":true,"skewtime":true,"signassertion":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnsamlssoprofile
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnsamlssoprofile?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnsamlssoprofile?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of vpnsamlssoprofile resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnsamlssoprofile?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnsamlssoprofile?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the vpnsamlssoprofile resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "vpnsamlssoprofile": [ {"name":<String_value>,"samlsigningcertname":<String_value>,"assertionconsumerserviceurl":<String_value>,"sendpassword":<String_value>,"samlissuername":<String_value>,"relaystaterule":<String_value>,"signaturealg":<String_value>,"digestmethod":<String_value>,"audience":<String_value>,"nameidformat":<String_value>,"nameidexpr":<String_value>,"attribute1":<String_value>,"attribute2":<String_value>,"attribute3":<String_value>,"attribute4":<String_value>,"attribute5":<String_value>,"attribute6":<String_value>,"attribute7":<String_value>,"attribute8":<String_value>,"attribute9":<String_value>,"attribute10":<String_value>,"attribute11":<String_value>,"attribute12":<String_value>,"attribute13":<String_value>,"attribute14":<String_value>,"attribute15":<String_value>,"attribute16":<String_value>,"attribute1friendlyname":<String_value>,"attribute2friendlyname":<String_value>,"attribute3friendlyname":<String_value>,"attribute4friendlyname":<String_value>,"attribute5friendlyname":<String_value>,"attribute6friendlyname":<String_value>,"attribute7friendlyname":<String_value>,"attribute8friendlyname":<String_value>,"attribute9friendlyname":<String_value>,"attribute10friendlyname":<String_value>,"attribute11friendlyname":<String_value>,"attribute12friendlyname":<String_value>,"attribute13friendlyname":<String_value>,"attribute14friendlyname":<String_value>,"attribute15friendlyname":<String_value>,"attribute16friendlyname":<String_value>,"attribute1format":<String_value>,"attribute2format":<String_value>,"attribute3format":<String_value>,"attribute4format":<String_value>,"attribute5format":<String_value>,"attribute6format":<String_value>,"attribute7format":<String_value>,"attribute8format":<String_value>,"attribute9format":<String_value>,"attribute10format":<String_value>,"attribute11format":<String_value>,"attribute12format":<String_value>,"attribute13format":<String_value>,"attribute14format":<String_value>,"attribute15format":<String_value>,"attribute16format":<String_value>,"attribute1expr":<String_value>,"attribute2expr":<String_value>,"attribute3expr":<String_value>,"attribute4expr":<String_value>,"attribute5expr":<String_value>,"attribute6expr":<String_value>,"attribute7expr":<String_value>,"attribute8expr":<String_value>,"attribute9expr":<String_value>,"attribute10expr":<String_value>,"attribute11expr":<String_value>,"attribute12expr":<String_value>,"attribute13expr":<String_value>,"attribute14expr":<String_value>,"attribute15expr":<String_value>,"attribute16expr":<String_value>,"encryptassertion":<String_value>,"samlspcertname":<String_value>,"encryptionalgorithm":<String_value>,"skewtime":<Double_value>,"signassertion":<String_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnsamlssoprofile/name_value&lt;String&gt;
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnsamlssoprofile/name_value&lt;String&gt;?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnsamlssoprofile/name_value&lt;String&gt;?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "vpnsamlssoprofile": [ {"name":<String_value>,"samlsigningcertname":<String_value>,"assertionconsumerserviceurl":<String_value>,"sendpassword":<String_value>,"samlissuername":<String_value>,"relaystaterule":<String_value>,"signaturealg":<String_value>,"digestmethod":<String_value>,"audience":<String_value>,"nameidformat":<String_value>,"nameidexpr":<String_value>,"attribute1":<String_value>,"attribute2":<String_value>,"attribute3":<String_value>,"attribute4":<String_value>,"attribute5":<String_value>,"attribute6":<String_value>,"attribute7":<String_value>,"attribute8":<String_value>,"attribute9":<String_value>,"attribute10":<String_value>,"attribute11":<String_value>,"attribute12":<String_value>,"attribute13":<String_value>,"attribute14":<String_value>,"attribute15":<String_value>,"attribute16":<String_value>,"attribute1friendlyname":<String_value>,"attribute2friendlyname":<String_value>,"attribute3friendlyname":<String_value>,"attribute4friendlyname":<String_value>,"attribute5friendlyname":<String_value>,"attribute6friendlyname":<String_value>,"attribute7friendlyname":<String_value>,"attribute8friendlyname":<String_value>,"attribute9friendlyname":<String_value>,"attribute10friendlyname":<String_value>,"attribute11friendlyname":<String_value>,"attribute12friendlyname":<String_value>,"attribute13friendlyname":<String_value>,"attribute14friendlyname":<String_value>,"attribute15friendlyname":<String_value>,"attribute16friendlyname":<String_value>,"attribute1format":<String_value>,"attribute2format":<String_value>,"attribute3format":<String_value>,"attribute4format":<String_value>,"attribute5format":<String_value>,"attribute6format":<String_value>,"attribute7format":<String_value>,"attribute8format":<String_value>,"attribute9format":<String_value>,"attribute10format":<String_value>,"attribute11format":<String_value>,"attribute12format":<String_value>,"attribute13format":<String_value>,"attribute14format":<String_value>,"attribute15format":<String_value>,"attribute16format":<String_value>,"attribute1expr":<String_value>,"attribute2expr":<String_value>,"attribute3expr":<String_value>,"attribute4expr":<String_value>,"attribute5expr":<String_value>,"attribute6expr":<String_value>,"attribute7expr":<String_value>,"attribute8expr":<String_value>,"attribute9expr":<String_value>,"attribute10expr":<String_value>,"attribute11expr":<String_value>,"attribute12expr":<String_value>,"attribute13expr":<String_value>,"attribute14expr":<String_value>,"attribute15expr":<String_value>,"attribute16expr":<String_value>,"encryptassertion":<String_value>,"samlspcertname":<String_value>,"encryptionalgorithm":<String_value>,"skewtime":<Double_value>,"signassertion":<String_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnsamlssoprofile?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "vpnsamlssoprofile": [ { "__count": "#no"} ] }```



