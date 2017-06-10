#cloudparameter

Configuration for cloud parameter resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>controllerfqdn</td><td>&lt;String></td><td>Read-write</td><td>FQDN of the controller to which the Netscaler SDProxy Connects.&lt;br>Minimum length = 1</td><tr><tr><td>controllerport</td><td>&lt;Integer></td><td>Read-write</td><td>Port number of the controller to which the Netscaler SDProxy connects.&lt;br>Minimum value = 1&lt;br>Range 1 - 65535&lt;br>* in CLI is represented as 65535 in NITRO API</td><tr><tr><td>instanceid</td><td>&lt;String></td><td>Read-write</td><td>Instance ID of the customer provided by Trust.&lt;br>Minimum length = 1</td><tr><tr><td>customerid</td><td>&lt;String></td><td>Read-write</td><td>Customer ID of the citrix cloud customer.&lt;br>Minimum length = 1</td><tr><tr><td>resourcelocation</td><td>&lt;String></td><td>Read-write</td><td>Resource Location of the customer provided by Trust.&lt;br>Minimum length = 1</td><tr><tr><td>verifyurl</td><td>&lt;String></td><td>Read-write</td><td>Verify url will be fetched from the trust service and consumed by GUI to login to the cloud.</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[UPDATE](#update) | [UNSET](#unset) | [GET (ALL)](#get-(all))


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###update



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/cloudparameter
HTTP Method: PUT
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"cloudparameter":{      "controllerfqdn":<String_value>,      "controllerport":<Integer_value>,      "instanceid":<String_value>,      "customerid":<String_value>,      "resourcelocation":<String_value>,      "verifyurl":<String_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/cloudparameter?action=unset
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"cloudparameter":{      "instanceid":true,      "customerid":true,      "resourcelocation":true,      "verifyurl":true}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/cloudparameter
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "cloudparameter": [ {      "controllerfqdn":<String_value>,      "controllerport":<Integer_value>,      "instanceid":<String_value>,      "customerid":<String_value>,      "resourcelocation":<String_value>,      "verifyurl":<String_value>}]}```



