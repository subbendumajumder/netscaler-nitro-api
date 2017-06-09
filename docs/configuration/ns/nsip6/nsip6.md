#nsip6

Configuration for ip6 resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>ipv6address</td><td>&lt;String></td><td>Read-write</td><td>IPv6 address to create on the NetScaler appliance.&lt;br>Minimum length = 1</td><tr><tr><td>scope</td><td>&lt;String></td><td>Read-write</td><td>Scope of the IPv6 address to be created. Cannot be changed after the IP address is created.&lt;br>Default value: global&lt;br>Possible values = global, link-local</td><tr><tr><td>type</td><td>&lt;String></td><td>Read-write</td><td>Type of IP address to be created on the NetScaler appliance. Cannot be changed after the IP address is created.&lt;br>Default value: SNIP&lt;br>Possible values = NSIP, VIP, SNIP, GSLBsiteIP, ADNSsvcIP, RADIUSListenersvcIP, CLIP</td><tr><tr><td>vlan</td><td>&lt;Double></td><td>Read-write</td><td>The VLAN number.&lt;br>Default value: 0&lt;br>Minimum value = 0&lt;br>Maximum value = 4094</td><tr><tr><td>nd</td><td>&lt;String></td><td>Read-write</td><td>Respond to Neighbor Discovery (ND) requests for this IP address.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>icmp</td><td>&lt;String></td><td>Read-write</td><td>Respond to ICMP requests for this IP address.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>vserver</td><td>&lt;String></td><td>Read-write</td><td>Enable or disable the state of all the virtual servers associated with this VIP6 address.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>telnet</td><td>&lt;String></td><td>Read-write</td><td>Allow Telnet access to this IP address.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>ftp</td><td>&lt;String></td><td>Read-write</td><td>Allow File Transfer Protocol (FTP) access to this IP address.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>gui</td><td>&lt;String></td><td>Read-write</td><td>Allow graphical user interface (GUI) access to this IP address.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, SECUREONLY, DISABLED</td><tr><tr><td>ssh</td><td>&lt;String></td><td>Read-write</td><td>Allow secure Shell (SSH) access to this IP address.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>snmp</td><td>&lt;String></td><td>Read-write</td><td>Allow Simple Network Management Protocol (SNMP) access to this IP address.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>mgmtaccess</td><td>&lt;String></td><td>Read-write</td><td>Allow access to management applications on this IP address.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>restrictaccess</td><td>&lt;String></td><td>Read-write</td><td>Block access to nonmanagement applications on this IP address. This option is applicable forMIP6s, SNIP6s, and NSIP6s, and is disabled by default. Nonmanagement applications can run on the underlying NetScaler Free BSD operating system.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>dynamicrouting</td><td>&lt;String></td><td>Read-write</td><td>Allow dynamic routing on this IP address. Specific to Subnet IPv6 (SNIP6) address.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>hostroute</td><td>&lt;String></td><td>Read-write</td><td>Advertise a route for the VIP6 address by using the dynamic routing protocols running on the NetScaler appliance.&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>ip6hostrtgw</td><td>&lt;String></td><td>Read-write</td><td>IPv6 address of the gateway for the route. If Gateway is not set, VIP uses :: as the gateway.&lt;br>Default value: 0</td><tr><tr><td>metric</td><td>&lt;Integer></td><td>Read-write</td><td>Integer value to add to or subtract from the cost of the route advertised for the VIP6 address.&lt;br>Minimum value = -16777215</td><tr><tr><td>vserverrhilevel</td><td>&lt;String></td><td>Read-write</td><td>Advertise or do not advertise the route for the Virtual IP (VIP6) address on the basis of the state of the virtual servers associated with that VIP6. * NONE - Advertise the route for the VIP6 address, irrespective of the state of the virtual servers associated with the address. * ONE VSERVER - Advertise the route for the VIP6 address if at least one of the associated virtual servers is in UP state. * ALL VSERVER - Advertise the route for the VIP6 address if all of the associated virtual servers are in UP state. * VSVR_CNTRLD. Advertise the route for the VIP address according to the RHIstate (RHI STATE) parameter setting on all the associated virtual servers of the VIP address along with their states. When Vserver RHI Level (RHI) parameter is set to VSVR_CNTRLD, the following are different RHI behaviors for the VIP address on the basis of RHIstate (RHI STATE) settings on the virtual servers associated with the VIP address: * If you set RHI STATE to PASSIVE on all virtual servers, the NetScaler ADC always advertises the route for the VIP address. * If you set RHI STATE to ACTIVE on all virtual servers, the NetScaler ADC advertises the route for the VIP address if at least one of the associated virtual servers is in UP state. *If you set RHI STATE to ACTIVE on some and PASSIVE on others, the NetScaler ADC advertises the route for the VIP address if at least one of the associated virtual servers, whose RHI STATE set to ACTIVE, is in UP state.&lt;br>Default value: ONE_VSERVER&lt;br>Possible values = ONE_VSERVER, ALL_VSERVERS, NONE, VSVR_CNTRLD</td><tr><tr><td>ospf6lsatype</td><td>&lt;String></td><td>Read-write</td><td>Type of LSAs to be used by the IPv6 OSPF protocol, running on the NetScaler appliance, for advertising the route for the VIP6 address.&lt;br>Default value: EXTERNAL&lt;br>Possible values = INTRA_AREA, EXTERNAL</td><tr><tr><td>ospfarea</td><td>&lt;Double></td><td>Read-write</td><td>ID of the area in which the Intra-Area-Prefix LSAs are to be advertised for the VIP6 address by the IPv6 OSPF protocol running on the NetScaler appliance. When ospfArea is not set, VIP6 is advertised on all areas.&lt;br>Default value: -1&lt;br>Minimum value = 0&lt;br>Maximum value = 4294967294LU</td><tr><tr><td>state</td><td>&lt;String></td><td>Read-write</td><td>Enable or disable the IP address.&lt;br>Default value: ENABLED&lt;br>Possible values = DISABLED, ENABLED</td><tr><tr><td>map</td><td>&lt;String></td><td>Read-write</td><td>Mapped IPV4 address for the IPV6 address.</td><tr><tr><td>ownernode</td><td>&lt;Double></td><td>Read-write</td><td>ID of the cluster node for which you are adding the IP address. Must be used if you want the IP address to be active only on the specific node. Can be configured only through the cluster IP address. Cannot be changed after the IP address is created.&lt;br>Default value: 255</td><tr><tr><td>td</td><td>&lt;Double></td><td>Read-write</td><td>Integer value that uniquely identifies the traffic domain in which you want to configure the entity. If you do not specify an ID, the entity becomes part of the default traffic domain, which has an ID of 0.&lt;br>Minimum value = 0&lt;br>Maximum value = 4094</td><tr><tr><td>iptype</td><td>&lt;String[]></td><td>Read-only</td><td>The type of the IPv6 address.&lt;br>Possible values = NSIP, VIP, SNIP, GSLBsiteIP, ADNSsvcIP, RADIUSListenersvcIP, CLIP</td><tr><tr><td>curstate</td><td>&lt;String></td><td>Read-only</td><td>Current state of this IP.&lt;br>Default value: ENABLED&lt;br>Possible values = DISABLED, ENABLED</td><tr><tr><td>viprtadv2bsd</td><td>&lt;Boolean></td><td>Read-only</td><td>Whether this route is advertised to FreeBSD.</td><tr><tr><td>vipvsercount</td><td>&lt;Double></td><td>Read-only</td><td>Number of vservers bound to this VIP.</td><tr><tr><td>vipvserdowncount</td><td>&lt;Double></td><td>Read-only</td><td>Number of vservers bound to this VIP, which are down.</td><tr><tr><td>systemtype</td><td>&lt;String></td><td>Read-only</td><td>The type of the System. Possible Values: Standalone, HA, Cluster. Used for display purpose.&lt;br>Possible values = Stand-alone, HA, Cluster</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [DELETE](#delete) | [UPDATE](#update) | [UNSET](#unset) | [GET (ALL)](#get-(all)) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>},"sessionid":"##sessionid","nsip6":{      "ipv6address":<String_value>,      "scope":<String_value>,      "type":<String_value>,      "vlan":<Double_value>,      "nd":<String_value>,      "icmp":<String_value>,      "vserver":<String_value>,      "telnet":<String_value>,      "ftp":<String_value>,      "gui":<String_value>,      "ssh":<String_value>,      "snmp":<String_value>,      "mgmtaccess":<String_value>,      "restrictaccess":<String_value>,      "dynamicrouting":<String_value>,      "hostroute":<String_value>,      "ip6hostrtgw":<String_value>,      "metric":<Integer_value>,      "vserverrhilevel":<String_value>,      "ospf6lsatype":<String_value>,      "ospfarea":<Double_value>,      "state":<String_value>,      "map":<String_value>,      "ownernode":<Double_value>,      "td":<Double_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/nsip6/ipv6address_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/nsip6/ipv6address_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","nsip6":{      "ipv6address":<String_value>,                  "td":<Double_value>,      "nd":<String_value>,      "icmp":<String_value>,      "vserver":<String_value>,      "telnet":<String_value>,      "ftp":<String_value>,      "gui":<String_value>,      "ssh":<String_value>,      "snmp":<String_value>,      "mgmtaccess":<String_value>,      "restrictaccess":<String_value>,      "state":<String_value>,      "map":<String_value>,      "dynamicrouting":<String_value>,      "hostroute":<String_value>,                  "ip6hostrtgw":<String_value>,                  "metric":<Integer_value>,                  "vserverrhilevel":<String_value>,                  "ospf6lsatype":<String_value>,                  "ospfarea":<Double_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","nsip6":{      "ipv6address":<String_value>,      "td":<Double_value>,      "ospfarea":true,      "nd":true,      "icmp":true,      "vserver":true,      "telnet":true,      "ftp":true,      "gui":true,      "ssh":true,      "snmp":true,      "mgmtaccess":true,      "restrictaccess":true,      "state":true,      "map":true,      "dynamicrouting":true,      "hostroute":true,      "ip6hostrtgw":true,      "metric":true,      "vserverrhilevel":true,      "ospf6lsatype":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/nsip6
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/nsip6?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of nsip6 resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/nsip6?view=summary
Use this query-parameter to get the summary output of nsip6 resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/nsip6?pagesize=#no;pageno=#no
Use this query-parameter to get the nsip6 resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/nsip6?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "nsip6": [ {      "ipv6address":<String_value>,                  "td":<Double_value>,      "scope":<String_value>,      "type":<String_value>,      "iptype":<String[]_value>,      "vlan":<Double_value>,      "nd":<String_value>,      "icmp":<String_value>,      "vserver":<String_value>,      "telnet":<String_value>,      "ssh":<String_value>,      "gui":<String_value>,      "snmp":<String_value>,      "ftp":<String_value>,      "mgmtaccess":<String_value>,      "restrictaccess":<String_value>,      "state":<String_value>,      "curstate":<String_value>,      "map":<String_value>,      "dynamicrouting":<String_value>,      "hostroute":<String_value>,      "ip6hostrtgw":<String_value>,      "metric":<Integer_value>,      "vserverrhilevel":<String_value>,      "viprtadv2bsd":<Boolean_value>,      "vipvsercount":<Double_value>,      "vipvserdowncount":<Double_value>,      "ospf6lsatype":<String_value>,      "ospfarea":<Double_value>,      "ownernode":<Double_value>,      "systemtype":<String_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/nsip6?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",nsip6: [ { "__count": "#no"} ] }


