# Performing NetScaler Resource Operations
NetScaler resources are organized into a set of packages or namespaces. Each package or namespace corresponds to a NetScaler feature. For example, all load-balancing related resources, such as load balancing virtual server, load balancing group, and load balancing monitor are available in com.citrix.netscaler.nitro.resource.config.lb.

Similarly, all application firewall related resources, such as application firewall policy and application firewall archive are available in com.citrix.netscaler.nitro.resource.config.appfw.

Each NetScaler resource is represented by a class. For example, the class that represents a load balancing virtual server is called lbvserver (in com.citrix.netscaler.nitro.resource.config.lb). The state of a resource is represented by properties of a class. You can get and set the properties of the class.

The setter and getter properties are always executed locally on the client. They do not involve any network interaction with the NITRO web service. All properties have basic simple types: integer, long, boolean, and string.

## Adding a NetScaler Resource

This topic covers adding a NetScaler resource by using REST APIs through HTTP or SDKs. 

**Using REST APIs through HTTP**

To create a new resource (for example, an lbvserver) on the appliance, specify the resource name and other related arguments in the specific resource object.

For example, to create an load balancing virtual server named MyFirstLbVServer:

**Request**

**HTTP Method:** POST

**URL:** http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lbvserver

**Request Headers:**

Cookie:NITRO\_AUTH\_TOKEN=&lt;tokenvalue&gt;

Content-Type:application/json

**Request Payload:**

```json
{ 
    "lbvserver": 
    { 
    "name":"MyFirstLbVServer", 
    "servicetype":"http" 
    } 
}
```

**Response**

**HTTP Status Code on Success:** 201 Created

**HTTP Status Code on Failure:** 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error.

**Using REST APIs through SDKs**

To create a new resource, instantiate the resource class, configure the resource by setting its properties locally, and then upload the new resource instance to the NetScaler appliance.

The following sample code creates a load balancing virtual server.

**Java - Sample code to add a NetScaler resource**

```java
//Create an instance of the lbvserver class 

lbvserver new_lbvserver_obj = new lbvserver(); 

//Set the properties of the resource locally 

new_lbvserver_obj.set_name("MyFirstLbVServer"); 
new_lbvserver_obj.set_ipv46("10.102.29.88"); 
new_lbvserver_obj.set_port(88); 
new_lbvserver_obj.set_servicetype("HTTP"); 
new_lbvserver_obj.set_lbmethod("ROUNDROBIN"); 

//Upload the resource to NetScaler 

lbvserver.add(ns_session,new_lbvserver_obj);
```

**.NET - Sample code to add a NetScaler resource**

```csharp
//Create an instance of the lbvserver class 

lbvserver new_lbvserver_obj = new lbvserver();  

//Set the properties of the resource locally 

new_lbvserver_obj.name = "MyFirstLbVServer"; 
new_lbvserver_obj.ipv46 = "10.102.29.88"; 
new_lbvserver_obj.port = 88; 
new_lbvserver_obj.servicetype = "HTTP"; 
new_lbvserver_obj.lbmethod = "ROUNDROBIN"; 

//Upload the resource to NetScaler 

lbvserver.add(ns_session,new_lbvserver_obj);
```

**Python - Sample code to add a NetScaler resource**

```python
#Create an instance of the lbvserver class

new_lbvserver_obj = lbvserver()

#Set the properties of the resource locally

new_lbvserver_obj.name = "MyFirstLbVServer"
new_lbvserver_obj.ipv46 = "10.102.29.88"
new_lbvserver_obj.port = 88
new_lbvserver_obj.servicetype = "HTTP"
new_lbvserver_obj.lbmethod = "ROUNDROBIN"

#Upload the resource to NetScaler

lbvserver.add(ns_session, new_lbvserver_obj)
```

## Enabling a NetScaler Resource

This topic covers enabling a NetScaler resource by using REST APIs through HTTP or SDKs. 

**Using REST APIs through HTTP**

To enable a resource on the NetScaler appliance, specify the action as "enable" in the URL query string, and in the request payload, specify the resource to be enabled. To disable a resource, in the URL query string, specify the action as "disable".

For example, to enable a load balancing virtual server named MyFirstLbVServer.

**Request**

**HTTP Method:** POST

**URL:** http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lbvserver?action=enable

**Request Headers:**

Cookie:NITRO\_AUTH\_TOKEN=&lt;tokenvalue&gt;

Content-Type:application/json

**Request Payload:**

```json
{ 
    "lbvserver": 
    { 
    "name":"MyFirstLbVServer" 
    } 
}
```

**Response**

**HTTP Status Code on Success:** 200 OK

**HTTP Status Code on Failure:**

4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error.
    
**Using REST APIs through SDKs**

To enable a resource, invoke the enable() method and to disable, invoke the disable() method.

The following sample code enables a load balancing virtual server named lb_vip.

**Java - Sample code to enable a NetScaler resource**

```java
lbvserver obj = new lbvserver();

obj.set_name("lb_vip");

lbvserver.enable(ns_session, obj);
```

**.NET - Sample code to enable a NetScaler resource**

```csharp
lbvserver obj = new lbvserver(); 

obj.name = "lb_vip"; 

lbvserver.enable(ns_session, obj);
```

**Python - Sample code to enable a NetScaler resource**

```python
obj = lbvserver()

obj.name = "lb_vip"

lbvserver.enable(ns_session, obj)
```

## Retrieving Properties of NetScaler Resources

This topic covers retrieving properties of a NetScaler resource by using REST APIs through HTTP or SDKs. 

**Using REST APIs through HTTP**

NITRO provides multiple approaches using which you can retrieve resources and their relevant details. The following table explains each of these approaches with the required URL.

