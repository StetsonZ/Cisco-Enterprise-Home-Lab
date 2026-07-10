# Phase 1 - Campus Network Foundation

## Overview

Phase 1 established the foundation of a small enterprise campus network using Cisco switching and routing technologies.

The goal of this phase was to design and implement a segmented campus architecture with Layer 2 access switching, Layer 3 inter-VLAN routing, DHCP services, and edge connectivity.

---

## Objectives

Phase 1 focused on:

- VLAN segmentation
- 802.1Q trunking
- Layer 3 switching and inter-VLAN routing
- DHCP services using a centralized router
- Routed edge connectivity
- End-to-end connectivity validation

---

## Network Architecture

The network was designed using a hierarchical campus model:

- **DSW1** - Layer 3 distribution/core switch responsible for inter-VLAN routing
- **DSW2** - Layer 2 distribution switch
- **ASW1 / ASW2** - Access layer switches
- **RTR-2** - Edge router and DHCP server

### VLAN Design

| VLAN | Purpose | Network | Gateway |
|------|---------|---------|---------|
| 10 | Users | 10.10.10.0/24 | 10.10.10.1 |
| 20 | Servers/Lab | 10.10.20.0/24 | 10.10.20.1 |
| 99 | Management / Transit | 10.10.99.0/24 | 10.10.99.1 |

All default gateways are hosted on DSW1 using Switch Virtual Interfaces (SVIs).

---

## Topology

### Physical Lab

![Physical Lab](images/Phase%201%20Physical%20Lab.jpeg)

### Logical Topology

![Logical Topology](images/Phase%201%20Logical%20Topology.png)

---

## Technologies Implemented

- Cisco Catalyst switching
- VLAN segmentation
- 802.1Q trunking
- Layer 3 switching
- SVIs
- DHCP relay (`ip helper-address`)
- Static routing
- Network troubleshooting and validation

---

## Validation Results

Phase 1 successfully achieved:

- Functional VLAN segmentation
- Working trunk links between switching layers
- Inter-VLAN routing through DSW1
- DHCP address assignment for multiple VLANs
- End-to-end connectivity between internal hosts and edge routing

---

## Documentation

Detailed documentation is available in the `docs` directory:

- [Objective](docs/Objective.md)
- [Network Topology Overview](docs/Network%20Topology%20Overview.md)
- [IP Addressing Scheme](docs/IP%20Addressing%20Scheme.md)
- [Device Interface Mapping](docs/Device%20Interface%20Mapping.md)
- [Routing Design](docs/Routing%20Design.md)
- [DHCP Configuration](docs/DHCP%20Configuration.md)
- [Verification Results](docs/Verification%20Results.md)
- [Troubleshooting Summary](docs/Troubleshooting%20Summary.md)
- [Key Design Lessons Learned](docs/Key%20Design%20Lessons%20Learned.md)
- [Phase 1 Conclusion](docs/Phase%201%20Conclusion.md)

---

## Key Lessons Learned

- Layer 2 connectivity does not guarantee end-to-end communication
- Proper return routing is required for bidirectional communication
- DHCP relay requires complete Layer 3 reachability
- Troubleshooting requires validating each layer individually

---

## Next Phase

Phase 2 expands this campus network into a routed WAN environment by introducing:

- Multi-router connectivity
- Static routing
- OSPF dynamic routing
- Loopback interfaces
- Routing validation and troubleshooting
