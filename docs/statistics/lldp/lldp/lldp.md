#lldp

Statistics for lldp.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>ifnum</td><td>&lt;String></td><td>Read-write</td><td>LLDP Statistics per interfaces.</td></tr><tr><td>clearstats</td><td>&lt;String></td><td>Read-write</td><td>Clear the statsistics / counters.<br>Possible values = basic, full</td></tr><tr><td>rxportframestotal</td><td>&lt;Double></td><td>Read-only</td><td>Total LLDP Packets received.</td></tr><tr><td>rxportframesrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for rxportframestotal</td></tr><tr><td>rxportbytestotal</td><td>&lt;Double></td><td>Read-only</td><td>Total LLDP bytes received</td></tr><tr><td>rxportbytesrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for rxportbytestotal</td></tr><tr><td>txportframestotal</td><td>&lt;Double></td><td>Read-only</td><td>Total LLDP Packets transmitted</td></tr><tr><td>txportframesrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for txportframestotal</td></tr><tr><td>txportbytestotal</td><td>&lt;Double></td><td>Read-only</td><td>Total LLDP bytes transmitted.</td></tr><tr><td>txportbytesrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for txportbytestotal</td></tr><tr><td>rxportframeserrors</td><td>&lt;Double></td><td>Read-only</td><td>Total errors in LLDP packets.</td></tr><tr><td>rxportframeserrorsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for rxportframeserrors</td></tr><tr><td>rxporttlvsdiscardedtotal</td><td>&lt;Double></td><td>Read-only</td><td>Total discarded LLDP packets.</td></tr><tr><td>rxporttlvsdiscardedrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for rxporttlvsdiscardedtotal</td></tr><tr><td>rxporttlvsunrecognizedtotal</td><td>&lt;Double></td><td>Read-only</td><td>Total TLVs not Recognised.</td></tr><tr><td>rxporttlvsunrecognizedrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for rxporttlvsunrecognizedtotal</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[GET (ALL)](#get-)| [GET]()


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/lldp
<b>Query-parameters:</b>
<b>args</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/lldp?<b>args=ifnum:&lt;String_value&gt;,detail:&lt;Boolean_value&gt;,fullvalues:&lt;Boolean_value&gt;,ntimes:&lt;Double_value&gt;,logfile:&lt;String_value&gt;,clearstats:&lt;String_value&gt;</b>
Use this query-parameter to get lldp resources based on additional properties.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "lldp": [ {"ifnum":<String_value>,"rxporttlvsdiscardedtotal":<Double_value>,"rxportframeserrors":<Double_value>,"rxportframeserrorsrate":<Double_value>,"rxportframestotal":<Double_value>,"txportbytestotal":<Double_value>,"txportframestotal":<Double_value>,"rxporttlvsunrecognizedtotal":<Double_value>,"rxportbytesrate":<Double_value>,"rxportbytestotal":<Double_value>,"rxporttlvsdiscardedrate":<Double_value>,"txportbytesrate":<Double_value>,"rxporttlvsunrecognizedrate":<Double_value>,"rxportframesrate":<Double_value>,"txportframesrate":<Double_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/lldp/ifnum_value&gt;&lt;String&gt;
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "lldp": [ {"ifnum":<String_value>,"rxporttlvsdiscardedtotal":<Double_value>,"rxportframeserrors":<Double_value>,"rxportframeserrorsrate":<Double_value>,"rxportframestotal":<Double_value>,"txportbytestotal":<Double_value>,"txportframestotal":<Double_value>,"rxporttlvsunrecognizedtotal":<Double_value>,"rxportbytesrate":<Double_value>,"rxportbytestotal":<Double_value>,"rxporttlvsdiscardedrate":<Double_value>,"txportbytesrate":<Double_value>,"rxporttlvsunrecognizedrate":<Double_value>,"rxportframesrate":<Double_value>,"txportframesrate":<Double_value>}]}```



