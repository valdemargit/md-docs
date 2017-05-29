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
* #
R1(config)# interface fa0/0.2
R1(config-subif)# encapsulation dot1q 2
R1(config-subif)# ip address 10.0.2.1 255.255.255.0
