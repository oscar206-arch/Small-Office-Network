\# Network Design



\## Overview



The network simulates a small office with separate

Administration, Staff, and Guest networks.



\## Topology



\- One router

\- One Layer 2 switch

\- Six PCs

\- Three VLANs



\## VLAN Design



| VLAN | Department | Subnet | Gateway |

|---|---|---|---|

| 10 | Administration | 192.168.10.0/24 | 192.168.10.1 |

| 20 | Staff | 192.168.20.0/24 | 192.168.20.1 |

| 30 | Guest | 192.168.30.0/24 | 192.168.30.1 |



\## Routing



Router-on-a-stick is used to provide inter-VLAN

routing through IEEE 802.1Q trunking.



\## Security



An extended ACL named GUEST\_RESTRICTIONS is applied

inbound on the Guest router subinterface.



It blocks Guest-originated IP traffic to the

Administration and Staff subnets.



Other IP traffic is permitted by the final ACL rule.

The configuration does not enforce complete,

bidirectional isolation.



