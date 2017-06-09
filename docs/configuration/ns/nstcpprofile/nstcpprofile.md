#nstcpprofile

Configuration for TCP profile resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for a TCP profile. Must begin with a letter, number, or the underscore \\(_\\) character. Other characters allowed, after the first character, are the hyphen \\(-\\), period \\(.\\), hash \\(\\#\\), space \\( \\), at \\(@\\), colon \\(:\\), and equal \\(=\\) characters. The name of a TCP profile cannot be changed after it is created. CLI Users: If the name includes one or more spaces, enclose the name in double or single quotation marks \\(for example, "my tcp profile" or my tcp profile\\).&lt;br>Minimum length = 1&lt;br>Maximum length = 127</td><tr><tr><td>ws</td><td>&lt;String></td><td>Read-write</td><td>Enable or disable window scaling.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>sack</td><td>&lt;String></td><td>Read-write</td><td>Enable or disable Selective ACKnowledgement (SACK).&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>wsval</td><td>&lt;Double></td><td>Read-write</td><td>Factor used to calculate the new window size. This argument is needed only when window scaling is enabled.&lt;br>Default value: 4&lt;br>Minimum value = 0&lt;br>Maximum value = 14</td><tr><tr><td>nagle</td><td>&lt;String></td><td>Read-write</td><td>Enable or disable the Nagle algorithm on TCP connections.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>ackonpush</td><td>&lt;String></td><td>Read-write</td><td>Send immediate positive acknowledgement (ACK) on receipt of TCP packets with PUSH flag.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>mss</td><td>&lt;Double></td><td>Read-write</td><td>Maximum number of octets to allow in a TCP data segment.&lt;br>Minimum value = 0&lt;br>Maximum value = 9176</td><tr><tr><td>maxburst</td><td>&lt;Double></td><td>Read-write</td><td>Maximum number of TCP segments allowed in a burst.&lt;br>Default value: 6&lt;br>Minimum value = 1&lt;br>Maximum value = 255</td><tr><tr><td>initialcwnd</td><td>&lt;Double></td><td>Read-write</td><td>Initial maximum upper limit on the number of TCP packets that can be outstanding on the TCP link to the server.&lt;br>Default value: 4&lt;br>Minimum value = 1&lt;br>Maximum value = 44</td><tr><tr><td>delayedack</td><td>&lt;Double></td><td>Read-write</td><td>Timeout for TCP delayed ACK, in milliseconds.&lt;br>Default value: 100&lt;br>Minimum value = 10&lt;br>Maximum value = 300</td><tr><tr><td>oooqsize</td><td>&lt;Double></td><td>Read-write</td><td>Maximum size of out-of-order packets queue. A value of 0 means no limit.&lt;br>Default value: 64&lt;br>Minimum value = 0&lt;br>Maximum value = 65535</td><tr><tr><td>maxpktpermss</td><td>&lt;Double></td><td>Read-write</td><td>Maximum number of TCP packets allowed per maximum segment size (MSS).&lt;br>Minimum value = 0&lt;br>Maximum value = 1460</td><tr><tr><td>pktperretx</td><td>&lt;Double></td><td>Read-write</td><td>Maximum limit on the number of packets that should be retransmitted on receiving a partial ACK.&lt;br>Default value: 1&lt;br>Minimum value = 1&lt;br>Maximum value = 512</td><tr><tr><td>minrto</td><td>&lt;Double></td><td>Read-write</td><td>Minimum retransmission timeout, in milliseconds, specified in 10-millisecond increments (value must yield a whole number if divided by 10).&lt;br>Default value: 1000&lt;br>Minimum value = 10&lt;br>Maximum value = 64000</td><tr><tr><td>slowstartincr</td><td>&lt;Double></td><td>Read-write</td><td>Multiplier that determines the rate at which slow start increases the size of the TCP transmission window after each acknowledgement of successful transmission.&lt;br>Default value: 2&lt;br>Minimum value = 1&lt;br>Maximum value = 100</td><tr><tr><td>buffersize</td><td>&lt;Double></td><td>Read-write</td><td>TCP buffering size, in bytes.&lt;br>Default value: 8190&lt;br>Minimum value = 8190&lt;br>Maximum value = 20971520</td><tr><tr><td>syncookie</td><td>&lt;String></td><td>Read-write</td><td>Enable or disable the SYNCOOKIE mechanism for TCP handshake with clients. Disabling SYNCOOKIE prevents SYN attack protection on the NetScaler appliance.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>kaprobeupdatelastactivity</td><td>&lt;String></td><td>Read-write</td><td>Update last activity for the connection after receiving keep-alive (KA) probes.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>flavor</td><td>&lt;String></td><td>Read-write</td><td>Set TCP congestion control algorithm.&lt;br>Default value: Default&lt;br>Possible values = Default, Westwood, BIC, CUBIC, Nile</td><tr><tr><td>dynamicreceivebuffering</td><td>&lt;String></td><td>Read-write</td><td>Enable or disable dynamic receive buffering. When enabled, allows the receive buffer to be adjusted dynamically based on memory and network conditions. Note: The buffer size argument must be set for dynamic adjustments to take place.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>ka</td><td>&lt;String></td><td>Read-write</td><td>Send periodic TCP keep-alive (KA) probes to check if peer is still up.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>kaconnidletime</td><td>&lt;Double></td><td>Read-write</td><td>Duration, in seconds, for the connection to be idle, before sending a keep-alive (KA) probe.&lt;br>Minimum value = 1&lt;br>Maximum value = 4095</td><tr><tr><td>kamaxprobes</td><td>&lt;Double></td><td>Read-write</td><td>Number of keep-alive (KA) probes to be sent when not acknowledged, before assuming the peer to be down.&lt;br>Minimum value = 1&lt;br>Maximum value = 255</td><tr><tr><td>kaprobeinterval</td><td>&lt;Double></td><td>Read-write</td><td>Time interval, in seconds, before the next keep-alive (KA) probe, if the peer does not respond.&lt;br>Minimum value = 1&lt;br>Maximum value = 4095</td><tr><tr><td>sendbuffsize</td><td>&lt;Double></td><td>Read-write</td><td>TCP Send Buffer Size.&lt;br>Default value: 8190&lt;br>Minimum value = 8190&lt;br>Maximum value = 20971520</td><tr><tr><td>mptcp</td><td>&lt;String></td><td>Read-write</td><td>Enable or disable Multipath TCP.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>establishclientconn</td><td>&lt;String></td><td>Read-write</td><td>Establishing Client Client connection on First data/ Final-ACK / Automatic.&lt;br>Default value: AUTOMATIC&lt;br>Possible values = AUTOMATIC, CONN_ESTABLISHED, ON_FIRST_DATA</td><tr><tr><td>tcpsegoffload</td><td>&lt;String></td><td>Read-write</td><td>Offload TCP segmentation to the NIC. If set to AUTOMATIC, TCP segmentation will be offloaded to the NIC, if the NIC supports it.&lt;br>Default value: AUTOMATIC&lt;br>Possible values = AUTOMATIC, DISABLED</td><tr><tr><td>rstwindowattenuate</td><td>&lt;String></td><td>Read-write</td><td>Enable or disable RST window attenuation to protect against spoofing. When enabled, will reply with corrective ACK when a sequence number is invalid.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>rstmaxack</td><td>&lt;String></td><td>Read-write</td><td>Enable or disable acceptance of RST that is out of window yet echoes highest ACK sequence number. Useful only in proxy mode.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>spoofsyndrop</td><td>&lt;String></td><td>Read-write</td><td>Enable or disable drop of invalid SYN packets to protect against spoofing. When disabled, established connections will be reset when a SYN packet is received.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>ecn</td><td>&lt;String></td><td>Read-write</td><td>Enable or disable TCP Explicit Congestion Notification.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>mptcpdropdataonpreestsf</td><td>&lt;String></td><td>Read-write</td><td>Enable or disable silently dropping the data on Pre-Established subflow. When enabled, DSS data packets are dropped silently instead of dropping the connection when data is received on pre established subflow.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>mptcpfastopen</td><td>&lt;String></td><td>Read-write</td><td>Enable or disable Multipath TCP fastopen. When enabled, DSS data packets are accepted before receiving the third ack of SYN handshake.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>mptcpsessiontimeout</td><td>&lt;Double></td><td>Read-write</td><td>MPTCP session timeout in seconds. If this value is not set, idle MPTCP sessions are flushed after vservers client idle timeout.&lt;br>Default value: 0&lt;br>Minimum value = 0&lt;br>Maximum value = 86400</td><tr><tr><td>timestamp</td><td>&lt;String></td><td>Read-write</td><td>Enable or Disable TCP Timestamp option (RFC 1323).&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>dsack</td><td>&lt;String></td><td>Read-write</td><td>Enable or disable DSACK.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>ackaggregation</td><td>&lt;String></td><td>Read-write</td><td>Enable or disable ACK Aggregation.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>frto</td><td>&lt;String></td><td>Read-write</td><td>Enable or disable FRTO (Forward RTO-Recovery).&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>maxcwnd</td><td>&lt;Double></td><td>Read-write</td><td>TCP Maximum Congestion Window.&lt;br>Default value: 524288&lt;br>Minimum value = 8190&lt;br>Maximum value = 20971520</td><tr><tr><td>fack</td><td>&lt;String></td><td>Read-write</td><td>Enable or disable FACK (Forward ACK).&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>refcnt</td><td>&lt;Double></td><td>Read-only</td><td>Number of entities using this profile.</td><tr><tr><td>builtin</td><td>&lt;String[]></td><td>Read-only</td><td>Flag to determine if tcp profile is built-in or not.&lt;br>Possible values = MODIFIABLE, DELETABLE, IMMUTABLE, PARTITION_ALL</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [DELETE](#delete) | [UPDATE](#update) | [UNSET](#unset) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>},"sessionid":"##sessionid","nstcpprofile":{      "name":<String_value>,      "ws":<String_value>,      "sack":<String_value>,      "wsval":<Double_value>,      "nagle":<String_value>,      "ackonpush":<String_value>,      "mss":<Double_value>,      "maxburst":<Double_value>,      "initialcwnd":<Double_value>,      "delayedack":<Double_value>,      "oooqsize":<Double_value>,      "maxpktpermss":<Double_value>,      "pktperretx":<Double_value>,      "minrto":<Double_value>,      "slowstartincr":<Double_value>,      "buffersize":<Double_value>,      "syncookie":<String_value>,      "kaprobeupdatelastactivity":<String_value>,      "flavor":<String_value>,      "dynamicreceivebuffering":<String_value>,      "ka":<String_value>,      "kaconnidletime":<Double_value>,      "kamaxprobes":<Double_value>,      "kaprobeinterval":<Double_value>,      "sendbuffsize":<Double_value>,      "mptcp":<String_value>,      "establishclientconn":<String_value>,      "tcpsegoffload":<String_value>,      "rstwindowattenuate":<String_value>,      "rstmaxack":<String_value>,      "spoofsyndrop":<String_value>,      "ecn":<String_value>,      "mptcpdropdataonpreestsf":<String_value>,      "mptcpfastopen":<String_value>,      "mptcpsessiontimeout":<Double_value>,      "timestamp":<String_value>,      "dsack":<String_value>,      "ackaggregation":<String_value>,      "frto":<String_value>,      "maxcwnd":<Double_value>,      "fack":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/nstcpprofile/name_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/nstcpprofile/name_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: ```{"params": {      "warning":<String_value>,      "onerror":<String_value>"},sessionid":"##sessionid","nstcpprofile":{      "name":<String_value>,      "ws":<String_value>,      "sack":<String_value>,      "wsval":<Double_value>,      "nagle":<String_value>,      "ackonpush":<String_value>,      "mss":<Double_value>,      "maxburst":<Double_value>,      "initialcwnd":<Double_value>,      "delayedack":<Double_value>,      "oooqsize":<Double_value>,      "maxpktpermss":<Double_value>,      "pktperretx":<Double_value>,      "minrto":<Double_value>,      "slowstartincr":<Double_value>,      "buffersize":<Double_value>,      "syncookie":<String_value>,      "kaprobeupdatelastactivity":<String_value>,      "flavor":<String_value>,      "dynamicreceivebuffering":<String_value>,      "ka":<String_value>,      "kaconnidletime":<Double_value>,      "kamaxprobes":<Double_value>,      "kaprobeinterval":<Double_value>,      "sendbuffsize":<Double_value>,      "mptcp":<String_value>,      "establishclientconn":<String_value>,      "tcpsegoffload":<String_value>,      "rstwindowattenuate":<String_value>,      "rstmaxack":<String_value>,      "spoofsyndrop":<String_value>,      "ecn":<String_value>,      "mptcpdropdataonpreestsf":<String_value>,      "mptcpfastopen":<String_value>,      "mptcpsessiontimeout":<Double_value>,      "timestamp":<String_value>,      "dsack":<String_value>,      "ackaggregation":<String_value>,      "frto":<String_value>,      "maxcwnd":<Double_value>,      "fack":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: ```object={"params":{      "warning":<String_value>,      "onerror":<String_value>,      "action":"unset"},"sessionid":"##sessionid","nstcpprofile":{      "name":<String_value>,      "ws":true,      "sack":true,      "wsval":true,      "nagle":true,      "ackonpush":true,      "mss":true,      "maxburst":true,      "initialcwnd":true,      "delayedack":true,      "oooqsize":true,      "maxpktpermss":true,      "pktperretx":true,      "minrto":true,      "slowstartincr":true,      "buffersize":true,      "syncookie":true,      "kaprobeupdatelastactivity":true,      "flavor":true,      "dynamicreceivebuffering":true,      "ka":true,      "kamaxprobes":true,      "kaconnidletime":true,      "kaprobeinterval":true,      "sendbuffsize":true,      "mptcp":true,      "establishclientconn":true,      "tcpsegoffload":true,      "rstwindowattenuate":true,      "rstmaxack":true,      "spoofsyndrop":true,      "ecn":true,      "mptcpdropdataonpreestsf":true,      "mptcpfastopen":true,      "mptcpsessiontimeout":true,      "timestamp":true,      "dsack":true,      "ackaggregation":true,      "frto":true,      "maxcwnd":true,      "fack":true,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/nstcpprofile
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/nstcpprofile?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of nstcpprofile resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/nstcpprofile?view=summary
Use this query-parameter to get the summary output of nstcpprofile resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/nstcpprofile?pagesize=#no;pageno=#no
Use this query-parameter to get the nstcpprofile resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/nstcpprofile?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "nstcpprofile": [ {      "name":<String_value>,      "ws":<String_value>,      "sack":<String_value>,      "wsval":<Double_value>,      "nagle":<String_value>,      "ackonpush":<String_value>,      "mss":<Double_value>,      "maxburst":<Double_value>,      "initialcwnd":<Double_value>,      "delayedack":<Double_value>,      "oooqsize":<Double_value>,      "maxpktpermss":<Double_value>,      "pktperretx":<Double_value>,      "minrto":<Double_value>,      "slowstartincr":<Double_value>,      "buffersize":<Double_value>,      "flavor":<String_value>,      "refcnt":<Double_value>,      "syncookie":<String_value>,      "kaprobeupdatelastactivity":<String_value>,      "dynamicreceivebuffering":<String_value>,      "ka":<String_value>,      "kaconnidletime":<Double_value>,      "kamaxprobes":<Double_value>,      "kaprobeinterval":<Double_value>,      "sendbuffsize":<Double_value>,      "mptcp":<String_value>,      "establishclientconn":<String_value>,      "tcpsegoffload":<String_value>,      "rstwindowattenuate":<String_value>,      "rstmaxack":<String_value>,      "timestamp":<String_value>,      "spoofsyndrop":<String_value>,      "ecn":<String_value>,      "mptcpdropdataonpreestsf":<String_value>,      "mptcpfastopen":<String_value>,      "mptcpsessiontimeout":<Double_value>,      "dsack":<String_value>,      "ackaggregation":<String_value>,      "frto":<String_value>,      "maxcwnd":<Double_value>,      "fack":<String_value>,      "builtin":<String[]_value>}]}```



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/nstcpprofile/name_value&lt;String&gt;
HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "nstcpprofile": [ {      "name":<String_value>,      "ws":<String_value>,      "sack":<String_value>,      "wsval":<Double_value>,      "nagle":<String_value>,      "ackonpush":<String_value>,      "mss":<Double_value>,      "maxburst":<Double_value>,      "initialcwnd":<Double_value>,      "delayedack":<Double_value>,      "oooqsize":<Double_value>,      "maxpktpermss":<Double_value>,      "pktperretx":<Double_value>,      "minrto":<Double_value>,      "slowstartincr":<Double_value>,      "buffersize":<Double_value>,      "flavor":<String_value>,      "refcnt":<Double_value>,      "syncookie":<String_value>,      "kaprobeupdatelastactivity":<String_value>,      "dynamicreceivebuffering":<String_value>,      "ka":<String_value>,      "kaconnidletime":<Double_value>,      "kamaxprobes":<Double_value>,      "kaprobeinterval":<Double_value>,      "sendbuffsize":<Double_value>,      "mptcp":<String_value>,      "establishclientconn":<String_value>,      "tcpsegoffload":<String_value>,      "rstwindowattenuate":<String_value>,      "rstmaxack":<String_value>,      "timestamp":<String_value>,      "spoofsyndrop":<String_value>,      "ecn":<String_value>,      "mptcpdropdataonpreestsf":<String_value>,      "mptcpfastopen":<String_value>,      "mptcpsessiontimeout":<Double_value>,      "dsack":<String_value>,      "ackaggregation":<String_value>,      "frto":<String_value>,      "maxcwnd":<Double_value>,      "fack":<String_value>,      "builtin":<String[]_value>}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/nstcpprofile?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",nstcpprofile: [ { "__count": "#no"} ] }


