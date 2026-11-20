# Networkwalks – Week 3: Password Cracking

A hands-on cybersecurity project completed as part of the Networkwalks Cybersecurity Internship.

This repository documents two compulsory Week 3 project modules focused on PDF password recovery using dictionary-based password attacks.

## Project Overview

| Module | Project | Tool |
|---|---|---|
| W3-PM1 | Password Cracking with JTR | John the Ripper |
| W3-PM2 | Password Cracking with NW Tools | Networkwalks Password Cracker |

## Objectives

- Understand how password-protected PDF files are handled.
- Learn the role of password hashes in password recovery.
- Perform dictionary-based password attacks in an authorized lab.
- Use John the Ripper in Kali Linux.
- Explore Networkwalks' browser-based password-cracking tool.
- Compare command-line and web-based workflows.
- Document practical results and technical observations.

## Module 1: Password Cracking with John the Ripper

**Objective:** Extract a password hash from a provided PDF and attempt password recovery using John the Ripper.

**Tools and technologies:**
- Kali Linux
- John the Ripper
- pdf2john
- pyHanko
- Python virtual environment
- RockYou wordlist

**Outcome:** The provided practice PDF password was successfully recovered using a dictionary attack.

[View W3-PM1 documentation](W3-PM1-JTR/README.md)

## Module 2: Password Cracking with Networkwalks Tools

**Objective:** Use the Networkwalks Password Cracker and its associated hash calculator to perform a dictionary-based password attack.

**Tools:**
- Networkwalks Password Cracker
- Networkwalks Hash Calculator
- Built-in password dictionary

**Outcome:** The practice PDF password was successfully recovered, and the first lab flag was captured.

[View W3-PM2 documentation](W3-PM2-Networkwalks-Tools/README.md)

## Skills Practiced

- Password security fundamentals
- PDF hash extraction
- Dictionary attacks
- Linux command-line operations
- Wordlist-based password testing
- Security tool usage
- Technical documentation
- Lab evidence collection

## Lab Environment

| Component | Environment |
|---|---|
| Operating System | Kali Linux 2026.3 |
| Virtualization | Oracle VirtualBox |
| Host Platform | Windows |
| Target | Networkwalks-provided practice PDF files |

## Repository Structure

```text
Week3/
├── README.md
├── W3-PM1-JTR/
│   ├── README.md
│   └── screenshots/
└── W3-PM2-Networkwalks-Tools/
    ├── README.md
    └── screenshots/
```

## Disclaimer

All practical exercises documented here were performed using materials provided for an authorized educational cybersecurity lab.

This repository is intended for learning and documentation purposes. Do not use password-cracking techniques against files or systems without authorization.
