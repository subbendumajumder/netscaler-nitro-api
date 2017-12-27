# Citrix NetScaler 12.0 REST APIs - NITRO
The NetScaler NITRO protocol allows you to configure and monitor the NetScaler appliance programmatically by using Representational State Transfer (REST) interfaces. Therefore, NITRO applications can be developed in any programming language. Additionally, for applications that must be developed in Java or .NET or Python, NITRO APIs are exposed through relevant libraries that are packaged as separate Software Development Kits (SDKs).

**How NITRO Works**

The NITRO infrastructure consists of a client application and the NITRO Web service running on a NetScaler appliance. The communication between the client application and the NITRO web service is based on REST architecture using HTTP or HTTPS.

A NITRO request is executed as follows:

1. The client application sends REST request message to the NITRO web service. When using the SDKs, an API call is translated into the appropriate REST request message.
2. The web service processes the REST request message.
3. The NITRO web service returns the corresponding REST response message to the client application. When using the SDKs, the REST response message is translated into the appropriate response for the API call.

To minimize traffic on the NetScaler network, you retrieve the whole state of a resource from the server, make modifications to the state of the resource locally, and then upload it back to the server in one network transaction. For example, to update a load balancing virtual server, you must retrieve the object, update the properties, and then upload the changed object in a single transaction.

**Note.** Local operations on a resource (changing its properties) do not affect its state on the server until the state of the object is explicitly uploaded.

NITRO APIs are synchronous in nature. This means that the client application waits for a response from the NITRO web service before executing another NITRO API.

**REST Web Services**

REST (REpresentational State Transfer) is an architectural style based on simple HTTP requests and responses between the client and the server. REST is used to query or change the state of objects on the server side. In REST, the server side is modeled as a set of entities where each entity is identified by a unique URL.

The general format for NITRO URLs is as follows:

* For configurations. http://&lt;netscaler-ip-address&gt;/nitro/v1/config/&lt;resource-type&gt;

* For retrieving statistics. http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/&lt;resource-type&gt;

For example, for a load balancing virtual server, &lt;resource-type&gt; can be replaced by lbvserver.

Some points to remember:

* In addition to the CRUD operations (Create, Read, Update, and Delete), resources (such as lbvserver) can support other operations or actions. These operations use the HTTP POST method, with the URL specifying the operation to be performed and the request body specifying the parameters for that operation.
* All NITRO operations are logged in the /var/log/nitro.log file on the NetScaler appliance.

For more information on the REST objects and the usage, see the documentation provided in the &lt;NITRO\_SDK\_HOME&gt;/index.html file.