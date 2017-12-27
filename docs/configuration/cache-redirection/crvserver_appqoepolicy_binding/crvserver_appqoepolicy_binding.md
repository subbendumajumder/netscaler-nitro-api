#crvserver_appqoepolicy_binding

Binding object showing the appqoepolicy that can be bound to crvserver.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>priority</td><td>&lt;Double></td><td>Read-write</td><td>The priority for the policy.</td><tr><tr><td>bindpoint</td><td>&lt;String></td><td>Read-write</td><td>The bindpoint to which the policy is bound.&lt;br>Possible values = REQUEST, RESPONSE, ICA_REQUEST</td><tr><tr><td>policyname</td><td>&lt;String></td><td>Read-write</td><td>Policies bound to this vserver.</td><tr><tr><td>labelname</td><td>&lt;String></td><td>Read-write</td><td>Name of the label invoked.</td><tr><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name of the cache redirection virtual server to which to bind the cache redirection policy.&lt;br>Minimum length = 1</td><tr><tr><td>targetvserver</td><td>&lt;String></td><td>Read-write</td><td>Name of the virtual server to which content is forwarded. Applicable only if the policy is a map policy and the cache redirection virtual server is of type REVERSE.&lt;br>Minimum length = 1</td><tr><tr><td>gotopriorityexpression</td><td>&lt;String></td><td>Read-write</td><td>Expression specifying the priority of the next policy which will get evaluated if the current policy rule evaluates to TRUE.</td><tr><tr><td>invoke</td><td>&lt;Boolean></td><td>Read-write</td><td>Invoke flag.</td><tr><tr><td>labeltype</td><td>&lt;String></td><td>Read-write</td><td>The invocation type.&lt;br>Possible values = reqvserver, resvserver, policylabel</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-write</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD:](#add:) | [DELETE:](#delete:) | [GET](#get) | [GET (ALL)](#get-(all)) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add:



URL: http://&lt;netscaler-ip-address/nitro/v1/config/crvserver_appqoepolicy_binding
HTTP Method: PUT
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Request Payload: 
Response:
HTTP Status Code on Success: 201 Created


###delete:



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/crvserver_appqoepolicy_binding/name_value&lt;String&gt;
HTTP Method: DELETE
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Response:
HTTP Status Code on Success: 200 OK


###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/crvserver_appqoepolicy_binding/name_value&lt;String&gt;
Query-parameters:
filter
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/crvserver_appqoepolicy_binding/name_value&lt;String&gt;?filter=property-name1:property-value1,property-name2:property-value2
Use this query-parameter to get the filtered set of crvserver_appqoepolicy_binding resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


pagination
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/crvserver_appqoepolicy_binding/name_value&lt;String&gt;?pagesize=#no;pageno=#no
Use this query-parameter to get the crvserver_appqoepolicy_binding resources in chunks.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Response:
HTTP Status Code on Success: 200 OK

Content-Type:application/json

Response Payload: 



###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/crvserver_appqoepolicy_binding
Query-parameters:
bulkbindings
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/crvserver_appqoepolicy_binding?bulkbindings=yes
NITRO allows you to fetch bindings in bulk.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Response:
HTTP Status Code on Success: 200 OK

Content-Type:application/json

Response Payload: 



###count



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/crvserver_appqoepolicy_binding/name_value&lt;String&gt;?count=yes
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Response:
HTTP Status Code on Success: 200 OK

Content-Type:application/json

Response Payload: 


