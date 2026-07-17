# Cisco Enterprise Home Lab

## Overview

This repository documents the design, implementation, and validation of a multi-phase Cisco enterprise network built using physical Cisco routers, switches, and firewalls.

The purpose of this project is to develop and demonstrate practical enterprise networking skills by progressively implementing enterprise technologies in a structured lab environment. Each phase builds upon the previous phase while following industry best practices for network design, documentation, troubleshooting, and validation.

---

# Hardware

## Routers

- Cisco 2811 Integrated Services Routers
- Cisco 2821 Integrated Services Router

## Switches

- Cisco Catalyst 3560 Layer 3 Switches
- Cisco Catalyst 2960 Layer 2 Switches

## Firewalls

- Cisco ASA 5510
- Cisco ASA 5505

---

# Project Roadmap

| Phase | Status | Technologies |
|---|---|---|
| Phase 1 – Campus Network Foundation | ✅ Complete | VLANs, Layer 2 Switching, Inter-VLAN Routing, DHCP |
| Phase 2 – WAN Routing | ✅ Complete | Serial WAN Links, Static Routing, OSPF |
| Phase 3 – Campus Redundancy | ✅ Complete | HSRP, EtherChannel, Rapid PVST+, Redundant Links |
| Phase 4 – Network Security | ⏳ Planned | ACLs, Port Security, SSH, DHCP Snooping, DAI |
| Phase 5 – Enterprise Services | ⏳ Planned | Syslog, NTP, SNMP, Monitoring, Logging |
| Phase 6 – Firewall & Edge Security | ⏳ Planned | ASA Deployment, NAT, VPN, Edge Redundancy |

---

# Skills Demonstrated

## Routing & Switching

- VLAN implementation
- Layer 2 switching
- Layer 3 switching
- Inter-VLAN routing
- 802.1Q trunking
- Static routing
- OSPF dynamic routing
- HSRP first-hop redundancy
- EtherChannel using LACP
- Rapid PVST+ optimization
- Loopback interfaces
- Route advertisement

---

## WAN Technologies

- Serial point-to-point WAN links
- DCE/DTE configuration
- /30 WAN addressing
- Static route configuration
- OSPF Area 0
- Dynamic route exchange
- Routing troubleshooting

---

## Enterprise Networking

- Hierarchical campus network design
- High availability architecture
- IP addressing design
- DHCP services
- DHCP relay
- Network troubleshooting
- Configuration backups
- IOS upgrades
- TFTP file transfers
- Network documentation
- Failure simulation and validation

---

# Repository Structure
Cisco-Enterprise-Home-Lab
│
├── README.md
│
├── images
│   ├── Phase 1 images
│   ├── Phase 2 images
│   └── Phase 3 images
│
├── Phase-1-Campus-Network
│   ├── README.md
│   ├── configs
│   └── docs
│
├── Phase-2-WAN-Routing
│   ├── README.md
│   ├── configs
│   └── docs
│
├── Phase-3-Network-Redundancy
│   ├── README.md
│   ├── configs
│   └── docs
│
├── Phase-4-Network-Security
│   ├── README.md
│   ├── configs
│   └── docs
│
└── Phase-5-Enterprise-Services
    ├── README.md
    ├── configs
    └── docs

---

# Completed Phases

# Phase 1 – Campus Network Foundation

Designed and implemented a hierarchical campus network featuring:

- VLAN segmentation
- 802.1Q trunking
- Layer 3 inter-VLAN routing
- DHCP services
- DHCP relay configuration
- Layer 3 switching
- End-to-end connectivity verification

📁 Folder: `Phase-1-Campus-Network`

---

# Phase 2 – WAN Routing

Expanded the campus network into a routed WAN by implementing:

- Serial point-to-point WAN links
- /30 WAN addressing
- Static routing
- OSPF Area 0
- Loopback interfaces
- Dynamic route advertisement
- Routing verification and troubleshooting

📁 Folder: `Phase-2-WAN-Routing`

---

# Phase 3 – Campus Redundancy

Transformed the campus network into a highly available enterprise design by implementing:

- Redundant Layer 3 distribution switching
- HSRP gateway redundancy
- Layer 3 EtherChannel using LACP
- Redundant access-layer uplinks
- Rapid PVST+ optimization
- OSPF expansion to DSW2
- Network failover testing

Validation included:

- Distribution switch failures
- EtherChannel member failures
- Access uplink failures
- OSPF adjacency failures
- Recovery testing

📁 Folder: `Phase-3-Network-Redundancy`

---

# Upcoming Phases

# Phase 4 – Network Security

Planned implementations:

- Cisco ASA firewall deployment
- Access Control Lists (ACLs)
- Port Security
- DHCP Snooping
- Dynamic ARP Inspection
- IP Source Guard
- SSH management
- Infrastructure hardening

---

# Phase 5 – Enterprise Services

Planned implementations:

- Syslog
- NTP
- SNMP
- Network monitoring
- Centralized logging
- Additional enterprise services

---

# Phase 6 – Firewall & Edge Security

Planned implementations:

- Dual edge router design
- ASA firewall deployment
- NAT/PAT
- Site-to-site VPN
- Firewall policies
- Internet edge security
- High availability firewall design

---

# Documentation

Each completed phase includes:

- Project overview
- Network topology
- IP addressing plan
- Interface mappings
- Configuration documentation
- Verification results
- Troubleshooting notes
- Lessons learned

---

# Goal

This project is designed to simulate the implementation of an enterprise network using physical Cisco hardware while documenting each stage of deployment.

As additional phases are completed, this repository will continue to evolve into a comprehensive networking portfolio demonstrating practical experience with:

- Enterprise routing
- Campus switching
- High availability
- Network security
- Firewall technologies
- Monitoring and network services

The final goal is to build a complete enterprise network environment that demonstrates real-world design, implementation, troubleshooting, and operational skills.
