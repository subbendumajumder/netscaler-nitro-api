#lldpneighbors

Configuration for lldp neighbors resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>ifnum</td><td>&lt;String></td><td>Read-write</td><td>Interface Name.</td><tr><tr><td>nodeid</td><td>&lt;Double></td><td>Read-write</td><td>Unique number that identifies the cluster node.&lt;br>Minimum value = 0&lt;br>Maximum value = 31</td><tr><tr><td>chassisidsubtype</td><td>&lt;String></td><td>Read-only</td><td>Chassis id sub type.&lt;br>Possible values = NONE, Component, Interface Alias, Port Component, MAC Address, Network Address, Interface Name, Locally Assigned</td><tr><tr><td>chassisid</td><td>&lt;String></td><td>Read-only</td><td>Chassis Id.</td><tr><tr><td>portidsubtype</td><td>&lt;String></td><td>Read-only</td><td>Port id subtype.&lt;br>Possible values = NONE, Interface Alias, Port Component, MAC Address, Network Address, Interface Name, Agent Circuit ID, Locally Assigned</td><tr><tr><td>portid</td><td>&lt;String></td><td>Read-only</td><td>Port Id.</td><tr><tr><td>ttl</td><td>&lt;Double></td><td>Read-only</td><td>Time to Live.</td><tr><tr><td>portdescription</td><td>&lt;String></td><td>Read-only</td><td>Port Description.</td><tr><tr><td>sys</td><td>&lt;String></td><td>Read-only</td><td>System Name.</td><tr><tr><td>sysdesc</td><td>&lt;String></td><td>Read-only</td><td>System Description.</td><tr><tr><td>mgmtaddresssubtype</td><td>&lt;String></td><td>Read-only</td><td>Management Address Type.&lt;br>Possible values = OTHER, IPv4, IPv6</td><tr><tr><td>mgmtaddress</td><td>&lt;String></td><td>Read-only</td><td>Management Address.</td><tr><tr><td>iftype</td><td>&lt;String></td><td>Read-only</td><td>Interface subtype.&lt;br>Possible values = UNKNOWN, ifIndex, system port number</td><tr><tr><td>ifnumber</td><td>&lt;Double></td><td>Read-only</td><td>Interface Number.</td><tr><tr><td>vlan</td><td>&lt;String></td><td>Read-only</td><td>vlan name.</td><tr><tr><td>vlanid</td><td>&lt;Double></td><td>Read-only</td><td>Vlan Id.</td><tr><tr><td>portprotosupported</td><td>&lt;Double></td><td>Read-only</td><td>Flag to show Port Protocol Support.</td><tr><tr><td>portprotoenabled</td><td>&lt;Double></td><td>Read-only</td><td>Flag to show Port Protocol support enabled.</td><tr><tr><td>portprotoid</td><td>&lt;Double></td><td>Read-only</td><td>Port Protocol ID.</td><tr><tr><td>portvlanid</td><td>&lt;Double></td><td>Read-only</td><td>Port Vlan Id.</td><tr><tr><td>protocolid</td><td>&lt;String></td><td>Read-only</td><td>port vlan id name.</td><tr><tr><td>linkaggrcapable</td><td>&lt;String></td><td>Read-only</td><td>Is neighbor Link Aggregation Capable.&lt;br>Possible values = NO, YES</td><tr><tr><td>linkaggrenabled</td><td>&lt;String></td><td>Read-only</td><td>Is link aggregation Enabled.&lt;br>Possible values = NO, YES</td><tr><tr><td>linkaggrid</td><td>&lt;Double></td><td>Read-only</td><td>Link Aggregation Id.</td><tr><tr><td>flag</td><td>&lt;Double></td><td>Read-only</td><td>.</td><tr><tr><td>syscapabilities</td><td>&lt;String></td><td>Read-only</td><td>Acronyms for remote system capabilities:&lt;br>OT : Other.&lt;br>RE : Repeater(IETF RFC 2108).&lt;br>BR : MAC Bridge(IEEE Std 802.1D).&lt;br>WL : WLAN Access Point(IEEE Std 802.11 MIB).&lt;br>RO : ROuter(IETF RFC 1812).&lt;br>TE : Telephone(IETF RFC 4293).&lt;br>DO : DOCSIS cable device(IETF RFC 4639 and IETF RFC 4546).&lt;br>ST : STation only(IETF RFC 4293).&lt;br>CV : C-VLAN component of a VLAN Bridge(IEEE Std 802.1Q).&lt;br>SV : S-VLAN component of a VLAN Bridge(IEEE Std 802.1Q).&lt;br>MR : Two port MAC Relay(IEEE Std 802.1Q).</td><tr><tr><td>syscapenabled</td><td>&lt;String></td><td>Read-only</td><td>Acronyms for remote system enabled capabilities:&lt;br>OT : Other.&lt;br>RE : Repeater(IETF RFC 2108).&lt;br>BR : MAC Bridge(IEEE Std 802.1D).&lt;br>WL : WLAN Access Point(IEEE Std 802.11 MIB).&lt;br>RO : ROuter(IETF RFC 1812).&lt;br>TE : Telephone(IETF RFC 4293).&lt;br>DO : DOCSIS cable device(IETF RFC 4639 and IETF RFC 4546).&lt;br>ST : STation only(IETF RFC 4293).&lt;br>CV : C-VLAN component of a VLAN Bridge(IEEE Std 802.1Q).&lt;br>SV : S-VLAN component of a VLAN Bridge(IEEE Std 802.1Q).&lt;br>MR : Two port MAC Relay(IEEE Std 802.1Q).</td><tr><tr><td>autonegsupport</td><td>&lt;String></td><td>Read-only</td><td>MAC/PHY autonegotiation support.&lt;br>Possible values = NO, YES</td><tr><tr><td>autonegenabled</td><td>&lt;String></td><td>Read-only</td><td>MAC/PHY autonegotiation enabled.&lt;br>Possible values = NO, YES</td><tr><tr><td>autonegadvertised</td><td>&lt;String></td><td>Read-only</td><td>MAC/PHY autonegotiation advetised.</td><tr><tr><td>autonegmautype</td><td>&lt;String></td><td>Read-only</td><td>MAC/PHY Medium Attachment Unit (MAU) type of the port. Description listed below:&lt;br>AUI - no internal MAU, view from AUI&lt;br>10Base5 - thick coax MAU&lt;br>Foirl - FOIRL MAU&lt;br>10Base2 - thin coax MAU&lt;br>10BaseT - UTP MAU&lt;br>10BaseFP - passive fiber MAU&lt;br>10BaseFB - sync fiber MAU&lt;br>10BaseFL - async fiber MAU&lt;br>10Broad36 - broadband DTE MAU&lt;br>10BaseTHD - UTP MAU, half duplex mode&lt;br>10BaseTFD - UTP MAU, full duplex mode&lt;br>10BaseFLHD - async fiber MAU, half duplex mode&lt;br>10BaseFLDF - async fiber MAU, full duplex mode&lt;br>10BaseT4 - 4 pair category 3 UTP&lt;br>100BaseTXHD - 2 pair category 5 UTP, half duplex mode&lt;br>100BaseTXFD - 2 pair category 5 UTP, full duplex mode&lt;br>100BaseFXHD - X fiber over PMT, half duplex mode&lt;br>100BaseFXFD - X fiber over PMT, full duplex mode&lt;br>100BaseT2HD - 2 pair category 3 UTP, half duplex mode&lt;br>100BaseT2DF - 2 pair category 3 UTP, full duplex mode&lt;br>1000BaseXHD - PCS/PMA, unknown PMD, half duplex mode&lt;br>1000BaseXFD - PCS/PMA, unknown PMD, full duplex mode&lt;br>1000BaseLXHD - Fiber over long-wavelength laser, half duplex mode&lt;br>1000BaseLXFD - Fiber over long-wavelength laser, full duplex mode&lt;br>1000BaseSXHD - Fiber over short-wavelength laser, half duplex mode&lt;br>1000BaseSXFD - Fiber over short-wavelength laser, full duplex mode&lt;br>1000BaseCXHD - Copper over 150-Ohm balanced cable, half duplex mode&lt;br>1000BaseCXFD - Copper over 150-Ohm balanced cable, full duplex mode&lt;br>1000BaseTHD - Four-pair Category 5 UTP, half duplex mode&lt;br>1000BaseTFD - Four-pair Category 5 UTP, full duplex mode&lt;br>10GigBaseX - X PCS/PMA, unknown PMD&lt;br>10GigBaseLX4 - X fiber over WWDM optics&lt;br>10GigBaseR - R PCS/PMA, unknown PMD&lt;br>10GigBaseER - R fiber over 1550 nm optics&lt;br>10GigBaseLR - R fiber over 1310 nm optics&lt;br>10GigBaseSR - R fiber over 850 nm optics&lt;br>10GigBaseW - W PCS/PMA, unknown PMD&lt;br>10GigBaseEW - W fiber over 1550 nm optics&lt;br>10GigBaseLW - W fiber over 1310 nm optics&lt;br>10GigBaseSW - W fiber over 850 nm optics.&lt;br>Possible values = Not Recieved, AUI, 10Base5, Foirl, 10Base2, 10BaseT, 10BaseFP, 10BaseFB, 10BaseFL, 10Broad36, 10BaseTHD, 10BaseTFD, 10BaseFLHD, 10BaseFLDF, 10BaseT4, 100BaseTXHD, 100BaseTXFD, 100BaseFXHD, 100BaseFXFD, 100BaseT2HD, 100BaseT2DF, 1000BaseXHD, 1000BaseXFD, 1000BaseLXHD, 1000BaseLXFD, 1000BaseSXHD, 1000BaseSXFD, 1000BaseCXHD, 1000BaseCXFD, 1000BaseTHD, 1000BaseTFD, 10GigBaseX, 10GigBaseLX4, 10GigBaseR, 10GigBaseER, 10GigBaseLR, 10GigBaseSR, 10GigBaseW, 10GigBaseEW, 10GigBaseLW, 10GigBaseSW</td><tr><tr><td>mtu</td><td>&lt;Double></td><td>Read-only</td><td>MTU of Remote Device.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[CLEAR](#clear) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###clear



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lldpneighbors?action=clear
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"lldpneighbors":{}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lldpneighbors
Query-parameters:
args
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lldpneighbors?args=ifnum:&lt;String_value&gt;,nodeid:&lt;Double_value&gt;
Use this query-parameter to get lldpneighbors resources based on additional properties.


attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lldpneighbors?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


filter
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lldpneighbors?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of lldpneighbors resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lldpneighbors?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).


