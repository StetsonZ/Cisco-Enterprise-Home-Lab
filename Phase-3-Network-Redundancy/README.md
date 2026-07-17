# Phase 3 - Campus Redundancy

## Overview

Phase 3 focused on transforming the campus network into a highly available enterprise design by implementing redundancy at both Layer 2 and Layer 3.

This phase introduced redundant distribution switching, first-hop redundancy, dynamic routing improvements, link aggregation, spanning-tree optimization, and extensive failover testing.

The goal was to design a campus network capable of maintaining connectivity during device and link failures while automatically recovering through redundancy protocols.

---

# Objectives

- Convert the campus network into a redundant architecture
- Implement gateway redundancy using HSRP
- Add redundant access-layer uplinks
- Configure Layer 3 EtherChannel using LACP
- Optimize Layer 2 forwarding with Rapid PVST+
- Expand OSPF to the secondary distribution switch
- Validate network resiliency through failure testing

---

# Topology Changes

Phase 3 introduced the following design improvements:

- DSW1 and DSW2 now operate as Layer 3 distribution switches
- Access switches are dual-homed to both distribution switches
- DSW1 and DSW2 are connected through a Layer 3 EtherChannel
- HSRP provides redundant default gateways
- Rapid PVST+ provides loop prevention and optimized forwarding
- OSPF provides dynamic routing between the campus and WAN

![Phase 3 Logical Topology](./Images/Phase%203%20Logical%20Topology.png)

![Phase 3 Hardware](./Images/Phase%203%20hardware.jpeg)

---

# Technologies Implemented

## First Hop Redundancy

## HSRP

Implemented HSRP across VLANs 10, 20, and 99 to provide redundant default gateways.

| VLAN | Active Router | Standby Router |
|---|---|---|
| VLAN 10 | DSW1 | DSW2 |
| VLAN 20 | DSW2 | DSW1 |
| VLAN 99 | DSW1 | DSW2 |

Traffic was load balanced between distribution switches while maintaining gateway availability.

---

# Layer 3 EtherChannel

Implemented an LACP Layer 3 EtherChannel between DSW1 and DSW2.

Purpose:

- Increase bandwidth
- Provide link redundancy
- Maintain routing connectivity if a physical link fails
