# Before you Begin
This section covers the prerequisites for using the NITRO APIs, NITRO changes across releases, and limitations.

## Prerequisites
To use NITRO, you must have a basic understanding of the NetScaler appliance and you must make sure that the client application has one of the following:

* Access to a NetScaler appliance.

* To use REST APIs through HTTP, you must have a system to generate HTTP or HTTPS requests (payload in JSON format) to the NetScaler appliance. You can use any programming language or tool.

* For Java clients, you must have a system where Java Development Kit (JDK) 1.5 or later is available. The JDK can be downloaded from http://www.oracle.com/technetwork/java/javase/downloads/index.html.
    
    The NITRO library (available in &lt;NITRO\_SDK\_HOME&gt;/lib) must be installed on the client path. For installation instructions, read the &lt;NITRO\_SDK\_HOME&gt;/README.txt file.

* For .NET clients, you must have a system with .NET framework 3.5 or later installed. The .NET framework can be downloaded from http://www.microsoft.com/downloads/en/default.aspx. 

    The NITRO library (available in &lt;NITRO\_SDK\_HOME&gt;/lib) must be installed on the client path. For installation instructions, read the &lt;NITRO\_SDK\_HOME&gt;/README.txt file.

* For Python clients, you must have a system with Python 2.7 or above version.

    The Python SDK is available from NetScaler 10.5 onwards. The NITRO library (available in &lt;NITRO\_SDK\_HOME&gt;/lib) must be installed on the client path. For installation instructions, read the &lt;NITRO\_SDK\_HOME&gt;/README.txt file.

**Obtaining the NITRO SDK Package**

The NITRO package is available as a tar file on the Downloads page of the configuration utility of the NetScaler appliance. You must download and untar the file to a folder on your local system. This folder is referred to as \<NITRO_SDK_HOME\> in this documentation.

The folder contains the NITRO libraries in the lib subfolder. The libraries must be added to the client application classpath to access NITRO functionality. The \<NITRO_SDK_HOME\> folder also provides samples and documentation that can help you understand the NITRO SDK.

## NITRO Changes Across Releases

Some NITRO API have changed across releases. This topic details information which can help you avoid compatibility issues in your application. The changes are categorized as:

### Changes Made from 11.1-53.3 -> 12.0-48.x

**Changes across NITRO flavors**

The NITRO changes that were made in NetScaler 12.0-48.x when compared with NetScaler 11.1-53.3.

