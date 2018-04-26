#appfwprofile_binding

Binding object which returns the resources bound to appfwprofile.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name of the application firewall profile.<br>Minimum length = 1</td></tr><tr><td>appfwprofile_xmlattachmenturl_binding</td><td>&lt;appfwprofile_xmlattachmenturl_binding[]></td><td>Read-only</td><td>xmlattachmenturl that can be bound to appfwprofile.</td></tr><tr><td>appfwprofile_excluderescontenttype_binding</td><td>&lt;appfwprofile_excluderescontenttype_binding[]></td><td>Read-only</td><td>excluderescontenttype that can be bound to appfwprofile.</td></tr><tr><td>appfwprofile_crosssitescripting_binding</td><td>&lt;appfwprofile_crosssitescripting_binding[]></td><td>Read-only</td><td>crosssitescripting that can be bound to appfwprofile.</td></tr><tr><td>appfwprofile_xmlwsiurl_binding</td><td>&lt;appfwprofile_xmlwsiurl_binding[]></td><td>Read-only</td><td>xmlwsiurl that can be bound to appfwprofile.</td></tr><tr><td>appfwprofile_xmldosurl_binding</td><td>&lt;appfwprofile_xmldosurl_binding[]></td><td>Read-only</td><td>xmldosurl that can be bound to appfwprofile.</td></tr><tr><td>appfwprofile_fieldconsistency_binding</td><td>&lt;appfwprofile_fieldconsistency_binding[]></td><td>Read-only</td><td>fieldconsistency that can be bound to appfwprofile.</td></tr><tr><td>appfwprofile_sqlinjection_binding</td><td>&lt;appfwprofile_sqlinjection_binding[]></td><td>Read-only</td><td>sqlinjection that can be bound to appfwprofile.</td></tr><tr><td>appfwprofile_safeobject_binding</td><td>&lt;appfwprofile_safeobject_binding[]></td><td>Read-only</td><td>safeobject that can be bound to appfwprofile.</td></tr><tr><td>appfwprofile_denyurl_binding</td><td>&lt;appfwprofile_denyurl_binding[]></td><td>Read-only</td><td>denyurl that can be bound to appfwprofile.</td></tr><tr><td>appfwprofile_trustedlearningclients_binding</td><td>&lt;appfwprofile_trustedlearningclients_binding[]></td><td>Read-only</td><td>trustedlearningclients that can be bound to appfwprofile.</td></tr><tr><td>appfwprofile_csrftag_binding</td><td>&lt;appfwprofile_csrftag_binding[]></td><td>Read-only</td><td>csrftag that can be bound to appfwprofile.</td></tr><tr><td>appfwprofile_starturl_binding</td><td>&lt;appfwprofile_starturl_binding[]></td><td>Read-only</td><td>starturl that can be bound to appfwprofile.</td></tr><tr><td>appfwprofile_cookieconsistency_binding</td><td>&lt;appfwprofile_cookieconsistency_binding[]></td><td>Read-only</td><td>cookieconsistency that can be bound to appfwprofile.</td></tr><tr><td>appfwprofile_xmlsqlinjection_binding</td><td>&lt;appfwprofile_xmlsqlinjection_binding[]></td><td>Read-only</td><td>xmlsqlinjection that can be bound to appfwprofile.</td></tr><tr><td>appfwprofile_creditcardnumber_binding</td><td>&lt;appfwprofile_creditcardnumber_binding[]></td><td>Read-only</td><td>creditcardnumber that can be bound to appfwprofile.</td></tr><tr><td>appfwprofile_xmlxss_binding</td><td>&lt;appfwprofile_xmlxss_binding[]></td><td>Read-only</td><td>xmlxss that can be bound to appfwprofile.</td></tr><tr><td>appfwprofile_fieldformat_binding</td><td>&lt;appfwprofile_fieldformat_binding[]></td><td>Read-only</td><td>fieldformat that can be bound to appfwprofile.</td></tr><tr><td>appfwprofile_contenttype_binding</td><td>&lt;appfwprofile_contenttype_binding[]></td><td>Read-only</td><td>contenttype that can be bound to appfwprofile.</td></tr><tr><td>appfwprofile_xmlvalidationurl_binding</td><td>&lt;appfwprofile_xmlvalidationurl_binding[]></td><td>Read-only</td><td>xmlvalidationurl that can be bound to appfwprofile.</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[GET]()| [GET (ALL)](#get-)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appfwprofile_binding/name_value&lt;String&gt;
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "appfwprofile_binding": [ {"name":<String_value>,"appfwprofile_csrftag_binding":<appfwprofile_csrftag_binding[]_value>,"appfwprofile_starturl_binding":<appfwprofile_starturl_binding[]_value>,"appfwprofile_xmlvalidationurl_binding":<appfwprofile_xmlvalidationurl_binding[]_value>,"appfwprofile_xmlattachmenturl_binding":<appfwprofile_xmlattachmenturl_binding[]_value>,"appfwprofile_safeobject_binding":<appfwprofile_safeobject_binding[]_value>,"appfwprofile_cookieconsistency_binding":<appfwprofile_cookieconsistency_binding[]_value>,"appfwprofile_fieldconsistency_binding":<appfwprofile_fieldconsistency_binding[]_value>,"appfwprofile_xmlwsiurl_binding":<appfwprofile_xmlwsiurl_binding[]_value>,"appfwprofile_xmlsqlinjection_binding":<appfwprofile_xmlsqlinjection_binding[]_value>,"appfwprofile_sqlinjection_binding":<appfwprofile_sqlinjection_binding[]_value>,"appfwprofile_trustedlearningclients_binding":<appfwprofile_trustedlearningclients_binding[]_value>,"appfwprofile_crosssitescripting_binding":<appfwprofile_crosssitescripting_binding[]_value>,"appfwprofile_excluderescontenttype_binding":<appfwprofile_excluderescontenttype_binding[]_value>,"appfwprofile_contenttype_binding":<appfwprofile_contenttype_binding[]_value>,"appfwprofile_denyurl_binding":<appfwprofile_denyurl_binding[]_value>,"appfwprofile_xmlxss_binding":<appfwprofile_xmlxss_binding[]_value>,"appfwprofile_fieldformat_binding":<appfwprofile_fieldformat_binding[]_value>,"appfwprofile_creditcardnumber_binding":<appfwprofile_creditcardnumber_binding[]_value>,"appfwprofile_xmldosurl_binding":<appfwprofile_xmldosurl_binding[]_value>}]}```



###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appfwprofile_binding
<b>Query-parameters:</b>
<b>bulkbindings</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appfwprofile_binding?<b>bulkbindings=yes</b>
NITRO allows you to fetch bindings in bulk.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "appfwprofile_binding": [ {"name":<String_value>,"appfwprofile_csrftag_binding":<appfwprofile_csrftag_binding[]_value>,"appfwprofile_starturl_binding":<appfwprofile_starturl_binding[]_value>,"appfwprofile_xmlvalidationurl_binding":<appfwprofile_xmlvalidationurl_binding[]_value>,"appfwprofile_xmlattachmenturl_binding":<appfwprofile_xmlattachmenturl_binding[]_value>,"appfwprofile_safeobject_binding":<appfwprofile_safeobject_binding[]_value>,"appfwprofile_cookieconsistency_binding":<appfwprofile_cookieconsistency_binding[]_value>,"appfwprofile_fieldconsistency_binding":<appfwprofile_fieldconsistency_binding[]_value>,"appfwprofile_xmlwsiurl_binding":<appfwprofile_xmlwsiurl_binding[]_value>,"appfwprofile_xmlsqlinjection_binding":<appfwprofile_xmlsqlinjection_binding[]_value>,"appfwprofile_sqlinjection_binding":<appfwprofile_sqlinjection_binding[]_value>,"appfwprofile_trustedlearningclients_binding":<appfwprofile_trustedlearningclients_binding[]_value>,"appfwprofile_crosssitescripting_binding":<appfwprofile_crosssitescripting_binding[]_value>,"appfwprofile_excluderescontenttype_binding":<appfwprofile_excluderescontenttype_binding[]_value>,"appfwprofile_contenttype_binding":<appfwprofile_contenttype_binding[]_value>,"appfwprofile_denyurl_binding":<appfwprofile_denyurl_binding[]_value>,"appfwprofile_xmlxss_binding":<appfwprofile_xmlxss_binding[]_value>,"appfwprofile_fieldformat_binding":<appfwprofile_fieldformat_binding[]_value>,"appfwprofile_creditcardnumber_binding":<appfwprofile_creditcardnumber_binding[]_value>,"appfwprofile_xmldosurl_binding":<appfwprofile_xmldosurl_binding[]_value>}]}```



