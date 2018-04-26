#appfwlearningsettings

Configuration for learning settings resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>profilename</td><td>&lt;String></td><td>Read-write</td><td>Name of the profile.<br>Minimum length = 1</td></tr><tr><td>starturlminthreshold</td><td>&lt;Double></td><td>Read-write</td><td>Minimum number of application firewall sessions that the learning engine must observe to learn start URLs.<br>Default value: 1<br>Minimum value = 1</td></tr><tr><td>starturlpercentthreshold</td><td>&lt;Double></td><td>Read-write</td><td>Minimum percentage of application firewall sessions that must contain a particular start URL pattern for the learning engine to learn that start URL.<br>Default value: 0<br>Minimum value = 0<br>Maximum value = 100</td></tr><tr><td>cookieconsistencyminthreshold</td><td>&lt;Double></td><td>Read-write</td><td>Minimum number of application firewall sessions that the learning engine must observe to learn cookies.<br>Default value: 1<br>Minimum value = 1</td></tr><tr><td>cookieconsistencypercentthreshold</td><td>&lt;Double></td><td>Read-write</td><td>Minimum percentage of application firewall sessions that must contain a particular cookie pattern for the learning engine to learn that cookie.<br>Default value: 0<br>Minimum value = 0<br>Maximum value = 100</td></tr><tr><td>csrftagminthreshold</td><td>&lt;Double></td><td>Read-write</td><td>Minimum number of application firewall sessions that the learning engine must observe to learn cross-site request forgery (CSRF) tags.<br>Default value: 1<br>Minimum value = 1</td></tr><tr><td>csrftagpercentthreshold</td><td>&lt;Double></td><td>Read-write</td><td>Minimum percentage of application firewall sessions that must contain a particular CSRF tag for the learning engine to learn that CSRF tag.<br>Default value: 0<br>Minimum value = 0<br>Maximum value = 100</td></tr><tr><td>fieldconsistencyminthreshold</td><td>&lt;Double></td><td>Read-write</td><td>Minimum number of application firewall sessions that the learning engine must observe to learn field consistency information.<br>Default value: 1<br>Minimum value = 1</td></tr><tr><td>fieldconsistencypercentthreshold</td><td>&lt;Double></td><td>Read-write</td><td>Minimum percentage of application firewall sessions that must contain a particular field consistency pattern for the learning engine to learn that field consistency pattern.<br>Default value: 0<br>Minimum value = 0<br>Maximum value = 100</td></tr><tr><td>crosssitescriptingminthreshold</td><td>&lt;Double></td><td>Read-write</td><td>Minimum number of application firewall sessions that the learning engine must observe to learn HTML cross-site scripting patterns.<br>Default value: 1<br>Minimum value = 1</td></tr><tr><td>crosssitescriptingpercentthreshold</td><td>&lt;Double></td><td>Read-write</td><td>Minimum percentage of application firewall sessions that must contain a particular cross-site scripting pattern for the learning engine to learn that cross-site scripting pattern.<br>Default value: 0<br>Minimum value = 0<br>Maximum value = 100</td></tr><tr><td>sqlinjectionminthreshold</td><td>&lt;Double></td><td>Read-write</td><td>Minimum number of application firewall sessions that the learning engine must observe to learn HTML SQL injection patterns.<br>Default value: 1<br>Minimum value = 1</td></tr><tr><td>sqlinjectionpercentthreshold</td><td>&lt;Double></td><td>Read-write</td><td>Minimum percentage of application firewall sessions that must contain a particular HTML SQL injection pattern for the learning engine to learn that HTML SQL injection pattern.<br>Default value: 0<br>Minimum value = 0<br>Maximum value = 100</td></tr><tr><td>fieldformatminthreshold</td><td>&lt;Double></td><td>Read-write</td><td>Minimum number of application firewall sessions that the learning engine must observe to learn field formats.<br>Default value: 1<br>Minimum value = 1</td></tr><tr><td>fieldformatpercentthreshold</td><td>&lt;Double></td><td>Read-write</td><td>Minimum percentage of application firewall sessions that must contain a particular web form field pattern for the learning engine to recommend a field format for that form field.<br>Default value: 0<br>Minimum value = 0<br>Maximum value = 100</td></tr><tr><td>creditcardnumberminthreshold</td><td>&lt;Double></td><td>Read-write</td><td>Minimum threshold to learn Credit Card information.<br>Default value: 1<br>Minimum value = 1</td></tr><tr><td>creditcardnumberpercentthreshold</td><td>&lt;Double></td><td>Read-write</td><td>Minimum threshold in percent to learn Credit Card information.<br>Default value: 0<br>Minimum value = 0<br>Maximum value = 100</td></tr><tr><td>contenttypeminthreshold</td><td>&lt;Double></td><td>Read-write</td><td>Minimum threshold to learn Content Type information.<br>Default value: 1<br>Minimum value = 1</td></tr><tr><td>contenttypepercentthreshold</td><td>&lt;Double></td><td>Read-write</td><td>Minimum threshold in percent to learn Content Type information.<br>Default value: 0<br>Minimum value = 0<br>Maximum value = 100</td></tr><tr><td>xmlwsiminthreshold</td><td>&lt;Double></td><td>Read-write</td><td>Minimum number of application firewall sessions that the learning engine must observe to learn web services interoperability (WSI) information.<br>Default value: 1<br>Minimum value = 1</td></tr><tr><td>xmlwsipercentthreshold</td><td>&lt;Double></td><td>Read-write</td><td>Minimum percentage of application firewall sessions that must contain a particular pattern for the learning engine to learn a web services interoperability (WSI) pattern.<br>Default value: 0<br>Minimum value = 0<br>Maximum value = 100</td></tr><tr><td>xmlattachmentminthreshold</td><td>&lt;Double></td><td>Read-write</td><td>Minimum number of application firewall sessions that the learning engine must observe to learn XML attachment patterns.<br>Default value: 1<br>Minimum value = 1</td></tr><tr><td>xmlattachmentpercentthreshold</td><td>&lt;Double></td><td>Read-write</td><td>Minimum percentage of application firewall sessions that must contain a particular XML attachment pattern for the learning engine to learn that XML attachment pattern.<br>Default value: 0<br>Minimum value = 0<br>Maximum value = 100</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[UPDATE](#u)| [UNSET](#)| [GET (ALL)](#get-)| [GET]()| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appfwlearningsettings
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"appfwlearningsettings":{<b>"profilename":<String_value>,</b>"starturlminthreshold":<Double_value>,"starturlpercentthreshold":<Double_value>,"cookieconsistencyminthreshold":<Double_value>,"cookieconsistencypercentthreshold":<Double_value>,"csrftagminthreshold":<Double_value>,"csrftagpercentthreshold":<Double_value>,"fieldconsistencyminthreshold":<Double_value>,"fieldconsistencypercentthreshold":<Double_value>,"crosssitescriptingminthreshold":<Double_value>,"crosssitescriptingpercentthreshold":<Double_value>,"sqlinjectionminthreshold":<Double_value>,"sqlinjectionpercentthreshold":<Double_value>,"fieldformatminthreshold":<Double_value>,"fieldformatpercentthreshold":<Double_value>,"creditcardnumberminthreshold":<Double_value>,"creditcardnumberpercentthreshold":<Double_value>,"contenttypeminthreshold":<Double_value>,"contenttypepercentthreshold":<Double_value>,"xmlwsiminthreshold":<Double_value>,"xmlwsipercentthreshold":<Double_value>,"xmlattachmentminthreshold":<Double_value>,"xmlattachmentpercentthreshold":<Double_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appfwlearningsettings?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"appfwlearningsettings":{<b>"profilename":<String_value>,</b>"starturlminthreshold":true,"starturlpercentthreshold":true,"cookieconsistencyminthreshold":true,"cookieconsistencypercentthreshold":true,"csrftagminthreshold":true,"csrftagpercentthreshold":true,"fieldconsistencyminthreshold":true,"fieldconsistencypercentthreshold":true,"crosssitescriptingminthreshold":true,"crosssitescriptingpercentthreshold":true,"sqlinjectionminthreshold":true,"sqlinjectionpercentthreshold":true,"fieldformatminthreshold":true,"fieldformatpercentthreshold":true,"creditcardnumberminthreshold":true,"creditcardnumberpercentthreshold":true,"contenttypeminthreshold":true,"contenttypepercentthreshold":true,"xmlwsiminthreshold":true,"xmlwsipercentthreshold":true,"xmlattachmentminthreshold":true,"xmlattachmentpercentthreshold":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appfwlearningsettings
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appfwlearningsettings?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appfwlearningsettings?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of appfwlearningsettings resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appfwlearningsettings?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appfwlearningsettings?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the appfwlearningsettings resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "appfwlearningsettings": [ {"profilename":<String_value>,"starturlminthreshold":<Double_value>,"starturlpercentthreshold":<Double_value>,"cookieconsistencyminthreshold":<Double_value>,"cookieconsistencypercentthreshold":<Double_value>,"csrftagminthreshold":<Double_value>,"csrftagpercentthreshold":<Double_value>,"fieldconsistencyminthreshold":<Double_value>,"fieldconsistencypercentthreshold":<Double_value>,"crosssitescriptingminthreshold":<Double_value>,"crosssitescriptingpercentthreshold":<Double_value>,"sqlinjectionminthreshold":<Double_value>,"sqlinjectionpercentthreshold":<Double_value>,"fieldformatminthreshold":<Double_value>,"fieldformatpercentthreshold":<Double_value>,"creditcardnumberminthreshold":<Double_value>,"creditcardnumberpercentthreshold":<Double_value>,"contenttypeminthreshold":<Double_value>,"contenttypepercentthreshold":<Double_value>,"xmlwsiminthreshold":<Double_value>,"xmlwsipercentthreshold":<Double_value>,"xmlattachmentminthreshold":<Double_value>,"xmlattachmentpercentthreshold":<Double_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appfwlearningsettings/profilename_value&lt;String&gt;
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appfwlearningsettings/profilename_value&lt;String&gt;?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appfwlearningsettings/profilename_value&lt;String&gt;?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "appfwlearningsettings": [ {"profilename":<String_value>,"starturlminthreshold":<Double_value>,"starturlpercentthreshold":<Double_value>,"cookieconsistencyminthreshold":<Double_value>,"cookieconsistencypercentthreshold":<Double_value>,"csrftagminthreshold":<Double_value>,"csrftagpercentthreshold":<Double_value>,"fieldconsistencyminthreshold":<Double_value>,"fieldconsistencypercentthreshold":<Double_value>,"crosssitescriptingminthreshold":<Double_value>,"crosssitescriptingpercentthreshold":<Double_value>,"sqlinjectionminthreshold":<Double_value>,"sqlinjectionpercentthreshold":<Double_value>,"fieldformatminthreshold":<Double_value>,"fieldformatpercentthreshold":<Double_value>,"creditcardnumberminthreshold":<Double_value>,"creditcardnumberpercentthreshold":<Double_value>,"contenttypeminthreshold":<Double_value>,"contenttypepercentthreshold":<Double_value>,"xmlwsiminthreshold":<Double_value>,"xmlwsipercentthreshold":<Double_value>,"xmlattachmentminthreshold":<Double_value>,"xmlattachmentpercentthreshold":<Double_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appfwlearningsettings?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "appfwlearningsettings": [ { "__count": "#no"} ] }```



