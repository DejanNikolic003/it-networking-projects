# Network Configuration
## Overview
- There are 1 LANs, 3 VLANs.
- LAN 1: 192.168.0.0/26
- VLAN 10: 192.168.0.0/28
- VLAN 20: 192.168.0.16/28
- VLAN 30: 192.168.0.32/28

## Router configuration
```
interface GigabitEthernet0/0
 no ip address
 duplex auto
 speed auto

interface GigabitEthernet0/0.10
 encapsulation dot1Q 10
 ip address 192.168.0.14 255.255.255.240

interface GigabitEthernet0/0.20
 encapsulation dot1Q 20
 ip address 192.168.0.30 255.255.255.240

interface GigabitEthernet0/0.30
 encapsulation dot1Q 30
 ip address 192.168.0.46 255.255.255.240

```
## Switch configuration
### SW1
```
interface FastEthernet0/1
 switchport access vlan 10
 switchport mode access

interface FastEthernet0/2
 switchport access vlan 10
 switchport mode access

interface FastEthernet0/3
 switchport access vlan 30
 switchport mode access

interface FastEthernet0/4
 switchport access vlan 30
 switchport mode access

interface FastEthernet0/5
 switchport access vlan 30
 switchport mode access

interface FastEthernet0/6
 switchport trunk native vlan 99
 switchport trunk allowed vlan 10,20
 switchport mode trunk

interface FastEthernet0/7
 switchport trunk native vlan 99
 switchport trunk allowed vlan 10,20,30
 switchport mode trunk

interface FastEthernet0/8
 switchport trunk native vlan 99
 switchport mode trunk
```
### SW2
```
interface FastEthernet0/1
 switchport access vlan 20
 switchport mode access

interface FastEthernet0/2
 switchport access vlan 20
 switchport mode access

interface FastEthernet0/3
 switchport access vlan 20
 switchport mode access

interface FastEthernet0/4
 switchport trunk native vlan 99
 switchport trunk allowed vlan 10,20
 switchport mode trunk
```
### SW3
```
interface FastEthernet0/1
 switchport access vlan 10
 switchport mode access

interface FastEthernet0/2
 switchport access vlan 10
 switchport mode access

interface FastEthernet0/3
 switchport trunk native vlan 99
 switchport trunk allowed vlan 10,20,30
 switchport mode trunk
```