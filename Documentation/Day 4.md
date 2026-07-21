# Day 4 - End Devices & Inter-VLAN Routing

## Objective

Deploy end devices, configure inter-VLAN routing using the core switch, and verify communication between VLANs.

---

## Devices Added

| Device | VLAN |
|--------|-----:|
| HR-PC01 | 30 |
| HR-PC02 | 30 |
| FIN-PC01 | 40 |
| FIN-PC02 | 40 |
| IT-PC01 | 20 |
| IT-PC02 | 20 |
| SALES-PC01 | 50 |
| SALES-PC02 | 50 |
| ENG-PC01 | 60 |
| ENG-PC02 | 60 |
| MGMT-PC01 | 10 |
| MGMT-PC02 | 10 |

---

## Completed

- Installed end devices
- Connected all PCs
- Configured VLAN interfaces (SVIs)
- Enabled Layer 3 routing
- Assigned static IP addresses
- Verified inter-VLAN communication

---

## Verification Commands

```text
show ip interface brief
show ip route
show vlan brief
ping
```

---

## Results

- All VLAN interfaces operational
- End devices successfully communicated across VLANs
- Static routing functioning through the core switch

---

## Issues Encountered

- None

---

## Time Spent

2 hours

---

## Lessons Learned

- Layer 3 switches can route between VLANs using SVIs.
- End devices require the correct default gateway to communicate outside their local VLAN.
- Proper VLAN assignments are essential for successful communication.
