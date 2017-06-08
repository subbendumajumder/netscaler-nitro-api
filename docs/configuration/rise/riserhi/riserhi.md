#riserhi

Configuration for RISE RHI rules resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>ipaddress</td><td>&lt;String></td><td>Read-only</td><td>(V)IP advertised.</td><tr><tr><td>prefixlen</td><td>&lt;Double></td><td>Read-only</td><td>Prefix Length.</td><tr><tr><td>hostrtgw</td><td>&lt;String></td><td>Read-only</td><td>Gateway for the advertised IP.</td><tr><tr><td>nexthopvlan</td><td>&lt;Double></td><td>Read-only</td><td>Vlan id on which the gateway is present.</td><tr><tr><td>weight</td><td>&lt;Double></td><td>Read-only</td><td>Cost of the route.</td><tr><tr><td>vserverrhilevel</td><td>&lt;String></td><td>Read-only</td><td>Advertisement level.&lt;br>Default value: ONE_VSERVER&lt;br>Possible values = ONE_VSERVER, ALL_VSERVERS, NONE, VSVR_CNTRLD</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[GET (ALL)](#get-(all)) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/riserhi
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/riserhi?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of riserhi resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/riserhi?view=summary
Use this query-parameter to get the summary output of riserhi resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/riserhi?pagesize=#no;pageno=#no
Use this query-parameter to get the riserhi resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/riserhi?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "riserhi": [ {      "ipaddress":<String_value>,      "prefixlen":<Double_value>,      "hostrtgw":<String_value>,      "nexthopvlan":<Double_value>,      "weight":<Double_value>,      "vserverrhilevel":<String_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/riserhi?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",riserhi: [ { "__count": "#no"} ] }


