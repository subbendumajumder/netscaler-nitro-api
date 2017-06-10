#wisite

Configuration for WI site resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>sitepath</td><td>&lt;String></td><td>Read-write</td><td>Path to the Web Interface site being created on the NetScaler appliance.&lt;br>Minimum length = 1&lt;br>Maximum length = 250</td><tr><tr><td>agurl</td><td>&lt;String></td><td>Read-write</td><td>Call back URL of the Gateway.&lt;br>Minimum length = 1&lt;br>Maximum length = 255</td><tr><tr><td>staurl</td><td>&lt;String></td><td>Read-write</td><td>URL of the Secure Ticket Authority (STA) server.&lt;br>Minimum length = 1&lt;br>Maximum length = 255</td><tr><tr><td>secondstaurl</td><td>&lt;String></td><td>Read-write</td><td>URL of the second Secure Ticket Authority (STA) server.&lt;br>Minimum length = 1&lt;br>Maximum length = 255</td><tr><tr><td>sessionreliability</td><td>&lt;String></td><td>Read-write</td><td>Enable session reliability through Access Gateway.&lt;br>Default value: OFF&lt;br>Possible values = ON, OFF</td><tr><tr><td>usetwotickets</td><td>&lt;String></td><td>Read-write</td><td>Request tickets issued by two separate Secure Ticket Authorities (STA) when a resource is accessed.&lt;br>Default value: OFF&lt;br>Possible values = ON, OFF</td><tr><tr><td>authenticationpoint</td><td>&lt;String></td><td>Read-write</td><td>Authentication point for the Web Interface site.&lt;br>Possible values = WebInterface, AccessGateway</td><tr><tr><td>agauthenticationmethod</td><td>&lt;String></td><td>Read-write</td><td>Method for authenticating a Web Interface site if you have specified Web Interface as the authentication point.&lt;br> Available settings function as follows:&lt;br> * Explicit - Users must provide a user name and password to log on to the Web Interface.&lt;br> * Anonymous - Users can log on to the Web Interface without providing a user name and password. They have access to resources published for anonymous users.&lt;br>Possible values = Explicit, SmartCard</td><tr><tr><td>wiauthenticationmethods</td><td>&lt;String[]></td><td>Read-write</td><td>The method of authentication to be used at Web Interface.&lt;br>Default value: Explicit&lt;br>Possible values = Explicit, Anonymous</td><tr><tr><td>defaultcustomtextlocale</td><td>&lt;String></td><td>Read-write</td><td>Default language for the Web Interface site.&lt;br>Default value: English&lt;br>Possible values = German, English, Spanish, French, Japanese, Korean, Russian, Chinese_simplified, Chinese_traditional</td><tr><tr><td>websessiontimeout</td><td>&lt;Double></td><td>Read-write</td><td>Time-out, in minutes, for idle Web Interface browser sessions. If a clients session is idle for a time that exceeds the time-out value, the NetScaler appliance terminates the connection.&lt;br>Default value: 20&lt;br>Minimum value = 1&lt;br>Maximum value = 1440</td><tr><tr><td>defaultaccessmethod</td><td>&lt;String></td><td>Read-write</td><td>Default access method for clients accessing the Web Interface site.&lt;br> &lt;br> Note: Before you configure an access method based on the client IP address, you must enable USIP mode on the Web Interface service to make the clients IP address available with the Web Interface.&lt;br> Depending on whether the Web Interface site is configured to use an HTTP or HTTPS virtual server or to use access gateway, you can send clients or access gateway the IP address, or the alternate address, of a XenApp or XenDesktop server. Or, you can send the IP address translated from a mapping entry, which defines mapping of an internal address and port to an external address and port.&lt;br> Note: In the NetScaler command line, mapping entries can be created by using the bind wi site command.&lt;br>Possible values = Direct, Alternate, Translated, GatewayDirect, GatewayAlternate, GatewayTranslated</td><tr><tr><td>logintitle</td><td>&lt;String></td><td>Read-write</td><td>A custom login page title for the Web Interface site.&lt;br>Default value: "Welcome to Web Interface on NetScaler"&lt;br>Minimum length = 1&lt;br>Maximum length = 255</td><tr><tr><td>appwelcomemessage</td><td>&lt;String></td><td>Read-write</td><td>Specifies localized text to appear at the top of the main content area of the Applications screen. LanguageCode is en, de, es, fr, ja, or any other supported language identifier.&lt;br>Minimum length = 1&lt;br>Maximum length = 255</td><tr><tr><td>welcomemessage</td><td>&lt;String></td><td>Read-write</td><td>Localized welcome message that appears on the welcome area of the login screen.&lt;br>Minimum length = 1&lt;br>Maximum length = 255</td><tr><tr><td>footertext</td><td>&lt;String></td><td>Read-write</td><td>Localized text that appears in the footer area of all pages.&lt;br>Minimum length = 1&lt;br>Maximum length = 255</td><tr><tr><td>loginsysmessage</td><td>&lt;String></td><td>Read-write</td><td>Localized text that appears at the bottom of the main content area of the login screen.&lt;br>Minimum length = 1&lt;br>Maximum length = 255</td><tr><tr><td>preloginbutton</td><td>&lt;String></td><td>Read-write</td><td>Localized text that appears as the name of the pre-login message confirmation button.&lt;br>Minimum length = 1&lt;br>Maximum length = 255</td><tr><tr><td>preloginmessage</td><td>&lt;String></td><td>Read-write</td><td>Localized text that appears on the pre-login message page.&lt;br>Minimum length = 1&lt;br>Maximum length = 2048</td><tr><tr><td>prelogintitle</td><td>&lt;String></td><td>Read-write</td><td>Localized text that appears as the title of the pre-login message page.&lt;br>Minimum length = 1&lt;br>Maximum length = 255</td><tr><tr><td>domainselection</td><td>&lt;String></td><td>Read-write</td><td>Domain names listed on the login screen for explicit authentication.&lt;br>Minimum length = 1&lt;br>Maximum length = 255</td><tr><tr><td>sitetype</td><td>&lt;String></td><td>Read-write</td><td>Type of access to the Web Interface site. Available settings function as follows:&lt;br>* XenApp/XenDesktop web site - Configures the Web Interface site for access by a web browser.&lt;br>* XenApp/XenDesktop services site - Configures the Web Interface site for access by the XenApp plug-in.&lt;br>Default value: XenAppWeb&lt;br>Possible values = XenAppWeb, XenAppServices</td><tr><tr><td>userinterfacebranding</td><td>&lt;String></td><td>Read-write</td><td>Specifies whether the site is focused towards users accessing applications or desktops. Setting the parameter to Desktops changes the functionality of the site to improve the experience for XenDesktop users. Citrix recommends using this setting for any deployment that includes XenDesktop.&lt;br>Default value: Applications&lt;br>Possible values = Desktops, Applications</td><tr><tr><td>publishedresourcetype</td><td>&lt;String></td><td>Read-write</td><td>Method for accessing the published XenApp and XenDesktop resources. &lt;br> Available settings function as follows:&lt;br> * Online - Allows applications to be launched on the XenApp and XenDesktop servers. &lt;br> * Offline - Allows streaming of applications to the client. &lt;br> * DualMode - Allows both online and offline modes.&lt;br>Default value: Online&lt;br>Possible values = Online, Offline, DualMode</td><tr><tr><td>kioskmode</td><td>&lt;String></td><td>Read-write</td><td>User settings do not persist from one session to another.&lt;br>Default value: OFF&lt;br>Possible values = ON, OFF</td><tr><tr><td>showsearch</td><td>&lt;String></td><td>Read-write</td><td>Enables search option on XenApp websites.&lt;br>Default value: OFF&lt;br>Possible values = ON, OFF</td><tr><tr><td>showrefresh</td><td>&lt;String></td><td>Read-write</td><td>Provides the Refresh button on the applications screen.&lt;br>Default value: OFF&lt;br>Possible values = ON, OFF</td><tr><tr><td>wiuserinterfacemodes</td><td>&lt;String></td><td>Read-write</td><td>Appearance of the login screen.&lt;br> * Simple - Only the login fields for the selected authentication method are displayed.&lt;br> * Advanced - Displays the navigation bar, which provides access to the pre-login messages and preferences screens.&lt;br>Default value: SIMPLE&lt;br>Possible values = SIMPLE, ADVANCED</td><tr><tr><td>userinterfacelayouts</td><td>&lt;String></td><td>Read-write</td><td>Specifies whether or not to use the compact user interface.&lt;br>Default value: AUTO&lt;br>Possible values = AUTO, NORMAL, COMPACT</td><tr><tr><td>restrictdomains</td><td>&lt;String></td><td>Read-write</td><td>The RestrictDomains setting is used to enable/disable domain restrictions. If domain restriction is enabled, the LoginDomains list is used for validating the login domain. It is applied to all the authentication methods except Anonymous for XenApp Web and XenApp Services sites.&lt;br>Default value: OFF&lt;br>Possible values = ON, OFF</td><tr><tr><td>logindomains</td><td>&lt;String></td><td>Read-write</td><td>[List of NetBIOS domain names], Domain names to use for access restriction.&lt;br> Only takes effect when used in conjunction with the RestrictDomains setting.&lt;br>Minimum length = 1&lt;br>Maximum length = 255</td><tr><tr><td>hidedomainfield</td><td>&lt;String></td><td>Read-write</td><td>The HideDomainField setting is used to control whether the domain field is displayed on the logon screen.&lt;br>Default value: OFF&lt;br>Possible values = ON, OFF</td><tr><tr><td>agcallbackurl</td><td>&lt;String></td><td>Read-write</td><td>Callback AGURL to which Web Interface contacts. .&lt;br>Minimum length = 1&lt;br>Maximum length = 255</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [DELETE](#delete) | [UPDATE](#update) | [UNSET](#unset) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/wisite
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"wisite":{      "sitepath":<String_value>,      "agurl":<String_value>,      "staurl":<String_value>,      "secondstaurl":<String_value>,      "sessionreliability":<String_value>,      "usetwotickets":<String_value>,      "authenticationpoint":<String_value>,      "agauthenticationmethod":<String_value>,      "wiauthenticationmethods":<String[]_value>,      "defaultcustomtextlocale":<String_value>,      "websessiontimeout":<Double_value>,      "defaultaccessmethod":<String_value>,      "logintitle":<String_value>,      "appwelcomemessage":<String_value>,      "welcomemessage":<String_value>,      "footertext":<String_value>,      "loginsysmessage":<String_value>,      "preloginbutton":<String_value>,      "preloginmessage":<String_value>,      "prelogintitle":<String_value>,      "domainselection":<String_value>,      "sitetype":<String_value>,      "userinterfacebranding":<String_value>,      "publishedresourcetype":<String_value>,      "kioskmode":<String_value>,      "showsearch":<String_value>,      "showrefresh":<String_value>,      "wiuserinterfacemodes":<String_value>,      "userinterfacelayouts":<String_value>,      "restrictdomains":<String_value>,      "logindomains":<String_value>,      "hidedomainfield":<String_value>,      "agcallbackurl":<String_value>}}```
Response:
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/wisite/sitepath_value&lt;String&gt;
HTTP Method: DELETE
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/wisite
HTTP Method: PUT
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"wisite":{      "sitepath":<String_value>,      "agurl":<String_value>,      "staurl":<String_value>,      "sessionreliability":<String_value>,      "usetwotickets":<String_value>,      "secondstaurl":<String_value>,      "wiauthenticationmethods":<String[]_value>,      "defaultaccessmethod":<String_value>,      "defaultcustomtextlocale":<String_value>,      "websessiontimeout":<Double_value>,      "logintitle":<String_value>,      "appwelcomemessage":<String_value>,      "welcomemessage":<String_value>,      "footertext":<String_value>,      "loginsysmessage":<String_value>,      "preloginbutton":<String_value>,      "preloginmessage":<String_value>,      "prelogintitle":<String_value>,      "domainselection":<String_value>,      "userinterfacebranding":<String_value>,      "authenticationpoint":<String_value>,      "agauthenticationmethod":<String_value>,      "publishedresourcetype":<String_value>,      "kioskmode":<String_value>,      "showsearch":<String_value>,      "showrefresh":<String_value>,      "wiuserinterfacemodes":<String_value>,      "userinterfacelayouts":<String_value>,      "restrictdomains":<String_value>,      "logindomains":<String_value>,      "hidedomainfield":<String_value>,      "agcallbackurl":<String_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/wisite?action=unset
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"wisite":{      "sitepath":<String_value>,      "appwelcomemessage":true,      "welcomemessage":true,      "footertext":true,      "loginsysmessage":true,      "preloginbutton":true,      "preloginmessage":true,      "prelogintitle":true,      "userinterfacebranding":true,      "logindomains":true}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/wisite
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/wisite?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


filter
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/wisite?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of wisite resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/wisite?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).


pagination
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/wisite?pagesize=#no;pageno=#no
Use this query-parameter to get the wisite resources in chunks.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "wisite": [ {      "sitepath":<String_value>,      "agurl":<String_value>,      "staurl":<String_value>,      "wiauthenticationmethods":<String[]_value>,      "logintitle":<String_value>,      "appwelcomemessage":<String_value>,      "welcomemessage":<String_value>,      "footertext":<String_value>,      "loginsysmessage":<String_value>,      "preloginbutton":<String_value>,      "preloginmessage":<String_value>,      "prelogintitle":<String_value>,      "domainselection":<String_value>,      "defaultcustomtextlocale":<String_value>,      "websessiontimeout":<Double_value>,      "sitetype":<String_value>,      "userinterfacebranding":<String_value>,      "showsearch":<String_value>,      "showrefresh":<String_value>,      "wiuserinterfacemodes":<String_value>,      "userinterfacelayouts":<String_value>,      "publishedresourcetype":<String_value>,      "defaultaccessmethod":<String_value>,      "agauthenticationmethod":<String_value>,      "sessionreliability":<String_value>,      "usetwotickets":<String_value>,      "secondstaurl":<String_value>,      "authenticationpoint":<String_value>,      "kioskmode":<String_value>,      "restrictdomains":<String_value>,      "logindomains":<String_value>,      "hidedomainfield":<String_value>,      "agcallbackurl":<String_value>}]}```



