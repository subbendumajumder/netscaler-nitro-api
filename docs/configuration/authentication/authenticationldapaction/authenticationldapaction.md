#authenticationldapaction

Configuration for LDAP action resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the new LDAP action. &lt;br>Must begin with a letter, number, or the underscore character (_), and must contain only letters, numbers, and the hyphen (-), period (.) pound (#), space ( ), at (@), equals (=), colon (:), and underscore characters. Cannot be changed after the LDAP action is added.&lt;br>&lt;br>The following requirement applies only to the NetScaler CLI:&lt;br>If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my authentication action" or my authentication action).&lt;br>Minimum length = 1</td><tr><tr><td>serverip</td><td>&lt;String></td><td>Read-write</td><td>IP address assigned to the LDAP server.&lt;br>Minimum length = 1</td><tr><tr><td>servername</td><td>&lt;String></td><td>Read-write</td><td>LDAP server name as a FQDN. Mutually exclusive with LDAP IP address.&lt;br>Minimum length = 1</td><tr><tr><td>serverport</td><td>&lt;Integer></td><td>Read-write</td><td>Port on which the LDAP server accepts connections.&lt;br>Default value: 389&lt;br>Minimum value = 1</td><tr><tr><td>authtimeout</td><td>&lt;Double></td><td>Read-write</td><td>Number of seconds the NetScaler appliance waits for a response from the RADIUS server.&lt;br>Default value: 3&lt;br>Minimum value = 1</td><tr><tr><td>ldapbase</td><td>&lt;String></td><td>Read-write</td><td>Base (node) from which to start LDAP searches. &lt;br>If the LDAP server is running locally, the default value of base is dc=netscaler, dc=com.</td><tr><tr><td>ldapbinddn</td><td>&lt;String></td><td>Read-write</td><td>Full distinguished name (DN) that is used to bind to the LDAP server. &lt;br>Default: cn=Manager,dc=netscaler,dc=com.</td><tr><tr><td>ldapbinddnpassword</td><td>&lt;String></td><td>Read-write</td><td>Password used to bind to the LDAP server.&lt;br>Minimum length = 1</td><tr><tr><td>ldaploginname</td><td>&lt;String></td><td>Read-write</td><td>LDAP login name attribute. &lt;br>The NetScaler appliance uses the LDAP login name to query external LDAP servers or Active Directories.</td><tr><tr><td>searchfilter</td><td>&lt;String></td><td>Read-write</td><td>String to be combined with the default LDAP user search string to form the search value. For example, if the search filter "vpnallowed=true" is combined with the LDAP login name "samaccount" and the user-supplied username is "bob", the result is the LDAP search string ""(;amp;(vpnallowed=true)(samaccount=bob)"" (Be sure to enclose the search string in two sets of double quotation marks; both sets are needed.).&lt;br>Minimum length = 1</td><tr><tr><td>groupattrname</td><td>&lt;String></td><td>Read-write</td><td>LDAP group attribute name.&lt;br>Used for group extraction on the LDAP server.</td><tr><tr><td>subattributename</td><td>&lt;String></td><td>Read-write</td><td>LDAP group sub-attribute name. &lt;br>Used for group extraction from the LDAP server.</td><tr><tr><td>sectype</td><td>&lt;String></td><td>Read-write</td><td>Type of security used for communications between the NetScaler appliance and the LDAP server. For the PLAINTEXT setting, no encryption is required.&lt;br>Default value: PLAINTEXT&lt;br>Possible values = PLAINTEXT, TLS, SSL</td><tr><tr><td>svrtype</td><td>&lt;String></td><td>Read-write</td><td>The type of LDAP server.&lt;br>Default value: AAA_LDAP_SERVER_TYPE_DEFAULT&lt;br>Possible values = AD, NDS</td><tr><tr><td>ssonameattribute</td><td>&lt;String></td><td>Read-write</td><td>LDAP single signon (SSO) attribute. &lt;br>The NetScaler appliance uses the SSO name attribute to query external LDAP servers or Active Directories for an alternate username.</td><tr><tr><td>authentication</td><td>&lt;String></td><td>Read-write</td><td>Perform LDAP authentication.&lt;br>If authentication is disabled, any LDAP authentication attempt returns authentication success if the user is found. &lt;br>CAUTION! Authentication should be disabled only for authorization group extraction or where other (non-LDAP) authentication methods are in use and either bound to a primary list or flagged as secondary.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>requireuser</td><td>&lt;String></td><td>Read-write</td><td>Require a successful user search for authentication.&lt;br>Default value: YES&lt;br>Possible values = YES, NO</td><tr><tr><td>passwdchange</td><td>&lt;String></td><td>Read-write</td><td>Allow password change requests.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>nestedgroupextraction</td><td>&lt;String></td><td>Read-write</td><td>Allow nested group extraction, in which the NetScaler appliance queries external LDAP servers to determine whether a group is part of another group.&lt;br>Default value: OFF&lt;br>Possible values = ON, OFF</td><tr><tr><td>maxnestinglevel</td><td>&lt;Double></td><td>Read-write</td><td>If nested group extraction is ON, specifies the number of levels up to which group extraction is performed.&lt;br>Default value: 2&lt;br>Minimum value = 2</td><tr><tr><td>followreferrals</td><td>&lt;String></td><td>Read-write</td><td>Setting this option to ON enables following LDAP referrals received from the LDAP server.&lt;br>Default value: OFF&lt;br>Possible values = ON, OFF</td><tr><tr><td>maxldapreferrals</td><td>&lt;Double></td><td>Read-write</td><td>Specifies the maximum number of nested referrals to follow.&lt;br>Default value: 1&lt;br>Minimum value = 1</td><tr><tr><td>referraldnslookup</td><td>&lt;String></td><td>Read-write</td><td>Specifies the DNS Record lookup Type for the referrals.&lt;br>Default value: A-REC&lt;br>Possible values = A-REC, SRV-REC, MSSRV-REC</td><tr><tr><td>mssrvrecordlocation</td><td>&lt;String></td><td>Read-write</td><td>MSSRV Specific parameter. Used to locate the DNS node to which the SRV record pertains in the domainname. The domainname is appended to it to form the srv record.&lt;br>Example : For "dc._msdcs", the srv record formed is _ldap._tcp.dc._msdcs.;lt;domainname;gt;.</td><tr><tr><td>validateservercert</td><td>&lt;String></td><td>Read-write</td><td>When to validate LDAP server certs.&lt;br>Default value: NO&lt;br>Possible values = YES, NO</td><tr><tr><td>ldaphostname</td><td>&lt;String></td><td>Read-write</td><td>Hostname for the LDAP server. If -validateServerCert is ON then this must be the host name on the certificate from the LDAP server.&lt;br>A hostname mismatch will cause a connection failure.</td><tr><tr><td>groupnameidentifier</td><td>&lt;String></td><td>Read-write</td><td>Name that uniquely identifies a group in LDAP or Active Directory.</td><tr><tr><td>groupsearchattribute</td><td>&lt;String></td><td>Read-write</td><td>LDAP group search attribute. &lt;br>Used to determine to which groups a group belongs.</td><tr><tr><td>groupsearchsubattribute</td><td>&lt;String></td><td>Read-write</td><td>LDAP group search subattribute. &lt;br>Used to determine to which groups a group belongs.</td><tr><tr><td>groupsearchfilter</td><td>&lt;String></td><td>Read-write</td><td>String to be combined with the default LDAP group search string to form the search value. For example, the group search filter ""vpnallowed=true"" when combined with the group identifier ""samaccount"" and the group name ""g1"" yields the LDAP search string ""(;amp;(vpnallowed=true)(samaccount=g1)"". (Be sure to enclose the search string in two sets of double quotation marks; both sets are needed.).</td><tr><tr><td>defaultauthenticationgroup</td><td>&lt;String></td><td>Read-write</td><td>This is the default group that is chosen when the authentication succeeds in addition to extracted groups.</td><tr><tr><td>attribute1</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute1 from the ldap response.</td><tr><tr><td>attribute2</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute2 from the ldap response.</td><tr><tr><td>attribute3</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute3 from the ldap response.</td><tr><tr><td>attribute4</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute4 from the ldap response.</td><tr><tr><td>attribute5</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute5 from the ldap response.</td><tr><tr><td>attribute6</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute6 from the ldap response.</td><tr><tr><td>attribute7</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute7 from the ldap response.</td><tr><tr><td>attribute8</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute8 from the ldap response.</td><tr><tr><td>attribute9</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute9 from the ldap response.</td><tr><tr><td>attribute10</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute10 from the ldap response.</td><tr><tr><td>attribute11</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute11 from the ldap response.</td><tr><tr><td>attribute12</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute12 from the ldap response.</td><tr><tr><td>attribute13</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute13 from the ldap response.</td><tr><tr><td>attribute14</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute14 from the ldap response.</td><tr><tr><td>attribute15</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute15 from the ldap response.</td><tr><tr><td>attribute16</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute16 from the ldap response.</td><tr><tr><td>success</td><td>&lt;Double></td><td>Read-only</td><td>.</td><tr><tr><td>failure</td><td>&lt;Double></td><td>Read-only</td><td>.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [DELETE](#delete) | [UPDATE](#update) | [UNSET](#unset) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationldapaction
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"authenticationldapaction":{      "name":<String_value>,      "serverip":<String_value>,      "servername":<String_value>,      "serverport":<Integer_value>,      "authtimeout":<Double_value>,      "ldapbase":<String_value>,      "ldapbinddn":<String_value>,      "ldapbinddnpassword":<String_value>,      "ldaploginname":<String_value>,      "searchfilter":<String_value>,      "groupattrname":<String_value>,      "subattributename":<String_value>,      "sectype":<String_value>,      "svrtype":<String_value>,      "ssonameattribute":<String_value>,      "authentication":<String_value>,      "requireuser":<String_value>,      "passwdchange":<String_value>,      "nestedgroupextraction":<String_value>,      "maxnestinglevel":<Double_value>,      "followreferrals":<String_value>,      "maxldapreferrals":<Double_value>,      "referraldnslookup":<String_value>,      "mssrvrecordlocation":<String_value>,      "validateservercert":<String_value>,      "ldaphostname":<String_value>,      "groupnameidentifier":<String_value>,      "groupsearchattribute":<String_value>,      "groupsearchsubattribute":<String_value>,      "groupsearchfilter":<String_value>,      "defaultauthenticationgroup":<String_value>,      "attribute1":<String_value>,      "attribute2":<String_value>,      "attribute3":<String_value>,      "attribute4":<String_value>,      "attribute5":<String_value>,      "attribute6":<String_value>,      "attribute7":<String_value>,      "attribute8":<String_value>,      "attribute9":<String_value>,      "attribute10":<String_value>,      "attribute11":<String_value>,      "attribute12":<String_value>,      "attribute13":<String_value>,      "attribute14":<String_value>,      "attribute15":<String_value>,      "attribute16":<String_value>}}```
Response:
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationldapaction/name_value&lt;String&gt;
HTTP Method: DELETE
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationldapaction
HTTP Method: PUT
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"authenticationldapaction":{      "name":<String_value>,      "serverip":<String_value>,      "servername":<String_value>,      "serverport":<Integer_value>,      "authtimeout":<Double_value>,      "ldapbase":<String_value>,      "ldapbinddn":<String_value>,      "ldapbinddnpassword":<String_value>,      "ldaploginname":<String_value>,      "searchfilter":<String_value>,      "groupattrname":<String_value>,      "subattributename":<String_value>,      "sectype":<String_value>,      "svrtype":<String_value>,      "ssonameattribute":<String_value>,      "authentication":<String_value>,      "requireuser":<String_value>,      "passwdchange":<String_value>,      "validateservercert":<String_value>,      "ldaphostname":<String_value>,      "nestedgroupextraction":<String_value>,      "maxnestinglevel":<Double_value>,      "groupnameidentifier":<String_value>,      "groupsearchattribute":<String_value>,      "groupsearchsubattribute":<String_value>,      "groupsearchfilter":<String_value>,      "followreferrals":<String_value>,      "maxldapreferrals":<Double_value>,      "referraldnslookup":<String_value>,      "mssrvrecordlocation":<String_value>,      "defaultauthenticationgroup":<String_value>,      "attribute1":<String_value>,      "attribute2":<String_value>,      "attribute3":<String_value>,      "attribute4":<String_value>,      "attribute5":<String_value>,      "attribute6":<String_value>,      "attribute7":<String_value>,      "attribute8":<String_value>,      "attribute9":<String_value>,      "attribute10":<String_value>,      "attribute11":<String_value>,      "attribute12":<String_value>,      "attribute13":<String_value>,      "attribute14":<String_value>,      "attribute15":<String_value>,      "attribute16":<String_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationldapaction?action=unset
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"authenticationldapaction":{      "name":<String_value>,      "serverport":true,      "authtimeout":true,      "ldapbase":true,      "ldapbinddn":true,      "ldapbinddnpassword":true,      "ldaploginname":true,      "searchfilter":true,      "groupattrname":true,      "subattributename":true,      "sectype":true,      "svrtype":true,      "ssonameattribute":true,      "authentication":true,      "requireuser":true,      "passwdchange":true,      "validateservercert":true,      "ldaphostname":true,      "nestedgroupextraction":true,      "maxnestinglevel":true,      "groupnameidentifier":true,      "groupsearchattribute":true,      "groupsearchsubattribute":true,      "groupsearchfilter":true,      "followreferrals":true,      "maxldapreferrals":true,      "referraldnslookup":true,      "mssrvrecordlocation":true,      "defaultauthenticationgroup":true,      "attribute1":true,      "attribute2":true,      "attribute3":true,      "attribute4":true,      "attribute5":true,      "attribute6":true,      "attribute7":true,      "attribute8":true,      "attribute9":true,      "attribute10":true,      "attribute11":true,      "attribute12":true,      "attribute13":true,      "attribute14":true,      "attribute15":true,      "attribute16":true}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationldapaction
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationldapaction?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


filter
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationldapaction?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of authenticationldapaction resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationldapaction?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).


pagination
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationldapaction?pagesize=#no;pageno=#no
Use this query-parameter to get the authenticationldapaction resources in chunks.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "authenticationldapaction": [ {      "name":<String_value>,      "serverip":<String_value>,      "servername":<String_value>,      "serverport":<Integer_value>,      "authtimeout":<Double_value>,      "ldapbinddn":<String_value>,      "ldapbinddnpassword":<String_value>,      "ldaploginname":<String_value>,      "ldapbase":<String_value>,      "searchfilter":<String_value>,      "groupattrname":<String_value>,      "subattributename":<String_value>,      "sectype":<String_value>,      "svrtype":<String_value>,      "ssonameattribute":<String_value>,      "authentication":<String_value>,      "requireuser":<String_value>,      "success":<Double_value>,      "failure":<Double_value>,      "nestedgroupextraction":<String_value>,      "maxnestinglevel":<Double_value>,      "followreferrals":<String_value>,      "maxldapreferrals":<Double_value>,      "referraldnslookup":<String_value>,      "mssrvrecordlocation":<String_value>,      "validateservercert":<String_value>,      "ldaphostname":<String_value>,      "groupnameidentifier":<String_value>,      "groupsearchattribute":<String_value>,      "groupsearchsubattribute":<String_value>,      "groupsearchfilter":<String_value>,      "passwdchange":<String_value>,      "defaultauthenticationgroup":<String_value>,      "attribute1":<String_value>,      "attribute2":<String_value>,      "attribute3":<String_value>,      "attribute4":<String_value>,      "attribute5":<String_value>,      "attribute6":<String_value>,      "attribute7":<String_value>,      "attribute8":<String_value>,      "attribute9":<String_value>,      "attribute10":<String_value>,      "attribute11":<String_value>,      "attribute12":<String_value>,      "attribute13":<String_value>,      "attribute14":<String_value>,      "attribute15":<String_value>,      "attribute16":<String_value>}]}```



