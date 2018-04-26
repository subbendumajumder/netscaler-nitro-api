#appfwprofile_xmldosurl_binding

Binding object showing the xmldosurl that can be bound to appfwprofile.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>xmlmaxelementdepthcheck</td><td>&lt;String></td><td>Read-write</td><td>State if XML Max element depth check is ON or OFF.<br>Possible values = ON, OFF</td></tr><tr><td>xmlmaxfilesize</td><td>&lt;Double></td><td>Read-write</td><td>Specify the maximum size of XML messages. Protects against overflow attacks.</td></tr><tr><td>xmlmaxnamespaceurilength</td><td>&lt;Double></td><td>Read-write</td><td>Specify the longest URI of any XML namespace. Protects against overflow attacks.</td></tr><tr><td>xmldosurl</td><td>&lt;String></td><td>Read-write</td><td>XML DoS URL regular expression length.</td></tr><tr><td>state</td><td>&lt;String></td><td>Read-write</td><td>Enabled.<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>xmlsoaparraycheck</td><td>&lt;String></td><td>Read-write</td><td>State if XML SOAP Array check is ON or OFF.<br>Possible values = ON, OFF</td></tr><tr><td>xmlmaxelementnamelengthcheck</td><td>&lt;String></td><td>Read-write</td><td>State if XML Max element name length check is ON or OFF.<br>Possible values = ON, OFF</td></tr><tr><td>xmlmaxelementscheck</td><td>&lt;String></td><td>Read-write</td><td>State if XML Max elements check is ON or OFF.<br>Possible values = ON, OFF</td></tr><tr><td>xmlmaxentityexpansions</td><td>&lt;Double></td><td>Read-write</td><td>Specify maximum allowed number of entity expansions. Protects aganist Entity Expansion Attack.</td></tr><tr><td>xmlmaxattributes</td><td>&lt;Double></td><td>Read-write</td><td>Specify maximum number of attributes per XML element. Protects against overflow attacks.</td></tr><tr><td>xmlmaxfilesizecheck</td><td>&lt;String></td><td>Read-write</td><td>State if XML Max file size check is ON or OFF.<br>Possible values = ON, OFF</td></tr><tr><td>xmlmaxchardatalength</td><td>&lt;Double></td><td>Read-write</td><td>Specify the maximum size of CDATA. Protects against overflow attacks and large quantities of unparsed data within XML messages.</td></tr><tr><td>xmlmaxnamespacescheck</td><td>&lt;String></td><td>Read-write</td><td>State if XML Max namespaces check is ON or OFF.<br>Possible values = ON, OFF</td></tr><tr><td>xmlmaxnamespaces</td><td>&lt;Double></td><td>Read-write</td><td>Specify maximum number of active namespaces. Protects against overflow attacks.</td></tr><tr><td>xmlmaxattributenamelengthcheck</td><td>&lt;String></td><td>Read-write</td><td>State if XML Max attribute name length check is ON or OFF.<br>Possible values = ON, OFF</td></tr><tr><td>xmlblockdtd</td><td>&lt;String></td><td>Read-write</td><td>State if XML DTD is ON or OFF. Protects against recursive Document Type Declaration (DTD) entity expansion attacks. Also, SOAP messages cannot have DTDs in messages. .<br>Possible values = ON, OFF</td></tr><tr><td>xmlmaxattributevaluelength</td><td>&lt;Double></td><td>Read-write</td><td>Specify the longest value of any XML attribute. Protects against overflow attacks.</td></tr><tr><td>xmlmaxelementdepth</td><td>&lt;Double></td><td>Read-write</td><td>Maximum nesting (depth) of XML elements. This check protects against documents that have excessive hierarchy depths.</td></tr><tr><td>xmlmaxelementnamelength</td><td>&lt;Double></td><td>Read-write</td><td>Specify the longest name of any element (including the expanded namespace) to protect against overflow attacks.</td></tr><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name of the profile to which to bind an exemption or rule.<br>Minimum length = 1</td></tr><tr><td>xmlblockpi</td><td>&lt;String></td><td>Read-write</td><td>State if XML Block PI is ON or OFF. Protects resources from denial of service attacks as SOAP messages cannot have processing instructions (PI) in messages.<br>Possible values = ON, OFF</td></tr><tr><td>xmlmaxelementchildrencheck</td><td>&lt;String></td><td>Read-write</td><td>State if XML Max element children check is ON or OFF.<br>Possible values = ON, OFF</td></tr><tr><td>xmlmaxelements</td><td>&lt;Double></td><td>Read-write</td><td>Specify the maximum number of XML elements allowed. Protects against overflow attacks.</td></tr><tr><td>xmlmaxentityexpansionscheck</td><td>&lt;String></td><td>Read-write</td><td>State if XML Max Entity Expansions Check is ON or OFF.<br>Possible values = ON, OFF</td></tr><tr><td>xmlmaxnamespaceurilengthcheck</td><td>&lt;String></td><td>Read-write</td><td>State if XML Max namespace URI length check is ON or OFF.<br>Possible values = ON, OFF</td></tr><tr><td>xmlmaxentityexpansiondepthcheck</td><td>&lt;String></td><td>Read-write</td><td>State if XML Max Entity Expansions Depth Check is ON or OFF.<br>Possible values = ON, OFF</td></tr><tr><td>xmlmaxattributevaluelengthcheck</td><td>&lt;String></td><td>Read-write</td><td>State if XML Max atribute value length is ON or OFF.<br>Possible values = ON, OFF</td></tr><tr><td>xmlmaxsoaparraysize</td><td>&lt;Double></td><td>Read-write</td><td>XML Max Total SOAP Array Size. Protects against SOAP Array Abuse attack.</td></tr><tr><td>xmlmaxentityexpansiondepth</td><td>&lt;Double></td><td>Read-write</td><td>Specify maximum entity expansion depth. Protects aganist Entity Expansion Attack.</td></tr><tr><td>xmlmaxnodescheck</td><td>&lt;String></td><td>Read-write</td><td>State if XML Max nodes check is ON or OFF.<br>Possible values = ON, OFF</td></tr><tr><td>xmlmaxattributenamelength</td><td>&lt;Double></td><td>Read-write</td><td>Specify the longest name of any XML attribute. Protects against overflow attacks.</td></tr><tr><td>xmlmaxchardatalengthcheck</td><td>&lt;String></td><td>Read-write</td><td>State if XML Max CDATA length check is ON or OFF.<br>Possible values = ON, OFF</td></tr><tr><td>xmlminfilesizecheck</td><td>&lt;String></td><td>Read-write</td><td>State if XML Min file size check is ON or OFF.<br>Possible values = ON, OFF</td></tr><tr><td>xmlmaxelementchildren</td><td>&lt;Double></td><td>Read-write</td><td>Specify the maximum number of children allowed per XML element. Protects against overflow attacks.</td></tr><tr><td>xmlminfilesize</td><td>&lt;Double></td><td>Read-write</td><td>Enforces minimum message size.</td></tr><tr><td>xmlmaxnodes</td><td>&lt;Double></td><td>Read-write</td><td>Specify the maximum number of XML nodes. Protects against overflow attacks.</td></tr><tr><td>comment</td><td>&lt;String></td><td>Read-write</td><td>Any comments about the purpose of profile, or other useful information about the profile.</td></tr><tr><td>xmlmaxattributescheck</td><td>&lt;String></td><td>Read-write</td><td>State if XML Max attributes check is ON or OFF.<br>Possible values = ON, OFF</td></tr><tr><td>xmlmaxsoaparrayrank</td><td>&lt;Double></td><td>Read-write</td><td>XML Max Individual SOAP Array Rank. This is the dimension of the SOAP array.</td></tr><tr><td>xmlblockexternalentities</td><td>&lt;String></td><td>Read-write</td><td>State if XML Block External Entities Check is ON or OFF. Protects against XML External Entity (XXE) attacks that force applications to parse untrusted external entities (sources) in XML documents.<br>Possible values = ON, OFF</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-write</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD:]()| [DELETE:](#de)| [GET]()| [GET (ALL)](#get-)| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add:



<b>URL:</b>http://&lt;netscaler-ip-address/nitro/v1/config/appfwprofile_xmldosurl_binding
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"appfwprofile_xmldosurl_binding":{<b>"name":<String_value>,</b>"comment":<String_value>,"state":<String_value>,"xmldosurl":<String_value>,"xmlmaxelementdepthcheck":<String_value>,"xmlmaxelementdepth":<Double_value>,"xmlmaxelementnamelengthcheck":<String_value>,"xmlmaxelementnamelength":<Double_value>,"xmlmaxelementscheck":<String_value>,"xmlmaxelements":<Double_value>,"xmlmaxelementchildrencheck":<String_value>,"xmlmaxelementchildren":<Double_value>,"xmlmaxattributescheck":<String_value>,"xmlmaxattributes":<Double_value>,"xmlmaxattributenamelengthcheck":<String_value>,"xmlmaxattributenamelength":<Double_value>,"xmlmaxattributevaluelengthcheck":<String_value>,"xmlmaxattributevaluelength":<Double_value>,"xmlmaxchardatalengthcheck":<String_value>,"xmlmaxchardatalength":<Double_value>,"xmlmaxfilesizecheck":<String_value>,"xmlmaxfilesize":<Double_value>,"xmlminfilesizecheck":<String_value>,"xmlminfilesize":<Double_value>,"xmlblockpi":<String_value>,"xmlblockdtd":<String_value>,"xmlblockexternalentities":<String_value>,"xmlmaxentityexpansionscheck":<String_value>,"xmlmaxentityexpansions":<Double_value>,"xmlmaxentityexpansiondepthcheck":<String_value>,"xmlmaxentityexpansiondepth":<Double_value>,"xmlmaxnamespacescheck":<String_value>,"xmlmaxnamespaces":<Double_value>,"xmlmaxnamespaceurilengthcheck":<String_value>,"xmlmaxnamespaceurilength":<Double_value>,"xmlsoaparraycheck":<String_value>,"xmlmaxsoaparraysize":<Double_value>,"xmlmaxsoaparrayrank":<Double_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete:



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appfwprofile_xmldosurl_binding/name_value&lt;String&gt;
<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appfwprofile_xmldosurl_binding/name_value&lt;String&gt;
<b>Query-parameters:</b>
<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appfwprofile_xmldosurl_binding/name_value&lt;String&gt;?<b>filter=property-name1:property-value1,property-name2:property-value2</b>
Use this query-parameter to get the filtered set of appfwprofile_xmldosurl_binding resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appfwprofile_xmldosurl_binding/name_value&lt;String&gt;?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the appfwprofile_xmldosurl_binding resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "appfwprofile_xmldosurl_binding": [ {"xmlmaxelementdepthcheck":<String_value>,"xmlmaxfilesize":<Double_value>,"xmlmaxnamespaceurilength":<Double_value>,"xmldosurl":<String_value>,"state":<String_value>,"xmlsoaparraycheck":<String_value>,"xmlmaxelementnamelengthcheck":<String_value>,"xmlmaxelementscheck":<String_value>,"xmlmaxentityexpansions":<Double_value>,"xmlmaxattributes":<Double_value>,"xmlmaxfilesizecheck":<String_value>,"xmlmaxchardatalength":<Double_value>,"xmlmaxnamespacescheck":<String_value>,"xmlmaxnamespaces":<Double_value>,"xmlmaxattributenamelengthcheck":<String_value>,"xmlblockdtd":<String_value>,"xmlmaxattributevaluelength":<Double_value>,"xmlmaxelementdepth":<Double_value>,"xmlmaxelementnamelength":<Double_value>,"name":<String_value>,"xmlblockpi":<String_value>,"xmlmaxelementchildrencheck":<String_value>,"xmlmaxelements":<Double_value>,"xmlmaxentityexpansionscheck":<String_value>,"xmlmaxnamespaceurilengthcheck":<String_value>,"xmlmaxentityexpansiondepthcheck":<String_value>,"xmlmaxattributevaluelengthcheck":<String_value>,"xmlmaxsoaparraysize":<Double_value>,"xmlmaxentityexpansiondepth":<Double_value>,"xmlmaxnodescheck":<String_value>,"xmlmaxattributenamelength":<Double_value>,"xmlmaxchardatalengthcheck":<String_value>,"xmlminfilesizecheck":<String_value>,"xmlmaxelementchildren":<Double_value>,"xmlminfilesize":<Double_value>,"xmlmaxnodes":<Double_value>,"comment":<String_value>,"xmlmaxattributescheck":<String_value>,"xmlmaxsoaparrayrank":<Double_value>,"xmlblockexternalentities":<String_value>}]}```



###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appfwprofile_xmldosurl_binding
<b>Query-parameters:</b>
<b>bulkbindings</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appfwprofile_xmldosurl_binding?<b>bulkbindings=yes</b>
NITRO allows you to fetch bindings in bulk.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "appfwprofile_xmldosurl_binding": [ {"xmlmaxelementdepthcheck":<String_value>,"xmlmaxfilesize":<Double_value>,"xmlmaxnamespaceurilength":<Double_value>,"xmldosurl":<String_value>,"state":<String_value>,"xmlsoaparraycheck":<String_value>,"xmlmaxelementnamelengthcheck":<String_value>,"xmlmaxelementscheck":<String_value>,"xmlmaxentityexpansions":<Double_value>,"xmlmaxattributes":<Double_value>,"xmlmaxfilesizecheck":<String_value>,"xmlmaxchardatalength":<Double_value>,"xmlmaxnamespacescheck":<String_value>,"xmlmaxnamespaces":<Double_value>,"xmlmaxattributenamelengthcheck":<String_value>,"xmlblockdtd":<String_value>,"xmlmaxattributevaluelength":<Double_value>,"xmlmaxelementdepth":<Double_value>,"xmlmaxelementnamelength":<Double_value>,"name":<String_value>,"xmlblockpi":<String_value>,"xmlmaxelementchildrencheck":<String_value>,"xmlmaxelements":<Double_value>,"xmlmaxentityexpansionscheck":<String_value>,"xmlmaxnamespaceurilengthcheck":<String_value>,"xmlmaxentityexpansiondepthcheck":<String_value>,"xmlmaxattributevaluelengthcheck":<String_value>,"xmlmaxsoaparraysize":<Double_value>,"xmlmaxentityexpansiondepth":<Double_value>,"xmlmaxnodescheck":<String_value>,"xmlmaxattributenamelength":<Double_value>,"xmlmaxchardatalengthcheck":<String_value>,"xmlminfilesizecheck":<String_value>,"xmlmaxelementchildren":<Double_value>,"xmlminfilesize":<Double_value>,"xmlmaxnodes":<Double_value>,"comment":<String_value>,"xmlmaxattributescheck":<String_value>,"xmlmaxsoaparrayrank":<Double_value>,"xmlblockexternalentities":<String_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appfwprofile_xmldosurl_binding/name_value&lt;String&gt;?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{"appfwprofile_xmldosurl_binding": [ { "__count": "#no"} ] }```



