# 🌐 Cisco Packet Tracer — Hands-on Networking & Security Labs

Welcome to my **Computer Networking Practical Lab Repository**.

This repository documents my hands-on practice with **Cisco Packet Tracer**, covering switching, VLANs, Inter-VLAN Routing, subnetting, and dynamic routing protocols.

The goal of this repository is to build practical skills in **network configuration, IP addressing, routing, network segmentation, troubleshooting, and Cisco IOS CLI**.

---

## 📌 Repository Overview & Visual Proofs

| Category       | Lab Topic                                  | Protocol / Concept                             | Topology Preview                                                                                              | Lab Files & Visuals                                                                                                  |
| :------------- | :----------------------------------------- | :--------------------------------------------- | :------------------------------------------------------------------------------------------------------------ | :------------------------------------------------------------------------------------------------------------------- |
| **Switching**  | Virtual Local Area Network                 | VLAN Segmentation & Trunking (802.1Q)          | <img src="./01-Switching/VLAN%20images/vlan%201.png" width="280px" alt="VLAN Topology">                       | [📁 Lab File](./01-Switching/VLAN%20lab.pkt)<br>[🖼️ Screenshots](./01-Switching/VLAN%20images/)                     |
| **Switching**  | Inter-VLAN Routing                         | Router-on-a-Stick, 802.1Q & VLAN Communication | <img src="./01-Switching/inter%20VLAN%20images/inter%20vlan%201.png" width="280px" alt="Inter-VLAN Topology"> | [📁 Lab File](./01-Switching/Inter-VLAN%20Routing.pkt)<br>[🖼️ 2 Screenshots](./01-Switching/inter%20VLAN%20images/) |
| **Subnetting** | Variable Length Subnet Masking             | VLSM & IP Address Allocation                   | <img src="./02-Subnetting/VLSM%20images/vlsm%201.png" width="280px" alt="VLSM Topology">                      | [📁 Lab File](./02-Subnetting/VLSM%20lab.pkt)<br>[🖼️ Screenshots](./02-Subnetting/VLSM%20images/)                   |
| **Routing**    | Routing Information Protocol               | RIPv2 Distance Vector                          | <img src="./03-Routing/RIP%20images/rip1.jpg" width="280px" alt="RIP Topology">                               | [📁 Lab File](./03-Routing/RIP%20Lab.pkt)<br>[🖼️ Screenshots](./03-Routing/RIP%20images/)                           |
| **Routing**    | Open Shortest Path First                   | OSPF Single-Area Link-State                    | <img src="./03-Routing/OSPF%20images/ospf1.jpg" width="280px" alt="OSPF Topology">                            | [📁 Lab File](./03-Routing/ospf%20lab.pkt)<br>[🖼️ Screenshots](./03-Routing/OSPF%20images/)                         |
| **Routing**    | Enhanced Interior Gateway Routing Protocol | EIGRP / Multi-Router Setup                     | <img src="./03-Routing/EIGRP%20images/eigrp1.jpg" width="280px" alt="EIGRP Topology">                         | [📁 Lab File](./03-Routing/dynamic%20routing.pkt)<br>[🖼️ Screenshots](./03-Routing/EIGRP%20images/)                 |

---

## 🗂️ Repository Structure

```text
Cisco-Packet-Tracer-Labs/
│
├── 01-Switching/
│   ├── VLAN lab.pkt
│   ├── VLAN images/
│   │   └── vlan 1.png
│   │
│   ├── Inter-VLAN Routing.pkt
│   └── inter VLAN images/
│       ├── inter vlan 1.png
│       └── inter vlan 2.png
│
├── 02-Subnetting/
│   ├── VLSM lab.pkt
│   └── VLSM images/
│
├── 03-Routing/
│   ├── RIP Lab.pkt
│   ├── ospf lab.pkt
│   ├── dynamic routing.pkt
│   │
│   ├── RIP images/
│   ├── OSPF images/
│   └── EIGRP images/
│
└── README.md
```

---

# 🛠️ Key CLI Configurations

## 1. VLAN & Trunking

VLANs (**Virtual Local Area Networks**) logically divide a network into separate broadcast domains.

### Create VLAN