<table border=1>
<tbody>
<tr>
<td>
<p><strong>Retrieving all details of all resources of a specific type</strong></p>
</td>
<td>
<p>In the URL, specify the type of resource for which you want to retrieve the details.</p>
<p>For example, to retrieve all details of load balancing virtual servers available on a NetScaler appliance.</p>
<p>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lbvserver</p>
</td>
</tr>
<tr>
<td>
<p><strong>Retrieving all details of a specific resource</strong></p>
</td>
<td>
<p>In the URL, specify the name of resource for which you want to retrieve the details.</p>
<p>For example, to retrieve all details of a load balancing virtual server named MyFirstLbVServer:</p>
<p>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lbvserver/MyFirstLbVServer</p>
</td>
</tr>
<tr>
<td>
<p><strong>Retrieving summary or detailed view of resources</strong></p>
</td>
<td>
<p>In the URL, use the "view" query parameter to specify whether you want to view the summary (mandatory parameters) or detail (all parameters).</p>
<p>For example, to view the mandatory parameters for all load balancing virtual servers:</p>
<div>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lbvserver?view=summary
<div>Note: By default, the retrieved results are displayed in detail view (?view=detail).</div>
</div>
</td>
</tr>
<tr>
<td>
<p><strong>Retrieving all details of resources that have multiple unique identifiers</strong></p>
</td>
<td>
<p>In the URL, specify the type of resource and use the "args" query parameter to specify the unique attributes and the values for those attributes.</p>
<p>For example, to get the application firewall profiles that have unique identifiers "name" and "starturl" as appfw1 and aa respectively.</p>
<p>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appfwprofile?args=name:appfw1,starturl:aa</p>
</td>
</tr>
<tr>
<td>
<p><strong>Retrieving specific details of all resources of a specific type</strong></p>
</td>
<td>
<p>In the URL, specify the type of the resource and use the "attrs" query parameter to specify the resource details that you want to retrieve.</p>
<p>For example, to retrieve the "name" and "lbmethod" of all load balancing virtual servers:</p>
<p>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lbvserver?attrs=name,lbmethod</p>
</td>
</tr>
<tr>
<td>
<p><strong>Retrieving specific details of a specific resource</strong></p>
</td>
<td>
<p>In the URL, specify the type and name of the resource and use the "attrs" query parameter to specify the resource details that you want to retrieve.</p>
<p>For example, to retrieve the "name" and "lbmethod" of a load balancing virtual server named "MyFirstLbVServer":</p>
<p>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lbvserver/MyFirstLbVServer?attrs=name,lbmethod</p>
</td>
</tr>
<tr>
<td>
<p><strong>Filtering the retrieved resources</strong></p>
</td>
<td>
<p>In the URL, specify the type of resource and use the "filter" query parameter to specify the attribute(s) and the value(s) of the attributes. The resources fetched will be filtered based on the filter criteria.</p>
<div>
<div>Note: The filter query parameter supports the use of PCRE regular expressions.</div>
</div>
<p>For example, to filter the load balancing virtual servers where the "lbmethod" is ROUNDROBIN.</p>
<p>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lbvserver?filter=lbmethod:ROUNDROBIN</p>
</td>
</tr>
<tr>
<td>
<p><strong>Retrieving resources in paginated manner</strong></p>
</td>
<td>
<p>If the request is likely to result in a large number of resources, you can divide the results into pages and retrieve them page by page (paginated). For example, if you are retrieving all the 53 load balancing virtual servers of a NetScaler appliance, instead of retrieving all 53 in one response, you can configure the results to be divided into 6 pages each having 10 results.</p>
<div>In the URL, specify the name of the resource and use the following query parameters:
<ul>
<li>"pageno" - The page number to be displayed.</li>
<li>"pagesize" - The number of resources to be displayed in each page.</li>
</ul>
</div>
<p>For example, to retrieve the load balancing virtual servers in a paginated form, first get a count (using the "count" query parameter shown in below row) of the load balancing virtual servers. Then, accordingly specify the number of results for each page and then specify the page number to be displayed.</p>
<p>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lbvserver?pagesize=10&amp;pageno=3</p>
</td>
</tr>
</tbody>
</table>

For example, to retrieve only the name and load balancing method of all load balancing virtual servers on a NetScaler.

**Request**
    
**HTTP Method:** GET

**URL:** http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lbvserver?attrs=name,lbmethod

**Request Headers:**

Cookie:NITRO\_AUTH\_TOKEN=&lt;tokenvalue&gt;

Accept:application/json

**Response**

**HTTP Status Code on Success:** 200 OK

**HTTP Status Code on Failure:**

4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error.

**Response Header:**

Content-Type:application/json

**Response Payload:**

```json
{ 
    lbvserver: 
    { 
        name: "test", 
        lbmethod: "LEASTCONNECTION" 
    } 
    { 
        name: "test1", 
        lbmethod: "LEASTCONNECTION" 
    } 
}
```

**Using REST APIs through SDKs**

To retrieve the properties of a resource, you retrieve the resource object from the NetScaler appliance. Once the object is retrieved, you can extract the required properties of the resource locally, without further network traffic.

The following sample code retrieves the details of a load balancing virtual server.

**Java - Sample code to get details of resource**

```java
//Retrieve the resource object from the NetScaler 

new_lbvserver_obj = lbvserver.get(ns_session,"MyFirstLbVServer"); 

//Extract the properties of the resource from the object locally 

System.out.println(new_lbvserver_obj.get_name()); 
System.out.println(new_lbvserver_obj.get_servicetype());
```

**.NET - Sample code to get details of resource**

```csharp
//Retrieve the resource object from the NetScaler 

new_lbvserver_obj = lbvserver.get(ns_session,"MyFirstLbVServer"); 

//Extract the properties of the resource from the object locally 

Console.WriteLine(new_lbvserver_obj.name); 
Console.WriteLine(new_lbvserver_obj.servicetype);
```

**Python - Sample code to get details of resource**

```python
#Retrieve the resource object from the NetScaler

new_lbvserver_obj = lbvserver.get(ns_session,"MyFirstLbVServer")

#Extract the properties of the resource from the object locally

print(new_lbvserver_obj.name)
print(new_lbvserver_obj.servicetype)
```

### Filtering Results

This topic covers retrieving filtered information of a resource by using REST APIs through SDKs. 

**Using REST APIs through SDKs**