<table border=1>
<thead>
<tr>
<td>
<p><strong>Type of change</strong></p>
</td>
<td>
<p><strong>Resource</strong></p>
</td>
<td>
<p><strong>Method</strong></p>
</td>
<td>
<p><strong>Attribute</strong></p>
</td>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Resource removed</p>
</td>
<td>
<p>vpath, vpathparam</p>
</td>
<td>
<p>ALL</p>
</td>
<td>
<p>All resources and parameters related to vpath feature. </p>
</td>
</tr>
<tr>
<td>
<p>Attribute removed </p>
</td>
<td>
<p>l3param </p>
</td>
<td>
<p>-</p>
</td>
<td>
<p>Icmperrgenerate</p>
<p>This attribute is related to vpath for which the support is removed in 12.0.&nbsp;</p>
</td>
</tr>
<tr>
<td>
<p>Attribute removed </p>
</td>
<td>
<p>qos_stats </p>
</td>
<td>
<p>-</p>
</td>
<td>
<p>ipcpe2qosfailedrate</p>
<p></p>
<p><strong>Note</strong>: Some of the counters under this resource are removed. For new definitions, see&nbsp;<a href="http://docs.citrix.com/en-us/netscaler/12/nitro-api/nitro-rest/api-reference/statistics/qos/qos.html">http://docs.citrix.com/en-us/netscaler/12/nitro-api/nitro-rest/api-reference/statistics/qos/qos.html</a>&nbsp;</p>
</td>
</tr>
<tr>
<td>
<p>Attribute removed </p>
</td>
<td>
<p>vrid_interface_binding</p>
</td>
<td>
<p>-</p>
</td>
<td>
<p>trackifnum</p>
<p>New resources (vrid_trackifnum_binding and vrid6_trackifnum_binding) are introduced to deal with track interfaces. </p>
</td>
</tr>
<tr>
<td>
<p>Attribute removed </p>
</td>
<td>
<p>vrid_interface_binding </p>
</td>
<td>
<p>-</p>
</td>
<td>
<p>ifaces is replaced with ifnum.</p>
<p>Previously, ifaces parameter was used in the response and ifnum was used in the input. Now both POST and GET are consistent and use the same attribute name. </p>
</td>
</tr>
<tr>
<td>
<p>Attribute removed </p>
</td>
<td>
<p>sslprofile_sslciphersuite_binding </p>
</td>
<td>
<p>-</p>
</td>
<td>
<p>cipheraliasname</p>
<p>cipheraliasname is a redundant parameter. The required information is provided by ciphername parameter.</p>
</td>
</tr>
<tr>
<td>
<p>Attribute removed </p>
</td>
<td>
<p>nslicense </p>
</td>
<td>
<p>-</p>
</td>
<td>
<p>Ispooledlicensing</p>
<p>Ispooledlicensing Is replaced with a new parameter licensingmode which returns if the license of "Local"/"Pooled"/"CICO" type.</p>
</td>
</tr>
<tr>
<td>
<p>Attribute removed </p>
</td>
<td>
<p>lbmonitor_sslcertkey_binding </p>
</td>
<td>
<p>DELETE</p>
</td>
<td>
<p>crlcheck </p>
</td>
</tr>
</tbody>
</table>

**Changes specific to NITRO SDKs**

The SDK-specific changes that were made in NetScaler 12.0-48.x when compared with NetScaler 11.1-53.3.

<table border=1>
<thead>
<tr>
<td>
<p><strong>Type of change</strong></p>
</td>
<td>
<p><strong>Class</strong></p>
</td>
<td>
<p><strong>Method/Attribute</strong></p>
</td>
<td>
<p><strong>Remarks</strong></p>
</td>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Attribute type changed&nbsp;</p>
</td>
<td>
<p>pcpmap</p>
</td>
<td>
<p>pcpprotocol</p>
</td>
<td>
<p>Datatype changed from double to string.</p>
</td>
</tr>
<tr>
<td>
<p>Class removed </p>
</td>
<td>
<p>mediaclassification_stats</p>
</td>
<td>
<p>-</p>
</td>
<td>
<p>-</p>
</td>
</tr>
<tr>
<td>
<p>Method removed </p>
</td>
<td>
<p>vxlan_iptunnel_binding </p>
</td>
<td>
<p>add(vxlan_iptunnel_binding obj, nitro_service session)</p>
<p>delete(vxlan_iptunnel_binding obj, nitro_service session)</p>
</td>
<td>
<p>Feature is deprecated, use bridgetable with broadcast mac option. </p>
</td>
</tr>
<tr>
<td>
<p>Method removed </p>
</td>
<td>
<p>inatsession_stats </p>
</td>
<td>
<p>get(inatsession obj, nitro_service session)</p>
</td>
<td>
<p>-</p>
</td>
</tr>
</tbody>
</table>


## Changes Made from 10.5 57.x -> 11.0

**All NITRO Flavors - Changes from 10.5 57.x to 11.0**

The NITRO changes that were made in NetScaler 11.0 when compared with NetScaler 10.5 Build 57.x.

<table border=1>
<thead>
<tr>
<td>
<p><strong>Type of Change</strong></p>
</td>
<td>
<p><strong>Resource</strong></p>
</td>
<td>
<p><strong>Attribute</strong></p>
</td>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Attribute removed</p>
</td>
<td>
<p>nstrace</p>
</td>
<td>
<p>doruntimemerge</p>
</td>
</tr>
<tr>
<td>
<p>Attribute removed</p>
</td>
<td>
<p>nstrace</p>
</td>
<td>
<p>tcpdump</p>
</td>
</tr>
<tr>
<td>
<p>Attribute removed</p>
</td>
<td>
<p>cacheobject</p>
</td>
<td>
<p>force</p>
</td>
</tr>
</tbody>
</table>

