# Lab 01: Basic Networking and VLAN Configuration

## Overview

This lab focuses on fundamental networking concepts using Cisco Packet Tracer. It involves constructing a small office network, configuring network devices, segmenting a network using VLANs, and connecting separate VLAN networks through a router.

## Objectives

- Build a basic LAN using Cisco switches and PCs.
- Understand Ethernet connections and switch ports.
- Configure and understand VLAN segmentation.
- Separate departments into different logical networks.
- Connect VLAN networks to a router using separate physical interfaces.
- Test connectivity between network devices.

## Tools and Equipment

- Cisco Packet Tracer
- Cisco 2960 switches
- Cisco 1941 router
- PC end devices
- Ethernet cables

---

## Part 1: Small Office Network

### Network Topology

The first exercise involved a Cisco 2960 switch connected to four PCs.

The network was divided into two departments:

| Department | Device | Switch Port |
|---|---|---|
| Administration | PC1 | Fa0/1 |
| Administration | PC2 | Fa0/2 |
| IT Department | PC3 | Fa0/3 |
| IT Department | PC4 | Fa0/4 |

### IP Addressing

The initial LAN used the following addressing scheme:

| Device | IP Address | Subnet Mask |
|---|---|---|
| PC1 | 192.168.10.1 | 255.255.255.0 |
| PC2 | 192.168.10.2 | 255.255.255.0 |
| PC3 | 192.168.10.3 | 255.255.255.0 |
| PC4 | 192.168.10.4 | 255.255.255.0 |

### Connectivity Testing

Connectivity was tested using the `ping` command.

The first four PCs successfully communicated within the network.

---

## Part 2: VLAN Networks Connected to a Router

### Network Topology

The second exercise involved:

- One Cisco 2960 switch.
- One Cisco 1941 router.
- Two PCs.
- Two separate physical connections between the switch and router.

### Network Segmentation

The network was divided into two VLANs:

| VLAN | Department |
|---|---|
| VLAN 10 | Administration |
| VLAN 20 | IT Department |

Each VLAN was connected to a separate physical router interface through its corresponding switch port.

### Router Configuration

The router interfaces were configured with IP addresses belonging to their respective VLAN networks.

The router automatically learned the networks connected to its active, configured interfaces as directly connected routes.

This allowed the router to route traffic between the two VLAN networks.

### Key Concepts Practised

- VLAN creation and segmentation.
- Assigning switch ports to VLANs.
- Router physical interfaces.
- Directly connected routes.
- Inter-VLAN communication.
- Basic connectivity testing.

### Connectivity Testing

Ping tests were performed to verify communication across the network.

---

## Skills Developed

Through this exercise, I gained practical experience with:

- Basic LAN construction.
- IPv4 addressing.
- Subnet masks.
- Ethernet switching.
- VLAN segmentation.
- Cisco router configuration.
- Directly connected routes.
- Network connectivity testing.

## Technologies Used

- Cisco Packet Tracer
- Cisco IOS
- Ethernet
- IPv4
- VLANs

## Project Files

| File | Description |
|---|---|
| `README.md` | Lab documentation |
| `topology.png` | Packet Tracer network topology |
| `Lab-01.pkt` | Original Packet Tracer project |

## Learning Reflection

This lab provided practical exposure to building and configuring small office networks. It helped develop an understanding of how switches, VLANs, and routers work together to establish communication between network devices.

Further configuration details and verification screenshots will be added as the original Packet Tracer project is reviewed.
