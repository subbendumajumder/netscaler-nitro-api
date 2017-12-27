# Use Cases and Samples
This section covers some use case scenarios to certain resources and scenarios. More scenarios will be added in future updates to this section.

## Managing a NetScaler Cluster
For managing clusters, you can add or remove a cluster instance or an individual node and perform a few other instance or node operations such as viewing instance or node properties. You can also configure the cluster IP address. Other cluster-management tasks include joining a NetScaler appliance to the cluster and configuring a linkset. For detailed information and best practices, see Clustering.

### Cluster Instance Operations

This topic covers cluster instance operations by using REST APIs through HTTP or SDKs. 

**Using REST APIs through HTTP**

All operations on a cluster instance must be performed on the clusterinstance object.

For example, to create a cluster instance with ID 1, connect to the NetScaler appliance that you are first adding to the cluster.

**Request**

**HTTP Method:** POST

**URL:** http://&lt;netscaler-ip-address&gt;/nitro/v1/config/clusterinstance

**Request Headers:**

Cookie:NITRO\_AUTH\_TOKEN=&lt;tokenvalue&gt; 

Content-Type:application/json

**Request Payload:**
```json
{ 
    "clusterinstance": 
    { 
    "clid":1, 
    "preemption":"ENABLED" 
    } 
} 
```

**Response**

**HTTP Status Code on Success:** 201 Created

**HTTP Status Code on Failure:** 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error.

**Using REST APIs through SDKs**

The com.citrix.netscaler.nitro.resource.config.cluster.clusterinstance class provides APIs to manage a cluster instance.

The following sample code creates a cluster instance with ID 1.

**Java - Sample code to create a cluster instance**

```java
clusterinstance new_cl_inst_obj = new clusterinstance(); 

//Set the properties of the cluster instance locally 

new_cl_inst_obj.set_clid(1); 
new_cl_inst_obj.set_preemption("ENABLED"); 

//Upload the cluster instance 

clusterinstance.add(ns_session,new_cl_inst_obj);
```


**.NET - Sample code to create a cluster instance**

```csharp
clusterinstance new_cl_inst_obj = new clusterinstance(); 

//Set the properties of the cluster instance locally 

new_cl_inst_obj.clid = 1; 

new_cl_inst_obj.preemption = "ENABLED"; 

 

//Upload the cluster instance 

clusterinstance.add(ns_session,new_cl_inst_obj);

```


**Python - Sample code to create a cluster instance**

```python
new_cl_inst_obj = clusterinstance() 

 

#Set the properties of the cluster instance locally 

new_cl_inst_obj.clid = 1 



#Upload the cluster instance 

clusterinstance.add(ns_session, new_cl_inst_obj)
```

### Cluster Node Operations

This topic covers cluster node operations by using REST APIs through HTTP or SDKs. 

**Using REST APIs through HTTP**

All operations on a cluster node must be performed on the clusternode object. For example, to add a NetScaler appliance with NSIP address 10.102.29.60 to the cluster.

**Request**

**HTTP Method:** POST

**URL:** http://&lt;netscaler-ip-address&gt;/nitro/v1/config/clusternode

**Request Headers:**

Cookie:NITRO\_AUTH\_TOKEN=&lt;tokenvalue&gt; 

Content-Type:application/json

**Request Payload:**

```json
{ 
"clusternode": 
    { 
    "nodeid":1, 
    "ipaddress":"10.102.29.60", 
    "state":"ACTIVE", 
    "backplane":"1/1/2" 
    } 
} 
```

**Response**

**HTTP Status Code on Success:** 201 Created

**HTTP Status Code on Failure:** 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error.

**Using REST APIs through SDKs**


The com.citrix.netscaler.nitro.resource.config.cluster.clusternode class provides APIs to manage cluster nodes.

The following sample code adds a cluster node with NSIP address 10.102.29.60.

**Java - Sample code to add a cluster node**

```java
clusternode new_cl_node_obj = new clusternode(); 

//Set the properties of the cluster node locally 

new_cl_node_obj.set_nodeid(0); 

new_cl_node_obj.set_ipaddress("10.102.29.60"); 

new_cl_node_obj.set_state("ACTIVE"); 

new_cl_node_obj.set_backplane("0/1/1"); 

 

//Upload the cluster node 

clusternode.add(ns_session,new_cl_node_obj);
```


**.NET - Sample code to add a cluster node**

```csharp
clusternode new_cl_node_obj = new clusternode(); 

//Set the properties of the cluster node locally 

new_cl_node_obj.nodeid = 0; 

new_cl_node_obj.ipaddress = "10.102.29.60"; 

new_cl_node_obj.state = "ACTIVE"; 

new_cl_node_obj.backplane = "0/1/1"; 

 

//Upload the cluster node 

clusternode.add(ns_session,new_cl_node_obj);
```


**Python - Sample code to add a cluster node**

```python
new_cl_node_obj = clusternode() 


#Set the properties of the cluster node locally 

new_cl_node_obj.nodeid = 0 

new_cl_node_obj.ipaddress = "10.102.29.60" 

new_cl_node_obj.state = "ACTIVE" 

new_cl_node_obj.backplane = "0/1/1" 


#Upload the cluster node 

clusternode.add(ns_session, new_cl_node_obj)
```

### Add a Cluster IP Address

This topic covers adding a cluster IP address by using REST APIs through HTTP or SDKs. 

**Using REST APIs through HTTP**

To define a cluster IP address, specify the required parameters in the nsip object. For example, to configure a cluster IP address.

**Request**

**HTTP Method:** POST

**URL:** http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsip


**Request Headers:**

