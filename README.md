# firewall-configuration-task4
This repository demonstrates how to configure and test basic firewall rules using UFW (Uncomplicated Firewall) on a Kali Linux system. It includes step-by-step instructions for blocking and allowing specific ports (like Telnet and SSH), viewing firewall status, and understanding default policies.

# 🔐 Cyber Security Internship - Task 4: Firewall Configuration

## 📁 Repository: `firewall-configuration-task4`

This repository contains the documentation and implementation steps for configuring a basic firewall using UFW (Uncomplicated Firewall) on a Kali Linux system. This is part of Task 4 of the Cyber Security Internship Program.

---

## 📌 Task Overview

### 🎯 Objective:
To configure and test essential firewall rules using UFW to manage network traffic securely and effectively.

---

## 🛠️ Tools Used
- **Kali Linux**
- **UFW (Uncomplicated Firewall)**

---

## 🧪 Steps Performed

### ✅ 1. Enabled UFW
```bash
sudo ufw enable
```
Activates the firewall with default deny (incoming) and allow (outgoing) rules.

---

### ✅ 2. Checked Firewall Status (Verbose)
```bash
sudo ufw status verbose
```
Displays current rules, logging level, and default policies.

---

### ✅ 3. Blocked Telnet (Port 23)
```bash
sudo ufw deny 23
```
Prevents access to insecure Telnet services.

---

### ✅ 4. Tested Telnet Block
```bash
telnet localhost 23
```
Result: **Connection refused** — confirms rule is working.

---

### ✅ 5. Allowed SSH (Port 22)
```bash
sudo ufw allow 22
```
Ensures remote access via SSH is permitted.

---

### ✅ 6. Removed Telnet Rule
```bash
sudo ufw delete deny 23
```
Reverts the block rule on port 23.

---

### ✅ 7. Final Status Check
```bash
sudo ufw status verbose
```
Displays the final state of the firewall after configuration.

---

## 🔍 Observations

- **UFW Status:** Enabled  
- **Logging Level:** Low  
- **Default Policies:**  
  - Incoming: Denied  
  - Outgoing: Allowed  

### 🔐 Rules Applied:
- ✅ Port 23 (Telnet) — Blocked (and tested)
- ✅ Port 22 (SSH) — Allowed for secure access

### 🌐 Web Access:
- Outbound connections to port **80 (HTTP)** and **443 (HTTPS)** are permitted by default.

---

## 🧾 Conclusion

UFW was successfully configured to filter incoming and outgoing traffic according to defined rules. The firewall ensures the system is protected from unauthorized access while still allowing secure and essential communication like SSH and web traffic. This task demonstrated the practicality and simplicity of UFW in securing Linux systems.

---

## ✅ Summary

This task showcases the use of **UFW** on **Kali Linux** to:
- Block unauthorized ports (Telnet)
- Allow secure access (SSH)
- Verify firewall effectiveness
- Understand default traffic policies

---

> 🔐 A small step in firewall configuration, a giant leap toward cybersecurity discipline.
