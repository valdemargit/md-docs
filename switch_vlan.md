### create vlan 2:
* #show vlan brief
* #show interfaces trunk
* #conf t
* #vlan 2
* #name 172.16.2.0/20
* #exit
* #exit
* #show vlan brief
* #show interfaces trunk

### range trunk
* #conf t
* #interface range Ethernet 2/0-3
* #switchport trunk encapsulation dot1q
* #switchport mode trunk
* #switchport access vlan 2
* #exit
* #exit
* #show vlan brief
* #show interfaces trunk

### ip
* #conf t
* #interface vlan 2
* #ip address 172.16.2.1 255.255.0.0
* #no shutdown
* #show ip interface brief
