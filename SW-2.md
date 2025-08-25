BDNET#  show running-config
Building configuration...


Current configuration:
!
!version 2.2.0D build 101032
service timestamps log date
service timestamps debug date
service password-encryption
logging buffered 409400
!
hostname BDNET
!
!
lldp run
!
!
!
!
spanning-tree mode rstp
spanning-tree rstp priority 40960
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
aaa accounting commands 0 default start-stop group tacacs+
aaa accounting commands 15 default start-stop group tacacs+
aaa accounting network default start-stop group tacacs+
!
localauthor full
 exec privilege default 8
!
username netx author-group full password 7 0212051c460c0e09046d
username noc author-group full password 7 0232410b
!
!
!
!
!
!
interface Port-aggregator1
 switchport mode trunk
!
interface Port-aggregator2
 switchport mode trunk
!
interface Null0
!
interface GigaEthernet0/0
 no ip address
!
interface TGigaEthernet0/1
 aggregator-group 1 mode lacp
 switchport mode trunk
!
interface TGigaEthernet0/2
 shutdown
!
interface TGigaEthernet0/3
 shutdown
 aggregator-group 2 mode lacp
 switchport trunk vlan-allowed 1,1105,1880,2105,3105
 switchport mode trunk
 no fiber-auto-config
!
interface TGigaEthernet0/4
 shutdown
 aggregator-group 2 mode lacp
 switchport mode trunk
!
interface TGigaEthernet0/5
 shutdown
 switchport mode trunk
!
interface TGigaEthernet0/6
 shutdown
 switchport mode trunk
!
interface TGigaEthernet0/7
 description **BDNET_MKT**
 switchport trunk vlan-allowed 1,1105,1880,2105,2501-2503,3105
 switchport mode trunk
 switchport pvid 16
 no fiber-auto-config
!
interface TGigaEthernet0/8
 shutdown
!
interface TGigaEthernet0/9
 shutdown
 switchport mode trunk
!
interface TGigaEthernet0/10
 shutdown
 switchport trunk vlan-allowed 1060,1062,1221,1359,1948,1950,2193,2421,2618
 switchport trunk vlan-allowed add 2742,2750,3104,3243
 switchport mode trunk
 switchport port-security dynamic maximum 40
!
interface TGigaEthernet0/11
 description ***Zazira-Online***
 spanning-tree bpduguard enable
 spanning-tree guard root
 switchport trunk vlan-allowed 1451,1651,2451,2747,2780,3451
 switchport mode trunk
 switchport pvid 10
!
interface TGigaEthernet0/12
 shutdown
 switchport mode trunk
 no fiber-auto-config
!
interface TGigaEthernet0/13
 shutdown
 switchport trunk vlan-allowed 1,1105,1880,2105,3105
 switchport mode trunk
 no fiber-auto-config
 speed 1000
 duplex auto
!
interface TGigaEthernet0/14
 shutdown
 no fiber-auto-config
!
interface TGigaEthernet0/15
 shutdown
!
interface TGigaEthernet0/16
 shutdown
!
interface TGigaEthernet0/17
 shutdown
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
 shutdown
!
interface TGigaEthernet0/21
 shutdown
 switchport mode trunk
!
interface TGigaEthernet0/22
 description ***Spark-link-Bkp***
 spanning-tree bpdufilter enable
 spanning-tree bpduguard enable
 spanning-tree guard root
 switchport trunk vlan-allowed 1176,1876,2176,2627,3176
 switchport mode trunk
 switchport pvid 15
!
interface TGigaEthernet0/23
 shutdown
 switchport mode trunk
!
interface TGigaEthernet0/24
 shutdown
 switchport mode trunk
!
interface CGigaEthernet0/1
!
interface CGigaEthernet0/2
 description ***Advance-2-Uplink***
 switchport trunk vlan-allowed 31-4094
 switchport mode trunk
!
interface CGigaEthernet0/3
 description ***Kazla-UPLINK***
 spanning-tree cost 1
 switchport trunk vlan-allowed 31-4094
 switchport mode trunk
!
interface CGigaEthernet0/4
 description ***MS-Universal***
 switchport trunk vlan-allowed 2-4093
 switchport mode trunk
!
interface VLAN3071
 no ip address
 no ip directed-broadcast
!
interface VLAN3072
 no ip address
 no ip directed-broadcast
!
interface VLAN3992
 ip address 172.16.186.15 255.255.255.0
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
!
ip http language english
ip http server
!
!
snmp-server community 0 Speed RO
!
radius-server host 192.168.254.11
radius-server key 7 0235490d40401009026d
!
tacacs-server host 172.20.1.206
tacacs-server key 7 0211121b43390e09046d
!
line vty 0 6
 login authorization radius
!
!
time-zone tz 6 0
ntp server 183.177.72.201
ntp server 10.11.1.26
ntp peer 10.11.1.26
ntp client enable
!
!
!
!
!Pending configurations for absent linecards:
!
!No configurations pending global
BDNET#
