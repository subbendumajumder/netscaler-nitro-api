#clusterfiles

Configuration for files resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>mode</td><td>&lt;String[]></td><td>Read-write</td><td>The directories and files to be synchronized. The available settings function as follows:<br>Mode Paths<br>all /nsconfig/ssl/<br>/var/netscaler/ssl/<br>/var/vpn/bookmark/<br>/nsconfig/dns/<br>/nsconfig/htmlinjection/<br>/netscaler/htmlinjection/ens/<br>/nsconfig/monitors/<br>/nsconfig/nstemplates/<br>/nsconfig/ssh/<br>/nsconfig/rc.netscaler<br>/nsconfig/resolv.conf<br>/nsconfig/inetd.conf<br>/nsconfig/syslog.conf<br>/nsconfig/snmpd.conf<br>/nsconfig/ntp.conf<br>/nsconfig/httpd.conf<br>/nsconfig/sshd_config<br>/nsconfig/hosts<br>/nsconfig/enckey<br>/var/nslw.bin/etc/krb5.conf<br>/var/nslw.bin/etc/krb5.keytab<br>/var/lib/likewise/db/<br>/var/download/<br>/var/wi/tomcat/webapps/<br>/var/wi/tomcat/conf/Catalina/localhost/<br>/var/wi/java_home/lib/security/cacerts<br>/var/wi/java_home/jre/lib/security/cacerts<br>/var/netscaler/locdb/<br>ssl /nsconfig/ssl/<br>/var/netscaler/ssl/<br>bookmarks /var/vpn/bookmark/<br>dns /nsconfig/dns/<br>htmlinjection /nsconfig/htmlinjection/<br>imports /var/download/<br>misc /nsconfig/license/<br>/nsconfig/rc.conf<br>all_plus_misc Includes *all* files and /nsconfig/license/ and /nsconfig/rc.conf.<br>Default value: all.<br>Possible values = all, bookmarks, ssl, htmlinjection, imports, misc, dns, krb, all_plus_misc, all_minus_misc</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[SYNC]()


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###sync



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/clusterfiles?<b>action=sync</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"clusterfiles":{"mode":<String[]_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


