Brovanga-SW#   show running-config
Building configuration...


Current configuration:
!
!version 2.2.0D build 124674
service timestamps log date
service timestamps debug date
!
hostname Brovanga-SW
!
!
!
lldp run
!
!
!
!
!
!
spanning-tree mode rstp
!
!
aggregator-group load-balance both-ip
!
!
!
!
!
!
!
!
!
!
!
!
!
!
aaa authentication login default local
aaa authentication enable default none
aaa authorization exec default local
!
username admin password 0 AllahMohan&1
username noc password 0 Noc@12345
username netx password 0 N3tx@1234
!
!
!
!
!
interface Port-aggregator1
 description ***Advance-SW***
 spanning-tree cost 65535
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
 switchport pvid 27
!
interface Port-aggregator2
 description ***Konapara-SW***
 spanning-tree cost 1
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
 switchport pvid 26
!
interface Port-aggregator3
 description ***Staff-quater-POP**
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
 switchport pvid 25
!
interface Null0
!
interface GigaEthernet0/0
 no ip address
!
interface TGigaEthernet0/1
 description ***Advance-SW***
 aggregator-group 1 mode lacp
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
 switchport pvid 27
!
interface TGigaEthernet0/2
 description ***Advance-SW***
 aggregator-group 1 mode lacp
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
 switchport pvid 27
!
interface TGigaEthernet0/3
 description ***Konapara-SW***
 aggregator-group 2 mode lacp
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
 switchport pvid 26
!
interface TGigaEthernet0/4
 description ***Konapara-SW***
 aggregator-group 2 mode lacp
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
 switchport pvid 26
!
interface TGigaEthernet0/5
 description ***Konapara-SW***
 aggregator-group 2 mode lacp
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
 switchport pvid 26
!
interface TGigaEthernet0/6
 description ***Staff-quater-POP**
 aggregator-group 3 mode lacp
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
 switchport pvid 25
!
interface TGigaEthernet0/7
 description ***Staff-quater-POP**
 aggregator-group 3 mode lacp
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
 switchport pvid 25
!
interface TGigaEthernet0/8
 description ***Green-Online***
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
!
interface TGigaEthernet0/9
 description ***Munna-Data-Link***
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
!
interface TGigaEthernet0/10
 description **Fair-Online-BKP***
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
!
interface TGigaEthernet0/11
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
!
interface TGigaEthernet0/12
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
!
interface TGigaEthernet0/13
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
!
interface TGigaEthernet0/14
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
!
interface TGigaEthernet0/15
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
!
interface TGigaEthernet0/16
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
!
interface TGigaEthernet0/17
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
!
interface TGigaEthernet0/18
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
!
interface TGigaEthernet0/19
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
!
interface TGigaEthernet0/20
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
!
interface TGigaEthernet0/21
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
!
interface TGigaEthernet0/22
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
!
interface TGigaEthernet0/23
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
!
interface TGigaEthernet0/24
 shutdown
!
interface CGigaEthernet0/1
 description ***Konapara-SW***
 spanning-tree cost 1
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
!
interface CGigaEthernet0/2
 shutdown
!
interface CGigaEthernet0/3
 description ***Advance-SW***
 spanning-tree cost 65535
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
!
interface CGigaEthernet0/4
 switchport mode trunk
!
interface VLAN1
 no ip address
 no ip directed-broadcast
!
interface VLAN3992
 ip address 172.16.186.4 255.255.255.0
 no ip directed-broadcast
!
!
!
vlan 1-4094
!
!
!
!
!
!
!
!
!
!
!
!
!
!
!
ip route default 172.16.186.1
ip exf
!
ipv6 exf
!
!
!
!
ip telnet attack-defense
ip telnet enable
!
ip http language english
ip http server
!
!
snmp-server community 0 Speed RO
!
!
!
!
!
!
!Pending configurations for absent linecards:
!
!No configurations pending global
Brovanga-SW#
