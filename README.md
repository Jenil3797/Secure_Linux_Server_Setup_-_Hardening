# Secure_Linux_Server_Setup_-_Hardening 
# Project-2-Secure-Linux-Server-Setup-Hardening
# Secure Kali Linux Server Setup & Hardening

## Project Overview
This project demonstrates how to deploy and secure a Kali Linux system using standard cybersecurity hardening techniques. The objective of this project is to protect the server from common threats such as unauthorized access, brute-force attacks, insecure configurations, and network vulnerabilities.

The project includes SSH hardening, firewall configuration, intrusion prevention using Fail2Ban, security auditing with Lynis, and vulnerability scanning using Nmap and Nikto.

---

## Objectives

- Deploy Kali Linux as a secure server environment
- Configure secure SSH access
- Implement firewall protection
- Prevent brute-force login attacks
- Perform vulnerability scanning
- Monitor system logs

---

## Tools & Technologies Used

| Tool | Purpose |
|-----|------|
| Kali Linux | Target system |
| OpenSSH | Secure remote access |
| UFW Firewall | Network security |
| Fail2Ban | Intrusion prevention |
| Lynis | Security auditing |
| Nmap | Network scanning |
| Nikto | Web vulnerability scanning |

---
# Project Roadmap

## Week 1 — Server Deployment & Basic Security

### Tasks
- Deploy Linux server locally or on cloud (AWS / DigitalOcean)
- Configure SSH security
- Disable root login
- Implement key-based authentication
- Configure firewall rules using UFW

### Key Commands

Update system

```bash
sudo apt update
sudo apt upgrade -y
## System Setup

### Step 1: Update Kali Linux

Update system packages to ensure all security patches are installed.


sudo apt update
sudo apt upgrade -y
VirtualBox / VMware

Minimum 2GB RAM

Internet connection

---

### Step 2: Install Basic Security Tools

Install required packages:

sudo apt install ufw fail2ban auditd lynis net-tools -y
sudo apt install openssh-server -y

**Step 3: Configure SSH Security**

Edit SSH configuration file

sudo nano /etc/ssh/sshd_config

