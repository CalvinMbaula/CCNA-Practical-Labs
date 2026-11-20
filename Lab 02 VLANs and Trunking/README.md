# Lab 02: VLANs and Trunking

## Overview

This lab focuses on Virtual Local Area Networks (VLANs), switch port configuration, and trunk links using Cisco Packet Tracer.

The exercise involved creating separate VLANs, assigning PCs to their respective VLANs, connecting two switches, and configuring trunk links to allow communication between devices belonging to the same VLAN across different switches.

## Objectives

- Understand VLANs and network segmentation.
- Create and name VLANs on Cisco switches.
- Assign switch ports to specific VLANs.
- Understand the difference between access ports and trunk ports.
- Configure trunk links between switches.
- Test connectivity between devices in the same and different VLANs.

## Tools and Equipment

- Cisco Packet Tracer
- 2 Cisco 2960 switches
- 4 PCs
- Ethernet cables (copper straight-through)

## Network Topology

The network consisted of two Cisco 2960 switches connected through a trunk link.

Each switch had two PCs connected to it.

The network was divided into two VLANs:

| VLAN ID | VLAN Name | Department |
|---|---|---|
| 10 | ADMIN | Administration |
| 20 | IT | IT Department |

## Part 1: VLAN Creation

Created two VLANs on the first switch.

### Commands Used

```cisco
enable
configure terminal

vlan 10
name ADMIN

vlan 20
name IT

end
```

The same VLANs were also created on the second switch.

## Part 2: Assigning Switch Ports

Configured access ports to assign connected PCs to their respective VLANs.

### First Switch Configuration

PC0 was connected to FastEthernet0/1 and assigned to VLAN 10.

PC1 was connected to FastEthernet0/2 and assigned to VLAN 20.

### Commands Used

```cisco
enable
configure terminal

interface fastEthernet 0/1
switchport mode access
switchport access vlan 10

interface fastEthernet 0/2
switchport mode access
switchport access vlan 20

end
```

## Part 3: Trunk Configuration

Connected the two switches using FastEthernet0/3 on both switches.

Configured the switch-to-switch connections as trunk ports.

### Commands Used

```cisco
enable
configure terminal

interface fastEthernet 0/24
switchport mode trunk

end
```

The same configuration was applied to the second switch.

Trunk links allow traffic belonging to multiple VLANs to travel through a single physical connection.

## Part 4: Verification and Connectivity Testing

Used the following commands to verify the configurations:

### Verify VLANs

```cisco
show vlan brief
```

### Verify Trunk Links

```cisco
show interfaces trunk
```

### Connectivity Testing

Ping tests were performed between PCs connected to different switches.

**Results:**

- Devices belonging to VLAN 10 successfully communicated across the two switches.
- Devices belonging to VLAN 20 successfully communicated across the two switches.
- Communication between VLAN 10 and VLAN 20 failed because inter-VLAN routing had not been configured.

## Key Concepts Learned

| Concept | Description |
|---|---|
| VLAN | Logically separates a network into different broadcast domains. |
| Access Port | Connects an end device to a specific VLAN. |
| Trunk Port | Carries traffic belonging to multiple VLANs. |
| VLAN Segmentation | Separates devices into logical networks. |
| Inter-VLAN Routing | Allows communication between different VLANs through a router or Layer 3 switch. |

## Skills Developed

- Creating and naming VLANs.
- Configuring switch access ports.
- Configuring trunk links.
- Connecting multiple switches.
- Verifying VLAN and trunk configurations.
- Testing network connectivity.
- Understanding network segmentation and VLAN isolation.

## Technologies Used

- Cisco Packet Tracer
- Cisco IOS CLI
- Ethernet
- VLANs
- IEEE 802.1Q trunking

## Project Files

| File | Description |
|---|---|
| README.md | Lab documentation |
| topology.png | Screenshot of the network topology |
| VLAN-Trunking.pkt | Packet Tracer project file |

## Learning Reflection

This lab provided practical experience with VLAN configuration and trunking.

It demonstrated how multiple logical networks can exist across different physical switches while maintaining separation between VLANs.

It also introduced the importance of trunk links in larger switched networks and the role of inter-VLAN routing in enabling communication between separate VLANs.
