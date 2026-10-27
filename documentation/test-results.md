\# Network Test Results



\## Gateway Connectivity



| Source | Destination | Result |

|---|---|---|

| Admin-PC1 | 192.168.10.1 | PASS |

| Staff-PC1 | 192.168.20.1 | PASS |

| Guest-PC1 | 192.168.30.1 | PASS |



\## Inter-VLAN Connectivity Before Guest ACL



| Source | Destination | Packet Loss | Result |

|---|---|---:|---|

| Admin-PC1 | 192.168.20.20 | 0% | PASS |

| Admin-PC1 | 192.168.30.30 | 0% | PASS |

| Staff-PC1 | 192.168.10.10 | 0% | PASS |



\## Guest Access Tests After ACL



| Source | Destination | Packet Loss | Expected |

|---|---|---:|---|

| Guest-PC1 | 192.168.10.10 | 100% | Blocked |

| Guest-PC1 | 192.168.20.20 | 100% | Blocked |

| Guest-PC1 | 192.168.30.31 | 0% | Allowed |



\## Conclusion



Gateway connectivity and the recorded inter-VLAN

tests were successful before applying Guest restrictions.



After applying the ACL, the recorded tests showed

Guest traffic to the Administration and Staff

networks was unsuccessful, while Guest-to-Guest

communication remained successful.



ACL counters should be checked to confirm that the

deny rules matched the blocked traffic.



