# ⚡ Cisco Networking Labs
### Build. Break. Verify. Understand.

<p align="center">
  <strong>🛡️ Cybersecurity Student &nbsp;•&nbsp; 🌐 Networking Enthusiast &nbsp;•&nbsp; 💻 Cisco IOS &nbsp;•&nbsp; 🔬 Packet Tracer</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Cisco-Packet%20Tracer-1f2937?style=for-the-badge&logo=cisco&logoColor=white" alt="Cisco Packet Tracer">
  <img src="https://img.shields.io/badge/Networking-Practical%20Labs-0f766e?style=for-the-badge" alt="Networking Labs">
  <img src="https://img.shields.io/badge/Cybersecurity-Hands--On-7c3aed?style=for-the-badge" alt="Cybersecurity">
  <img src="https://img.shields.io/badge/Status-Actively%20Learning-16a34a?style=for-the-badge" alt="Actively Learning">
</p>

<p align="center">
  <em>Not just commands. Not just diagrams.</em><br>
  <strong>Configure → Verify → Test → Troubleshoot → Understand</strong>
</p>

---

## 🧭 Quick Navigation

**[⚡ Lab Map](#-lab-map)** •
**[🗂️ Repository Structure](#️-repository-structure)** •
**[🔥 Visual Proof](#-visual-proof-of-work)** •
**[🧪 Labs](#-hands-on-labs)** •
**[🛠️ CLI Reference](#️-quick-cisco-ios-reference)** •
**[🔍 Verification](#-verification-workflow)** •
**[🧠 Concepts](#-concepts-practiced)** •
**[📈 Roadmap](#-learning-roadmap)**

---

# 🧠 What This Repository Is

This repository is my **hands-on Cisco networking lab portfolio**, built while developing practical networking and cybersecurity skills.

Instead of only studying networking theory, I use **Cisco Packet Tracer** to build topologies, configure Cisco IOS devices, test connectivity, verify protocol behavior, and troubleshoot failures.

### Current focus

| Domain | Practical Work |
| :--- | :--- |
| 🔀 **Switching** | VLANs, access ports, trunks, 802.1Q |
| 🔗 **Inter-VLAN** | Router-on-a-Stick, sub-interfaces, gateway communication |
| ⚡ **Link Aggregation** | EtherChannel, LACP, Port-Channel |
| 🌳 **Loop Prevention** | STP / RSTP concepts and verification |
| 🧩 **Subnetting** | VLSM, subnet masks, IP allocation |
| 🛣️ **Routing** | RIPv2, OSPF, EIGRP |
| 🔍 **Operations** | IOS verification, connectivity testing, troubleshooting |

> ### ⚔️ The rule
> **A lab is not finished when the configuration is typed.  
> It is finished when the behavior is verified.**

---

# ⚡ Lab Map

<p align="center">

| # | Area | Lab | Core Skills | Status |
| :---: | :--- | :--- | :--- | :---: |
| 01 | 🔀 Switching | **VLAN** | Segmentation, Access Ports, Trunks | ✅ |
| 02 | 🔀 Switching | **Inter-VLAN Routing** | 802.1Q, Router-on-a-Stick | ✅ |
| 03 | ⚡ Switching | **EtherChannel + LACP** | Link Aggregation, Port-Channel | ✅ |
| 04 | 🌳 Switching | **STP / RSTP** | Loop Prevention, Redundancy | ✅ |
| 05 | 🧩 Subnetting | **VLSM** | Efficient IP Allocation | ✅ |
| 06 | 🛣️ Routing | **RIPv2** | Distance-Vector Routing | ✅ |
| 07 | 🧭 Routing | **OSPF** | Link-State, Area 0 | ✅ |
| 08 | 🚀 Routing | **EIGRP** | Dynamic Routing, Neighbors | ✅ |

</p>

---

# 🔥 Visual Proof of Work

The repository is organized around **actual Packet Tracer work and verification evidence**, not just theory.

## ⚡ EtherChannel + LACP

<p align="center">
  <img src="./01-Switching/EtherChannel-LACP/lacp1.png" width="31%" alt="LACP topology">
  <img src="./01-Switching/EtherChannel-LACP/lacp2.png" width="31%" alt="LACP verification">
  <img src="./01-Switching/EtherChannel-LACP/lacp3.png" width="31%" alt="LACP configuration">
</p>

**Focus:** LACP negotiation, member links, Port-Channel formation, and verification.

### 🌳 STP / RSTP

The STP/RSTP lab is stored separately so the switching section stays easy to navigate:

**`01-Switching/STP-RSTP-Lab/`**

It contains the Packet Tracer lab plus multiple verification screenshots and an **STP vs RSTP** visual reference.

---

# 🗂️ Repository Structure

```text
Cisco-Networking-Labs/
│
├── 📄 README.md
│
├── 🔀 01-Switching/
│   │
│   ├── 📁 VLAN images/
│   │   └── vlan 1.png
│   ├── 📦 VLAN lab.pkt
│   │
│   ├── 📁 inter VLAN images/
│   │   ├── inter vlan 1.png
│   │   └── inter vlan 2.png
│   ├── 📦 Inter-VLAN Routing.pkt
│   │
│   ├── 📁 EtherChannel-LACP/
│   │   ├── 📦 LACP lab.pkt
│   │   ├── 🖼️ lacp1.png
│   │   ├── 🖼️ lacp2.png
│   │   └── 🖼️ lacp3.png
│   │
│   └── 📁 STP-RSTP-Lab/
│       ├── 📦 STP LAB
│       ├── 🖼️ STP AND RSTP 1
│       ├── 🖼️ STP AND RSTP 2
│       ├── 🖼️ STP AND RSTP 3
│       ├── 🖼️ STP AND RSTP 4
│       ├── 🖼️ STP AND RSTP 5
│       └── 🖼️ STP VS RSTP
│
├── 🧩 02-Subnetting/
│   ├── 📦 VLSM lab.pkt
│   └── 📁 VLSM images/
│
└── 🛣️ 03-Routing/
    ├── 📦 RIP Lab.pkt
    ├── 📦 ospf lab.pkt
    ├── 📦 dynamic routing.pkt
    ├── 📁 RIP images/
    ├── 📁 OSPF images/
    └── 📁 EIGRP images/
```

> **Organization principle:** each major networking domain has its own top-level folder, while larger labs keep their screenshots and supporting evidence inside dedicated lab folders.

---

# 🧪 Hands-On Labs

<details>
<summary><strong>🔀 01 — VLAN & Trunking</strong></summary>

### What I practiced
- VLAN creation
- VLAN segmentation
- Access ports
- Trunk ports
- 802.1Q trunking
- VLAN verification

### Core commands

```text
Switch# configure terminal
Switch(config)# vlan 10
Switch(config-vlan)# name IT_Dept
Switch(config-vlan)# exit

Switch(config)# interface FastEthernet 0/1
Switch(config-if)# switchport mode access
Switch(config-if)# switchport access vlan 10

Switch(config)# interface GigabitEthernet 0/1
Switch(config-if)# switchport mode trunk
```

### Verify

```text
Switch# show vlan brief
Switch# show interfaces trunk
```

</details>

<details>
<summary><strong>🔗 02 — Inter-VLAN Routing</strong></summary>

### What I practiced
- Router-on-a-Stick
- Router sub-interfaces
- 802.1Q encapsulation
- Default gateways
- Inter-VLAN communication

### Example

```text
Router# configure terminal

Router(config)# interface GigabitEthernet 0/0.10
Router(config-subif)# encapsulation dot1Q 10
Router(config-subif)# ip address 192.168.1.1 255.255.255.0

Router(config)# interface GigabitEthernet 0/0.20
Router(config-subif)# encapsulation dot1Q 20
Router(config-subif)# ip address 192.168.2.1 255.255.255.0
```

### Verify

```text
Router# show ip interface brief
Router# show ip route
PC> ping <destination-ip>
```

</details>

<details>
<summary><strong>⚡ 03 — EtherChannel with LACP</strong></summary>

### What I practiced
- EtherChannel
- LACP negotiation
- Member interfaces
- Port-Channel
- Link aggregation
- Verification

### Example

```text
Switch# configure terminal

Switch(config)# interface range FastEthernet 0/1 - 2
Switch(config-if-range)# channel-group 1 mode active
Switch(config-if-range)# exit

Switch(config)# interface Port-channel 1
Switch(config-if)# switchport mode trunk
```

### Verify

```text
Switch# show etherchannel summary
Switch# show interfaces port-channel 1
Switch# show lacp neighbor
Switch# show interfaces status
```

<p align="center">
  <img src="./01-Switching/EtherChannel-LACP/lacp1.png" width="45%" alt="LACP topology">
  <img src="./01-Switching/EtherChannel-LACP/lacp2.png" width="45%" alt="LACP verification">
</p>

<p align="center">
  <img src="./01-Switching/EtherChannel-LACP/lacp3.png" width="55%" alt="LACP configuration">
</p>

> **Key idea:** multiple physical links can operate as one logical Port-Channel, while LACP handles dynamic negotiation.

</details>

<details>
<summary><strong>🌳 04 — STP / RSTP</strong></summary>

### What I practiced
- Spanning Tree concepts
- Redundant switch links
- Loop prevention
- STP vs RSTP behavior
- Verification and topology analysis

### Lab folder

```text
01-Switching/STP-RSTP-Lab/
```

The folder contains the Packet Tracer topology, five supporting screenshots, and an STP vs RSTP visual comparison.

### Useful verification commands

```text
Switch# show spanning-tree
Switch# show spanning-tree summary
Switch# show interfaces status
```

> **Key idea:** redundancy is useful only when the network can control Layer-2 loops.

</details>

<details>
<summary><strong>🧩 05 — VLSM & IP Address Allocation</strong></summary>

### What I practiced
- Variable Length Subnet Masking
- Host requirements
- Subnet masks
- Network and host addressing
- Efficient address allocation

### Example

```text
Router# configure terminal

Router(config)# interface GigabitEthernet 0/0.10
Router(config-subif)# encapsulation dot1Q 10
Router(config-subif)# ip address 192.168.1.1 255.255.255.192
```

### Verify

```text
Router# show ip interface brief
Router# show ip route
```

</details>

<details>
<summary><strong>🛣️ 06 — RIPv2 Dynamic Routing</strong></summary>

### What I practiced
- RIPv2
- Distance-vector routing
- Dynamic route learning
- Routing table verification

```text
Router# configure terminal
Router(config)# router rip
Router(config-router)# version 2
Router(config-router)# network 192.168.10.0
Router(config-router)# network 10.0.0.0
Router(config-router)# no auto-summary
```

### Verify

```text
Router# show ip protocols
Router# show ip route
```

RIP-learned routes are identified by:

```text
R
```

</details>

<details>
<summary><strong>🧭 07 — OSPF Single-Area Routing</strong></summary>

### What I practiced
- OSPF
- Link-state routing
- Area 0
- Neighbor relationships
- Routing table verification

```text
Router# configure terminal
Router(config)# router ospf 1
Router(config-router)# network 192.168.1.0 0.0.0.255 area 0
Router(config-router)# network 10.1.1.0 0.0.0.3 area 0
```

### Verify

```text
Router# show ip protocols
Router# show ip ospf neighbor
Router# show ip route
```

OSPF-learned routes are identified by:

```text
O
```

</details>

<details>
<summary><strong>🚀 08 — EIGRP</strong></summary>

### What I practiced
- EIGRP
- Dynamic routing
- Neighbor relationships
- Route verification

```text
Router# configure terminal
Router(config)# router eigrp 10
Router(config-router)# network 192.168.1.0 0.0.0.255
Router(config-router)# network 10.0.0.0 0.0.0.3
Router(config-router)# no auto-summary
```

### Verify

```text
Router# show ip protocols
Router# show ip eigrp neighbors
Router# show ip route
```

EIGRP-learned routes are identified by:

```text
D
```

</details>

---

# 🛠️ Quick Cisco IOS Reference

| Goal | Command |
| :--- | :--- |
| Interface state | `show ip interface brief` |
| VLANs | `show vlan brief` |
| Trunks | `show interfaces trunk` |
| STP state | `show spanning-tree` |
| STP summary | `show spanning-tree summary` |
| EtherChannel | `show etherchannel summary` |
| LACP neighbors | `show lacp neighbor` |
| Port-Channel | `show interfaces port-channel 1` |
| Routing table | `show ip route` |
| Routing protocols | `show ip protocols` |
| OSPF neighbors | `show ip ospf neighbor` |
| EIGRP neighbors | `show ip eigrp neighbors` |
| Connectivity | `ping <destination-ip>` |
| Path tracing | `traceroute <destination-ip>` |

---

# 🔍 Verification Workflow

```text
        ┌───────────────┐
        │   BUILD LAB   │
        └───────┬───────┘
                ↓
        ┌───────────────┐
        │ CONFIGURE IOS │
        └───────┬───────┘
                ↓
        ┌───────────────┐
        │ VERIFY STATE  │
        └───────┬───────┘
                ↓
        ┌───────────────┐
        │ TEST TRAFFIC  │
        └───────┬───────┘
                ↓
        ┌───────────────┐
        │ FIND FAILURES │
        └───────┬───────┘
                ↓
        ┌───────────────┐
        │ TROUBLESHOOT  │
        └───────┬───────┘
                ↓
        ┌───────────────┐
        │ DOCUMENT PROOF│
        └───────────────┘
```

### My troubleshooting mindset

**1. Is the interface up?**  
→ `show ip interface brief`

**2. Is the VLAN correct?**  
→ `show vlan brief`

**3. Is the trunk actually trunking?**  
→ `show interfaces trunk`

**4. Is the EtherChannel formed?**  
→ `show etherchannel summary`

**5. Is LACP negotiating?**  
→ `show lacp neighbor`

**6. Is STP behaving as expected?**  
→ `show spanning-tree`

**7. Is the route present?**  
→ `show ip route`

**8. Can the endpoint communicate?**  
→ `ping`

**9. Where does the path break?**  
→ `traceroute`

---

# 🧠 Concepts Practiced

### 🔀 Switching
- VLAN configuration
- VLAN segmentation
- Access ports
- Trunk ports
- 802.1Q
- Inter-VLAN Routing
- Router-on-a-Stick
- EtherChannel
- LACP
- Port-Channel
- STP
- RSTP
- Layer-2 redundancy
- Loop prevention

### 🧩 Subnetting
- VLSM
- IP address allocation
- Subnet masks
- Network addressing
- Host addressing

### 🛣️ Routing
- RIPv2
- OSPF
- EIGRP
- Dynamic routing
- Routing tables
- Routing protocol verification
- Neighbor relationships

### 🔍 Troubleshooting
- Interface verification
- VLAN verification
- Trunk verification
- STP verification
- EtherChannel verification
- LACP verification
- Routing verification
- Connectivity testing
- Ping
- Traceroute
- Routing table analysis

---

# 📈 Learning Roadmap

```text
                    NETWORKING FOUNDATIONS
                             │
                             ▼
                    ┌─────────────────┐
                    │ VLAN + TRUNKING │
                    └────────┬────────┘
                             ▼
                  ┌──────────────────────┐
                  │ INTER-VLAN ROUTING   │
                  └──────────┬───────────┘
                             ▼
                ┌──────────────────────────┐
                │ STP / RSTP               │
                │ LOOP PREVENTION          │
                └────────────┬─────────────┘
                             ▼
                ┌──────────────────────────┐
                │ ETHERCHANNEL / LACP      │
                │ LINK AGGREGATION         │
                └────────────┬─────────────┘
                             ▼
                    ┌────────────────┐
                    │ VLSM + IP PLAN │
                    └───────┬────────┘
                            ▼
               ┌────────────────────────┐
               │ RIPv2 → OSPF → EIGRP  │
               └───────────┬────────────┘
                           ▼
                ┌───────────────────────┐
                │ VERIFY + TROUBLESHOOT │
                └───────────┬───────────┘
                            ▼
                 ┌─────────────────────┐
                 │ ADVANCED NETWORKING │
                 │ + CYBERSECURITY     │
                 └─────────────────────┘
```

---

# 🧭 What Comes Next

Planned expansion of this repository:

- [ ] Static Routing
- [ ] DHCP
- [ ] NAT
- [ ] ACLs
- [ ] Advanced OSPF
- [ ] More STP/RSTP scenarios
- [ ] Advanced EtherChannel scenarios
- [ ] Cisco troubleshooting scenarios
- [ ] Network security labs
- [ ] More realistic multi-router topologies

---

# 🎯 Why This Repository Exists

This is more than a collection of `.pkt` files.

It is a **practical record of the progression from networking fundamentals to more advanced networking and security concepts**.

The goal is to keep every lab:

**Buildable → Configurable → Verifiable → Troubleshootable → Documented**

So when something breaks, the objective is not simply to make it green again.

> **Find the failure. Understand the failure. Fix the failure. Verify the fix.**

---

# 👨‍💻 Author

<p align="center">
  <strong>Mashhood Ali Khan</strong><br>
  Cybersecurity Student • Networking Enthusiast
</p>

<p align="center">
  <em>Learning networking by building, configuring, testing, breaking, troubleshooting, and rebuilding real-world-style topologies in Cisco Packet Tracer.</em>
</p>

<p align="center">
  <strong>⚔️ Don't just make it work. Understand why it works — and know how to find it when it doesn't.</strong>
</p>

---

<p align="center">
  <sub>Built with Cisco Packet Tracer • Cisco IOS • Curiosity • Practice • Troubleshooting</sub>
</p>
