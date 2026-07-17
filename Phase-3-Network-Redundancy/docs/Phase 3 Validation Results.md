## Failover Test Results

| Test                          | Result                                                           | Status |
| ----------------------------- | ---------------------------------------------------------------- | ------ |
| DSW1 failure                  | HSRP failed over to DSW2, network remained operational           | ✅ Pass |
| DSW1 recovery                 | HSRP preemption returned gateway ownership to DSW1               | ✅ Pass |
| DSW2 failure                  | DSW1 maintained gateway and routing functionality                | ✅ Pass |
| EtherChannel member failure   | Port-Channel remained operational with one active link           | ✅ Pass |
| EtherChannel recovery         | Member link successfully rejoined the Port-Channel               | ✅ Pass |
| ASW1 uplink failure           | STP unblocked the alternate path and connectivity was maintained | ✅ Pass |
| Layer 3 EtherChannel failure  | OSPF adjacency was lost, routes were removed as expected         | ✅ Pass |
| Layer 3 EtherChannel recovery | OSPF adjacency reformed and routes were restored                 | ✅ Pass |
