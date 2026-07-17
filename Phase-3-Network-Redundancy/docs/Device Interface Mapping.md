## DSW1

| Interface | Connected To        |
| --------- | ------------------- |
| Fa0/1     | ASW1                |
| Fa0/2     | ASW2                |
| Fa0/22-23 | DSW2 (EtherChannel) |
| Fa0/24    | RTR-2               |

---

## DSW2

| Interface | Connected To        |
| --------- | ------------------- |
| Fa0/1     | ASW2                |
| Fa0/2     | ASW1                |
| Fa0/22-23 | DSW1 (EtherChannel) |


---

## ASW1

| Interface | Connected To |
| --------- | ------------ |
| Fa0/1     | DSW1         |
| Fa0/24    | DSW2         |

---

## ASW2

| Interface | Connected To |
| --------- | ------------ |
| Fa0/24    | DSW1         |
| Fa0/1     | DSW2         |