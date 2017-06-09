#systemmemory

Statistics for Global system memory stats resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>clearstats</td><td>&lt;String></td><td>Read-write</td><td>Clear the statsistics / counters.&lt;br>Possible values = basic, full</td><tr><tr><td>cacmemmaxmemlimitpcnt</td><td>&lt;Double></td><td>Read-only</td><td>Integrated Cache memory insue percent.</td><tr><tr><td>cacmemmaxmemlimit</td><td>&lt;Double></td><td>Read-only</td><td>Integrated Cache memory insue, in megabytes.</td><tr><tr><td>shmemerrallocfailed</td><td>&lt;Double></td><td>Read-only</td><td>Total shared memory allocation failed.</td><tr><tr><td>shmemallocpcnt</td><td>&lt;Double></td><td>Read-only</td><td>Shared memory insue percent.</td><tr><tr><td>shmemallocinmb</td><td>&lt;Double></td><td>Read-only</td><td>Shared memory insue, in megabytes.</td><tr><tr><td>shmemtotinmb</td><td>&lt;Double></td><td>Read-only</td><td>Total shared memory allowed to allocate, in megabytes.</td><tr><tr><td>memtotallocfailed</td><td>&lt;Double></td><td>Read-only</td><td>Total system memory allocation failed.</td><tr><tr><td>memtotfree</td><td>&lt;Double></td><td>Read-only</td><td>Total Free PE Memory in the System.</td><tr><tr><td>memusagepcnt</td><td>&lt;Double></td><td>Read-only</td><td>Percentage of memory utilization on NetScaler.</td><tr><tr><td>memtotuseinmb</td><td>&lt;Double></td><td>Read-only</td><td>Total NetScaler Memory in use, in megabytes.</td><tr><tr><td>memtotallocpcnt</td><td>&lt;Double></td><td>Read-only</td><td>Currently allocated memory in percent.</td><tr><tr><td>memtotallocmb</td><td>&lt;Double></td><td>Read-only</td><td>Currently allocated memory, in megabytes.</td><tr><tr><td>memtotinmb</td><td>&lt;Double></td><td>Read-only</td><td>Total memory available (grabbed) for use by packet engine (PE), in megabytes.</td><tr><tr><td>memtotavail</td><td>&lt;Double></td><td>Read-only</td><td>Total system memory available for PE to grab from the system.</td><tr><tr><td>cacmemmaxsyslimitmb</td><td>&lt;Double></td><td>Read-only</td><td>Integrated Cache memory, in megabytes.</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[GET (ALL)](#get-(all))


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/systemmemory
Query-parameters:
args
http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/systemmemory?args=detail:&lt;Boolean_value&gt;,fullvalues:&lt;Boolean_value&gt;,ntimes:&lt;Double_value&gt;,logfile:&lt;String_value&gt;,clearstats:&lt;String_value&gt;
Use this query-parameter to get systemmemory resources based on additional properties.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "systemmemory": [ {      "memtotallocpcnt":<Double_value>,      "memtotfree":<Double_value>,      "shmemallocpcnt":<Double_value>,      "cacmemmaxmemlimitpcnt":<Double_value>,      "shmemallocinmb":<Double_value>,      "memtotuseinmb":<Double_value>,      "cacmemmaxmemlimit":<Double_value>,      "memusagepcnt":<Double_value>,      "memtotinmb":<Double_value>,      "cacmemmaxsyslimitmb":<Double_value>,      "memtotallocfailed":<Double_value>,      "memtotallocmb":<Double_value>,      "shmemerrallocfailed":<Double_value>,      "memtotavail":<Double_value>,      "shmemtotinmb":<Double_value>}]}```



