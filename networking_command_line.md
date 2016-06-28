
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
    ```netctl policy``` command is used for policy manipulation like create, delete list,inspect , add rule , delete rule and list rules for the policy
    
    ```netctl policy create``` is used to create a new policy to which rule manipulations can be 
    
    ```netctl policy rm``` is used to delete a policy
    ```netctl policy ls``` is used to list all the policies
    ``` netctl rule-ls``` is used to list all the rules attached to a policy
    ``` netctl rule-rm``` is used to remove a rule attached to a policy
    ``` netctl rule-add``` is used to add a rule to a policy alone with the following supported options
		```--priority, -p```  Priority Indicator . Default: 1
		```--direction, -d``` Direction of traffic (in/out).Default: in
		```--from-group, -g``` From Endpoint Group Name (Valid in incoming direction only)
		```--to-group, -e```   To Endpoint Group Name (Valid in outgoing direction only)
		```--from-network, -n``` From Network name (Valid in incoming direction only)
		```--to-network, -o``` To Network name (Valid in outgoing direction only)
		```--from-ip-address, -i``` From IP address/CIDR (Valid in incoming direction only)
		```--to-ip-address, -s``` To IP address/CIDR (Valid in outgoing direction only)
		```--protocol, -l``` Protocol (e.g., tcp, udp, icmp)
		```--port, -P``` Port
		```--action, -j``` Action to take (allow or deny).Default:allow
		


    


