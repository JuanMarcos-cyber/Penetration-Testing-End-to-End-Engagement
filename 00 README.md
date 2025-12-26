# Penetration Testing Lab – End-to-End Assessment

This repository documents a complete end-to-end penetration testing exercise,
covering all phases from pre-engagement to final risk reporting.

The objective of this project is to demonstrate practical penetration testing
skills, structured methodology, evidence-based reporting, and risk-focused
communication aligned with industry standards.

---

## Scope and Objectives

The assessment simulates a real-world web application penetration test with
the following objectives:

- Identify and validate security vulnerabilities
- Demonstrate exploitation and post-exploitation impact
- Assess systemic security weaknesses
- Communicate risk using CVSS v3.1
- Provide actionable remediation guidance

---

## Repository Structure

```text
.
├── screenshots/
├── 00_README.md
├── 01_Pre-engagement.md
├── 02_Info-gathering.md
├── 03_Threat_modelling.md
├── 04_Vulnerability_assessment.md
├── 05_Exploitation.md
├── 06_Post-exploitation.md
└── 07_Reporting.md
```



Each phase builds on the previous one and reflects a standard professional
penetration testing workflow.

---

## Methodology

The assessment follows an industry-aligned penetration testing methodology,
including:

- Pre-engagement and scope definition
- Passive and active reconnaissance
- Threat modeling and attack surface analysis
- Vulnerability identification and validation
- Manual exploitation and attack chaining
- Post-exploitation analysis
- Risk scoring using CVSS v3.1
- Remediation and lessons learned

---

## Key Findings Overview

The assessment identified multiple high and critical vulnerabilities affecting:

- Input validation
- Authentication and session management
- File handling and access control

A particular focus is placed on **weak session identifiers**, which represent
a systemic authentication failure and significantly amplify overall risk.

Detailed findings, exploitation evidence, and CVSS vectors are documented in
Phases 04 through 07.

---

## Tools and Techniques

- Manual testing (Burp Suite Community Edition)
- Directory enumeration (DIRB)
- Web server vulnerability scanning (Nikto)
- Authentication brute-force testing (Hydra)
- Network discovery and port scanning (Nmap)
- Local network and service inspection (netstat)
- WHOIS lookup (whois)
- DNS enumeration and resolution testing (dig)
- HTTP request testing and validation (curl)
- Web technology fingerprinting (WhatWeb)
- Custom payload crafting
- Log analysis and forensic timeline reconstruction
- CVSS v3.1 risk scoring

No fully automated exploitation frameworks were relied upon, reflecting a
realistic attacker workflow.

---

## Reporting and Risk Communication

Phase 07 consolidates all findings into a risk-focused report suitable for
decision-makers, emphasizing:

- Business impact
- CVSS-based prioritization
- Remediation strategy
- Lessons learned

---

---

## ⚠️ Disclaimer

This project was conducted in a **controlled lab environment** for **educational
purposes only**.

All testing activities were **explicitly authorized** and performed against
**intentionally vulnerable systems** designed for security training.

# 🙌 Author

**Juan Marcos Lázaro**  
Cloud Security & GRC Professional  
Miami, FL  
LinkedIn: https://www.linkedin.com/in/juanmarcoslazaro

⚠️ **No real-world systems, networks, or user data were targeted or impacted
during this assessment.**

---