Cookie:NITRO\_AUTH\_TOKEN=&lt;tokenvalue&gt; 

Content-Type:application/json

**Request Payload:**

```json
{ 
"nsip": 
    { 
    "ipaddress":"10.102.29.61",  
    "netmask":"255.255.255.255", 
    "type":"CLIP" 
    } 
} 
```

**Response**

**HTTP Status Code on Success:** 201 Created

**HTTP Status Code on Failure:** 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error.

**Using REST APIs through SDKs**

The com.citrix.netscaler.nitro.resource.config.ns.nsip class provides the add() API to configure an IP address. To configure the IP address as a cluster IP address, you must specify the type as CLIP.

The following sample code configures a cluster IP address on NetScaler appliance with IP address 10.102.29.60.

**Java - Sample code to add a cluster IP address**

```java
nsip new_nsip_obj = new nsip(); 

//Set the properties locally 

new_nsip_obj.set_ipaddress("10.102.29.61"); 

new_nsip_obj.set_netmask("255.255.255.255"); 

new_nsip_obj.set_type("CLIP"); 

 

//Upload the cluster node 

nsip.add(ns_session,new_nsip_obj);
```


**.NET - Sample code to add a cluster IP address**

```csharp
nsip new_nsip_obj = new nsip(); 

//Set the properties locally 

new_nsip_obj.ipaddress = "10.102.29.61"; 

new_nsip_obj.netmask = "255.255.255.255"; 

new_nsip_obj.type = "CLIP"; 

 

//Upload the cluster node 

nsip.add(ns_session,new_nsip_obj);
```


**Python - Sample code to add a cluster IP address**

```python
new_nsip_obj = nsip() 


#Set the properties locally 

new_nsip_obj.ipaddress = "10.102.29.61" 

new_nsip_obj.netmask = "255.255.255.255" 

new_nsip_obj.type = "CLIP" 


#Upload the cluster node 

nsip.add(ns_session, new_nsip_obj)
```


### Add a Spotted IP Address

This topic covers adding a spotted IP address by using REST APIs through HTTP or SDKs. 

**Using REST APIs through HTTP**

To configure an IP address as spotted, specify the required parameters in the nsip object. This configuration must be done on the cluster IP address.

For example, to configure a spotted SNIP address on a node with ID 1.

**Request**

**HTTP Method:** POST

**URL:** http://\<cluster-ip-address\>/nitro/v1/config/nsip


**Request Headers:**

Cookie:NITRO\_AUTH\_TOKEN=&lt;tokenvalue&gt; 

Content-Type:application/json

**Request Payload:**

```json
{ 
"nsip": 
    { 
    "ipaddress":"10.102.29.77",  
    "netmask":"255.255.255.0", 
    "type":"SNIP", 
    "ownernode":1 
    } 
} 
```

**Response**

**HTTP Status Code on Success:** 201 Created

**HTTP Status Code on Failure:** 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error.

**Using REST APIs through SDKs**

The com.citrix.netscaler.nitro.resource.config.ns.nsip class provides the add() API to configure an IP address. To configure the IP address as spotted, you must specify the ID of the node that must own the IP address. This configuration must be done on the cluster IP address.

The following sample code configures a spotted SNIP address on a node with ID 1.

**Java - Sample code to configure a spotted IP address**

```java
nsip new_nsip_obj = new nsip();

//Set the properties locally

new_nsip_obj.set_ipaddress("10.102.29.77");

new_nsip_obj.set_netmask("255.255.255.0");

new_nsip_obj.set_type("SNIP");

new_nsip_obj.set_ownernode(1);


//Upload the cluster node

nsip.add(ns_session,new_nsip_obj);
```


**.NET - Sample code to configure a spotted IP address**

```csharp
nsip new_nsip_obj = new nsip(); 

//Set the properties locally 

new_nsip_obj.ipaddress = "10.102.29.77"; 

new_nsip_obj.netmask = "255.255.255.0"; 

new_nsip_obj.type = "SNIP"; 

new_nsip_obj.ownernode = 1; 

 

//Upload the cluster node 

nsip.add(ns_session,new_nsip_obj);
```


**Python - Sample code to configure a spotted IP address**

```python
#Add a spotted IP address

new_nsip_obj = nsip()


#Set the properties locally

new_nsip_obj.ipaddress = "10.102.29.77"

new_nsip_obj.netmask = "255.255.255.0"

new_nsip_obj.type = "SNIP"

new_nsip_obj.ownernode = 1


#Upload the cluster node

nsip.add(ns_session, new_nsip_obj)
```

### Join NetScaler Appliance to Cluster

This topic covers adding a NetScaler appliance to a cluster by using REST APIs through HTTP or SDKs. 

**Using REST APIs through HTTP**

To join an appliance to a cluster, specify the required parameters in the cluster object. For example, to join a NetScaler appliance to a cluster.

**Request**

**HTTP Method:** POST

**URL:** http://&lt;netscaler-ip-address&gt;/nitro/v1/config/cluster

**Request Headers:**

Cookie:NITRO\_AUTH\_TOKEN=&lt;tokenvalue&gt; 

Content-Type:application/json

**Request Payload:**

```json
{ 
"cluster": 
    { 
    "clip":"10.102.29.61", 
    "password":"verysecret" 
    } 
} 
```

**Response**

**HTTP Status Code on Success:** 201 Created

**HTTP Status Code on Failure:** 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error.

**Using REST APIs through SDKs**

The com.citrix.netscaler.nitro.resource.config.cluster.cluster class provides the join() API to join a NetScaler appliance to the cluster. You must specify the cluster IP address and the nsroot password of the configuration coordinator.

