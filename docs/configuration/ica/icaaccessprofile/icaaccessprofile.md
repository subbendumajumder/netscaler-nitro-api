#icaaccessprofile

Configuration for ica accessprofile resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the ICA accessprofile. Must begin with a letter, number, or the underscore character (_), and must contain only letters, numbers, and<br>the hyphen (-), period (.) pound (#), space ( ), at (@), equals (=), colon (:), and underscore characters. Cannot be changed after the ICA accessprofile is added.<br><br>The following requirement applies only to the NetScaler CLI:<br>If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my ica accessprofile" or 'my ica accessprofile').<br><br>Each of the features can be configured as DEFAULT/DISABLED.<br>Here, DISABLED means that the policy settings on the backend XenApp/XenDesktop server are overridden and the NetScaler makes the decision to deny access. Whereas DEFAULT means that the NetScaler allows the request to reach the XenApp/XenDesktop that takes the decision to allow/deny access based on the policy configured on it. For example, if ClientAudioRedirection is enabled on the backend XenApp/XenDesktop server, and the configured profile has ClientAudioRedirection as DISABLED, the NetScaler makes the decision to deny the request irrespective of the configuration on the backend. If the configured profile has ClientAudioRedirection as DEFAULT, then the NetScaler forwards the requests to the backend XenApp/XenDesktop server.It then makes the decision to allow/deny access based on the policy configured on it.<br>Minimum length = 1</td></tr><tr><td>connectclientlptports</td><td>&lt;String></td><td>Read-write</td><td>Allow Default access/Disable automatic connection of LPT ports from the client when the user logs on.<br>Default value: DISABLED<br>Possible values = DEFAULT, DISABLED</td></tr><tr><td>clientaudioredirection</td><td>&lt;String></td><td>Read-write</td><td>Allow Default access/Disable applications hosted on the server to play sounds through a sound device installed on the client computer, also allows or prevents users to record audio input.<br>Default value: DISABLED<br>Possible values = DEFAULT, DISABLED</td></tr><tr><td>localremotedatasharing</td><td>&lt;String></td><td>Read-write</td><td>Allow Default access/Disable file/data sharing via the Reciever for HTML5.<br>Default value: DISABLED<br>Possible values = DEFAULT, DISABLED</td></tr><tr><td>clientclipboardredirection</td><td>&lt;String></td><td>Read-write</td><td>Allow Default access/Disable the clipboard on the client device to be mapped to the clipboard on the server.<br>Default value: DISABLED<br>Possible values = DEFAULT, DISABLED</td></tr><tr><td>clientcomportredirection</td><td>&lt;String></td><td>Read-write</td><td>Allow Default access/Disable COM port redirection to and from the client.<br>Default value: DISABLED<br>Possible values = DEFAULT, DISABLED</td></tr><tr><td>clientdriveredirection</td><td>&lt;String></td><td>Read-write</td><td>Allow Default access/Disables drive redirection to and from the client.<br>Default value: DISABLED<br>Possible values = DEFAULT, DISABLED</td></tr><tr><td>clientprinterredirection</td><td>&lt;String></td><td>Read-write</td><td>Allow Default access/Disable client printers to be mapped to a server when a user logs on to a session.<br>Default value: DISABLED<br>Possible values = DEFAULT, DISABLED</td></tr><tr><td>multistream</td><td>&lt;String></td><td>Read-write</td><td>Allow Default access/Disable the multistream feature for the specified users.<br>Default value: DISABLED<br>Possible values = DEFAULT, DISABLED</td></tr><tr><td>clientusbdriveredirection</td><td>&lt;String></td><td>Read-write</td><td>Allow Default access/Disable the redirection of USB devices to and from the client.<br>Default value: DISABLED<br>Possible values = DEFAULT, DISABLED</td></tr><tr><td>refcnt</td><td>&lt;Double></td><td>Read-only</td><td>Number of entities using this accessprofile.</td></tr><tr><td>builtin</td><td>&lt;String[]></td><td>Read-only</td><td>Indicates that the ICA accessprofile is a built-in (SYSTEM INTERNAL) type.<br>Possible values = MODIFIABLE, DELETABLE, IMMUTABLE, PARTITION_ALL</td></tr><tr><td>isdefault</td><td>&lt;Boolean></td><td>Read-only</td><td>A value of true is returned if it is a default accessprofile.</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD]()| [DELETE](#d)| [UPDATE](#u)| [UNSET](#)| [GET (ALL)](#get-)| [GET]()| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/icaaccessprofile
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"icaaccessprofile":{<b>"name":<String_value>,</b>"connectclientlptports":<String_value>,"clientaudioredirection":<String_value>,"localremotedatasharing":<String_value>,"clientclipboardredirection":<String_value>,"clientcomportredirection":<String_value>,"clientdriveredirection":<String_value>,"clientprinterredirection":<String_value>,"multistream":<String_value>,"clientusbdriveredirection":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/icaaccessprofile/name_value&lt;String&gt;
<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/icaaccessprofile
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"icaaccessprofile":{<b>"name":<String_value>,</b>"connectclientlptports":<String_value>,"clientaudioredirection":<String_value>,"localremotedatasharing":<String_value>,"clientclipboardredirection":<String_value>,"clientcomportredirection":<String_value>,"clientdriveredirection":<String_value>,"clientprinterredirection":<String_value>,"multistream":<String_value>,"clientusbdriveredirection":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/icaaccessprofile?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"icaaccessprofile":{<b>"name":<String_value>,</b>"connectclientlptports":true,"clientaudioredirection":true,"localremotedatasharing":true,"clientclipboardredirection":true,"clientcomportredirection":true,"clientdriveredirection":true,"clientprinterredirection":true,"multistream":true,"clientusbdriveredirection":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/icaaccessprofile
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/icaaccessprofile?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/icaaccessprofile?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of icaaccessprofile resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/icaaccessprofile?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/icaaccessprofile?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the icaaccessprofile resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "icaaccessprofile": [ {"name":<String_value>,"connectclientlptports":<String_value>,"clientaudioredirection":<String_value>,"localremotedatasharing":<String_value>,"clientclipboardredirection":<String_value>,"clientcomportredirection":<String_value>,"clientdriveredirection":<String_value>,"clientprinterredirection":<String_value>,"multistream":<String_value>,"clientusbdriveredirection":<String_value>,"refcnt":<Double_value>,"builtin":<String[]_value>,"isdefault":<Boolean_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/icaaccessprofile/name_value&lt;String&gt;
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/icaaccessprofile/name_value&lt;String&gt;?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/icaaccessprofile/name_value&lt;String&gt;?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "icaaccessprofile": [ {"name":<String_value>,"connectclientlptports":<String_value>,"clientaudioredirection":<String_value>,"localremotedatasharing":<String_value>,"clientclipboardredirection":<String_value>,"clientcomportredirection":<String_value>,"clientdriveredirection":<String_value>,"clientprinterredirection":<String_value>,"multistream":<String_value>,"clientusbdriveredirection":<String_value>,"refcnt":<Double_value>,"builtin":<String[]_value>,"isdefault":<Boolean_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/icaaccessprofile?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "icaaccessprofile": [ { "__count": "#no"} ] }```



