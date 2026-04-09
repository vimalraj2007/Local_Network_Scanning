# 🔍 Task 1: Network Port Scanning & Analysis

## 📌 Objective
The objective of this task is to discover open ports and services running on devices within a local network and understand potential security risks associated with exposed services.

---

## 🛠️ Tools Used
- Kali Linux  
- Nmap  
- Wireshark  
- Metasploit (Target Machine)

---

## 🧠 Methodology

### 1️⃣ Identify Local Network
- Checked the IP address of the Kali Linux machine
- Identified the network range (e.g., 192.168.29.0/24)

---

### 2️⃣ Network Scanning (Nmap)
- Performed a TCP SYN scan on the entire network:
  Discovered active devices and open ports in the network
  nmap -sS 192.168.1.0/24
---

### 3️⃣ Service Detection

Scanned target (Metasploit machine) with version detection:

nmap -sV <target-ip>(192.168.29.130)
Identified running services on open ports

---

---

## 4️⃣ Specific Port Scanning

Focused scan on common ports:

nmap -p 21,22,80 <target-ip>
Verified services like:
FTP (21)
SSH (22)
HTTP (80)

---

---

## 5️⃣ Packet Analysis (Wireshark)
Captured network traffic during scans
Observed:
SYN packets
Handshake process
Communication between devices

---

---

## 6️⃣ Save Results

Saved scan output:

nmap -sS 192.168.1.0/24 -oN scan.txt
---

---

## 6️⃣ Save Results

Saved scan output:

nmap -sS 192.168.1.0/24 -oN scan.txt
---


---

## 🔍 Key Findings
Multiple devices active in the network
Open ports detected (21, 22, 80)
Services exposed:
FTP (File Transfer)
SSH (Remote Access)
HTTP (Web Service)
---


---

## ⚠️ Security Risks Identified

Open ports increase attack surface
FTP may allow unauthorized access
SSH brute-force attacks possible
HTTP can expose web vulnerabilities
---

---

## 🛡️ Recommendations
Close unused ports
Use firewalls to restrict access
Disable unnecessary services
Use strong authentication for SSH
Monitor network traffic regularly
---

---

## 📁 Repository Structure

---
Task1-Network-Scan/

├── scan.txt
├── screenshots/
├── README.md
---
---
