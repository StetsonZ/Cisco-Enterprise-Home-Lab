# Phase 3 — Campus Redundancy & High Availability

## Part 1 — Physical Topology Changes

### Objectives

- Add redundant uplinks from both access switches.

### Tasks

- Connect ASW1 to DSW2.
- Connect ASW2 to DSW1.
- Connect DSW1 ↔ DSW2 using two FastEthernet links (Fa0/22 and Fa0/23, for example).
- Verify interfaces are up/up.

---

# Part 2 — Layer 3 Distribution Configuration

### Objectives

- Convert DSW2 into a Layer 3 distribution switch.
- Create a Layer 3 EtherChannel between DSW1 and DSW2.
- Configure DSW2 to operate as a redundant distribution switch.

### Tasks

- Enable `ip routing`.
- Create VLAN 10, 20, and 99.
- Create SVIs.
- Assign SVI IP addresses (.2/.3 scheme).
- Configure the DSW1–DSW2 links as an LACP Layer 3 EtherChannel.
- Configure the Layer 3 Port-Channel IP addresses.
- Configure trunk ports
- Verify routing table.

---

# Part 3 — HSRP Configuration
### Objectives

Provide redundant default gateways.

### Tasks

Configure HSRP for:

- VLAN 10
- VLAN 20
- VLAN 99

Configure:

- Virtual IPs
- Priorities
- Preemption

Example load balancing:

|VLAN|Active|Standby|
|---|---|---|
|10|DSW1|DSW2|
|20|DSW2|DSW1|
|99|DSW1|DSW2|

Verify:

- Active/Standby status
- Virtual MAC addresses

---

# Part 4 — OSPF Expansion

### Objectives

Extend OSPF to include DSW2.

### Tasks

- Configure OSPF Process 1.
- Advertise:
    - VLAN 10
    - VLAN 20
    - VLAN 99
    - DSW2 Loopback
    - Layer 3 EtherChannel
- Configure passive interfaces on the SVIs.
- Verify:
    - Neighbor adjacency between DSW1 and DSW2.
    - Routing tables.
    - Reachability to RTR-2, RTR-3, and RTR-4.

---

# Part 5 — Spanning Tree Optimization

### Objectives

Optimize Layer 2 forwarding.

### Tasks

Enable:

- Rapid PVST+

Configure:

- DSW1 Root Primary for VLAN 10 & 99
- DSW2 Root Primary for VLAN 20

Verify:

- Root bridge election
- Port roles
- Blocked ports
- Forwarding ports

---

# Part 6 — Verification

### Objectives

Double check and verify redundancy and aggregation.

### Tasks

Verify:

- EtherChannel
- STP
- OSPF
- HSRP

---

# Part 7 — Failover Testing

This is where the fun starts.

## Test 1

Shutdown DSW1.

Verify:

- HSRP failover
- Pings continue
- OSPF converges

---

## Test 2

Bring DSW1 back online.

Verify:

- Preemption
- Gateway returns to DSW1
---

## Test 3

Shutdown DSW2.

Verify:

- Network remains operational

---

## Test 4

Shutdown one EtherChannel member.

Verify:

- Port-channel stays up

---

## Test 5

Reconnect interface.

Verify:

- EtherChannel rebuilds

---

## Test 6

Disconnect one uplink from ASW1.

Verify:

- STP unblocks the alternate path
- Connectivity remains

---
### Test 7

Shutdown the Layer 3 EtherChannel.

Verify:

- OSPF neighbor loss
- Expected routing behavior
- HSRP state

---
### Test 8

Reconnect the EtherChannel.

Verify:

- OSPF adjacency reforms
- Routes are restored
- HSRP remains stable