# Network Configuration
## Overview
All PCs are in the same LAN network: **10.1.1.0/24**
- Subnet Mask: 255.255.255.0
- Default gateway: Not configured

---

## PC Configuration
### PC1
- IP Address: 10.1.1.1
- Subnet Mask: 255.255.255.0

### PC2
- IP Address: 10.1.1.2
- Subnet Mask: 255.255.255.0

### PC3
- IP Address: 10.1.1.3
- Subnet Mask: 255.255.255.0

### PC4
- IP Address: 10.1.1.4
- Subnet Mask: 255.255.255.0

---

## Switch Configuration
### VLAN Creation
``` 
vlan 10
name IT
```
```
vlan 20
name FINANCE
```
### Access ports VLAN 10
```
interface FastEthernet0/1
 switchport mode access
 switchport access vlan 10

interface FastEthernet0/2
 switchport mode access
 switchport access vlan 10
```
### Access ports VLAN 20
```
interface FastEthernet0/3
 switchport mode access
 switchport access vlan 20

interface FastEthernet0/4
 switchport mode access
 switchport access vlan 20

```