# Day 3 - VLANs and Trunking

## Objective

Configure VLANs across the enterprise network, establish trunk links between switches, and prepare access ports for departmental devices.

## Work Completed

* Created VLANs on all switches.
* Configured trunk links between Core, Distribution, and Access switches.
* Allowed VLANs 10, 20, 30, 40, 50, 60, 70, and 80 on trunk interfaces.
* Configured access ports on ACC-SW1 for HR, Finance, and IT.
* Added basic interface descriptions to trunk ports.
* Saved configurations on all modified devices.

## VLAN Plan

| VLAN | Name        | Subnet        |
| ---- | ----------- | ------------- |
| 10   | MANAGEMENT  | 10.10.10.0/24 |
| 20   | IT          | 10.10.20.0/24 |
| 30   | HR          | 10.10.30.0/24 |
| 40   | FINANCE     | 10.10.40.0/24 |
| 50   | SALES       | 10.10.50.0/24 |
| 60   | ENGINEERING | 10.10.60.0/24 |
| 70   | SERVERS     | 10.10.70.0/24 |
| 80   | GUEST-WIFI  | 10.10.80.0/24 |

## Trunk Links Configured

| Connection          | Port Type             |
| ------------------- | --------------------- |
| CORE-SW1 ↔ CORE-SW2 | GigabitEthernet trunk |
| CORE-SW1 ↔ DIST-SW1 | GigabitEthernet trunk |
| CORE-SW1 ↔ DIST-SW2 | GigabitEthernet trunk |
| CORE-SW2 ↔ DIST-SW1 | GigabitEthernet trunk |
| CORE-SW2 ↔ DIST-SW2 | GigabitEthernet trunk |
| DIST-SW1 ↔ ACC-SW1  | trunk                 |
| DIST-SW1 ↔ ACC-SW2  | trunk                 |
| DIST-SW2 ↔ ACC-SW3  | trunk                 |
| DIST-SW2 ↔ ACC-SW4  | trunk                 |

## Access Port Configuration

### ACC-SW1

| Ports     | VLAN | Department |
| --------- | ---- | ---------- |
| Fa0/2-6   | 30   | HR         |
| Fa0/7-11  | 40   | Finance    |
| Fa0/12-16 | 20   | IT         |

The remaining access switches will be configured after end devices are added and the final port allocation plan is confirmed.

## Verification Performed

### Commands Used

```cisco
show vlan brief
show interfaces trunk
show running-config
```

### Results

* All VLANs were present on the switches.
* Trunk ports were operational.
* Required VLANs were allowed across trunk links.
* ACC-SW1 access ports were assigned to the correct VLANs.
* Configurations were saved successfully.

## Hardware Notes

* Core switches are Cisco 3650 multilayer switches.
* Distribution and Access switches are Cisco 2960 switches with two Gigabit uplinks and FastEthernet access ports.
* Server-PT devices use FastEthernet interfaces.
* Infrastructure links use Gigabit interfaces where available; end hosts will use FastEthernet interfaces.

## Lessons Learned

* VLANs must exist on switches before access ports can be assigned to them.
* Trunk links must allow all required VLANs for traffic to pass between switches.
* Packet Tracer hardware limitations should influence the network design.
* It is better to wait for end hosts before configuring all access ports.

## Next Steps

* Add end devices to the topology.
* Create the final port allocation plan for ACC-SW2, ACC-SW3, and ACC-SW4.
* Connect servers and the wireless access point.
* Configure switch management IP addresses.
* Configure inter-VLAN routing on the core switches.

## Time Spent

Approximately 2 hours
