#gslbsite

Statistics for GSLB site resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>sitename</td><td>&lt;String></td><td>Read-write</td><td>Name of the GSLB site for which to display detailed statistics. If a name is not specified, basic information about all GSLB sites is displayed.&lt;br>Minimum length = 1</td><tr><tr><td>clearstats</td><td>&lt;String></td><td>Read-write</td><td>Clear the statsistics / counters.&lt;br>Possible values = basic, full</td><tr><tr><td>sitepublicip</td><td>&lt;String></td><td>Read-only</td><td>The public IP address of this GSLB site.</td><tr><tr><td>siteip</td><td>&lt;String></td><td>Read-only</td><td>The private IP address of this GSLB site.</td><tr><tr><td>sitemepstatus</td><td>&lt;String></td><td>Read-only</td><td>Indicates the status of the Metric Exchange Policy at this GSLB site.</td><tr><tr><td>persexchange</td><td>&lt;String></td><td>Read-only</td><td>Indicates whether Persistence entries exchange is enabled or disabled at this GSLB site.</td><tr><tr><td>nwmetricexchange</td><td>&lt;String></td><td>Read-only</td><td>Indicates whether network metric exchange is enabled or disabled at this GSLB site.</td><tr><tr><td>sitemetricexchange</td><td>&lt;String></td><td>Read-only</td><td>Indicates whether metric exchange is enabled or disabled at this GSLB site.</td><tr><tr><td>sitetype</td><td>&lt;String></td><td>Read-only</td><td>Indicates whether this GSLB site is local or remote.</td><tr><tr><td>siteipstr</td><td>&lt;String></td><td>Read-only</td><td>The private IP address of this GSLB site.</td><tr><tr><td>sitepublicipstr</td><td>&lt;String></td><td>Read-only</td><td>The public IP address of this GSLB site.</td><tr><tr><td>sitemetricmepstatus</td><td>&lt;String></td><td>Read-only</td><td>Indicates the status of the site metric Metric Exchange connection at this GSLB site.</td><tr><tr><td>nwmetricmepstatus</td><td>&lt;String></td><td>Read-only</td><td>Indicates the status of the network metric Metric Exchange connection at this GSLB site.</td><tr><tr><td>sitetotalrequestbytes</td><td>&lt;Double></td><td>Read-only</td><td>Total number of request bytes received by the virtual servers represented by all GSLB services associated with this GSLB site.</td><tr><tr><td>siterequestbytesrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for sitetotalrequestbytes</td><tr><tr><td>sitetotalresponsebytes</td><td>&lt;Double></td><td>Read-only</td><td>Number of response bytes received by the virtual servers represented by all GSLB services associated with this GSLB site.</td><tr><tr><td>siteresponsebytesrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for sitetotalresponsebytes</td><tr><tr><td>sitetotalrequests</td><td>&lt;Double></td><td>Read-only</td><td>Total number of requests received by the virtual servers represented by all GSLB services associated with this GSLB site.</td><tr><tr><td>siterequestsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for sitetotalrequests</td><tr><tr><td>sitetotalresponses</td><td>&lt;Double></td><td>Read-only</td><td>Number of responses received by the virtual servers represented by all GSLB services associated with this GSLB site.</td><tr><tr><td>siteresponsesrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for sitetotalresponses</td><tr><tr><td>sitecurclntconnections</td><td>&lt;Double></td><td>Read-only</td><td>Number of current client connections to the virtual servers represented by all GSLB services associated with this GSLB site.</td><tr><tr><td>sitecursrvrconnections</td><td>&lt;Double></td><td>Read-only</td><td>Number of current connections to the real servers behind the virtual servers represented by all GSLB services associated with this GSLB site.</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[GET (ALL)](#get-(all)) | [GET](#get)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/gslbsite
Query-parameters:
args
http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/gslbsite?args=sitename:&lt;String_value&gt;,detail:&lt;Boolean_value&gt;,fullvalues:&lt;Boolean_value&gt;,ntimes:&lt;Double_value&gt;,logfile:&lt;String_value&gt;,clearstats:&lt;String_value&gt;
Use this query-parameter to get gslbsite resources based on additional properties.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "gslbsite": [ {      "sitename":<String_value>,      "siteresponsesrate":<Double_value>,      "siteipstr":<String_value>,      "sitetotalrequests":<Double_value>,      "siterequestsrate":<Double_value>,      "nwmetricmepstatus":<String_value>,      "sitemetricexchange":<String_value>,      "sitepublicip":<String_value>,      "sitetotalresponsebytes":<Double_value>,      "sitecursrvrconnections":<Double_value>,      "sitepublicipstr":<String_value>,      "sitetotalrequestbytes":<Double_value>,      "siteip":<String_value>,      "sitemepstatus":<String_value>,      "sitecurclntconnections":<Double_value>,      "sitetype":<String_value>,      "nwmetricexchange":<String_value>,      "persexchange":<String_value>,      "siterequestbytesrate":<Double_value>,      "siteresponsebytesrate":<Double_value>,      "sitetotalresponses":<Double_value>,      "sitemetricmepstatus":<String_value>}]}```



###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/gslbsite/sitename_value&gt;&lt;String&gt;
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "gslbsite": [ {      "sitename":<String_value>,      "siteresponsesrate":<Double_value>,      "siteipstr":<String_value>,      "sitetotalrequests":<Double_value>,      "siterequestsrate":<Double_value>,      "nwmetricmepstatus":<String_value>,      "sitemetricexchange":<String_value>,      "sitepublicip":<String_value>,      "sitetotalresponsebytes":<Double_value>,      "sitecursrvrconnections":<Double_value>,      "sitepublicipstr":<String_value>,      "sitetotalrequestbytes":<Double_value>,      "siteip":<String_value>,      "sitemepstatus":<String_value>,      "sitecurclntconnections":<Double_value>,      "sitetype":<String_value>,      "nwmetricexchange":<String_value>,      "persexchange":<String_value>,      "siterequestbytesrate":<Double_value>,      "siteresponsebytesrate":<Double_value>,      "sitetotalresponses":<Double_value>,      "sitemetricmepstatus":<String_value>}]}```



