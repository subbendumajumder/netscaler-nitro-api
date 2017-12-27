# Performing Basic NetScaler Operations
This section covers procedures for performing the following basic NetScaler operations using NITRO APIs.

* Connecting to the NetScaler Appliance
* Enabling NetScaler Features and Modes
* Saving NetScaler Configurations
* Killing a System Session
* Disconnecting from the NetScaler Appliance

## Connecting to the NetScaler Appliance
The first step towards using NITRO is to establish a session with the NetScaler appliance and then authenticate the session by using the NetScaler administrator's credentials.

Some points to note with regards to session timeout for NetScaler 10.5 and later versions:

* When restricted timeout param is enabled, NITRO, by default, uses the timeout value that is configured for the logged in user. You can customize this value but it must be limited to the value specified for the user. If no value is specified for the user, the default timeout value of 15 minutes is used.
* When restricted timeout param is not enabled, NITRO uses the default value of 30 minutes as session timeout.

**Using REST APIs through HTTP**

You must specify the username and password in the login object. The session ID that is created must be specified in the request header of all further operations in the session.

**Note.**

* You must have a user account on the appliance to log on to it. The configuration operations that you can perform are limited by the administrative roles assigned to your account.
* To ensure secure communication, use the HTTPS protocol in NITRO requests.
* Instead of creating a NITRO session, you can log on to the NetScaler appliance while performing individual operations. To do this, you must specify the username and password in the request header of the NITRO request as follows:
    * X-NITRO-USER:&lt;username\>
    * X-NITRO-PASS:&lt;password\> 
    * Content-Type:application/json

For example, to connect and create a session with a NetScaler appliance with NSIP address 10.102.29.60 by using the HTTP protocol:

**Request**

**HTTP Method:** POST
    
**URL:** http://10.102.29.60/nitro/v1/config/login
    
**Request Headers:** Content-Type:application/json
    
**Request Payload:**
    
```json  
{ 
    "login": 
    { 
    "username":"admin", 
    "password":"verysecret"     
    } 
}     
```    

**Response**

**HTTP Status Code on Success:** 201 Created

**HTTP Status Code on Failure:** 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error.

**Response Header:**
   
```json
Set-Cookie:NITRO\_AUTH\_TOKEN=<tokenvalue>;  
path=/nitro/v1   
```    

**Using REST APIs through SDKs**

You must create an object of the com.citrix.netscaler.nitro.service.nitro_service class by specifying the NetScaler IP (NSIP) address and the protocol to connect to the appliance (HTTP or HTTPS). You then use this object and log on to the appliance by specifying the user name and the password of the NetScaler administrator.

**Note:**

* For the python SDK, the package path is of the form nssrc.com.citrix.netscaler...
* You must have a user account on that appliance. The configuration operations that you perform are limited by the administrative roles assigned to your account.

The following sample code establishes a session with a NetScaler appliance with IP address 10.102.29.60 by using the HTTPS protocol and also sets a session timeout period (in seconds) of 60 minutes.

**Java - Sample code to establish session**

```java
//Specify the NetScaler appliance IP address and protocol
nitro_service ns_session = new nitro_service("10.102.29.60","https");

//Specify the login credentials
ns_session.login("admin","verysecret",3600);
```

**.NET - Sample code to establish session**

```csharp
//Specify the NetScaler appliance IP address and protocol
nitro_service ns_session = new nitro_service("10.102.29.60","https");

//Specify the login credentials
ns_session.login("admin","verysecret",3600);
```

**Python - Sample code to establish session**

```python
#Specify the NetScaler appliance IP address and protocol
ns_session = nitro_service("10.102.29.60","https")

#Specify the login credentials
ns_session.login("admin","verysecret",3600)
```

### Disable SSL Checks

When using HTTPS, you must make sure that the root CA is added to the truststore. By default, NITRO validates the SSL certificate and verifies the hostname. 

**Using REST APIs through SDKs**

Disable these validations as shown in the following sample codes.

**Java - Sample code for disabling SSL checks**

