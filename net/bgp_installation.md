#Steps to bring up a demo cluster with routing capabilites:

![bgp](https://cloud.githubusercontent.com/assets/784144/12862804/17546052-cc24-11e5-9a17-277999761344.png)


##STEP 0 : Provision the host nodes with required services

Please follow the [prequesite] and [download] steps in the [demo installer] page. This would enable installation of all the required packages , versions of the binary that would be needed to bring up the contiv infrastrure services. At the end of these steps netplugin , netmaster would be started in routing mode. Once the prerequiste is completed please start the installer script. 

```
$chmod +x net_demo_installer
$./net_demo_installer -l 
```
The net_demo_installer will create a cfg.yaml template file on the first run. 

The [cfg.yaml] for the demo topology is as shown below.

```
CONNECTION_INFO:
      172.29.205.224:
        control: eth1
        data: eth7
      172.29.205.255:
        control: eth1
        data: eth6
```
Note: As shown in the topo diagram data interface should be the uplink interface and not the management interface of the server.

Rerun the installer after filling up the cfg.yaml. 
```
./net_demo_installer -l 
```
