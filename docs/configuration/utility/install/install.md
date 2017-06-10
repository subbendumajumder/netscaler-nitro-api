#install

Configuration for 0 resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>url</td><td>&lt;String></td><td>Read-write</td><td>Url for the build file. Must be in the following formats:&lt;br>http://[user]:[password]@host/path/to/file&lt;br>https://[user]:[password]@host/path/to/file&lt;br>sftp://[user]:[password]@host/path/to/file&lt;br>scp://[user]:[password]@host/path/to/file&lt;br>ftp://[user]:[password]@host/path/to/file&lt;br>file://path/to/file.</td><tr><tr><td>y</td><td>&lt;Boolean></td><td>Read-write</td><td>Do not prompt for yes/no before rebooting.</td><tr><tr><td>l</td><td>&lt;Boolean></td><td>Read-write</td><td>Use this flag to enable callhome.</td><tr><tr><td>enhancedupgrade</td><td>&lt;Boolean></td><td>Read-write</td><td>Use this flag for upgrading from/to enhancement mode.</td><tr><tr><td>resizeswapvar</td><td>&lt;Boolean></td><td>Read-write</td><td>Use this flag to change swap size on ONLY 64bit nCore/MCNS/VMPE systems NON-VPX systems.</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[INSTALL](#install)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###Install



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/install
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"install":{      "url":<String_value>,      "y":<Boolean_value>,      "l":<Boolean_value>,      "enhancedupgrade":<Boolean_value>,      "resizeswapvar":<Boolean_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


