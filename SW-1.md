Advance-2-100G#show running-config
Building configuration...


Current configuration:
!
!version 2.2.0D build 124674
service timestamps log date
service timestamps debug date
service password-encryption
logging buffered 409400
logging monitor informational
!
hostname Advance-2-100G
!
!
!
!
!
!
!
!
spanning-tree mode rstp
spanning-tree rstp priority 57344
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
aaa authentication login default group tacacs+ local
aaa authentication enable default none
aaa authorization commands 15 default group tacacs+
aaa authorization commands 0 default group tacacs+
aaa authorization exec default group tacacs+ local
aaa accounting commands 15 default start-stop group tacacs+
aaa accounting commands 0 default start-stop group tacacs+
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
 description ***Borovanga-group***
 spanning-tree cost 65535
 switchport mode trunk
!
interface Port-aggregator3
 description ***F@H-Bundle***
 spanning-tree bpduguard enable
 spanning-tree guard root
 switchport mode trunk
!
interface Port-aggregator4
 description ***Tarabo-SW***
 switchport mode trunk
!
interface Port-aggregator5
 description ***MS-Universal***
 switchport mode trunk
!
interface Null0
!
interface GigaEthernet0/0
 no ip address
!
interface TGigaEthernet0/1
 shutdown
 description ***Borovanga-Link***
 aggregator-group 1 mode lacp
 switchport mode trunk
!
interface TGigaEthernet0/2
 shutdown
 description ***Borovanga-Link***
 aggregator-group 1 mode lacp
 switchport mode trunk
!
interface TGigaEthernet0/3
 shutdown
!
interface TGigaEthernet0/4
 shutdown
!
interface TGigaEthernet0/5
 description ***BDNET-AShik***
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
!
interface TGigaEthernet0/6
 description ***ZARA-Communication***
 switchport trunk vlan-allowed 1338,1738,2338,2738,3338
 switchport mode trunk
!
interface TGigaEthernet0/7
 shutdown
 switchport mode trunk
!
interface TGigaEthernet0/8
 shutdown
 switchport mode trunk
!
interface TGigaEthernet0/9
 shutdown
 switchport mode trunk
!
interface TGigaEthernet0/10
 description ***Advance-MKT***
 spanning-tree bpdufilter enable
 switchport mode trunk
!
interface TGigaEthernet0/11
 description ***Shanarper-Cyber-Net***
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
!
interface TGigaEthernet0/12
 shutdown
 switchport mode trunk
!
interface TGigaEthernet0/13
 description ***Tarabo-Link***
 aggregator-group 4 mode lacp
 switchport mode trunk
!
interface TGigaEthernet0/14
 description ***Tarabo-Link***
 aggregator-group 4 mode lacp
 switchport mode trunk
!
interface TGigaEthernet0/15
 description ***Munnta-DATA-Link***
 switchport trunk vlan-allowed 470-473
 switchport mode trunk
!
interface TGigaEthernet0/16
 shutdown
 switchport mode trunk
!
interface TGigaEthernet0/17
 shutdown
 switchport mode trunk
!
interface TGigaEthernet0/18
 shutdown
 switchport mode trunk
!
interface TGigaEthernet0/19
 shutdown
 switchport mode trunk
!
interface TGigaEthernet0/20
 description ***NYG-F@H-AGG***
 aggregator-group 3 mode lacp
 switchport trunk vlan-allowed 2
 switchport mode trunk
 switchport pvid 20
!
interface TGigaEthernet0/21
 shutdown
 switchport mode trunk
!
interface TGigaEthernet0/22
 description ***MS-Universal***
 aggregator-group 5 mode lacp
 switchport mode trunk
!
interface TGigaEthernet0/23
 description ***MS-Universal***
 aggregator-group 5 mode lacp
 switchport mode trunk
!
interface TGigaEthernet0/24
 shutdown
 switchport mode trunk
!
interface CGigaEthernet0/1
 description ***BDNET-UPLINK***
 spanning-tree cost 1
 switchport trunk vlan-allowed 31-4094
 switchport mode trunk
!
interface CGigaEthernet0/2
 spanning-tree cost 65535
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
!
interface CGigaEthernet0/3
 description **Borovanga-SW**
 spanning-tree cost 20000
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
!
interface CGigaEthernet0/4
 shutdown
 switchport mode trunk
!
interface VLAN3992
 ip address 172.16.186.42 255.255.255.0
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
radius-server host 192.168.254.11
radius-server key 7 1150473453636d130516
!
tacacs-server host 172.20.1.206
tacacs-server key 7 112c1042565c6b130716
!
line vty 0 6
 login authorization radius
!
!
time-zone tz 6 0
ntp server 183.177.72.201
!
!
!
!
!Pending configurations for absent linecards:
!
!No configurations pending global
Advance-2-100G#
