## Campus Networks

|VLAN|Purpose|Network|Gateway|
|---|---|---|---|
|10|Users|10.10.10.0/24|10.10.10.1|
|20|Servers/Lab|10.10.20.0/24|10.10.20.1|
|99|Management / Transit|10.10.99.0/24|10.10.99.1|

---

## Transit & WAN Networks

| Link          | Network        | Usable Addresses |
| ------------- | -------------- | ---------------- |
| DSW1 ↔ RTR-2  | 10.10.100.0/30 | .1 – .2          |
| RTR-2 ↔ RTR-3 | 10.10.100.4/30 | .5 – .6          |
| RTR-3 ↔ RTR-4 | 10.10.100.8/30 | .9 – .10         |

---

## Interface Addressing

| Device | Interface | IP Address      |
| ------ | --------- | --------------- |
| DSW1   | VLAN10    | 10.10.10.1/24   |
| DSW1   | VLAN20    | 10.10.20.1/24   |
| DSW1   | VLAN99    | 10.10.99.1/24   |
| DSW1   | Fa0/24    | 10.10.100.1/30  |
| RTR-2  | Fa0/1     | 10.10.100.2/30  |
| RTR-2  | S0/0/0    | 10.10.100.5/30  |
| RTR-3  | S0/0/0    | 10.10.100.6/30  |
| RTR-3  | S0/0/1    | 10.10.100.9/30  |
| RTR-4  | S0/0/0    | 10.10.100.10/30 |

## Loopback Interfaces

| Device | Loopback      |
| ------ | ------------- |
| RTR-2  | 10.255.2.2/32 |
| RTR-3  | 10.255.3.3/32 |
| RTR-4  | 10.255.4.4/32 |
| DSW1   | 10.255.1.1/32 |
