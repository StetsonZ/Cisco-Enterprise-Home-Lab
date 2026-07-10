## DSW1 (Core Layer 3 Switch)

| Interface | Connected To | Mode   | VLANs      |
| --------- | ------------ | ------ | ---------- |
| Fa0/1     | ASW1         | Trunk  | 1,10,20,99 |
| Fa0/23    | DSW2         | Trunk  | 1,10,20,99 |
| Fa0/24    | RTR-2        | Access | VLAN 99    |

---

## DSW2 (Distribution / Layer 2 in Phase 1)

| Interface | Connected To | Mode  | VLANs      |
| --------- | ------------ | ----- | ---------- |
| Fa0/1     | ASW2         | Trunk | 1,10,20,99 |
| Fa0/23    | DSW1         | Trunk | 1,10,20,99 |

---

## Access Layer Switches

| Device | Interface | Connected To | Mode   | VLAN       |
| ------ | --------- | ------------ | ------ | ---------- |
| ASW1   | Fa0/1     | DSW1         | Trunk  | 1,10,20,99 |
| ASW1   | Fa0/2     | PC           | Access | 10         |
| ASW2   | Fa0/1     | DSW2         | Trunk  | 1,10,20,99 |
| ASW2   | Fa0/2     | PC           | Access | 20         |
