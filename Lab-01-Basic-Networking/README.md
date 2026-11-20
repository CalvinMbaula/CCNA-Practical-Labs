# Lab 01: Basic Networking and Routing

## Objectives

- Build a basic network using PCs, switches, and a router.
- Configure IP addressing on end devices.
- Understand VLAN segmentation.
- Connect separate VLANs to a router using physical interfaces.
- Test network connectivity using "ping".

## Part 1: Basic LAN Configuration

### Topology:

- 1 Cisco 2960 switch
- 4 PCs
- Straight-through Ethernet cables

### IP Addressing:

Device| IP Address| Subnet Mask
PC1| 192.168.10.1| 255.255.255.0
PC2| 192.168.10.2| 255.255.255.0
PC3| 192.168.10.3| 255.255.255.0
PC4| 192.168.10.4| 255.255.255.0

### Testing:

Connectivity was tested using the "ping" command. All four PCs successfully communicated within the network.

## Part 2: VLANs and Router Connectivity

### Topology:

- 2 PCs
- 1 Cisco switch
- 1 router
- Two separate physical connections between the switch and router

### Configuration Overview:

The switch was configured with two separate VLANs. Each VLAN was connected to the router through its own physical router interface.

The router interfaces were configured with IP addresses belonging to their respective networks. The router automatically learned these networks as directly connected routes.

### Key Concepts:

- VLAN segmentation
- Router interfaces
- Directly connected routes
- Basic inter-VLAN routing
- Network connectivity testing

### Testing:

Connectivity was tested using "ping" to verify communication across the network.

Note: Exact VLAN IDs, IP addresses, subnet masks, interface numbers, and command configurations will be added after reviewing the original Packet Tracer file.

### Skills Practiced

- Basic LAN setup
- IPv4 addressing
- Subnet masks
- Switch configuration
- VLAN configuration
- Router interface configuration
- Directly connected routing
- Connectivity troubleshooting

### Tools Used

- Cisco Packet Tracer
- Cisco IOS CLI
- Git and GitHub

### Repository Structure

CCNA-Practical-Labs/
│
├── Lab-01-Basic-Networking/
│   ├── README.md
│   ├── topology.png
│   └── Lab-01.pkt
│
└── README.md

### Learning Progress

This repository will be updated as I complete more practical networking exercises, document configurations, and develop my networking skills.
