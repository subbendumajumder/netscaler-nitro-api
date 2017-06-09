#nsip

Configuration for ip resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>ipaddress</td><td>&lt;String></td><td>Read-write</td><td>IPv4 address to create on the NetScaler appliance. Cannot be changed after the IP address is created.&lt;br>Minimum length = 1</td><tr><tr><td>netmask</td><td>&lt;String></td><td>Read-write</td><td>Subnet mask associated with the IP address.</td><tr><tr><td>type</td><td>&lt;String></td><td>Read-write</td><td>Type of the IP address to create on the NetScaler appliance. Cannot be changed after the IP address is created. The following are the different types of NetScaler owned IP addresses:&lt;br>* A Subnet IP (SNIP) address is used by the NetScaler ADC to communicate with the servers. The NetScaler also uses the subnet IP address when generating its own packets, such as packets related to dynamic routing protocols, or to send monitor probes to check the health of the servers.&lt;br>* A Virtual IP (VIP) address is the IP address associated with a virtual server. It is the IP address to which clients connect. An appliance managing a wide range of traffic may have many VIPs configured. Some of the attributes of the VIP address are customized to meet the requirements of the virtual server.&lt;br>* A GSLB site IP (GSLBIP) address is associated with a GSLB site. It is not mandatory to specify a GSLBIP address when you initially configure the NetScaler appliance. A GSLBIP address is used only when you create a GSLB site.&lt;br>* A Cluster IP (CLIP) address is the management address of the cluster. All cluster configurations must be performed by accessing the cluster through this IP address.&lt;br>Default value: SNIP&lt;br>Possible values = SNIP, VIP, NSIP, GSLBsiteIP, CLIP</td><tr><tr><td>arp</td><td>&lt;String></td><td>Read-write</td><td>Respond to ARP requests for this IP address.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>icmp</td><td>&lt;String></td><td>Read-write</td><td>Respond to ICMP requests for this IP address.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>vserver</td><td>&lt;String></td><td>Read-write</td><td>Use this option to set (enable or disable) the virtual server attribute for this IP address.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>telnet</td><td>&lt;String></td><td>Read-write</td><td>Allow Telnet access to this IP address.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>ftp</td><td>&lt;String></td><td>Read-write</td><td>Allow File Transfer Protocol (FTP) access to this IP address.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>gui</td><td>&lt;String></td><td>Read-write</td><td>Allow graphical user interface (GUI) access to this IP address.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, SECUREONLY, DISABLED</td><tr><tr><td>ssh</td><td>&lt;String></td><td>Read-write</td><td>Allow secure shell (SSH) access to this IP address.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>snmp</td><td>&lt;String></td><td>Read-write</td><td>Allow Simple Network Management Protocol (SNMP) access to this IP address.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>mgmtaccess</td><td>&lt;String></td><td>Read-write</td><td>Allow access to management applications on this IP address.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>restrictaccess</td><td>&lt;String></td><td>Read-write</td><td>Block access to nonmanagement applications on this IP. This option is applicable for MIPs, SNIPs, and NSIP, and is disabled by default. Nonmanagement applications can run on the underlying NetScaler Free BSD operating system.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>dynamicrouting</td><td>&lt;String></td><td>Read-write</td><td>Allow dynamic routing on this IP address. Specific to Subnet IP (SNIP) address.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>ospf</td><td>&lt;String></td><td>Read-write</td><td>Use this option to enable or disable OSPF on this IP address for the entity.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>bgp</td><td>&lt;String></td><td>Read-write</td><td>Use this option to enable or disable BGP on this IP address for the entity.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>rip</td><td>&lt;String></td><td>Read-write</td><td>Use this option to enable or disable RIP on this IP address for the entity.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>hostroute</td><td>&lt;String></td><td>Read-write</td><td>Advertise a route for the VIP address using the dynamic routing protocols running on the NetScaler appliance.&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>hostrtgw</td><td>&lt;String></td><td>Read-write</td><td>IP address of the gateway of the route for this VIP address.&lt;br>Default value: -1</td><tr><tr><td>metric</td><td>&lt;Integer></td><td>Read-write</td><td>Integer value to add to or subtract from the cost of the route advertised for the VIP address.&lt;br>Minimum value = -16777215</td><tr><tr><td>vserverrhilevel</td><td>&lt;String></td><td>Read-write</td><td>Advertise the route for the Virtual IP (VIP) address on the basis of the state of the virtual servers associated with that VIP.&lt;br>* NONE - Advertise the route for the VIP address, regardless of the state of the virtual servers associated with the address.&lt;br>* ONE VSERVER - Advertise the route for the VIP address if at least one of the associated virtual servers is in UP state.&lt;br>* ALL VSERVER - Advertise the route for the VIP address if all of the associated virtual servers are in UP state.&lt;br>* VSVR_CNTRLD - Advertise the route for the VIP address according to the RHIstate (RHI STATE) parameter setting on all the associated virtual servers of the VIP address along with their states.&lt;br>&lt;br>When Vserver RHI Level (RHI) parameter is set to VSVR_CNTRLD, the following are different RHI behaviors for the VIP address on the basis of RHIstate (RHI STATE) settings on the virtual servers associated with the VIP address:&lt;br> * If you set RHI STATE to PASSIVE on all virtual servers, the NetScaler ADC always advertises the route for the VIP address.&lt;br> * If you set RHI STATE to ACTIVE on all virtual servers, the NetScaler ADC advertises the route for the VIP address if at least one of the associated virtual servers is in UP state.&lt;br> *If you set RHI STATE to ACTIVE on some and PASSIVE on others, the NetScaler ADC advertises the route for the VIP address if at least one of the associated virtual servers, whose RHI STATE set to ACTIVE, is in UP state.&lt;br>&lt;br>Default value: ONE_VSERVER&lt;br>Possible values = ONE_VSERVER, ALL_VSERVERS, NONE, VSVR_CNTRLD</td><tr><tr><td>vserverrhimode</td><td>&lt;String></td><td>Read-write</td><td>Advertise the route for the Virtual IP (VIP) address using dynamic routing protocols or using RISE&lt;br>* DYNMAIC_ROUTING - Advertise the route for the VIP address using dynamic routing protocols (default)&lt;br>* RISE - Advertise the route for the VIP address using RISE.&lt;br>Default value: DYNAMIC_ROUTING&lt;br>Possible values = DYNAMIC_ROUTING, RISE</td><tr><tr><td>ospflsatype</td><td>&lt;String></td><td>Read-write</td><td>Type of LSAs to be used by the OSPF protocol, running on the NetScaler appliance, for advertising the route for this VIP address.&lt;br>Default value: TYPE5&lt;br>Possible values = TYPE1, TYPE5</td><tr><tr><td>ospfarea</td><td>&lt;Double></td><td>Read-write</td><td>ID of the area in which the type1 link-state advertisements (LSAs) are to be advertised for this virtual IP (VIP) address by the OSPF protocol running on the NetScaler appliance. When this parameter is not set, the VIP is advertised on all areas.&lt;br>Default value: -1&lt;br>Minimum value = 0&lt;br>Maximum value = 4294967294LU</td><tr><tr><td>state</td><td>&lt;String></td><td>Read-write</td><td>Enable or disable the IP address.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>vrid</td><td>&lt;Double></td><td>Read-write</td><td>A positive integer that uniquely identifies a VMAC address for binding to this VIP address. This binding is used to set up NetScaler appliances in an active-active configuration using VRRP.&lt;br>Minimum value = 1&lt;br>Maximum value = 255</td><tr><tr><td>icmpresponse</td><td>&lt;String></td><td>Read-write</td><td>Respond to ICMP requests for a Virtual IP (VIP) address on the basis of the states of the virtual servers associated with that VIP. Available settings function as follows:&lt;br>* NONE - The NetScaler appliance responds to any ICMP request for the VIP address, irrespective of the states of the virtual servers associated with the address.&lt;br>* ONE VSERVER - The NetScaler appliance responds to any ICMP request for the VIP address if at least one of the associated virtual servers is in UP state.&lt;br>* ALL VSERVER - The NetScaler appliance responds to any ICMP request for the VIP address if all of the associated virtual servers are in UP state.&lt;br>* VSVR_CNTRLD - The behavior depends on the ICMP VSERVER RESPONSE setting on all the associated virtual servers.&lt;br>&lt;br>The following settings can be made for the ICMP VSERVER RESPONSE parameter on a virtual server:&lt;br>* If you set ICMP VSERVER RESPONSE to PASSIVE on all virtual servers, NetScaler always responds.&lt;br>* If you set ICMP VSERVER RESPONSE to ACTIVE on all virtual servers, NetScaler responds if even one virtual server is UP.&lt;br>* When you set ICMP VSERVER RESPONSE to ACTIVE on some and PASSIVE on others, NetScaler responds if even one virtual server set to ACTIVE is UP.&lt;br>Default value: 5&lt;br>Possible values = NONE, ONE_VSERVER, ALL_VSERVERS, VSVR_CNTRLD</td><tr><tr><td>ownernode</td><td>&lt;Double></td><td>Read-write</td><td>The owner node in a Cluster for this IP address. Owner node can vary from 0 to 31. If ownernode is not specified then the IP is treated as Striped IP.&lt;br>Default value: 255</td><tr><tr><td>arpresponse</td><td>&lt;String></td><td>Read-write</td><td>Respond to ARP requests for a Virtual IP (VIP) address on the basis of the states of the virtual servers associated with that VIP. Available settings function as follows:&lt;br>&lt;br>* NONE - The NetScaler appliance responds to any ARP request for the VIP address, irrespective of the states of the virtual servers associated with the address.&lt;br>* ONE VSERVER - The NetScaler appliance responds to any ARP request for the VIP address if at least one of the associated virtual servers is in UP state.&lt;br>* ALL VSERVER - The NetScaler appliance responds to any ARP request for the VIP address if all of the associated virtual servers are in UP state.&lt;br>Default value: 5&lt;br>Possible values = NONE, ONE_VSERVER, ALL_VSERVERS</td><tr><tr><td>td</td><td>&lt;Double></td><td>Read-write</td><td>Integer value that uniquely identifies the traffic domain in which you want to configure the entity. If you do not specify an ID, the entity becomes part of the default traffic domain, which has an ID of 0.&lt;br>Minimum value = 0&lt;br>Maximum value = 4094</td><tr><tr><td>flags</td><td>&lt;Double></td><td>Read-only</td><td>The flags for this entry.</td><tr><tr><td>hostrtgwact</td><td>&lt;String></td><td>Read-only</td><td>Actual Gateway used for advertising host route.</td><tr><tr><td>ospfareaval</td><td>&lt;Double></td><td>Read-only</td><td>The area ID of the area in which OSPF Type1 LSAs are advertised.</td><tr><tr><td>viprtadv2bsd</td><td>&lt;Boolean></td><td>Read-only</td><td>Whether this route is advertised to FreeBSD.</td><tr><tr><td>vipvsercount</td><td>&lt;Double></td><td>Read-only</td><td>Number of vservers bound to this VIP.</td><tr><tr><td>vipvserdowncount</td><td>&lt;Double></td><td>Read-only</td><td>Number of vservers bound to this VIP, which are down.</td><tr><tr><td>vipvsrvrrhiactivecount</td><td>&lt;Double></td><td>Read-only</td><td>Number of vservers that have RHI state ACTIVE.</td><tr><tr><td>vipvsrvrrhiactiveupcount</td><td>&lt;Double></td><td>Read-only</td><td>Number of vservers that have RHI state ACTIVE, which are UP.</td><tr><tr><td>freeports</td><td>&lt;Double></td><td>Read-only</td><td>Number of free Ports available on this IP.</td><tr><tr><td>riserhimsgcode</td><td>&lt;Integer></td><td>Read-only</td><td>The code indicating the rise rhi status.</td><tr><tr><td>iptype</td><td>&lt;String[]></td><td>Read-only</td><td>.&lt;br>Possible values = SNIP, VIP, NSIP, GSLBsiteIP, CLIP</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [DELETE](#delete) | [UPDATE](#update) | [UNSET](#unset) | [ENABLE](#enable) | [DISABLE](#disable) | [GET (ALL)](#get-(all)) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsip
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"nsip":{      "ipaddress":<String_value>,      "netmask":<String_value>,      "type":<String_value>,      "arp":<String_value>,      "icmp":<String_value>,      "vserver":<String_value>,      "telnet":<String_value>,      "ftp":<String_value>,      "gui":<String_value>,      "ssh":<String_value>,      "snmp":<String_value>,      "mgmtaccess":<String_value>,      "restrictaccess":<String_value>,      "dynamicrouting":<String_value>,      "ospf":<String_value>,      "bgp":<String_value>,      "rip":<String_value>,      "hostroute":<String_value>,      "hostrtgw":<String_value>,      "metric":<Integer_value>,      "vserverrhilevel":<String_value>,      "vserverrhimode":<String_value>,      "ospflsatype":<String_value>,      "ospfarea":<Double_value>,      "state":<String_value>,      "vrid":<Double_value>,      "icmpresponse":<String_value>,      "ownernode":<Double_value>,      "arpresponse":<String_value>,      "td":<Double_value>}}```
Response:
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsip/ipaddress_value&lt;String&gt;
HTTP Method: DELETE
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsip
HTTP Method: PUT
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"nsip":{      "ipaddress":<String_value>,      "td":<Double_value>,      "netmask":<String_value>,      "arp":<String_value>,      "icmp":<String_value>,      "vserver":<String_value>,      "telnet":<String_value>,      "ftp":<String_value>,      "gui":<String_value>,      "ssh":<String_value>,      "snmp":<String_value>,      "mgmtaccess":<String_value>,      "restrictaccess":<String_value>,      "dynamicrouting":<String_value>,      "ospf":<String_value>,      "bgp":<String_value>,      "rip":<String_value>,      "hostroute":<String_value>,      "hostrtgw":<String_value>,      "metric":<Integer_value>,      "vserverrhilevel":<String_value>,      "vserverrhimode":<String_value>,      "ospflsatype":<String_value>,      "ospfarea":<Double_value>,      "vrid":<Double_value>,      "icmpresponse":<String_value>,      "arpresponse":<String_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsip?action=unset
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"nsip":{      "ipaddress":<String_value>,      "td":<Double_value>,      "ospfarea":true,      "hostrtgw":true,      "netmask":true,      "arp":true,      "icmp":true,      "vserver":true,      "telnet":true,      "ftp":true,      "gui":true,      "ssh":true,      "snmp":true,      "mgmtaccess":true,      "restrictaccess":true,      "dynamicrouting":true,      "ospf":true,      "bgp":true,      "rip":true,      "hostroute":true,      "metric":true,      "vserverrhilevel":true,      "vserverrhimode":true,      "ospflsatype":true,      "vrid":true,      "icmpresponse":true,      "arpresponse":true}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###enable



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsip?action=enable
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"nsip":{      "ipaddress":<String_value>,      "td":<Double_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###disable



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsip?action=disable
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"nsip":{      "ipaddress":<String_value>,      "td":<Double_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsip
Query-parameters:
args
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsip?args=ipaddress:&lt;String_value&gt;,td:&lt;Double_value&gt;,type:&lt;String_value&gt;
Use this query-parameter to get nsip resources based on additional properties.


attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsip?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


filter
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsip?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of nsip resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsip?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).


pagination
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsip?pagesize=#no;pageno=#no
Use this query-parameter to get the nsip resources in chunks.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "nsip": [ {ipaddress:<String_value>,td:<Double_value>,type:<String_value>      "netmask":<String_value>,      "flags":<Double_value>,      "arp":<String_value>,      "icmp":<String_value>,      "vserver":<String_value>,      "telnet":<String_value>,      "ssh":<String_value>,      "gui":<String_value>,      "snmp":<String_value>,      "ftp":<String_value>,      "mgmtaccess":<String_value>,      "restrictaccess":<String_value>,      "dynamicrouting":<String_value>,      "bgp":<String_value>,      "ospf":<String_value>,      "rip":<String_value>,      "hostroute":<String_value>,      "hostrtgw":<String_value>,      "hostrtgwact":<String_value>,      "metric":<Integer_value>,      "ospfarea":<Double_value>,      "ospfareaval":<Double_value>,      "vserverrhilevel":<String_value>,      "vserverrhimode":<String_value>,      "viprtadv2bsd":<Boolean_value>,      "vipvsercount":<Double_value>,      "vipvserdowncount":<Double_value>,      "vipvsrvrrhiactivecount":<Double_value>,      "vipvsrvrrhiactiveupcount":<Double_value>,      "ospflsatype":<String_value>,      "state":<String_value>,      "freeports":<Double_value>,      "vrid":<Double_value>,      "riserhimsgcode":<Integer_value>,      "iptype":<String[]_value>,      "icmpresponse":<String_value>,      "ownernode":<Double_value>,      "arpresponse":<String_value>}]}```



###count



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsip?count=yes
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: 
{ "nsip": [ { "__count": "#no"} ] }


