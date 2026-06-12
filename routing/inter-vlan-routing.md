# Inter-VLAN Routing (Router-on-a-Stick)

## Objective

Enable communication between different VLANs while maintaining logical separation of departments.

## VLANs

| VLAN | Department     | Network         |
| ---- | -------------- | --------------- |
| 10   | Administration | 192.168.10.0/24 |
| 20   | Sales          | 192.168.20.0/24 |
| 30   | IT Support     | 192.168.30.0/24 |
| 40   | Servers        | 192.168.40.0/24 |

## Router Subinterfaces

### VLAN 10

Interface: G0/0.10

IP Address:
192.168.10.1/24

### VLAN 20

Interface: G0/0.20

IP Address:
192.168.20.1/24

### VLAN 30

Interface: G0/0.30

IP Address:
192.168.30.1/24

### VLAN 40

Interface: G0/0.40

IP Address:
192.168.40.1/24

## Traffic Flow Example

PC in Administration VLAN (192.168.10.10)

↓

Default Gateway (192.168.10.1)

↓

Router

↓

Sales VLAN Gateway (192.168.20.1)

↓

Destination Device (192.168.20.15)

## Benefits

* Department isolation
* Improved security
* Centralized routing
* Better traffic management

## Verification

* Ping between VLANs
* Verify gateway reachability
* Check routing table entries
* Confirm trunk link operation