###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/wisite/sitepath_value&lt;String&gt;
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/wisite/sitepath_value&lt;String&gt;?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/wisite/sitepath_value&lt;String&gt;?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "wisite": [ {      "sitepath":<String_value>,      "agurl":<String_value>,      "staurl":<String_value>,      "wiauthenticationmethods":<String[]_value>,      "logintitle":<String_value>,      "appwelcomemessage":<String_value>,      "welcomemessage":<String_value>,      "footertext":<String_value>,      "loginsysmessage":<String_value>,      "preloginbutton":<String_value>,      "preloginmessage":<String_value>,      "prelogintitle":<String_value>,      "domainselection":<String_value>,      "defaultcustomtextlocale":<String_value>,      "websessiontimeout":<Double_value>,      "sitetype":<String_value>,      "userinterfacebranding":<String_value>,      "showsearch":<String_value>,      "showrefresh":<String_value>,      "wiuserinterfacemodes":<String_value>,      "userinterfacelayouts":<String_value>,      "publishedresourcetype":<String_value>,      "defaultaccessmethod":<String_value>,      "agauthenticationmethod":<String_value>,      "sessionreliability":<String_value>,      "usetwotickets":<String_value>,      "secondstaurl":<String_value>,      "authenticationpoint":<String_value>,      "kioskmode":<String_value>,      "restrictdomains":<String_value>,      "logindomains":<String_value>,      "hidedomainfield":<String_value>,      "agcallbackurl":<String_value>}]}```



###count



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/wisite?count=yes
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: 
{ "wisite": [ { "__count": "#no"} ] }


