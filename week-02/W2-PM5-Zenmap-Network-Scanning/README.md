
# W2-PM5: Zenmap-Based Network Scanning

**Program:** Networkwalks Cybersecurity Internship  
**Week:** 02  
**Project Module:** W2-PM5  
**Tool:** Zenmap (Nmap GUI)  
**Platform:** Windows

## 1. Objective

To perform network discovery using Zenmap, identify active hosts within an authorized local network, examine available IP and MAC address information, and understand network topology visualization.

## 2. Tools Used

- **Zenmap:** Graphical interface for Nmap.
- **Nmap:** Network scanning and host discovery engine.

## 3. Scan Configuration

| Parameter | Value |
|---|---|
| Target subnet | `10.141.146.0/24` |
| Scan profile | Ping Scan |
| Command | `nmap -sn 10.141.146.0/24` |
| Nmap version | 7.993 |

## 4. Methodology

1. Opened Zenmap on Windows.
2. Entered the target subnet.
3. Selected the Ping Scan profile.
4. Executed the scan.
5. Examined the Nmap output.
6. Identified the discovered active hosts.
7. Reviewed the available MAC address information.

## 5. Scan Results

The scan examined 256 IP addresses and identified two active hosts.

| Parameter | Result |
|---|---|
| Total IP addresses scanned | 256 |
| Live hosts detected | 2 |
| Scan duration | 7.91 seconds |

### Discovered Hosts

| IP Address | Status | MAC Address |
|---|---|---|
| `10.141.146.208` | Up | `16:13:26:A5:95:66` |
| `10.141.146.25` | Up | Not displayed |

**Observation:** The MAC address of the first host was displayed, but its vendor identification was unknown. A MAC address was not reported for the second host.

## 6. Analysis

The Ping Scan successfully identified two responsive hosts within the specified subnet.

The scan demonstrated how Nmap performs host discovery without conducting a port scan. The available MAC address information also helped illustrate device identification at the network level.

## 7. Key Learnings

- Understanding network discovery using Nmap.
- Identifying active hosts within a subnet.
- Understanding IP and MAC addresses.
- Interpreting Zenmap scan output.
- Learning the basics of network topology visualization.

## 8. Evidence

Screenshots of the Zenmap interface, scan output, host details and network topology will be maintained in the `screenshots/` and `reports/` directories.

## 9. Disclaimer

This activity was performed for educational purposes within an authorized network environment. Network scanning should only be conducted on systems and networks for which appropriate permission has been granted.

---

**Networkwalks Cybersecurity Internship | Week 02 | W2-PM5**
