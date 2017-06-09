#dnsprofile

Configuration for DNS profile resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>dnsprofilename</td><td>&lt;String></td><td>Read-write</td><td>Name of the DNS profile.&lt;br>Minimum length = 1&lt;br>Maximum length = 127</td><tr><tr><td>dnsquerylogging</td><td>&lt;String></td><td>Read-write</td><td>DNS query logging; if enabled, DNS query information such as DNS query id, DNS query flags , DNS domain name and DNS query type will be logged.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>dnsanswerseclogging</td><td>&lt;String></td><td>Read-write</td><td>DNS answer section; if enabled, answer section in the response will be logged.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>dnsextendedlogging</td><td>&lt;String></td><td>Read-write</td><td>DNS extended logging; if enabled, authority and additional section in the response will be logged.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>dnserrorlogging</td><td>&lt;String></td><td>Read-write</td><td>DNS error logging; if enabled, whenever error is encountered in DNS module reason for the error will be logged.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>cacherecords</td><td>&lt;String></td><td>Read-write</td><td>Cache resource records in the DNS cache. Applies to resource records obtained through proxy configurations only. End resolver and forwarder configurations always cache records in the DNS cache, and you cannot disable this behavior. When you disable record caching, the appliance stops caching server responses. However, cached records are not flushed. The appliance does not serve requests from the cache until record caching is enabled again.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>cachenegativeresponses</td><td>&lt;String></td><td>Read-write</td><td>Cache negative responses in the DNS cache. When disabled, the appliance stops caching negative responses except referral records. This applies to all configurations - proxy, end resolver, and forwarder. However, cached responses are not flushed. The appliance does not serve negative responses from the cache until this parameter is enabled again.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>referencecount</td><td>&lt;Double></td><td>Read-only</td><td>Number of entities using this profile.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [UPDATE](#update) | [UNSET](#unset) | [DELETE](#delete) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>},"sessionid":"##sessionid","dnsprofile":{      "dnsprofilename":<String_value>,      "dnsquerylogging":<String_value>,      "dnsanswerseclogging":<String_value>,      "dnsextendedlogging":<String_value>,      "dnserrorlogging":<String_value>,      "cacherecords":<String_value>,      "cachenegativeresponses":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","dnsprofile":{      "dnsprofilename":<String_value>,      "dnsquerylogging":<String_value>,      "dnsanswerseclogging":<String_value>,      "dnsextendedlogging":<String_value>,      "dnserrorlogging":<String_value>,      "cacherecords":<String_value>,      "cachenegativeresponses":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","dnsprofile":{      "dnsprofilename":<String_value>,      "dnsquerylogging":true,      "dnsanswerseclogging":true,      "dnsextendedlogging":true,      "dnserrorlogging":true,      "cacherecords":true,      "cachenegativeresponses":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/dnsprofile/dnsprofilename_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/dnsprofile/dnsprofilename_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/dnsprofile
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/dnsprofile?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of dnsprofile resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/dnsprofile?view=summary
Use this query-parameter to get the summary output of dnsprofile resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/dnsprofile?pagesize=#no;pageno=#no
Use this query-parameter to get the dnsprofile resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/dnsprofile?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "dnsprofile": [ {      "dnsprofilename":<String_value>,      "dnsquerylogging":<String_value>,      "dnsanswerseclogging":<String_value>,      "dnsextendedlogging":<String_value>,      "dnserrorlogging":<String_value>,      "cacherecords":<String_value>,      "cachenegativeresponses":<String_value>,      "referencecount":<Double_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/dnsprofile/dnsprofilename_value&lt;String&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "dnsprofile": [ {      "dnsprofilename":<String_value>,      "dnsquerylogging":<String_value>,      "dnsanswerseclogging":<String_value>,      "dnsextendedlogging":<String_value>,      "dnserrorlogging":<String_value>,      "cacherecords":<String_value>,      "cachenegativeresponses":<String_value>,      "referencecount":<Double_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/dnsprofile?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",dnsprofile: [ { "__count": "#no"} ] }