You can also retrieve resources by specifying a filter on the value of their properties by using the com.citrix.netscaler.nitro.util.filtervalue class.

For example, you can retrieve all the load balancing virtual servers that have their port set to 80 and servicetype to HTTP.

**Java - Sample code to get filtered results**

```java
filtervalue[] filter = new filtervalue[2];
filter[0] = new filtervalue("port","80");
filter[1] = new filtervalue("servicetype","HTTP");
lbvserver[] result = lbvserver.get_filtered(ns_session,filter);
```

**.NET - Sample code to get filtered results**

```csharp
filtervalue[] filter = new filtervalue[2]; 
filter[0] = new filtervalue("port","80"); 
filter[1] = new filtervalue("servicetype","HTTP"); 
lbvserver[] result = lbvserver.get_filtered(ns_session,filter);
```

**Python - Sample code to get filtered results**

```python
filter_params = []

      filter_params = [ filtervalue() for _ in range(2)]

      filter_params[0] = filtervalue("servicetype","HTTP")

      filter_params[1] = filtervalue("port","80")

      result = lbvserver.get_filtered(ns_session1, filter_params)
```

## Retrieving Statistics of NetScaler Resources
The NetScaler appliance collects statistics about the usage of its features and the corresponding resources. NITRO can retrieve these statistics. Not all NetScaler features and resources have statistic objects associated with them.

**Using REST APIs through HTTP**

To get statistics of a feature, the URL format must be: http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/\<feature_name\>.

To get statistics of a resource, the URL format must be: http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/\<resource_type\>/\<resource_name\>.

To get statistics of the services and service groups that are bound to a load balancing virtual server, the URL format must be: http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/lbvserver/\<name\>?statbindings=yes*.

**Request**
    
**HTTP Method:** GET

**URL:** http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/lbvserver/MyFirstLbVServer

**Request Headers:**

Cookie:NITRO\_AUTH\_TOKEN=\<tokenvalue\>

Accept:application/json


**Response**
    
**HTTP Status Code on Success:** 200 OK

**HTTP Status Code on Failure:**

4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error.

**Response Payload:**

```json
{

    "lbvserver":

    [

        {

            "name":"MyFirstLbVServer",

            "establishedconn":0,

            "vslbhealth":0,

            "primaryipaddress":"0.0.0.0",

            ...

        }

    ]

}
```

To get statistics of the bound entities, use statbindings=yes.
For example, to get the statistics of the services that are bound to a load balancing virtual server named MyFirstLbVServer.

**Request**
    
**HTTP Method:** GET

**URL:** http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/lbvserver/MyFirstLbVServer?statbindings=yes

**Request Headers:**

Cookie:NITRO\_AUTH\_TOKEN=\<tokenvalue\>

Accept:application/json


**Response**
    
**HTTP Status code on success:** 200 OK  

**HTTP Status code on failure:**

4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error.   

**Response Header:**

Content-Type:application/json

**Response Payload:**

```json
{


"lbvserver": [{


    "name": "MyFirstLbVServer",


    "sortorder": "descending",


    "vsvrsurgecount": "0",


    "establishedconn": "0",

    ...

    "service": [{


        "name": "s1",


        "throughput": "0",


        "throughputrate": 0,


        "avgsvrttfb": "0",  


        "primaryipaddress": "1.2.3.5",


        "primaryport": 80,


        "servicetype": "HTTP",


        "state": "DOWN",


            "totalrequests": "0",


            "requestsrate": 0,

            ...

            }]
    }]

}
```

**Using REST APIs through SDKs**

The NetScaler appliance collects statistics about the usage of its features and the corresponding resources. You can retrieve these statistics by using NITRO API. The statistics APIs are available in different packages from the configuration APIs.

For example, the API to retrieve statistics of the load balancing virtual server are available in 
com.citrix.netscaler.nitro.resource.stat.lb.

**Note.**
* For the python SDK, the package path is of the form nssrc.com.citrix.netscaler......
* Not all NetScaler features and resources have statistic objects associated with them.

The following sample code retrieves the statistics of a load balancing virtual server and displays some of the statistics returned.

**Java - Sample code to get feature statistics**

```java
lbvserver_stats stats = lbvserver_stats.get(ns_session,"MyFirstLbVServer"); 

System.out.println(stats.get_curclntconnections()); 

System.out.println(stats.get_deferredreqrate());
```

**.NET - Sample code to get feature statistics**

```csharp
lbvserver_stats stats = lbvserver_stats.get(ns_session,"MyFirstLbVServer");

Console.WriteLine(stats.curclntconnections);

Console.WriteLine(stats.deferredreqrate);
```

**Python - Sample code to get feature statistics**

```python
stats = lbvserver_stats.get(ns_session,"MyFirstLbVServer")

print(stats.curclntconnections)

print(stats.deferredreqrate)
```

## Retrieving Statistics of NetScaler Resources
The NetScaler appliance collects statistics about the usage of its features and the corresponding resources. NITRO can retrieve these statistics. Not all NetScaler features and resources have statistic objects associated with them.

**Using REST APIs through HTTP**

To get statistics of a feature, the URL format must be: http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/\<feature_name\>.

To get statistics of a resource, the URL format must be: http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/\<resource_type\>/\<resource_name\>.

To get statistics of the services and service groups that are bound to a load balancing virtual server, the URL format must be: http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/lbvserver/\<name\>?statbindings=yes*.

**Request**
    
**HTTP Method:** GET

**URL:** http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/lbvserver/MyFirstLbVServer

**Request Headers:**

Cookie:NITRO\_AUTH\_TOKEN=\<tokenvalue\>

Accept:application/json


**Response**
    
**HTTP Status Code on Success:** 200 OK

**HTTP Status Code on Failure:**

4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error.

**Response Payload:**

```json
{

    "lbvserver":

    [

        {

            "name":"MyFirstLbVServer",

            "establishedconn":0,

            "vslbhealth":0,

            "primaryipaddress":"0.0.0.0",

            ...

        }

    ]

}
```

