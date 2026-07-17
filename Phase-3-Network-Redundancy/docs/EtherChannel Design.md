Protocol:

```
LACP
```

Port Channel 1:

```
DSW1 Fa0/22
DSW1 Fa0/23

DSW2 Fa0/22
DSW2 Fa0/23
```

|Device|Interface|IP Address|Subnet|
|---|---|---|---|
|DSW1|Port-channel1|10.10.101.1|/30|
|DSW2|Port-channel1|10.10.101.2|/30|
|Network||10.10.101.0/30||
|Broadcast||10.10.101.3|

Purpose:

- Increased bandwidth
- Link redundancy
- Simplified STP topology