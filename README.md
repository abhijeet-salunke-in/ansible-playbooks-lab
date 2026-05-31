# Ansible Playbook Lab

A collection of beginner-friendly and well-commented Ansible playbooks created while learning DevOps and Infrastructure Automation.

The main goal of this repository is not only to automate tasks but also to understand **why each task is performed**, making it useful for students, beginners, and anyone preparing for DevOps interviews.

---

## Topics Covered

### Package Management

* Install packages using different Ansible methods
* Package installation with variables
* Cross-platform package installation

### System Information

* Check Git version
* Get IPv4 information
* Get Operating System details

### File Management

* Create files
* Create directories
* Create files inside directories
* Set file ownership and permissions

### User Management

* Create single user
* Create multiple users

### Git Automation

* Clone public GitHub repositories
* Clone private GitHub repositories
* Secure credentials using Ansible Vault

### Service Management

* Handlers
* Start services after package installation

### Advanced Concepts

* Variables
* Tags
* Conditional Execution (when)
* Register Variables
* Debug Module

### Application Deployment

* Apache Web Server Installation
* Tomcat Installation and Configuration

---

## Prerequisites

### Install Ansible

```bash
sudo yum install ansible-core -y
```

### Verify Installation

```bash
ansible --version
```

### Check Connectivity

```bash
ansible all -m ping
```

---

## Inventory Example

```ini
[dev]
192.168.1.10 ansible_user=root
192.168.1.11 ansible_user=root
```

---

## Running a Playbook

```bash
ansible-playbook playbook-name.yml
```

Example:

```bash
ansible-playbook install-packages.yml
```

---

## Running Tagged Tasks

Run only tagged tasks:

```bash
ansible-playbook tags-example.yml --tags abhi
```

Skip tagged tasks:

```bash
ansible-playbook tags-example.yml --skip-tags abhi
```

---

## Working with Ansible Vault

Encrypt a playbook:

```bash
ansible-vault encrypt playbook.yml
```

Decrypt a playbook:

```bash
ansible-vault decrypt playbook.yml
```

Run encrypted playbook:

```bash
ansible-playbook playbook.yml --ask-vault-pass
```

Change Vault Password:

```bash
ansible-vault rekey playbook.yml
```

---

## Learning Philosophy

Every playbook in this repository contains:

* Detailed comments
* Step-by-step explanation
* Real-world examples
* Beginner-friendly syntax
* DevOps best practices

The focus is on understanding:

**What is happening?**

and more importantly,

**Why it is happening?**

---

## Author

Abhijeet Salunke

DevOps Engineer in Progress 🚀

Learning • Practicing • Automating

---

## License

This repository is intended for educational and learning purposes.