**NITRO SDKs - Changes from 10.5 57.x to 11.0**

The SDK-specific changes that were made in NetScaler 11.0 when compared with NetScaler 10.5 Build 57.x.

<table border=1>
<thead>
<tr>
<td>
<p><strong>Type of Change</strong></p>
</td>
<td>
<p><strong>Class</strong></p>
</td>
<td>
<p><strong>Method</strong></p>
</td>
<td>
<p><strong>Replace with</strong></p>
</td>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Attribute missing in method</p>
</td>
<td>
<p>cacheobject</p>
</td>
<td>
<p>(base_response) flush(cacheobject obj, nitro_service session)</p>
<p>'force' attribute missing in this method.</p>
</td>
<td>
<p>-</p>
</td>
</tr>
<tr>
<td>
<p>Method missing</p>
</td>
<td>
<p>clustersync</p>
</td>
<td>
<p>(base_response) Force(clustersync obj, nitro_service session)</p>
</td>
<td>
<p>(base_response) Force(nitro_service session)</p>
</td>
</tr>
<tr>
<td>
<p>Method missing</p>
</td>
<td>
<p>shutdown</p>
</td>
<td>
<p>(base_response) Shutdown(shutdown obj, nitro_service session)</p>
</td>
<td>
<p>(base_response) Shutdown(nitro_service session)</p>
</td>
</tr>
<tr>
<td>
<p>Method missing</p>
</td>
<td>
<p>systemfile</p>
</td>
<td>
<p>(systemfile) get(systemfile obj, nitro_service session)</p>
</td>
<td>
<p>-</p>
</td>
</tr>
<tr>
<td>
<p>Method missing</p>
</td>
<td>
<p>sslfips</p>
</td>
<td>
<p>(base_response) reset(sslfips obj, nitro_service session)</p>
</td>
<td>
<p>(base_response) reset(nitro_service session)</p>
</td>
</tr>
</tbody>
</table>

### Changes made from 9.3 -> 10.1/10.5

**Note.** No changes are introduced from NetScaler 10.1 to NetScaler 10.5. Therefore, you should not face any compatibility issues when migrating from NetScaler 10.1 to 10.5.


**All NITRO Flavors - Changes from 9.3 to 10.1/10.5**

The NITRO changes that were made in NetScaler 10.1/10.5 when compared with NetScaler 9.3.

