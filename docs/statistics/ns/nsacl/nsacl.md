#nsacl

Statistics for ACL entry resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>aclname</td><td>&lt;String></td><td>Read-write</td><td>Name of the extended ACL rule whose statistics you want the NetScaler appliance to display.<br>Minimum length = 1</td></tr><tr><td>clearstats</td><td>&lt;String></td><td>Read-write</td><td>Clear the statsistics / counters.<br>Possible values = basic, full</td></tr><tr><td>acltotpktsbridged</td><td>&lt;Double></td><td>Read-only</td><td>Packets matching a bridge ACL, which is in transparent mode and bypasses service processing.</td></tr><tr><td>aclpktsbridgedrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for acltotpktsbridged</td></tr><tr><td>acltotpktsdenied</td><td>&lt;Double></td><td>Read-only</td><td>Packets dropped because they match ACLs with processing mode set to DENY.</td></tr><tr><td>aclpktsdeniedrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for acltotpktsdenied</td></tr><tr><td>acltotpktsallowed</td><td>&lt;Double></td><td>Read-only</td><td>Packets matching ACLs with processing mode set to ALLOW. NetScaler processes these packets.</td></tr><tr><td>aclpktsallowedrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for acltotpktsallowed</td></tr><tr><td>acltotpktsnat</td><td>&lt;Double></td><td>Read-only</td><td>Packets matching a NAT ACL, resulting in a NAT session.</td></tr><tr><td>aclpktsnatrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for acltotpktsnat</td></tr><tr><td>acltothits</td><td>&lt;Double></td><td>Read-only</td><td>Packets matching an ACL.</td></tr><tr><td>aclhitsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for acltothits</td></tr><tr><td>acltotmisses</td><td>&lt;Double></td><td>Read-only</td><td>Packets not matching any ACL.</td></tr><tr><td>aclmissesrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for acltotmisses</td></tr><tr><td>acltotcount</td><td>&lt;Double></td><td>Read-only</td><td>Total number of ACL rules configured.</td></tr><tr><td>aclperhits</td><td>&lt;Double></td><td>Read-only</td><td>Number of times the acl was hit</td></tr><tr><td>aclperhitsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for aclperhits</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[GET (ALL)](#get-)| [GET]()


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/nsacl
<b>Query-parameters:</b>
<b>args</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/nsacl?<b>args=aclname:&lt;String_value&gt;,detail:&lt;Boolean_value&gt;,fullvalues:&lt;Boolean_value&gt;,ntimes:&lt;Double_value&gt;,logfile:&lt;String_value&gt;,clearstats:&lt;String_value&gt;</b>
Use this query-parameter to get nsacl resources based on additional properties.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "nsacl": [ {"aclname":<String_value>,"acltotpktsnat":<Double_value>,"aclpktsdeniedrate":<Double_value>,"aclhitsrate":<Double_value>,"aclpktsallowedrate":<Double_value>,"acltotpktsallowed":<Double_value>,"aclpktsbridgedrate":<Double_value>,"acltotpktsdenied":<Double_value>,"acltothits":<Double_value>,"aclperhits":<Double_value>,"aclperhitsrate":<Double_value>,"aclpktsnatrate":<Double_value>,"acltotcount":<Double_value>,"acltotmisses":<Double_value>,"acltotpktsbridged":<Double_value>,"aclmissesrate":<Double_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/nsacl/aclname_value&gt;&lt;String&gt;
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "nsacl": [ {"aclname":<String_value>,"acltotpktsnat":<Double_value>,"aclpktsdeniedrate":<Double_value>,"aclhitsrate":<Double_value>,"aclpktsallowedrate":<Double_value>,"acltotpktsallowed":<Double_value>,"aclpktsbridgedrate":<Double_value>,"acltotpktsdenied":<Double_value>,"acltothits":<Double_value>,"aclperhits":<Double_value>,"aclperhitsrate":<Double_value>,"aclpktsnatrate":<Double_value>,"acltotcount":<Double_value>,"acltotmisses":<Double_value>,"acltotpktsbridged":<Double_value>,"aclmissesrate":<Double_value>}]}```



