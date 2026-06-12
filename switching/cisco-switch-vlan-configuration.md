# Cisco Switch VLAN Configuration

## Objective

Configure VLANs for Administration, Sales, IT Support, and Servers.

## Create VLANs

```bash
enable
configure terminal

vlan 10
name Administration

vlan 20
name Sales

vlan 30
name IT_Support

vlan 40
name Servers
```

## Configure Access Ports

### Administration PCs

```bash
interface range fa0/1-5
switchport mode access
switchport access vlan 10
```

### Sales PCs

```bash
interface range fa0/6-10
switchport mode access
switchport access vlan 20
```

### IT Support PCs

```bash
interface range fa0/11-15
switchport mode access
switchport access vlan 30
```

### Servers

```bash
interface range fa0/16-18
switchport mode access
switchport access vlan 40
```

## Configure Trunk Port

```bash
interface g0/1
switchport mode trunk
```

## Verification Commands

```bash
show vlan brief

show interfaces trunk

show running-config
```

## Expected Outcome

* Devices are assigned to the correct VLANs.
* VLAN traffic is separated.
* Trunk link carries multiple VLANs to the router.
