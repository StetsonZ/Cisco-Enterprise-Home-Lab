## DHCP Pools (RTR-2)

### VLAN 10 Pool

- Network: 10.10.10.0/24
- Default Gateway: 10.10.10.1
- Excluded Range: 10.10.10.100 – 10.10.10.199

### VLAN 20 Pool

- Network: 10.10.20.0/24
- Default Gateway: 10.10.20.1
- Excluded Range: 10.10.20.100 – 10.10.20.199

### DHCP Relay

Configured on DSW1 SVIs:

- `ip helper-address 10.10.99.31`