<table border=1>
<thead>
<tr>
<td>
<p><strong>Type of Change</strong></p>
</td>
<td>
<p><strong>Resource</strong></p>
</td>
<td>
<p><strong>Method</strong></p>
</td>
<td>
<p><strong>Attribute</strong></p>
</td>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Resource removed</p>
</td>
<td>
<p>lbmonitor_lbmetrictable_binding</p>
<p>Replaced with the resource 'lbmonitor_metric_binding'.</p>
</td>
<td>
<p>-</p>
</td>
<td>
<p>-</p>
</td>
</tr>
<tr>
<td>
<p>Method removed</p>
</td>
<td>
<p>vserver</p>
</td>
<td>
<p>GET</p>
<p>Perform the GET operation on specific virtual server types such as lb/cr/cs.</p>
</td>
<td>
<p>-</p>
</td>
</tr>
<tr>
<td>
<p>Method removed</p>
</td>
<td>
<p>filterpolicy</p>
</td>
<td>
<p>POST with 'action=unset'</p>
<p>This method is removed as unsetting the attributes('action') of a policy makes it invalid.</p>
</td>
<td>
<p>-</p>
</td>
</tr>
<tr>
<td>
<p>Method removed</p>
</td>
<td>
<p>auditsyslogpolicy</p>
</td>
<td>
<p>POST with 'action=unset'</p>
<p>This method is removed as unsetting the attributes('action') of a policy makes it invalid.</p>
</td>
<td>
<p>-</p>
</td>
</tr>
<tr>
<td>
<p>Method removed</p>
</td>
<td>
<p>auditnslogpolicy</p>
</td>
<td>
<p>POST with 'action=unset'</p>
<p>This method is removed as unsetting the attributes('action') of a policy makes it invalid.</p>
</td>
<td>
<p>-</p>
</td>
</tr>
<tr>
<td>
<p>Method removed</p>
</td>
<td>
<p>authorizationpolicy</p>
</td>
<td>
<p>POST with 'action=unset'</p>
<p>This method is removed as unsetting the attributes('action') of a policy makes it invalid.</p>
</td>
<td>
<p>-</p>
</td>
</tr>
<tr>
<td>
<p>Return-type changed</p>
</td>
<td>
<p>snmpengineid</p>
</td>
<td>
<p>GET</p>
<p>Return type changed to an array.</p>
</td>
<td>
<p>-</p>
</td>
</tr>
<tr>
<td>
<p>Return-type changed</p>
</td>
<td>
<p>nshostname</p>
</td>
<td>
<p>GET</p>
<p>Return type changed to an array.</p>
</td>
<td>
<p>-</p>
</td>
</tr>
<tr>
<td>
<p>Attribute-type changed</p>
</td>
<td>
<p>appfwpolicy_lbvserver_binding</p>
</td>
<td>
<p>-</p>
</td>
<td>
<p>activepolicy</p>
<p>Data type changed from Boolean to Integer.</p>
</td>
</tr>
<tr>
<td>
<p>Attribute-type changed</p>
</td>
<td>
<p>appfwpolicy_appfwglobal_binding</p>
</td>
<td>
<p>-</p>
</td>
<td>
<p>activepolicy</p>
<p>Data type changed from Boolean to Integer.</p>
</td>
</tr>
<tr>
<td>
<p>Attribute-type changed</p>
</td>
<td>
<p>vlan</p>
</td>
<td>
<p>-</p>
</td>
<td>
<p>portbitmap</p>
<p>Data type changed from uint to ulong.</p>
</td>
</tr>
<tr>
<td>
<p>Attribute-type changed</p>
</td>
<td>
<p>vlan</p>
</td>
<td>
<p>-</p>
</td>
<td>
<p>tagbitmap</p>
<p>Data type changed from uint to ulong.</p>
</td>
</tr>
<tr>
<td>
<p>Attribute removed</p>
</td>
<td>
<p>policypatset_pattern_binding</p>
</td>
<td>
<p>-</p>
</td>
<td>
<p>indextype</p>
<p>This attribute is moved to 'policypatset' resource as this attribute is applicable at patset level.</p>
</td>
</tr>
<tr>
<td>
<p>Attribute removed</p>
</td>
<td>
<p>system_stats</p>
</td>
<td>
<p>-</p>
</td>
<td>
<p>powersupply1failure</p>
<p>Replaced with 'powersupply1status'.</p>
<p>Note:&nbsp;Change is applicable from NetScaler 9.3 Build 65.8.</p>
</td>
</tr>
<tr>
<td>
<p>Attribute removed</p>
</td>
<td>
<p>system_stats</p>
</td>
<td>
<p>-</p>
</td>
<td>
<p>powersupply2failure</p>
<p>Replaced with 'powersupply2status'.</p>
<p>Note:&nbsp;Change is applicable from NetScaler 9.3 Build 65.8.</p>
</td>
</tr>
<tr>
<td>
<p>Attribute removed</p>
</td>
<td>
<p>server_servicegroup_binding</p>
</td>
<td>
<p>-</p>
</td>
<td>
<p>servicetype</p>
<p>Replaced with 'svctype'.</p>
</td>
</tr>
<tr>
<td>
<p>Attribute removed</p>
</td>
<td>
<p>server_service_binding</p>
</td>
<td>
<p>-</p>
</td>
<td>
<p>servicetype</p>
<p>Replaced with 'svctype'.</p>
</td>
</tr>
<tr>
<td>
<p>Attribute removed</p>
</td>
<td>
<p>crvserver</p>
</td>
<td>
<p>-</p>
</td>
<td>
<p>hits</p>
<p>Hits are calculated per policy binding hence moved this parameter to binding resources.</p>
</td>
</tr>
<tr>
<td>
<p>Attribute removed</p>
</td>
<td>
<p>crvserver</p>
</td>
<td>
<p>-</p>
</td>
<td>
<p>dstvsvr</p>
<p>Replaced with 'destinationvserver'.</p>
</td>
</tr>
<tr>
<td>
<p>Attribute removed</p>
</td>
<td>
<p>crvserver</p>
</td>
<td>
<p>-</p>
</td>
<td>
<p>destvserver</p>
<p>Replaced with 'domain'.</p>
</td>
</tr>
<tr>
<td>
<p>Attribute removed</p>
</td>
<td>
<p>crvserver</p>
</td>
<td>
<p>-</p>
</td>
<td>
<p>dnsvserver</p>
<p>Replaced with 'dnsvservername'.</p>
</td>
</tr>
<tr>
<td>
<p>Attribute removed</p>
</td>
<td>
<p>appflowpolicylabel</p>
</td>
<td>
<p>-</p>
</td>
<td>
<p>type</p>
<p>Replaced with 'policylabeltype'.</p>
</td>
</tr>
<tr>
<td>
<p>Attribute removed</p>
</td>
<td>
<p>sslcipher</p>
</td>
<td>
<p>-</p>
</td>
<td>
<p>ciphgrpals</p>
<p>Replaced with 'ciphergroupname'.</p>
</td>
</tr>
<tr>
<td>
<p>Attribute removed</p>
</td>
<td>
<p>csvserver_cspolicy_binding</p>
</td>
<td>
<p>-</p>
</td>
<td>
<p>targetvserver</p>
<p>Replaced with 'targetlbvserver'.</p>
<p>Note:&nbsp;This change is applicable for the 'sslcipher_*_binding' resources also.</p>
</td>
</tr>
<tr>
<td>
<p>Attribute removed</p>
</td>
<td>
<p>csvserver_cspolicy_binding</p>
</td>
<td>
<p>-</p>
</td>
<td>
<p>targetvserver</p>
<p>Replaced with 'targetlbvserver'.</p>
</td>
</tr>
<tr>
<td>
<p>Attribute removed</p>
</td>
<td>
<p>rewriteaction</p>
</td>
<td>
<p>-</p>
</td>
<td>
<p>allow_unsafe_pi1, allow_unsafe_pi</p>
<p>Replaced with 'bypassSafetyCheck'.</p>
</td>
</tr>
<tr>
<td>
<p>Attribute removed</p>
</td>
<td>
<p>nsconfig</p>
</td>
<td>
<p>-</p>
</td>
<td>
<p>nwfwmode</p>
<p>Marked as a hidden attribute.</p>
</td>
</tr>
</tbody>
</table>

