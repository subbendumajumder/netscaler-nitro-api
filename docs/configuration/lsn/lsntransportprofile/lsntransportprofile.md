#lsntransportprofile

Configuration for LSN Transport Profile resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>transportprofilename</td><td>&lt;String></td><td>Read-write</td><td>Name for the LSN transport profile. Must begin with an ASCII alphanumeric or underscore (_) character, and must contain only ASCII alphanumeric, underscore, hash (#), period (.), space, colon (:), at (@), equals (=), and hyphen (-) characters. Cannot be changed after the LSN transport profile is created. The following requirement applies only to the NetScaler CLI: If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "lsn transport profile1" or lsn transport profile1).&lt;br>Minimum length = 1&lt;br>Maximum length = 127</td><tr><tr><td>transportprotocol</td><td>&lt;String></td><td>Read-write</td><td>Protocol for which to set the LSN transport profile parameters.&lt;br>Possible values = TCP, UDP, ICMP</td><tr><tr><td>sessiontimeout</td><td>&lt;Double></td><td>Read-write</td><td>Timeout, in seconds, for an idle LSN session. If an LSN session is idle for a time that exceeds this value, the NetScaler ADC removes the session.&lt;br>&lt;br>This timeout does not apply for a TCP LSN session when a FIN or RST message is received from either of the endpoints. .&lt;br>Default value: 120&lt;br>Minimum value = 60</td><tr><tr><td>finrsttimeout</td><td>&lt;Double></td><td>Read-write</td><td>Timeout, in seconds, for a TCP LSN session after a FIN or RST message is received from one of the endpoints.&lt;br>&lt;br>If a TCP LSN session is idle (after the NetScaler ADC receives a FIN or RST message) for a time that exceeds this value, the NetScaler ADC removes the session.&lt;br>&lt;br>Since the LSN feature of the NetScaler ADC does not maintain state information of any TCP LSN sessions, this timeout accommodates the transmission of the FIN or RST, and ACK messages from the other endpoint so that both endpoints can properly close the connection.&lt;br>Default value: 30</td><tr><tr><td>stuntimeout</td><td>&lt;Double></td><td>Read-write</td><td>STUN protocol timeout.&lt;br>Default value: 600&lt;br>Minimum value = 120&lt;br>Maximum value = 1200</td><tr><tr><td>synidletimeout</td><td>&lt;Double></td><td>Read-write</td><td>SYN Idle timeout.&lt;br>Default value: 60&lt;br>Minimum value = 30&lt;br>Maximum value = 120</td><tr><tr><td>portquota</td><td>&lt;Double></td><td>Read-write</td><td>Maximum number of LSN NAT ports to be used at a time by each subscriber for the specified protocol. For example, each subscriber can be limited to a maximum of 500 TCP NAT ports. When the LSN NAT mappings for a subscriber reach the limit, the NetScaler ADC does not allocate additional NAT ports for that subscriber.&lt;br>Default value: 0&lt;br>Minimum value = 0&lt;br>Maximum value = 65535</td><tr><tr><td>sessionquota</td><td>&lt;Double></td><td>Read-write</td><td>Maximum number of concurrent LSN sessions allowed for each subscriber for the specified protocol. &lt;br>When the number of LSN sessions reaches the limit for a subscriber, the NetScaler ADC does not allow the subscriber to open additional sessions.&lt;br>Default value: 0&lt;br>Minimum value = 0&lt;br>Maximum value = 65535</td><tr><tr><td>groupsessionlimit</td><td>&lt;Double></td><td>Read-write</td><td>Maximum number of concurrent LSN sessions(for the specified protocol) allowed for all subscriber of a group to which this profile has bound. This limit will get split across the netscalers packet engines and rounded down. When the number of LSN sessions reaches the limit for a group in packet engine, the NetScaler ADC does not allow the subscriber of that group to open additional sessions through that packet engine.&lt;br>Default value: 0</td><tr><tr><td>portpreserveparity</td><td>&lt;String></td><td>Read-write</td><td>Enable port parity between a subscriber port and its mapped LSN NAT port. For example, if a subscriber initiates a connection from an odd numbered port, the NetScaler ADC allocates an odd numbered LSN NAT port for this connection. &lt;br>You must set this parameter for proper functioning of protocols that require the source port to be even or odd numbered, for example, in peer-to-peer applications that use RTP or RTCP protocol.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>portpreserverange</td><td>&lt;String></td><td>Read-write</td><td>If a subscriber initiates a connection from a well-known port (0-1023), allocate a NAT port from the well-known port range (0-1023) for this connection. For example, if a subscriber initiates a connection from port 80, the NetScaler ADC can allocate port 100 as the NAT port for this connection.&lt;br>&lt;br>This parameter applies to dynamic NAT without port block allocation. It also applies to Deterministic NAT if the range of ports allocated includes well-known ports.&lt;br>&lt;br>When all the well-known ports of all the available NAT IP addresses are used in different subscribers\\? connections (LSN sessions), and a subscriber initiates a connection from a well-known port, the NetScaler ADC drops this connection.&lt;br>Default value: DISABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>syncheck</td><td>&lt;String></td><td>Read-write</td><td>Silently drop any non-SYN packets for connections for which there is no LSN-NAT session present on the NetScaler ADC. &lt;br>&lt;br>If you disable this parameter, the NetScaler ADC accepts any non-SYN packets and creates a new LSN session entry for this connection. &lt;br>&lt;br>Following are some reasons for the NetScaler ADC to receive such packets:&lt;br>&lt;br>* LSN session for a connection existed but the NetScaler ADC removed this session because the LSN session was idle for a time that exceeded the configured session timeout.&lt;br>* Such packets can be a part of a DoS attack.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [DELETE](#delete) | [UPDATE](#update) | [UNSET](#unset) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsntransportprofile
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"lsntransportprofile":{      "transportprofilename":<String_value>,      "transportprotocol":<String_value>,      "sessiontimeout":<Double_value>,      "finrsttimeout":<Double_value>,      "stuntimeout":<Double_value>,      "synidletimeout":<Double_value>,      "portquota":<Double_value>,      "sessionquota":<Double_value>,      "groupsessionlimit":<Double_value>,      "portpreserveparity":<String_value>,      "portpreserverange":<String_value>,      "syncheck":<String_value>}}```
Response:
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsntransportprofile/transportprofilename_value&lt;String&gt;
HTTP Method: DELETE
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsntransportprofile
HTTP Method: PUT
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"lsntransportprofile":{      "transportprofilename":<String_value>,      "sessiontimeout":<Double_value>,      "finrsttimeout":<Double_value>,      "stuntimeout":<Double_value>,      "synidletimeout":<Double_value>,      "portquota":<Double_value>,      "sessionquota":<Double_value>,      "groupsessionlimit":<Double_value>,      "portpreserveparity":<String_value>,      "portpreserverange":<String_value>,      "syncheck":<String_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsntransportprofile?action=unset
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"lsntransportprofile":{      "transportprofilename":<String_value>,      "sessiontimeout":true,      "finrsttimeout":true,      "stuntimeout":true,      "synidletimeout":true,      "portquota":true,      "sessionquota":true,      "groupsessionlimit":true,      "portpreserveparity":true,      "portpreserverange":true,      "syncheck":true}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsntransportprofile
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsntransportprofile?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


filter
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsntransportprofile?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of lsntransportprofile resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsntransportprofile?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).


pagination
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsntransportprofile?pagesize=#no;pageno=#no
Use this query-parameter to get the lsntransportprofile resources in chunks.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "lsntransportprofile": [ {      "transportprofilename":<String_value>,      "transportprotocol":<String_value>,      "sessiontimeout":<Double_value>,      "finrsttimeout":<Double_value>,      "stuntimeout":<Double_value>,      "synidletimeout":<Double_value>,      "portquota":<Double_value>,      "sessionquota":<Double_value>,      "groupsessionlimit":<Double_value>,      "portpreserveparity":<String_value>,      "portpreserverange":<String_value>,      "syncheck":<String_value>}]}```



###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsntransportprofile/transportprofilename_value&lt;String&gt;
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsntransportprofile/transportprofilename_value&lt;String&gt;?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsntransportprofile/transportprofilename_value&lt;String&gt;?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "lsntransportprofile": [ {      "transportprofilename":<String_value>,      "transportprotocol":<String_value>,      "sessiontimeout":<Double_value>,      "finrsttimeout":<Double_value>,      "stuntimeout":<Double_value>,      "synidletimeout":<Double_value>,      "portquota":<Double_value>,      "sessionquota":<Double_value>,      "groupsessionlimit":<Double_value>,      "portpreserveparity":<String_value>,      "portpreserverange":<String_value>,      "syncheck":<String_value>}]}```



###count



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsntransportprofile?count=yes
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: 
{ "lsntransportprofile": [ { "__count": "#no"} ] }


