MAHMUDPUR-SW#show running-config
Building configuration...


Current configuration:
!
!version 2.9.0B build 81508
service timestamps log date
service timestamps debug date
service password-encryption
logging 192.168.254.13 notifications
logging buffered 409400
logging trap debugging
!
hostname MAHMUDPUR-SW
!
!
lldp run
!
!
!
!
!
spanning-tree mode rstp
spanning-tree rstp priority 61440
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
aaa accounting commands 0 default start-stop group tacacs+
aaa accounting commands 15 default start-stop group tacacs+
aaa accounting network default start-stop group tacacs+
!
localauthen aaa
!
localauthor full
 exec privilege default 8
!
username netx password 7 03205A42441D08036C13
username noc password 7 03204A0E6C4B4634 author-group full
!
!
!
!
interface Port-aggregator2
 description *****BD-NET-to-BKB*****
 aggregator-group load-balance both-ip
 switchport trunk vlan-allowed 2-4093
 switchport mode trunk
!
interface Port-aggregator3
 description ****Office-BDNET*****
 aggregator-group load-balance both-ip
 switchport mode trunk
!
interface Null0
!
interface GigaEthernet0/1
 switchport pvid 3039
!
interface GigaEthernet0/2
 shutdown
 spanning-tree bpduguard enable
 spanning-tree guard root
 switchport trunk vlan-allowed 200
 switchport mode trunk
!
interface GigaEthernet0/3
 shutdown
 switchport mode trunk
!
interface GigaEthernet0/4
 shutdown
 switchport mode trunk
!
interface GigaEthernet0/5
 shutdown
 switchport mode trunk
!
interface GigaEthernet0/6
 shutdown
 switchport mode trunk
!
interface GigaEthernet0/7
 shutdown
 switchport mode trunk
!
interface GigaEthernet0/8
 shutdown
 switchport mode trunk
!
interface GigaEthernet0/9
 shutdown
 switchport mode trunk
!
interface GigaEthernet0/10
 shutdown
 switchport mode trunk
!
interface GigaEthernet0/11
 shutdown
 switchport mode trunk
!
interface GigaEthernet0/12
 shutdown
 switchport mode trunk
!
interface GigaEthernet0/13
 shutdown
 switchport mode trunk
!
interface GigaEthernet0/14
 shutdown
 switchport mode trunk
!
interface GigaEthernet0/15
 shutdown
 switchport mode trunk
!
interface GigaEthernet0/16
 shutdown
 switchport mode trunk
!
interface GigaEthernet0/17
 shutdown
 switchport mode trunk
!
interface GigaEthernet0/18
 switchport trunk vlan-allowed 841-844
 switchport mode trunk
 duplex full
!
interface GigaEthernet0/19
 shutdown
 switchport mode trunk
!
interface GigaEthernet0/20
 switchport mode trunk
!
interface GigaEthernet0/21
 shutdown
!
interface GigaEthernet0/22
 description ***NET-LAND-Primary***
 switchport trunk vlan-allowed 1437,1456,1637,2037,2437,3437
 switchport trunk vlan-untagged none
 switchport mode trunk
!
interface GigaEthernet0/23
 description **Jitu-Network**
 switchport trunk vlan-allowed 1354,1496,1696,1754,2354,2496,2659,2771,3100
 switchport trunk vlan-allowed add 3354,3496
 switchport mode trunk
!
interface GigaEthernet0/24
 shutdown
 switchport mode trunk
!
interface TGigaEthernet0/1
 description ***Jhalkuri-UPLINK***
 switchport mode trunk
!
interface TGigaEthernet0/2
 description ***Spark-Link-SW***
 switchport trunk vlan-allowed 2-4094
 switchport mode trunk
!
interface TGigaEthernet0/3
 description **Signboard-UPL-LINK**
 spanning-tree cost 1
 switchport mode trunk
!
interface TGigaEthernet0/4
 description ***Zaker-NET***
 spanning-tree bpdufilter enable
 spanning-tree guard root
 switchport trunk vlan-allowed 1225,1445,1645,2445,2757,3445
 switchport mode trunk
!
interface VLAN3100
 ip address 172.16.100.10 255.255.255.0
 no ip directed-broadcast
!
!
!
vlan 1-4093
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
ip telnet attack-defense
!
ip http language english
ip http server
!
!
snmp-server community 0 Speed RO
!
radius-server host 192.168.254.11
radius-server key 7 03431F333E510A036A13
!
tacacs-server host 172.20.1.206
tacacs-server key 7 031F6741414A08036C13
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
MAHMUDPUR-SW#