```bash
Switch# configure terminal
Switch(config)# vlan 10
Switch(config-vlan)# name IT_Dept
Switch(config-vlan)# exit
```

### Configure Access Port

```bash
Switch(config)# interface FastEthernet 0/1
Switch(config-if)# switchport mode access
Switch(config-if)# switchport access vlan 10
Switch(config-if)# exit
```

### Configure Trunk Port

```bash
Switch(config)# interface GigabitEthernet 0/1
Switch(config-if)# switchport mode trunk
Switch(config-if)# exit
```

### Verify VLANs

```bash
Switch# show vlan brief
```

### Verify Trunk

```bash
Switch# show interfaces trunk
```

---

# 2. Inter-VLAN Routing — Router-on-a-Stick

Inter-VLAN Routing allows devices belonging to **different VLANs** to communicate with each other through a Layer 3 device.

This lab uses the **Router-on-a-Stick** method, where one physical router interface is divided into multiple sub-interfaces.

Each sub-interface is associated with a VLAN and acts as its **default gateway**.

### Configure Router Sub-Interfaces

```bash
Router# configure terminal

Router(config)# interface GigabitEthernet 0/0.10
Router(config-subif)# encapsulation dot1Q 10
Router(config-subif)# ip address 192.168.1.1 255.255.255.0
Router(config-subif)# exit

Router(config)# interface GigabitEthernet 0/0.20
Router(config-subif)# encapsulation dot1Q 20
Router(config-subif)# ip address 192.168.2.1 255.255.255.0
Router(config-subif)# exit

Router(config)# interface GigabitEthernet 0/0.30
Router(config-subif)# encapsulation dot1Q 30
Router(config-subif)# ip address 192.168.3.1 255.255.255.0
Router(config-subif)# exit
```

### Configure Switch Trunk

```bash
Switch# configure terminal
Switch(config)# interface GigabitEthernet 0/1
Switch(config-if)# switchport mode trunk
Switch(config-if)# exit
```

### Verify VLANs

```bash
Switch# show vlan brief
```

### Verify Trunk

```bash
Switch# show interfaces trunk
```

### Verify Router Interfaces

```bash
Router# show ip interface brief
```

### Verify Routing Table

```bash
Router# show ip route
```

### Test Inter-VLAN Connectivity

```bash
PC> ping <destination-ip>
```

A successful ping between devices in different VLANs confirms that **Inter-VLAN Routing** is functioning correctly.

### 🖼️ Lab Screenshots

<p align="center">
  <img src="./01-Switching/inter%20VLAN%20images/inter%20vlan%201.png" width="45%" alt="Inter-VLAN Lab 1">
  <img src="./01-Switching/inter%20VLAN%20images/inter%20vlan%202.png" width="45%" alt="Inter-VLAN Lab 2">
</p>

---

# 3. VLSM & IP Address Allocation

VLSM (**Variable Length Subnet Masking**) allows a network to use different subnet sizes according to the number of hosts required.

### Configure Sub-Interfaces

```bash
Router# configure terminal

Router(config)# interface GigabitEthernet 0/0.10
Router(config-subif)# encapsulation dot1Q 10
Router(config-subif)# ip address 192.168.1.1 255.255.255.192
Router(config-subif)# exit

Router(config)# interface GigabitEthernet 0/0.20
Router(config-subif)# encapsulation dot1Q 20
Router(config-subif)# ip address 192.168.1.65 255.255.255.224
Router(config-subif)# exit
```

### Verify Interfaces

```bash
Router# show ip interface brief
```

### Verify Routing Table

```bash
Router# show ip route
```

---

# 4. RIPv2 Dynamic Routing

RIP (**Routing Information Protocol**) is a distance-vector dynamic routing protocol.

### Configuration

```bash
Router# configure terminal

Router(config)# router rip
Router(config-router)# version 2
Router(config-router)# network 192.168.10.0
Router(config-router)# network 10.0.0.0
Router(config-router)# no auto-summary
```

### Verify RIP

```bash
Router# show ip protocols
```

```bash
Router# show ip route
```

RIP-learned routes are identified by:

```text
R
```

---

# 5. OSPF Single-Area Routing

