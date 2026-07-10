## VLAN Design

|VLAN|Purpose|Network|Default Gateway|
|---|---|---|---|
|10|Users|10.10.10.0/24|10.10.10.1|
|20|Servers/Lab|10.10.20.0/24|10.10.20.1|
|99|Management|10.10.99.0/24|10.10.99.1|

### Design Note

- All default gateways reside on **DSW1 (Layer 3 switch)**.
- VLAN 99 is used as a routed transit/management network between DSW1 and RTR-2.
