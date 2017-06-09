#riseprofile

Configuration for RISE profile resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>profilename</td><td>&lt;String></td><td>Read-write</td><td>Name of the RISE profile.&lt;br>Minimum length = 1&lt;br>Maximum length = 83</td><tr><tr><td>servicename</td><td>&lt;String></td><td>Read-only</td><td>RISE Service name.&lt;br>Minimum length = 1&lt;br>Maximum length = 31</td><tr><tr><td>deviceid</td><td>&lt;String></td><td>Read-only</td><td>Device id.&lt;br>Minimum length = 1&lt;br>Maximum length = 31</td><tr><tr><td>slotid</td><td>&lt;Double></td><td>Read-only</td><td>Slot number of the RISE profile.</td><tr><tr><td>slotno</td><td>&lt;Double></td><td>Read-only</td><td>Slot number of the RISE profile.</td><tr><tr><td>vdcid</td><td>&lt;Double></td><td>Read-only</td><td>RISE vdc id.</td><tr><tr><td>vpcid</td><td>&lt;Double></td><td>Read-only</td><td>RISE vpc id.</td><tr><tr><td>ipaddress</td><td>&lt;String></td><td>Read-only</td><td>RISE ip address.</td><tr><tr><td>mode</td><td>&lt;String></td><td>Read-only</td><td>RISE attach mode.&lt;br>Possible values = Direct, Indirect, vPC-Direct</td><tr><tr><td>status</td><td>&lt;String></td><td>Read-only</td><td>RISE status.&lt;br>Possible values = Active, Inactive</td><tr><tr><td>vlan</td><td>&lt;Double></td><td>Read-only</td><td>RISE Vlan id.</td><tr><tr><td>vlangroupid</td><td>&lt;Double></td><td>Read-only</td><td>RISE Vlan Group id.</td><tr><tr><td>vlancfgstatus</td><td>&lt;String></td><td>Read-only</td><td>RISE config status.&lt;br>Possible values = Ok, Invalid</td><tr><tr><td>ifnum</td><td>&lt;String></td><td>Read-only</td><td>RISE Interface number.</td><tr><tr><td>issu</td><td>&lt;String></td><td>Read-only</td><td>RISE issu status.&lt;br>Possible values = InProgress, None</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/riseprofile
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/riseprofile?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


filter
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/riseprofile?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of riseprofile resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/riseprofile?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).


pagination
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/riseprofile?pagesize=#no;pageno=#no
Use this query-parameter to get the riseprofile resources in chunks.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "riseprofile": [ {      "profilename":<String_value>,      "servicename":<String_value>,      "deviceid":<String_value>,      "slotid":<Double_value>,      "slotno":<Double_value>,      "vdcid":<Double_value>,      "vpcid":<Double_value>,      "ipaddress":<String_value>,      "mode":<String_value>,      "status":<String_value>,      "vlan":<Double_value>,      "vlangroupid":<Double_value>,      "vlancfgstatus":<String_value>,      "ifnum":<String_value>,      "issu":<String_value>}]}```



###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/riseprofile/profilename_value&lt;String&gt;
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/riseprofile/profilename_value&lt;String&gt;?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/riseprofile/profilename_value&lt;String&gt;?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "riseprofile": [ {      "profilename":<String_value>,      "servicename":<String_value>,      "deviceid":<String_value>,      "slotid":<Double_value>,      "slotno":<Double_value>,      "vdcid":<Double_value>,      "vpcid":<Double_value>,      "ipaddress":<String_value>,      "mode":<String_value>,      "status":<String_value>,      "vlan":<Double_value>,      "vlangroupid":<Double_value>,      "vlancfgstatus":<String_value>,      "ifnum":<String_value>,      "issu":<String_value>}]}```



###count



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/riseprofile?count=yes
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: 
{ "riseprofile": [ { "__count": "#no"} ] }