To get statistics of the bound entities, use statbindings=yes.
For example, to get the statistics of the services that are bound to a load balancing virtual server named MyFirstLbVServer.

**Request**
    
**HTTP Method:** GET

**URL:** http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/lbvserver/MyFirstLbVServer?statbindings=yes

**Request Headers:**

Cookie:NITRO\_AUTH\_TOKEN=\<tokenvalue\>

Accept:application/json


**Response**
    
**HTTP Status code on success:** 200 OK  

**HTTP Status code on failure:**

4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error.   

**Response Header:**

Content-Type:application/json

**Response Payload:**

```json
{


"lbvserver": [{


    "name": "MyFirstLbVServer",


    "sortorder": "descending",


    "vsvrsurgecount": "0",


    "establishedconn": "0",

    ...

    "service": [{


        "name": "s1",


        "throughput": "0",


        "throughputrate": 0,


        "avgsvrttfb": "0",  


        "primaryipaddress": "1.2.3.5",


        "primaryport": 80,


        "servicetype": "HTTP",


        "state": "DOWN",


            "totalrequests": "0",


            "requestsrate": 0,

            ...

            }]
    }]

}
```

**Using REST APIs through SDKs**

The NetScaler appliance collects statistics about the usage of its features and the corresponding resources. You can retrieve these statistics by using NITRO API. The statistics APIs are available in different packages from the configuration APIs.

For example, the API to retrieve statistics of the load balancing virtual server are available in 
com.citrix.netscaler.nitro.resource.stat.lb.

**Note:**
* For the python SDK, the package path is of the form nssrc.com.citrix.netscaler......
* Not all NetScaler features and resources have statistic objects associated with them.

The following sample code retrieves the statistics of a load balancing virtual server and displays some of the statistics returned.

**Java - Sample code to get feature statistics**

```java
lbvserver_stats stats = lbvserver_stats.get(ns_session,"MyFirstLbVServer"); 

System.out.println(stats.get_curclntconnections()); 

System.out.println(stats.get_deferredreqrate());
```

**.NET - Sample code to get feature statistics**

```csharp
lbvserver_stats stats = lbvserver_stats.get(ns_session,"MyFirstLbVServer");

Console.WriteLine(stats.curclntconnections);

Console.WriteLine(stats.deferredreqrate);
```

**Python - Sample code to get feature statistics**

```python
stats = lbvserver_stats.get(ns_session,"MyFirstLbVServer")

print(stats.curclntconnections)

print(stats.deferredreqrate)
```

## Updating a NetScaler Resource
You can modify the properties of a resource after creating it.

Some properties in some NetScaler resources are not allowed to be modified after creation. The port number or the service type (protocol) of a load balancing virtual server or a service, are examples of such properties. Even though the update method appears to succeed, these properties retain their original values on the appliance.

**Using REST APIs through HTTP**

To update the details of an existing resource on the NetScaler appliance, specify the name of the resource in the URL, and in the request payload,within the specific resource object, specify the name and the updated details of the resource.

For example, to change the load balancing method to ROUNDROBIN and update the comment property for a load balancing virtual server named MyFirstLbVServer:

**Request**

**HTTP Method:** PUT

**URL:** http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lbvserver/MyFirstLbVServer

**Request Headers:**

Cookie:NITRO\_AUTH\_TOKEN=&lt;tokenvalue&gt;

Content-Type:application/json

**Request Payload:**

```json
{ 
    "lbvserver": 
    { 
        "name":"MyFirstLbVServer", 
        "lbmethod":"ROUNDROBIN", 
        "comment":"Updated comments" 
    } 
}
```

**Response**

**HTTP Status Code on Success:** 200 OK

**HTTP Status Code on Failure:**

4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error.

**Using REST APIs through SDKs**

To update the properties of a resource, instantiate the resource class, specify the name of the resource to be updated, configure the resource by updating its properties locally, and then upload the updated resource instance to the NetScaler appliance.

The following sample code updates the service type and load balancing method of a load balancing virtual server.

**Java - Sample code to update a NetScaler resource**

```java
//Create an instance of the lbvserver class 

lbvserver update_lb = new lbvserver(); 

//Specify the name of the lbvserver to be updated 

update_lb.set_name("MyFirstLbVServer"); 

//Specify the updated service type and lb method 

update_lb.set_servicetype("https"); 
update_lb.set_lbmethod("LEASTRESPONSETIME"); 

//Upload the resource to NetScaler 

lbvserver.update(ns_session,update_lb);
```

**.NET - Sample code to update a NetScaler resource**

```csharp
//Create an instance of the lbvserver class 

lbvserver update_lb = new lbvserver(); 

//Specify the name of the lbvserver to be updated 

update_lb.name = "MyFirstLbVServer"; 

//Specify the updated service type and lb method 

update_lb.servicetype = "https"; 
update_lb.lbmethod = "LEASTRESPONSETIME"; 

//Upload the resource to NetScaler 

lbvserver.update(ns_session, update_lb);
```

**Python - Sample code to update a NetScaler resource**

```python
#Create an instance of the lbvserver class

update_lb = lbvserver()

#Specify the name of the lbvserver to be updated

update_lb.name = "MyFirstLbVServer"

#Specify the updated service type and lb method

update_lb.servicetype = "https"
update_lb.lbmethod = "LEASTRESPONSETIME"

#Upload the resource to the NetScaler

lbvserver.update(ns_session, update_lb)
```

## Binding NetScaler Resources

NetScaler resources form relationships with each other through the process of binding. This is how services are associated with a load balancing virtual server, or how policies are bound to a load balancing virtual server. Each binding relationship is represented by its own object.

A binding resource has properties representing the name of each NetScaler resource in the binding relationship. It can also have other properties related to that relationship (for example, the weight of the binding between an lbvserver resource and a service resource).

**Using REST APIs through HTTP**

To bind one NetScaler resource to another, you must instantiate the appropriate binding class (for example, to bind a service to a load balancing virtual server, you must instantiate the lbvserver_service_binding class) and add it to the NetScaler configuration (by using the static add() method on this class).

