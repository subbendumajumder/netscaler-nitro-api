#nshostname

Configuration for host name resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>hostname</td><td>&lt;String></td><td>Read-write</td><td>Host name for the NetScaler appliance.&lt;br>Minimum length = 1&lt;br>Maximum length = 255</td><tr><tr><td>ownernode</td><td>&lt;Double></td><td>Read-write</td><td>ID of the cluster node for which you are setting the hostname. Can be configured only through the cluster IP address.&lt;br>Default value: 255&lt;br>Minimum value = 0&lt;br>Maximum value = 31</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[UPDATE](#update) | [GET (ALL)](#get-(all)) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","nshostname":{      "hostname":<String_value>,      "ownernode":<Double_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/nshostname
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/nshostname?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of nshostname resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/nshostname?view=summary
Use this query-parameter to get the summary output of nshostname resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/nshostname?pagesize=#no;pageno=#no
Use this query-parameter to get the nshostname resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/nshostname?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "nshostname": [ {      "hostname":<String_value>,      "ownernode":<Double_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/nshostname?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",nshostname: [ { "__count": "#no"} ] }


