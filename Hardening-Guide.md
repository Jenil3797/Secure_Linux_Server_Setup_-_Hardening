# Linux Server Hardening Guide

## 1. System Update

sudo apt update && sudo apt upgrade -y

---

## 2. SSH Hardening

Edit SSH config:
sudo nano /etc/ssh/sshd_config

Set:
PermitRootLogin no
PasswordAuthentication no

Restart:
sudo systemctl restart ssh

---

## 3. Firewall Setup (UFW)

sudo ufw enable
sudo ufw allow OpenSSH
sudo ufw status

---

## 4. Install Fail2Ban

sudo apt install fail2ban -y
sudo systemctl start fail2ban
sudo systemctl enable fail2ban

---

## 5. Enable Auditd

sudo apt install auditd -y
sudo systemctl enable auditd
sudo systemctl start auditd

---

## 6. Run Lynis Audit

sudo apt install lynis -y
sudo lynis audit system

---

## 7. Vulnerability Scanning

* Installed Nessus Essentials
* Performed scan on localhost
* Fixed identified issues

---

## 8. Monitoring Commands

sudo ausearch -m USER_LOGIN
sudo ss -tulnp