To unbind a resource, use the DELETE method and specify an "args" query string parameter in the URL that contains the attribute name and value in the relationship resource that designates the secondary resource.

The following example binds a service named svc_prod to a load balancing virtual server named MyFirstLbVServer and specify a weight for the binding.

**Request**

**HTTP Method:** POST

**URL:** http://\<netscaler-ip-address \>/nitro/v1/config/lbvserver_service_binding

**Request Headers:**
Cookie:NITRO\_AUTH\_TOKEN=&lt;tokenvalue&gt;
Content-Type:application/json

**Request Payload:**

```json
{ 
"lbvserver_service_binding": 
    { 
    "servicename":"svc_prod", 
    "weight":"20", 
    "name":"MyFirstLbVServer" 
    } 
}
```

**Response**

**HTTP Status Code on Success:** 201 Created

**HTTP Status Code on Failure:**  4xx \<string \> (for general HTTP errors) or 5xx \<string \> (for NetScaler-specific errors). The response payload provides details of the error.

The following example binds a policy to a policy label.

**Request**

**HTTP Method:** POST

**URL:** http://\<netscaler-ip-address \>/nitro/v1/config/authenticationpolicylabel_authenticationpolicy_binding

**Request Headers:**

Cookie:NITRO\_AUTH\_TOKEN=&lt;tokenvalue&gt;

Content-Type:application/json

**Request Payload:**

```json
{ 
"authenticationpolicylabel_authenticationpolicy_binding": 
    { 
    "policyname":"p1", 
    "priority":"100", 
    "gotopriorityexpression":"END", 
    "labelname":"pl1" 
    } 
}
```

**Response**

**HTTP Status Code on Success:** 201 Created

**HTTP Status Code on Failure:**

4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error.

The following example unbinds the service svc_prod from the load balancing virtual server MyFirstLbVServer.

**Request**

**HTTP Method:** DELETE

**URL:** http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lbvserver_service_binding/MyFirstLbVServer?args=servicename:svc_prod

**Request Header:**

Cookie:NITRO\_AUTH\_TOKEN=\<tokenvalue\>

**Response**

**HTTP Status Code on Success:** 200 OK

**HTTP Status Code on Failure:**

4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error.

**Using REST APIs through SDKs**

To bind one NetScaler resource to another, you must instantiate the appropriate binding class (for example, to bind a service to a load balancing virtual server, you must instantiate the lbvserver_service_binding class) and add it to the NetScaler configuration (by using the static add() method on this class).

To unbind a resource from another, invoke the delete() method from the resource binding class, by passing the name of the two resources.

The following sample code binds a service to a load balancing virtual server, by specifying a certain weight for the binding.

**Java - Sample code for binding** 

```java
lbvserver_service_binding bindObj = new lbvserver_service_binding(); 
bindObj.set_name("MyFirstLbVServer"); 
bindObj.set_servicename("svc_prod"); 
bindObj.set_weight(20); 
lbvserver_service_binding.add(ns_session,bindObj);
```

**.NET - Sample code for binding**

```csharp
lbvserver_service_binding bindObj = new lbvserver_service_binding(); 
bindObj.name = "MyFirstLbVServer"; 
bindObj.servicename = "svc_prod"; 
bindObj.weight = 20; 
lbvserver_service_binding.add(ns_session,bindObj);
```

**Python - Sample code for binding**

```python
bindObj = lbvserver_service_binding()
bindObj.name = "MyFirstLbVServer"
bindObj.servicename = "svc_prod"
bindObj.weight = 20
lbvserver_service_binding.add(ns_session, bindObj)
```

The following code sample unbinds a service from a server.

**Java - Sample Code for unbinding**

```java
lbvserver_service_binding bindObj = new lbvserver_service_binding(); 
bindObj.set_name("MyFirstLbVServer"); 
bindObj.set_servicename("svc_prod"); 
lbvserver_service_binding.delete(ns_session,bindObj);
```

**.NET - Sample code for unbinding**

```csharp
lbvserver_service_binding bindObj = new lbvserver_service_binding(); 
bindObj.name("MyFirstLbVServer"); 
bindObj.servicename("svc_prod"); 
lbvserver_service_binding.delete(ns_session,bindObj);
```

**Python - Sample code for unbinding**

```python
bindObj = lbvserver_service_binding()
bindObj.name = "MyFirstLbVServer"
bindObj.servicename = "svc_prod"
lbvserver_service_binding.delete(ns_session, bindObj)
```

## Globally Binding NetScaler Resources
Some NetScaler resources can be bound globally to affect the whole system. For example, a compression policy can be bound to an load balancing virtual server, in which case the policy affects only the traffic on that load balancing virtual server. However, if bound globally, it can affect any traffic on the appliance, regardless of which virtual servers handle the traffic.

The names of NITRO resources that can be used to bind resources globally have the pattern *\<featurename \>global_\<resourcetype \>_binding*. For example, the object *aaaglobal_aaapreauthenticationpolicy_binding* is used to bind preauthentication policies globally.


**Using REST APIs through HTTP**

The following example binds the policy named preautpol1 globally at priority 200.

**Request**

**HTTP Method:** POST

**URL:** 

http://\<netscaler-ip-address \>/nitro/v1/config/aaaglobal_aaapreauthenticationpolicy_binding/preautpol1

**Request Headers:**

Cookie:NITRO\_AUTH\_TOKEN=&lt;tokenvalue&gt;

Content-Type:application/json

**Request Payload:**

```json
{ 
"aaaglobal_aaapreauthenticationpolicy_binding": 
    { 
    "policy":"preautpol1", 
    "priority":"200" 
    } 
}
```

**Response**

**HTTP Status Code on Success:** 200 OK

**HTTP Status Code on Failure:**

4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error.

The following example unbinds the policy named preautpol1.

**Request**

**HTTP Method:** DELETE

**URL:** 

http://\<netscaler-ip-address \>/nitro/v1/config/aaaglobal_aaapreauthenticationpolicy_binding?args=policy:preautpol1

**Request Header:**

Cookie:NITRO\_AUTH\_TOKEN=\<tokenvalue\>

