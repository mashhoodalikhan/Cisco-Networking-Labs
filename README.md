# ⚡ Cisco Networking Labs — Build. Break. Verify. Repeat.

<p align="center">
  <strong>🛡️ Cybersecurity Student • 🌐 Networking Enthusiast • 💻 Cisco IOS • 🔬 Packet Tracer</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Cisco-Packet%20Tracer-1f2937?style=for-the-badge&logo=cisco&logoColor=white">
  <img src="https://img.shields.io/badge/Networking-Labs-0f766e?style=for-the-badge">
  <img src="https://img.shields.io/badge/Cybersecurity-Practical%20Learning-7c3aed?style=for-the-badge">
  <img src="https://img.shields.io/badge/Status-Actively%20Learning-16a34a?style=for-the-badge">
</p>

<p align="center">
  <em>Not just commands. Not just diagrams.</em><br>
  <strong>Configure → Verify → Troubleshoot → Understand</strong>
</p>

---

## 🧭 Quick Navigation

**[📊 Lab Map](#-current-lab-map)** •
**[🖼️ Visual Proof Table](#-repository-overview--visual-proofs)** • **[🖼️ Complete Gallery](#-complete-visual-gallery)** •
**[🗂️ Structure](#️-repository-structure)** •
**[⚡ LACP](#-etherchannel--lacp)** •
**[🌳 STP/RSTP](#-stprstp)** •
**[🛠️ CLI](#️-key-cli-configurations)** •
**[🔍 Verification](#-verification-workflow)** •
**[📈 Roadmap](#-learning-progression)**

---

## 🧠 What This Repository Is About

This is my **hands-on Cisco networking lab repository**, built while developing practical networking and cybersecurity skills.

Instead of only reading theory, I use **Cisco Packet Tracer** to build topologies, configure Cisco IOS devices, test connectivity, verify protocols, and troubleshoot failures.

### Current focus

- 🔀 **Switching & VLANs**
- 🔗 **Inter-VLAN Routing**
- ⚡ **EtherChannel & LACP**
- 🌳 **STP / RSTP**
- 🧩 **VLSM & IP Addressing**
- 🛣️ **RIPv2**
- 🧭 **OSPF**
- 🚀 **EIGRP**
- 🔍 **Verification & Troubleshooting**

> **The objective:** understand the network from configuration to packet flow — not just memorize commands.

---

# 📊 Current Lab Map

| # | Area | Lab | Core Skills | Status |
| :---: | :--- | :--- | :--- | :---: |
| 01 | 🔀 Switching | **VLAN & Trunking** | Segmentation, Access Ports, 802.1Q | ✅ |
| 02 | 🔗 Switching | **Inter-VLAN Routing** | Router-on-a-Stick, Sub-Interfaces | ✅ |
| 03 | ⚡ Switching | **EtherChannel + LACP** | Link Aggregation, Port-Channel | ✅ |
| 04 | 🌳 Switching | **STP / RSTP** | Loop Prevention, Redundancy | ✅ |
| 05 | 🧩 Subnetting | **VLSM** | Efficient IP Allocation | ✅ |
| 06 | 🛣️ Routing | **RIPv2** | Distance-Vector Routing | ✅ |
| 07 | 🧭 Routing | **OSPF** | Link-State, Area 0 | ✅ |
| 08 | 🚀 Routing | **EIGRP** | Dynamic Routing, Neighbors | ✅ |

---

# 📌 Repository Overview & Visual Proofs

> ### 🔥 The visual table is back.
> Each major lab is presented with its **topic, protocol/concept, topology preview, and direct lab/screenshot location**.

| Category | Lab Topic | Protocol / Concept | Topology Preview | Lab Files & Visuals |
| :--- | :--- | :--- | :--- | :--- |
| **Switching** | Virtual Local Area Network | VLAN Segmentation & Trunking (802.1Q) | <img src="./01-Switching/VLAN%20images/vlan%201.png" width="280px" alt="VLAN Topology"> | [📁 Lab File](./01-Switching/VLAN%20lab.pkt)<br>[🖼️ Screenshots](./01-Switching/VLAN%20images/) |
| **Switching** | Inter-VLAN Routing | Router-on-a-Stick, 802.1Q & VLAN Communication | <img src="./01-Switching/inter%20VLAN%20images/inter%20vlan%201.png" width="280px" alt="Inter-VLAN Topology"> | [📁 Lab File](./01-Switching/Inter-VLAN%20Routing.pkt)<br>[🖼️ Screenshots](./01-Switching/inter%20VLAN%20images/) |
| **Switching** | EtherChannel with LACP | LACP, Link Aggregation & Port-Channel | <img src="./01-Switching/EtherChannel-LACP/lacp1.png" width="280px" alt="LACP Topology"> | [📁 Lab File](./01-Switching/EtherChannel-LACP/LACP%20lab.pkt)<br>[🖼️ Screenshots](./01-Switching/EtherChannel-LACP/) |
| **Switching** | STP / RSTP | Loop Prevention & Layer-2 Redundancy | **See STP/RSTP gallery below** | [📁 Lab Folder](./01-Switching/STP-RSTP-Lab/) |
| **Subnetting** | Variable Length Subnet Masking | VLSM & IP Address Allocation | <img src="./02-Subnetting/VLSM%20images/vlsm%201.png" width="280px" alt="VLSM Topology"> | [📁 Lab File](./02-Subnetting/VLSM%20lab.pkt)<br>[🖼️ Screenshots](./02-Subnetting/VLSM%20images/) |
| **Routing** | Routing Information Protocol | RIPv2 Distance Vector | <img src="./03-Routing/RIP%20images/rip1.jpg" width="280px" alt="RIP Topology"> | [📁 Lab File](./03-Routing/RIP%20Lab.pkt)<br>[🖼️ Screenshots](./03-Routing/RIP%20images/) |
| **Routing** | Open Shortest Path First | OSPF Single-Area Link-State | <img src="./03-Routing/OSPF%20images/ospf1.jpg" width="280px" alt="OSPF Topology"> | [📁 Lab File](./03-Routing/ospf%20lab.pkt)<br>[🖼️ Screenshots](./03-Routing/OSPF%20images/) |
| **Routing** | Enhanced Interior Gateway Routing Protocol | EIGRP / Multi-Router Setup | <img src="./03-Routing/EIGRP%20images/eigrp1.jpg" width="280px" alt="EIGRP Topology"> | [📁 Lab File](./03-Routing/dynamic%20routing.pkt)<br>[🖼️ Screenshots](./03-Routing/EIGRP%20images/) |

---

# 🗂️ Repository Structure

```text
Cisco-Networking-Labs/
│
├── 📄 README.md
│
├── 🔀 01-Switching/
│   ├── 📦 VLAN lab.pkt
│   ├── 📁 VLAN images/
│   │   └── 🖼️ vlan 1.png
│   │
│   ├── 📦 Inter-VLAN Routing.pkt
│   ├── 📁 inter VLAN images/
│   │   ├── 🖼️ inter vlan 1.png
│   │   └── 🖼️ inter vlan 2.png
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

---

# 🔥 Proof of Work

Every lab is backed by a **Packet Tracer topology and visual verification** where available.

## ⚡ EtherChannel + LACP

<p align="center">
  <img src="./01-Switching/EtherChannel-LACP/lacp1.png" width="31%" alt="LACP Topology">
  <img src="./01-Switching/EtherChannel-LACP/lacp2.png" width="31%" alt="LACP Verification">
  <img src="./01-Switching/EtherChannel-LACP/lacp3.png" width="31%" alt="LACP Configuration">
</p>

**Focus:** link aggregation, LACP negotiation, Port-Channel formation and verification.

---

# 🖼️ Complete Visual Gallery

The README keeps the **visual-proof table at the top** and also gives each major lab its own gallery below, so a reviewer can see the actual Packet Tracer work without digging through the repository.

## 🔀 VLAN & Trunking

<p align="center">
  <img src="./01-Switching/VLAN%20images/vlan%201.png" width="70%" alt="VLAN Lab Topology">
</p>

**Lab:** [📁 VLAN Lab](./01-Switching/VLAN%20lab.pkt) · [🖼️ All VLAN Screenshots](./01-Switching/VLAN%20images/)

## 🔗 Inter-VLAN Routing

<p align="center">
  <img src="./01-Switching/inter%20VLAN%20images/inter%20vlan%201.png" width="47%" alt="Inter-VLAN Lab 1">
  <img src="./01-Switching/inter%20VLAN%20images/inter%20vlan%202.png" width="47%" alt="Inter-VLAN Lab 2">
</p>

**Lab:** [📁 Inter-VLAN Lab](./01-Switching/Inter-VLAN%20Routing.pkt) · [🖼️ All Inter-VLAN Screenshots](./01-Switching/inter%20VLAN%20images/)

## ⚡ EtherChannel + LACP

<p align="center">
  <img src="./01-Switching/EtherChannel-LACP/lacp1.png" width="31%" alt="LACP Topology">
  <img src="./01-Switching/EtherChannel-LACP/lacp2.png" width="31%" alt="LACP Verification">
  <img src="./01-Switching/EtherChannel-LACP/lacp3.png" width="31%" alt="LACP Configuration">
</p>

**Lab:** [📁 LACP Packet Tracer Lab](./01-Switching/EtherChannel-LACP/LACP%20lab.pkt) · [🖼️ LACP Evidence](./01-Switching/EtherChannel-LACP/)

## 🌳 STP / RSTP

<p align="center">
  <strong>STP/RSTP visual evidence is stored in the dedicated lab folder.</strong>
</p>

**Lab folder:** [📁 STP-RSTP-Lab](./01-Switching/STP-RSTP-Lab/)

Includes the Packet Tracer lab, five STP/RSTP verification screenshots, and the **STP VS RSTP** comparison visual.

## 🧩 VLSM & IP Address Allocation

<p align="center">
  <img src="./02-Subnetting/VLSM%20images/vlsm%201.png" width="70%" alt="VLSM Lab Topology">
</p>

**Lab:** [📁 VLSM Lab](./02-Subnetting/VLSM%20lab.pkt) · [🖼️ VLSM Screenshots](./02-Subnetting/VLSM%20images/)

## 🛣️ RIPv2

<p align="center">
  <img src="./03-Routing/RIP%20images/rip1.jpg" width="70%" alt="RIPv2 Lab Topology">
</p>

**Lab:** [📁 RIPv2 Lab](./03-Routing/RIP%20Lab.pkt) · [🖼️ RIP Evidence](./03-Routing/RIP%20images/)

## 🧭 OSPF

<p align="center">
  <img src="./03-Routing/OSPF%20images/ospf1.jpg" width="70%" alt="OSPF Lab Topology">
</p>

**Lab:** [📁 OSPF Lab](./03-Routing/ospf%20lab.pkt) · [🖼️ OSPF Evidence](./03-Routing/OSPF%20images/)

## 🚀 EIGRP

<p align="center">
  <img src="./03-Routing/EIGRP%20images/eigrp1.jpg" width="70%" alt="EIGRP Lab Topology">
</p>

**Lab:** [📁 EIGRP / Dynamic Routing Lab](./03-Routing/dynamic%20routing.pkt) · [🖼️ EIGRP Evidence](./03-Routing/EIGRP%20images/)

---

# 🌳 STP/RSTP

The STP/RSTP lab is now part of the **Switching** section.

### 📁 Lab

`01-Switching/STP-RSTP-Lab/`

It contains the Packet Tracer topology plus five supporting screenshots and an STP vs RSTP visual reference.

### 🧠 Core concepts

- Spanning Tree Protocol
- Rapid Spanning Tree Protocol
- Root Bridge
- Port Roles / States
- Layer-2 Loop Prevention
- Redundancy
- Faster convergence with RSTP

### 🔍 Verification

```bash
Switch# show spanning-tree
Switch# show spanning-tree summary
Switch# show interfaces status
```

---

# 🛠️ Key CLI Configurations

## 1. VLAN & Trunking

```bash
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

```bash
Switch# show vlan brief
Switch# show interfaces trunk
```

---

## 2. Inter-VLAN Routing — Router-on-a-Stick

```bash
Router# configure terminal

Router(config)# interface GigabitEthernet 0/0.10
Router(config-subif)# encapsulation dot1Q 10
Router(config-subif)# ip address 192.168.1.1 255.255.255.0

Router(config)# interface GigabitEthernet 0/0.20
Router(config-subif)# encapsulation dot1Q 20
Router(config-subif)# ip address 192.168.2.1 255.255.255.0
```

### Verify

```bash
Router# show ip interface brief
Router# show ip route
PC> ping <destination-ip>
```

---

## 3. EtherChannel with LACP

```bash
Switch# configure terminal

Switch(config)# interface range FastEthernet 0/1 - 2
Switch(config-if-range)# channel-group 1 mode active
Switch(config-if-range)# exit

Switch(config)# interface Port-channel 1
Switch(config-if)# switchport mode trunk
```

### Verify

```bash
Switch# show etherchannel summary
Switch# show interfaces port-channel 1
Switch# show lacp neighbor
Switch# show interfaces status
```

---

## 4. VLSM & IP Address Allocation

VLSM (**Variable Length Subnet Masking**) allows different subnet sizes to be used according to host requirements.

```bash
Router# show ip interface brief
Router# show ip route
```

---

## 5. RIPv2 Dynamic Routing

```bash
Router# configure terminal
Router(config)# router rip
Router(config-router)# version 2
Router(config-router)# network 192.168.10.0
Router(config-router)# network 10.0.0.0
Router(config-router)# no auto-summary
```

Verify:

```bash
Router# show ip protocols
Router# show ip route
```

RIP routes are identified by `R`.

---

## 6. OSPF Single-Area Routing

```bash
Router# configure terminal
Router(config)# router ospf 1
Router(config-router)# network 192.168.1.0 0.0.0.255 area 0
Router(config-router)# network 10.1.1.0 0.0.0.3 area 0
```

Verify:

```bash
Router# show ip ospf neighbor
Router# show ip route
```

OSPF routes are identified by `O`.

---

## 7. EIGRP

```bash
Router# configure terminal
Router(config)# router eigrp 10
Router(config-router)# network 192.168.1.0 0.0.0.255
Router(config-router)# network 10.0.0.0 0.0.0.3
Router(config-router)# no auto-summary
```

Verify:

```bash
Router# show ip eigrp neighbors
Router# show ip route
```

EIGRP routes are identified by `D`.

---

# 🧰 Verification Command Matrix

| Goal | Cisco IOS Command |
| :--- | :--- |
| Check interface state | `show ip interface brief` |
| Check VLANs | `show vlan brief` |
| Check trunks | `show interfaces trunk` |
| Check STP | `show spanning-tree` |
| Check EtherChannel | `show etherchannel summary` |
| Check LACP neighbors | `show lacp neighbor` |
| Check routing table | `show ip route` |
| Check routing protocols | `show ip protocols` |
| Check OSPF neighbors | `show ip ospf neighbor` |
| Check EIGRP neighbors | `show ip eigrp neighbors` |
| Test connectivity | `ping <destination-ip>` |
| Trace a path | `traceroute <destination-ip>` |

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
        │ FIND FAILURE  │
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

> **A lab is not finished when the configuration is typed. It is finished when the behavior is verified.**

---

# 🧠 Concepts Practiced

### 🔀 Switching
VLANs • Segmentation • Access Ports • Trunks • 802.1Q • Inter-VLAN Routing • Router-on-a-Stick • EtherChannel • LACP • Port-Channel • STP • RSTP • Loop Prevention

### 🧩 Subnetting
VLSM • IP Address Allocation • Subnet Masks • Network & Host Addressing

### 🛣️ Routing
RIPv2 • OSPF • EIGRP • Dynamic Routing • Routing Tables • Neighbor Relationships

### 🔍 Troubleshooting
Interface Verification • VLAN Verification • Trunk Verification • STP Verification • EtherChannel Verification • LACP Verification • Ping • Traceroute • Routing Table Analysis

---

# 📈 Learning Progression

```text
VLAN
  ↓
Trunking
  ↓
Inter-VLAN Routing
  ↓
STP / RSTP
  ↓
EtherChannel / LACP
  ↓
VLSM & IP Addressing
  ↓
RIPv2 → OSPF → EIGRP
  ↓
Verification & Troubleshooting
  ↓
Advanced Networking & Security
```

---

# 🚀 Future Labs

Planned expansion:

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
