#sslfips

Configuration for fips resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>inithsm</td><td>&lt;String></td><td>Read-write</td><td>FIPS initialization level. The appliance currently supports Level-2 (FIPS 140-2).<br>Possible values = Level-2</td></tr><tr><td>sopassword</td><td>&lt;String></td><td>Read-write</td><td>Security officer password that will be in effect after you have configured the HSM.<br>Minimum length = 1</td></tr><tr><td>oldsopassword</td><td>&lt;String></td><td>Read-write</td><td>Old password for the security officer.<br>Minimum length = 1</td></tr><tr><td>userpassword</td><td>&lt;String></td><td>Read-write</td><td>The Hardware Security Module's (HSM) User password.<br>Minimum length = 1</td></tr><tr><td>hsmlabel</td><td>&lt;String></td><td>Read-write</td><td>Label to identify the Hardware Security Module (HSM).<br>Minimum length = 1</td></tr><tr><td>fipsfw</td><td>&lt;String></td><td>Read-write</td><td>Path to the FIPS firmware file.<br>Minimum length = 1</td></tr><tr><td>erasedata</td><td>&lt;String></td><td>Read-only</td><td>Erase data.<br>Default value: FIPS_ERASE<br>Minimum length = 1</td></tr><tr><td>serial</td><td>&lt;Integer></td><td>Read-only</td><td>FIPS card serial number.</td></tr><tr><td>majorversion</td><td>&lt;Integer></td><td>Read-only</td><td>Firmware major version.</td></tr><tr><td>minorversion</td><td>&lt;Integer></td><td>Read-only</td><td>Firmware minor version.</td></tr><tr><td>fipshwmajorversion</td><td>&lt;Integer></td><td>Read-only</td><td>FIPS card hardware major version.</td></tr><tr><td>fipshwminorversion</td><td>&lt;Integer></td><td>Read-only</td><td>FIPS card hardware minor version.</td></tr><tr><td>fipshwversionstring</td><td>&lt;String></td><td>Read-only</td><td>FIPS card hardware extended version string.</td></tr><tr><td>flashmemorytotal</td><td>&lt;Integer></td><td>Read-only</td><td>Total size of the flash memory on card.</td></tr><tr><td>flashmemoryfree</td><td>&lt;Integer></td><td>Read-only</td><td>Total size of free flash memory.</td></tr><tr><td>sramtotal</td><td>&lt;Integer></td><td>Read-only</td><td>Total size of the SRAM memory on card.</td></tr><tr><td>sramfree</td><td>&lt;Integer></td><td>Read-only</td><td>Total size of free SRAM memory.</td></tr><tr><td>status</td><td>&lt;Integer></td><td>Read-only</td><td>Status.</td></tr><tr><td>flag</td><td>&lt;Integer></td><td>Read-only</td><td>Internal Flags.</td></tr><tr><td>serialno</td><td>&lt;String></td><td>Read-only</td><td>FIPS card serial number.</td></tr><tr><td>model</td><td>&lt;String></td><td>Read-only</td><td>FIPS card model info.</td></tr><tr><td>state</td><td>&lt;Integer></td><td>Read-only</td><td>FIPS card state.</td></tr><tr><td>firmwarereleasedate</td><td>&lt;String></td><td>Read-only</td><td>FIPS card firmware revision date.</td></tr><tr><td>coresmax</td><td>&lt;Integer></td><td>Read-only</td><td>Maximum number of crypto cores present in the FIPS card.</td></tr><tr><td>coresenabled</td><td>&lt;Integer></td><td>Read-only</td><td>Number of crypto cores enabled in the FIPS card.</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[UPDATE](#u)| [UNSET](#)| [RESET](#)| [CHANGE](#c)| [GET (ALL)](#get-)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslfips
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"sslfips":{<b>"inithsm":<String_value>,</b><b>"sopassword":<String_value>,</b><b>"oldsopassword":<String_value>,</b><b>"userpassword":<String_value>,</b>"hsmlabel":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslfips?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"sslfips":{"hsmlabel":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###reset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslfips?<b>action=reset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"sslfips":{}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###change



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslfips?<b>action=update</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"sslfips":{<b>"fipsfw":<String_value></b>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslfips
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "sslfips": [ {"inithsm":<String_value>,"sopassword":<String_value>,"userpassword":<String_value>,"oldsopassword":<String_value>,"erasedata":<String_value>,"hsmlabel":<String_value>,"serial":<Integer_value>,"majorversion":<Integer_value>,"minorversion":<Integer_value>,"fipshwmajorversion":<Integer_value>,"fipshwminorversion":<Integer_value>,"fipshwversionstring":<String_value>,"flashmemorytotal":<Integer_value>,"flashmemoryfree":<Integer_value>,"sramtotal":<Integer_value>,"sramfree":<Integer_value>,"status":<Integer_value>,"flag":<Integer_value>,"serialno":<String_value>,"model":<String_value>,"state":<Integer_value>,"firmwarereleasedate":<String_value>,"coresmax":<Integer_value>,"coresenabled":<Integer_value>}]}```



