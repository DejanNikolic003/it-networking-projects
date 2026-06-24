# Network Configuration
## Overview
- There are 3 LANs, 2 WANs.
- LAN 1: 192.168.0.0/28
- LAN 2: 192.168.0.16/28
- LAN 3: 192.168.0.32/28
- WAN 1: 192.168.0.48/30
- WAN 2: 192.168.0.52/30

## Router configuration
### R1 (LAN 1)
```
interface GigabitEthernet0/0
 ip address 192.168.0.53 255.255.255.252
 duplex auto
 speed auto

interface GigabitEthernet0/1
 ip address 192.168.0.14 255.255.255.240
 duplex auto
 speed auto

ip route 192.168.0.32 255.255.255.240 GigabitEthernet0/0 ** Static route to LAN 3 **
ip route 192.168.0.16 255.255.255.240 GigabitEthernet0/0 ** Static route to LAN 2 **
```
### R2 (LAN 2)
```
interface GigabitEthernet0/0
 ip address 192.168.0.30 255.255.255.240
 duplex auto
 speed auto

interface GigabitEthernet0/1
 ip address 192.168.0.49 255.255.255.252
 duplex auto
 speed auto

interface GigabitEthernet0/2
 ip address 192.168.0.54 255.255.255.252
 duplex auto
 speed auto

ip route 192.168.0.0 255.255.255.240 GigabitEthernet0/2 ** Static route to LAN 1 **
ip route 192.168.0.32 255.255.255.240 GigabitEthernet0/1 ** Static route to LAN 3 **
```
### R2 (LAN 3)
```
interface GigabitEthernet0/0
 ip address 192.168.0.50 255.255.255.252
 duplex auto
 speed auto

interface GigabitEthernet0/1
 ip address 192.168.0.46 255.255.255.240
 duplex auto
 speed auto

ip route 192.168.0.0 255.255.255.240 GigabitEthernet0/0 ** Static route to LAN 1 **
ip route 192.168.0.16 255.255.255.240 GigabitEthernet0/0 ** Static route to LAN 2 **
```