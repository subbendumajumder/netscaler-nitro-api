#nsacl6

Statistics for ACL6 entry resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>acl6name</td><td>&lt;String></td><td>Read-write</td><td>Name of the ACL6 rule whose statistics you want the NetScaler appliance to display.&lt;br>Minimum length = 1</td><tr><tr><td>clearstats</td><td>&lt;String></td><td>Read-write</td><td>Clear the statsistics / counters.&lt;br>Possible values = basic, full</td><tr><tr><td>acl6totpktsbridged</td><td>&lt;Double></td><td>Read-only</td><td>Packets matching a bridge IPv6 ACL, which is in transparent mode and bypasses service processing.</td><tr><tr><td>acl6pktsbridgedrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for acl6totpktsbridged</td><tr><tr><td>acl6totpktsdenied</td><td>&lt;Double></td><td>Read-only</td><td>Packets dropped because they match IPv6 ACLs with processing mode set to DENY.</td><tr><tr><td>acl6pktsdeniedrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for acl6totpktsdenied</td><tr><tr><td>acl6totpktsallowed</td><td>&lt;Double></td><td>Read-only</td><td>Packets matching IPv6 ACLs with processing mode set to ALLOW. NetScaler processes these packets.</td><tr><tr><td>acl6pktsallowedrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for acl6totpktsallowed</td><tr><tr><td>acl6totpktsnat</td><td>&lt;Double></td><td>Read-only</td><td>Packets matching a NAT ACL6, resulting in a NAT session.</td><tr><tr><td>acl6pktsnatrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for acl6totpktsnat</td><tr><tr><td>acl6tothits</td><td>&lt;Double></td><td>Read-only</td><td>Packets matching an IPv6 ACL.</td><tr><tr><td>acl6hitsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for acl6tothits</td><tr><tr><td>acl6totmisses</td><td>&lt;Double></td><td>Read-only</td><td>Packets not matching any IPv6 ACL.</td><tr><tr><td>acl6missesrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for acl6totmisses</td><tr><tr><td>acl6totpktsnat64</td><td>&lt;Double></td><td>Read-only</td><td>Packets matching a NAT64 ACL6, resulting in a NAT64 translation.</td><tr><tr><td>acl6pktsnat64rate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for acl6totpktsnat64</td><tr><tr><td>acl6totcount</td><td>&lt;Double></td><td>Read-only</td><td>Total number of ACL6 rules configured.</td><tr><tr><td>acl6perhits</td><td>&lt;Double></td><td>Read-only</td><td>Number of times the acl6 was hit</td><tr><tr><td>acl6perhitsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for acl6perhits</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[GET (ALL)](#get-(all)) | [GET](#get)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/nsacl6
Query-parameters:
args
http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/nsacl6?args=acl6name:&lt;String_value&gt;,detail:&lt;Boolean_value&gt;,fullvalues:&lt;Boolean_value&gt;,ntimes:&lt;Double_value&gt;,logfile:&lt;String_value&gt;,clearstats:&lt;String_value&gt;
Use this query-parameter to get nsacl6 resources based on additional properties.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "nsacl6": [ {      "acl6name":<String_value>,      "acl6pktsnatrate":<Double_value>,      "acl6missesrate":<Double_value>,      "acl6totmisses":<Double_value>,      "acl6totpktsnat64":<Double_value>,      "acl6pktsnat64rate":<Double_value>,      "acl6totpktsnat":<Double_value>,      "acl6perhitsrate":<Double_value>,      "acl6perhits":<Double_value>,      "acl6tothits":<Double_value>,      "acl6pktsbridgedrate":<Double_value>,      "acl6pktsallowedrate":<Double_value>,      "acl6totpktsbridged":<Double_value>,      "acl6totpktsdenied":<Double_value>,      "acl6totcount":<Double_value>,      "acl6totpktsallowed":<Double_value>,      "acl6pktsdeniedrate":<Double_value>,      "acl6hitsrate":<Double_value>}]}```



###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/nsacl6/acl6name_value&gt;&lt;String&gt;
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "nsacl6": [ {      "acl6name":<String_value>,      "acl6pktsnatrate":<Double_value>,      "acl6missesrate":<Double_value>,      "acl6totmisses":<Double_value>,      "acl6totpktsnat64":<Double_value>,      "acl6pktsnat64rate":<Double_value>,      "acl6totpktsnat":<Double_value>,      "acl6perhitsrate":<Double_value>,      "acl6perhits":<Double_value>,      "acl6tothits":<Double_value>,      "acl6pktsbridgedrate":<Double_value>,      "acl6pktsallowedrate":<Double_value>,      "acl6totpktsbridged":<Double_value>,      "acl6totpktsdenied":<Double_value>,      "acl6totcount":<Double_value>,      "acl6totpktsallowed":<Double_value>,      "acl6pktsdeniedrate":<Double_value>,      "acl6hitsrate":<Double_value>}]}```



