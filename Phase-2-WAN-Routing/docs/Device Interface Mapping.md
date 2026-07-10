## DSW1

|Interface|Connected To|
|---|---|
|Fa0/1|ASW1|
|Fa0/23|DSW2|
|Fa0/24|RTR-2|

---

## RTR-2

| Interface | Connected To |
| --------- | ------------ |
| Fa0/1     | DSW1         |
| S0/0/0    | RTR-3        |

---

## RTR-3

|Interface|Connected To|
|---|---|
|S0/0/0|RTR-2|
|S0/0/1|RTR-4|

---

## RTR-4

|Interface|Connected To|
|---|---|
|S0/0/0|RTR-3|

**WAN Links:** Serial point-to-point links use a DCE clock rate of **128000 bps** for lab simulation. In production networks, clocking is typically provided by the service provider rather than configured on customer routers.