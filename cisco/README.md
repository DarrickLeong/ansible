# Cisco ACI Ansible Playbooks

Playbooks for automating Cisco Application Centric Infrastructure (ACI) using the `cisco.aci` collection.

## Playbooks

| Playbook | Description |
|----------|-------------|
| `cisco_aci.yml` | General ACI configuration tasks |
| `cisco_aci_vlan.yml` | Complete VLAN setup with all related policies and profiles |
| `cisco_aci_vlan_delete.yml` | Remove VLAN configurations from ACI |

## Features

The `cisco_aci_vlan.yml` playbook provides comprehensive VLAN configuration:

- **Switch Leaf Profiles** - Create and manage leaf switch profiles
- **Leaf Selectors** - Associate leaf nodes with profiles
- **Interface Profiles** - Configure interface-level policies
- **Access Port Selectors** - Define port ranges and mappings
- **CDP Policy** - Enable/disable Cisco Discovery Protocol
- **LLDP Policy** - Configure Link Layer Discovery Protocol
- **Port Channel Policy** - LACP configuration for link aggregation
- **Leaf Access Port Policy Groups** - Group interface policies
- **VPC Interface Policy Groups** - Virtual Port Channel configuration

## Prerequisites

```bash
ansible-galaxy collection install cisco.aci
```

## Configuration

Update the following variables in the playbook or pass via extra vars:

```yaml
hostname: <ACI APIC IP>
username: admin
password: <password>
```

## Usage

```bash
ansible-playbook cisco_aci_vlan.yml -i inventory.yml
```

[← Back to Main README](../README.md)
