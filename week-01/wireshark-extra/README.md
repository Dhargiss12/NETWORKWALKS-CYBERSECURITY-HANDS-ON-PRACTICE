# Week 01 – Extra: Wireshark SOC Investigation

<p align="left">
  <img src="https://img.shields.io/badge/Networkwalks-Cybersecurity%20Internship-blue?style=for-the-badge" alt="Networkwalks" />
  <img src="https://img.shields.io/badge/Wireshark-Network%20Analysis-1679A7?style=for-the-badge&logo=wireshark&logoColor=white" alt="Wireshark" />
  <img src="https://img.shields.io/badge/Focus-SOC%20Investigation-red?style=for-the-badge" alt="SOC Investigation" />
  <img src="https://img.shields.io/badge/Labs-06-orange?style=for-the-badge" alt="Six Labs" />
  <img src="https://img.shields.io/badge/Tasks-60-blue?style=for-the-badge" alt="60 Tasks" />
</p>

## 📌 Project Overview

As an additional practical assignment during Week 01 of my Cybersecurity Internship at **Networkwalks Pvt. Ltd.**, I completed the Wireshark SOC Project Module (Extra).

The module consisted of six browser-based SOC investigation labs, with ten tasks in each lab.

The exercises focused on analyzing network captures, identifying attackers, reconstructing TCP conversations, discovering exposed credentials, investigating brute-force attacks, and analyzing suspicious VoIP communications.

## 🎯 Objectives

- Investigate network traffic using Wireshark.
- Identify suspicious IP addresses and network activities.
- Reconstruct TCP conversations.
- Extract relevant information from packet captures.
- Identify credentials transmitted over HTTP.
- Investigate repeated authentication attempts.
- Analyze VoIP communications.
- Develop practical network investigation skills.

## 🛠️ Tools & Technologies

| Tool / Technology | Purpose |
|---|---|
| Wireshark | Network packet analysis |
| TCP/IP | Network communication |
| HTTP | Application traffic investigation |
| TCP Stream | Communication reconstruction |
| VoIP | Voice communication investigation |
| Browser-based Labs | Practical SOC exercises |

## 🔬 Practical Labs

### 01. Identify the Attacker's IP

<badge color="info">Network Investigation</badge>

**Original Lab:** Lab 03

**Objective:** Find the attacker's IP address in captured network traffic.

Activities:
- Investigated captured network traffic.
- Identified the attacker's IP address.
- Examined communication between network endpoints.
- Analyzed suspicious network activities.

**Concepts:** IP address analysis, TCP communication and port scanning.

**Lab:** https://networkwalks.com/wireshark-lab3/

### 02. Follow TCP Stream – Part 1

<badge color="info">TCP Analysis</badge>

**Original Lab:** Lab 04

**Objective:** Reconstruct a network conversation and inspect transmitted data.

Activities:
- Examined TCP communication.
- Used Follow TCP Stream.
- Reconstructed transmitted conversations.
- Investigated relevant application-level information.

**Concepts:** TCP stream reconstruction and packet inspection.

**Lab:** https://networkwalks.com/wireshark-lab4/

### 03. Follow TCP Stream – Part 2

<badge color="info">Network Forensics</badge>

**Original Lab:** Lab 05

**Objective:** Analyze a new packet capture and discover hidden information.

Activities:
- Investigated another network capture.
- Practiced TCP stream reconstruction.
- Examined transmitted data.
- Identified relevant hidden information.

**Concepts:** TCP stream analysis and network forensics.

**Lab:** https://networkwalks.com/wireshark-lab5/

### 04. HTTP Plaintext Credentials

<badge color="warning">Credential Exposure</badge>

**Original Lab:** Lab 06

**Objective:** Find usernames and passwords transmitted in cleartext over HTTP.

Activities:
- Investigated HTTP traffic.
- Examined authentication-related requests.
- Identified plaintext credentials.
- Explored security risks associated with unencrypted communication.

**Concepts:** HTTP, authentication, plaintext credentials and data confidentiality.

**Lab:** https://networkwalks.com/wireshark-lab6/

### 05. Catch the Brute Force Attacker

<badge color="warning">Threat Detection</badge>

**Original Lab:** Lab 07

**Objective:** Identify repeated login attempts and determine who is guessing passwords.

Activities:
- Investigated repeated authentication attempts.
- Analyzed suspicious login patterns.
- Identified the source of password-guessing activity.

**Concepts:** Brute-force attacks, authentication monitoring and threat detection.

**Lab:** https://networkwalks.com/wireshark-lab7/

### 06. Catch the Call Scammer

<badge color="info">VoIP Investigation</badge>

**Original Lab:** Lab 08

**Objective:** Investigate captured communication, analyze the call and identify the scammer.

Activities:
- Examined captured VoIP traffic.
- Investigated recorded voice communication.
- Analyzed the call.
- Identified suspicious caller activity.

**Concepts:** VoIP traffic analysis and communication investigation.

**Lab:** https://networkwalks.com/wireshark-lab8/

## 📊 Lab Completion Summary

| No. | Investigation Lab | Tasks |
|---|---|---:|
| 01 | Identify the Attacker's IP | 10 |
| 02 | Follow TCP Stream – Part 1 | 10 |
| 03 | Follow TCP Stream – Part 2 | 10 |
| 04 | HTTP Plaintext Credentials | 10 |
| 05 | Catch the Brute Force Attacker | 10 |
| 06 | Catch the Call Scammer | 10 |
| | **Total** | **60** |

## 📚 Key Technical Learnings

| Area | Learning Outcome |
|---|---|
| Network Traffic Analysis | Investigating captured network packets |
| IP Investigation | Identifying suspicious IP addresses |
| TCP Analysis | Reconstructing network conversations |
| Network Forensics | Extracting information from packet captures |
| HTTP Security | Understanding plaintext credential exposure |
| Brute Force Detection | Recognizing repeated login attempts |
| VoIP Analysis | Investigating voice communication |
| SOC Investigation | Identifying suspicious network activities |

## 📸 Screenshots & Evidence

Screenshots and lab completion evidence are organized separately for each investigation.

```text
week-01-wireshark-extra/
│
├── README.md
│
└── screenshots/
    ├── lab-01-attacker-ip/
    ├── lab-02-tcp-stream-1/
    ├── lab-03-tcp-stream-2/
    ├── lab-04-http-credentials/
    ├── lab-05-brute-force/
    └── lab-06-voip/
```

## 💡 Key Takeaways

- Developed practical exposure to network packet investigation.
- Understood how TCP streams help reconstruct network conversations.
- Recognized the risks of transmitting credentials over unencrypted HTTP.
- Practiced identifying suspicious authentication patterns.
- Explored VoIP communication analysis.
- Understood the importance of network traffic investigation in SOC operations.

## 🔐 Security Disclaimer

All exercises were conducted within the authorized browser-based training environments provided by Networkwalks.

This project is documented for educational purposes and defensive cybersecurity learning.

## 🏢 Internship Information

| Field | Details |
|---|---|
| Organization | Networkwalks Pvt. Ltd. |
| Program | Cybersecurity Internship |
| Week | 01 – Extra |
| Project | Wireshark SOC Project Module |
| Domain | Network Security / SOC Analysis |
| Labs | 6 |
| Tasks | 60 |
| Status | Completed |

## 👤 Author

**Dhargiss V**

B.Tech – Computer Science and Engineering (Cyber Security)

- GitHub: [Dhargiss12](https://github.com/Dhargiss12)
- LinkedIn: [Connect with me](https://www.linkedin.com/)

---

*Learning through practical investigation. Building cybersecurity skills one packet at a time.*
