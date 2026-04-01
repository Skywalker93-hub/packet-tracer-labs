# VLAN DHCP Network Lab

## Description
This project demonstrates a small enterprise network built in Cisco Packet Tracer.

The topology includes two switches, multiple end devices, and a router configured using the **router-on-a-stick** approach. The network is segmented into VLANs, and IP addresses are assigned dynamically via DHCP.

---

## Topology
- 2 Layer 2 switches
- 1 router (Cisco 2811)
- Multiple end devices (PCs)
- Trunk link between switches
- Trunk link between switch and router

---

## VLAN Configuration
- **VLAN 10 – WORKERS**
- **VLAN 20 – ACCOUNTING**

Each VLAN represents a separate logical network, isolating traffic between departments.

---

## IP Addressing
- VLAN 10 → `192.168.10.0/24`
- VLAN 20 → `192.168.20.0/24`

---

## Features Implemented
- VLAN segmentation on switches
- Trunk links using 802.1Q
- Inter-VLAN routing (router-on-a-stick)
- DHCP configuration on the router
- Dynamic IP assignment for end devices

---

## How It Works
1. End devices send DHCP requests within their VLAN
2. Traffic is tagged and forwarded via trunk links
3. The router processes requests using subinterfaces:
   - `Fa0/0.10` → VLAN 10
   - `Fa0/0.20` → VLAN 20
4. Router assigns IP addresses from corresponding DHCP pools
5. Inter-VLAN communication is enabled through routing

---

## Key Concepts
- VLAN (Virtual Local Area Network)
- Trunk vs Access ports
- 802.1Q tagging
- Router-on-a-stick
- DHCP operation in segmented networks

---

## Files
- `vlan_network_lab.pkt` – Packet Tracer topology

---

## Result
- Devices within the same VLAN can communicate
- Devices across VLANs can communicate via the router
- All devices receive IP addresses automatically via DHCP

---

## Notes
This lab was created as part of hands-on practice for networking fundamentals and L2/L3 concepts.