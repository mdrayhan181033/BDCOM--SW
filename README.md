# BDCOM--SW

Signboard-SW#show running-config
Building configuration...


Current configuration:
!
!version 2.2.0D build 97625
service timestamps log date
service timestamps debug date
service password-encryption
logging 192.168.254.13
logging buffered 409400
!
hostname Signboard-SW
!
!
!
!
!
spanning-tree mode rstp
spanning-tree rstp priority 61440
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
aaa authorization commands 0 default group tacacs+
aaa authorization commands 15 default group tacacs+
aaa authorization exec default group tacacs+ local
aaa accounting commands 15 default start-stop group tacacs+
aaa accounting commands 0 default start-stop group tacacs+
aaa accounting network default start-stop group tacacs+
!
localauthor full
 exec privilege default 8
!
username netx password 7 142f222f591413691110
username noc author-group full password 7 142f127a0242511b
!
!
!
!
!
!
interface Port-aggregator1
 description ***CTG-Road-SW***
 spanning-tree cost 65535
 switchport mode trunk
!
interface Port-aggregator2
 description ***F@H-UG-Link***
 switchport mode trunk
!
interface Port-aggregator4
 description ***Skylink-Bundle***
 spanning-tree bpduguard enable
 spanning-tree guard root
 switchport trunk vlan-allowed 1,1051,1161,1935-1936,2051,2161,3051,3161
 switchport mode trunk
!
interface Null0
!
interface Tunnel1
 no ip address
 no ip directed-broadcast
!
interface GigaEthernet0/0
 no ip address
!
interface TGigaEthernet0/1
 description ***F@H-UG-Link***
 aggregator-group 2 mode lacp
 switchport mode trunk
!
interface TGigaEthernet0/2
 shutdown
!
interface TGigaEthernet0/3
 shutdown
!
interface TGigaEthernet0/4
 shutdown
!
interface TGigaEthernet0/5
 description **Zara-Communication-BKP**
 switchport trunk vlan-allowed 1339,1739,2339,2739,3339
 switchport mode trunk
!
interface TGigaEthernet0/6
 description ***Bhuighor-Akash***
 spanning-tree bpduguard enable
 spanning-tree guard root
 switchport trunk vlan-allowed 1201,1301,1401,1501
 switchport mode trunk
!
interface TGigaEthernet0/7
 shutdown
!
interface TGigaEthernet0/8
 description **Super-Zone**
 switchport trunk vlan-allowed 31-4094
 switchport mode trunk
 switchport pvid 21
!
interface TGigaEthernet0/9
 description **MAHMUDPUR-POP**
 switchport mode trunk
!
interface TGigaEthernet0/10
 description ***Pulok-Bhuighor***
 no spanning-tree
 switchport trunk vlan-allowed 1258,1756,2104,2657-2658,2758,3098
 switchport mode trunk
 switchport port-security dynamic maximum 15
!
interface TGigaEthernet0/11
 shutdown
!
interface TGigaEthernet0/12
 shutdown
!
interface TGigaEthernet0/13
 description ***Shuvash-Broadband***
 switchport trunk vlan-allowed 1415,1615,2415,2756,3415
 switchport mode trunk
!
interface TGigaEthernet0/14
 description ***JItu-Network**
 switchport mode trunk
!
interface TGigaEthernet0/15
 description ***Zaker-Net***
 switchport trunk vlan-allowed 1042,1835,2042,2751,2757,3042
 switchport mode trunk
!
interface TGigaEthernet0/16
 description ***Appyon-Online**
 switchport trunk vlan-allowed 1,1026,1824,2026,2692,3026
 switchport mode trunk
!
interface TGigaEthernet0/17
 shutdown
!
interface TGigaEthernet0/18
 description ****Sonali-Ash***
 no spanning-tree
 switchport mode trunk
 switchport pvid 1096
!
interface TGigaEthernet0/19
 shutdown
 switchport trunk vlan-allowed 1281,1992,2281,2743,3281
 switchport mode trunk
!
interface TGigaEthernet0/20
 shutdown
!
interface TGigaEthernet0/21
 shutdown
!
interface TGigaEthernet0/22
 shutdown
 description ***FSN-SW-Link***
 spanning-tree cost 65535
 switchport trunk vlan-allowed 160,1024,1027,1274,1852,1856,1981,2024,2027
 switchport trunk vlan-allowed add 2274,3010,3027,3101,3309
 switchport mode trunk
!
interface TGigaEthernet0/23
 description ***Green-Touch***
 switchport trunk vlan-allowed 1281,1992,2281,2743,3281
 switchport mode trunk
!
interface TGigaEthernet0/24
 description ***ABCD-Online****
 switchport trunk vlan-allowed 1031,1033,1467,1667,1885,2031,2467,2720,3031
 switchport mode trunk
!
interface CGigaEthernet0/1
 description ****Kazla***
 spanning-tree cost 1
 switchport mode trunk
!
interface CGigaEthernet0/2
 shutdown
!
interface CGigaEthernet0/3
 description ***Jhalkuri-SW***
 switchport mode trunk
!
interface CGigaEthernet0/4
 shutdown
!
interface VLAN3100
 ip address 172.16.100.30 255.255.255.0
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
ip route default 172.16.100.1
ip exf
!
ipv6 exf
!
!
!
!
!
ip http language english
ip http server
!
!
snmp-server community 0 Speed RO
!
radius-server host 192.168.254.11
radius-server key 7 14526620534815690f10
!
tacacs-server host 172.20.1.206
tacacs-server key 7 142e2f2e564113691110
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

