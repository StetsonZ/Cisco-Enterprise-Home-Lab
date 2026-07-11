# Cisco Enterprise Home Lab

## Overview

This repository documents the design, implementation, and validation of a multi-phase Cisco enterprise network built using physical Cisco routers, switches, and firewalls.

The purpose of this project is to develop and demonstrate practical enterprise networking skills by progressively implementing core networking technologies in a structured lab environment. Each phase builds upon the previous one while following industry best practices for network design, documentation, and troubleshooting.

---

## Hardware

### Routers
- Cisco 2811 Integrated Services Routers
- Cisco 2821 Integrated Services Router

### Switches
- Cisco Catalyst 3560 Layer 3 Switches
- Cisco Catalyst 2960 Layer 2 Switches

### Firewalls
- Cisco ASA 5510
- Cisco ASA 5505

---

## Project Roadmap

| Phase | Status | Technologies |
|-------|:------:|--------------|
| **Phase 1 – Campus Network Foundation** | ✅ Complete | VLANs, Layer 2 Switching, Inter-VLAN Routing, DHCP |
| **Phase 2 – WAN Routing** | ✅ Complete | Serial WAN Links, Static Routing, OSPF |
| **Phase 3 – Network Redundancy** | 🚧 In Progress | HSRP, EtherChannel, STP, Redundant Links |
| **Phase 4 – Network Security** | ⏳ Planned | ASA Firewall, ACLs, NAT, VPN |
| **Phase 5 – Enterprise Services** | ⏳ Planned | Monitoring, Logging, Network Services |

---

## Skills Demonstrated

### Routing & Switching
- VLAN implementation
- Inter-VLAN routing
- Layer 2 switching
- Layer 3 switching
- 802.1Q trunking
- Static routing
- OSPF dynamic routing

### WAN Technologies
- Serial point-to-point links
- DCE/DTE configuration
- /30 WAN addressing
- Loopback interfaces
- Route advertisement

### Enterprise Networking
- IP addressing design
- DHCP
- Network troubleshooting
- Configuration backup
- Network documentation
- End-to-end validation

---

## Repository Structure

```text
Cisco-Enterprise-Home-Lab
│
├── README.md
│
├── Phase-1-Campus-Network
│   ├── README.md
│   ├── configs
│   ├── docs
│   └── images
│
├── Phase-2-WAN-Routing
│   ├── README.md
│   ├── configs
│   ├── docs
│   └── images
│
├── Phase-3-Network-Redundancy
│   ├── README.md
│   ├── configs
│   ├── docs
│   └── images
│
├── Phase-4-Network-Security
│   ├── README.md
│   ├── configs
│   ├── docs
│   └── images
│
└── Phase-5-Enterprise-Services
    ├── README.md
    ├── configs
    ├── docs
    └── images
```

---

## Completed Phases

### Phase 1 – Campus Network Foundation

Designed and implemented a hierarchical campus network featuring:

- VLAN segmentation
- 802.1Q trunking
- Layer 3 inter-VLAN routing
- DHCP services
- DHCP relay
- End-to-end connectivity verification

📁 **Folder:** `Phase-1-Campus-Network`

---

### Phase 2 – WAN Routing

Expanded the campus network into a routed WAN by implementing:

- Serial point-to-point WAN links
- Static routing
- OSPF Area 0
- Loopback interfaces
- Dynamic route advertisement
- Routing verification and troubleshooting

📁 **Folder:** `Phase-2-WAN-Routing`

---

## Upcoming Phases

### Phase 3 – Network Redundancy
- HSRP
- EtherChannel
- Spanning Tree optimization
- Redundant Layer 3 distribution
- Network failover testing

### Phase 4 – Network Security
- Cisco ASA firewall deployment
- Access Control Lists (ACLs)
- Network Address Translation (NAT)
- Site-to-site VPN

### Phase 5 – Enterprise Services
- Syslog
- NTP
- SNMP
- SSH management
- Network monitoring
- Additional enterprise services

---

## Documentation

Each phase includes:

- Project overview
- Network topology
- IP addressing plan
- Configuration backups
- Verification results
- Troubleshooting notes
- Lessons learned

---

## Goal

This project is designed to simulate the implementation of an enterprise network using physical Cisco hardware while documenting each stage of the deployment. As additional phases are completed, this repository will continue to evolve into a comprehensive networking portfolio demonstrating practical experience with enterprise routing, switching, redundancy, security, and network services.