```java
ns_session.set_certvalidation(false); 
ns_session.set_hostnameverification(false);
```

**.NET - Sample code for disabling SSL checks**

```csharp
ns_session.certvalidation = false; 
ns_session.hostnameverification = false;
```

**Python - Sample code for disabling SSL checks**

```python
ns_session.certvalidation = false 
ns_session.hostnameverification = false
```

## Enabling NetScaler Features and Modes

Some NetScaler features and modes are disabled by default and therefore must be enabled before they can be configured. To enable a NetScaler feature or mode, specify the action as "enable" in the URL query string, and in the request payload, specify the feature or mode to be enabled.

**Using REST APIs through HTTP**

To disable a feature or mode, in the URL query string, specify the action as "disable".

For example, to enable the load balancing and content switching features:

**Request**

**HTTP Method:** POST

**URL:** http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsfeature?action=enable

**Request Headers:**

Cookie:NITRO\_AUTH\_TOKEN=&lt;tokenvalue&gt; 

Content-Type:application/json    

**Request Payload:**

```json
{ 
    "nsfeature":  
    { 
        "feature":  
        [ 
            "LB", 
            "CS" 
        ] 
    } 
}
```

**Response**

**HTTP Status Code on Success:** 200 OK

**HTTP Status Code on Failure:** 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error.

To enable the L2 and fast ramp modes:

**Request**

**HTTP Method:** POST

**URL:** http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsmode?action=enable

**Request Headers:**

Cookie:NITRO\_AUTH\_TOKEN=&lt;tokenvalue&gt; 

Content-Type:application/json

**Request Payload:**

```json
{ 
    "nsmode": 
    { 
        "mode": 
        [ 
            "L2", 
            "FR" 
        ] 
    } 
}
```

**Response**

**HTTP Status Code on Success:** 200 OK

**HTTP Status Code on Failure:** 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error.
    
## Saving NetScaler Configurations
To make sure that the configurations persist on rebooting the appliance, you must save the NetScaler configurations. To save the configurations, specify the action as "save" in the URL query string.

**Using REST APIs through HTTP**

To save the configurations:

**Request**

**HTTP Method:** POST

**URL:** http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsconfig?action=save

**Request Headers:**

Cookie:NITRO\_AUTH\_TOKEN=&lt;tokenvalue&gt; 

Content-Type:application/json

**Request Payload:**

```json
{ 
    "nsconfig": 
    {} 
}
```

**Response**

**HTTP Status Code on Success:** 200 OK

**HTTP Status Code on Failure:** 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error.

## Killing a System Session

A NetScaler administrator can kill any system session by specifying the action as "kill" in the URL query string and by specifying the required system session ID in the request payload.

**Using REST APIs through HTTP**

For example, to kill a system session that has ID as 311:

**Request**

**HTTP Method:** POST

**URL:** http://&lt;netscaler-ip-address&gt;/nitro/v1/config/systemsession?action=kill

**Request Headers:**

Cookie:NITRO\_AUTH\_TOKEN=&lt;tokenvalue&gt; 

Content-Type:application/json

**Request Payload:**

```json
{ 
    "systemsession": 
    { 
    "sid":"311" 
    } 
}
```

**Response**

**HTTP Status Code on Success:** 200 OK

**HTTP Status Code on Failure:** 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error. 
    
## Disconnecting from the NetScaler Appliance

Before disconnecting (logging out) from the NetScaler appliance, make sure that you have saved the NetScaler configurations.

**Using REST APIs through HTTP**

To logout of the NetScaler appliance:

**Request**

**HTTP Method:** POST

**URL:** http://&lt;netscaler-ip-address&gt;/nitro/v1/config/logout

**Request Headers:**

Cookie:NITRO\_AUTH\_TOKEN=&lt;tokenvalue&gt; 

Content-Type:application/json

**Request Payload:**

```json
{ 
    "logout":{} 
}
```

**Response**

**HTTP Status Code on Success:** 200 OK

**HTTP Status Code on Failure:** 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error.
    