The following sample code joins a NetScaler appliance to a cluster.

**Java - Sample code to join an appliance to a cluster**

```java
cluster new_cl_obj = new cluster(); 

//Set the properties of the cluster  locally 

new_cl_obj.set_clip("10.102.29.61"); 

new_cl_obj.set_password("verysecret"); 

 

//Upload the cluster 

cluster.add(ns_session,new_cl_obj);
```


**.NET - Sample code to join an appliance to a cluster**

```csharp
cluster new_cl_obj = new cluster(); 

//Set the properties of the cluster locally 

new_cl_obj.clip = "10.102.29.61"; 

new_cl_obj.password = "verysecret"; 

 
//Upload the cluster node 

cluster.add(ns_session,new_cl_node_obj);
```


**Python - Sample code to join an appliance to a cluster**

```python
new_cl_obj = cluster()


#Set the properties of the cluster locally

new_cl_obj.clip = "10.102.29.61"

new_cl_obj.password = "verysecret"


#Upload the cluster
cluster.add(ns_session, new_cl_obj)
```

### Linkset Operations

This topic covers some linkset operations by using REST APIs through HTTP or SDKs. 

**Using REST APIs through HTTP**

To configure a linkset, do the following:

Create a linkset by specifying the required parameters in the linkset object. For example, to add a linkset LS/1:

**Request:**

**HTTP Method:** POST

**URL:** http://\<cluster-ip-address\>/nitro/v1/config/linkset


**Request Headers:**

Cookie:NITRO\_AUTH\_TOKEN=&lt;tokenvalue&gt; 

Content-Type:application/json

**Request Payload**

```json
{ 
"linkset": 
    { 
    "id":"LS/1" 
} 
} 
```

**Response**

**HTTP Status Code on Success:** 201 Created

**HTTP Status Code on Failure:** 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error.

Bind the required interfaces to the linkset by specifying the interfaces in the linkset_interface_binding object.For example, to bind interfaces 1/1/2 and 2/1/2 to linkset LS/1.
    
**Request**

**HTTP Method:** PUT

**URL:** http://\<cluster-ip-address\>/nitro/v1/config/linkset_interface_binding/LS%2F1?action=bind
**Note.** The linkset name (LS/1), must be URL encoded as LS%2F1.

**Request Headers:**

Cookie:NITRO\_AUTH\_TOKEN=\<tokenvalue> 

Content-Type:application/json

**Request Payload:**

```json
{ 
"linkset_interface_binding": 
    { 
    "id":"LS/1", 
    "ifnum":"1/1/2 2/1/2" 
    } 
} 
```

**Response**

**HTTP Status Code on Success:** 200 Ok

**HTTP Status Code on Failure:** 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error.

**Using REST APIs through SDKs**

The com.citrix.netscaler.nitro.resource.config.network.linkset class provides the APIs to manage linksets.

To configure a linkset, do the following:

1. Add a linkset by invoking the add() method of the linkset class.
2. Bind the interfaces to the linkset using the add() method of the linkset_interface_binding class.

The following sample code creates a linkset LS/1 and bind interfaces 1/1/2 and 2/1/2 to it.

**Java - Sample code to configure linksets**

```java
linkset new_linkset_obj = new linkset(); 

new_linkset_obj.set_id("LS/1"); 

linkset.add(ns_session,new_linkset_obj); 

 

//Bind the interfaces to the linkset 

linkset_interface_binding new_linkif_obj = new linkset_interface_binding(); 

new_linkif_obj.set_id("LS/1"); 

new_linkif_obj.set_ifnum("1/1/2 2/1/2"); 

linkset_interface_binding.add(ns_session,new_linkif_obj);
```

**.NET - Sample code to configure linksets**

```csharp
linkset new_linkset_obj = new linkset(); 

new_linkset_obj.id = "LS/1"; 

linkset.add(ns_session,new_linkset_obj); 


//Bind the interfaces to the linkset 

linkset_interface_binding new_linkif_obj = new linkset_interface_binding(); 

new_linkif_obj.id = "LS/1"; 

new_linkif_obj.ifnum = "1/1/2 2/1/2"; 

linkset_interface_binding.add(ns_session,new_linkif_obj); 
```

**Python - Sample code to configure linksets**

```python
#Create a new linkset

new_linkset_obj = linkset()

new_linkset_obj.id = "LS/1"

linkset.add(ns_session, new_linkset_obj)



#Bind the interfaces to the linkset

new_linkif_obj = linkset_interface_binding()

new_linkif_obj.id = "LS/1"

new_linkif_obj.ifnum = "1/1/2 2/1/2"

linkset_interface_binding.add(ns_session, new_linkif_obj)
```

## Configuring Admin Partitions

To create an admin partition, you must perform a set of operations on the default partition. To understand this procedure, let us consider a company that has two departments each of which has an application that requires the NetScaler functionality. The NetScaler admin wants to have a different partition for each department so that there is isolation of users and configurations. For detailed information and best practices, see Admin Partitions.

### Creating an Admin Partition

While creating an admin partition, you must also specify the system resources that must be allocated to that partition.

**Using REST APIs through HTTP**

The following example creates an admin partition named partition-dept1.

**Request**

**HTTP Method:** POST

**URL:** http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nspartition

**Request Headers:**

Cookie:NITRO\_AUTH\_TOKEN=&lt;tokenvalue&gt; 

Content-Type:application/json

**Request Payload:**

```json
{ 
"nspartition": 
{ 
    "partitionname":"partition-dept1", 
    "maxbandwidth":"10240",  
    "minbandwidth":"10240", 
    "maxconn":"1024", 
    "maxmemlimit":"10" 
} 
}
```

