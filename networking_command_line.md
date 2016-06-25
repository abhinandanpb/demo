
#Network Manipulation 
 ```netctl network ``` command is used for network manipulation like create , delete , inspect , list
 
 ```netctl network create``` is used to create a network with the following supported options
 
    --nw-type,-n Network Type. Accepted values:infra or data. Default:vlan
    
    ```--encap, -e```  Network Encap type Accepted values:vlan or vxlan. Default:vxlan
    
		```--pkt-tag, -p``` Network Packet tag. Optional parameter.
		
		```--subnet, -s``` Network subnet. CIDR notation - x.x.x.x/24
		
		```--gateway, -g"``` Default network gateway

	  ```--subnetv6,-s6``` Network IPv6 Subnet. CIDR notation xxxx::xx/64"

		```--gatewayv6, -g6``` Default ipv6 network gateway
		
		```--tenant, -t``` tenant to attach the network. Default:"default"
		
	``` netctl network delete``` is used to delete a network with the following supported options
	    	```--tenant, -t``` tenant to which network was attached. Default:"default"
 
  ``` netctl network list``` is used to list the networks attached to a tenant with the following supported options
           ```--tenant, -t``` tenant to which network was attached. Default:"default"
  
  ``` netctl network inspect``` is used to inspect operational state of a  network and the endpoints attached to it 
          ```--tenant, -t``` tenant to which network was attached. Default:"default"
          
#Tenant Manipulation
    ```netctl tenant``` command is used for tenant manipulation like create, delete, list and inspect.
    ```netctl tenant create``` is used to create a tenant 
    ```netctl tenant delete``` is used to delete a tenant 
    ```netctl tenant list```   is used to list all tenants in the cluster
    ```netctl tenant inspect```is used to inspect a tenant.

#Policy Manipulation
    ```netctl policy``` command is used for policy manipulation like create, delete list and inspect
    


