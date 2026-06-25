# Lab overview
This lab demonstrates the configuration of VLANs, trunk ports, and inter-VLAN routing using Router-on-a-Stick (ROAS). Multiple switches are connected through trunk links, while a router is used to enable communication between different VLANs.

## Topology includes
- 1 Router
- 3 Switches
- 10 PCs
- 1 LAN
- 3 VLANs


## IP Addressing Table
| LAN   | Network         | First usable address | Last usable address | Broadcast    | Name |
| ----- | --------------- | -------------------- | ------------------- | ------------ | ----- |
| LAN 1 | 192.168.0.0/26  | 192.168.0.1          | 192.168.0.62        | 192.168.0.63 | - |
| VLAN 10 | 192.168.0.0/28  | 192.168.0.1          | 192.168.0.14        | 192.168.0.15 | IT  |
| VLAN 20 | 192.168.0.16/28 | 192.168.0.17         | 192.168.0.30        | 192.168.0.31 | PRODUCTION |
| VLAN 30 | 192.168.0.32/28 | 192.168.0.33         | 192.168.0.46        | 192.168.0.47 | OFFICE |