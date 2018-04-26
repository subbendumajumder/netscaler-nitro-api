#videooptimizationdetectionpolicy

Configuration for videooptimization detectionpolicy resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the videooptimization detection policy. Must begin with a letter, number, or the underscore character (_), and must contain only letters, numbers, and the hyphen (-), period (.) pound (#), space ( ), at (@), equals (=), colon (:), and underscore characters.Can be modified, removed or renamed.</td></tr><tr><td>rule</td><td>&lt;String></td><td>Read-write</td><td>Expression that determines which request or response match the video optimization detection policy. Written in default syntax.<br>Note:<br>Maximum length of a string literal in the expression is 255 characters. A longer string can be split into smaller strings of up to 255 characters each, and the smaller strings concatenated with the + operator. For example, you can create a 500-character string as follows: '"&lt;string of 255 characters&gt;" + "&lt;string of 245 characters&gt;"'<br>(Classic expressions are not supported in the cluster build.)<br><br>The following requirements apply only to the NetScaler CLI:<br>* If the expression includes one or more spaces, enclose the entire expression in double quotation marks.<br>* If the expression itself includes double quotation marks, escape the quotations by using the \ character.<br>* Alternatively, you can use single quotation marks to enclose the rule, in which case you do not have to escape the double quotation marks.</td></tr><tr><td>action</td><td>&lt;String></td><td>Read-write</td><td>Name of the videooptimization detection action to perform if the request matches this videooptimization detection policy. Built-in actions should be used. These are:<br>* DETECT_CLEARTEXT_PD - Cleartext PD is detected and increment related counters.<br>* DETECT_CLEARTEXT_ABR - Cleartext ABR is detected and increment related counters.<br>* DETECT_ENCRYPTED_ABR - Encrypted ABR is detected and increment related counters.<br>* TRIGGER_ENC_ABR_DETECTION - This is potentially encrypted ABR. Internal traffic heuristics algorithms will further process traffic to confirm detection.<br>* TRIGGER_CT_ABR_BODY_DETECTION - This is potentially cleartext ABR. Internal traffic heuristics algorithms will further process traffic to confirm detection.<br>* RESET - Reset the client connection by closing it.<br>* DROP - Drop the connection without sending a response.</td></tr><tr><td>undefaction</td><td>&lt;String></td><td>Read-write</td><td>Action to perform if the result of policy evaluation is undefined (UNDEF). An UNDEF event indicates an internal error condition. Only the above built-in actions can be used.</td></tr><tr><td>comment</td><td>&lt;String></td><td>Read-write</td><td>Any type of information about this videooptimization detection policy.</td></tr><tr><td>logaction</td><td>&lt;String></td><td>Read-write</td><td>Name of the messagelog action to use for requests that match this policy.</td></tr><tr><td>newname</td><td>&lt;String></td><td>Read-write</td><td>New name for the videooptimization detection policy. Must begin with a letter, number, or the underscore character (_), and must contain only letters, numbers, and the hyphen (-), period (.) hash (#), space ( ), at (@), equals (=), colon (:), and underscore characters.<br>Minimum length = 1</td></tr><tr><td>hits</td><td>&lt;Double></td><td>Read-only</td><td>Number of hits.</td></tr><tr><td>undefhits</td><td>&lt;Double></td><td>Read-only</td><td>Number of policy UNDEF hits.</td></tr><tr><td>builtin</td><td>&lt;String[]></td><td>Read-only</td><td>Flag to determine if videooptimization detection policy is built-in or not.<br>Possible values = MODIFIABLE, DELETABLE, IMMUTABLE, PARTITION_ALL</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD]()| [DELETE](#d)| [UPDATE](#u)| [UNSET](#)| [RENAME](#r)| [GET (ALL)](#get-)| [GET]()| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/videooptimizationdetectionpolicy
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Request Payload: </b>
<b>Response:</b>
HTTP Status Code on Success: 201 Created


###delete



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/videooptimizationdetectionpolicy/name_value&lt;String&gt;
<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OK


###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/videooptimizationdetectionpolicy
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Request Payload: </b>
<b>Response:</b>
HTTP Status Code on Success: 200 OK


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/videooptimizationdetectionpolicy?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Request Payload: </b>
<b>Response:</b>
HTTP Status Code on Success: 200 OK


###rename



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/videooptimizationdetectionpolicy?<b>action=rename</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Request Payload: </b>
<b>Response:</b>
HTTP Status Code on Success: 200 OK


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/videooptimizationdetectionpolicy
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/videooptimizationdetectionpolicy?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/videooptimizationdetectionpolicy?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of videooptimizationdetectionpolicy resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/videooptimizationdetectionpolicy?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/videooptimizationdetectionpolicy?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the videooptimizationdetectionpolicy resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OK

Content-Type:application/json

<b>Response Payload: </b>



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/videooptimizationdetectionpolicy/name_value&lt;String&gt;
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/videooptimizationdetectionpolicy/name_value&lt;String&gt;?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/videooptimizationdetectionpolicy/name_value&lt;String&gt;?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OK

Content-Type:application/json

<b>Response Payload: </b>



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/videooptimizationdetectionpolicy?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OK

Content-Type:application/json

<b>Response Payload: </b>


