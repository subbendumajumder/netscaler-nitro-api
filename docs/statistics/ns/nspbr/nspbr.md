#nspbr

Statistics for Policy Based Routing(PBR) entry resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name of the PBR whose statistics you want the NetScaler appliance to display.&lt;br>Minimum length = 1</td><tr><tr><td>clearstats</td><td>&lt;String></td><td>Read-write</td><td>Clear the statsistics / counters.&lt;br>Possible values = basic, full</td><tr><tr><td>pbrtotpktsallowed</td><td>&lt;Double></td><td>Read-only</td><td>Total packets that matched the PBR (Policy-Based Routes) with action ALLOW</td><tr><tr><td>pbrpktsallowedrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for pbrtotpktsallowed</td><tr><tr><td>pbrtotpktsdenied</td><td>&lt;Double></td><td>Read-only</td><td>Total packets that matched the PBR with action DENY</td><tr><tr><td>pbrpktsdeniedrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for pbrtotpktsdenied</td><tr><tr><td>pbrtothits</td><td>&lt;Double></td><td>Read-only</td><td>Total packets that matched one of the configured PBR</td><tr><tr><td>pbrhitsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for pbrtothits</td><tr><tr><td>pbrtotmisses</td><td>&lt;Double></td><td>Read-only</td><td>Total packets that did not match any PBR</td><tr><tr><td>pbrmissesrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for pbrtotmisses</td><tr><tr><td>pbrtotnulldrop</td><td>&lt;Double></td><td>Read-only</td><td>Total packets that are dropped due to null nexthop</td><tr><tr><td>pbrnulldroprate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for pbrtotnulldrop</td><tr><tr><td>pbrperhits</td><td>&lt;Double></td><td>Read-only</td><td>Number of times the pbr was hit</td><tr><tr><td>pbrperhitsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for pbrperhits</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[GET (ALL)](#get-(all)) | [GET](#get)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/nspbr
Query-parameters:
args
http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/nspbr?args=name:&lt;String_value&gt;,detail:&lt;Boolean_value&gt;,fullvalues:&lt;Boolean_value&gt;,ntimes:&lt;Double_value&gt;,logfile:&lt;String_value&gt;,clearstats:&lt;String_value&gt;
Use this query-parameter to get nspbr resources based on additional properties.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "nspbr": [ {      "name":<String_value>,      "pbrpktsdeniedrate":<Double_value>,      "pbrmissesrate":<Double_value>,      "pbrnulldroprate":<Double_value>,      "pbrtothits":<Double_value>,      "pbrperhitsrate":<Double_value>,      "pbrtotnulldrop":<Double_value>,      "pbrhitsrate":<Double_value>,      "pbrperhits":<Double_value>,      "pbrtotmisses":<Double_value>,      "pbrtotpktsallowed":<Double_value>,      "pbrtotpktsdenied":<Double_value>,      "pbrpktsallowedrate":<Double_value>}]}```



###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/nspbr/name_value&gt;&lt;String&gt;
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "nspbr": [ {      "name":<String_value>,      "pbrpktsdeniedrate":<Double_value>,      "pbrmissesrate":<Double_value>,      "pbrnulldroprate":<Double_value>,      "pbrtothits":<Double_value>,      "pbrperhitsrate":<Double_value>,      "pbrtotnulldrop":<Double_value>,      "pbrhitsrate":<Double_value>,      "pbrperhits":<Double_value>,      "pbrtotmisses":<Double_value>,      "pbrtotpktsallowed":<Double_value>,      "pbrtotpktsdenied":<Double_value>,      "pbrpktsallowedrate":<Double_value>}]}```