**Response**

**HTTP Status Code on Success:** 200 OK

**HTTP Status Code on Failure:**

4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error.

**Using REST APIs through SDKs**

The following sample code creates a preauthentication action and a preauthentication policy that uses that action, and then binds the policy globally at priority 200.

**Java - Sample code**

```java
aaapreauthenticationaction preauth_act1; 

aaapreauthenticationpolicy preauth_pol1; 

aaaglobal_aaapreauthenticationpolicy_binding glob_binding; 

preauth_act1 = new aaapreauthenticationaction(); 

preauth_act1.set_name("preauth_act1"); 

preauth_act1.set_preauthenticationaction("ALLOW"); 

aaapreauthenticationaction.add(ns_session,preauth_act1); 

preauth_pol1 = new aaapreauthenticationpolicy(); 

preauth_pol1.set_name("preauth_pol1"); 

preauth_pol1.set_rule("CLIENT.APPLICATION.PROCESS(antivirus.exe) EXISTS"); 

preauth_pol1.set_reqaction("preauth_act1"); 

aaapreauthenticationpolicy.add(ns_session,preauth_pol1); 

 
 glob_binding = new aaaglobal_aaapreauthenticationpolicy_binding(); 

glob_binding.set_policy("preauth_pol1"); 

glob_binding.set_priority(200); 

aaaglobal_aaapreauthenticationpolicy_binding.add(ns_session,glob_binding);
```


**.NET - Sample code**

```csharp
aaapreauthenticationaction preauth_act1; 

aaapreauthenticationpolicy preauth_pol1; 

aaaglobal_aaapreauthenticationpolicy_binding glob_binding; 

preauth_act1 = new aaapreauthenticationaction(); 

preauth_act1.name = "preauth_act1"; 

preauth_act1.preauthenticationaction = "ALLOW"; 

aaapreauthenticationaction.add(ns_session, preauth_act1); 

 

preauth_pol1 = new aaapreauthenticationpolicy(); 

preauth_pol1.name = "preauth_pol1"; 

preauth_pol1.rule = "CLIENT.APPLICATION.PROCESS(antivirus.exe) EXISTS"; 

preauth_pol1.reqaction = "preauth_act1"; 

aaapreauthenticationpolicy.add(ns_session, preauth_pol1); 

 

glob_binding = new aaaglobal_aaapreauthenticationpolicy_binding(); 

glob_binding.policy = "preauth_pol1";  

glob_binding.priority = 200; 

aaaglobal_aaapreauthenticationpolicy_binding.add(ns_session,glob_binding);
```


**Python - Sample code**

```python
preauth_act1 = aaapreauthenticationaction()

preauth_act1.name = "preauth_act1"

preauth_act1.preauthenticationaction = "ALLOW"

aaapreauthenticationaction.add(ns_session, preauth_act1)


preauth_pol1 = aaapreauthenticationpolicy()

preauth_pol1.name = "preauth_pol1"

preauth_pol1.rule = "CLIENT.APPLICATION.PROCESS(antivirus.exe) EXISTS"

preauth_pol1.reqaction = "preauth_act1"

aaapreauthenticationpolicy.add(ns_session, preauth_pol1)


glob_binding = aaaglobal_aaapreauthenticationpolicy_binding()

glob_binding.policy = "preauth_pol1"

glob_binding.priority = 200

aaaglobal_aaapreauthenticationpolicy_binding.add(ns_session, glob_binding)
```

## Deleting a NetScaler Resource
The usage of the delete operation depends on the unique identifiers (UIDs) of the resource being deleted.

Deleting Resource with Single UID. To delete a NetScaler resource that can be identified by a single identifier, specify the resource name.
Deleting Resource with Multiple UIDs. To delete a NetScaler resource that is identified using multiple identifiers, use the "args" query parameter to specify the unique attributes along with their values.

**Using REST APIs through HTTP**

The following example deletes a load balancing virtual server named MyFirstLbVServer.

**Request**

**HTTP Method:** DELETE

**URL:** http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lbvserver/MyFirstLbVServer

**Request Header:** Cookie:NITRO\_AUTH\_TOKEN=\<tokenvalue\>

**Response**

**HTTP Status Code on Success:** 200 OK

**HTTP Status Code on Failure:**

4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error.

The following example deletes a resource with multiple UIDs. Consider a SNIP (10.102.29.71) that belongs to two traffic domains (TDs) 123 and 110. To delete the SNIP from one of the traffic domains, specify the IP address and the relevant TD in the URL as follows:

**Request**

**HTTP Method:** DELETE

**URL:** 

http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsip?args=ipaddress:10.102.29.71,td:123

**Request Header:** Cookie:NITRO\_AUTH\_TOKEN=\<tokenvalue\>

**Response**

**HTTP Status Code on Success:** 200 OK

**HTTP Status Code on Failure:**

4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error.

**Using REST APIs through SDKs**

To delete an existing resource, invoke the static method delete() on the resource class, by passing the name of the resource.

The following sample code deletes a load balancing virtual server with name MyFirstLbVServer.

**Java - Sample code to delete a NetScaler resource**

```java
lbvserver remove_lb = new lbvserver(); 
remove_lb.set_name("MyFirstLbVServer"); 
lbvserver.delete(ns_session, remove_lb);
```

**.NET - Sample code to delete a NetScaler resource**

```csharp
lbvserver remove_lb = new lbvserver(); 
remove_lb.name("MyFirstLbVServer"); 
lbvserver.delete(ns_session, remove_lb);
```

**Python - Sample code to delete a NetScaler resource**

```python
remove_lb = lbvserver()
remove_lb.name = "MyFirstLbVServer"
lbvserver.delete(ns_session, remove_lb)
```

## Performing Bulk Operations
You can create, retrieve, update, and delete multiple resources simultaneously and thus minimize network traffic. For example, you can add multiple load balancing virtual servers in the same operation. 

To account for the failure of some operations within the bulk operation, NITRO allows you to configure one of the following behaviors while establishing a connection with the appliance.

