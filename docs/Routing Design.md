## DSW1 (Core Layer 3 Switching)

- Inter-VLAN routing enabled (`ip routing`)
- SVIs configured:

|VLAN|SVI IP|
|---|---|
|10|10.10.10.1|
|20|10.10.20.1|
|99|10.10.99.1|

---

## RTR-2 (Edge Router)

- Interface to DSW1: `10.10.99.31/24`
- DHCP server for VLAN 10 and VLAN 20
- Static routes configured for return traffic to internal VLANs
