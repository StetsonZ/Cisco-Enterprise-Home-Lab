# Phase 2 - WAN Routing & Dynamic Routing

## Overview

Phase 2 expanded the existing campus network into a routed WAN environment using Cisco routers and serial point-to-point connections.

The goal of this phase was to build routing fundamentals by first implementing static routes, validating end-to-end connectivity, and then migrating the network to dynamic routing using OSPF Area 0.

---

## Objectives

Phase 2 focused on:

- Configuring Cisco serial WAN links
- Understanding DCE/DTE clocking
- Implementing point-to-point /30 addressing
- Configuring static routing
- Implementing OSPF dynamic routing
- Establishing OSPF neighbor relationships
- Advertising networks and loopback interfaces
- Validating routing tables and end-to-end connectivity

---

# Network Architecture

The WAN design extends the Phase 1 campus network into a multi-router environment:

 RTR-4
              |
          RTR-3
              |
          RTR-2
              |
            DSW1
              |
         Campus LAN

         ### Device Roles

| Device | Role |
|---|---|
| DSW1 | Layer 3 campus distribution switch and LAN gateway |
| RTR-2 | Headquarters edge router |
| RTR-3 | WAN transit router |
| RTR-4 | Remote branch router |

---

# WAN Addressing

Point-to-point WAN links use /30 networks:

| Link | Network |
|---|---|
| DSW1 ↔ RTR-2 | 10.10.100.0/30 |
| RTR-2 ↔ RTR-3 | 10.10.100.4/30 |
| RTR-3 ↔ RTR-4 | 10.10.100.8/30 |

Serial interfaces were configured with DCE clocking at: 128000 bps

---

# Routing Implementation

## Static Routing

Static routing was implemented first to:

- Validate Layer 3 connectivity
- Confirm routing paths
- Reinforce manual route configuration concepts

Validation included:

- Routing table verification
- End-to-end ping testing
- Traceroute testing

---

## OSPF Dynamic Routing

After validating static routing, the network was migrated to OSPF.

### OSPF Design

| Parameter | Value |
|---|---|
| Process ID | 1 |
| Area | 0 |
| Routing Protocol | OSPF |

OSPF was configured on:

- DSW1
- RTR-2
- RTR-3
- RTR-4

Advertised networks included:

- Campus VLAN networks
- WAN point-to-point networks
- Router loopback interfaces

---

# Loopback Design

Loopback interfaces were configured as stable router identifiers:

| Device | Loopback |
|---|---|
| DSW1 | 10.255.1.1/32 |
| RTR-2 | 10.255.2.2/32 |
| RTR-3 | 10.255.3.3/32 |
| RTR-4 | 10.255.4.4/32 |

These interfaces were advertised through OSPF.

---

# Topology

### Logical Topology

![Logical Topology](images/Phase%202%20Logical%20Topology.png)

---

# Technologies Implemented

- Cisco routing
- Serial WAN connectivity
- DCE/DTE clocking
- Point-to-point addressing
- Static routing
- OSPF Area 0
- Loopback interfaces
- Route advertisement
- Routing verification

---

# Validation Results

Phase 2 successfully achieved:

- All serial interfaces operational
- Successful static routing implementation
- Successful migration to OSPF
- OSPF neighbor adjacencies established
- Dynamic route learning verified
- Successful ping and traceroute validation

---

# Troubleshooting & Lessons Learned

During Phase 2, the addressing design was refined after initial static routing implementation.

The connection between DSW1 and RTR-2 was redesigned from a VLAN 99 transit design to a routed Layer 3 point-to-point connection. This required updating:

- Interface addressing
- Routing configuration
- DHCP configuration

This reinforced the importance of maintaining consistent IP addressing and understanding the impact of design changes across multiple network services.

---

# Documentation

Detailed documentation is available in the `docs` directory:

- [Objective](docs/Objective.md)
- [IP Addressing Scheme](docs/IP%20Addressing%20Scheme.md)
- [Device Interface Mapping](docs/Device%20Interface Mapping.md)
- [Routing Design](docs/Routing%20Design.md)
- [OSPF Design](docs/OSPF%20Design.md)
- [Verification Results](docs/Verification%20Results.md)
- [Troubleshooting](docs/Troubleshooting.md)
- [Phase 2 Conclusion](docs/Phase%202%20Conclusion.md)

---

# Next Phase

Phase 3 will introduce enterprise network redundancy and high availability, including:

- Multiple Layer 3 distribution switches
- HSRP gateway redundancy
- EtherChannel
- STP optimization
- Redundant network paths
