#dnsrecords

Read/write properties


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>dnsrecordtype</td><td>&lt;String></td><td>Read-write</td><td>Display statistics for the specified DNS record or query type or, if a record or query type is not specified, statistics for all record types supported on the NetScaler appliance.</td></tr><tr><td>clearstats</td><td>&lt;String></td><td>Read-write</td><td>Clear the statsistics / counters.<br>Possible values = basic, full</td></tr><tr><td>dnstotentries</td><td>&lt;Double></td><td>Read-only</td><td>Total number of DNS record entries</td></tr><tr><td>dnstotupdates</td><td>&lt;Double></td><td>Read-only</td><td>Total number of DNS proactive updates</td></tr><tr><td>dnstotresponses</td><td>&lt;Double></td><td>Read-only</td><td>Total number of DNS server responses</td></tr><tr><td>dnstotrequests</td><td>&lt;Double></td><td>Read-only</td><td>Total number of DNS queries recieved</td></tr><tr><td>dnscurentries</td><td>&lt;Double></td><td>Read-only</td><td>Current number of DNS entries</td></tr><tr><td>dnstoterrlimits</td><td>&lt;Double></td><td>Read-only</td><td>Total number of times we have recieved dns record with more entries than we support</td></tr><tr><td>dnstoterrrespform</td><td>&lt;Double></td><td>Read-only</td><td>Total number of times we have recieved malformed responses from the backend</td></tr><tr><td>dnstoterraliasex</td><td>&lt;Double></td><td>Read-only</td><td>Total number of times we have recieved non-cname record for a domain for which an alias exists</td></tr><tr><td>dnstoterrnodomains</td><td>&lt;Double></td><td>Read-only</td><td>Total number of cache misses</td></tr><tr><td>dnscurrecords</td><td>&lt;Double></td><td>Read-only</td><td>Current number of DNS Records</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[GET (ALL)](#get-)| [GET]()


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/dnsrecords
<b>Query-parameters:</b>
<b>args</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/dnsrecords?<b>args=dnsrecordtype:&lt;String_value&gt;,detail:&lt;Boolean_value&gt;,fullvalues:&lt;Boolean_value&gt;,ntimes:&lt;Double_value&gt;,logfile:&lt;String_value&gt;,clearstats:&lt;String_value&gt;</b>
Use this query-parameter to get dnsrecords resources based on additional properties.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "dnsrecords": [ {"dnsrecordtype":<String_value>,"dnscurentries":<Double_value>,"dnstotupdates":<Double_value>,"dnstotrequests":<Double_value>,"dnstoterraliasex":<Double_value>,"dnstoterrrespform":<Double_value>,"dnstotentries":<Double_value>,"dnscurrecords":<Double_value>,"dnstoterrnodomains":<Double_value>,"dnstoterrlimits":<Double_value>,"dnstotresponses":<Double_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/dnsrecords/dnsrecordtype_value&gt;&lt;String&gt;
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "dnsrecords": [ {"dnsrecordtype":<String_value>,"dnscurentries":<Double_value>,"dnstotupdates":<Double_value>,"dnstotrequests":<Double_value>,"dnstoterraliasex":<Double_value>,"dnstoterrrespform":<Double_value>,"dnstotentries":<Double_value>,"dnscurrecords":<Double_value>,"dnstoterrnodomains":<Double_value>,"dnstoterrlimits":<Double_value>,"dnstotresponses":<Double_value>}]}```



