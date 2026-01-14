# Ansible

A collection of Ansible playbooks for automating infrastructure across various platforms and use cases.

| Category | Brief Description |
|---|---|
| [AWS](aws) | Playbooks for EC2 instance provisioning, security group management, and instance discovery on Amazon Web Services. |
| [Cisco ACI](cisco) | Network automation for Cisco Application Centric Infrastructure including VLAN configuration, switch profiles, interface policies, and VPC setup. |
| [NetBox](netbox) | Integration with NetBox DCIM/IPAM for VM inventory management, IP address allocation, and security group tracking. |
| [NFS](nfs) | NFS server configuration and client mounting for RHEL systems including exports, firewall rules, and service management. |
| [RHEL](rhel) | Red Hat Enterprise Linux system administration including fact gathering, connectivity testing, and sample application deployment. |
| [Migration](migration) | Ansible Automation Platform 2.4 migration from RPM-based installation to OpenShift, including database export/import and secret key migration. |
| [Templates](templates) | Jinja2 templates used by migration playbooks for generating manifest and secrets files. |

---

## Getting Started

### Prerequisites

- Ansible Core 2.14+
- Required collections:

```bash
ansible-galaxy collection install amazon.aws
ansible-galaxy collection install cisco.aci
ansible-galaxy collection install community.general
```

### Usage

```bash
ansible-playbook <category>/<playbook>.yml -i inventory.yml
```

---

## License

See [LICENSE](LICENSE) for details.
