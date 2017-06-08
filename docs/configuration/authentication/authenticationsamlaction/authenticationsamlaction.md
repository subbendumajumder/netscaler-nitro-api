#authenticationsamlaction

Configuration for AAA Saml action resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the SAML server profile (action). Must begin with a letter, number, or the underscore character (_), and must contain only letters, numbers, and the hyphen (-), period (.) pound (#), space ( ), at (@), equals (=), colon (:), and underscore characters. Cannot be changed after SAML profile is created. The following requirement applies only to the NetScaler CLI: If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, ?my authentication action? or ?my authentication action?).&lt;br>Minimum length = 1</td><tr><tr><td>samlidpcertname</td><td>&lt;String></td><td>Read-write</td><td>Name of the SAML server as given in that server?s SSL certificate.&lt;br>Minimum length = 1</td><tr><tr><td>samlsigningcertname</td><td>&lt;String></td><td>Read-write</td><td>Name of the signing authority as given in the SAML server?s SSL certificate.&lt;br>Minimum length = 1</td><tr><tr><td>samlredirecturl</td><td>&lt;String></td><td>Read-write</td><td>URL to which users are redirected for authentication.&lt;br>Minimum length = 1</td><tr><tr><td>samlacsindex</td><td>&lt;Double></td><td>Read-write</td><td>Index/ID of the metadata entry corresponding to this configuration.&lt;br>Default value: 255&lt;br>Minimum value = 0&lt;br>Maximum value = 255</td><tr><tr><td>samluserfield</td><td>&lt;String></td><td>Read-write</td><td>SAML user ID, as given in the SAML assertion.&lt;br>Minimum length = 1</td><tr><tr><td>samlrejectunsignedassertion</td><td>&lt;String></td><td>Read-write</td><td>Reject unsigned SAML assertions.&lt;br>Default value: ON&lt;br>Possible values = ON, OFF, STRICT</td><tr><tr><td>samlissuername</td><td>&lt;String></td><td>Read-write</td><td>The name to be used in requests sent from Netscaler to IdP to uniquely identify Netscaler.&lt;br>Minimum length = 1</td><tr><tr><td>samltwofactor</td><td>&lt;String></td><td>Read-write</td><td>Option to enable second factor after SAML.&lt;br>Default value: OFF&lt;br>Possible values = ON, OFF</td><tr><tr><td>defaultauthenticationgroup</td><td>&lt;String></td><td>Read-write</td><td>This is the default group that is chosen when the authentication succeeds in addition to extracted groups.&lt;br>Maximum length = 64</td><tr><tr><td>attribute1</td><td>&lt;String></td><td>Read-write</td><td>Name of the attribute in SAML Assertion whose value needs to be extracted and stored as attribute1.&lt;br>Maximum length = 64</td><tr><tr><td>attribute2</td><td>&lt;String></td><td>Read-write</td><td>Name of the attribute in SAML Assertion whose value needs to be extracted and stored as attribute2.&lt;br>Maximum length = 64</td><tr><tr><td>attribute3</td><td>&lt;String></td><td>Read-write</td><td>Name of the attribute in SAML Assertion whose value needs to be extracted and stored as attribute3.&lt;br>Maximum length = 64</td><tr><tr><td>attribute4</td><td>&lt;String></td><td>Read-write</td><td>Name of the attribute in SAML Assertion whose value needs to be extracted and stored as attribute4.&lt;br>Maximum length = 64</td><tr><tr><td>attribute5</td><td>&lt;String></td><td>Read-write</td><td>Name of the attribute in SAML Assertion whose value needs to be extracted and stored as attribute5.&lt;br>Maximum length = 64</td><tr><tr><td>attribute6</td><td>&lt;String></td><td>Read-write</td><td>Name of the attribute in SAML Assertion whose value needs to be extracted and stored as attribute6.&lt;br>Maximum length = 64</td><tr><tr><td>attribute7</td><td>&lt;String></td><td>Read-write</td><td>Name of the attribute in SAML Assertion whose value needs to be extracted and stored as attribute7.&lt;br>Maximum length = 64</td><tr><tr><td>attribute8</td><td>&lt;String></td><td>Read-write</td><td>Name of the attribute in SAML Assertion whose value needs to be extracted and stored as attribute8.&lt;br>Maximum length = 64</td><tr><tr><td>attribute9</td><td>&lt;String></td><td>Read-write</td><td>Name of the attribute in SAML Assertion whose value needs to be extracted and stored as attribute9.&lt;br>Maximum length = 64</td><tr><tr><td>attribute10</td><td>&lt;String></td><td>Read-write</td><td>Name of the attribute in SAML Assertion whose value needs to be extracted and stored as attribute10.&lt;br>Maximum length = 64</td><tr><tr><td>attribute11</td><td>&lt;String></td><td>Read-write</td><td>Name of the attribute in SAML Assertion whose value needs to be extracted and stored as attribute11.&lt;br>Maximum length = 64</td><tr><tr><td>attribute12</td><td>&lt;String></td><td>Read-write</td><td>Name of the attribute in SAML Assertion whose value needs to be extracted and stored as attribute12.&lt;br>Maximum length = 64</td><tr><tr><td>attribute13</td><td>&lt;String></td><td>Read-write</td><td>Name of the attribute in SAML Assertion whose value needs to be extracted and stored as attribute13.&lt;br>Maximum length = 64</td><tr><tr><td>attribute14</td><td>&lt;String></td><td>Read-write</td><td>Name of the attribute in SAML Assertion whose value needs to be extracted and stored as attribute14.&lt;br>Maximum length = 64</td><tr><tr><td>attribute15</td><td>&lt;String></td><td>Read-write</td><td>Name of the attribute in SAML Assertion whose value needs to be extracted and stored as attribute15.&lt;br>Maximum length = 64</td><tr><tr><td>attribute16</td><td>&lt;String></td><td>Read-write</td><td>Name of the attribute in SAML Assertion whose value needs to be extracted and stored as attribute16.&lt;br>Maximum length = 64</td><tr><tr><td>signaturealg</td><td>&lt;String></td><td>Read-write</td><td>Algorithm to be used to sign/verify SAML transactions.&lt;br>Default value: RSA-SHA1&lt;br>Possible values = RSA-SHA1, RSA-SHA256</td><tr><tr><td>digestmethod</td><td>&lt;String></td><td>Read-write</td><td>Algorithm to be used to compute/verify digest for SAML transactions.&lt;br>Default value: SHA1&lt;br>Possible values = SHA1, SHA256</td><tr><tr><td>requestedauthncontext</td><td>&lt;String></td><td>Read-write</td><td>This element specifies the authentication context requirements of authentication statements returned in the response.&lt;br>Default value: exact&lt;br>Possible values = exact, minimum, maximum, better</td><tr><tr><td>authnctxclassref</td><td>&lt;String[]></td><td>Read-write</td><td>This element specifies the authentication class types that are requested from IdP (IdentityProvider). InternetProtocol: This is applicable when a principal is authenticated through the use of a provided IP address. InternetProtocolPassword: This is applicable when a principal is authenticated through the use of a provided IP address, in addition to a username/password. Kerberos: This is applicable when the principal has authenticated using a password to a local authentication authority, in order to acquire a Kerberos ticket. MobileOneFactorUnregistered: This indicates authentication of the mobile device without requiring explicit end-user interaction. MobileTwoFactorUnregistered: This indicates two-factor based authentication during mobile customer registration process, such as secure device and user PIN. MobileOneFactorContract: Reflects mobile contract customer registration procedures and a single factor authentication. MobileTwoFactorContract: Reflects mobile contract customer registration procedures and a two-factor based authentication. Password: This class is applicable when a principal authenticates using password over unprotected http session. PasswordProtectedTransport: This class is applicable when a principal authenticates to an authentication authority through the presentation of a password over a protected session. PreviousSession: This class is applicable when a principal had authenticated to an authentication authority at some point in the past using any authentication context. X509: This indicates that the principal authenticated by means of a digital signature where the key was validated as part of an X.509 Public Key Infrastructure. PGP: This indicates that the principal authenticated by means of a digital signature where the key was validated as part of a PGP Public Key Infrastructure. SPKI: This indicates that the principal authenticated by means of a digital signature where the key was validated via an SPKI Infrastructure. XMLDSig: This indicates that the principal authenticated by means of a digital signature according to the processing rules specified in the XML Digital Signature specification. Smartcard: This indicates that the principal has authenticated using smartcard. SmartcardPKI: This class is applicable when a principal authenticates to an authentication authority through a two-factor authentication mechanism using a smartcard with enclosed private key and a PIN. SoftwarePKI: This class is applicable when a principal uses an X.509 certificate stored in software to authenticate to the authentication authority. Telephony: This class is used to indicate that the principal authenticated via the provision of a fixed-line telephone number, transported via a telephony protocol such as ADSL. NomadTelephony: Indicates that the principal is "roaming" and authenticates via the means of the line number, a user suffix, and a password element. PersonalTelephony: This class is used to indicate that the principal authenticated via the provision of a fixed-line telephone. AuthenticatedTelephony: Indicates that the principal authenticated via the means of the line number, a user suffix, and a password element. SecureRemotePassword: This class is applicable when the authentication was performed by means of Secure Remote Password. TLSClient: This class indicates that the principal authenticated by means of a client certificate, secured with the SSL/TLS transport. TimeSyncToken: This is applicable when a principal authenticates through a time synchronization token. Unspecified: This indicates that the authentication was performed by unspecified means. Windows: This indicates that Windows integrated authentication is utilized for authentication.&lt;br>Possible values = InternetProtocol, InternetProtocolPassword, Kerberos, MobileOneFactorUnregistered, MobileTwoFactorUnregistered, MobileOneFactorContract, MobileTwoFactorContract, Password, PasswordProtectedTransport, PreviousSession, X509, PGP, SPKI, XMLDSig, Smartcard, SmartcardPKI, SoftwarePKI, Telephony, NomadTelephony, PersonalTelephony, AuthenticatedTelephony, SecureRemotePassword, TLSClient, TimeSyncToken, Unspecified, Windows</td><tr><tr><td>samlbinding</td><td>&lt;String></td><td>Read-write</td><td>This element specifies the transport mechanism of saml messages.&lt;br>Default value: POST&lt;br>Possible values = REDIRECT, POST</td><tr><tr><td>attributeconsumingserviceindex</td><td>&lt;Double></td><td>Read-write</td><td>Index/ID of the attribute specification at Identity Provider (IdP). IdP will locate attributes requested by SP using this index and send those attributes in Assertion.&lt;br>Default value: 255&lt;br>Minimum value = 0&lt;br>Maximum value = 255</td><tr><tr><td>sendthumbprint</td><td>&lt;String></td><td>Read-write</td><td>Option to send thumbprint instead of x509 certificate in SAML request.&lt;br>Default value: OFF&lt;br>Possible values = ON, OFF</td><tr><tr><td>logouturl</td><td>&lt;String></td><td>Read-write</td><td>SingleLogout URL on IdP to which logoutRequest will be sent on Netscaler session cleanup.&lt;br>Maximum length = 256</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
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
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>},"sessionid":"##sessionid","authenticationsamlaction":{      "name":<String_value>,      "samlidpcertname":<String_value>,      "samlsigningcertname":<String_value>,      "samlredirecturl":<String_value>,      "samlacsindex":<Double_value>,      "samluserfield":<String_value>,      "samlrejectunsignedassertion":<String_value>,      "samlissuername":<String_value>,      "samltwofactor":<String_value>,      "defaultauthenticationgroup":<String_value>,      "attribute1":<String_value>,      "attribute2":<String_value>,      "attribute3":<String_value>,      "attribute4":<String_value>,      "attribute5":<String_value>,      "attribute6":<String_value>,      "attribute7":<String_value>,      "attribute8":<String_value>,      "attribute9":<String_value>,      "attribute10":<String_value>,      "attribute11":<String_value>,      "attribute12":<String_value>,      "attribute13":<String_value>,      "attribute14":<String_value>,      "attribute15":<String_value>,      "attribute16":<String_value>,      "signaturealg":<String_value>,      "digestmethod":<String_value>,      "requestedauthncontext":<String_value>,      "authnctxclassref":<String[]_value>,      "samlbinding":<String_value>,      "attributeconsumingserviceindex":<Double_value>,      "sendthumbprint":<String_value>,      "logouturl":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/authenticationsamlaction/name_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/authenticationsamlaction/name_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","authenticationsamlaction":{      "name":<String_value>,      "samlidpcertname":<String_value>,      "samlsigningcertname":<String_value>,      "samlredirecturl":<String_value>,      "samlacsindex":<Double_value>,      "samluserfield":<String_value>,      "samlrejectunsignedassertion":<String_value>,      "samlissuername":<String_value>,      "samltwofactor":<String_value>,      "defaultauthenticationgroup":<String_value>,      "attribute1":<String_value>,      "attribute2":<String_value>,      "attribute3":<String_value>,      "attribute4":<String_value>,      "attribute5":<String_value>,      "attribute6":<String_value>,      "attribute7":<String_value>,      "attribute8":<String_value>,      "attribute9":<String_value>,      "attribute10":<String_value>,      "attribute11":<String_value>,      "attribute12":<String_value>,      "attribute13":<String_value>,      "attribute14":<String_value>,      "attribute15":<String_value>,      "attribute16":<String_value>,      "signaturealg":<String_value>,      "digestmethod":<String_value>,      "requestedauthncontext":<String_value>,      "authnctxclassref":<String[]_value>,      "samlbinding":<String_value>,      "attributeconsumingserviceindex":<Double_value>,      "sendthumbprint":<String_value>,      "logouturl":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","authenticationsamlaction":{      "name":<String_value>,      "samlidpcertname":true,      "samlsigningcertname":true,      "samlredirecturl":true,      "samlacsindex":true,      "samluserfield":true,      "samlrejectunsignedassertion":true,      "samlissuername":true,      "samltwofactor":true,      "defaultauthenticationgroup":true,      "attribute1":true,      "attribute2":true,      "attribute3":true,      "attribute4":true,      "attribute5":true,      "attribute6":true,      "attribute7":true,      "attribute8":true,      "attribute9":true,      "attribute10":true,      "attribute11":true,      "attribute12":true,      "attribute13":true,      "attribute14":true,      "attribute15":true,      "attribute16":true,      "signaturealg":true,      "digestmethod":true,      "requestedauthncontext":true,      "authnctxclassref":true,      "samlbinding":true,      "attributeconsumingserviceindex":true,      "sendthumbprint":true,      "logouturl":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/authenticationsamlaction
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/authenticationsamlaction?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of authenticationsamlaction resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/authenticationsamlaction?view=summary
Use this query-parameter to get the summary output of authenticationsamlaction resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/authenticationsamlaction?pagesize=#no;pageno=#no
Use this query-parameter to get the authenticationsamlaction resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/authenticationsamlaction?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "authenticationsamlaction": [ {      "name":<String_value>,      "samlidpcertname":<String_value>,      "samlsigningcertname":<String_value>,      "samlredirecturl":<String_value>,      "samlacsindex":<Double_value>,      "samluserfield":<String_value>,      "samlrejectunsignedassertion":<String_value>,      "samlissuername":<String_value>,      "samltwofactor":<String_value>,      "defaultauthenticationgroup":<String_value>,      "attribute1":<String_value>,      "attribute2":<String_value>,      "attribute3":<String_value>,      "attribute4":<String_value>,      "attribute5":<String_value>,      "attribute6":<String_value>,      "attribute7":<String_value>,      "attribute8":<String_value>,      "attribute9":<String_value>,      "attribute10":<String_value>,      "attribute11":<String_value>,      "attribute12":<String_value>,      "attribute13":<String_value>,      "attribute14":<String_value>,      "attribute15":<String_value>,      "attribute16":<String_value>,      "signaturealg":<String_value>,      "digestmethod":<String_value>,      "requestedauthncontext":<String_value>,      "authnctxclassref":<String[]_value>,      "samlbinding":<String_value>,      "attributeconsumingserviceindex":<Double_value>,      "sendthumbprint":<String_value>,      "logouturl":<String_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/authenticationsamlaction/name_value&lt;String&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "authenticationsamlaction": [ {      "name":<String_value>,      "samlidpcertname":<String_value>,      "samlsigningcertname":<String_value>,      "samlredirecturl":<String_value>,      "samlacsindex":<Double_value>,      "samluserfield":<String_value>,      "samlrejectunsignedassertion":<String_value>,      "samlissuername":<String_value>,      "samltwofactor":<String_value>,      "defaultauthenticationgroup":<String_value>,      "attribute1":<String_value>,      "attribute2":<String_value>,      "attribute3":<String_value>,      "attribute4":<String_value>,      "attribute5":<String_value>,      "attribute6":<String_value>,      "attribute7":<String_value>,      "attribute8":<String_value>,      "attribute9":<String_value>,      "attribute10":<String_value>,      "attribute11":<String_value>,      "attribute12":<String_value>,      "attribute13":<String_value>,      "attribute14":<String_value>,      "attribute15":<String_value>,      "attribute16":<String_value>,      "signaturealg":<String_value>,      "digestmethod":<String_value>,      "requestedauthncontext":<String_value>,      "authnctxclassref":<String[]_value>,      "samlbinding":<String_value>,      "attributeconsumingserviceindex":<Double_value>,      "sendthumbprint":<String_value>,      "logouturl":<String_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/authenticationsamlaction?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",authenticationsamlaction: [ { "__count": "#no"} ] }


