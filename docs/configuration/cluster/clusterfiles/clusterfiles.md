#clusterfiles

Configuration for files resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>mode</td><td>&lt;String[]></td><td>Read-write</td><td>The directories and files to be synchronized. The available settings function as follows:&lt;br> Mode Paths&lt;br> all /nsconfig/ssl/&lt;br> /var/netscaler/ssl/&lt;br> /var/vpn/bookmark/&lt;br> /nsconfig/dns/&lt;br> /nsconfig/htmlinjection/&lt;br> /netscaler/htmlinjection/ens/&lt;br> /nsconfig/monitors/&lt;br> /nsconfig/nstemplates/&lt;br> /nsconfig/ssh/&lt;br> /nsconfig/rc.netscaler&lt;br> /nsconfig/resolv.conf&lt;br> /nsconfig/inetd.conf&lt;br> /nsconfig/syslog.conf&lt;br> /nsconfig/snmpd.conf&lt;br> /nsconfig/ntp.conf&lt;br> /nsconfig/httpd.conf&lt;br> /nsconfig/sshd_config&lt;br> /nsconfig/hosts&lt;br> /nsconfig/enckey&lt;br> /var/nslw.bin/etc/krb5.conf&lt;br> /var/nslw.bin/etc/krb5.keytab&lt;br> /var/lib/likewise/db/&lt;br> /var/download/&lt;br> /var/wi/tomcat/webapps/&lt;br> /var/wi/tomcat/conf/Catalina/localhost/&lt;br> /var/wi/java_home/lib/security/cacerts&lt;br> /var/wi/java_home/jre/lib/security/cacerts&lt;br> /var/netscaler/locdb/&lt;br>ssl /nsconfig/ssl/&lt;br> /var/netscaler/ssl/&lt;br>bookmarks /var/vpn/bookmark/&lt;br>dns /nsconfig/dns/&lt;br>htmlinjection /nsconfig/htmlinjection/&lt;br>imports /var/download/&lt;br>misc /nsconfig/license/&lt;br> /nsconfig/rc.conf&lt;br>all_plus_misc Includes *all* files and /nsconfig/license/ and /nsconfig/rc.conf.&lt;br>Default value: all.&lt;br>Possible values = all, bookmarks, ssl, htmlinjection, imports, misc, dns, krb, all_plus_misc, all_minus_misc</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[SYNC](#sync)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###sync



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/clusterfiles?action=sync
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

Request Payload: ```{"clusterfiles":{      "mode":<String[]_value>}}```
Response:
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


