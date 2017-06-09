#crvserver_filterpolicy_binding

Binding object showing the filterpolicy that can be bound to crvserver.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>priority</td><td>&lt;Double></td><td>Read-write</td><td>The priority for the policy.</td><tr><tr><td>gotopriorityexpression</td><td>&lt;String></td><td>Read-write</td><td>Expression or other value specifying the next policy to be evaluated if the current policy evaluates to TRUE. Specify one of the following values: * NEXT ~V Evaluate the policy with the next higher priority number. * END ~V End policy evaluation. * USE_INVOCATION_RESULT ~V Applicable if this policy invokes another policy label. If the final goto in the invoked policy label has a value of END, the eval* USE_INVOCATION_RESULT ~V Applicable if this policy invokes another policy label. If the final goto in the invoked policy label has a value of END, the eval uation stops. If the final goto is anything other than END, the current policy label performs a NEXT. * A default syntax expression that evaluates to a number. If you specify an expression, the number to which it evaluates determines the next policy to evaluate, as follows: * If the expression evaluates to a higher numbered priority, the policy with that priority is evaluated next. * If the expression evaluates to the priority of the current policy, the policy with the next higher numbered priority is evaluated next. * If the expression evaluates to a priority number that is numerically higher than the highest numbered priority, policy evaluation ends. An UNDEF event is triggered if: * The expression is invalid. * The expression evaluates to a priority number that is numerically lower than the current policy~Rs priority. * The expression evaluates to a priority number that is between the current policy~Rs priority number (say, 30) and the highest priority number (say, 100), b ut does not match any configured priority number (for example, the expression evaluates to the number 85). This example assumes that the priority number incr ements by 10 for every successive policy, and therefore a priority number of 85 does not exist in the policy label.</td><tr><tr><td>policyname</td><td>&lt;String></td><td>Read-write</td><td>Policies bound to this vserver.</td><tr><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name of the cache redirection virtual server to which to bind the cache redirection policy.&lt;br>Minimum length = 1</td><tr><tr><td>bindpoint</td><td>&lt;String></td><td>Read-write</td><td>For a rewrite policy, the bind point to which to bind the policy. Note: This parameter applies only to rewrite policies, because content switching policies are evaluated only at request time.&lt;br>Possible values = REQUEST, RESPONSE, ICA_REQUEST</td><tr><tr><td>targetvserver</td><td>&lt;String></td><td>Read-write</td><td>Name of the virtual server to which content is forwarded. Applicable only if the policy is a map policy and the cache redirection virtual server is of type REVERSE.&lt;br>Minimum length = 1</td><tr><tr><td>labeltype</td><td>&lt;String></td><td>Read-write</td><td>Type of label to be invoked.&lt;br>Possible values = reqvserver, resvserver, policylabel</td><tr><tr><td>labelname</td><td>&lt;String></td><td>Read-write</td><td>Name of the label to be invoked.</td><tr><tr><td>invoke</td><td>&lt;Boolean></td><td>Read-write</td><td>Invoke a policy label if this policys rule evaluates to TRUE (valid only for default-syntax policies such as application firewall, transform, integrated cache, rewrite, responder, and content switching).</td><tr><tr><td>inherited</td><td>&lt;String></td><td>Read-only</td><td>On State describes that policy bound is inherited from global binding.&lt;br>Possible values = ON, OFF</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
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
Request Payload: ```{"params":{      "warning":<String_value>,      "onerror":<String_value>},sessionid":"##sessionid","crvserver_filterpolicy_binding":{      "name":<String_value>,      "policyname":<String_value>,                  "targetvserver":<String_value>,                  "priority":<Double_value>,                  "gotopriorityexpression":<String_value>,                  "bindpoint":<String_value>,                  "invoke":<Boolean_value>,                  "labeltype":<String_value>,                  "labelname":<String_value>,}}```
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###delete:



URL: http://&lt;NS_IP&gt;/nitro/v1/config/crvserver_filterpolicy_binding/name_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/crvserver_filterpolicy_binding/name_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 
{ "errorcode": 0, "message": "Done", "severity": <String_value> }


###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/crvserver_filterpolicy_binding/name_value&lt;String&gt;
Query-parameters:
filter
http://&lt;NS_IP&gt;/nitro/v1/config/crvserver_filterpolicy_binding/name_value&lt;String&gt;?filter=property-name1:property-value1,property-name2:property-value2
Use this query-parameter to get the filtered set of crvserver_filterpolicy_binding resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/crvserver_filterpolicy_binding/name_value&lt;String&gt;?pagesize=#no;pageno=#no
Use this query-parameter to get the crvserver_filterpolicy_binding resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/crvserver_filterpolicy_binding?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: ```{ "errorcode": 0, "message": "Done", "severity": <String_value>, "crvserver_filterpolicy_binding": [ {      "priority":<Double_value>,      "gotopriorityexpression":<String_value>,      "policyname":<String_value>,      "name":<String_value>,      "bindpoint":<String_value>,      "targetvserver":<String_value>,      "labeltype":<String_value>,      "labelname":<String_value>,      "invoke":<Boolean_value>,      "inherited":<String_value>,}]}```



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/crvserver_filterpolicy_binding/name_value&lt;String&gt;?count=yes
HTTP Method: GET
Response Payload: 
{ "errorcode": 0, "message": "Done",crvserver_filterpolicy_binding: [ { "__count": "#no"} ] }


