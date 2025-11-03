# Small-Office-Network-Setup
**Configured VLAN segmentation, DHCP, and Wi-Fi setup for a secure small office environment using Cisco Packet Tracer.**

**To open this project lab: Download the .pkt file and open it using Cisco Packet Tracer.**
## Project Overview
A comprehensive Packet Tracer project demonstrating core networking concepts, including:  
- VLANs (Virtual Land Area Networks)  
- Inter-VLAN Routing  
- DHCP (Dynamic Host Configuration Protocol)   
- Wifi Setup

This project demonstrates the configuration of a **small office network** with VLANs, Inter-Vlan routing, DHCP, and basic Wi-Fi setup.  
The goal is to design and implement a simple yet functional network that supports multiple departments while ensuring segmentation and connectivity.

## Brief Description of the used concepts and the Roles they play in the network
1. **VLANs (Virtual land Area Networks)**
- **Purpose:** Segment a network into smaller, isolated segments (VLANs) to improve organization, security, and management.
- **Role:** VLANs act as separate networks, allowing devices within a VLAN to communicate with each other but not with devices in other VLANs without routing.

2. **Routing Configuration**
- **Purpose:** Enable communication between VLANs and other networks.
- **Role:** Routers connect multiple VLANs and networks, allowing devices to communicate with each other across different VLANs.

3. **DHCP (Dynamic Host Configuration Protocol) Configuration**
- **Purpose:** Automatically assign IP addresses to devices on a network.
- **Role:** DHCP servers assign IP addresses, subnet masks, default gateways, and other network settings to devices, eliminating the need for manual configuration.

## Tools used for this Lab
- Cisco Packet Tracer  
- Virtual Studio Code Terminal (for documentation editing)  

## Network Topology
| Device | Quantity | Purpose |
|---------|--------|------------------|
|Router (Cisco 2911)| 1 | Inter-VLAN Routing, DHCP & ACLs Configurations |
|Switches (Cisco Catalyst 2960)| 2 | Connect end devices, assign VLANs, forward traffic to trunk uplinks
|Access Point | 1 | Connect end devies thru wireless|
|Personal Computers | 5 | End devices |
|Laptops | 1 | End devices |
|Smart Phone | 1 | End devices |

## IP Address Scheme
| VLAN |	Subnet |	Gateway |	DHCP Range |
|-----------------|----------------|--------------|---------------------|
|VLAN 10(ADMIN)|192.168.10.0/24|192.168.10.1|	192.168.10.2 - 192.168.10.254|
|VLAN 20 (STAFF)|	192.168.20.0/24|192.168.20.1|	192.168.20.2 - 192.168.20.254|
|VLAN 30 (GUEST)|	192.168.30.0/24|	192.168.30.1|	192.168.30.2 - 192.168.30.254|

# Step-by-Step Configuration of the Simulated Network in Cisco Packet Tracer
![Network-Lab-Setup](Small Network Setup/Network Topology.png)
## STEP 1: Network Design
### Open Cisco Packet Tracer and Set Up the Topology
- Launch Cisco Packet Tracer.
On the open blank space: 
- Click "End Devices" > click and drop 8 Laptops into the setup 
- Click "Switches" under Networking devices > click and drop:
    - 1 Multilayer Switch (3650-24PS)
    - 3 Access Switches (2960-24TT)
- Click "Routers" under Networking devices> click and drop Router (2911)
