## sw1(0/0) <===(vlan 172(172.16.0.0/20))===> (0/0)r1


### sw:
* #conf t
* #vlan 172
* #ip address 172.16.0.1 255.255.0.0
* #interface Ethernet 0/0
* #switchport trunk encapsulation dot1q
* #switchport mode trunk
* #switchport trunk allowed vlan 

### router:
* # interface Ethernet 0/0.172
* # encapsulation dot1q 2
* # ip address 172.16.0.1 255.255.0.0