* **Exit**. When the first error is encountered, the execution stops. The commands that were executed before the error are committed.
* **Rollback**. When the first error is encountered, the execution stops. The commands that were executed before the error are rolled back. Rollback is only supported for add and bind commands.
* **Continue**. All the commands in the list are executed even if some commands fail.

**Using REST APIs through HTTP**

To perform a bulk operation, specify the required parameters in the same request payload. You must specify the behavior of the bulk operation in the request header using the X-NITRO-ONERROR parameter.

The following example adds two load balancing virtual servers in one operation. The operation continues even if one of the add operation fails.

**Request**

**HTTP Method:** POST

**URL:** http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lbvserver

**Request Headers:**

Cookie:NITRO\_AUTH\_TOKEN=&lt;tokenvalue&gt;

Content-Type:application/json

**Request Payload:**

```json
{ 
    "lbvserver": 
    [ 
        { 
        "name":"new_lbvserver1", 
        "servicetype":"http" 
        }, 

        { 
        "name":"new_lbvserver2", 
        "servicetype":"http" 
        } 
    ] 
}
```

**Response**

**HTTP Status Code on Success:**
201 Created for the add operation and 200 OK for the update operation.

**HTTP Status Code on Failure:**
207 Multi Status with error details in the response payload.

The following example enables multiple load balancing virtual servers in the same operation.

**Request**

**HTTP Method:** POST

**URL:** http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lbvserver?action=enable

**Request Headers:**

Cookie:NITRO\_AUTH\_TOKEN=\<tokenvalue\>

Content-Type:application/json

**Request Payload:**

```json
{
            "lbvserver":
    [
        {
            "name":"v1",
        },

        {
            "name":"v2",
        }
    ]
}
```

**Response**

**HTTP Status Code on Success:** 201 Created for the add operation and 200 OK for the update operation.

**HTTP Status Code on Failure:** 207 Multi Status with error details in the response payload. 

**Using REST APIs through SDKs**

To perform a bulk operation, you instantiate an array of the resource class, configure the properties of all the instances locally, and then upload all the instances to the NetScaler with one command.

The following sample code specifies bulk operation behavior.

**Java - Sample code to specify bulk operation behavior**

```java
nitro_service ns_session = new nitro_service("10.102.29.60","http"); 
ns_session.set_onerror(OnerrorEnum.CONTINUE); 
ns_session.login("admin","verysecret");
```

**.NET - Sample code to specify bulk operation behavior**

```csharp
nitro_service ns_session = new nitro_service("10.102.29.60","http"); 
ns_session.onerror = OnerrorEnum.CONTINUE; 
ns_session.login("admin","verysecret");
```

**Python - Sample code to specify bulk operation behavior**

```python
ns_session = nitro_service("10.102.29.60","http")
ns_session.onerror = OnerrorEnum.CONTINUE
ns_session.login("admin","verysecret")
```

The following sample code creates two load balancing virtual servers.

**Java - Sample code for bulk creation**

```java
//Create an array of lbvserver instances 

lbvserver[] lbs = new lbvserver[2]; 

//Specify properties of the first lbvserver 

lbs[0] = new lbvserver(); 
lbs[0].set_name("lbvserv1"); 
lbs[0].set_servicetype("http"); 
lbs[0].set_ipv46("10.70.136.5"); 
lbs[0].set_port(80); 

//Specify properties of the second lbvserver 

lbs[1] = new lbvserver(); 
lbs[1].set_name("lbvserv2"); 
lbs[1].set_servicetype("https"); 
lbs[1].set_ipv46("10.70.136.5"); 
lbs[1].set_port(443); 

//Upload the properties of the two lbvservers to the NetScaler 

lbvserver.add(ns_session,lbs);
```

**.NET - Sample code for bulk creation**

```csharp
//Create an array of lbvserver instances 
lbvserver[] lbs = new lbvserver[2]; 

//Specify details of first lbvserver 

lbs[0] = new lbvserver(); 
lbs[0].name = "lbvserv1"; 
lbs[0].servicetype = "http"; 
lbs[0].ipv46 = "10.70.136.5"; 
lbs[0].port = 80; 

//Specify details of second lbvserver 

lbs[1] = new lbvserver(); 
lbs[1].name = "lbvserv2"; 
lbs[1].servicetype = "https"; 
lbs[1].ipv46 = "10.70.136.5"; 
lbs[1].port = 443; 

//upload the details of the lbvservers to the NITRO server 

lbvserver.add(ns_session,lbs);
```

**Python - Sample code for bulk creation**

```python
#Create an array of lbvserver instances

lbs = lbvserver[2]

#Specify properties of the first lbvserver

lbs[0] = lbvserver()
lbs[0].name = "lbvserv1"
lbs[0].servicetype = "http"
lbs[0].ipv46 = "10.70.136.5"
lbs[0].port = 80

#Specify properties of the second lbvserver

lbs[1] = lbvserver()
lbs[1].name = "lbvserv2"
lbs[1].servicetype = "https"
lbs[1].ipv46 = "10.70.136.5"
lbs[1].port = 443

#Upload the properties of the two lbvservers to the NetScaler

lbvserver.add(ns_session, lbs)
```

## Getting the Count of NetScaler Resources

This topic covers getting the count of a type of NetScaler resource present in a NetScaler appliance by using REST APIs through HTTP. 


**Using REST APIs through HTTP**

To get a count of a specific resource type, in the URL specify the count query parameter as "yes".

For example, to get a count of all the load balancing virtual servers.

**Request**

**HTTP Method:** GET

**URL:** http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lbvserver?count=yes

**Request Headers:**

Cookie:NITRO\_AUTH\_TOKEN=&lt;tokenvalue&gt;

Accept:application/json

**Response**

**HTTP Status Code on Success:** 200 OK

**HTTP Status Code on Failure:**

4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error.

**Response Header:**

Content-Type:application/json

**Response Payload:**

```json
{ 
    "lbvserver": 
    [ 
        { 
            "__count": 4 
        } 
    ] 
}
```


## Renaming a NetScaler Resource

