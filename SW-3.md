Stafquater-SW#      show running-config
Building configuration...


Current configuration:
!
!version 2.2.0C build 113955
service timestamps log date
service timestamps debug date
service password-encryption
logging 172.16.180.34 informational
logging 11.11.11.34 informational
logging buffered 409400
logging trap debugging
!
hostname Stafquater-SW
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
spanning-tree rstp priority 40960
!
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
aaa authentication login default group tacacs+ local
aaa authentication enable default none
aaa authorization commands 15 default group tacacs+
aaa authorization commands 0 default group tacacs+
aaa authorization exec default group tacacs+ local
aaa accounting commands 0 default start-stop group tacacs+
aaa accounting commands 15 default start-stop group tacacs+
aaa accounting network default start-stop group tacacs+
!
localauthor full
 exec privilege default 8
!
username netx password 7 112d0343592f6b130716
username noc author-group full password 7 112d720f025d2a44
!
!
!
!
!
!
interface Port-aggregator1
 description ***Brovanga-SW***
 spanning-tree cost 1
 switchport mode trunk
!
interface Port-aggregator2
 description ***Tarabo-SW***
 spanning-tree cost 65535
 switchport trunk vlan-allowed 30-4094
 switchport mode trunk
!
interface Null0
!
interface GigaEthernet0/1
 description ***X-Press-412***
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
!
interface GigaEthernet0/2
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
!
interface GigaEthernet0/3
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
!
interface GigaEthernet0/4
 switchport trunk vlan-allowed 1435,1635
 switchport mode trunk
!
interface GigaEthernet0/5
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
!
interface GigaEthernet0/6
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
!
interface GigaEthernet0/7
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
!
interface GigaEthernet0/8
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
!
interface GigaEthernet0/9
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
!
interface GigaEthernet0/10
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
!
interface GigaEthernet0/11
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
!
interface GigaEthernet0/12
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
!
interface GigaEthernet0/13
 shutdown
 switchport trunk vlan-allowed 1078,1822,2078,3078
 switchport mode trunk
!
interface GigaEthernet0/14
 shutdown
 switchport trunk vlan-allowed 1095,1895,2095,2704,3095
 switchport mode trunk
 no fiber-auto-config
!
interface GigaEthernet0/15
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
!
interface GigaEthernet0/16
 switchport trunk vlan-allowed 1213,1480,1680,1919,2213,2480
 switchport mode trunk
!
interface GigaEthernet0/17
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
!
interface GigaEthernet0/18
 switchport mode trunk
!
interface GigaEthernet0/19
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
!
interface GigaEthernet0/20
 switchport mode trunk
!
interface GigaEthernet0/21
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
!
interface GigaEthernet0/22
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
!
interface GigaEthernet0/23
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
!
interface GigaEthernet0/24
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
!
interface GigaEthernet0/25
!
interface GigaEthernet0/26
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
!
interface GigaEthernet0/27
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
!
interface GigaEthernet0/28
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
!
interface GigaEthernet0/29
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
!
interface GigaEthernet0/30
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
!
interface GigaEthernet0/31
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
!
interface GigaEthernet0/32
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
!
interface GigaEthernet0/33
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
!
interface GigaEthernet0/34
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
!
interface GigaEthernet0/35
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
!
interface GigaEthernet0/36
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
!
interface GigaEthernet0/37
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
!
interface GigaEthernet0/38
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
!
interface GigaEthernet0/39
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
!
interface GigaEthernet0/40
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
!
interface GigaEthernet0/41
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
!
interface GigaEthernet0/42
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
!
interface GigaEthernet0/43
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
!
interface GigaEthernet0/44
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
!
interface GigaEthernet0/45
 shutdown
!
interface GigaEthernet0/46
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
!
interface GigaEthernet0/47
 shutdown
!
interface GigaEthernet0/48
 shutdown
!
interface TGigaEthernet1/1
 description ***Brovanga-SW***
 aggregator-group 1 mode lacp
 switchport mode trunk
!
interface TGigaEthernet1/2
 description ***Brovanga-SW***
 aggregator-group 1 mode lacp
 switchport mode trunk
!
interface TGigaEthernet1/3
 description ***Nurjahan-Cable***
 switchport mode trunk
!
interface TGigaEthernet1/4
 description ***Ether-Tech***
 switchport mode trunk
!
interface TGigaEthernet1/5
 description ***Ramisa-Online***
 switchport mode trunk
!
interface TGigaEthernet1/6
 description ***Freedom-online-BKP***
 switchport trunk vlan-allowed 1250,1455,1784,2322,2621,3322
 switchport mode trunk
 switchport pvid 22
 switchport port-security dynamic maximum 15
!
interface TGigaEthernet1/7
 description ***Tarabo-SW***
 aggregator-group 2 mode lacp
 switchport trunk vlan-allowed 30-4094
 switchport mode trunk
!
interface TGigaEthernet1/8
 description ***Tarabo-SW***
 aggregator-group 2 mode lacp
 switchport trunk vlan-allowed 30-4094
 switchport mode trunk
!
interface VLAN3992
 ip address 172.16.186.6 255.255.255.0
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
!
snmp-server community 0 Speed RO
!
radius-server host 192.168.254.11
radius-server key 7 1150473453636d130516
!
tacacs-server host 172.20.1.206
tacacs-server key 7 112c1042565c6b130716
!
line vty 0 6
 exec-timeout 0
 login authorization radius
!
line vty 7 31
 exec-timeout 0
!
!
time-zone tz 6 0
ntp server 183.177.72.201
!
!
!Pending configurations for absent linecards:
!
!Pending configurations for global:
!
ddm enable
!
interface Port-aggregator1
aggregator-group mode lacp
!
!
interface Port-aggregator2
aggregator-group mode lacp
!
!
interface TGigaEthernet1/1
aggregator-group 1
!
!
interface TGigaEthernet1/2
aggregator-group 1
!
!
interface TGigaEthernet1/3
aggregator-group 2
!
!
interface TGigaEthernet1/4
aggregator-group 2
!
!
interface TGigaEthernet1/6
aggregator-group 1
!
!
interface TGigaEthernet1/7
aggregator-group 2
!
!

Stafquater-SW#


