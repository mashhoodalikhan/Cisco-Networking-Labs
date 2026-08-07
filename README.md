# 🌐 Cisco Packet Tracer - Hands-on Networking & Security Labs

Welcome to my **Computer Networking Practical Lab Repository**!
This repository contains Cisco Packet Tracer labs covering **switching, subnetting, VLANs, trunking, and dynamic routing protocols**.

These labs were created through hands-on practice to build a strong understanding of **network configuration, troubleshooting, routing, and network segmentation**.

---

## 📌 Repository Overview & Visual Proofs

| Category       | Lab Topic                                  | Protocol / Concept                    | Topology Preview                                                                         | Lab Files & Visuals                                                                                           |
| :------------- | :----------------------------------------- | :------------------------------------ | :--------------------------------------------------------------------------------------- | :------------------------------------------------------------------------------------------------------------ |
| **Switching**  | Virtual Local Area Network                 | VLAN Segmentation & Trunking (802.1Q) | <img src="./01-Switching/VLAN%20images/vlan%201.png" width="280px" alt="VLAN Topology">  | [📁 Lab File (`.pkt`)](./01-Switching/VLAN%20lab.pkt)<br>[🖼️ Screenshots](./01-Switching/VLAN%20images/)     |
| **Subnetting** | Variable Length Subnet Masking             | VLSM & IP Address Allocation          | <img src="./02-Subnetting/VLSM%20images/vlsm%201.png" width="280px" alt="VLSM Topology"> | [📁 Lab File (`.pkt`)](./02-Subnetting/VLSM%20lab.pkt)<br>[🖼️ Screenshots](./02-Subnetting/VLSM%20images/)   |
| **Routing**    | Routing Information Protocol               | RIPv2 Distance Vector                 | <img src="./03-Routing/RIP%20images/rip1.jpg" width="280px" alt="RIP Topology">          | [📁 Lab File (`.pkt`)](./03-Routing/RIP%20Lab.pkt)<br>[🖼️ Screenshots](./03-Routing/RIP%20images/)           |
| **Routing**    | Open Shortest Path First                   | OSPF Single-Area Link-State           | <img src="./03-Routing/OSPF%20images/ospf1.jpg" width="280px" alt="OSPF Topology">       | [📁 Lab File (`.pkt`)](./03-Routing/ospf%20lab.pkt)<br>[🖼️ Screenshots](./03-Routing/OSPF%20images/)         |
| **Routing**    | Enhanced Interior Gateway Routing Protocol | EIGRP / Multi-Router Setup            | <img src="./03-Routing/EIGRP%20images/eigrp1.jpg" width="280px" alt="EIGRP Topology">    | [📁 Lab File (`.pkt`)](./03-Routing/dynamic%20routing.pkt)<br>[🖼️ Screenshots](./03-Routing/EIGRP%20images/) |

---

## 🗂️ Repository Structure

```text
Cisco-Packet-Tracer-Labs/
│
├── 01-Switching/
│   ├── VLAN lab.pkt
│   └── VLAN images/
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

# 🛠️ Key CLI Configurations Covered

## 1. VLAN & Trunking Setup

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

### Verify VLAN Configuration

```bash
Switch# show vlan brief
```

### Verify Trunk

```bash
Switch# show interfaces trunk
```

---

## 2. VLSM & Sub-Interface Setup

VLSM (**Variable Length Subnet Masking**) allows different subnet sizes to be assigned according to the number of required hosts.

### Configure Sub-Interface

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

# 3. RIPv2 Dynamic Routing

RIP (**Routing Information Protocol**) is a distance-vector routing protocol.

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

Look for routes marked with:

```text
R
```

`R` indicates a route learned through RIP.

---

# 4. OSPF Single-Area Routing

OSPF (**Open Shortest Path First**) is a link-state dynamic routing protocol.

This lab uses **Area 0**, also known as the backbone area.

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

OSPF-learned routes normally appear with:

```text
O
```

---

# 5. EIGRP Configuration

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

EIGRP-learned routes normally appear with:

```text
D
```

---

# 🔍 Common Verification Commands

These commands are useful for checking whether a Cisco Packet Tracer topology is working correctly.

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

### Trace the Path

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

After configuring a topology, use the following basic workflow:

```text
1. Configure device interfaces
        ↓
2. Assign IP addresses
        ↓
3. Configure VLANs / Sub-Interfaces
        ↓
4. Configure routing protocol
        ↓
5. Verify interfaces
        ↓
6. Verify routing table
        ↓
7. Check neighbors
        ↓
8. Test connectivity using ping
        ↓
9. Use traceroute if required
```

---

# 📚 Concepts Practiced

* VLAN Configuration
* VLAN Segmentation
* Access Ports
* Trunk Ports
* 802.1Q Encapsulation
* Inter-VLAN Routing
* VLSM
* IP Address Allocation
* RIPv2
* OSPF
* EIGRP
* Dynamic Routing
* Routing Tables
* Routing Protocol Verification
* Network Troubleshooting
* Connectivity Testing

---

# 🎯 Purpose of This Repository

The purpose of this repository is to document my **hands-on networking practice** and maintain a reference for Cisco IOS commands and Packet Tracer configurations.

It can also be used as a quick revision guide when reviewing:

**VLAN → VLSM → RIP → OSPF → EIGRP → Routing Verification → Troubleshooting**

---

## 🚀 Future Labs

More networking and cybersecurity labs will be added as I continue learning and practicing:

* Static Routing
* Inter-VLAN Routing
* DHCP
* NAT
* ACLs
* STP
* EtherChannel
* Advanced OSPF
* Network Security
* Cisco Troubleshooting

---

## 👨‍💻 Author

**Mashhood Ali Khan**

Cybersecurity Student | Networking Enthusiast

> Learning networking by building, configuring, testing, and troubleshooting real-world-style topologies in Cisco Packet Tracer.
