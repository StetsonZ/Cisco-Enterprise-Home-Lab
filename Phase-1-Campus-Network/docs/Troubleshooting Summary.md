### Issue 1: DHCP failure for VLAN 10 and 20

- **Symptom:** Clients did not receive IP addresses
- **Cause:** 
	- Missing return routes on RTR-2 for VLAN 10 and VLAN 20 networks 
	- DSW1 port connected to RTR-2 not in access mode with VLAN 99 access
	- DSW1 was not set as a DHCP relay agent
- **Fix:** Added static routes pointing to 10.10.99.1, changed port to access port allowing VLAN 99, and added `ip helper-address 10.10.99.31` command to VLANs 10 and 20 SVIs

---

### Issue 2: Partial connectivity (VLAN 99 only working)

- **Symptom:** Only VLAN 99 could reach RTR-2
- **Cause:** Only directly connected network had return path
- **Fix:** Added routing for internal VLAN subnets

---

### Issue 3: Initial DHCP renewal issues on Windows clients

- **Symptom:** DHCP renew failed / hung
- **Cause:** No valid DHCP lease due to upstream routing failure
- **Fix:** Resolved after routing correction on RTR-2
