#smppparam

Configuration for SMPP configuration parameters resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>clientmode</td><td>&lt;String></td><td>Read-write</td><td>Mode in which the client binds to the ADC. Applicable settings function as follows: * TRANSCEIVER - Client can send and receive messages to and from the message center. * TRANSMITTERONLY - Client can only send messages. * RECEIVERONLY - Client can only receive messages.&lt;br>Default value: TRANSCEIVER&lt;br>Possible values = TRANSCEIVER, TRANSMITTERONLY, RECEIVERONLY</td><tr><tr><td>msgqueue</td><td>&lt;String></td><td>Read-write</td><td>Queue SMPP messages if a client that is capable of receiving the destination address messages is not available.&lt;br>Default value: OFF&lt;br>Possible values = ON, OFF</td><tr><tr><td>msgqueuesize</td><td>&lt;Double></td><td>Read-write</td><td>Maximum number of SMPP messages that can be queued. After the limit is reached, the NetScaler ADC sends a deliver_sm_resp PDU, with an appropriate error message, to the message center.&lt;br>Default value: 10000</td><tr><tr><td>addrton</td><td>&lt;Double></td><td>Read-write</td><td>Type of Number, such as an international number or a national number, used in the ESME address sent in the bind request.&lt;br>Default value: 0&lt;br>Minimum value = 0&lt;br>Maximum value = 256</td><tr><tr><td>addrnpi</td><td>&lt;Double></td><td>Read-write</td><td>Numbering Plan Indicator, such as landline, data, or WAP client, used in the ESME address sent in the bind request.&lt;br>Default value: 0&lt;br>Minimum value = 0&lt;br>Maximum value = 256</td><tr><tr><td>addrrange</td><td>&lt;String></td><td>Read-write</td><td>Set of SME addresses, sent in the bind request, serviced by the ESME.&lt;br>Default value: "\\\\d*"</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[UPDATE](#update) | [UNSET](#unset) | [GET (ALL)](#get-(all))


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: 
Response Payload: 



###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: 
Response Payload: 



###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/smppparam
HTTP Method: GET
Response Payload: 


