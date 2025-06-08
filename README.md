# 🔐 Secure Linux Server Automation using Ansible

This project automates the configuration, hardening, and monitoring of Linux systems (Ubuntu or RHEL-based) using **Ansible**. It follows industry best practices for system security and compliance by integrating tools like **UFW**, **Fail2Ban**, **Netdata**, and **Lynis**.

---

## 📌 Project Summary

Ansible-based automation framework to provision and harden Linux systems. It includes:
- Creation of secure non-root admin users
- SSH configuration hardening
- Firewall and intrusion prevention setup
- Real-time system monitoring
- Security compliance scanning (CIS Benchmark via Lynis)

---

## 🔧 Key Features

| Area              | Description                                                                 |
|-------------------|-----------------------------------------------------------------------------|
| **Provisioning**   | Creates a secure non-root admin user and sets timezone                     |
| **Security**       | Hardens SSH, disables root login, enables UFW, configures auditd & fail2ban |
| **Monitoring**     | Installs and configures **Netdata** for real-time metrics                  |
| **Compliance**     | Executes **Lynis** to identify gaps against CIS benchmarks                 |
| **Automation**     | Uses modular Ansible roles with `group_vars` for clean configuration       |
| **Idempotency**    | Playbook can be safely re-run without causing duplicate changes            |

---

## 📂 Project Structure

```text
secure-linux-ansible/
├── site.yml                # Main playbook
├── ansible.cfg             # Ansible configuration
├── inventory/
│   └── hosts               # Inventory file
├── group_vars/
│   └── all.yml             # Global variables
├── roles/
│   ├── base/               # Provisioning tasks
│   ├── security/           # Hardening tasks
│   ├── monitoring/         # Netdata setup
│   └── compliance/         # Lynis scan and reporting

## 🧪 Tools Used

- **Ansible** – Automation engine for system configuration
- **UFW** – Host-based firewall for Ubuntu systems
- **Fail2Ban** – SSH brute-force protection
- **auditd** – Security auditing
- **Netdata** – Real-time performance and health monitoring
- **Lynis** – Linux security compliance scanner (CIS benchmark aligned)

---

## 🔐 Features

- SSH hardening (disables root login, enforces key-based auth)
- Password policy enforcement
- Firewall configuration (UFW or Firewalld)
- Fail2Ban + auditd integration
- Netdata or Node Exporter setup for monitoring
- Lynis-based compliance auditing
- Ansible Vault support for encrypted secrets

---

## 🧰 Requirements

- Ansible 2.10 or later
- Target OS: Ubuntu 22.04 or RHEL 9 / Rocky Linux
- SSH access with a user having `sudo` privileges

---

## 🚀 Quick Start

```bash
git clone https://github.com/RishantShukla/secure-linux-ansible.git
cd secure-linux-ansible

ansible-playbook -i inventory/hosts ./site.yml --ask-pass --ask-become-pass
