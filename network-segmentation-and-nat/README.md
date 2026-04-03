# Multi-Site Network Segmentation with VLAN, ACL and NAT

## Overview

This project demonstrates the design and implementation of a segmented multi-tenant network using Cisco technologies.

The solution isolates traffic between different organizations sharing the same infrastructure, while still allowing controlled access to external services via NAT.

---

## Topology

The network consists of:

* Two organizations sharing a common access layer (Switch)
* VLAN-based segmentation (Layer 2 isolation)
* Inter-VLAN routing using Router-on-a-Stick
* Access Control Lists (ACL) for traffic filtering
* Two interconnected sites (Router-to-Router communication)
* External provider network with public IP addressing
* NAT (PAT) for outbound connectivity

---

## Objectives

* Isolate traffic between organizations within the same physical infrastructure
* Enable communication only within each organization
* Prevent inter-VLAN communication using ACLs
* Establish connectivity between two sites
* Provide access to external servers using NAT
* Ensure scalable and secure network design

---

## Technologies Used

* VLAN (IEEE 802.1Q)
* Trunking
* Inter-VLAN Routing (Router-on-a-Stick)
* Extended Access Control Lists (ACL)
* Static Routing
* NAT Overload (PAT)
* Cisco Packet Tracer

---

## Key Features

### 1. VLAN Segmentation

* VLAN 100 → Organization 1 (172.16.10.0/24)
* VLAN 200 → Organization 2 (172.16.20.0/24)

Traffic is isolated at Layer 2.

---

### 2. Inter-VLAN Routing

* Implemented via subinterfaces on the router
* 802.1Q encapsulation used for VLAN tagging

---

### 3. Traffic Filtering (ACL)

* Bidirectional blocking between VLANs
* Controlled routing between sites
* Ensures tenant isolation

---

### 4. Multi-Site Connectivity

* Routers interconnected via point-to-point network
* Static routes used for reachability

---

### 5. NAT (PAT)

* Internal networks translated to a public IP (210.0.11.10)
* Enables access to external servers:

  * 210.0.11.50
  * 210.0.11.51
  * 210.0.11.52

---

## Security Considerations

* Strict isolation between tenants
* ACL rules applied at routing boundaries
* No direct communication between private subnets

---

## Validation

The following tests were successfully performed:

* ✅ Devices within the same VLAN can communicate
* ❌ Devices across VLANs are isolated
* ✅ Inter-site routing works correctly
* ❌ Unauthorized cross-network traffic is blocked
* ✅ External servers are reachable via NAT

---

## Files

* Packet Tracer topology file (.pkt)
* Screenshots of configuration and validation

---

## Result

A scalable and secure multi-tenant network design with:

* Proper segmentation
* Controlled traffic flow
* External connectivity via NAT


