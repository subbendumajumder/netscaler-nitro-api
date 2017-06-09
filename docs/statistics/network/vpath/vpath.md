#vpath

Statistics for Vpath resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>clearstats</td><td>&lt;String></td><td>Read-write</td><td>Clear the statsistics / counters.&lt;br>Possible values = basic, full</td><tr><tr><td>vpathtotl2datarx</td><td>&lt;Double></td><td>Read-only</td><td>Total number of non-fragmented vPath data packets decapsulated in L2 adjacency</td><tr><tr><td>vpathl2datarxrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for vpathtotl2datarx</td><tr><tr><td>vpathtotl3datarx</td><td>&lt;Double></td><td>Read-only</td><td>Total number of non-fragmented vPath data packets decapsulated in L3 adjacency</td><tr><tr><td>vpathl3datarxrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for vpathtotl3datarx</td><tr><tr><td>vpathtotl2cntrlpkts</td><td>&lt;Double></td><td>Read-only</td><td>Total number of vPath control packets received in L2 adjacency</td><tr><tr><td>vpathl2cntrlpktsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for vpathtotl2cntrlpkts</td><tr><tr><td>vpathtotl3cntrlpkts</td><td>&lt;Double></td><td>Read-only</td><td>Total number of vPath control packets received in L3 adjacency</td><tr><tr><td>vpathl3cntrlpktsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for vpathtotl3cntrlpkts</td><tr><tr><td>vpathtotfragpkts</td><td>&lt;Double></td><td>Read-only</td><td>Total number of vPath fragments received</td><tr><tr><td>vpathfragpktsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for vpathtotfragpkts</td><tr><tr><td>vpathtotl2encappkts</td><td>&lt;Double></td><td>Read-only</td><td>Total number of L2 vPath encapsulated packets injected to VEM</td><tr><tr><td>vpathl2encappktsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for vpathtotl2encappkts</td><tr><tr><td>vpathtotl3encappkts</td><td>&lt;Double></td><td>Read-only</td><td>Total number of L3 vPath encapsulated packets injected to VEM</td><tr><tr><td>vpathl3encappktsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for vpathtotl3encappkts</td><tr><tr><td>vpathtotfragencappkts</td><td>&lt;Double></td><td>Read-only</td><td>Number of fragmented vPath packets transmitted</td><tr><tr><td>vpathfragencappktsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for vpathtotfragencappkts</td><tr><tr><td>vpathtotoffload</td><td>&lt;Double></td><td>Read-only</td><td>Number of offloaded vPath packets transmitted</td><tr><tr><td>vpathoffloadrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for vpathtotoffload</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[GET (ALL)](#get-(all))


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/vpath
Query-parameters:
args
http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/vpath?args=detail:&lt;Boolean_value&gt;,fullvalues:&lt;Boolean_value&gt;,ntimes:&lt;Double_value&gt;,logfile:&lt;String_value&gt;,clearstats:&lt;String_value&gt;
Use this query-parameter to get vpath resources based on additional properties.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "vpath": [ {      "vpathfragencappktsrate":<Double_value>,      "vpathtotl2cntrlpkts":<Double_value>,      "vpathtotoffload":<Double_value>,      "vpathtotl3encappkts":<Double_value>,      "vpathtotl2datarx":<Double_value>,      "vpathtotl2encappkts":<Double_value>,      "vpathoffloadrate":<Double_value>,      "vpathl3cntrlpktsrate":<Double_value>,      "vpathfragpktsrate":<Double_value>,      "vpathtotl3datarx":<Double_value>,      "vpathtotl3cntrlpkts":<Double_value>,      "vpathtotfragencappkts":<Double_value>,      "vpathl3encappktsrate":<Double_value>,      "vpathl2encappktsrate":<Double_value>,      "vpathl2cntrlpktsrate":<Double_value>,      "vpathl3datarxrate":<Double_value>,      "vpathl2datarxrate":<Double_value>,      "vpathtotfragpkts":<Double_value>}]}```



