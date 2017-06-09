#systembackup

Configuration for Backup Data for ns backup and restore resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>filename</td><td>&lt;String></td><td>Read-write</td><td>Name of the backup file(*.tgz) to be restored.</td><tr><tr><td>level</td><td>&lt;String></td><td>Read-write</td><td>Level of data to be backed up.&lt;br>Default value: basic&lt;br>Possible values = basic, full</td><tr><tr><td>comment</td><td>&lt;String></td><td>Read-write</td><td>Comment specified at the time of creation of the backup file(*.tgz).</td><tr><tr><td>skipbackup</td><td>&lt;Boolean></td><td>Read-write</td><td>Use this option to skip taking backup during restore operation.</td><tr><tr><td>size</td><td>&lt;Double></td><td>Read-only</td><td>Size of the backup file(*.tgz) in KB.</td><tr><tr><td>creationtime</td><td>&lt;String></td><td>Read-only</td><td>Creation time of the backup file(*.tgz).</td><tr><tr><td>version</td><td>&lt;String></td><td>Read-only</td><td>Build version of the backup file(*.tgz).</td><tr><tr><td>createdby</td><td>&lt;String></td><td>Read-only</td><td>Name of user who created the backup file(*.tgz).</td><tr><tr><td>ipaddress</td><td>&lt;String></td><td>Read-only</td><td>Ip of Netscaler box where the backup file(*.tgz) was created.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[CREATE](#create) | [RESTORE](#restore) | [ADD](#add) | [DELETE](#delete) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###create



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/systembackup?action=create
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"systembackup":{      "filename":<String_value>,      "level":<String_value>,      "comment":<String_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###restore



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/systembackup?action=restore
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"systembackup":{      "filename":<String_value>,      "skipbackup":<Boolean_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###add



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/systembackup
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"systembackup":{      "filename":<String_value>}}```
Response:
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/systembackup/filename_value&lt;String&gt;
HTTP Method: DELETE
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/systembackup
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/systembackup?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


filter
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/systembackup?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of systembackup resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/systembackup?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).


pagination
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/systembackup?pagesize=#no;pageno=#no
Use this query-parameter to get the systembackup resources in chunks.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "systembackup": [ {      "filename":<String_value>,      "level":<String_value>,      "comment":<String_value>,      "size":<Double_value>,      "creationtime":<String_value>,      "version":<String_value>,      "createdby":<String_value>,      "ipaddress":<String_value>}]}```



###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/systembackup/filename_value&lt;String&gt;
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/systembackup/filename_value&lt;String&gt;?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/systembackup/filename_value&lt;String&gt;?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "systembackup": [ {      "filename":<String_value>,      "level":<String_value>,      "comment":<String_value>,      "size":<Double_value>,      "creationtime":<String_value>,      "version":<String_value>,      "createdby":<String_value>,      "ipaddress":<String_value>}]}```



###count



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/systembackup?count=yes
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: 
{ "systembackup": [ { "__count": "#no"} ] }


