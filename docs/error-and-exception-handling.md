# Error and Exception Handling
This section covers error handling support for NITRO APIs and exception handling support for SDKs.

## Error Handling for NITRO APIs

In case of a failed request, NITRO provides the required information through the HTTP status code and in the response header and response payload.
* Error in a Single Resource Operation
* Error in a Bulk Operations
* Warnings

**Error in a Single Resource Operation**

The response of a single erroneous operation is as follows:

**Response**

**HTTP Status Code:** 4xx \<string\> (for general HTTP errors) or 5xx \<string\> (for NetScaler-specific errors)

**Response Header:** Content-Type:application/json

**Response Payload:**

```json
{ 
    errorcode: <Error code>, 
    message: "<Error message>", 
    severity: "ERROR" 
}
```

**Error in a Bulk Operation**

When there is a failure in one of the bulk operations, the response payload gives a combination of success and failure (depends on the value set for X-NITRO-ONERROR in the request header).

**Response**

**HTTP Status Code:** 207 Multi Status

**Response Header:** Content-Type:application/json

**Response Payload when X-NITRO-ONERROR is set to continue:**

When the first operation fails, the request is not terminated. The response payload shows the error details of the failed operation and the success status of the other operations.


```json
{ 
    "errorcode": 1243, 
    "message": "Bulk operation failed", 
    "severity": "ERROR", 
    "response": 
    [ 
        { 
            "errorcode": 273, 
            "message": "Resource already exists", 
            "severity": "ERROR" 
        }, 
        { 
            "errorcode": 0, 
            "message": "Done", 
            "severity": "NONE" 
        } 
    ] 
}
```

**Response Payload when X-NITRO-ONERROR is set to exit:**

When the first operation fails, the request is terminated. The response payload only shows the error details of the failed operation.

```json
{ 
    "errorcode": 1243, 
    "message": "Bulk operation failed", 
    "severity": "ERROR", 
    "response": 
    [ 
        { 
            "errorcode": 273, 
            "message": "Resource already exists", 
            "severity": "ERROR" 
        } 
    ] 
}
```

**Warnings in NITRO Operations**

Warnings can be captured by specifying the "warning" query parameter as "yes" when performing any NITRO operation. For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:

http://&lt;netscaler-ip-address&gt;/nitro/v1/config/llbvserver?warning=yes

If there are any warnings, the response is as follows:

**Response**

**HTTP Status Code:** 209 X-NITRO-WARNING

**Response Header:** X-NITRO-WARNING →1067 - Feature(s) not enabled [LB]

## Exception Handling Support for SDKs

The status of a NITRO request is captured in the com.citrix.netscaler.nitro.exception.nitro_exception class. This class provides the following details of the exception:

* **Session ID**. The session in which the exception occurred.
* **Severity**. The severity of the exception: error or warning. By default, only errors are captured. To capture warnings, you must set the warning flag to true, while connecting to the appliance.
* **Error code**. The status of the NITRO request. An error code of 0 indicates that the NITRO request is successful. A non-zero error code indicates an error in processing the NITRO request.
* **Error message**. Provides a brief description of the exception.

For a list of error codes, see the errorlisting.html file available in the \<NITRO\_SDK\_HOME\>/doc/api\_reference folder.
