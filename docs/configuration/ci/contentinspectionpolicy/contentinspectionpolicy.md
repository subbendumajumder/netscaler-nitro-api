#contentinspectionpolicy

Configuration for ContentInspection policy resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the contentInspection policy.<br>Must begin with a letter, number, or the underscore character (_), and must contain only letters, numbers, and the hyphen (-), period (.) pound (#), space ( ), at (@), equals (=), colon (:), and underscore characters. Can be changed after the contentInspection policy is added.<br><br>The following requirement applies only to the NetScaler CLI:<br>If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my contentInspection policy" or 'my contentInspection policy').<br></td></tr><tr><td>rule</td><td>&lt;String></td><td>Read-write</td><td>Advanced expression that the policy uses to determine whether to execute the specified action.</td></tr><tr><td>action</td><td>&lt;String></td><td>Read-write</td><td>Name of the contentInspection action to perform if the request matches this contentInspection policy. There are also some built-in actions which can be used. These are:<br>* RESET - Reset the client connection by closing it. The client program, such as a browser, will handle this and may inform the user. The client may then resend the request if desired.<br>* DROP - Drop the request without sending a response to the user.</td></tr><tr><td>undefaction</td><td>&lt;String></td><td>Read-write</td><td>Action to perform if the result of policy evaluation is undefined (UNDEF). An UNDEF event indicates an internal error condition. Only the above built-in actions can be used.</td></tr><tr><td>comment</td><td>&lt;String></td><td>Read-write</td><td>Any type of information about this contentInspection policy.</td></tr><tr><td>logaction</td><td>&lt;String></td><td>Read-write</td><td>Name of the messagelog action to use for requests that match this policy.</td></tr><tr><td>newname</td><td>&lt;String></td><td>Read-write</td><td>New name for the contentInspection policy. Must begin with a letter, number, or the underscore character (_), and must contain only letters, numbers, and the hyphen (-), period (.) hash (#), space ( ), at (@), equals (=), colon (:), and underscore characters. <br><br>The following requirement applies only to the NetScaler CLI:<br>If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my contentInspection policy" or 'my contentInspection policy').<br>Minimum length = 1</td></tr><tr><td>hits</td><td>&lt;Double></td><td>Read-only</td><td>Number of hits.</td></tr><tr><td>undefhits</td><td>&lt;Double></td><td>Read-only</td><td>Number of policy UNDEF hits.</td></tr><tr><td>builtin</td><td>&lt;String[]></td><td>Read-only</td><td>Flag to determine if contentInspection policy is built-in or not.<br>Possible values = MODIFIABLE, DELETABLE, IMMUTABLE, PARTITION_ALL</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD]()| [DELETE](#d)| [UPDATE](#u)| [UNSET](#)| [RENAME](#r)| [GET (ALL)](#get-)| [GET]()| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/contentinspectionpolicy
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Request Payload: </b>
<b>Response:</b>
HTTP Status Code on Success: 201 Created


###delete



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/contentinspectionpolicy/name_value&lt;String&gt;
<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OK


###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/contentinspectionpolicy
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Request Payload: </b>
<b>Response:</b>
HTTP Status Code on Success: 200 OK


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/contentinspectionpolicy?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Request Payload: </b>
<b>Response:</b>
HTTP Status Code on Success: 200 OK


###rename



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/contentinspectionpolicy?<b>action=rename</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Request Payload: </b>
<b>Response:</b>
HTTP Status Code on Success: 200 OK


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/contentinspectionpolicy
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/contentinspectionpolicy?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/contentinspectionpolicy?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of contentinspectionpolicy resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/contentinspectionpolicy?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/contentinspectionpolicy?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the contentinspectionpolicy resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OK

Content-Type:application/json

<b>Response Payload: </b>



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/contentinspectionpolicy/name_value&lt;String&gt;
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/contentinspectionpolicy/name_value&lt;String&gt;?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/contentinspectionpolicy/name_value&lt;String&gt;?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OK

Content-Type:application/json

<b>Response Payload: </b>



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/contentinspectionpolicy?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OK

Content-Type:application/json

<b>Response Payload: </b>