**Response**

**HTTP Status Code on Success:** 201 Created

**HTTP Status Code on Failure:** 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error.

**Using REST APIs through SDKs**

The following sample code creates an admin partition named partition-dept1.

**Java - Sample code to create an admin partition**

```java
nspartition nspartitionObject = new nspartition(); 

nspartitionObject.set_partitionname("partition-dept1"); 

nspartitionObject.set_maxbandwidth(10240); 

nspartitionObject.set_maxconn(1024); 

nspartitionObject.set_maxmemlimit(10); 

nspartitionObject.set_minbandwidth(1240); 

base_response result = nspartition.add(nitroService, nspartitionObject);
```

**.NET - Sample code to create an admin partition**

```csharp
nspartition nspartitionObject = new nspartition(); 

nspartitionObject.partitionname = "partition-dept1"; 

nspartitionObject.maxbandwidth = 10240; 

nspartitionObject.maxconn = 1024; 

nspartitionObject.maxmemlimit = 10; 

nspartitionObject.minbandwidth = 1240; 

base_response result = nspartition.add(nitroService, nspartitionObject);
```


**Python - Sample code to create an admin partition**

```python
nspartitionObject = nspartition()

nspartitionObject.partitionname = "partition-dept1"

nspartitionObject.maxbandwidth = 10240

nspartitionObject.maxconn = 1024

nspartitionObject.maxmemlimit = 10

nspartitionObject.minbandwidth = 1240

result = nspartition.add(nitroService, nspartitionObject)
```


### Associating Users with Partitions
Associate the appropriate users with the partition.

**Using REST APIs through HTTP**

The following example associates user1 to a partition named partition-dept1.

**Request**

**HTTP Method:** PUT

**URL:** http://\<netscaler-ip-address \>/nitro/v1/config/systemuser_nspartition_binding/user1

**Request Headers:**

Cookie:NITRO\_AUTH\_TOKEN=&lt;tokenvalue&gt; 

Content-Type:application/json

**Request Payload:**

```json
{ 
    "systemuser_nspartition_binding": 
    { 
    "username":"user1",  
    "partitionname":"partition-dept1" 
    } 
}   
```

**Response**

**HTTP Status Code on Success:** 201 Created

**HTTP Status Code on Failure:** 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error.

**Using REST APIs through SDKs**

The following sample code associates "user1" to a partition named "partition-dept1".

**Java - Sample code for associating user with partition**

```java
systemuser_nspartition_binding systemuser_nspartition_binding_object = new systemuser_nspartition_binding(); 

systemuser_nspartition_binding_object.set_partitionname("partition-dept1"); 

systemuser_nspartition_binding_object.set_username("user1"); 

base_response result = systemuser_nspartition_binding.add(nitroService, systemuser_nspartition_binding_object);
```


**.NET - Sample code for associating user with partition**

```csharp
systemuser_nspartition_binding systemuser_nspartition_binding_object = new systemuser_nspartition_binding(); 

systemuser_nspartition_binding_object.partitionname = "partition-dept1"; 

systemuser_nspartition_binding_object.username = "user1"; 

base_response result = systemuser_nspartition_binding.add(nitroService, systemuser_nspartition_binding_object);
```

**Python - Sample code for associating user with partition**

```python
systemuser_nspartition_binding_object =  systemuser_nspartition_binding()

systemuser_nspartition_binding_object.partitionname = "partition-dept1"

systemuser_nspartition_binding_object.username = "user1"

result = systemuser_nspartition_binding.add(nitroService, systemuser_nspartition_binding_object)
```

### Specifying Command Policy for Partition Users

Associate an appropriate command policy to the admin partition user.

**Using REST APIs through HTTP**

The following example associates the command policy partition-admin to user1.

**Request**

**HTTP Method:** PUT

**URL:** http://&lt;netscaler-ip-address&gt;/nitro/v1/config/systemuser_systemcmdpolicy_binding/user1

**Request Headers:**

Cookie:NITRO\_AUTH\_TOKEN=&lt;tokenvalue&gt; 

Content-Type:application/json

**Request Payload:**

```json
{ 
    "systemuser_systemcmdpolicy_binding": 
    { 
    "username":"user1",  
    "policyname":"partition-admin", 
    "priority":"1" 
    } 
}
```

**Response**

**HTTP Status Code on Success:** 201 Created

**HTTP Status Code on Failure:** 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error.

**Using REST APIs through SDKs**

The following sample code associates the command policy "partition-admin" to "user1".

**Java - Sample code to specify command policy for partition user**

```java
systemuser_systemcmdpolicy_binding binding_object = new systemuser_systemcmdpolicy_binding();

binding_object.set_username("user1");

binding_object.set_policyname("partition-admin");

binding_object.set_priority(1);

base_response result = systemuser_systemcmdpolicy_binding.add(nitroService,binding_object);
```


**.NET - Sample code to specify command policy for partition user**

```csharp
systemuser_systemcmdpolicy_binding binding_object = new systemuser_systemcmdpolicy_binding();

binding_object.username = "user1";

binding_object.policyname = "partition-admin";

binding_object.priority = 1;

base_response result = systemuser_systemcmdpolicy_binding.add(nitroService,binding_object);
```


**Python - Sample code to specify command policy for partition user**

```python
binding_object = systemuser_systemcmdpolicy_binding()

binding_object.username = "user1"

binding_object.policyname = "partition-admin"

binding_object.priority = 1

result = systemuser_systemcmdpolicy_binding.add(nitroService,binding_object)
```


### Specifying the Admin Partition VLAN or Bridgegroup

