#channel_interface_binding

Binding object showing the interface that can be bound to channel.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>ID of the LA channel or the cluster LA channel to which you want to bind interfaces. Specify an LA channel in LA/x notation, where x can range from 1 to 8 or a cluster LA channel in CLA/x notation or Link redundant channel in LR/x notation , where x can range from 1 to 4.</td><tr><tr><td>ifnum</td><td>&lt;String[]></td><td>Read-write</td><td>Interfaces to be bound to the LA channel of a NetScaler appliance or to the LA channel of a cluster configuration. For an LA channel of a NetScaler appliance, specify an interface in C/U notation (for example, 1/3). For an LA channel of a cluster configuration, specify an interface in N/C/U notation (for example, 2/1/3). where C can take one of the following values: * 0 - Indicates a management interface. * 1 - Indicates a 1 Gbps port. * 10 - Indicates a 10 Gbps port. U is a unique integer for representing an interface in a particular port group. N is the ID of the node to which an interface belongs in a cluster configuration. Use spaces to separate multiple entries.</td><tr><tr><td>lamode</td><td>&lt;String></td><td>Read-only</td><td>The mode(AUTO/MANNUAL) for the LA channel.&lt;br>Possible values = MANUAL, AUTO</td><tr><tr><td>slaveduplex</td><td>&lt;Double></td><td>Read-only</td><td>Duplex of the member interfaces.</td><tr><tr><td>slaveflowctl</td><td>&lt;Double></td><td>Read-only</td><td>Flowcontrol of the member interfaces.</td><tr><tr><td>slavetime</td><td>&lt;Double></td><td>Read-only</td><td>UP time of the member interfaces.</td><tr><tr><td>slavestate</td><td>&lt;Double></td><td>Read-only</td><td>State of the member interfaces.</td><tr><tr><td>slavespeed</td><td>&lt;Double></td><td>Read-only</td><td>Speed of the member interfaces.</td><tr><tr><td>slavemedia</td><td>&lt;Double></td><td>Read-only</td><td>Media type of the member interfaces.</td><tr><tr><td>lractiveintf</td><td>&lt;Boolean></td><td>Read-only</td><td>LR set member interface state(active/inactive).</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD:](#add:) | [DELETE:](#delete:) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add:



URL: http://NS_IP/nitro/v1/config
HTTP Method: PUT
Request Payload: ```{"params":{      "warning":<String_value>,      "onerror":<String_value>},sessionid":"##sessionid","channel_interface_binding":{      "id":<String_value>,      "ifnum":<String[]_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete:



URL: http://&lt;NS_IP&gt;/nitro/v1/config/channel_interface_binding/id_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/channel_interface_binding/id_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/channel_interface_binding/id_value&lt;String&gt;
Query-parameters:
filter
http://&lt;NS_IP&gt;/nitro/v1/config/channel_interface_binding/id_value&lt;String&gt;?filter=property-name1:property-value1,property-name2:property-value2
Use this query-parameter to get the filtered set of channel_interface_binding resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/channel_interface_binding/id_value&lt;String&gt;?pagesize=#no;pageno=#no
Use this query-parameter to get the channel_interface_binding resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/channel_interface_binding?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "channel_interface_binding": [ {      "id":<String_value>,      "ifnum":<String[]_value>,      "lamode":<String_value>,      "slaveduplex":<Double_value>,      "slaveflowctl":<Double_value>,      "slavetime":<Double_value>,      "slavestate":<Double_value>,      "slavespeed":<Double_value>,      "slavemedia":<Double_value>,      "lractiveintf":<Boolean_value>,}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/channel_interface_binding/id_value&lt;String&gt;?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",channel_interface_binding: [ { "__count": "#no"} ] }


