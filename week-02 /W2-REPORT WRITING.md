
# PENETRATION TESTING REPORT
## FOOTPRINTING & NETWORK SCANNING PHASES

**W2-PM-FINAL | CYBERSECURITY | NETWORKWALKS**

| Field | Details |
|---|---|
| Pentester Name (Cybersecurity Professional) | DHARGISS V |
| Program/Batch | B084-Networkwalks |
| Date | 14 November 2026 |
| Modules completed | W2-PM1 (Multiple Kali Tools) / W2-PM5 (Zenmap Scanning) |
| Client/Target | 1. Networkwalks (secured written permission already)  2. My own local LAN Network |
| Permission secured from client? | Yes |
| Phases covered | Phase 1: Reconnaissance & Footprinting / Phase 2: Scanning & Network Discovery / Phase 3-5: In Progress |

---

# 1. Liability Disclaimer

I have performed these activities only on systems and devices for which I had authorization or on devices and networks that I own. All activities documented in this report were conducted for educational and research purposes only.

The tools and techniques described in this report must not be used for unauthorized access, scanning, or testing. The instructor, authors, and Networkwalks are not responsible for any misuse of the information provided. Every action performed using this knowledge is the responsibility of the individual. Unauthorized access to computer systems may result in legal consequences, even when no damage is caused.

---

# 2. Introduction

This report covers footprinting the networkwalks.com domain using multiple Kali Linux tools (W2-PM1) and scanning my own local network using Zenmap (W2-PM5). The first module focuses on collecting publicly available information about a website, while the second module focuses on identifying active hosts within a local network. Together, these activities demonstrate two important stages of a cybersecurity assessment: reconnaissance and network discovery. This report documents the Week 2 practical activities completed as part of my ongoing internship program at Networkwalks.

The footprinting activities were performed using Kali Linux, while network scanning was performed using Zenmap on a Windows PC. Each activity includes the command or procedure followed, the observations obtained from the tool, and supporting screenshots as evidence. The findings are also discussed to understand their relevance from a cybersecurity perspective.

---

# 3. Tools Used

The table below lists each tool used in this report and its purpose.

| Tool | Purpose |
|---|---|
| Kali Linux & Windows | Operating systems used to perform footprinting and network scanning activities. |
| WHOIS | Retrieves domain registration information, including registrar, registration dates, and name servers. |
| whatweb | Identifies website technologies, content management systems, servers, and plugins. |
| nslookup | Resolves a domain name into its corresponding IP address using DNS. |
| curl -I | Retrieves and displays the HTTP response headers of a website. |
| wafw00f | Checks whether a Web Application Firewall is detected on a website. |
| dnsrecon | Collects DNS records such as NS, MX, SPF, TXT, and SRV records. |
| Zenmap (Nmap GUI) | Scans a local subnet to identify active hosts and available IP and MAC address information. |
| Windows CMD | Identifies local network configuration, including IP address, subnet mask, and default gateway. |

---

# 4. Activities Performed

## 4.1 Footprinting & Reconnaissance

I performed reconnaissance against the networkwalks.com domain using six Kali Linux tools: WHOIS, WhatWeb, Nslookup, Curl, Wafw00f, and DNSRecon. Each tool was used to collect a different type of publicly available information about the target domain.

First, I used WHOIS to obtain publicly available domain registration information. This helped me examine details such as the domain registrar, registration information, and name servers associated with the domain.

I then used WhatWeb to identify the technologies used by the website. The tool analyzed the website and provided information about its detectable technologies, content management system, and other web components. The actual technologies and versions identified during the scan are documented in the corresponding output screenshot.

Using Nslookup, I resolved the domain name to its corresponding IP address. This activity helped me understand how DNS translates a human-readable domain name into an IP address used for network communication. The IP address returned by the command is documented in the screenshot.

I used Curl with the -I option to inspect the HTTP response headers returned by the website. This helped me examine the server's HTTP response and identify technical information made available through the response headers.

Next, I used Wafw00f to determine whether a Web Application Firewall could be detected on the target website. This activity helped me understand how security technologies protecting web applications can be identified through reconnaissance.

Finally, I used DNSRecon to enumerate publicly available DNS records. The tool helped me examine DNS information such as name servers, mail servers, and TXT records, providing a better understanding of the domain's DNS infrastructure.

Through these activities, I gained practical experience in using different reconnaissance tools to collect and analyze information about a website. The command outputs and observations are included in the screenshots attached to this report.

## 4.2 Network Scanning with Zenmap

For the second activity, I used Zenmap to perform network discovery on my own local network. The objective was to identify my local IP address and subnet, discover active hosts, and examine the available IP and MAC address information.

I first used the Windows ipconfig command to identify my local network configuration. After identifying the network subnet, I entered it into Zenmap and selected Ping Scan to discover active hosts.

The scan was performed on the following subnet:

**Target Subnet:** 10.141.146.0/24