This topic covers renaming a NetScaler resource by using REST APIs through HTTP. 

**Using REST APIs through HTTP**

To change the name of an existing resource, specify the action as "rename" in the URL query string, and in the request payload, specify the existing name and the new name.

For example, to change the name of a load balancing virtual server from MyFirstLbVServer to MyServer:

**Request**

**HTTP Method:** POST

**URL:** http://\<netscaler-ip-address \>/nitro/v1/config/lbvserver?action=rename

**Request Headers:**

Cookie:NITRO\_AUTH\_TOKEN=&lt;tokenvalue&gt;

Content-Type:application/json

**Request Payload:**

```json
{ 
    "lbvserver": 
    { 
        "name":"MyFirstLbVServer", 
        "newname":"MyServer" 
    } 
}
```

**Response**

**HTTP Status Code on Success:** 200 OK

**HTTP Status Code on Failure:**

4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error.
    
## Performing File Operations

NetScaler operations such as configuring SSL certificates requires the input files to be available locally on the NetScaler appliance. NITRO allows you to perform file operations such as uploading files, retrieving files, retrieving file content, and deleting files of types: txt, cert, req, xml, lic, and key.

**Notes**

* File size must be less than or equal to 2 MB.
* Use the "BASE64" value for the fileencoding attribute in the request payload. This is the only valid encoding currently supported.
* The filelocation path must be URL encoded. For example, if the path is /nsconfig/ssl, encode the / and use the file location as %2Fnsconfig%2Fssl.
* When uploading a file, make sure that each directory of the file path has the 755 (read, write, execute) permission. For example, to upload a file to the "/nsconfig/ssl/" directory, the following directories must have the 755 permission:
flash (because the "/nsconfig" folder is actually a link to "/flash/nsconfig/" directory)
    * nsconfig
    * ssl

### Uploading a File

To upload a file to the NetScaler, specify a name for the file, the location where the file must be created on the NetScaler, and the content of the file.

**Using REST APIs through HTTP**

For example, to upload a file named cert1.crt in the /nsconfig/ssl/ directory:

**Request**

**HTTP Method:** POST

**URL:** http://&lt;netscaler-ip-address&gt;/nitro/v1/config/systemfile

**Request Headers:**

Cookie:NITRO\_AUTH\_TOKEN=&lt;tokenvalue&gt;

Content-Type:application/json

**Request Payload:**

```json
{ 
        "systemfile": 
        { 
            "filename": "cert1.crt", 
            "filelocation": "/nsconfig/ssl/",        
            "filecontent":"VGhpcyBpcyBteSBmaWxl", 
            "fileencoding": "BASE64" 
        } 
}
```

**Response**

**HTTP Status Code on Success:** 200 OK

**HTTP Status Code on Failure:**

4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error.

### Retrieving the Files

To retrieve the files from a specific NetScaler directory, specify the directory path in the URL.

**Using REST APIs through HTTP**

For example, to retrieve the files from the /nsconfig/ssl directory.

**Request**

**HTTP Method:** GET

**URL:**

http://&lt;netscaler-ip-address&gt;/nitro/v1/config/systemfile?args=filelocation:%2Fnsconfig%2Fssl

**Request Header:**

Cookie:NITRO\_AUTH\_TOKEN=\<tokenvalue\>

Accept:application/json

**Response**

**HTTP Status Code on Success:** 200 OK

**HTTP Status Code on Failure:**

4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error.

**Response Header:**

Content-Type:application/json

**Response Payload:**

```json
{ 
    "systemfile":  
    [  
            "filename": "ns-root.key",  
            "filelocation": "/nsconfig/ssl",  
            "fileaccesstime": "Tue Jan 14 19:27:01 2014",  
            "filemodifiedtime": "Tue Nov  5 17:16:00 2013" 
        },  
        { 
        {  
            "filename": "ns-root.req",  
            "filelocation": "/nsconfig/ssl",  
            "fileaccesstime": "Tue Jan 14 19:27:01 2014",  
            "filemodifiedtime": "Tue Nov  5 17:16:00 2013"  
        } 
    ] 
} 
```

### Retrieving Contents of a Specific File

To retrieve the contents of a file, specify the filename and its directory path in the URL.

**Using REST APIs through HTTP**

For example, to retrieve the contents of the ns-root.key file from the /nsconfig/ssl directory.

**Request**

**HTTP Method:** GET

**URL:** http://&lt;netscaler-ip-address&gt;/nitro/v1/config/systemfile/ns-root.key?args=filelocation:%2Fnsconfig%2Fssl

**Request Header:**

Cookie:NITRO\_AUTH\_TOKEN=\<tokenvalue\>

Accept:application/json

**Response**

**HTTP Status Code on Success:**

200 OK

**HTTP Status Code on Failure:**

4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for 
NetScaler-specific errors). The response payload provides details of the error.

**Response Header:**

Content-Type:application/json

**Response Payload:**

```json
{ 
    "systemfile":  
    [  
        {  
            "filename": "ns-root.key",  
            "filelocation": "/nsconfig/ssl",  
            "filecontent": "LS0tLS1CRUdJTiBSU0EgUFJJVkFU0tLQo=",  
            "fileencoding": "BASE64",  
            "fileaccesstime": "Tue Jan 14 19:27:01 2014",  
            "filemodifiedtime": "Tue Nov  5 17:16:00 2013"  
        }  
    ]  
}
```

### Deleting a File

To delete a file from the NetScaler appliance, specify the filename and the directory path in the URL.

**Using REST APIs through HTTP**

For example, to delete the ns-root.key file from the /nsconfig/ssl directory.

**Request:**

**HTTP Method:** DELETE

**URL:** https://&lt;netscaler-ip-address&gt;/nitro/v1/config/systemfile/ns-root.key?args=filelocation:%2Fnsconfig%2Fssl

**Request Header:**

Cookie:NITRO\_AUTH\_TOKEN=\<tokenvalue\>

**Response**

**HTTP Status Code on Success:** 200 OK

**HTTP Status Code on Failure:** 

4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error.
