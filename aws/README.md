# AWS Ansible Playbooks

Playbooks for managing AWS EC2 instances and security groups using the `amazon.aws` collection.

## Playbooks

| Playbook | Description |
|----------|-------------|
| `aws_create_instance.yml` | Create EC2 instances with custom networking, security groups, and private IP addresses |
| `aws_gather.instance.yml` | Gather information about existing EC2 instances |
| `aws_instance_edit_inventory.yml` | Edit inventory based on EC2 instance data |
| `aws_ping.yml` | Test connectivity to AWS instances |
| `aws_security_group.yml` | Manage EC2 security group inbound rules dynamically |

## Prerequisites

```bash
ansible-galaxy collection install amazon.aws
```

## Configuration

Ensure your AWS credentials are configured via:
- Environment variables (`AWS_ACCESS_KEY_ID`, `AWS_SECRET_ACCESS_KEY`)
- AWS credentials file (`~/.aws/credentials`)
- IAM role (when running on EC2)

## Usage Examples

### Create an EC2 Instance

```bash
ansible-playbook aws_create_instance.yml \
  -e "new_ip_address=10.0.1.100" \
  -e "new_ip_id=001"
```

### Edit Security Group Rules

```bash
ansible-playbook aws_security_group.yml \
  -e "security_group_id=sg-xxxxxxxx" \
  -e "firewall_protocol=tcp" \
  -e "firewall_port=443" \
  -e "firewall_cidr_ip=0.0.0.0/0" \
  -e "firewall_rule_description=Allow HTTPS"
```

[← Back to Main README](../README.md)
