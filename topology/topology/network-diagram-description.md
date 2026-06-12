# Network Diagram Description

## Devices

- Internet Cloud
- Router
- Core Switch
- Server VLAN (VLAN 40)

## Department VLANs

### VLAN 10 - Administration
- PC-A1
- PC-A2

### VLAN 20 - Sales
- PC-S1
- PC-S2

### VLAN 30 - IT Support
- PC-IT1
- PC-IT2

## Connectivity

Internet
    |
Router
    |
Core Switch
    |
----------------------------------------------------
|               |                |                 |
VLAN 10       VLAN 20         VLAN 30          VLAN 40
Admin         Sales           IT Support       Server
