#sslcipher_service_binding

Binding object showing the service that can be bound to sslcipher.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>cipherpriority</td><td>&lt;Double></td><td>Read-write</td><td>Priority of the cipher to be added.<br>Minimum value = 1<br>Maximum value = 1000</td></tr><tr><td>ciphgrpals</td><td>&lt;String></td><td>Read-write</td><td>A cipher-suite can consist of an individual cipher name, the system predefined cipher-alias name, or user defined cipher-group name.<br>Minimum length = 1</td></tr><tr><td>servicegroupname</td><td>&lt;String></td><td>Read-write</td><td>The name of the SSL service name to which the cipher-suite is to be bound.<br>Minimum length = 1</td></tr><tr><td>servicegroup</td><td>&lt;Boolean></td><td>Read-write</td><td>Indicates that the cipher operation is to be performed on the named SSL service or service group.</td></tr><tr><td>service</td><td>&lt;Boolean></td><td>Read-write</td><td>Indicates that the cipher operation is to be performed on the named SSL service or service group.</td></tr><tr><td>servicename</td><td>&lt;String></td><td>Read-write</td><td>The name of the SSL service name to which the cipher-suite is to be bound.<br>Minimum length = 1</td></tr><tr><td>ciphergroupname</td><td>&lt;String></td><td>Read-write</td><td>Name of the user-defined cipher group.<br>Minimum length = 1</td></tr><tr><td>cipheroperation</td><td>&lt;String></td><td>Read-write</td><td>The operation that is performed when adding the cipher-suite. Possible cipher operations are: ADD - Appends the given cipher-suite to the existing one configured for the virtual server. REM - Removes the given cipher-suite from the existing one configured for the virtual server. ORD - Overrides the current configured cipher-suite for the virtual server with the given cipher-suite.<br>Default value: 0<br>Possible values = ADD, REM, ORD</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

