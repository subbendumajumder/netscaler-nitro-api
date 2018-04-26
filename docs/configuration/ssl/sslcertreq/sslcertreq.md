#sslcertreq

Configuration for certificate request resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>reqfile</td><td>&lt;String></td><td>Read-write</td><td>Name for and, optionally, path to the certificate signing request (CSR). /nsconfig/ssl/ is the default path.<br>Maximum length = 63</td></tr><tr><td>keyfile</td><td>&lt;String></td><td>Read-write</td><td>Name of and, optionally, path to the private key used to create the certificate signing request, which then becomes part of the certificate-key pair. The private key can be either an RSA or a DSA key. The key must be present in the appliance's local storage. /nsconfig/ssl is the default path.<br>Maximum length = 63</td></tr><tr><td>subjectaltname</td><td>&lt;String></td><td>Read-write</td><td>Subject Alternative Name (SAN) is an extension to X.509 that allows various values to be associated with a security certificate using a subjectAltName field. These values are called "Subject Alternative Names" (SAN). Names include:<br>1. Email addresses<br>2. IP addresses<br>3. URIs<br>4. DNS names (this is usually also provided as the Common Name RDN within the Subject field of the main certificate.)<br>5. Directory names (alternative Distinguished Names to that given in the Subject).<br>Minimum length = 1</td></tr><tr><td>fipskeyname</td><td>&lt;String></td><td>Read-write</td><td>Name of the FIPS key used to create the certificate signing request. FIPS keys are created inside the Hardware Security Module of the FIPS card.<br>Minimum length = 1<br>Maximum length = 31</td></tr><tr><td>keyform</td><td>&lt;String></td><td>Read-write</td><td>Format in which the key is stored on the appliance.<br>Default value: PEM<br>Possible values = DER, PEM</td></tr><tr><td>pempassphrase</td><td>&lt;String></td><td>Read-write</td><td>.<br>Minimum length = 1<br>Maximum length = 31</td></tr><tr><td>countryname</td><td>&lt;String></td><td>Read-write</td><td>Two letter ISO code for your country. For example, US for United States.<br>Minimum length = 2<br>Maximum length = 2</td></tr><tr><td>statename</td><td>&lt;String></td><td>Read-write</td><td>Full name of the state or province where your organization is located. <br>Do not abbreviate.<br>Minimum length = 1</td></tr><tr><td>organizationname</td><td>&lt;String></td><td>Read-write</td><td>Name of the organization that will use this certificate. The organization name (corporation, limited partnership, university, or government agency) must be registered with some authority at the national, state, or city level. Use the legal name under which the organization is registered. <br>Do not abbreviate the organization name and do not use the following characters in the name: <br>Angle brackets (&lt; &gt;) tilde (~), exclamation mark, at (@), pound (#), zero (0), caret (^), asterisk (*), forward slash (/), square brackets ([ ]), question mark (?).<br>Minimum length = 1</td></tr><tr><td>organizationunitname</td><td>&lt;String></td><td>Read-write</td><td>Name of the division or section in the organization that will use the certificate.<br>Minimum length = 1</td></tr><tr><td>localityname</td><td>&lt;String></td><td>Read-write</td><td>Name of the city or town in which your organization's head office is located.<br>Minimum length = 1</td></tr><tr><td>commonname</td><td>&lt;String></td><td>Read-write</td><td>Fully qualified domain name for the company or web site. The common name must match the name used by DNS servers to do a DNS lookup of your server. Most browsers use this information for authenticating the server's certificate during the SSL handshake. If the server name in the URL does not match the common name as given in the server certificate, the browser terminates the SSL handshake or prompts the user with a warning message. <br>Do not use wildcard characters, such as asterisk (*) or question mark (?), and do not use an IP address as the common name. The common name must not contain the protocol specifier &lt;http://&gt; or &lt;https://&gt;.<br>Minimum length = 1</td></tr><tr><td>emailaddress</td><td>&lt;String></td><td>Read-write</td><td>Contact person's e-mail address. This address is publically displayed as part of the certificate. Provide an e-mail address that is monitored by an administrator who can be contacted about the certificate.<br>Minimum length = 1</td></tr><tr><td>challengepassword</td><td>&lt;String></td><td>Read-write</td><td>Pass phrase, embedded in the certificate signing request that is shared only between the client or server requesting the certificate and the SSL certificate issuer (typically the certificate authority). This pass phrase can be used to authenticate a client or server that is requesting a certificate from the certificate authority.<br>Minimum length = 4</td></tr><tr><td>companyname</td><td>&lt;String></td><td>Read-write</td><td>Additional name for the company or web site.<br>Minimum length = 1</td></tr><tr><td>digestmethod</td><td>&lt;String></td><td>Read-write</td><td>Digest algorithm used in creating CSR.<br>Possible values = SHA1, SHA256</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[CREATE](#c)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###create



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslcertreq?<b>action=create</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"sslcertreq":{<b>"reqfile":<String_value>,</b>"keyfile":<String_value>,"subjectaltname":<String_value>,"fipskeyname":<String_value>,"keyform":<String_value>,"pempassphrase":<String_value>,<b>"countryname":<String_value>,</b><b>"statename":<String_value>,</b><b>"organizationname":<String_value>,</b>"organizationunitname":<String_value>,"localityname":<String_value>,"commonname":<String_value>,"emailaddress":<String_value>,"challengepassword":<String_value>,"companyname":<String_value>,"digestmethod":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


