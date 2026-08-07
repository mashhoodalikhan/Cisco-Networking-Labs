# 🌐 Cisco Packet Tracer - Hands-on Networking & Security Labs

Welcome to my computer networking practical lab repository! This repository showcases custom Cisco Packet Tracer topologies, CLI configurations, dynamic routing protocols, and network segmentation experiments created to master fundamental and advanced networking concepts.

---

## 📌 Repository Overview & Visual Proofs

| Category | Lab Topic | Protocol / Concept | Primary Topology Preview | Lab Files & Visuals |
| :--- | :--- | :--- | :--- | :--- |
| **Switching** | Virtual Local Area Network | VLAN Segmentation & Trunking (802.1Q) | <img src="./01-Switching/VLAN%20images/vlan%201.png" width="280px" alt="VLAN Topology"> | [📁 Lab File (`.pkt`)](./01-Switching/VLAN%20lab.pkt)<br>[🖼️ All 5 Screenshots](./01-Switching/VLAN%20images/) |
| **Subnetting** | Variable Length Subnet Masking | VLSM & IP Allocation | <img src="./02-Subnetting/VLSM%20images/vlsm%201.png" width="280px" alt="VLSM Topology"> | [📁 Lab File (`.pkt`)](./02-Subnetting/VLSM%20lab.pkt)<br>[🖼️ All 4 Screenshots](./02-Subnetting/VLSM%20images/) |
| **Routing** | Routing Information Protocol | RIP v2 Distance Vector | <img src="./03-Routing/RIP%20images/rip1.jpg" width="280px" alt="RIP Topology"> | [📁 Lab File (`.pkt`)](./03-Routing/RIP%20Lab.pkt)<br>[🖼️ All 4 Screenshots](./03-Routing/RIP%20images/) |
| **Routing** | Open Shortest Path First | OSPF Single-Area Link-State | *(Add Screenshot)* | [📁 Lab File (`.pkt`)](./03-Routing/ospf%20lab.pkt) |
| **Routing** | Dynamic Routing Setup | Multi-Router Dynamic Setup | *(Add Screenshot)* | [📁 Lab File (`.pkt`)](./03-Routing/dynamic%20routing.pkt) |

---

## 🛠️ Key CLI Configurations Covered

### 1. VLAN & Trunking Setup (Switching)
```bash
Switch# configure terminal
Switch(config)# vlan 10
Switch(config-vlan)# name IT_Dept
Switch(config-vlan)# exit
Switch(config)# interface FastEthernet 0/1
Switch(config-if)# switchport mode access
Switch(config-if)# switchport access vlan 10