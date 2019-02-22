# Before you Begin

This topic covers the prerequisites  and limitations related to using the NITRO APIs.

## Prerequisites
To use NITRO, you must have a basic understanding of the NetScaler appliance and you must make sure that the client application has one of the following:

-  Access to a NetScaler appliance.

-  To use REST APIs through HTTP, you must have a system to generate HTTP or HTTPS requests (payload in JSON format) to the NetScaler appliance. You can use any programming language or tool.

-  For Java clients, you must have a system where Java Development Kit (JDK) 1.5 or later is available. The JDK can be downloaded from http://www.oracle.com/technetwork/java/javase/downloads/index.html.

    The NITRO library (available in &lt;NITRO\_SDK\_HOME&gt;/lib) must be installed on the client path. For installation instructions, read the &lt;NITRO\_SDK\_HOME&gt;/README.txt file.

-  For .NET clients, you must have a system with .NET framework 3.5 or later installed. The .NET framework can be downloaded from http://www.microsoft.com/downloads/en/default.aspx.

    The NITRO library (available in &lt;NITRO\_SDK\_HOME&gt;/lib) must be installed on the client path. For installation instructions, read the &lt;NITRO\_SDK\_HOME&gt;/README.txt file.

-  For Python clients, you must have a system with Python 2.7 or above version.

    The Python SDK is available from NetScaler 10.5 onwards. The NITRO library (available in &lt;NITRO\_SDK\_HOME&gt;/lib) must be installed on the client path. For installation instructions, read the &lt;NITRO\_SDK\_HOME&gt;/README.txt file.

### Obtaining the NITRO SDK Package

The NITRO package is available as a tar file on the Downloads page of the configuration utility of the NetScaler appliance. You must download and untar the file to a folder on your local system. This folder is referred to as \<NITRO_SDK_HOME\> in this documentation.

The folder contains the NITRO libraries in the lib subfolder. The libraries must be added to the client application classpath to access NITRO functionality. The \<NITRO_SDK_HOME\> folder also provides samples and documentation that can help you understand the NITRO SDK.

## Limitations

The section lists the NetScaler operations that cannot be performed by using NITRO API.

**Note:** These operations can be performed on the NetScaler CLI or the GUI.

-  install API and diff API on nsconfig resource
-  UI-internal APIs (update, unset, and get)
-  show ns info
-  shutdown
-  Application firewall API
-  importwsdl
-  importcustom
-  importxmlschema
-  importxmlerrorpage
-  importhtmlerrorpage
-  rmcustom
-  rmxmlschema
-  rmxmlerrorpage
-  rmhtmlerrorpage
-  CLI-specific API
-  start nstrace/stop nstrace/show nstrace
-  scp
-  configaudit
-  show defaults
-  show permission
-  batch
-  source