Specify the VLANs or bridgegroups to be associated with the partition. This step ensures network isolation of the traffic. Traffic received on the interfaces of the VLAN or bridgegroup is isolated from the traffic of other partitions.

**Using REST APIs through HTTP**

The following example specifies a VLAN for an admin partition.

**Request**

**HTTP Method:** PUT

**URL:** http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nspartition_vlan_binding/partition-dept1

**Request Headers:**

Cookie:NITRO\_AUTH\_TOKEN=&lt;tokenvalue&gt; 

Content-Type:application/json

**Request Payload:**

```json
{ 
    "nspartition_vlan_binding": 
    { 
    "partitionname":"partition-dept1", 
    "vlan":"2" 
    } 
}    
```

**Response**

**HTTP Status Code on Success:** 201 Created

**HTTP Status Code on Failure:** 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error.

**Using REST APIs through SDKs**

The following sample code specifies a VLAN for an admin partition.

**Java - Sample Code to specify the VLAN**

```java
nspartition_vlan_binding nspartition_vlan_binding_object = new nspartition_vlan_binding();

nspartition_vlan_binding_object.set_vlan(2);

nspartition_vlan_binding_object.set_partitionname("partition-dept1");

base_response result = nspartition_vlan_binding.add(nitroService, nspartition_vlan_binding_object);
```

**.NET - Sample code to specify the VLAN**

```csharp
nspartition_vlan_binding nspartition_vlan_binding_object = new nspartition_vlan_binding();

nspartition_vlan_binding_object.vlan = 2;

nspartition_vlan_binding_object.partitionname = "partition-dept1";

base_response result = nspartition_vlan_binding.add(nitroService, nspartition_vlan_binding_object);
```

**Python - Sample code to specify the VLAN**

```python
nspartition_vlan_binding_object = nspartition_vlan_binding()

nspartition_vlan_binding_object.vlan = 2

nspartition_vlan_binding_object.partitionname = "partition-dept1"

result = nspartition_vlan_binding.add(nitroService, nspartition_vlan_binding_object)
```

### Switching Partitions

If you are associated with multiple admin partitions, you can switch to the required partition.

**Using REST APIs through HTTP**

The following  example shows how to switch from current partition to a partition named partition-dept2.

**Request**

**HTTP Method:** POST

**URL:** http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nspartition?action=Switch

**Request Headers:**

Cookie:NITRO\_AUTH\_TOKEN=&lt;tokenvalue&gt; 

Content-Type:application/json

**Request Payload:**

```json
{ 
    "nspartition": 
    { 
    "partitionname":"partition-dept2" 
    } 
}
```

**Response**

**HTTP Status Code on Success:** 201 Created

**HTTP Status Code on Failure:** 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error.
    
**Using REST APIs through SDKs**

The following sample code switches from current partition to a partition named "partition-dept2".

**Java - Sample code to switch partitions**

```java
nspartition nspartitionObject = new nspartition(); 

vnspartitionObject.set_partitionname("partition-dept2"); 

base_response result = nspartition.Switch(nitroService, nspartitionObject);
```

**.NET - Sample code to switch partitions**

```csharp
nspartition nspartitionObject = new nspartition(); 

nspartitionObject.partitionname = "partition-dept2"; 

base_response result = nspartition.Switch(nitroService, nspartitionObject);
```

**Python - Sample code to switch partitions**

```python
nspartitionObject = nspartition()

nspartitionObject.partitionname = "partition-dept2"

result = nspartition.Switch(nitroService, nspartitionObject)
```

## Managing AppExpert Applications
The following sections talks about exporting and importing an AppExpert application using NITRO APIs.

### Exporting an AppExpert Application

This topic covers exporting an AppExpert application by using REST APIs through HTTP or SDKs. 

**Using REST APIs through HTTP**

To export an AppExpert application, specify the parameters needed for the export operation in the apptemplateinfo object. Optionally, you can specify basic information about the AppExpert application template, such as the author of the configuration, a summary of the template functionality, and the template version number, in the template_info object. This information is stored as part of the template file that is created.

For example, to export an AppExpert application named MyApp1.

**Request**

**HTTP Method:** POST

**URL:** http://&lt;netscaler-ip-address&gt;/nitro/v1/config/apptemplateinfo?action=export

**Request Headers:**

Cookie:NITRO\_AUTH\_TOKEN=&lt;tokenvalue&gt; 

Content-Type:application/json

**Request Payload:**

```json
{ 
    "apptemplateinfo": 
    { 
        "appname":"MyApp1", 
        "apptemplatefilename":"BizAp.xml", 
        "template_info": 
        { 
            "templateversion_major":"2", 
            "templateversion_minor":"1", 
            "author":"XYZ", 
            "introduction":"Intro", 
            "summary":"Summary" 
        } 
    } 
}
```

**Response**

**HTTP Status Code on Success:** 200 OK

**HTTP Status Code on Failure:** 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error.


**Using REST APIs through SDKs**

To export an AppExpert application, you must do the following:

1. Instantiate the com.citrix.netscaler.nitro.resource.config.app.application class.
    
    **Note.** For the python SDK, the package path is of the form nssrc.com.citrix.netscaler......

2. Configure the properties of the AppExpert locally.
3. Export the AppExpert application.


The following samples export an AppExpert application named MyApp1.

**JAVA - sample code to export an AppExpert application**

```java
application myapp = new application(); 
myapp.set_appname("MyApp1"); 
myapp.set_apptemplatefilename("myapp_template"); 
application.export(ns_session,myapp);
```

**.NET - sample code to export an AppExpert application**

