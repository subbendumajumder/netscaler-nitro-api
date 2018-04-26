#lsnsipalgprofile

Configuration for LSN SIPALG Profile resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>sipalgprofilename</td><td>&lt;String></td><td>Read-write</td><td>The name of the SIPALG Profile.<br>Minimum length = 1<br>Maximum length = 127</td></tr><tr><td>datasessionidletimeout</td><td>&lt;Double></td><td>Read-write</td><td>Idle timeout for the data channel sessions in seconds.<br>Default value: 120</td></tr><tr><td>sipsessiontimeout</td><td>&lt;Double></td><td>Read-write</td><td>SIP control channel session timeout in seconds.<br>Default value: 600</td></tr><tr><td>registrationtimeout</td><td>&lt;Double></td><td>Read-write</td><td>SIP registration timeout in seconds.<br>Default value: 60</td></tr><tr><td>sipsrcportrange</td><td>&lt;String></td><td>Read-write</td><td>Source port range for SIP_UDP and SIP_TCP.</td></tr><tr><td>sipdstportrange</td><td>&lt;String></td><td>Read-write</td><td>Destination port range for SIP_UDP and SIP_TCP.</td></tr><tr><td>openregisterpinhole</td><td>&lt;String></td><td>Read-write</td><td>ENABLE/DISABLE RegisterPinhole creation.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>opencontactpinhole</td><td>&lt;String></td><td>Read-write</td><td>ENABLE/DISABLE ContactPinhole creation.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>openviapinhole</td><td>&lt;String></td><td>Read-write</td><td>ENABLE/DISABLE ViaPinhole creation.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>openrecordroutepinhole</td><td>&lt;String></td><td>Read-write</td><td>ENABLE/DISABLE RecordRoutePinhole creation.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>siptransportprotocol</td><td>&lt;String></td><td>Read-write</td><td>SIP ALG Profile transport protocol type.<br>Possible values = TCP, UDP</td></tr><tr><td>openroutepinhole</td><td>&lt;String></td><td>Read-write</td><td>ENABLE/DISABLE RoutePinhole creation.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>rport</td><td>&lt;String></td><td>Read-write</td><td>ENABLE/DISABLE rport.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD]()| [UPDATE](#u)| [UNSET](#)| [DELETE](#d)| [GET (ALL)](#get-)| [GET]()| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsnsipalgprofile
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"lsnsipalgprofile":{<b>"sipalgprofilename":<String_value>,</b>"datasessionidletimeout":<Double_value>,"sipsessiontimeout":<Double_value>,"registrationtimeout":<Double_value>,"sipsrcportrange":<String_value>,"sipdstportrange":<String_value>,"openregisterpinhole":<String_value>,"opencontactpinhole":<String_value>,"openviapinhole":<String_value>,"openrecordroutepinhole":<String_value>,<b>"siptransportprotocol":<String_value>,</b>"openroutepinhole":<String_value>,"rport":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsnsipalgprofile
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"lsnsipalgprofile":{<b>"sipalgprofilename":<String_value>,</b>"datasessionidletimeout":<Double_value>,"sipsessiontimeout":<Double_value>,"registrationtimeout":<Double_value>,"sipsrcportrange":<String_value>,"sipdstportrange":<String_value>,"openregisterpinhole":<String_value>,"opencontactpinhole":<String_value>,"openviapinhole":<String_value>,"openrecordroutepinhole":<String_value>,"siptransportprotocol":<String_value>,"openroutepinhole":<String_value>,"rport":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsnsipalgprofile?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"lsnsipalgprofile":{<b>"sipalgprofilename":<String_value>,</b>"datasessionidletimeout":true,"sipsessiontimeout":true,"registrationtimeout":true,"sipsrcportrange":true,"sipdstportrange":true,"openregisterpinhole":true,"opencontactpinhole":true,"openviapinhole":true,"openrecordroutepinhole":true,"siptransportprotocol":true,"openroutepinhole":true,"rport":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsnsipalgprofile/sipalgprofilename_value&lt;String&gt;
<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsnsipalgprofile
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsnsipalgprofile?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsnsipalgprofile?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of lsnsipalgprofile resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsnsipalgprofile?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsnsipalgprofile?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the lsnsipalgprofile resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "lsnsipalgprofile": [ {"sipalgprofilename":<String_value>,"datasessionidletimeout":<Double_value>,"sipsessiontimeout":<Double_value>,"registrationtimeout":<Double_value>,"sipsrcportrange":<String_value>,"sipdstportrange":<String_value>,"openregisterpinhole":<String_value>,"opencontactpinhole":<String_value>,"openviapinhole":<String_value>,"openrecordroutepinhole":<String_value>,"siptransportprotocol":<String_value>,"openroutepinhole":<String_value>,"rport":<String_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsnsipalgprofile/sipalgprofilename_value&lt;String&gt;
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsnsipalgprofile/sipalgprofilename_value&lt;String&gt;?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsnsipalgprofile/sipalgprofilename_value&lt;String&gt;?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "lsnsipalgprofile": [ {"sipalgprofilename":<String_value>,"datasessionidletimeout":<Double_value>,"sipsessiontimeout":<Double_value>,"registrationtimeout":<Double_value>,"sipsrcportrange":<String_value>,"sipdstportrange":<String_value>,"openregisterpinhole":<String_value>,"opencontactpinhole":<String_value>,"openviapinhole":<String_value>,"openrecordroutepinhole":<String_value>,"siptransportprotocol":<String_value>,"openroutepinhole":<String_value>,"rport":<String_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsnsipalgprofile?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "lsnsipalgprofile": [ { "__count": "#no"} ] }```