The scan was executed using Nmap version 7.93 with the command:

```bash
nmap -sn 10.141.146.0/24
```

The scan examined 256 IP addresses and identified two active hosts:

- 10.141.146.208
- 10.141.146.25

The scan results displayed the MAC address 16:13:26:A5:95:66 for the first host. A MAC address was not displayed for the second host in the scan output.

The scan was completed in approximately 7.91 seconds.

This activity helped me understand how Zenmap can be used to identify active devices within a local network. It also provided practical experience in examining network addresses and interpreting host discovery results.

---

# 5. Risk Analysis / Impact

Based on the information collected during the footprinting and network scanning activities, I identified the following potential security considerations.

| # | Risk / Finding | Evidence / Observation | Potential Impact | Risk Level |
|---|---|---|---|---|
| 1 | Web technology information exposed | Information collected using WhatWeb | Publicly visible technology details may help attackers identify components for further security assessment. | ● Medium |
| 2 | Domain IP address identification | DNS resolution performed using Nslookup | Provides information about the IP address associated with the target domain. | ● Low |
| 3 | HTTP technical information exposure | HTTP response headers examined using Curl | May provide technical information that can assist further website reconnaissance. | ● Low |
| 4 | WAF identification | WAF detection checked using Wafw00f | Identifying security technologies may reveal information about the website's security architecture. | ● Low |
| 5 | DNS infrastructure information exposure | DNS records examined using DNSRecon | Public DNS information may help build a profile of the domain's infrastructure. | ● Medium |
| 6 | Multiple active hosts visible on local network | Zenmap identified two active hosts in the scanned subnet | Unknown or unauthorized devices may require verification and monitoring. | ● Medium |

**Risk level key:** ● Critical | ● Medium | ● Low

The findings above represent observations from the footprinting and network scanning activities. They do not confirm the presence of security vulnerabilities.

The practical exercises primarily involved information gathering and host discovery. No exploitation or vulnerability validation was performed as part of these two modules.

Therefore, the presence of information such as website technologies, IP addresses, HTTP headers, or DNS records does not automatically indicate that a system is vulnerable. Further authorized security testing would be required to identify and confirm actual vulnerabilities.

---

# 6. Recommendations

Based on the observations from these activities, I recommend the following security improvements:

1. **Review publicly exposed technology information**

   Organizations should regularly review what information about their web technologies, content management systems, and plugins is publicly visible.

2. **Keep software updated**

   Content management systems, plugins, and other web technologies should be regularly updated and reviewed against current security advisories.

3. **Review HTTP headers**

   HTTP response headers should be reviewed to identify and minimize unnecessary technical information exposed by web servers.

4. **Review DNS records regularly**

   DNS records should be checked periodically to ensure that only required information and services are publicly exposed.

5. **Properly configure and monitor the WAF**

   Web Application Firewalls should be properly configured, regularly updated, and monitored to help detect and mitigate malicious web traffic.

6. **Perform regular internal network discovery**

   Organizations should periodically scan their own networks to identify active devices and maintain awareness of connected systems.

7. **Investigate unknown devices**

   Any unexpected device discovered during network scanning should be investigated and verified by the network administrator.

8. **Maintain network documentation**

   Network topology, IP addresses, and connected device information should be documented and updated regularly.

9. **Perform security testing with authorization**

   Reconnaissance and scanning should only be performed against systems and networks where appropriate authorization has been provided.

---

# 7. Conclusion

During Week 2 of my Cybersecurity and Ethical Hacking internship, I performed practical activities covering footprinting, reconnaissance, and network scanning.

In the footprinting activity, I used six Kali Linux tools: WHOIS, WhatWeb, Nslookup, Curl, Wafw00f, and DNSRecon. I learned how these tools can be used to collect domain registration information, identify website technologies, resolve domain names, inspect HTTP response headers, detect Web Application Firewalls, and examine DNS records.

In the network scanning activity, I used Zenmap to perform a Ping Scan on my own local network. I scanned the subnet 10.141.146.0/24 and identified two active hosts out of 256 IP addresses. I also examined the available IP and MAC address information in the scan results.

These exercises helped me understand the importance of reconnaissance and network discovery in cybersecurity assessments. I learned how publicly available information and network responses can be analyzed to understand a target environment.

I also gained experience in interpreting command outputs, identifying active hosts, and documenting technical observations. The practical activities improved my understanding of footprinting tools, DNS analysis, HTTP information gathering, and network scanning.

Finally, I understood the importance of conducting all cybersecurity activities ethically and within an authorized scope. These activities were completed as part of the assigned educational internship practical exercises.

---

# 8. Evidences Collected

---

## Author

**Dhargiss V**  
Cybersecurity Professional B084  
LinkedIn: https://lnkd.in/p/dubj6Y2M

## Project Information

**Program Name:** Cybersecurity program at Networkwalks | **Week:** 02 | **Repository:** GitHub

---

*Pentesting Project Report | Networkwalks*
