sw1(0/0) <===(vlan 172(172.16.0.0/20))===> (0/0)r1


sw
conf t
interface Ethernet 0/0
 switchport trunk encapsulation dot1q
 switchport mode trunk
 switchport trunk allowed vlan 

router
