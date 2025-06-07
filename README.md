# Secure Linux Server Automation with Ansible

This project automates the provisioning and hardening of Ubuntu and RHEL-based Linux servers using Ansible. It follows CIS Benchmark Level 1 recommendations, includes monitoring and compliance tools, and is ready for enterprise or lab deployments.

## 🔧 Features

- SSH hardening (no root login, key-based auth)
- Password policy enforcement
- Firewall configuration (UFW/Firewalld)
- Fail2Ban and auditd setup
- Monitoring with Netdata or Node Exporter
- Compliance scans using Lynis
- Ansible Vault support for secrets

## 🧰 Requirements

- Ansible 2.10+
- Target: Ubuntu 22.04 / RHEL 9 (or Rocky)
- SSH access with sudo privileges

## 🚀 Quick Start

```bash
git clone https://github.com/RishantShukla/secure-linux-ansible.git
cd secure-linux-ansible

ansible-playbook -i inventory/hosts site.yml --ask-pass --ask-become-pass
