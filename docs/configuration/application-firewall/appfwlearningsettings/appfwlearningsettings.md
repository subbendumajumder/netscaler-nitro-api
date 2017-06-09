#appfwlearningsettings

Configuration for learning settings resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>profilename</td><td>&lt;String></td><td>Read-write</td><td>Name of the profile.&lt;br>Minimum length = 1</td><tr><tr><td>starturlminthreshold</td><td>&lt;Double></td><td>Read-write</td><td>Minimum number of application firewall sessions that the learning engine must observe to learn start URLs.&lt;br>Default value: 1&lt;br>Minimum value = 1</td><tr><tr><td>starturlpercentthreshold</td><td>&lt;Double></td><td>Read-write</td><td>Minimum percentage of application firewall sessions that must contain a particular start URL pattern for the learning engine to learn that start URL.&lt;br>Default value: 0&lt;br>Minimum value = 0&lt;br>Maximum value = 100</td><tr><tr><td>cookieconsistencyminthreshold</td><td>&lt;Double></td><td>Read-write</td><td>Minimum number of application firewall sessions that the learning engine must observe to learn cookies.&lt;br>Default value: 1&lt;br>Minimum value = 1</td><tr><tr><td>cookieconsistencypercentthreshold</td><td>&lt;Double></td><td>Read-write</td><td>Minimum percentage of application firewall sessions that must contain a particular cookie pattern for the learning engine to learn that cookie.&lt;br>Default value: 0&lt;br>Minimum value = 0&lt;br>Maximum value = 100</td><tr><tr><td>csrftagminthreshold</td><td>&lt;Double></td><td>Read-write</td><td>Minimum number of application firewall sessions that the learning engine must observe to learn cross-site request forgery (CSRF) tags.&lt;br>Default value: 1&lt;br>Minimum value = 1</td><tr><tr><td>csrftagpercentthreshold</td><td>&lt;Double></td><td>Read-write</td><td>Minimum percentage of application firewall sessions that must contain a particular CSRF tag for the learning engine to learn that CSRF tag.&lt;br>Default value: 0&lt;br>Minimum value = 0&lt;br>Maximum value = 100</td><tr><tr><td>fieldconsistencyminthreshold</td><td>&lt;Double></td><td>Read-write</td><td>Minimum number of application firewall sessions that the learning engine must observe to learn field consistency information.&lt;br>Default value: 1&lt;br>Minimum value = 1</td><tr><tr><td>fieldconsistencypercentthreshold</td><td>&lt;Double></td><td>Read-write</td><td>Minimum percentage of application firewall sessions that must contain a particular field consistency pattern for the learning engine to learn that field consistency pattern.&lt;br>Default value: 0&lt;br>Minimum value = 0&lt;br>Maximum value = 100</td><tr><tr><td>crosssitescriptingminthreshold</td><td>&lt;Double></td><td>Read-write</td><td>Minimum number of application firewall sessions that the learning engine must observe to learn HTML cross-site scripting patterns.&lt;br>Default value: 1&lt;br>Minimum value = 1</td><tr><tr><td>crosssitescriptingpercentthreshold</td><td>&lt;Double></td><td>Read-write</td><td>Minimum percentage of application firewall sessions that must contain a particular cross-site scripting pattern for the learning engine to learn that cross-site scripting pattern.&lt;br>Default value: 0&lt;br>Minimum value = 0&lt;br>Maximum value = 100</td><tr><tr><td>sqlinjectionminthreshold</td><td>&lt;Double></td><td>Read-write</td><td>Minimum number of application firewall sessions that the learning engine must observe to learn HTML SQL injection patterns.&lt;br>Default value: 1&lt;br>Minimum value = 1</td><tr><tr><td>sqlinjectionpercentthreshold</td><td>&lt;Double></td><td>Read-write</td><td>Minimum percentage of application firewall sessions that must contain a particular HTML SQL injection pattern for the learning engine to learn that HTML SQL injection pattern.&lt;br>Default value: 0&lt;br>Minimum value = 0&lt;br>Maximum value = 100</td><tr><tr><td>fieldformatminthreshold</td><td>&lt;Double></td><td>Read-write</td><td>Minimum number of application firewall sessions that the learning engine must observe to learn field formats.&lt;br>Default value: 1&lt;br>Minimum value = 1</td><tr><tr><td>fieldformatpercentthreshold</td><td>&lt;Double></td><td>Read-write</td><td>Minimum percentage of application firewall sessions that must contain a particular web form field pattern for the learning engine to recommend a field format for that form field.&lt;br>Default value: 0&lt;br>Minimum value = 0&lt;br>Maximum value = 100</td><tr><tr><td>creditcardnumberminthreshold</td><td>&lt;Double></td><td>Read-write</td><td>Minimum threshold to learn Credit Card information.&lt;br>Default value: 1&lt;br>Minimum value = 1</td><tr><tr><td>creditcardnumberpercentthreshold</td><td>&lt;Double></td><td>Read-write</td><td>Minimum threshold in percent to learn Credit Card information.&lt;br>Default value: 0&lt;br>Minimum value = 0&lt;br>Maximum value = 100</td><tr><tr><td>contenttypeminthreshold</td><td>&lt;Double></td><td>Read-write</td><td>Minimum threshold to learn Content Type information.&lt;br>Default value: 1&lt;br>Minimum value = 1</td><tr><tr><td>contenttypepercentthreshold</td><td>&lt;Double></td><td>Read-write</td><td>Minimum threshold in percent to learn Content Type information.&lt;br>Default value: 0&lt;br>Minimum value = 0&lt;br>Maximum value = 100</td><tr><tr><td>xmlwsiminthreshold</td><td>&lt;Double></td><td>Read-write</td><td>Minimum number of application firewall sessions that the learning engine must observe to learn web services interoperability (WSI) information.&lt;br>Default value: 1&lt;br>Minimum value = 1</td><tr><tr><td>xmlwsipercentthreshold</td><td>&lt;Double></td><td>Read-write</td><td>Minimum percentage of application firewall sessions that must contain a particular pattern for the learning engine to learn a web services interoperability (WSI) pattern.&lt;br>Default value: 0&lt;br>Minimum value = 0&lt;br>Maximum value = 100</td><tr><tr><td>xmlattachmentminthreshold</td><td>&lt;Double></td><td>Read-write</td><td>Minimum number of application firewall sessions that the learning engine must observe to learn XML attachment patterns.&lt;br>Default value: 1&lt;br>Minimum value = 1</td><tr><tr><td>xmlattachmentpercentthreshold</td><td>&lt;Double></td><td>Read-write</td><td>Minimum percentage of application firewall sessions that must contain a particular XML attachment pattern for the learning engine to learn that XML attachment pattern.&lt;br>Default value: 0&lt;br>Minimum value = 0&lt;br>Maximum value = 100</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[UPDATE](#update) | [UNSET](#unset) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###update



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appfwlearningsettings
HTTP Method: PUT
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"appfwlearningsettings":{      "profilename":<String_value>,      "starturlminthreshold":<Double_value>,      "starturlpercentthreshold":<Double_value>,      "cookieconsistencyminthreshold":<Double_value>,      "cookieconsistencypercentthreshold":<Double_value>,      "csrftagminthreshold":<Double_value>,      "csrftagpercentthreshold":<Double_value>,      "fieldconsistencyminthreshold":<Double_value>,      "fieldconsistencypercentthreshold":<Double_value>,      "crosssitescriptingminthreshold":<Double_value>,      "crosssitescriptingpercentthreshold":<Double_value>,      "sqlinjectionminthreshold":<Double_value>,      "sqlinjectionpercentthreshold":<Double_value>,      "fieldformatminthreshold":<Double_value>,      "fieldformatpercentthreshold":<Double_value>,      "creditcardnumberminthreshold":<Double_value>,      "creditcardnumberpercentthreshold":<Double_value>,      "contenttypeminthreshold":<Double_value>,      "contenttypepercentthreshold":<Double_value>,      "xmlwsiminthreshold":<Double_value>,      "xmlwsipercentthreshold":<Double_value>,      "xmlattachmentminthreshold":<Double_value>,      "xmlattachmentpercentthreshold":<Double_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appfwlearningsettings?action=unset
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"appfwlearningsettings":{      "profilename":<String_value>,      "starturlminthreshold":true,      "starturlpercentthreshold":true,      "cookieconsistencyminthreshold":true,      "cookieconsistencypercentthreshold":true,      "csrftagminthreshold":true,      "csrftagpercentthreshold":true,      "fieldconsistencyminthreshold":true,      "fieldconsistencypercentthreshold":true,      "crosssitescriptingminthreshold":true,      "crosssitescriptingpercentthreshold":true,      "sqlinjectionminthreshold":true,      "sqlinjectionpercentthreshold":true,      "fieldformatminthreshold":true,      "fieldformatpercentthreshold":true,      "creditcardnumberminthreshold":true,      "creditcardnumberpercentthreshold":true,      "contenttypeminthreshold":true,      "contenttypepercentthreshold":true,      "xmlwsiminthreshold":true,      "xmlwsipercentthreshold":true,      "xmlattachmentminthreshold":true,      "xmlattachmentpercentthreshold":true}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appfwlearningsettings
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appfwlearningsettings?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


filter
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appfwlearningsettings?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of appfwlearningsettings resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appfwlearningsettings?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).


pagination
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appfwlearningsettings?pagesize=#no;pageno=#no
Use this query-parameter to get the appfwlearningsettings resources in chunks.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "appfwlearningsettings": [ {      "profilename":<String_value>,      "starturlminthreshold":<Double_value>,      "starturlpercentthreshold":<Double_value>,      "cookieconsistencyminthreshold":<Double_value>,      "cookieconsistencypercentthreshold":<Double_value>,      "csrftagminthreshold":<Double_value>,      "csrftagpercentthreshold":<Double_value>,      "fieldconsistencyminthreshold":<Double_value>,      "fieldconsistencypercentthreshold":<Double_value>,      "crosssitescriptingminthreshold":<Double_value>,      "crosssitescriptingpercentthreshold":<Double_value>,      "sqlinjectionminthreshold":<Double_value>,      "sqlinjectionpercentthreshold":<Double_value>,      "fieldformatminthreshold":<Double_value>,      "fieldformatpercentthreshold":<Double_value>,      "creditcardnumberminthreshold":<Double_value>,      "creditcardnumberpercentthreshold":<Double_value>,      "contenttypeminthreshold":<Double_value>,      "contenttypepercentthreshold":<Double_value>,      "xmlwsiminthreshold":<Double_value>,      "xmlwsipercentthreshold":<Double_value>,      "xmlattachmentminthreshold":<Double_value>,      "xmlattachmentpercentthreshold":<Double_value>}]}```



###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appfwlearningsettings/profilename_value&lt;String&gt;
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appfwlearningsettings/profilename_value&lt;String&gt;?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appfwlearningsettings/profilename_value&lt;String&gt;?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "appfwlearningsettings": [ {      "profilename":<String_value>,      "starturlminthreshold":<Double_value>,      "starturlpercentthreshold":<Double_value>,      "cookieconsistencyminthreshold":<Double_value>,      "cookieconsistencypercentthreshold":<Double_value>,      "csrftagminthreshold":<Double_value>,      "csrftagpercentthreshold":<Double_value>,      "fieldconsistencyminthreshold":<Double_value>,      "fieldconsistencypercentthreshold":<Double_value>,      "crosssitescriptingminthreshold":<Double_value>,      "crosssitescriptingpercentthreshold":<Double_value>,      "sqlinjectionminthreshold":<Double_value>,      "sqlinjectionpercentthreshold":<Double_value>,      "fieldformatminthreshold":<Double_value>,      "fieldformatpercentthreshold":<Double_value>,      "creditcardnumberminthreshold":<Double_value>,      "creditcardnumberpercentthreshold":<Double_value>,      "contenttypeminthreshold":<Double_value>,      "contenttypepercentthreshold":<Double_value>,      "xmlwsiminthreshold":<Double_value>,      "xmlwsipercentthreshold":<Double_value>,      "xmlattachmentminthreshold":<Double_value>,      "xmlattachmentpercentthreshold":<Double_value>}]}```



###count



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appfwlearningsettings?count=yes
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: 
{ "appfwlearningsettings": [ { "__count": "#no"} ] }


