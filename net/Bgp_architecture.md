 
#What does L3 capabilty facilitate in a Contiv container infrastructure ?

-  Enable communication between containers on different hosts natively using vlan encap 
-  Enables communication between containers and non containers 
-  Provides capability for uplink TOR's/Leaf switches to learn containers deployed in the fabric

#What are the recommended topologies ?

![topo](https://cloud.githubusercontent.com/assets/784144/12862973/26d1136c-cc25-11e5-9451-a266ea033b5e.png)


#Typical worklow:
- Configure Bgp on the Leaf switches Leaf 1 and Leaf 2 
- Bring up Contiv – netplugin and netmaster
- Create a Vlan network with subnet pool and gateway
- Add Bgp configuration on the host, to peer with the uplink leaf
- Bring up containers in the networks created on the host

#What are the supported configurations

- Ensure that BGP peering between the host server and the leaf switch is eBGP
- Currently only one uplink from the server is supported
- Currently supported on bare-metals (watch this space for support on VMs soon)

#Supported version

This document would be applicable starting from the following version:

```
Version: v0.1-02-06-2016.14-42-05.UTC
GitCommit: 392e0a7
BuildTime: 02-06-2016.14-42-05.UTC
```
