# 🔐 Secure Linux Server Automation using Ansible

Automated the deployment, configuration, and security hardening of a fleet of Linux servers using Ansible. Applied CIS Benchmark Level 1 recommendations for Ubuntu and RHEL systems. Integrated log management, user access auditing, and monitoring tools. Designed for enterprise environments needing secure, compliant Linux infrastructure.

---

## 📌 Project Summary

- Provision secure non-root admin users  
- Harden SSH configuration (disable root login, enforce key-based auth)  
- Setup firewall and intrusion prevention (UFW/Fail2Ban)  
- Install real-time system monitoring (Netdata)  
- Perform security compliance scanning (Lynis - CIS Benchmark)  

---

## 🔧 Key Features

| Area        | Description                                         |
|-------------|-----------------------------------------------------|
| Provisioning | Secure admin user creation, timezone setting       |
| Security     | SSH hardening, root login disabled, auditd & Fail2Ban configured |
| Monitoring  | Netdata installation and setup                      |
| Compliance  | Lynis scans for CIS benchmark compliance            |
| Automation  | Modular Ansible roles with group_vars               |
| Idempotency | Safe to re-run playbook without duplicate changes   |

---

## 📂 Project Structure

The project secure-linux-ansible includes the main playbook site.yml, an Ansible configuration file ansible.cfg, an inventory directory containing the hosts file, a group_vars directory with global variables defined in all.yml, and a roles directory that contains modular roles for provisioning (base), security hardening (security), monitoring setup (monitoring), and compliance scanning (compliance).

---

## 🧪 Tools Used

- Ansible  
- UFW (Ubuntu firewall)  
- Fail2Ban (SSH brute force protection)  
- auditd (Security auditing)  
- Netdata (Real-time monitoring)  
- Lynis (Security compliance scanner)  

---

## 🧰 Requirements

- Ansible 2.10+  
- Target OS: Ubuntu 22.04 or RHEL 9 / Rocky Linux  
- SSH access with sudo privileges  

---

## 🚀 Quick Start

```bash
git clone https://github.com/RishantShukla/secure-linux-ansible.git
cd secure-linux-ansible

ansible-playbook -i inventory/hosts site.yml --ask-pass --ask-become-pass
