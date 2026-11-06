# Week 01 – Extra: Cybersecurity Lab Environment Setup

<p align="left">
  <img src="https://img.shields.io/badge/Networkwalks-Cybersecurity%20Internship-blue?style=for-the-badge" alt="Networkwalks" />
  <img src="https://img.shields.io/badge/VirtualBox-Hypervisor-183A61?style=for-the-badge&logo=virtualbox&logoColor=white" alt="VirtualBox" />
  <img src="https://img.shields.io/badge/Kali_Linux-Security_OS-557C94?style=for-the-badge&logo=kalilinux&logoColor=white" alt="Kali Linux" />
  <img src="https://img.shields.io/badge/Focus-Lab%20Setup-red?style=for-the-badge" alt="Lab Setup" />
  <img src="https://img.shields.io/badge/Status-Ongoing-orange?style=for-the-badge" alt="Ongoing" />
</p>

## 📌 Project Overview

As an additional practical activity during Week 01 of my Cybersecurity Internship at **Networkwalks Pvt. Ltd.**, I worked on building an isolated virtual cybersecurity laboratory using Oracle VirtualBox and Kali Linux.

The objective was to establish a controlled environment for cybersecurity practice, network reconnaissance, port scanning, vulnerability assessment, and future penetration-testing exercises.

The project involved configuring virtual machines, exploring virtual networking modes, verifying IPv4 connectivity, troubleshooting network issues, and preparing a clean virtual machine environment.

## 🎯 Objectives

- Install and configure Oracle VirtualBox.
- Set up Kali Linux as a virtual machine.
- Understand NAT, NAT Network, and Host-Only networking.
- Configure virtual network adapters.
- Inspect IPv4 addressing and routing.
- Verify network connectivity and DNS resolution.
- Create virtual machine snapshots.
- Document laboratory configuration and troubleshooting.

## 🛠️ Tools & Technologies

| Tool | Purpose |
|---|---|
| Oracle VirtualBox | Virtual machine management |
| Kali Linux | Security testing environment |
| Windows 11 | Host operating system |
| 7-Zip | Archive extraction |
| Nmap | Network scanning |
| Wireshark | Network packet analysis |
| TCP/IP | Network communication |

## ⚙️ Lab Configuration

| Component | Configuration |
|---|---|
| Host OS | Windows 11 |
| Host RAM | 16 GB |
| Processor | Intel Core i5-1334U |
| Hypervisor | Oracle VirtualBox |
| Security OS | Kali Linux |
| Kali RAM | 4096 MB |
| Kali CPU | 2 CPUs |
| Virtual Networking | NAT / Host-Only |
| IP Configuration | DHCP / Static IPv4 |

## 🪜 Implementation Steps

### 01. Install 7-Zip

Installed 7-Zip to extract compressed virtual machine packages.

Download: https://www.7-zip.org/

### 02. Install Oracle VirtualBox

Installed Oracle VirtualBox to create and manage virtual machines.

Download: https://www.virtualbox.org/wiki/Downloads

### 03. Configure Virtual Networking

Explored the different VirtualBox networking modes.

| Network Mode | Description |
|---|---|
| NAT | Provides external network access to a VM |
| NAT Network | Allows connected VMs to communicate and access external networks |
| Host-Only | Enables private communication between the host and VMs |
| Bridged Adapter | Connects a VM directly to the physical network |

### 04. Install Kali Linux

Downloaded and configured Kali Linux as a virtual machine.

Configuration:
- RAM: 4096 MB
- CPU: 2 cores
- Network Adapter: NAT
- Operating System: Kali Linux

Download: https://www.kali.org/get-kali/

### 05. Configure Kali Linux Networking

Used Linux networking commands to inspect the network configuration.

**IP Address:**
```bash
ip addr
```

**Network Interfaces:**
```bash
ip link
```

**Routing Table:**
```bash
ip route
```

**DNS Configuration:**
```bash
cat /etc/resolv.conf
```

### 06. Verify Network Connectivity

Performed connectivity and DNS resolution checks.

**Gateway Connectivity:**
```bash
ping -c 4 <GATEWAY_IP>
```

**Internet Connectivity:**
```bash
ping -c 4 8.8.8.8
```

**DNS Resolution:**
```bash
nslookup google.com
```

### 07. Create a Virtual Machine Snapshot

Created a recovery point after the initial Kali Linux configuration.

Example snapshot name:

```text
Kali-Linux-Initial-Setup
```

This provides a way to restore the virtual machine to a previous working configuration before performing further experiments.

## 🔎 Lab Verification

| Test | Command | Purpose |
|---|---|---|
| IP Address | `ip addr` | Inspect assigned IP |
| Network Interface | `ip link` | Check interface status |
| Routing | `ip route` | Inspect routing information |
| Gateway | `ping -c 4 <GATEWAY_IP>` | Test gateway connectivity |
| Internet | `ping -c 4 8.8.8.8` | Test external connectivity |
| DNS | `nslookup google.com` | Verify DNS resolution |
| Nmap | `nmap --version` | Verify Nmap installation |

## 🐞 Problems Encountered & Troubleshooting

### 01. Kali Linux Network Connectivity

**Issue:** Network connectivity was unavailable after changing VirtualBox network adapter settings.

**Troubleshooting:**
- Checked VirtualBox network adapter configuration.
- Verified virtual network cable connection.
- Inspected interfaces using `ip link`.
- Checked IP addressing and routing.
- Restarted the network connection when required.

### 02. Kali Linux Startup Issue

**Issue:** The graphical desktop did not load correctly during virtual machine startup.

**Troubleshooting:**
- Checked virtual machine resource allocation.
- Reviewed VirtualBox configuration.
- Performed a complete power-off and restart.
- Verified virtual machine startup.

**Result:** The graphical desktop loaded successfully after restarting the virtual machine.

## 💡 Key Learnings

- Understanding VirtualBox virtualization and virtual machine configuration.
- Comparing NAT, NAT Network, and Host-Only networking.
- Understanding IPv4 addressing, gateways, and DNS.
- Practicing Linux network troubleshooting commands.
- Verifying connectivity and routing.
- Understanding virtual machine snapshots and recovery.
- Building a foundation for practical cybersecurity exercises.

## 🔐 Security & Ethical Use

This laboratory is intended for educational purposes and authorized cybersecurity testing.

All scanning, reconnaissance, vulnerability assessment, and testing activities must be restricted to systems owned by me or systems for which explicit permission has been granted.

## 🔗 Tools & Resources

- [7-Zip](https://www.7-zip.org/)
- [Oracle VirtualBox](https://www.virtualbox.org/wiki/Downloads)
- [Kali Linux](https://www.kali.org/get-kali/)
- [Nmap](https://nmap.org/)
- [Wireshark](https://www.wireshark.org/)

## 🏢 Internship Information

| Field | Details |
|---|---|
| Organization | Networkwalks Pvt. Ltd. |
| Program | Cybersecurity Internship |
| Week | 01 – Extra |
| Project | Cybersecurity Lab Environment Setup |
| Domain | Cybersecurity / Virtualization / Networking |
| Hypervisor | Oracle VirtualBox |
| Operating System | Kali Linux |
| Status | Completed |

## 👤 Author

**Dhargiss V**

B.Tech – Computer Science and Engineering (Cyber Security)

- GitHub: [Dhargiss12](https://github.com/Dhargiss12)
- LinkedIn: [Connect with me](https://www.linkedin.com/)

---

*Building a practical cybersecurity foundation through virtualization, Linux, networking, and hands-on experimentation.*
