## Layer 2 Validation

- VLANs 10, 20, 99 created on all switches
- Trunk links operational between ASW ↔ DSW layers
- VLAN tagging confirmed across uplinks

---

## Layer 3 Validation (DSW1)

- SVIs operational and up/up
- Inter-VLAN routing functional
- Routing table correctly shows all connected networks

---

## Edge Routing (RTR-2)

- VLAN 99 connectivity established successfully
- Static routes added for VLAN 10 and VLAN 20 return paths
- Bidirectional communication restored after route configuration

---

## End-to-End Connectivity

- PCs successfully receive DHCP addresses
- Inter-VLAN ping successful
- DSW1 ↔ RTR-2 connectivity verified across all VLANs
