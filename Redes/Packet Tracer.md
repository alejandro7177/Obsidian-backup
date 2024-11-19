## DHCP(router)

```
ip dhcp pool default
```

network \<ip> \<mask>  
```
network 192.168.0.0 255.255.255.0
```

default-router \<ip>
```
default-router 192.168.0.1
```

dns-server \<ip>
```
dns-server 192.168.99.10
```

ip dhcp excluded-address \<ip> \<ip>
```
ip dhcp excluded-address 192.168.0.1 192.168.0.10
```

## OSPF
```
router ospf 1
```

network \<ip> \<wildcard> area \<num_area>
```
network 192.168.99.0 0.0.0.255 area 0
```

## BGP
```
router bgp 20001 
```

```(config-router)
network 172.16.1.0 mask 255.255.255.0
```

Le decimos a que red conoce
```Router
neighbor 200.45.54.2 remote-as 20001
```

## OSPF + BGP(una vez ambos cofig)
```Router
router ospf 1
```

```
redistribute bgp 10001 subnets
```

## VLAN-VTP

Configurar servidor VLAN (switch)
```
vtp mode server
vtp domain redes.edu
vtp password pass1234
```

Definir VLAN (switch)
```
vlan 10 
name datacenter 
Vlan 50 
Name administracion 
Vlan 100 
Name gerencia 
Vlan 200 
Name invitados 
Vlan 300 
Name infraestructura 
Vlan 400 
Name sistemas 
Vlan 500 
Name deposito
Vlan 600 
Name test
```

Configurar gateway's VLAN (router)
gateway (xxx.xxx.xxx.1 o xxx.xxx.xxx.254)
```
interface GigabitEthernet0/0.20
encapsulation dot1Q 20
ip address 10.40.16.254 255.255.255.0 
```

***Opcional*** DHCP VLAN
```
ip dhcp pool red20
network 10.40.16.0 255.255.255.0
default-router 10.40.16.254
ip dhcp excluded-address 10.40.16.254
```

Configuración Switches Clientes (switch)
```
vtp mode client
vtp domain redes.edu
vtp password pass1234
```

## Linux
```
sudo mount 192.168.200.68:/nfs/csv /mnt/nfs-cliente
```