```csharp
application myapp = new application(); 
myapp.appname = "MyApp1"; 
myapp.apptemplatefilename = "myapp_template"; 
application.export(ns_session,myapp);
```

**Python - sample code to export an AppExpert application**

```python
myapp = application()
myapp.appname = "MyApp1"
myapp.apptemplatefilename = "myapp_template"
application.export(ns_session, myapp)
```

### Importing an AppExpert Application

This topic covers importing an AppExpert application by using REST APIs through HTTP or SDKs.

**Using REST APIs through HTTP**

To import an AppExpert application, specify the parameters needed for the import operation in the apptemplateinfo object.

For example, to import an AppExpert application named MyApp1.

**Request**

**HTTP Method:** POST

**URL:** http://&lt;netscaler-ip-address&gt;/nitro/v1/config/apptemplateinfo?action=import

**Request Headers:**

Cookie:NITRO\_AUTH\_TOKEN=&lt;tokenvalue&gt; 

Content-Type:application/json

**Request Payload:**

```json
{ 
"apptemplateinfo": 
{ 
    "apptemplatefilename":"BizAp.xml", 
    "deploymentfilename":"BizAp_deployment.xml", 
    "appname":"MyApp1" 
} 
}
```

**Response**

**HTTP Status Code on Success:** 200 OK

**HTTP Status Code on Failure:** 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error.

To import an AppExpert application by specifying different deployment settings.

**Request**

**HTTP Method:** POST

**URL:** http://&lt;netscaler-ip-address&gt;/nitro/v1/config/apptemplateinfo?action=import

**Request Headers:**

Cookie:NITRO\_AUTH\_TOKEN=&lt;tokenvalue&gt; 

Content-Type:application/json

**Request Payload:**

```json
{ 
    "apptemplateinfo": 
    { 
    "apptemplatefilename":"BizAp.xml", 
    "appname":"Myapp2", 
    "deploymentinfo": 
    { 
        "appendpoint": 
        [ 
            { 
                "ipv46":"11.2.3.8", 
                "port":80, 
                "servicetype":"HTTP" 
            } 
        ], 
        "service": 
        [ 
            { 
                "ip":"12.3.3.15",   
                "port":80, 
                "servicetype":"SSL" 
            }, 
            { 
                "ip":"14.5.5.16",   
                "port":443, 
                "servicetype":"SSL" 
            } 
        ] 
    } 
    } 
}
```

**Response**

**HTTP Status Code on Success:** 200 OK

**HTTP Status Code on Failure:** 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error.

**Using REST APIs through SDKs**

To import an AppExpert application, you must do the following:

1. Instantiate the com.citrix.netscaler.nitro.resource.config.app.application class.
    
    **Note**. For the python SDK, the package path is of the form nssrc.com.citrix.netscaler......

2. Configure the properties of the AppExpert locally.
3. Import the AppExpert application.

The following samples import an AppExpert application named MyApp1.

**Java - sample code to import an AppExpert application**

```java
application myapp = new application();
myapp.set_appname("MyApp1");
myapp.set_apptemplatefilename("myapp_template");
application.Import(ns_session,myapp);
```

**.NET - sample code to import an AppExpert application**

```csharp
application myapp = new application(); 
myapp.appname = "MyApp1"; 
myapp.apptemplatefilename = "myapp_template"; 
application.Import(ns_session,myapp);
```


**Python - sample code to import an AppExpert application**

```python
myapp = application()
myapp.appname = "MyApp1"
myapp.apptemplatefilename = "myapp_template"
application.Import(ns_session, myapp)
```

## Automate NetScaler Upgrade and Downgrade with a Single API

You can use the "install" API to automate not just installation, but also an upgrade or a downgrade of the build on a NetScaler appliance. You can specify a local or remote location for the build file.

**Using REST APIs through HTTP**

For example, the following information describes a downgrade to NetScaler release 10.5 build 46, using a local  build file:

**Request**
    
**HTTP Method:** POST

**URL:** http://\<NSIP\>/nitro/v1/config/install

**Request Headers:** 

Cookie:NITRO\_AUTH\_TOKEN=\<tokenvalue \>

Content-Type: application/json

**Request Payload:**

```json
{

“install”:

{

        “url”: “file:///var/tagma/build_tagma_46_nc.tgz”


    }                           

}     
```


**Response**
    
**HTTP status Code on Success:**

201 Created

209 Netscaler specific warning

**Note.** when “y” option is not specified and warning is enabled, API returns “1120 - The configuration must be saved and the system rebooted for these settings to take effect” message in X-NITRO-WARNING.

**HTTP Status Code on Failure:** 599 Netscaler specific error


**Additional parameters available in the install API request payload**

* “y”:“true” -  This option enables reboot on successful loading of kernel.

* “L”:“true” -  This option enables the callhome feature.

**Supported formats for the "url" parameter (specifies the location of the tar.gz file for the build)**

* http://[user]:[password]@host/path/to/file
* https://[user]:[password]@host/path/to/file
* sftp://[user]:[password]@host/path/to/file
* scp://[user]:[password]@host/path/to/file
* ftp://[user]:[password]@host/path/to/file
* file://path/to/file

**Possible errors**

* Installation failed. [No space on file system. Please check the log file /var/tmp/install​]
* Installation failed. [File transfer failed]
* Installation failed. [File does not exist]
* Installation failed. [Failed to copy file to /var/tmp]
* Installation failed. [Extraction failed, invalid tar archive?​]
* Installation failed. [Invalid file transfer protocol]
* Installation failed. [Unable to create temporary directory]
* Installation failed. [Please check the log file /var/tmp/install for more information]

