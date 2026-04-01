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
```
---

### 🔹 Step 2: Environment Setup
VirtualBox / VMware installed
Minimum 2GB RAM
Active internet connection

---

### 🔹 Step 3: Install Security Tools
```bash
sudo apt install ufw fail2ban auditd lynis net-tools -y
sudo apt install openssh-server -y
```

---

### 🔹 Step 4: Configure SSH Security
```bash
sudo nano /etc/ssh/sshd_config
```

---

### Update configuration:
PermitRootLogin no
PasswordAuthentication no
PubkeyAuthentication yes

## **Restart SSH:**
```bash
sudo systemctl restart ssh
```

 ---

### 🔹 Step 5: Setup SSH Key Authentication
```bash
ssh-keygen
ssh-copy-id parth@your_server_ip
```

---

### 🔹 Step 6: Configure Firewall (UFW)
```bash
sudo ufw allow OpenSSH
sudo ufw allow 80
sudo ufw allow 443
sudo ufw enable
sudo ufw status
```

---

📅 Week 2 — Advanced Security & Monitoring

### 🔹Step 7: Setup Fail2Ban
```bash
sudo systemctl enable fail2ban
sudo systemctl start fail2ban
```

**Edit config:**
```bash
sudo nano /etc/fail2ban/jail.local
```

**Add:**
```
[sshd]
enabled = true
maxretry = 3
bantime = 600
```

**Restart**
```bash
sudo systemctl restart fail2ban
```

---

### 🔹 Step 8: Setup Auditd
```bash
sudo systemctl enable auditd
sudo systemctl start auditd
```

---

### 🔹 Step 9: Run Security Audit (Lynis)
```bash
sudo lynis audit system
```

---

### 🔹 Step 10: Monitoring Commands
```bash
sudo ausearch -m USER_LOGIN
sudo ss -tulnp
```

