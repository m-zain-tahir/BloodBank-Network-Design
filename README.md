# 🌐 Blood Bank VLAN Network — Cisco Packet Tracer

> VLAN-based 3-Tier Hierarchical Network for a Blood Bank Organization  
> **Computer Networks Semester Project — University of Lahore, Fall 2025**

---

## Master Mind
| Name | SAP ID |
|------|--------|
| Muhammad Zain Tahir | 70174031 |

**Instructor:** Syed Habib Ullah Shah
**Department:** Software Engineering, University of Lahore

---

## 📌 Project Overview

This project designs and implements a **secure, scalable, and fully functional computer network** for a Blood Bank organization using **Cisco Packet Tracer**. The network logically separates all departments using **VLANs**, enables controlled inter-department communication via **Router-on-a-Stick**, and provides automatic IP addressing through a **centralized DHCP + DNS server**.

---

## 🏗️ Network Architecture — 3-Tier Hierarchical Model

```
                        [ Router ]
                            |
                      [ Core Switch ]
                     /      |       \
           [Dist-SW1]  [Dist-SW2]  [Dist-SW3]  [Dist-SW4]
              |              |           |            |
         [Access SWs]  [Access SWs] [Access SWs] [Access SWs]
              |              |           |            |
           [PCs]          [PCs]       [PCs]        [PCs]
```

| Tier | Devices | Role |
|------|---------|------|
| **Core** | 1 Core Switch + Router | Inter-VLAN routing, backbone connectivity |
| **Distribution** | 4 Distribution Switches (2960-24TT) | VLAN aggregation, trunk links |
| **Access** | Multiple Access Switches (2960-24TT) | End-device connectivity per department |

---

## 📋 VLAN Design

| Department | VLAN ID | Subnet | Default Gateway |
|------------|---------|--------|-----------------|
| Registration Department | 10 | 192.168.0.0/28 | 192.168.0.1 |
| Donor Screening | 20 | 192.168.0.16/28 | 192.168.0.17 |
| Blood Collection | 30 | 192.168.0.32/28 | 192.168.0.33 |
| Testing & Lab | 40 | 192.168.0.48/28 | 192.168.0.49 |
| Storage & Inventory | 50 | 192.168.0.64/28 | 192.168.0.65 |
| Testing Distribution | 60 | 192.168.0.80/28 | 192.168.0.81 |
| Server VLAN | 70 | 192.168.0.96/28 | 192.168.0.97 |

> Each VLAN uses a **/28 subnet** — 16 total IPs, 14 usable hosts per department.

---

## ⚙️ Key Features

- **3-Tier Hierarchy** — Core, Distribution, and Access layers for scalability and fault isolation
- **7 VLANs** — Each department fully isolated at Layer 2
- **Router-on-a-Stick** — Single router interface with sub-interfaces for inter-VLAN routing
- **Centralized DHCP + DNS Server** — Automatic IP assignment for all PCs across all VLANs
- **Trunk Links** — Between all switches to carry multi-VLAN traffic
- **20+ End Devices** — PCs distributed across all 7 departments

---

## 🛠️ Technologies Used

![Cisco](https://img.shields.io/badge/Cisco-Packet%20Tracer-blue?style=flat-square&logo=cisco)
![Networking](https://img.shields.io/badge/Concepts-VLANs%20%7C%20Trunking%20%7C%20DHCP%20%7C%20DNS-lightgrey?style=flat-square)
![Routing](https://img.shields.io/badge/Routing-Router--on--a--Stick-orange?style=flat-square)
![Subnetting](https://img.shields.io/badge/Subnetting-%2F28-green?style=flat-square)

---

## 📁 Repository Contents

| File | Description |
|------|-------------|
| `Cisco.Project.Final.pkt` | Cisco Packet Tracer simulation file |
| `Computer Networks Project Documentation.pdf` | Full project documentation |

---

## 🚀 How to Open

1. Install **Cisco Packet Tracer** (v8.0 or later recommended)
2. Download `Cisco.Project.Final.pkt`
3. Open the file in Packet Tracer
4. Explore the topology, ping between departments, and verify DHCP assignments

---

<p align="center">
  <i>Built as part of the Computer Networks course — Fall 2025, University of Lahore</i>
</p>