pagination
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lldpneighbors?pagesize=#no;pageno=#no
Use this query-parameter to get the lldpneighbors resources in chunks.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "lldpneighbors": [ {ifnum:<String_value>,nodeid:<Double_value>      "chassisidsubtype":<String_value>,      "chassisid":<String_value>,      "portidsubtype":<String_value>,      "portid":<String_value>,      "ttl":<Double_value>,      "portdescription":<String_value>,      "sys":<String_value>,      "sysdesc":<String_value>,      "mgmtaddresssubtype":<String_value>,      "mgmtaddress":<String_value>,      "iftype":<String_value>,      "ifnumber":<Double_value>,      "vlan":<String_value>,      "vlanid":<Double_value>,      "portprotosupported":<Double_value>,      "portprotoenabled":<Double_value>,      "portprotoid":<Double_value>,      "portvlanid":<Double_value>,      "protocolid":<String_value>,      "linkaggrcapable":<String_value>,      "linkaggrenabled":<String_value>,      "linkaggrid":<Double_value>,      "flag":<Double_value>,      "syscapabilities":<String_value>,      "syscapenabled":<String_value>,      "autonegsupport":<String_value>,      "autonegenabled":<String_value>,      "autonegadvertised":<String_value>,      "autonegmautype":<String_value>,      "mtu":<Double_value>}]}```



###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lldpneighbors/ifnum_value&lt;String&gt;
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lldpneighbors/ifnum_value&lt;String&gt;?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lldpneighbors/ifnum_value&lt;String&gt;?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "lldpneighbors": [ {ifnum:<String_value>,nodeid:<Double_value>      "chassisidsubtype":<String_value>,      "chassisid":<String_value>,      "portidsubtype":<String_value>,      "portid":<String_value>,      "ttl":<Double_value>,      "portdescription":<String_value>,      "sys":<String_value>,      "sysdesc":<String_value>,      "mgmtaddresssubtype":<String_value>,      "mgmtaddress":<String_value>,      "iftype":<String_value>,      "ifnumber":<Double_value>,      "vlan":<String_value>,      "vlanid":<Double_value>,      "portprotosupported":<Double_value>,      "portprotoenabled":<Double_value>,      "portprotoid":<Double_value>,      "portvlanid":<Double_value>,      "protocolid":<String_value>,      "linkaggrcapable":<String_value>,      "linkaggrenabled":<String_value>,      "linkaggrid":<Double_value>,      "flag":<Double_value>,      "syscapabilities":<String_value>,      "syscapenabled":<String_value>,      "autonegsupport":<String_value>,      "autonegenabled":<String_value>,      "autonegadvertised":<String_value>,      "autonegmautype":<String_value>,      "mtu":<Double_value>}]}```



###count



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lldpneighbors?count=yes
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: 
{ "lldpneighbors": [ { "__count": "#no"} ] }