###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationldapaction/name_value&lt;String&gt;
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationldapaction/name_value&lt;String&gt;?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationldapaction/name_value&lt;String&gt;?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "authenticationldapaction": [ {      "name":<String_value>,      "serverip":<String_value>,      "servername":<String_value>,      "serverport":<Integer_value>,      "authtimeout":<Double_value>,      "ldapbinddn":<String_value>,      "ldapbinddnpassword":<String_value>,      "ldaploginname":<String_value>,      "ldapbase":<String_value>,      "searchfilter":<String_value>,      "groupattrname":<String_value>,      "subattributename":<String_value>,      "sectype":<String_value>,      "svrtype":<String_value>,      "ssonameattribute":<String_value>,      "authentication":<String_value>,      "requireuser":<String_value>,      "success":<Double_value>,      "failure":<Double_value>,      "nestedgroupextraction":<String_value>,      "maxnestinglevel":<Double_value>,      "followreferrals":<String_value>,      "maxldapreferrals":<Double_value>,      "referraldnslookup":<String_value>,      "mssrvrecordlocation":<String_value>,      "validateservercert":<String_value>,      "ldaphostname":<String_value>,      "groupnameidentifier":<String_value>,      "groupsearchattribute":<String_value>,      "groupsearchsubattribute":<String_value>,      "groupsearchfilter":<String_value>,      "passwdchange":<String_value>,      "defaultauthenticationgroup":<String_value>,      "attribute1":<String_value>,      "attribute2":<String_value>,      "attribute3":<String_value>,      "attribute4":<String_value>,      "attribute5":<String_value>,      "attribute6":<String_value>,      "attribute7":<String_value>,      "attribute8":<String_value>,      "attribute9":<String_value>,      "attribute10":<String_value>,      "attribute11":<String_value>,      "attribute12":<String_value>,      "attribute13":<String_value>,      "attribute14":<String_value>,      "attribute15":<String_value>,      "attribute16":<String_value>}]}```



###count



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationldapaction?count=yes
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: 
{ "authenticationldapaction": [ { "__count": "#no"} ] }


