# Week 01 – Wireshark SOC Investigation

<p align="left">
  <img src="https://img.shields.io/badge/Networkwalks-Cybersecurity%20Internship-blue?style=for-the-badge" alt="Networkwalks Internship" />
  <img src="https://img.shields.io/badge/Tool-Wireshark-1679A7?style=for-the-badge&logo=wireshark&logoColor=white" alt="Wireshark" />
  <img src="https://img.shields.io/badge/Tool-TShark-lightblue?style=for-the-badge" alt="TShark" />
  <img src="https://img.shields.io/badge/Focus-SOC%20Analysis-red?style=for-the-badge" alt="SOC Analysis" />
  <img src="https://img.shields.io/badge/Status-Completed-success?style=for-the-badge" alt="Completed" />
</p>

## 📌 Project Overview

As part of Week 01 of my Cybersecurity Internship at **Networkwalks Pvt. Ltd.**, I completed a hands-on Wireshark SOC Project Module consisting of six browser-based security investigation labs.

The project focused on analyzing network packet captures, identifying suspicious network activities, investigating communication patterns, and extracting security-relevant information using Wireshark.

## 🎯 Objectives

- Understand network traffic and packet-level communication.
- Identify suspicious source and destination IP addresses.
- Investigate TCP connections and port scanning activities.
- Analyze TCP flags and connection responses.
- Reconstruct network conversations using Follow TCP Stream.
- Identify plaintext credentials and authentication traffic.
- Investigate repeated login attempts and brute-force activity.
- Analyze VoIP traffic and suspicious communications.

## 🛠️ Tools & Technologies

| Tool | Purpose |
|---|---|
| Wireshark | Network packet capture and analysis |
| TShark | Command-line packet analysis |
| Kali Linux | Cybersecurity analysis environment |
| TCP/IP | Network communication analysis |

## 🔬 Practical Labs

### 01. Identify the Attacker's IP

**Focus:** Network traffic analysis and port scanning investigation.

Activities:
- Identified the suspicious source IP address.
- Investigated communication between attacker and target.
- Analyzed TCP conversations.
- Identified different destination ports.
- Distinguished open and closed ports using TCP flags.
- Examined protocol hierarchy and identified FTP traffic.

**Concepts:** IP analysis, TCP conversations, SYN, SYN-ACK, RST, port scanning and protocol identification.

### 02. Follow TCP Stream – Part 1

**Focus:** TCP conversation reconstruction.

Activities:
- Followed TCP communication between network endpoints.
- Reconstructed transmitted data.
- Inspected application-level communication.

**Concepts:** TCP stream reconstruction and packet inspection.

### 03. Follow TCP Stream – Part 2

**Focus:** Advanced TCP stream investigation.

Activities:
- Analyzed another network capture.
- Reconstructed communication streams.
- Investigated relevant transmitted information.

**Concepts:** TCP stream analysis and data investigation.

### 04. HTTP Plaintext Credentials

**Focus:** Credential exposure analysis.

Activities:
- Examined HTTP traffic.
- Investigated authentication requests.
- Identified credentials transmitted in plaintext.

**Concepts:** HTTP, authentication, plaintext data exposure and network security.

### 05. Catch the Brute Force Attacker

**Focus:** Authentication attack investigation.

Activities:
- Identified repeated login attempts.
- Investigated suspicious authentication patterns.
- Analyzed traffic associated with password guessing.

**Concepts:** Brute-force attacks, login analysis and suspicious traffic identification.

### 06. Catch the Call Scammer

**Focus:** VoIP traffic investigation.

Activities:
- Investigated captured VoIP traffic.
- Analyzed recorded communication.
- Identified suspicious call activity.

**Concepts:** VoIP analysis and communication investigation.

## 💻 Wireshark Display Filters Practiced

### IP Address Investigation

Identify traffic from a specific source:

```wireshark
ip.src == 192.168.10.66
```

Identify traffic going to a specific destination:

```wireshark
ip.dst == 192.168.10.20
```

Filter communication between two endpoints:

```wireshark
ip.addr == 192.168.10.66 && ip.addr == 192.168.10.20
```

### TCP Connection Analysis

Initial TCP SYN packets:

```wireshark
tcp.flags.syn == 1 && tcp.flags.ack == 0
```

SYN-ACK responses:

```wireshark
tcp.flags.syn == 1 && tcp.flags.ack == 1
```

TCP reset packets:

```wireshark
tcp.flags.reset == 1
```

### Protocol Identification

```wireshark
ftp
```

```wireshark
http
```

```wireshark
dns
```

```wireshark
icmp
```

### FTP Authentication Investigation

```wireshark
ftp.request.command == "USER" || ftp.request.command == "PASS"
```

## 📚 Key Technical Concepts Learned

| Concept | Learning Outcome |
|---|---|
| Packet Analysis | Understanding captured network packets |
| IP Address Analysis | Identifying communication endpoints |
| TCP Three-Way Handshake | Understanding SYN, SYN-ACK and ACK |
| TCP Flags | Identifying connection requests and resets |
| Port Scanning | Investigating attempts to access multiple ports |
| Protocol Hierarchy | Identifying protocols in captured traffic |
| Follow TCP Stream | Reconstructing network conversations |
| FTP Authentication | Understanding USER and PASS commands |
| HTTP Security | Recognizing plaintext credential exposure |
| Brute Force Detection | Identifying repeated login attempts |
| VoIP Analysis | Investigating voice communication traffic |

## 📸 Screenshots & Evidence

Investigation screenshots are organized by individual lab.

```text
screenshots/
├── lab-01/
├── lab-02/
├── lab-03/
├── lab-04/
├── lab-05/
└── lab-06/
```

## 💡 Key Takeaways

- Learned to identify suspicious network activities through packet analysis.
- Understood TCP connection patterns and port scanning behavior.
- Explored how network protocols reveal application-level communication.
- Identified security risks associated with unencrypted authentication.
- Recognized repeated login attempts as potential brute-force activity.
- Understood how packet-level evidence supports security investigations.

## 🔐 Security Disclaimer

All exercises were performed within the authorized training environments provided for the internship.

This repository is intended for educational purposes and defensive cybersecurity learning. No unauthorized systems or networks were targeted.

## 🏢 Internship Information

| Field | Details |
|---|---|
| Organization | Networkwalks Pvt. Ltd. |
| Program | Cybersecurity Internship |
| Week | 01 |
| Project | Wireshark SOC Project Module (Extra) |
| Domain | Network Security / SOC Analysis |
| Status | Completed |

## 👤 Author

**Dhargiss V**

B.Tech – Computer Science and Engineering (Cyber Security)

- GitHub: [Dhargiss12](https://github.com/Dhargiss12)
- LinkedIn: [Connect with me](https://www.linkedin.com/)

---

*Learning through practical investigation. Building cybersecurity skills one lab at a time.*
