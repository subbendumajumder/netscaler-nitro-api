#authorizationpolicylabel

Configuration for authorization policy label resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>labelname</td><td>&lt;String></td><td>Read-write</td><td>Name for the new authorization policy label. <br>Must begin with a letter, number, or the underscore character (_), and must contain only letters, numbers, and the hyphen (-), period (.) pound (#), space ( ), at (@), equals (=), colon (:), and underscore characters. Cannot be changed after the authorization policy is created.<br><br>The following requirement applies only to the NetScaler CLI:<br>If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my authorization policy label" or 'authorization policy label').</td></tr><tr><td>newname</td><td>&lt;String></td><td>Read-write</td><td>The new name of the auth policy label.<br>Minimum length = 1</td></tr><tr><td>numpol</td><td>&lt;Double></td><td>Read-only</td><td>Number of polices bound to label.</td></tr><tr><td>hits</td><td>&lt;Double></td><td>Read-only</td><td>Number of times policy label was invoked.</td></tr><tr><td>policyname</td><td>&lt;String></td><td>Read-only</td><td>Name of the authorization policy to bind to the policy label.</td></tr><tr><td>priority</td><td>&lt;Double></td><td>Read-only</td><td>Specifies the priority of the policy.</td></tr><tr><td>gotopriorityexpression</td><td>&lt;String></td><td>Read-only</td><td>Expression specifying the priority of the next policy which will get evaluated if the current policy rule evaluates to TRUE.</td></tr><tr><td>labeltype</td><td>&lt;String></td><td>Read-only</td><td>Type of invocation. Available settings function as follows:<br>* reqvserver - Send the request to the specified request virtual server.<br>* resvserver - Send the response to the specified response virtual server.<br>* policylabel - Invoke the specified policy label.<br>Possible values = reqvserver, resvserver, policylabel</td></tr><tr><td>invoke_labelname</td><td>&lt;String></td><td>Read-only</td><td>Name of the policy label to invoke if the current policy evaluates to TRUE, the invoke parameter is set, and Label Type is set to Policy Label.</td></tr><tr><td>flowtype</td><td>&lt;Double></td><td>Read-only</td><td>Flowtype of the bound authorization policy.</td></tr><tr><td>description</td><td>&lt;String></td><td>Read-only</td><td>Description of the policylabel.</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD]()| [DELETE](#d)| [RENAME](#r)| [GET (ALL)](#get-)| [GET]()| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authorizationpolicylabel
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"authorizationpolicylabel":{<b>"labelname":<String_value></b>}}```
<b>Response:</b>
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authorizationpolicylabel/labelname_value&lt;String&gt;
<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###rename



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authorizationpolicylabel?<b>action=rename</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"authorizationpolicylabel":{<b>"labelname":<String_value>,</b><b>"newname":<String_value></b>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authorizationpolicylabel
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authorizationpolicylabel?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authorizationpolicylabel?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of authorizationpolicylabel resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authorizationpolicylabel?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authorizationpolicylabel?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the authorizationpolicylabel resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "authorizationpolicylabel": [ {"labelname":<String_value>,"numpol":<Double_value>,"hits":<Double_value>,"policyname":<String_value>,"priority":<Double_value>,"gotopriorityexpression":<String_value>,"labeltype":<String_value>,"invoke_labelname":<String_value>,"flowtype":<Double_value>,"description":<String_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authorizationpolicylabel/labelname_value&lt;String&gt;
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authorizationpolicylabel/labelname_value&lt;String&gt;?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authorizationpolicylabel/labelname_value&lt;String&gt;?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "authorizationpolicylabel": [ {"labelname":<String_value>,"numpol":<Double_value>,"hits":<Double_value>,"policyname":<String_value>,"priority":<Double_value>,"gotopriorityexpression":<String_value>,"labeltype":<String_value>,"invoke_labelname":<String_value>,"flowtype":<Double_value>,"description":<String_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authorizationpolicylabel?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "authorizationpolicylabel": [ { "__count": "#no"} ] }```