## Handle Multiple NITRO Calls in a Single Request

You can use the "macroapi" API to create, update, and delete multiple resources simultaneously, and thereby minimize network traffic. For example, multiple load-balancing virtual servers can be added in a single API.

To account for the failure of some operations within the bulk operation, NITRO allows configuring one of the following behaviors.

* **EXIT**. When the first error is encountered, execution stops. The commands that were executed before the error are committed.
* **ROLLBACK**. When the first error is encountered, execution stops. The commands that were executed before the error are rolled back. Rollback is supported for add and bind commands only.
* **CONTINUE**. All the commands in the request are executed even if some commands fail.

You must specify the behavior of the bulk operation in the request header, by using the X-NITRO-ONERROR parameter.

**Advantages**

Heterogeneous resources can be configured with a single API. For example, multiple load balancing virtual servers and multiple services can be created, and services can be bound to load balancing virtual servers in a single API.

**Limitations**

Only homogenous operation is supported in this API. For example, multiple load balancing virtual servers can be created but cannot be updated or deleted in the same API.
“rollback” is supported only on “add” and “bind” operations.

**Using REST APIs through HTTP**

To add multiple load balancing resources in a single request:

**Request**
    
**HTTP Method:** POST

**URL:** http://\<NSIP\>/nitro/v1/config/macroapi

**Request Headers:**

Content-Type: application/json

Cookie: NITRO\_AUTH\_TOKEN=&lt;tokenvalue&gt;

X-NITRO-ONERROR: exit


**Request Payload:**
    
```json
{

"lbvserver":[  

{"name":"lbv1","servicetype":"http"},

{"name":"lbv2","servicetype":"http"}

],

"serviceGroup": [

{ "servicegroupname": "sg1", "servicetype": "HTTP" },

{ "servicegroupname": "sg2", "servicetype": "HTTP" }

],

"lbvserver_servicegroup_binding":[ 

{ "name":"lbv1", "servicegroupname":"sg1" },

{ "name":"lbv2", "servicegroupname":"sg2" }

]

}
```

**Response**
    
**HTTP Status Code on Success:** 201 Created for the add operation and 200 OK for the update operation.

**HTTP Status Code on Failure:** 207 Multi Status with error details in the response payload. For more information, see Error Handling.

For deleting multiple resources using macroapi, use POST HTTP method with query parameter “action=remove” in the URI.

## Simplify Management Operations with an Idempotent API
You can add or update NetScaler resources seamlessly, with a single API. Previously, an attempt to add a resource that was already configured, or to update a resource that was not yet configured, caused an error.

If you enable the “idempotent” query parameter (“idempotent=yes”) in any POST request, NITRO executes the request in an idempotent manner. An idempotent HTTP method is an HTTP method that can be called many times without different results, and POST is desinged as a non-idempotent method.

**Note.** Use POST request with “idempotent” option if you are unsure whether the resource in the request exists on NetScaler or not.

This API  hides the inconsistencies between parameter lists of POST and PUT operations. For some NITRO resources, certain parameters are accepted only on PUT not in POST, or vice versa. By using this idempotent API, you can overcome such challenges.

**Limitations**

If a resource is already configured and you try to add the same resource again, the resource is  "updated," but the arguments already present are not unset. For example, if a  load balancing virtual server named  "V1" is configured to use the round robin load balancing method, and you try to ADD an lbvserver named "V1" without specifying a value for "lbmethod" in the request, the NetScaler appliance does not  unset "lbmethod" to its default value of "leastconnection."

**Using REST APIs through HTTP**

In the following example, “preferredntpserver” is allowed only in PUT, but when given in POST request with idempotent=yes, NITRO internally adds the ntpserver and updates it with given properties.

**Request**
    
**HTTP Method:** POST

**URL:** http://\<NSIP\>/nitro/v1/config/ntpserver?idempotent=yes

**Request Headers:**

Cookie:NITRO\_AUTH\_TOKEN=&lt;tokenvalue&gt;

Content-Type: application/json


**Request Payload:**

```json
{

“ntpserver”:{“servername”:“ntp1”,“minpoll”:“4,  “preferredntpserver”: “yes”}


}
```

**Response**
    
**HTTP Status Code on Success:** 200 OK

**HTTP Status Code on Failure:** 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error.
    
## Retrieve Bindings in Bulk
This topic covers retrieving bindings information in bulk by using REST APIs through HTTP.

**Using REST APIs through HTTP**

You can use a bulk GET API to fetch bindings of all the entities of a given entity type.

For example, you can fetch bindings of all the load balancing virtual servers in one call instead of by using multiple GET by "name" calls. In the examples below, the NetScaler appliance has the following configuration.

* add lb vserver lbv1 http
* add lb vserver lbv2 http
* add service svc1 10.20.30.40 http 80
* add servicegroup sg1 http
* bind lb vserver lbv1 svc1
* bind lb vserver lbv1 sg1
* bind lb vserver lbv2 svc1
* bind lb vserver lbv2 sg1

**Example - To fetch bindings of all lbvservers, in a single NITRO API**

**Request**
    
**HTTP Method:** GET

**URL:** http://\<NSIP\>/nitro/v1/config/lbvserver_binding?bulkbindings=yes

**Request Headers:**

Cookie:NITRO\_AUTH\_TOKEN=&lt;tokenvalue&gt;

Accept: application/json

**Response**
    
**HTTP Status Code on Success:** 200 OK

**HTTP Status Code on Failure:** 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error.

**Response Header:** Content-Type:application/json

**Response Payload:**