OSPF (**Open Shortest Path First**) is a link-state dynamic routing protocol.

This lab uses **Area 0**, the OSPF backbone area.

### Configuration

```bash
Router# configure terminal

Router(config)# router ospf 1
Router(config-router)# network 192.168.1.0 0.0.0.255 area 0
Router(config-router)# network 10.1.1.0 0.0.0.3 area 0
```

### Verify OSPF

```bash
Router# show ip protocols
```

```bash
Router# show ip ospf neighbor
```

```bash
Router# show ip route
```

OSPF-learned routes are identified by:

```text
O
```

---

# 6. EIGRP Configuration

EIGRP (**Enhanced Interior Gateway Routing Protocol**) is a dynamic routing protocol developed by Cisco.

### Configuration

```bash
Router# configure terminal

Router(config)# router eigrp 10
Router(config-router)# network 192.168.1.0 0.0.0.255
Router(config-router)# network 10.0.0.0 0.0.0.3
Router(config-router)# no auto-summary
```

### Verify EIGRP

```bash
Router# show ip protocols
```

```bash
Router# show ip eigrp neighbors
```

```bash
Router# show ip route
```

EIGRP-learned routes are identified by:

```text
D
```

---

# 🔍 Common Verification Commands

### Check Interfaces

```bash
Router# show ip interface brief
```

### Check Routing Table

```bash
Router# show ip route
```

### Check Routing Protocols

```bash
Router# show ip protocols
```

### Test Connectivity

```bash
Router# ping <destination-ip>
```

### Trace Network Path

```bash
Router# traceroute <destination-ip>
```

### Check VLANs

```bash
Switch# show vlan brief
```

### Check Trunk Links

```bash
Switch# show interfaces trunk
```

### Check OSPF Neighbors

```bash
Router# show ip ospf neighbor
```

### Check EIGRP Neighbors

```bash
Router# show ip eigrp neighbors
```

---

# 🧪 Lab Verification Workflow

After configuring a topology, follow this general workflow:

```text
1. Configure device interfaces
        ↓
2. Assign IP addresses
        ↓
3. Configure VLANs / Sub-Interfaces
        ↓
4. Configure trunk links
        ↓
5. Configure routing protocol
        ↓
6. Verify interfaces
        ↓
7. Verify VLANs and trunks
        ↓
8. Verify routing table
        ↓
9. Check routing neighbors
        ↓
10. Test connectivity using ping
        ↓
11. Use traceroute for path verification
```

---

# 📚 Concepts Practiced

### Switching

* VLAN Configuration
* VLAN Segmentation
* Access Ports
* Trunk Ports
* 802.1Q Encapsulation
* Inter-VLAN Routing
* Router-on-a-Stick
* Router Sub-Interfaces
* VLAN Communication

### Subnetting

* VLSM
* IP Address Allocation
* Subnet Masks
* Network & Host Addressing

### Routing

* RIPv2
* OSPF
* EIGRP
* Dynamic Routing
* Routing Tables
* Routing Protocol Verification
* Neighbor Relationships

### Troubleshooting

* Interface Verification
* VLAN Verification
* Trunk Verification
* Connectivity Testing
* Ping
* Traceroute
* Routing Table Analysis

---

# 🎯 Purpose of This Repository

This repository serves as a practical record of my **Cisco networking journey** and a personal reference for Cisco IOS commands, Packet Tracer configurations, and troubleshooting techniques.

It can also be used as a quick revision guide for:

**VLAN → Inter-VLAN Routing → VLSM → RIP → OSPF → EIGRP → Verification → Troubleshooting**

---

# 🚀 Future Labs

More networking and cybersecurity labs will be added as I continue learning and practicing.

Planned topics include:

* Static Routing
* DHCP
* NAT
* ACLs
* STP
* EtherChannel
* Advanced OSPF
* Network Security
* Cisco Troubleshooting
* Additional Packet Tracer Topologies

---

## 👨‍💻 Author

**Mashhood Ali Khan**

**Cybersecurity Student | Networking Enthusiast**

> Learning networking by building, configuring, testing, and troubleshooting real-world-style topologies in Cisco Packet Tracer.
