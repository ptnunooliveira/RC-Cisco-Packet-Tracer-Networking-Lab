# 🌐 Corporate Network Infrastructure Implementation and Simulation

![Cisco Packet Tracer](https://img.shields.io/badge/Simulation-Cisco_Packet_Tracer-1BA0D7?style=for-the-badge&logo=cisco)
![Networking](https://img.shields.io/badge/Domain-Computer_Networks-4CAF50?style=for-the-badge)
![IPCA](https://img.shields.io/badge/Institution-IPCA-005A9C?style=for-the-badge)

This repository contains the documentation and architectural details of a practical project focused on the design, addressing, and configuration of computer networks. The project encompasses IPv4 network segmentation, VLAN implementation, and transition and routing using the IPv6 protocol.

---

## 📋 Project Overview

The project aims to simulate a complex network infrastructure, divided into three main phases:
1. **Subnetting and NAT (IPv4):** Creation of an efficient addressing scheme and ensuring connectivity with the outside.
2. **VLANs:** Logical segmentation of the infrastructure by functional areas (Managers, Commercial, and Operational) to optimize traffic and security.
3. **IPv6 and Dynamic Routing:** Implementation of the IPv6 protocol with autoconfiguration and adaptive routing.

---

## 🛠️ Implemented Technologies and Protocols

### Part I: IPv4 Addressing and NAT
* **Subnetting (CIDR/VLSM):** Address planning for the Production (50 hosts), Commercial (40 hosts), and Financial (29 hosts) departments using appropriate subnets.
* **Logical and Physical Topologies:** Use of wired networks (Ethernet/Star Topology) and wireless networks in infrastructure mode.
* **Static Routing:** Manual configuration of routing tables in routers to ensure data flow between subnets and the ISP.
* **NAT / PAT (NAPT):** Implementation of Network Address and Port Translation (NAPT) on the edge router, allowing multiple internal devices to share a single public IP address to access the external network.

### Part II: Virtual Local Area Networks (VLANs)
* **Segmentation (IEEE 802.1Q):** Creation of independent VLANs for the different company profiles, assigning private class B IP addresses.
* **Access and Trunk Ports:** Configuration of Access ports to connect end devices to a specific VLAN, and Trunk ports to carry traffic from multiple VLANs between switches.
* **Inter-VLAN Routing:** Use of subinterfaces on a layer 3 device (Router) to allow controlled communication between different VLANs.

### Part III: Transition to IPv6
* **Global Unicast Addressing:** Assignment of 128-bit addresses with a `/64` prefix to the different areas.
* **SLAAC (Stateless Address Autoconfiguration):** Automatic configuration of IPv6 addresses on end hosts using the EUI-64 format and Router Advertisement messages.
* **Dynamic Routing (OSPF):** Use of the OSPF (Open Shortest Path First) protocol for automatic and dynamic route updates between the infrastructure routers.
* **ICMPv6:** Use of the control protocol for network diagnostics, namely through connectivity tests (Ping).

---

## 🔍 Testing and Validation Methodology

During development, network integrity was validated through:
* **Connectivity Tests:** Use of ICMP datagrams (ping) to evaluate Round Trip Time (RTT) and packet loss.
* **Route Tracking:** Use of the tracert command to analyze the hops of IP packets in the network.
* **Datagram Analysis:** Inspection of PDU traffic to validate VLAN tagging (insertion of the 802.1Q tag) and NAT/PAT table translations.

---

## 🎓 Academic Context

This project was developed within an academic context:
* **Course Unit:** Computer Networks
* **Degree:** Bachelor's in Computer Systems Engineering (After-hours Mode)
* **Institution:** School of Technology - IPCA (Polytechnic Institute of Cávado and Ave)
* **Date:** December 2024
* **Supervising Professor:** Paulo Macedo

### 👥 Development Team
* **Marina Silva** (No. 31029)
* **Nelson Cruz** (No. 31103)
* **Nuno Oliveira** (No. 31550)

---
*Note: The complete infrastructure and its respective configurations are designed to be simulated in the Cisco Packet Tracer environment.*