**NITRO SDKs - Changes from 9.3 to 10.1/10.5**

The SDK-specific changes that were made in NetScaler 10.1/10.5 when compared with NetScaler 9.3.

<table border=1>
<thead>
<tr>
<td>
<p><strong>Type of Change</strong></p>
</td>
<td>
<p><strong>Class</strong></p>
</td>
<td>
<p><strong>Method</strong></p>
</td>
<td>
<p><strong>Replace with</strong></p>
</td>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Class removed</p>
</td>
<td>
<p>Routerbgp</p>
</td>
<td>
<p>-</p>
</td>
<td>
<p>This class is removed as all router configurations are deprecated in 9.2.</p>
</td>
</tr>
<tr>
<td>
<p>Method signature changed</p>
</td>
<td>
<p>dnsptrrec</p>
</td>
<td>
<p>get(dnsptrrec obj, nitro_service session)</p>
</td>
<td>
<p>get(nitro_service session, String reversedomain)</p>
</td>
</tr>
<tr>
<td>
<p>Method signature changed</p>
</td>
<td>
<p>dnsaddrec</p>
</td>
<td>
<p>get(dnsaddrec obj, nitro_service session)</p>
</td>
<td>
<p>get(nitro_service session, String hostname)</p>
</td>
</tr>
<tr>
<td>
<p>Method signature changed</p>
</td>
<td>
<p>dnsnsrec</p>
</td>
<td>
<p>get(dnsnsrec obj, nitro_service session)</p>
</td>
<td>
<p>get(nitro_service session, String domain)</p>
</td>
</tr>
<tr>
<td>
<p>Method signature changed</p>
</td>
<td>
<p>snmpengineid</p>
</td>
<td>
<p>unset(nitro_service session, String[] args)</p>
</td>
<td>
<p>unset(nitro_service session, snmpengineid resource, String[] args)</p>
</td>
</tr>
<tr>
<td>
<p>Method signature changed</p>
</td>
<td>
<p>arp</p>
</td>
<td>
<p>arp.get(nitro_service session, String ipaddress)</p>
</td>
<td>
<p>arp.get(nitro_service session, arp resource)</p>
</td>
</tr>
<tr>
<td>
<p>Method signature changed</p>
</td>
<td>
<p>nsip</p>
</td>
<td>
<p>get(nitro_service session, String ipaddress)</p>
</td>
<td>
<p>get(nitro_service client, nsip resource)</p>
</td>
</tr>
<tr>
<td>
<p>Method signature changed</p>
</td>
<td>
<p>nsip6</p>
</td>
<td>
<p>get(nitro_service session, String ipv6address)</p>
</td>
<td>
<p>get(nitro_service session, nsip6 resource)</p>
</td>
</tr>
<tr>
<td>
<p>Method signature changed</p>
</td>
<td>
<p>dnsmxrec</p>
</td>
<td>
<p>dnsmxrec.get(dnsmxrec obj, nitro_service session)</p>
</td>
<td>
<p>dnsmxrec[] get(nitro_service service, dnsmxrec_args args)</p>
</td>
</tr>
<tr>
<td>
<p>Method Missing</p>
</td>
<td>
<p>authenticationnegotiatepolicy</p>
</td>
<td>
<p>(base_response) unset(nitro_service session, String[] args, String name)' is missing in&nbsp;</p>
</td>
<td>
<p>-</p>
</td>
</tr>
<tr>
<td>
<p>Method missing</p>
</td>
<td>
<p>authenticationnegotiatepolicy</p>
</td>
<td>
<p>(base_response) unset(authenticationnegotiatepolicy obj, nitro_service session, String[] args)</p>
</td>
<td>
<p>-</p>
</td>
</tr>
<tr>
<td>
<p>Attribute missing in method</p>
</td>
<td>
<p>nsconfig</p>
</td>
<td>
<p>(base_response) update(nsconfig obj, nitro_service session)</p>
<p>'nwfwmode' attribute is missing in this method.</p>
</td>
<td>
<p>-</p>
</td>
</tr>
</tbody>
</table>

###  Limitations

The section lists the NetScaler operations that cannot be performed by using NITRO API.

**Note:** These operations can be performed on the NetScaler CLI or the GUI.

* install API (supported from NetScaler 11.1 onwards)
diff API on nsconfig resource (supported from NetScaler 10.5 onwards)
* UI-internal APIs (update, unset, and get)
* show ns info
* shutdown
* Application firewall API
* importwsdl
* importcustom
* importxmlschema
* importxmlerrorpage
* importhtmlerrorpage
* rmcustom
* rmxmlschema
* rmxmlerrorpage
* rmhtmlerrorpage
* CLI-specific API
* start nstrace/stop nstrace/show nstrace
* scp
* configaudit
* show defaults
* show permission
* batch
* source