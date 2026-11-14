
# WEEK 02 – CYBERSECURITY HANDS-ON PRACTICE

This folder contains my Week 2 practical activities completed as part of the Cybersecurity Internship Program at **Networkwalks**.

During this week, I worked on footprinting and reconnaissance using Kali Linux tools and network scanning using Zenmap.

## 📌 Modules Covered

### 1. W2-PM1 – Footprinting with Multiple Kali Linux Tools (Elective)

**Objective:** To perform footprinting and reconnaissance on `networkwalks.com` using different Kali Linux tools.

**Tools Used:**
- WHOIS
- WhatWeb
- Nslookup
- Curl
- Wafw00f
- DNSRecon

**Activities Performed:**
- Collected publicly available domain registration information.
- Identified website technologies and components.
- Performed DNS resolution.
- Examined HTTP response headers.
- Checked for detectable Web Application Firewall (WAF) technologies.
- Enumerated publicly available DNS records.

📂 **Project Folder:** [`W2-PM1`](./W2-PM1/)

---

### 2. W2-PM5 – Zenmap Based Network Scanning (Mandatory)

**Objective:** To identify active hosts within my own local network using Zenmap.

**Tool Used:**
- Zenmap (Nmap GUI)

**Activities Performed:**
- Identified local IP configuration using Windows CMD.
- Identified the local network subnet.
- Performed a Ping Scan using Zenmap.
- Discovered active hosts in the scanned subnet.
- Examined available IP and MAC address information.

**Scan Details:**
- Target Subnet: `10.141.146.0/24`
- Scan Type: Ping Scan
- Command: `nmap -sn 10.141.146.0/24`
- Total IP Addresses Scanned: 256
- Active Hosts Identified: 2

📂 **Project Folder:** [`W2-PM5`](./W2-PM5/)

---

## 📄 Week 2 Final Report

The final report documents the activities performed in both selected modules, including the procedures, observations, risk analysis, recommendations, and conclusion.

📑 **Report:** [`W2-PM-FINAL-REPORT.md`](./W2-PM-FINAL-REPORT.md)

---

## 📁 Repository Structure

```text
week-02/
│
├── README.md
│
├── W2-PM1/
│   ├── README.md
│   └── screenshots/
│
├── W2-PM5/
│   ├── README.md
│   └── screenshots/
│
└── W2-PM-FINAL-REPORT.md
```

---

## 🛠️ Environment Used

- Kali Linux
- Windows
- Zenmap
- Nmap 7.93
- Windows Command Prompt

## 🎯 Learning Outcomes

- Understood the fundamentals of website footprinting and reconnaissance.
- Gained practical experience with multiple Kali Linux reconnaissance tools.
- Learned how DNS resolution and HTTP response headers work.
- Understood how to perform network discovery using Zenmap.
- Gained experience identifying active hosts and interpreting scan results.
- Improved technical documentation and cybersecurity reporting skills.

## ⚠️ Disclaimer

All practical activities were performed for educational purposes and within the authorized scope. Network scanning was conducted on my own local network. Unauthorized scanning or testing of systems is strictly discouraged.

---

**Program:** Networkwalks Cybersecurity Internship  
**Week:** 02  
**Intern:** Dhargiss V
