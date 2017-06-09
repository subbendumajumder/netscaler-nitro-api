#location

Configuration for location resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>ipfrom</td><td>&lt;String></td><td>Read-write</td><td>First IP address in the range, in dotted decimal notation.&lt;br>Minimum length = 1</td><tr><tr><td>ipto</td><td>&lt;String></td><td>Read-write</td><td>Last IP address in the range, in dotted decimal notation.&lt;br>Minimum length = 1</td><tr><tr><td>preferredlocation</td><td>&lt;String></td><td>Read-write</td><td>String of qualifiers, in dotted notation, describing the geographical location of the IP address range. Each qualifier is more specific than the one that precedes it, as in continent.country.region.city.isp.organization. For example, "NA.US.CA.San Jose.ATT.citrix". &lt;br>Note: A qualifier that includes a dot (.) or space ( ) must be enclosed in double quotation marks.&lt;br>Minimum length = 1</td><tr><tr><td>longitude</td><td>&lt;Integer></td><td>Read-write</td><td>Numerical value, in degrees, specifying the longitude of the geographical location of the IP address-range. &lt;br>Note: Longitude and latitude parameters are used for selecting a service with the static proximity GSLB method. If they are not specified, selection is based on the qualifiers specified for the location.&lt;br>Minimum value = -180&lt;br>Maximum value = 180</td><tr><tr><td>latitude</td><td>&lt;Integer></td><td>Read-write</td><td>Numerical value, in degrees, specifying the latitude of the geographical location of the IP address-range. &lt;br>Note: Longitude and latitude parameters are used for selecting a service with the static proximity GSLB method. If they are not specified, selection is based on the qualifiers specified for the location.&lt;br>Minimum value = -90&lt;br>Maximum value = 90</td><tr><tr><td>q1label</td><td>&lt;String></td><td>Read-only</td><td>Least specific location qualifier.</td><tr><tr><td>q2label</td><td>&lt;String></td><td>Read-only</td><td>Location qualifier 2.</td><tr><tr><td>q3label</td><td>&lt;String></td><td>Read-only</td><td>Location qualifier 3.</td><tr><tr><td>q4label</td><td>&lt;String></td><td>Read-only</td><td>Location qualifier 4.</td><tr><tr><td>q5label</td><td>&lt;String></td><td>Read-only</td><td>Location qualifier 5.</td><tr><tr><td>q6label</td><td>&lt;String></td><td>Read-only</td><td>Most specific location qualifier.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [DELETE](#delete) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/location
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"location":{      "ipfrom":<String_value>,      "ipto":<String_value>,      "preferredlocation":<String_value>,      "longitude":<Integer_value>,      "latitude":<Integer_value>}}```
Response:
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/location/ipfrom_value&lt;String&gt;
HTTP Method: DELETE
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/location
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/location?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


filter
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/location?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of location resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/location?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).


pagination
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/location?pagesize=#no;pageno=#no
Use this query-parameter to get the location resources in chunks.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "location": [ {      "ipfrom":<String_value>,      "ipto":<String_value>,      "preferredlocation":<String_value>,      "q1label":<String_value>,      "q2label":<String_value>,      "q3label":<String_value>,      "q4label":<String_value>,      "q5label":<String_value>,      "q6label":<String_value>,      "longitude":<Integer_value>,      "latitude":<Integer_value>}]}```



###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/location/ipfrom_value&lt;String&gt;
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/location/ipfrom_value&lt;String&gt;?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/location/ipfrom_value&lt;String&gt;?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: ```{ "location": [ {      "ipfrom":<String_value>,      "ipto":<String_value>,      "preferredlocation":<String_value>,      "q1label":<String_value>,      "q2label":<String_value>,      "q3label":<String_value>,      "q4label":<String_value>,      "q5label":<String_value>,      "q6label":<String_value>,      "longitude":<Integer_value>,      "latitude":<Integer_value>}]}```



###count



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/location?count=yes
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the errorResponse Headers:

Content-Type:application/json

Response Payload: 
{ "location": [ { "__count": "#no"} ] }


