#contentinspectionglobal_contentinspectionpolicy_binding

Binding object showing the contentinspectionpolicy that can be bound to contentinspectionglobal.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>priority</td><td>&lt;Double></td><td>Read-write</td><td>Specifies the priority of the policy.</td></tr><tr><td>globalbindtype</td><td>&lt;String></td><td>Read-write</td><td>.<br>Default value: SYSTEM_GLOBAL<br>Possible values = SYSTEM_GLOBAL, VPN_GLOBAL, RNAT_GLOBAL</td></tr><tr><td>gotopriorityexpression</td><td>&lt;String></td><td>Read-write</td><td>Expression specifying the priority of the next policy which will get evaluated if the current policy rule evaluates to TRUE.</td></tr><tr><td>policyname</td><td>&lt;String></td><td>Read-write</td><td>Name of the contentInspection policy.</td></tr><tr><td>type</td><td>&lt;String></td><td>Read-write</td><td>The bindpoint to which to policy is bound.<br>Possible values = REQ_OVERRIDE, REQ_DEFAULT, RES_OVERRIDE, RES_DEFAULT</td></tr><tr><td>labeltype</td><td>&lt;String></td><td>Read-write</td><td>Type of invocation. Available settings function as follows: * reqvserver - Forward the request to the specified request virtual server. * resvserver - Forward the response to the specified response virtual server. * policylabel - Invoke the specified policy label.<br>Possible values = reqvserver, resvserver, policylabel</td></tr><tr><td>labelname</td><td>&lt;String></td><td>Read-write</td><td>* If labelType is policylabel, name of the policy label to invoke. * If labelType is reqvserver or resvserver, name of the virtual server to which to forward the request of response.</td></tr><tr><td>invoke</td><td>&lt;Boolean></td><td>Read-write</td><td>Terminate evaluation of policies bound to the current policy label, and then forward the request to the specified virtual server or evaluate the specified policy label.</td></tr><tr><td>numpol</td><td>&lt;Double></td><td>Read-only</td><td>The number of policies bound to the bindpoint.</td></tr><tr><td>flowtype</td><td>&lt;Double></td><td>Read-only</td><td>flowtype of the bound contentInspection policy.</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD:]()| [DELETE:](#de)| [GET]()| [GET (ALL)](#get-)| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add:



<b>URL:</b>http://&lt;netscaler-ip-address/nitro/v1/config/contentinspectionglobal_contentinspectionpolicy_binding
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Request Payload: </b>
<b>Response:</b>
HTTP Status Code on Success: 201 Created


###delete:



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/contentinspectionglobal_contentinspectionpolicy_binding
<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OK


###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/contentinspectionglobal_contentinspectionpolicy_binding
<b>Query-parameters:</b>
<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/contentinspectionglobal_contentinspectionpolicy_binding?<b>filter=property-name1:property-value1,property-name2:property-value2</b>
Use this query-parameter to get the filtered set of contentinspectionglobal_contentinspectionpolicy_binding resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/contentinspectionglobal_contentinspectionpolicy_binding?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the contentinspectionglobal_contentinspectionpolicy_binding resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OK

Content-Type:application/json

<b>Response Payload: </b>



###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/contentinspectionglobal_contentinspectionpolicy_binding
<b>Query-parameters:</b>
<b>bulkbindings</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/contentinspectionglobal_contentinspectionpolicy_binding?<b>bulkbindings=yes</b>
NITRO allows you to fetch bindings in bulk.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OK

Content-Type:application/json

<b>Response Payload: </b>



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/contentinspectionglobal_contentinspectionpolicy_binding?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OK

Content-Type:application/json

<b>Response Payload: </b>


