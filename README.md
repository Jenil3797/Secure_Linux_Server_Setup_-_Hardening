# 🔐 Secure Linux Server Setup & Hardening

## 📌 Project Overview
This project demonstrates the deployment and hardening of a Linux server using industry-standard security practices. The goal is to protect the system from common cyber threats such as unauthorized access, brute-force attacks, and misconfigurations.

---

## 🎯 Objectives
- Deploy a Linux server (VirtualBox / VMware / Cloud)
- Secure SSH using key-based authentication
- Configure firewall using UFW
- Prevent brute-force attacks using Fail2Ban
- Monitor system using Auditd
- Perform security audit using Lynis

---

## 🛠️ Tools & Technologies
- Ubuntu / Kali Linux  
- OpenSSH Server  
- UFW Firewall  
- Fail2Ban  
- Auditd  
- Lynis  

---

## ⚙️ Implementation Steps

### 🔹 Step 1: Update System
```bash
sudo apt update
sudo apt upgrade -y