```json
{

"errorcode":0,

"message":"Done",

"severity":"NONE",

"lbvserver_binding":[

{

    "name":"lbv1",

    "lbvserver_service_binding":[

    {

        "name":"lbv1",

        "servicename":"svc1",

        "stateflag":"536936451",

        "ipv46":"10.20.30.40",

        "port":80,

        "servicetype":"HTTP",

        "curstate":"DOWN",

        "weight":"1",

        "dynamicweight":"0",

        "cookieipport":"",

        "vserverid":"mcw1",

        "vsvrbindsvcip":"10.20.30.40",

        "vsvrbindsvcport":80,

        "preferredlocation":""

    }

    ],

    "lbvserver_servicegroup_binding":[

    {

        "name":"lbv1",

        "servicegroupname":"sg1",

        "stateflag":"536936464",

        "servicename":"sg1"

    }

    ]

},

{

    "name":"lbv2",

    "lbvserver_service_binding":[

    {

        "name":"lbv2",

        "servicename":"svc1",

        "stateflag":"536936451",

        "ipv46":"10.20.30.40",

        "port":80,

        "servicetype":"HTTP",

        "curstate":"DOWN",

        "weight":"1",

        "dynamicweight":"0",

        "cookieipport":"",

        "vserverid":"mcw2",

        "vsvrbindsvcip":"10.20.30.40",

        "vsvrbindsvcport":80,

        "preferredlocation":""

    }        


    ],

    "lbvserver_servicegroup_binding":[

    {

        "name":"lbv2",

        "servicegroupname":"sg1",

        "stateflag":"536936464",

        "servicename":"sg1"

    }        


    ]

}


]

}
```

**Example - To fetch only “service” bindings of all lbvservers**

**Request**
    
**HTTP Method:** GET

**URL:** http://\<NSIP\>/nitro/v1/config/lbvserver_service_binding?bulkbindings=yes

**Request Header:** Content-Type:application/json

**Response**
    
**Response Payload:**
    
```json
{ 

"errorcode":0,

"message":"Done",

"severity":"NONE",

"lbvserver_service_binding":[ 

    { 

        "name":"lbv1",

        "servicename":"svc1",

        "stateflag":"536936451",

        "ipv46":"10.20.30.40",

        "port":80,

        "servicetype":"HTTP",

        "curstate":"DOWN",

        "weight":"1",

        "dynamicweight":"0",

        "cookieipport":"",

        "vserverid":"mcw1",

        "vsvrbindsvcip":"10.20.30.40",

        "vsvrbindsvcport":80,

        "preferredlocation":""

    },

    { 

        "name":"lbv2",

        "servicename":"svc1",

        "stateflag":"536936451",

        "ipv46":"10.20.30.40",

        "port":80,

        "servicetype":"HTTP",

        "curstate":"DOWN",

        "weight":"1",

        "dynamicweight":"0",

        "cookieipport":"",

        "vserverid":"mcw2",

        "vsvrbindsvcip":"10.20.30.40",

        "vsvrbindsvcport":80,

        "preferredlocation":""

    }   


    ]

}
```
    
## View Individual Counter Information
This topic viewing individual counter information by using REST APIs through HTTP. 

**Using REST APIs through HTTP**

To view global counters that are not otherwise shown by the NetScaler CLI or the GUI, you can now use the following URL format.

**URL**: http://\<NSIP\>/nitro/v1/stat/nsglobalcntr?args=counters:\<counter1\>;\<counter2\>

Previously, these counter values could be viewed only through the “nsconmsg” Shell command.

**Note.** You can view only global counters of type ULONG and only up to 12 counters in a single request.

**Example**

This example shows how to view the individual counters http_tot_Requests and http_tot_Responses. Enter the details in the system or tool that you are using to generate HTTP or HTTPS requests.

**Request**

**HTTP Method:** GET

**URL:** http://\<NSIP\>/nitro/v1/stat/nsglobalcntr?args=counters:http_tot_Requests;http_tot_Responses

**Response**
    
```json
{
"errorcode": 0,

"message": "Done",

"severity": "NONE",

"nsglobalcntr": 
    {
    "http_tot_Requests": "5783",
    "http_tot_Responses": "5783"
    }
}
```
    
## Prevent XSS and CSRF Attacks by Disabling Basic Authentication

As an administrator or a root user, you can now prevent users from making API calls after using basic authentication (such as one-time credentials) to log on. You can use this feature to prevent Cross-Site Scripting (XSS), Cross-Site Request Forgery (CSRF), and other types of attacks.

**Procedure for Disabling Basic Authentication**

Use the following formats to enter the details in the system or tool that you are using to generate HTTP or HTTPS requests.

**Using REST APIs through HTTP**

**Request**
    
**URL:** http://\<netscaler-ip-address \>/nitro/v1/config/systemparameter

**HTTP Method:** PUT

**Request Headers:**

Cookie:NITRO\_AUTH\_TOKEN=&lt;tokenvalue&gt;

Content-Type:application/json


**Request Payload:**

```json
{
    "systemparameter":{ "basicauth":"disabled",}
    
}
```


**Response**

**HTTP Status Code on Success:** 200 OK

After you disable the basic authentication, access to NetScaler through the one-time password is denied and an error message is displayed.

**Example**

This example shows what happens if you make any API call after basic authentication has been disabled. 

**Request**

**URL:** http://10.102.201.159/nitro/v1/config/lbvserver

**HTTP Method:** GET

After you make a GET call, the a logon screen appears. If you click **Log In** after entering the logon credentials, then you get the following response, which shows an error message. 

**Response**

```json
{"errorcode": 1244,"message": "Authentication Failed: Use of Basic Authentication is Disabled.","severity": "ERROR"
}
```

 




